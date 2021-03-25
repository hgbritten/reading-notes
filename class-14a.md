# CSS Animation
<!--notes taken from https://learn.shayhowe.com/advanced-html-css/css-transforms/ https://learn.shayhowe.com/advanced-html-css/transitions-animations/ https://codepen.io/dp_lewis/pen/gCfBv https://codepen.io/kieranfivestars/pen/MYdQxX https://codepen.io/akshaychauhan/pen/oAfae https://codepen.io/retyui/pen/ByoaXV https://www.webdesignerdepot.com/2014/05/8-simple-css3-transitions-that-will-wow-your-users -->

## Transforms
> With CSS3 came new ways to position and alter elements. Now general layour technigues can be revisted with alternative ways to size, position, and change elements. All of these new techniques are made possible by the transform property.

- transform comes in two settings 2D and 3D

### Syntax

```

div {
    -webkit-transform: scale(1.5);
    -moz-transform: scale(1.5);
    -o-transform: scale(1.5);
    transform: scale(1.5);
}

```

- these are the prefixes to have the best support across all browsers.
- the last line is the basic transform works in case the browser fully supports transform properties.

### Rotate
- rotate value
- rotate(20deg)
- rotate(-55deg)
- can go all the way to 360 to get back to where you started.

### Scale
- scale(.75) - decrease the size by 1/4
- scale(1.25) - increase the size by 1/4
- you can also choose just to scale the sides by doing scaleX or scaleY or scale(x value, y value)

### Translate
- translate moves the box around
- translateX, translateY, translate(x value, y value)
- values can be shown in percents and pixels

### Skew
- transform: skewX, skewY, or skew(x val, y val) can do some funny things to objects. 
- This is also done with degrees

### C-C-C-COMBO

```

transform: rotate(25deg) scale(.75);

```

### Cubes

```
IN HTML
<div class="cube">
    <figure class="side top">1</figure>
    <figure class="side left">2</figure>
    <figure class="side right">3</figure>
</div>

IN CSS
.cube {
    position: relative;
}
.side {
    height: 95px;
    position: absolute;
    width 95px;
}
.top {
    background: somecolor;
    transform: rotate(deg) skew(deg, deg);
}
.left {
    background: someothercolor;
    transform: rotate(deg) skew(deg, deg) translate(-%, %);
}
.right {
    background: someotherothercolor;
    transform: rotate(deg) skew(-deg, -deg) translate(%, %)
}

```

### Transform Origin
- where the transform is happening from
- 0 0 is the top left
- 100% 100% is the bottom right
- can also be called out with pixels

### Perspective
- also known sort of as a vanishing point (where the camera is looking from).
- if used on a parent element all the elements inside will reference the same vanishing point.
- used almost always with a rotate value. Or else you won't see much change.

### Perspective Depth Value
- how close or how far you are really determines the shape of the object.

### Perspective Origin
- moves the camera from where it was originally placed like a transform origin.
- perspective-origin: 100%, 100%;


### 3D Transforms
- uses Z like rotateZ(deg)

### 3D Scale
- doesn't really have an effect when other 3D transforms aren't in place

### 3D Translate
- translateZ can be negative to push things away or positive to bring them closer

### 3D Skew - doesn't exist - can only be used on x and y axis

### 3D Transform Style
- needs to be placed on the parent element.
- preserve-3d value allows the transform children elements to appear in their own 3D plane while the flat value forces the transformed children elements to lie flat on the 2D plane.

### Backface Visibility
- can be set to hidden so you can't see the item from the back.
- important in animations

## Transitions & Animations
> One evolution with CSS3 was the ability to write behaviors for transitions and animations...With CSS3 transitions you have the potential to alter the appearance and behavior of an element whenever a state change occurs, such as when it is hovered over, focused on, active, or targeted. 

### Transitions
- elements must have a change in state with different styles for each state so you notice a change.
- transition-property, transition-duration, transition-timing-function, and transition-delay aren't all required but they can be used.

```

.box {
  background: #2db34a;
  transition-property: background;
  transition-duration: 1s;
  transition-timing-function: linear;
}
.box:hover {
  background: #ff7b29;
}

```

#### For best support across all browsers use:

```

.box {
    background: #2db34a;
    -webkit-transition-property: background;
       -moz-transition-property: background;
         -o-transition-property: background;
            transition-property: background;
    -webkit-transition-duration: 1s;
       -moz-transition-duration: 1s;
         -o-transition-duration: 1s;
            transition-duration: 1s;
    -webkit-transition-timing-function: linear;
       -moz-transition-timing-function: linear;
         -o-transition-timing-function: linear;
            transition-timing-function: linear;
}
.box:hover {
  background: #ff7b29;
}

```

### Transitional Property
- transition-property decides exactly what properties will be altered

```

.box {
    background: #2db34a;
    border-radius: 6px
    transition-property: background, border-radius;
    transition-duration: 1s;
    transition-timing-function: linear;
  }
  .box:hover {
    background: #ff7b29;
    border-radius: 50%;
  }

```

### Transitional Properties
- things like opacity, background-color, min-height, margin, border-width, and many more can't be changed with transition.

### Transition Duration

```

.box {
  background: #2db34a;
  border-radius: 6px;
  transition-property: background, border-radius;
  transition-duration: .2s, 1s;
  transition-timing-function: linear;
}
.box:hover {
  background: #ff7b29;
  border-radius: 50%;
}

```

- In this example the .2 refers to the first transition for hover which is changing the color
- The 1s refers to the border-radius.
- So it changes color .8s before it fully changes size.

### Transition Timing
- transition-timing-function sets what it looks like while transforming.
- linear is one fluid motion
- ease-in starts slow and finishes quickly

### Transition Delay
- This can change when the transitions start and can't be negative.

### Shorthand

```

.box {
  background: #2db34a;
  border-radius: 6px;
  transition: background .2s linear, border-radius 1s ease-in 1s;
}
.box:hover {
  color: #ff7b29;
  border-radius: 50%;
}

```

### Buttons, Card Flips
- fancy stuff

```

<div class="card-container">
  <div class="card">
    <div class="side">...</div>
    <div class="side back">...</div>
  </div>
</div>

.card-container {
  height: 150px;
  perspective: 600;
  position: relative;
  width: 150px;
}
.card {
  height: 100%;
  position: absolute;
  transform-style: preserve-3d;
  transition: all 1s ease-in-out;
  width: 100%;
}
.card:hover {
  transform: rotateY(180deg);
}
.card .side {
  backface-visibility: hidden;
  height: 100%;
  position: absolute;
  width: 100%;
}
.card .back {
  transform: rotateY(180deg);
}


```

- This reminds me of VH1 website back in the day.
- You hover a album cover photo and flips on the x axis and on the back it displays the name of the band.

## Animations
- Animations pick up where transitions leave off.
- If you need to do a lot you probably need an animation.

### Animation Keyframes
- @keyframes is a rule that includes the animation name such as slide, any animation breakpoints, and the properties to be animated.

```

@keyframes slide {
  0% {
    left: 0;
    top: 0;
  }
  50% {
    left: 244px;
    top: 100px;
  }
  100% {
    left: 488px;
    top: 0;
  }
}

```

- The above using the slide animation so the object will go to all the spots listed.
- 0% shows the starting point of top left
- 50% shows the middle point which happens to be bottom middle
- 100% shows the ending point at the top right

#### Vendor prefixing the keyframe rule
- @-moz-keyframes
- @-o-keyframes
- @-webkit-keyframes

### Animation Duration, Timing Funciton & Delay
- Work much the same as transition

### Animation Direction
- Which way does it run? And does it run both ways?
- also animation-iteration-count: infinite; will set the animation to run as long as you are say hovering the key frame.

[<== Back](README.md)