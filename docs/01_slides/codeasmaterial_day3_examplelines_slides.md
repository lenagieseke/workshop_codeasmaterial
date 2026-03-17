name: inverse
layout: true
class: center, middle, inverse
---

### Code as Material
## Creative Coding Foundations for Artistic and Design Practices

#### - Line Drawing Algorithm -

<br />
### Prof. Dr. Lena Gieseke | l.gieseke@filmuniversitaet.de  

#### Film University Babelsberg KONRAD WOLF

<br />
.center[<img src="./img/iart_logo_01.png" alt="iart_logo_01" style="width:100%;">]



---
layout:false

.header[Code as Material]

.center[<img src="./img/intro/brera_poster_b_01.png" alt="brera_poster_b_01" style="width:36%;">]

---
.header[Code as Material]

.center[<img src="./img/intro/brera_poster_a_01.png" alt="brera_poster_a_01" style="width:36%;">]

---

<iframe width="1024" height="640" src="https://editor.p5js.org/legie/full/9WDwO8l1U"></iframe>


---
.header[Code as Material]

## Example *Line Drawing Algorithm*


.left-even[

<iframe width="512" height="320" src="https://editor.p5js.org/legie/full/9WDwO8l1U"></iframe>

]

.right-even[

> What do we see?
]


---
.header[Code as Material]

## Example *Line Drawing Algorithm*


.left-even[

<iframe width="512" height="320" src="https://editor.p5js.org/legie/full/9WDwO8l1U"></iframe>

]

.right-even[

> What do we see?

* Which shapes?
* Which movement?
* Which coloring?

]

---
.header[Code as Material]

## Example *Line Drawing Algorithm*

--

* One line is drawn each frame

--

* With each new draw, the line’s start and end points  are moved by adding fixed values, also the color is slightly changed

--

* If the start or endpoint of a line is hitting a canvas boundary, change its direction

???
We are not animating a line directly. We are animating two points.
The line is the visible consequence of their relationship.
Once we understand that, the sketch becomes much less mysterious and much more programmable.

That is a lovely computational lesson, because many generative systems work exactly like this:
* define simple agents or values
* let them evolve
* observe the form that emerges

---
.header[Code as Material]

## Example *Line Drawing Algorithm*

The setup

--
* One line, defined by a start and an end point:

--
    * Each endpoint has a position

--
    * Each endpoint has a step value

--
* A color with a step value for it

---
.header[Code as Material]

## Example *Line Drawing Algorithm*

The animation

--

* Every frame:

--
    * Draw the line

--
    * Add the step value to the color

--
        * Constrain it to the range 0–255

--
    * Add the step values to both endpoints

--
        * If an endpoint hits a canvas edge, reverse its step direction

---
template:inverse

### *Let's Go Step by Step*


---
.header[Code as Material | Example *Line Drawing Algorithm*]

## Steps

--

1. Setup & Draw a Line
2. Line Variables
3. Move Start and Endpoints
4. Keep in Bounds
5. Random Movement
6. Setting Color
7. Color Drift
8. Pause Key `p`


---
.header[Code as Material | Example *Line Drawing Algorithm* | 1. Setup & Draw a Line]


```javascript
function setup() {
  createCanvas(windowWidth, windowHeight);
  background(255);
}

function draw() {
  line(100, 100, 300, 200);
}
```

---
.header[Code as Material | Example *Line Drawing Algorithm* | 2. Line Variables]


```javascript

let lineStartX, lineStartY;
let lineEndX, lineEndY;

function setup() {
  createCanvas(windowWidth, windowHeight);
  background(255);

  lineStartX = 100;
  lineStartY = 100;
  lineEndX = 300;
  lineEndY = 200;
}

function draw() {

  line(lineStartX, lineStartY, lineEndX, lineEndY);
}
```


---
.header[Code as Material | Example *Line Drawing Algorithm* | 3. Move Start and Endpoints]


```javascript
let lineStartX, lineStartY;
let lineEndX, lineEndY;
let stepStartX = 2;
let stepStartY = 1;
let stepEndX = -3;
let stepEndY = 2;

...

function draw() {

  line(lineStartX, lineStartY, lineEndX, lineEndY);
  
  lineStartX += stepStartX;
  lineStartY += stepStartY;
  lineEndX += stepEndX;
  lineEndY += stepEndY;
}
```


---
.header[Code as Material | Example *Line Drawing Algorithm* | 4. Keep in Bounds]

```javascript
function draw() {
...

  if (lineStartX < 0 || lineStartX > width) {
    stepStartX *= -1;
  }

  if (lineStartY < 0 || lineStartY > height) {
    stepStartY *= -1;
  }

  if (lineEndX < 0 || lineEndX > width) {
    stepEndX *= -1;
  }

  if (lineEndY < 0 || lineEndY > height) {
    stepEndY *= -1;
  }
}
```

---
.header[Code as Material | Example *Line Drawing Algorithm* | 5. Random Movement]

```javascript
let stepStartX, stepStartY;
let stepEndX, stepEndY;
let rangeStep = 10;

function setup() {
  ...
  stepStartX = random(-rangeStep, rangeStep);
  stepStartY = random(-rangeStep, rangeStep);
  stepEndX = random(-rangeStep, rangeStep);
  stepEndY = random(-rangeStep, rangeStep);
}

...
```


---
.header[Code as Material | Example *Line Drawing Algorithm* | 6. Setting Color]

```javascript
let r, g, b;

function setup() {

    ...

  r = random(255);
  g = random(255);
  b = random(255);
}

function draw(){
...
    stroke(r, g, b, 40);
}
```



---
.header[Code as Material | Example *Line Drawing Algorithm* | 7. Color Drift]

```javascript
let rangeColor = 4;


function draw(){
...
    r += random(-rangeColor, rangeColor);
    g += random(-rangeColor, rangeColor);
    b += random(-rangeColor, rangeColor);

    r = constrain(r, 0, 255);
    g = constrain(g, 0, 255);
    b = constrain(b, 0, 255);
}
```


---
.header[Code as Material | Example *Line Drawing Algorithm* | 8. Pause Key `p`]

```javascript
let pause = false;

function draw() {
  if (!pause) {
    // animation
  }
}

function keyPressed() {
  if (key === 'p') {
    pause = !pause;
  }
}
```

---
.header[Code as Material | Example *Line Drawing Algorithm*]

## Possible Adjustments

--

* Make the line thicker or thinner or adjust alpha over time.


--

* Give both endpoints the same step value so the line moves rigidly.

--

* Replace random color drift with a gradual color cycle.

--

* Add a key that changes some of the values.

--

* Have multiple lines

--

* Change the line to a Bézier curve.


---
.header[Code as Material | Example *Line Drawing Algorithm* |  Possible Adjustments]

## Bézier Curves


Reference: [bezier](https://p5js.org/reference/p5/bezier/)


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
.header[Code as Material | Example *Line Drawing Algorithm*]

## Creative Control

> Which aspects would you want (interactive) control over?

???
Motion (endpoints as agents)
* Step magnitude (rangeStep): overall speed and turbulence.
* Step anisotropy: separate ranges for x vs y to bias motion (e.g., mostly horizontal).
* Coupling between endpoints: make end follow start (rigid-ish line) vs independent (wild geometry).
* Step evolution: keep steps constant, or slowly drift them (random walk on velocity).
* Smoothing / inertia: interpolate position toward target (adds “mass”, reduces jitter).
* Time modulation: scale speed by sin(t) or noise for breathing-like tempo.

Boundary behavior (what “bouncing” means)
* Reflect vs wrap: bounce off edges, or teleport to opposite side (toroidal space).
* Soft walls: instead of flipping instantly, gradually steer back (spring force near edges).
* Energy loss: damp the step on bounce (velocity *= 0.98) for “cooling” dynamics.
* Sticky edges: pause or slow briefly on contact for a glitchy “edge obsession.”

Color dynamics
* Color step size (rangeColor): rate of chromatic drift.
* Color model: RGB drift vs HSB/HSV drift (HSB gives more perceptual control over hue cycling).
* Palette constraints: snap to a palette or restrict hue bands (less randomness, more art direction).
* Alpha as a parameter: trail density and ghosting are mostly stroke(..., alpha).

Temporal accumulation (memory)
* Clear mode: never clear (infinite memory) vs clear every frame (no memory).
* Decay background: draw a translucent rect each frame to fade trails gradually (finite memory).
* Frame rate: lower FPS makes “steps” more legible, higher FPS makes silk.

Geometry choice
* Line vs Bézier: switch between direct connection and curvature control.
* Control-point mapping: treat endpoints as Bézier controls (as you started), or as anchors, or both.
* Stroke weight dynamics: thickness tied to speed, distance between points, or time.

Reproducibility and performance
* Seed control (randomSeed, noiseSeed): rerunnable “editions” of a run.
* Spawn/reset triggers: key press to re-roll steps/color, or periodic resets for structured chapters.


---

<iframe width="1024" height="640" src="https://editor.p5js.org/legie/full/9WDwO8l1U"></iframe>


---
template:inverse 

# *The End*


### Prof. Dr. Lena Gieseke | l.gieseke@filmuniversitaet.de  

#### Film University Babelsberg KONRAD WOLF
