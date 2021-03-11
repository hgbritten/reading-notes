# HTML Links, JS Functions, and Intro to CSS Layout
<!-- Info gained from Duckett HTML and JS books-->
## Links
> Links are a defining feature of the web because they allow you to move from one web page to another

### Common types of links
- Links from one website to another
- From one page to another
- One part of a page to another part of the same page
- Links that open a new browser window
- ect.

### Writing links
- Links in html are created using the `<a>` element. 
- You specify the page you want to link to using the href attribute on the a tag like the following.

```
<a href="http://www.imdb.com">IMDB</a>
```

- The a href is the opening tag and the `</a>` is the closing link tag
- This link will show up as IMDB as a clickable link because it is what is between the link tags
- When linking it is important to know which folder the file you are trying to reach lives in. We have experienced this many times in 201 so far.
- If you are linking to your own site it is best to use relative links rather than qualified URLs.
- Using id attributes can target specific elements to link to on your page.

## Layout
- Where does each element sit on a page? How do we create attractive layouts?
  
### Block level elements vs Inline
- Block-level boxes start on a new line and act as the main building blocks of any layout, while inline elements flow between surrounding text.

- Block elements are h1 p ul li
- Inline are img b i

### Containing elements just means if a block-level is inside another block-level then the one containing the other is a containing element.

### Controlling Position of Elements
- Normal flow - every block just goes in a top down order.
- Relative positioning - moves an element from the position it would normally be in a direction based on the surrounding elements.
- Absolute positioning - An element that has no effect on other blocks.
- Fixed positioning - form of absolute in relation to the browser window.
- Floating elements - can be tucked arounf other block level elements (good example is a picture)

## Functions, Methods, and Objects
- Functions: consist of a series of statements that have been grouped together because they perform a specific task. Methods are the same they are just part of objects
- Objects: Made up of properties and methods.

```
function sayHello() {
    document.write('Hello!');
}
```

- Declaring a function begins by using the function keyword.
- You can name the fuction whatever you like followed by the () 
- The "code block" is after that contained in the squiggly braces.
- now you have made a function named sayHello that can be called on later with sayHello(); and it will perform document.write('Hello!');

### Functions that need info are a little bit different.

```
function getArea(width, height) {
    return width * height;
}
```

- To be frank I am still unsure how this would work in actual code. Does it give the dimensions of the property it is called to?

## 6 Reasons for Pair Programming
- Pair programming works in pairs. One driver and one Navigator. Much like racing.
- The driver is the one stroking the keys and the navigator is letting the driver know what is next.
- Pair programming can help teach more skills in the development world.

### Some Bennys!
1. Greater efficiency
2. Engaged collaboration
3. Learning from fellow students
4. Social skills
5. Job interview readiness - this one is great because you really have to be able to articulate what you are thinking. Your brain can think in code, but can you speak it? Speaking code is much more attractive to prospective employers
6. Work environment readiness - companies use pair programming and thats why Code Fellows does as well.

[<== Back](README.md)