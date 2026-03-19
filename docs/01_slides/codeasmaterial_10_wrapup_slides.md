name: inverse
layout: true
class: center, middle, inverse
---

### Code as Material
## Creative Coding Foundations for Artistic and Design Practices

#### - Wrap Up -

<br /><br />
### Prof. Dr. Lena Gieseke | l.gieseke@filmuniversitaet.de  

#### Film University Babelsberg KONRAD WOLF



---
template:inverse

## Summary



---
layout:false

.header[Course Summary]

## Environment

* p5.js Editor
    * The environment
    * Sketches
    * Errors (are our friends!)
    * Saving
    * Sharing



---
.header[Course Summary]

## Functions

Function **calls** and function **definitions**:

--
  
```
circle(200, 200, 100);
```

--

```
function circle(x, y, d){
    ...
}
```



---

.header[Course Summary]

## Commands

* Commands are just *function calls*.

--
* You can define what should happen in given functions, e.g., `setup()`

```javascript
function setup() {
    // Code that is executed when p5 calls the function
}
```


???

* You can write your own functions and call them

```javascript
function functionname([parameter1,...]) {

    // Code that is executed when we call the function

    [return value;]
}
```

---
.header[Course Summary]

## The p5 Coordinate System

--

.center[<img src="../01_slides/img/drawing/ch01_12.png" alt="name" style="width:50%;">]


---
.header[Course Summary]

## Drawing commands

--


* `arc()`, `ellipse()`, `circle()`, `line()`, `rect()`, `square()`, `triangle()`
* `fill(r, g, b)`, `stroke(r, g, b)`, `strokeWeight(w)`


--
* Color systems:
    * RGBA
    * HSB
    * `colorMode(HSB);`
    * `colorMode(HSB, 50, 50, 50);`


---
.header[Course Summary]

## Interaction

--
* Functions: `function mousePressed(){}`, `function keyPressed(){}`, ...

--

* System variables: `mouseX`, `key`, `keyPressed`, ...




---
.header[Course Summary]

## Conditionals

--
* `if(condition is true){}`
* `else{}`


--
Operators

--

* Comparison: `>`, `>=`, `<`, `<=`, `==`, `!=`
* Logical Operators: `&&`, `||`, `!`

--
* Arithmetic Operators: `+`, `-` , `*` , `/` , `++`, `--`, `+=`, `-=`, `*=`



---
.header[Course Summary]

## Variables

--

We use variables to save and access data

--
* `let hue = 0;`
    * Variables have a data type
    * Variables live inside `{}` and have a scope


---
.header[Course Summary]

## Loops

--

```js
let myCounter = 0;
while(myCounter < numberOfTimes){
    …
}
```

--

```js
for(let i = 0; i < numberOfTimes; i++){
    …
}
```

???

```js
for(let element of myArray)…
```


---
.header[Course Summary]

## Loops

2D Loop

*For every row look at every element…*

```js
for (let y = 0; y < numberRows; y++){

    for (let x = 0; x < numberColumns; x++){

        print("Row: " + y + " Column: " + x);
    }
}
```


---
.header[Course Summary]

## Images

--

```js
let imgPanda;

function preload() {
    imgPanda = loadImage("panda.jpg");
}

function draw() {
    image(imgPanda, 50, 50);
}
```

--
* Like any other object, e.g. change the positions...
* Store sequence in array and display them sequentially to animate
* `get(x, y)` and `set(x, y, color)` for, e.g., custom filter

???

* Animate images e.g. by changing their position like any other shape
* Store images in arrays and display them sequentially to animate image series
* Use `get(x, y)` and `set(x, y, color)` to return or set the color of the image at a specific pixel



---
.header[Course Summary]

## Objects

--

* Have properties and functions that *belong to* them
* You access those properties and functions with the `.` notation
    * `myImage.width`
    * `myImage.resize(100, 100);`
--
* p5.Image, p5.sound, arrays



---
.header[Course Summary]

## Programming

.left-even[

* Break a problem into manageable pieces (*divide and conquer*)
]

???
  
* **Decomposition**: Break a problem down into smaller pieces
* **Pattern Matching**: Find similarities
* **Abstraction**: Reduce specific differences and make one solution work for multiple cases



---
.header[Course Summary]

## Programming

.left-even[

* Break a problem into manageable pieces (*divide and conquer*)
* Work with what you have
]



---
.header[Course Summary]

## Programming

.left-even[

* Break a problem into manageable pieces (*divide and conquer*)
* Work with what you have
* Test each step
    * Use `print` to check 
]



---
.header[Course Summary]

## Programming

.left-even[

* Break a problem into manageable pieces (*divide and conquer*)
* Work with what you have
* Test each step
    * Use `print` to check 
]

.right-even[
* Layout does matter
    * Represent the logic / structure
    * Prevent and find errors
]


---
.header[Course Summary]

## Programming

.left-even[

* Break a problem into manageable pieces (*divide and conquer*)
* Work with what you have
* Test each step
    * Use `print` to check 
]

.right-even[
* Layout does matter
    * Represent the logic / structure
    * Prevent and find errors
* Errors are part of the process
]

---
.header[Course Summary]

## Programming
.left-even[

* Break a problem into manageable pieces (*divide and conquer*)
* Work with what you have
* Test each step
    * Use `print` to check 
]

.right-even[
* Layout does matter
    * Represent the logic / structure
    * Prevent and find errors
* Errors are part of the process
* Use the reference, look at example code
]


---
.header[Course Summary]

# Use the [Reference](https://p5js.org/) 🚒

--

* [Open Processing](https://www.openprocessing.org)
* [Happy Coding](https://happycoding.io/tutorials/p5js/)
* [Generative Gestaltung](http://www.generative-gestaltung.de)
* [Creative Applications](https://www.creativeapplications.net/tools/framework/p5js/)
* The fairest of them all: [Daniel Shiffmann](https://shiffman.net/) 🤴🏼
* [Nature of Code](https://natureofcode.com/)


???
  

* https://happycoding.io/tutorials/p5js/


---
.header[Course Summary]

## Learning Objectives

--

With this course, you hopefully gained

--
* An understanding of programming

--
* **Skills to develop simple programs from scratch**

--
* Skills to apply programming as (an expressive) tool


???
  

* But it is like a poetry class in Japanese

---
template:inverse

# Follow-Up Topics

---
## Follow-Up Topics

--
* Code Organization
    * Writing your own functions
    * Splitting code into different files

--
* Arrays

--
* p5 libraries, e.g. for sound
* Video

--
* Object Oriented Programming

--
* [ml5js](https://ml5js.org/)

--
* A local coding environment




---
template: inverse

# Where Should You Go From Here?
# 🤔

---

## Where Should You Go From Here?

--
* Work with the code from the course, adjust its, etc.

--
* Pick a direction you want to focus on
    * Generative designs
    * Games
    * Tools
    * etc.
--
* Watch tutorials and courses

--
* Look through other people's and professional code

--
* Create your own projects

---
## Where Should You Go From Here?

Once you stop to practice coding your will lose the skill. 😨 

--

<br />
But it will come back much faster once you are coding again! 😁


---
## Where Should You Go From Here?

I am happy to advise projects, theses, etc.  
  
Just get in touch.

<br />
### l.gieseke@filmuniversitaet.de


---
template:inverse 

# *The End End*


### Prof. Dr. Lena Gieseke | l.gieseke@filmuniversitaet.de  

#### Film University Babelsberg KONRAD WOLF
