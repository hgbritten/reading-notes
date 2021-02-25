# Dynamic web pages with JavaScript

## How HTML, CSS, & JavaScript fit together

### HTML is the content layer made up of everything your webpage says

### CSS is the presentation layer which decides how that content is presented

### JavaScript is the behavior layer which decides how the page behaves. Try to keep js in its own separate file.

## JavaScript is written in plain text just like HTML and CSS
    > JavaScript can take a simple greeting like "Welcome" and cater it to the person who is visiting your site or even the time of day that it is.

### Linking your js files to your index.html is essential if you want it to have any effect on your page. 
    - To do this make sure your index.html and you .js file are in the same location or that you include navigation in your command that should look something like this: <script src="js/add-content.js"><script>
    - That line should be included somewhere near the bottom of the </body> of your html code
    - You can also if needed add JavaScript directly into your HTML file like <script>document.write('<h3>Welcome!<h3>');</script>

## How do you use objects and methods?

### Objects are what/where you want to change things. Is it the document? Great! Start off with document

### Methods are how you want to change things. Do you want to write something? continue with write()
    > This is all surface level stuff. The browser uses quite a bit more code to make the words appear on the screen than just what we write. We are basically plugging digits into a calculator and it is giving us the answer

### JavaScript is found in the HTML
    - Did you place the <script> below the <p>? That is where it will show up!
    - This can also affect the loading times of webpages

## Basics of JavaScript

### Statements
    - A script is a series of instructions that a computer can follow one-by-one and each individual step is called a statement
    - Statements should end in a semicolon
    - A statement is something like "greeting" and a code block can contain them in {} curly braces
    - Statements are instructions and each one begins on a new line

### Comments
    - Comments can be included to help tell people looking at it what the code does. However, this can't be seen on the front facing website.
    - To execute a multi-line comment use the /* */ characters and put your comment between them.
    - To execute a single-line comment use // on a line that will not be processed by JavaScript and include your comment after.

### Variables
    > A script will have to temporarily store the bits of information it needs to do its job. It can store this data in **variables**.
