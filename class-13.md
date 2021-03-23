# The Past, Present & Future of Local Storage For Web Applicatoins

<!--All info taken from http://diveinto.html5doctor.com/storage.html -->

## Things to know
- Cookies were used for persistent local storage of small amounts of data. But They have down sides.
  - Cookies are in every HTTP request, which slows down your web app by transmitting the same data over and oever
  - Cookies send data unencrypted over the internet (usually)
  - Cookies are limited to 4KB of data - enough to slow you down, but not enough to help.

### Goals
- A lot of storage space
- on the client
- that persists beyond a page refresh
- and isn't transmitted to the server

#### History lesson
- Multiple iterations from userData to Flash 6 to Dojo Toolkit
- The pattern - all solutions are specific to a single browser or reliant on a third party plugin - enter HTML5. Porviding a standardized API without having to rely on plugins.

## HTML5 Storage
- persistent local storage
- available even when third-party browser plugins are not.

### Support
- IE 8.0+
- Firefox 3.5+
- Safari 4.0+
- Chrome 4.0+
- Opera 10.5+
- Iphone 2.0+
- Android 2.0+


#### Checking for Storage / detecting

```

function supports_html5_storage() {
    try {
        return 'localStorage' in window && window['localStorage'] !== null;
    } catch (e) {
        return false;
    }
}

```

##### Or use Modernizr

```

if (Modernizr.localStorage) {
} else {
}


```


## Using HTML5 Storage
- based on key/value pairs
  - you store data based on a named key and then you can retrieve that data with the same key.
  - The named key is a string and the data type can be any supported by JavaScript, including
    - strings
    - Booleans
    - integers
    - floats
  - data is stored as a string
  - If you are storing data you need to retrieve it with functions like parseInt() or parseFloat() to get the data type needed

```

interface Storage {
    getter any getItem(in DOMString key);
    setter creator void setItem(in DOMString key, in any data);
};

```

- calling setItem() with a named key that already exists will silently overwrite the previous value. Calling getItem() with a non-existent key will return null rather than throw an exception.
- In JS you can treat localStorage the object as an associative array. Instead of using getItem or setItem methods you can use square brackets:

```

let foo = localStorage.getItem("bar");
//
localStorage.setItem("bar", foo);

as

let foo = localStorage["bar"];
//
localStorage["bar"] = foo;

```

- To remove values from a key and clearing storage area

```

interface Storage {
    deleter void removeItem(in DOMString key);
    void clear();
}

```

- calling removeItem() with a non-existent key will do nothing

### Tracking Changes to Storage Area
- storage event is not cancellable

### Limitations in current browsers
- 5 megabytes - your storage total
- QUOTA_EXCEEDED_ERR - you stored too much
- no - no you can't have more storage

### In action
- You can save progress locally in browsers like in a game. 

```

function saveGameState() {
    if (!supportsLocalStorage()) { return false; }
    localStorage["halma.game.in.progress"] = gGameInProgress;
    for (let i = 0; i < kNumPieces; i++) {
        localStorage["halma.piece." + i + ".row"] = gPieces[i].row;
        localStorage["halma.piece." + i + ".column"] = gPieces[i].column;       
    }
    localStorage["halma.selectedpiece"] = gSelectedPieceIndex;
    localStorage["halma.selectedpiecehasmoved"] = gSelectedPieceHasMoved;
    localStorage["halma.movecount"] = gMSoveCount;
    return true;
}

```

- This data is stored as a string

[<== Back](README.md)
