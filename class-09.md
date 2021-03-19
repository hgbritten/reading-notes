# Forms and JS Events

<!-- notes taken from Duckett HTML and JS books-->

## Forms


### Different kinds of form controls
- Adding text
      - Text input
      - Password input
      - Text area
- Making Choices
      - Radio buttons
      - Checkboxes
      - Drop-down boxes
- Submitting forms
      - Submit buttons
      - Image buttons
- Uploading files
      - File upload

### How forms work
    1. User fills in form and presses a button to submit
    2. Name of each form control is sent to server along with the value entered
    3. Server process information
    4. Server creates new page to send back

- A form may have several form controls, each gathering different info. The server needs to know which piece of inputted data corresponds with which form element.

```
username=Ivy
```

- In this example username is the name and Ivy is the value

#### `<form>` structure
- action
- method
- id

#### text `<input>`
- type="text"
- name
- size
- maxlength

#### password `<input>`
- type="password"
- name
- size, maxlength

#### `<textarea>` pops out the image below
  
```
<form action="example.com">
<p>What did you think of this gig?</p>
<textarea name="comments" cols="20" rows="4">Enter your comments...</textarea>
</form>
```

[image](!textarea.PNG)

#### Radio button
- type="radio"
- name
- value
- checked

#### Checkbox
- type="checkbox"
- name
- value
- checked

#### Drop down list box
- `<select>`
- name
- `<option>`
- value
- selected

#### Multiple select box
- `<select>`
- size
- multiple

#### File input box
- `<input>`
- type="file"

#### Submit button
- `type="submit"`
- name
- value

#### Image button
- `<input type="image">`

#### Button & hidden controls
- `<button>`
- `<input type="hidden">`

#### Labeling form controls
- `<label for="gender">`

#### Grouping form elements
- `<fieldset>`
- `<legend>`

## AND MANY MORE

## Lists, Tables, and Forms

### Specifying bullet point styles
#### uls
- none
- disc
- circle
- square

```
In CSS
ul {
    list-style-type: disc;
}
```

#### ols
- decimal
- decimal-leading-zero
- lower-alpha
- upper-alpha
- lower-roman
- upper-roman

```
In CSS
ol {
    list-style-type: lower-alpha;
}
```

### Adding borders and backgrounds to tables

#### Images!


```
In CSS
ul {
    list-style-image: url("images/star.png");
}
```


#### Positions
- outside
- inside

#### Table properties
- width
- padding
- text-transform
- letter-spacing, font-size
- border-top, border-bottom
- text-align
- background-color
- :hover to highlight!

#### Border on empty cells and cell gaps


```  
table.one {
    empty-cells: show;
    border-spacing: 5px 15px;}
```


### Changing the apperance of form elements

#### Styling text inputs
- font-size
- color
- background-color
- border
- border-radius
- :focus - changes the background color of the text when it is being used kind of like :hover
- background-image

#### Styling submit buttons
- text shadow

#### Cursor styles
- auto
- crosshair
- default
- pointer
- move
- text
- wait
- help
- url("cursor.gif");

```
a {
    cursor: move;
}
```

## Events



[<== Back](README.md)