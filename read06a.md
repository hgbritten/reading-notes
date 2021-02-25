# Dynamic web pages with JavaScript

## How HTML, CSS, & JavaScript fit together

### HTML is the content layer made up of everything your webpage says

### CSS is the presentation layer which decides how that content is presented

### JavaScript is the behavior layer which decides how the page behaves. Try to keep js in its own separate file.

## JavaScript is written in plain text just like HTML and CSS
- JavaScript can take a simple greeting like "Welcome" and cater it to the person who is visiting your site or even the time of day that it is.

### Linking your js files to your index.html is essential if you want it to have any effect on your page. 
- To do this make sure your index.html and you .js file are in the same location or that you include navigation in your command that should look something like this: `<script src="js/add-content.js"><script>`
 - That line should be included somewhere near the bottom of the `</body>` of your html code
 - You can also if needed add JavaScript directly into your HTML file like `<script>document.write('<h3>Welcome!<h3>');</script>`

## How do you use objects and methods?

### Objects are what/where you want to change things. Is it the document? Great! Start off with document

### Methods are how you want to change things. Do you want to write something? continue with write()
  - This is all surface level stuff. The browser uses quite a bit more code to make the words appear on the screen than just what we write. We are basically plugging digits into a calculator and it is giving us the answer

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
- A script will have to temporarily store the bits of information it needs to do its job. It can store this data in **variables**.
- Variables are just that: variable. They can change each time the script runs. The results have to be calculated
- You can think of it as width x height 

#### Declaring Variables
- Before you can use a variable, you need to announce that you want to use it. This involves creating the variable and giving it a name. Programmers say that you **declare** the variable.
- This is achieved by stating a variable key word like var or let followed by a variable name such a quantity ending in a ;
- camelCase is used when the variable name is more than one work such as userName. It states that the first word is lower case and the second word starts as uppercase and they are stuck together.

#### Assigning Variables
- Once you create a varaible you need to assign it a value `(eg: quantity = 3)`


### Data Types
- Numeric Data, String Data, and Boolean Data
- Numeric is used for tasks that involve counting
- String is usually consists of letters and other special characters
- Boolean data can only have two values: true or false

### Rules for naming
1. Name must begin with a letter, dolar sign ($), or an underscore (_). It must not start with a number.
2. The name can contain letters, number, dollar sign ($), or an underscore (_). Note that you must not use a dash (-) or a period (.) in a variable name.
3.  You cannot use **keywords** or **reserved** words. Keywords are special words that tell the interpreter to do something. For example, var is a keyword used to declare a variable. Reserved words are ones that may be used in a future version of JavaScript.
4.  All variables are case sensitive, so score and Score would be different variable names, but it is a bad practice to create two variables that have the same name using different cases.
5.  Use a name to describe the kind of information that the variable stores. For example, firstName might be used to store a person's first name, lastName for their last name, and age for their age.
6.  If your variable name is made up of more than one word, use a capital leter for the first leter of every word *after* the first word. For example, firstName rather than firstname (thisis referred to as camel case). You can also use an underscore between each word (you cannot use a dash).



[<== Back](README.md)