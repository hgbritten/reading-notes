# Object-Oriented Programming, HTML Tables

<!-- notes taken from Duckett Js and HTML books and https://github.com/codefellows/domain_modeling#domain-modeling -->

## Domain Modeling
> Domain modeling is the process of creating a conceptual model in codee for a specific problem.
> An entity that stores data in properties and encapsulates behaviors in methods is commonly referred to as an object -oriented model.

- A domain model is a communication tool. It helps outline the problem the team is facing.

### EpicFailVideo
- While coding we made epicFailVideo a variable then assigned a function with the two parameters epicRating and hasAnimals.

```

let epicFailVideo = function(epicRating, hasAnimals) {
  this.epicRating = epicRating;
  this.hasAnimals = hasAnimals;
}

let parkourFail = new epicFailVideo(7, false);
let corgiFail = new epicFailVideo(4, true);

console.log(parkourFail);
console.log(corgiFail);

```

> This is object-oriented programming in JavaScript at its most fundamental level.
1. The `new` keyword creates an object
2. the constructor function initializes the properties inside that object using the `this` variable.
3. The object is stored in a variable for later use

### Generate Random Numbers

```

let epicFailVideo = function(epicRating, hasAnimals) {
  this.epicRating = epicRating;
  this.hasAnimals = hasAnimals;
}
epicFailVideo.prototype.generateRandom = function(min, max) {
  return Math.floor(Math.random() * (max - min + 1)) + min;
}
let parkourFail = new epicFailVideo(7, false);
let corgiFail = new epicFailVideo(4, true);

console.log(parkourFail.generateRandom(1,5));
console.log(corgiFail.generateRandom(1,5));

```

- In this section we add a random number generator and as you can see we used dot to pass through arguements 1 and 5 to be min and max on the random number generator.
- Prototype being added is a best practice and helps things run faster when they are sharing the same code.

### Daily Likes

```

let epicFailVideo = function(epicRating, hasAnimals) {
  this.epicRating = epicRating;
  this.hasAnimals = hasAnimals;
}
epicFailVideo.prototype.generateRandom = function(min, max) {
  return Math.floor(Math.random() * (max - min + 1)) + min;
}

epicFailVideo.prototype.dailyLikes = function() {
  let viewers, percentage;
  viewers = this.generateRandom(10, 30) * this.epicRating;
  if (this.hasAnimals) {
    percentage = 0.75;
  } else {
    percentage = 0.40;
  }
  return Math.round(viewers * percentage);
}

let parkourFail = new epicFailVideo(7, false);
let corgiFail = new epicFailVideo(4, true);

console.log(parkourFail.dailyLikes());
console.log(corgiFail.dailyLikes());

```

- In this section you can see that we created a function that calculates the percentage of likes with some more math involved.
- This helped us return bigger random numbers with the console log. 

- I am still not sure how this. works

### Weekly Likes


```

let epicFailVideo = function(epicRating, hasAnimals) {
  this.epicRating = epicRating;
  this.hasAnimals = hasAnimals;
}
epicFailVideo.prototype.generateRandom = function(min, max) {
  return Math.floor(Math.random() * (max - min + 1)) + min;
}

epicFailVideo.prototype.dailyLikes = function() {
  let viewers, percentage;
  viewers = this.generateRandom(10, 30) * this.epicRating;
  if (this.hasAnimals) {
    percentage = 0.75;
  } else {
    percentage = 0.40;
  }
  return Math.round(viewers * percentage);
}

epicFailVideo.prototype.weeklyLikes = function() {
  let total = 0
  for (let i = 0; i < 7; i +=1){
    total += this.dailyLikes();
  }
  return total;
}

let parkourFail = new epicFailVideo(7, false);
let corgiFail = new epicFailVideo(4, true);

console.log(parkourFail.weeklyLikes());
console.log(corgiFail.weeklyLikes());

```

- In this example code you can see that I took the dailyLikes generator and used it inside of a for loop in a new function to do that math 7 times to get the amount for a whole week.

### Summation
1. When modeling a single entity that will have many instances, build self-contained objects with the same attributes and behaviors.
2. Model its attributes with a constructor function that defines and initializes properties.
3. Model its behaviors with small methods that focus on doing one job well.
4. Create instances using the `new` keyword followed by a call to a constructor function.
5. Store the newly created object in a variable so you can access its properties and methods from **outside**.
6. Use the `this` variable within methods so you can access the object's properties and methods from **inside**.

## This was all fantastic information that I didn't know how to not just rewrite because everything seemed so cut and dry. 


### Tables
- Basic Table Structure:
    1. table - used to create a table
    2. tr - each new row
    3. td - each value on the row (so one tr tag is usually followed by many td tags)
    4. th - used like td but it is supposed to be the heading for each column or row
    5. colspan="#" and rowspan="#" span the number of columns or rows specified and are included in the element as an attribute
    6. thead is the heading 
    7. tbody is the body
    8. tfoot is the foot (can be used for totals and such, use these three in longer tables)
    9. bgcolor can add in background colors to boxes

### Functions, Methods, and Objects


```

let hotel = new Object();

hotel.name = 'Park';
hotel.rooms = 120;
hotel.booked = 7;
hotel.checkAvailability = function() {
  return this.rooms - this.booked;
}

let elName = document.getElementById('hotelName');
elName.textContent = hotel.name;

let elRooms = document.getElementById('rooms');
elRooms.textContent = hotel.checkAvailability();

```

- In this example given the object is the hotel
- The key is the name/rooms/booked/checkAvailability
- And the value is after the = sign
- The checkAvailability is a method while Park/120/77 are all properties.
- things can be deleted with delete. if they need to be overwritten but not lost.

#### This is used mostly inside functions and objects. Where the function is declared alters what **this** means.
- When a function is defined inside an object is becomes a method and then **this** refers to the containing object. So whatever it is inside.

### Arrays are Objects

### Simple data types
1. String
2. Number
3. Boolean
4. Undefined
5. Null

### Complex Data types
- Objects (arrays and functions)

[<== Back](README.md)