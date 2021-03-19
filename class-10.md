# Debugging
<!-- All info from Duckett JS book-->

> JavaScript can be hard to learn and everyone makes mistakes when writing it.

## Common Problems
- Order of execution - you have to make sure things can run before you call them and the order of operations is imperative to keep in mind.

### The STACK
> The JavaScript interpreter processes one line of code at a time. When a statement needs data from another function, it stacks (or piles) the new function on top of the current task.

```
function greetUser {
    return 'Hello ' + getName();
}
function getName() {
    let name = 'Hunter';
    return name;
}
let greeting = greetUser();
alert(greeting);
```

- In this case the alert you would see is "Hello Hunter"
- Prepare your content and then Execute it

#### Error objects
- name - type of execution
- message - description
- fileNumber - name of the js file
- lineNumber - line number of error
- Error - generic error - the other errors are all based on this error
- SyntaxError - syntax has not been followed
- ReferenceError - tried to reference a variable that is not declared/within scope
- TypeError - An unexpected data type that cannot be coerced
- RangeError - numbers not in acceptable range
- URIError - encodeURI (), decodeURI(), and similar methods used incorrectly
- EvalError - eval() function used incorrectly

## Handling Errors

#### Dealing with errors/A debugging workflow
1. Debug the script to fix errors
2. Handle errors gracefully
3. Where is the problem?
   - Read the error
   - How far is the script running?
   - Use breakpoints where things are going wrong.
4. What exactly is the problem?
   - Break down the code into smaller pieces
   - Check the number of parameters for a function or the number of items in an array
   - Repeat the process as necessary

##### In totality/keys
- debugger keyword
- breakpoints - Chrome - sources option, then select the script you are working with.
- conditional breakpoints - right click and select Add Conditional Breakpoing in Chrome.
- Some problems are browser specific
- If you understand execution contexts (which have two stages) and stacks, you are more likely to find the error in your code
- Debugging is the process of finding errors. It involves a process of deduction
- The console helps narrow down the area in which the error is located, so you can try to find the exact error.
- JavaScript has 7 different types of errors. Each creates its own error object, which can tell you its line number and gives a description of the error.
- If you know that you may get an error you can handle it gracefully using the try, catch, finally statements. Use them to give your users helpful feedback.


[<== Back](README.md)