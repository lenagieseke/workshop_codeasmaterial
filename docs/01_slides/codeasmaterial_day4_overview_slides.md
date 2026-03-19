name: inverse
layout: true
class: center, middle, inverse
---

# Code as Material

## From Instruction to Expression

#### - Day 4 Overview -

<br />
### Prof. Dr. Lena Gieseke | l.gieseke@filmuniversitaet.de  

#### Film University Babelsberg KONRAD WOLF

<br />
.center[<img src="./img/iart_logo_01.png" alt="iart_logo_01" style="width:100%;">]


---
layout:false

## Recap Day 3

--

* [`constraint()`](https://p5js.org/reference/p5/constrain/)

--

<br />
* Operation shortening

```
x = x + 1
```



---
layout:false

## Recap Day 3

* [`constraint()`](https://p5js.org/reference/p5/constrain/)

<br />
* Operation shortening

```
x = x + 1   →    x += 1
```

--
```
x = x * step   →   x *= step
```

---
layout:false

## Recap Day 3

* [`constraint()`](https://p5js.org/reference/p5/constrain/)

<br />
* Operation shortening

```
x = x + 1   →   x += 1
```



---
layout:false

## Recap Day 3

* [`constraint()`](https://p5js.org/reference/p5/constrain/)

<br />
* Operation shortening

```
x = x + 1   →   x += 1   →   x++
```


---
.header[Code as Material | Example *Line Drawing Algorithm* |  Possible Adjustments]

## Bézier Curves


Reference: [bezier](https://p5js.org/reference/p5/bezier/), [wikipedia](https://en.wikipedia.org/wiki/B%C3%A9zier_curve)


```javascript

function setup() {
    noFill();
}

function draw() {

    bezier(0, 0, lineStartX, lineStartY, lineEndX, lineEndY, 
                                    windowWidth, windowHeight);

}
```

???
What is a Bézier curve
* Start point → where the curve begins
* End point → where it ends
* Two control points → define how it bends

The curve does not pass through the control points but they act like "directional forces".



---
.header[Code as Material]

## Day 4

--

* Loops

--

* Algorithmic Thinking

--

* Images

--
* Summary





---
template:inverse 

# *The End*

### Prof. Dr. Lena Gieseke | l.gieseke@filmuniversitaet.de  

#### Film University Babelsberg KONRAD WOLF

