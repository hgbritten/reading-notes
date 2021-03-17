# Layout - Recap
<!-- all notes from Duckett HTML/CSS book-->

## Controlling the position of elements
- CSS treats each HTML element as if it is in its own box. This box will either be a block leve box or an inline box.
- block levels start their own new line and inline goes along the same level in a line.
- Containing elements are block-level elements that contain other block-levels.
- Relative positioning moves things from where they would normally be
- Absolute positioning sticks things on the page not to move. Fixed is like this
- Floating an element allows you to take that element out of normal flow and positions it to the left or right of a containing box and it becomes its own block-level.
- The ***z-index*** property allows you to control which box appears on top.

## Creating site layouts - w/ examples
- position: absolute;
- position: relative;
- width: 
- position: fixed;
- z-inded: 10;
- float: right(or left);
- 

## Designing for different sized screens
- fixed width layouts!
- Liquid layouts! - uses percentages to speicify the width of each box so that the design will stretch to fit the size of the screen.

```
#nav {
    margin: 1%;
    .column1, .column2, .column3 {
        width: 31.3%;
        float: left;
        margin: 1%;
    }
}
```


[<== Back](README.md)