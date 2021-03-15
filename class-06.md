# Problem Domain, Objects, and the DOM

<!-- Notes from JS Duckett book and https://simpleprogrammer.com/understanding-the-problem-domain-is-the-hardest-part-of-programming-->

## Understanding The Problem Domain Is The Hardest Part Of Programming
- When learning to code the hardest thing to do is know what you need to build to get the answer you want. If you are learning that and you are learning how to code in the first place it will take you a lot longer. It is better to be able to focus on one section of learning at once.

## Objects
> Objects group together a set of variables and functions to create a model of a something you would recognize from the real world. In an object, variables and functions take on new names.

### In an Object, variables become known as properties and functions become known as methods
- Properties tell us about the object, such as the name of a hotel or the number of rooms it has. 

```
let hotel = {
    name: 'Quay',
    rooms: 40,
    booked: 25,
    gym: true,
    roomTypes: ['twin', 'double', 'suite'],
    checkAvailability: function() {
        return this.rooms - this.booked;
    }
}
```

- As you can see in the example above the variables name, rooms, booked, ect. are properties of the hotel. The function checkAvailability becomes a method to determining something for the hotel.
- You can access the property or method of an object using dot notation or square brackets.

```
let hotelName = hotel.name;
let hotelName = hotel['name'];
```

- The period is the member operator. Properties can also be accessed with the square bracket syntax, but methods of an object cannot be. 

### Documents Object Model
#### Methods that select individual elements
- getElementById() and querySelector() can both search an entire document and returnh individual elements.

- getElements can let you select by the tags like h1 or li. The querySelector can select things by their id.


[<== Back](README.md)