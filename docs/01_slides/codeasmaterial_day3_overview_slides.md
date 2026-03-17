name: inverse
layout: true
class: center, middle, inverse
---

# Code as Material

## From Instruction to Expression

#### - Day 3 Overview -

<br />
### Prof. Dr. Lena Gieseke | l.gieseke@filmuniversitaet.de  

#### Film University Babelsberg KONRAD WOLF

<br />
.center[<img src="./img/iart_logo_01.png" alt="iart_logo_01" style="width:100%;">]


---
layout:false

## Recap Day 2

--

* Program Flow & Interaction
    * *mouse pressed*, *key pressed*

--
* Conditionals
    * *if [...] happens, then...*

--
* Variables
    * *store values*



---
.header[Code as Material]

## Day 3

* Brief exercise

--

* Example recap

--

* Code Example *Lines*

--
* Loops



---
.header[Code as Material]

## Color and Position Animation

???

* https://editor.p5js.org/legie/sketches/pA5Ddli51
* Chose random start values

--

.left-even[
```js
// Pseudo Code

let positionX = 0;
let stepX = 1;

...

positionX = positionX + stepX;
```
]

.right-even[
This means as long as `stepX` is a positive number such as 1, we count `positionX` up:  
* positionX = positionX + stepX;
* positionX = 0 + 1 = 1
* positionX = 1 + 1 = 2
* positionX = 2 + 1 = 3
* positionX = 3 + 1 = 4
* ...
]

---
.header[Code as Material]

## Color and Position Animation

.left-even[
```js
// Pseudo Code

let positionX = 100;
let stepX = -1;

...

positionX = positionX + stepX;
```
]

.right-even[
This means as long as `stepX` is a negative number such as -1, we count `positionX` down:  
* positionX = positionX + stepX;
* positionX = 100 + (-1) = 99
* positionX =  99 + (-1) = 98
* positionX =  98 + (-1) = 97
* positionX =  97 + (-1) = 96
* ...
]


???

* https://editor.p5js.org/legie/sketches/pA5Ddli51


---
.header[Code as Material]

## Color and Position Animation

* We are going up, `stepX = 1`

--

* When positionX becomes larger than `windowWidth`, we multiply stepX by -1 so that stepX becomes equal -1

--

```
if(positionX > windowWidth) {
    stepX = stepX * -1;
}
```

--

* `1 * (-1) = -1` → *stepX is now -1*

--

This would work the same with any other value for stepX. Let's say seepX is 5:  
* `5 * (-1) = -5` → *stepX is now -5*


---
.header[Code as Material]

## Color and Position Animation

* We are going down, `stepX = -1`

--

* When positionX becomes smaller than `0`, we multiply stepX by -1 so that stepX becomes equal 1

--

```
if(positionX > windowWidth) {
    stepX = stepX * -1;
}
```

--

* `(-1) * (-1) = 1` → *stepX is now 1*

--

This would work the same with any other value for stepX. Let's say stepX is -5:  
* `(-5) * (-1) = 5` → *stepX is now 5*






---
template:inverse 

# *The End*

### Prof. Dr. Lena Gieseke | l.gieseke@filmuniversitaet.de  

#### Film University Babelsberg KONRAD WOLF

