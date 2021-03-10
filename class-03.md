<!--Some of these notes come from my previous notes taken in 102 and form the John Ducket HTML and JavaScript books-->

# HTML Lists, Control Flow with JS, and the CSS Box Model

## Lists
- There are many types of lists such as ordered, unordered, and definition lists.


```
<ol> is an ordered list
<li> is a list item
<ul> is an unordered list
<dl> is a definition list
<dt> is used to contain the term being defined
<dd> is used to contain the definition
```

## Boxes
- Boxes have quite a few functions
  - from size to borders to margins and padding to displaying and hiding them.
- All aspects of boxes are controlled in the CSS file by calling out the elements they are being used for 
- Percentages are better to use because they change based on the size of the browser ***THIS WOULD HAVE BEEN GREAT TO KNOW BEFORE SUBMITTING TODAYS LAB***
- You can also place limits on boxes for minmum and maximum height and width so they look the same across platforms.
- Border, margin, and padding are a part of every box.
  - Border is the outside of the box which is not always visible
  - Margin sits outside the edge of the border keeping the box away from other things
  - Padding is the space between the border of a box and any content in that box
- The code could look like something as simple as this:


```
p.one {
    border-color: #0088dd:
}

This can also go in an order of top right bottom left as follows

p.two {
    border-color: #bbbbaa #111111 #ee3e80 #0088dd:
}

```


<!-- https://www.geeksforgeeks.org/decision-making-javaif-else-switch-break-continue-jump/#switch-case helped me with the definition -->
## Decisions and Loops "switch statements"
- "The switch statement is a multiway branch statement. It provides an easy way to dispatch execution to different parts of code base on the value of the expression.

```
switch(expression)
{
    case value1:
        statement1;
        break;
    case value2:
        statementN;
        break;
    .
    .
    case valueN:
        statementN;
        break;
    default:
        statementDefault;
}
```

- This kind of code helps you break up your code into a nice sort of flow chart. 

}


[<== Back](README.md)