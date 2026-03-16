---
layout: default
title: Exercise 02
parent: Exercises
nav_order: 2
---

### Workshop
# Code as Material - From Instruction to Expression

  
Prof. Dr. Lena Gieseke \| l.gieseke@filmuniversitaet.de  

![iart_logo_01](../../01_slides/img/iart_logo_01.png)

---

  
## Exercise 02 - Program Flow & Interaction


### Task 02.01 - Inspiration
  
Find a publicly available p5 example, e.g., from [OpenProcessing](https://openprocessing.org/discover/#/trending), that you like. Briefly describe why you like it.  
  

### Task 02.02 - Learning Materials

Recap the slides:

* [Program Flow and Interaction](../../01_slides/codeasmaterial_04_flow_slides.html)
* [Conditionals](../../01_slides/codeasmaterial_05_conditionals_slides.html)
* [Variables](../../01_slides/codeasmaterial_06_variables_slides.html)


### Task 02.03 - Errors

[This code](https://editor.p5js.org/legie/sketches/2wzE7ba4V) has three errors. Can you find and fix them? Make sure to read the error messages, they might (or might not) help you find the issues.

Briefly explain what the code does.


```js
function setup() {createCanvas(400, 400);colorMode(HSB);noStroke();
  // Properties for the
  // text() command
  // https://p5js.org/reference/p5/text/
  // https://p5js.org/reference/p5/textAlign/
  textAlign(CENTER, CENTER);textSize(36);}

function draw() // hour() returns the current hour

  // from 0..23
  // https://p5js.org/reference/p5/hour/
  if( hour() < 5 ) {
    
    // Night
    background(240, 100, 40);fill(50, 40, 100);text('⭐️ Good Night! ⭐️', 200, 200);} else if (hour() < 12) { // Morning
    background(200, 20, 100);fill(42, 100, 100);text('☀️ Good Morning! ☀️, 200, 200);} else if (hour() < 16) {
    
    //Midday
    background(210, 60, 100);    
    
    fill(42, 60, 100);text('🌼 Good Afternoon! 🌼', 200, 200);} else {
    
    //Evening
    background(210, 100, 80);    
    fill(100);
    text('🍿 Good Evening! 🛋️', 200);
  }}
```




### Task 02.04 - Interaction

Create a sketch up to your liking and that uses interaction and conditionals. You could also add interaction to yesterday's creative sketch. The goal is to practice the learned functionalities.


---

*Happy Flowing!*

