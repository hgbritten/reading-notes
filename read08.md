# Operators and Loops

## Comparison and logical operators
- BOOLEANS! You can evaluate a situation by comparing one value in your script to what you expect it might be. If you are trying to find answers to things this is a great tool!
- `==` is equal to 
- `!=` is not equal to
- `===` is a strict equal to and will check that both the data _type_ and the **value** are the same.
- `!==` is a strict not equal to where only one of the data type or value can be false to make the statement true
- The rest of the mathematical symbols `> < >= <=` work like they normally would in math

### Logical operators allow you to compare the results of more than one comparison operator. Logical operators need both comparison operators to return true or it evaluates to false.
- `&& tests more than one condition` = Logical And / if either return false this is false
- `|| tests at least one condition` = Logical Or / if either return true this is true
- `! takes a single Boolean value and inverts it` = Logical Not / if true, false / if false, true

## Using While Loops
- while is a function that will continue to run for as long as the condition in the parentheses is true.
    > `for (var i = 0; i < 10; i++) {
        document.write(i);
    }`

- The first time a loop is run the i value is assigned the value of 0.
- Variable i can be used inside the loop. In the above it is used to write a number to the page. During a loop when the statements have finished, the variable is incremented by 1. This is indicated via the i++ code
- The var i = 0 creates the variable
- The i < 10; sets the condition of the counter to count until the i value is no longer less than 10
- i++ every time the loop is run the i value will increase by 1.

## For is used to run a code a specific number of times. While is used if you don't know how many times the code needs to be run. Do while is similar to the while loop, but it will always run and give a statement at least once even if the condition evaluates to false.
<!-- All informtion gathered from Duckett: JavaScript & jQuery-->

[<== Back](README.md)