# Programming with JavaScript

## Intro + Scripts
- JavaScript helps you to make web pages more interactive by letting you access the content, modify that content, program rules for that content and react to events triggered by the user or browser

#### An example of this might be a slide show that goes something like this
- React: Script triggered when the page loads
- Access: Get each slide from the slideshow
- Modify: Only show the first slide `(hide others)`
- Program: Set a timer: when to show next slide
- Modify: Change which slide is shown
- React: When user clicks button for different slide
- Program: Determine which slide to show
- Modify: Show requested slide

##### Other examples are filling out forms, reloading parts of a page, and filtering data

##### Not all versions of browsers react the same way to JavaScript and that will need to be accounted for when writting your code

### The ABC of Programming
- What is a script and how do I create one?
- How do computers fit in with the world around them?
- How do I write a script for a webpage?

### What is a script and how do you create one?
- A script is a series of instructions that a computer can follow to achieve a goal.
- The computer will follow these step by step in the order the code has laid out to perform the appropriate actions
- The scripts can also run different pieces of itself depending on the situations `(if this then this)`
- To write a script you need to state your intended goal and then list the tasks that need to be completed in order to achieve it.
- Humans think differently than computers and thus we can access certain information almost instantly that it might take lines of code and instructions for a computer to get correct.
- We need to be able to see the pathway the computer will have to take to get the same information to write the proper script.

#### Define a goal, design the script, code each step
- Give the computer a puzzle to solve, split the goal into a series of tasks that will be involved in solving the puzzle, convert those tasks into JavaScript the computer can understand.

#### Vocabulary and Syntax knowledge are essential to convert your steps into code
- Vocabulary: The words that computers understand
- Syntax: How you put those words together to create instructions computers can follow
- Computers are logical and obedient and will need to be told absolutely every detail of the path they are to follow to do what they are expected to do. If you want to get a certain result you need to make sure all your bases are covered by your code so that the computer does not get lost along the way.

#### Thinking like a computer is essential to understanding how you need to write code
- Stop thinking like a human because we solve problems differently and access information completely differently than a computer.

#### Flowcharts can be very helpful for understanding the process of a computer and what steps you will need to go through to get the desired results.

## Expressions

### Expressions come in two forms
- A single value
- Two or more values that return a single value

### Operators are essential for expressions and they allow programmers to create a single value from one or more values
- `+` adds one value to another
- `-` subtracts one value from another
- `/` divides
- `*` multiplies
- `++` adds one to the current number also known as increments
- `--` does the opposite
- `%` is modulus and divides two values and returns a remainder

#### Order of execution is much like normal math where multiplication and divison are preformed before addition and subtraction `(think PEMDAS)`

## What is a function?

### Functions group statements together to perform a specific task. If different parts of a script repeat the same task, you can reuse the function `(rather than repeating the same set of statements)`.

### Declaring a function
- To create a function, you give it a name and then write the statements needed to achieve its task inside the curly braces. This is known as a function declaration.
- Functions store the code required to perform a specific task and the script can ask the function to perform that task whenever needed.

### Calling a function
- To run a code in the function you have to use the function name followed by `()`
- Declare functions before calling them for now

### Declaring functions that need information
- ***If a function needs information to work, you indicate what it needs to know in parentheses after the function name!***
    > function getArea(width, height) {
        return width * height;
    }
- It is like a math problem!
- ***When you design a script, you need to note the information the function will require in order to preform its task*** or else it won't work

### Values vs Variables
    - wallWiidth = 3; 
    - WallHeight = 5; 
    - getArea(wallWidth, wallHeight);

- Values would be `getArea(3,5);` and that will always return those numbers.
- If they need to be calculated you would use variables like the one shown above


### Getting a single value out of a function 
    > function calculateArea(width, height) {
        var area = width * height;
        return area;
    }
    var wallOne = calculateArea(3, 5);
    var wallTwo = calculateArea(8, 5);
- This demonstrated how the same functions can be used to perform the same steps with different values

### Getting multiple values out of a function
    > function getSize(width, height, depth) {
        var area = width * height;
        var volume = width * height * depth;
        var size = [area, volume]:
        return sizes;
    }
    var areaOne = getSize(3, 2, 3)[0];
    var volumeOne = getSize(3, 2, 3)[1];

### Function Declaration vs Expression
- A function declaration creates a function that you can call on later in your code
- A function expression calls on that declaration


###### Examples and information taken from Duckett: JavaScript & jQuery

[<== Back](README.md)