# p5js-designing-interactive-patterns

P5js is a project from processing which is a programming language based on Java oriented towards graphic and interactive creation. P5js aims to transpose the spirit of processing to the web and therefore to the JavaScript language. It's an easy-to-access framework for beginners with good documentation and an active community.

P5js offers the integration into an HTML5 canvas of a maximum of functions for drawing and animation, interaction possibilities through different human-machine interfaces (keyboard, mouse, webcam, microphone, etc.), or even with the components of a web page and partial but developing support for webgl.

You can consult [the p5js reference](https://p5js.org/reference/) which will describe with examples all of the p5js functions, but do not hesitate to also consult [the examples](https://p5js.org/examples/) - which may however prove to be a little more complicated to understand.

Many libraries offer new possibilities, but p5js can naturally interface with any js library.

The techniques described here are accessible to beginners; however, it is necessary to know the basics of programming with p5js in a development environment of your choice, that is to say, for example, to have read and integrated the first 3 paragraphs of this [resource. 'introduction](https://github.com/b2renger/Introduction_p5js) :

-   [How to work with p5js](https://github.com/b2renger/Introduction_p5js#p5js_tools)
-   [The basic principles](https://github.com/b2renger/Introduction_p5js#bases)
-   [Draw with the mouse](https://github.com/b2renger/Introduction_p5js#dessiner)

The first link also has _resource_ and _reference_ sections at the end of the page which point to other tutorials or libraries and to artistic and/or fun projects involving web technologies.

You can find all the code for the different examples on this [github repository](https://github.com/b2renger/p5js-designing-interactive-patterns)

## [](https://github.com/djsnipa1/p5js-designing-interactive-patterns#contenu)Content

-   [The big differences between processing and p5js](https://github.com/djsnipa1/p5js-designing-interactive-patterns#Les-grandes-differences-entre-processing-et-p5js)
    -   [Theoretical differences](https://github.com/djsnipa1/p5js-designing-interactive-patterns#Les-differences-theoriques)
    -   [In practice](https://github.com/djsnipa1/p5js-designing-interactive-patterns#En-pratique)
-   [A responsive web page - Draw a circle that stays in the middle](https://github.com/djsnipa1/p5js-designing-interactive-patterns#Une-page-web-responsive---Dessiner-un-cercle-qui-reste-au-milieu)
-   [Draw a grid - long live for loops!](https://github.com/djsnipa1/p5js-designing-interactive-patterns#Dessiner-une-grille---vive-les-boucles-for-!)
    -   [First grid](https://github.com/djsnipa1/p5js-designing-interactive-patterns#premiere-grille)
    -   [A grid of circles](https://github.com/djsnipa1/p5js-designing-interactive-patterns#une-grille-de-cercles)
        -   [a little interaction: a grid with different granularities](https://github.com/djsnipa1/p5js-designing-interactive-patterns#un-peu-d'interaction-changer-la-taille-des-cases)
        -   [circles centered in our boxes](https://github.com/djsnipa1/p5js-designing-interactive-patterns#des-cercles-centres-dans-nos-cases) - [**DEMO**](https://b2renger.github.io/p5js-designing-interactive-patterns/sketch_01_b_responsive_grid/)
        -   [a grid centered in our page](https://github.com/djsnipa1/p5js-designing-interactive-patterns#une-grille-centree-dans-notre-page) - [**DEMO**](https://b2renger.github.io/p5js-designing-interactive-patterns/sketch_01_c_responsive_grid/)
-   [A little interaction with the mouse](https://github.com/djsnipa1/p5js-designing-interactive-patterns#Un-peu-d'interaction-avec-la-souris)
    -   [A grid of circles that change size depending on mouse position](https://github.com/djsnipa1/p5js-designing-interactive-patterns#Une-grille-de-cercles-qui-changent-de-taille-en-fonction-de-la-position-de-la-souris) - [**DEMO**](https://b2renger.github.io/p5js-designing-interactive-patterns/sketch_02_a_interactive_grid/)
    -   [A grid of concentric circles](https://github.com/djsnipa1/p5js-designing-interactive-patterns#une-grille-de-cercles-concentriques) - [**DEMO**](https://github.com/djsnipa1/p5js-designing-interactive-patterns/blob/master)
    -   [A grid of interactive lines](https://github.com/djsnipa1/p5js-designing-interactive-patterns#une-grille-de-lignes-interactives) - [**DEMO**](https://b2renger.github.io/p5js-designing-interactive-patterns/sketch_02_d_triple-for-lines/)
    -   [A grid of concentric circles 2](https://github.com/djsnipa1/p5js-designing-interactive-patterns#Une-grille-de-cercles-concentriques-2) - [**DEMO**](https://b2renger.github.io/p5js-designing-interactive-patterns/sketch_02_c_triple-for/)
-   [Write conditions with if()](https://github.com/djsnipa1/p5js-designing-interactive-patterns#Ecrire-des-conditions-avec-if())
    -   [if - else and random() - randomSeed()](https://github.com/djsnipa1/p5js-designing-interactive-patterns#if-else-et-random()---randomSeed()) - [**DEMO**](https://b2renger.github.io/p5js-designing-interactive-patterns/sketch_03_a_if/)
    -   [Variation 1 with nested if](https://github.com/djsnipa1/p5js-designing-interactive-patterns#Variation-1-avec-if-imbriques) - [**DEMO**](https://b2renger.github.io/p5js-designing-interactive-patterns/sketch_03_b_if/)
    -   [Variation 2 with if - else if](https://github.com/djsnipa1/p5js-designing-interactive-patterns#Variation-2-avec-if---else-if) - [**DEMO**](https://b2renger.github.io/p5js-designing-interactive-patterns/sketch_03_c_if/)
-   [Make some Noise!](https://github.com/djsnipa1/p5js-designing-interactive-patterns#Make-some-Noise-!)
    -   [one-dimensional noise](https://github.com/djsnipa1/p5js-designing-interactive-patterns#noise-1-dimension) - [**DEMO**](https://b2renger.github.io/p5js-designing-interactive-patterns/sketch_04_a_noise-1D/)
    -   [two-dimensional noise](https://github.com/djsnipa1/p5js-designing-interactive-patterns#noise-2-dimensions) - [**DEMO**](https://b2renger.github.io/p5js-designing-interactive-patterns/sketch_04_b_noise-2D/)
    -   [three-dimensional noise](https://github.com/djsnipa1/p5js-designing-interactive-patterns#noise-3-dimensions) - [**DEMO**](https://b2renger.github.io/p5js-designing-interactive-patterns/sketch_04_c_noise-3D/)
    -   [noise and polar coordinates](https://github.com/djsnipa1/p5js-designing-interactive-patterns#noise-et-coordonnees-polaires) - [**DEMO**](https://b2renger.github.io/p5js-designing-interactive-patterns/sketch_04_d_noise-circle-rad-angle/)
    -   [noise and symmetries](https://github.com/djsnipa1/p5js-designing-interactive-patterns#noise-et-symetries) - [**DEMO**](https://b2renger.github.io/p5js-designing-interactive-patterns/sketch_04_e_noise-symetric/)
    -   [symmetrical noise and polar coordinates](https://github.com/djsnipa1/p5js-designing-interactive-patterns#Noise-symetrique-et-coordonnees-polaires) - [**DEMO**](https://b2renger.github.io/p5js-designing-interactive-patterns/sketch_04_f_noise-circle-symetric/)
    -   [asymmetric noise and polar coordinates](https://github.com/djsnipa1/p5js-designing-interactive-patterns#Noise-asymetrique-et-coordonnees-polaires) - [**DEMO**](https://b2renger.github.io/p5js-designing-interactive-patterns/sketch_04_g_noise-circle-asymetric/)
    -   [interlude unknown pleasures](https://github.com/djsnipa1/p5js-designing-interactive-patterns#interlude-unknown-pleasures) - [**DEMO**](https://b2renger.github.io/p5js-designing-interactive-patterns/sketch_04_h_joydivision/)
-   [rotate() and translate()](https://github.com/b2renger/p5js-designing-interactive-patterns#rotate-translate)
    -   [a basic example](https://github.com/djsnipa1/p5js-designing-interactive-patterns#un-exemple-basique) - [**DEMO**](https://b2renger.github.io/p5js-designing-interactive-patterns/sketch_05_a_rotate/)
    -   [use of fonts](https://github.com/djsnipa1/p5js-designing-interactive-patterns#utilisation-de-fonts) - [**DEMO1**](https://b2renger.github.io/p5js-designing-interactive-patterns/sketch_05_b_rotate_typo_reflection/) - [**DEMO2**](https://b2renger.github.io/p5js-designing-interactive-patterns/sketch_05_c_rotate_typo_polar/)
-   [Drawing in layers](https://github.com/djsnipa1/p5js-designing-interactive-patterns#Dessiner-dans-des-calques) - [**DEMO 1**](https://b2renger.github.io/p5js-designing-interactive-patterns/sketch_06_a_layers_half-cirdles/) - [**DEMO 2**](https://b2renger.github.io/p5js-designing-interactive-patterns/sketch_06_b_layers_supperpositions/index.html)

## [](https://github.com/djsnipa1/p5js-designing-interactive-patterns#les-grandes-differences-entre-processing-et-p5js)The big differences between processing and p5js

### [](https://github.com/djsnipa1/p5js-designing-interactive-patterns#les-differences-theoriques)Theoretical differences

I advise you to start by reading the [basic principles](https://github.com/b2renger/Introduction_p5js#les-principes-de-bases) allowing you to understand how a web page is structured between html file and javascript file(s) and which sets out the fundamental principles of processing and therefore of p5js.

In reality processing and p5js are both very similar and very different. **In processing we write java** code and in p5js we write **javascript** . Java and javascript are fundamentally different languages:

-   java is compiled (when you click on the arrow your code is "reread" by your computer and errors are possibly presented to you, but above all it is transformed at this moment into executable instructions = machine language by your processor etc.) Javascript is an interpreted language: it is essentially composed of text and it is not precompiled before execution.
    
-   java is executed by a virtual software layer, javascript is executed directly by the browser(s).
    
-   Java is a typed language (there are data types: _float_ , _int_ , _String_ , _boolean etc), JS does not have a type (all these types are replaced by a_ _let_ keyword ).
    

In practice we will focus on a subpart of javascript with the discovery of p5js, just as we are interested in a subpart of java when we write processing code.

[**home**](https://github.com/djsnipa1/p5js-designing-interactive-patterns#contenu)  

### [](https://github.com/djsnipa1/p5js-designing-interactive-patterns#en-pratique)In practice

1- Types: more _float_ etc. but _let_

[2- The size()](https://processing.org/reference/size_.html) function allowing us to specify the size of our window is replaced by the [createCanvas()](https://p5js.org/reference/%23/p5/createCanvas) function . In fact we no longer create a window but a [**canvas**](https://en.wikipedia.org/wiki/Canvas_element) in a web page. The canvas is an HTML element introduced with HTML5 allowing dynamic images to be displayed via the execution of JavaScript scripts.

3- Semicolons at the end of each statement are no longer necessary! but we will still keep them...

4- The "debugging" process linked to the console (the part in which the error messages are displayed in red) is also a little different. In order to access any error messages, you must right-click on our page and click on "Inspect", then click on the "console" tab. To display messages from our code in this same console, instead of using _println("my message to display")_ , we will use _console.log("my message to display")_

There are of course other differences but they are less impactful. Using the basic processing functions you already know are the same or slightly different:

[ellipse()](https://p5js.org/reference/%23/p5/ellipse) , [line()](https://p5js.org/reference/%23/p5/line) , [rect()](https://p5js.org/reference/%23/p5/rect) , [background()](https://p5js.org/reference/%23/p5/background) , [colorMode()](https://p5js.org/reference/%23/p5/colorMode) , [fill()](https://p5js.org/reference/%23/p5/fill) , [stroke()](https://p5js.org/reference/%23/p5/stroke) etc.

We will now focus more directly on the code and the implementation of our first programs. However, we must keep in mind that our programs are executed in a browser and that the user can change the size of his window at any time and graphically this must not change the situation too much: we will therefore have to work in a responsive **manner** and therefore to express the coordinates of our geometric shapes according to the size of our canvas.

[**home**](https://github.com/djsnipa1/p5js-designing-interactive-patterns#contenu)  

## [](https://github.com/djsnipa1/p5js-designing-interactive-patterns#une-page-web-responsive---dessiner-un-cercle-qui-reste-au-milieu)A responsive web page - Draw a circle that stays in the middle

Everything is said in the title !

The first step, as previously stated, consists of creating a **canvas** which will take the entire size available on our web page. Instead of using the processing _size() function we will use the_ [**createCanvas()**](https://p5js.org/reference/%23/p5/createCanvas) function . For this canvas to take the entire size of our browser window we will pass two variables [**windowWidth**](https://p5js.org/reference/%23/p5/windowWidth) and [**windowHeight**](https://p5js.org/reference/%23/p5/windowHeight) . As specified in the documentation, these variables are system variables, meaning that they exist and are accessible everywhere in our javascript code and do not need to be declared.

```js
function setup() {
  createCanvas(windowWidth, windowHeight); 
  // createCanvas(800, 600);
  background(180);
}
function draw(){
  background(180);
}
```

By typing or copying/pasting this little piece of code, when you click on the _play_ button you will see a magnificent gray page appear taking up the entire surface of your window.

Note that if you resize your window, scroll bars will appear at the bottom right to move you through your page. This means that your canvas is larger than the web page in which it is displayed. Indeed the canvas is created in setup() and therefore only once when the page is displayed or refreshed and it keeps its initial size.

You can try commenting out the _createCanvas(windowWidth, windowHeight);_ by putting "//" in front to deactivate it (lines of code preceded by two slashes are not executed by our browser) and uncomment the line below (by removing the two slashes preceding it). You will then see a gray square smaller than our browser window which will not change size either when the page is resized.

We must therefore be able to resize our canvas to the size of our window when the user changes its size. [**The windowResize()**](https://p5js.org/reference/%23/p5/windowResized) function is made for just this! It allows the code located between its curly brackets '{}' to be executed when the user resizes their browser window. All we then have to do is call the [**resizeCanvas**](https://p5js.org/reference/%23/p5/resizeCanvas) function to resize our canvas to the new size of our window by again calling on the **windowWidth** and **windowHeight** variables which have changed their value following our user's action.

```js
function setup() {
  createCanvas(windowWidth, windowHeight); 
  // createCanvas(800, 600);
  background(180);
}
function draw(){
    
}

function windowResized() {
  resizeCanvas(windowWidth, windowHeight);
}
```

So this time it’s good! our canvas remains the size of our browser window. We will now make sure to draw a circle in the middle of our canvas and try to make it stay in the middle.

As a reminder, the processing coordinate system places the origin of our coordinate system in the upper left corner of our canvas:

[https://www.openprocessing.org/sketch/388459](https://www.openprocessing.org/sketch/388459)

If we want to draw a circle in the middle of our window and it remains in the middle we must therefore express its coordinates according to [**width**](https://p5js.org/reference/%23/p5/width) and [**height**](https://p5js.org/reference/%23/p5/height) which are the width and height of our drawing area.

[**By adding a call to the ellipse()**](https://p5js.org/reference/%23/p5/ellipse) function in the draw(), we can make our circle stay in the middle of our window regardless of its size:

```js
fill(255);
ellipse(width*0.5, height*0.5, 50, 50);
```

If we want our designs / patterns to be responsive and keep a similar appearance whatever the size of our window we must succeed in expressing all the coordinates of our shapes using percentages (i.e. by multiplying or _width_ or _height_ by a value between 0 and 1)

[**home**](https://github.com/djsnipa1/p5js-designing-interactive-patterns#contenu)  

## [](https://github.com/djsnipa1/p5js-designing-interactive-patterns#dessiner-une-grille---vive-les-boucles-for-)Draw a grid - long live for loops!

### [](https://github.com/djsnipa1/p5js-designing-interactive-patterns#premiere-grille)First grid

[**We will use for()**](https://processing.org/reference/for.html) loops . For loops are very useful for automating an action that will have to be repeated several times.

The generic syntax for a for loop looks like this:

```js
for ( /* écrire les conditions qui régissent l'execution*/){
    // écrire le code à exécuter si les conditions sont respectées
}
```

The **execution conditions** are specified in three steps separated by semicolons, these steps must be specified in parentheses following the **for** keyword :

-   declare and initialize a variable
-   do a test on this variable to find out if we should execute the code enclosed in braces.
-   manipulate the variable for the next execution.

For example, if you write this in the setup:

```js
for (let i = 0 ; i < 10 ; i = i+1){
    println(i);
}
```

You will repeat the "println(i)" action ten times; this will have the effect of printing the value of the variable i in the console as long as it is less than 10.

Here is what the computer will understand:

1 - First iteration - i is 0 - 0 is less than 10 - I print i (i.e. 0) in the console - I add 1 to i

2 - Second iteration - i is worth 1 (last step of the previous iteration) - 1 is less than 10 - I print i (i.e. 1) in the console - I add 1 to i (which will therefore be worth 2)

(..)

11 - Eleventh iteration - i is 10 - 10 is no longer less than 10 - I exit the loop and execute the next line of code located after the closing brace.

By manipulating the initialization, end and increment conditions of the loop we will be able to create a number of visual effects. Let's start by trying to draw vertical lines sweeping across the screen every 50 pixels.

In the draw() you can type this loop:

```js
for (let i = 0 ; i < width ; i += 50){
    line(i,0,i,height);
}
```

You will get something like this:

[![Green](https://github.com/djsnipa1/p5js-designing-interactive-patterns/raw/master/images/vertical-lines.png)](https://github.com/djsnipa1/p5js-designing-interactive-patterns/blob/master/images/vertical-lines.png)

You should be able to fairly easily write a loop that would allow you to obtain a series of horizontal lines equally spaced 50 pixels apart:

[![hor](https://github.com/djsnipa1/p5js-designing-interactive-patterns/raw/master/images/horizontal-lines.png)](https://github.com/djsnipa1/p5js-designing-interactive-patterns/blob/master/images/horizontal-lines.png)

Then finally a 100 spacing grid by combining two for loops, one inside the other.

[![hor](https://github.com/djsnipa1/p5js-designing-interactive-patterns/raw/master/images/grid.png)](https://github.com/djsnipa1/p5js-designing-interactive-patterns/blob/master/images/grid.png)

Note here that the coordinates (i,j) which are calculated by the nesting of our two loops give us the upper left point of each box.

```js
for (let i = 0; i <= width; i += 100) {
    for (let j = 0; j <= height; j+= 100) {
        line(i,0,i,height);
        line(0,j,width,j);
    }
}
```

[**home**](https://github.com/djsnipa1/p5js-designing-interactive-patterns#contenu)  

### [](https://github.com/djsnipa1/p5js-designing-interactive-patterns#une-grille-de-cercles)A grid of circles

We will now try to draw a grid of circles:

[![circle-grid](https://github.com/djsnipa1/p5js-designing-interactive-patterns/raw/master/images/circlegrid.gif)](https://github.com/djsnipa1/p5js-designing-interactive-patterns/blob/master/images/circlegrid.gif)

```js
for (let i = 0; i <= width; i += 100) {
    for (let j = 0; j <= height; j+= 100) {
        ellipse(i,j,100,100);
        line(i,0,i,height);
        line(0,j,width,j);
    }
}
```

The ellipse() function takes the center coordinates of the circle as parameters, our circle is drawn around each intersection.

[![circles-inter](https://github.com/djsnipa1/p5js-designing-interactive-patterns/raw/master/images/circles-intersection.png)](https://github.com/djsnipa1/p5js-designing-interactive-patterns/blob/master/images/circles-intersection.png)

In this example our circles have a fixed size of 100 pixels. We will now make these circles change size every time we click the mouse.

[**home**](https://github.com/djsnipa1/p5js-designing-interactive-patterns#contenu)  

#### [](https://github.com/djsnipa1/p5js-designing-interactive-patterns#un-peu-dinteraction-changer-la-taille-des-cases)a little interaction change the size of the boxes

First of all we will need to create a variable which will be the size of each box and which will therefore correspond to the value by which we increase each variable in the for loop. This variable could for example be called "slotSize" and we will initialize it with a value of 100.

Before setup() (and this so that our variable is available throughout our program), we can therefore write this line which is used to declare and initialize a variable.

```js
let slotSize = 100;
```

We will now use our variable in our for loop (which is in the draw()) to adjust the size of our boxes and our ellipse to the value contained in the slotSize variable (here 100 for the moment but we will be able to change it later) - just replace "100" with "slotSize" in our two nested for loops:

```js
for (let i = 0; i <= width; i += slotSize) {
    for (let j = 0; j <= height; j+= slotSize) {
        ellipse(i,j,slotSize,slotSize);
        line(i,0,i,height);
        line(0,j,width,j);
    }
}
```

All we have to do now is manipulate our slotSize variable and give it new values: we will make this value change to a random value each time we press the mouse. To do this, simply use the [**mousePressed()**](https://p5js.org/reference/%23/p5/mousePressed) function : each time we press the mouse the code between the braces will be executed. We then want to use [**random()**](https://p5js.org/reference/%23/p5/random) to assign our "slotSize" variable a new random value between a minimum value and a maximum value.

```
function mousePressed() {
    slotSize = random(10, 200);
}
```

Note that mousePressed() is a new function which must therefore be located outside of setup() and draw().

[**home**](https://github.com/djsnipa1/p5js-designing-interactive-patterns#contenu)

#### [](https://github.com/djsnipa1/p5js-designing-interactive-patterns#des-cercles-centres-dans-nos-cases)circles centers in our boxes

We will now make our circles centered in our boxes. We will therefore manipulate the start and stop conditions of our loops so that "i" and "j" give us the center of the boxes rather than the upper left corner.

[![circles-cente](https://github.com/djsnipa1/p5js-designing-interactive-patterns/raw/master/images/circles-centered.png)](https://github.com/djsnipa1/p5js-designing-interactive-patterns/blob/master/images/circles-centered.png)

Our boxes are square and of size "slotSize", so we just need to add half the slotSize to i and j to get the center of each box.

```js
fill(255);
for (let i = 0; i <= width ; i += slotSize) {
    for (let j = 0; j <= height ; j += slotSize) {
        line(i, 0, i, height);
        line(0, j, width, j);
    }
}

for (let i = slotSize / 2; i <= width - slotSize / 2; i += slotSize) {
    for (let j = slotSize / 2; j <= height - slotSize / 2; j += slotSize) {
        ellipse(i, j, slotSize, slotSize);  
    }
}
```

Notice that when you resize your window, some circles appear or disappear at the border and that our grid is not centered. We will try to remedy this.

You can find the program [here](https://b2renger.github.io/p5js-designing-interactive-patterns/sketch_01_b_responsive_grid/)

As well as the code: [https://github.com/b2renger/p5js-designing-interactive-patterns/tree/master/sketch\_01\_b\_responsive\_grid](https://github.com/b2renger/p5js-designing-interactive-patterns/tree/master/sketch_01_b_responsive_grid)

[**home**](https://github.com/djsnipa1/p5js-designing-interactive-patterns#contenu)

#### [](https://github.com/djsnipa1/p5js-designing-interactive-patterns#une-grille-centree-dans-notre-page)a grid centered in our page

There are several options here:

-   either we know the number of boxes that we want to display in width and height and we calculate the size of our increments (the 'i = i+100' part) so that the right number of boxes is created.
    
-   either we know the size of the boxes that we want to display and we calculate the number of boxes according to the size of the window.
    

Given what we have achieved so far, we will opt for the second option. Besides, the description of what we must achieve is not entirely accurate. It is not guaranteed that the random number we will come across when clicking the mouse is a multiple of the size of our window... especially since this number is potentially a decimal number and our user can change the size of the window as he sees fit... so it's a little more complicated...

We need to calculate the maximum number of boxes that can fit in our window based on the size of the boxes and the size of our window.

Depending on the result of this calculation we will be left with an empty space which will be less than the size of a box. We can divide this value (in pixels) of the remaining space by two to create a margin at the top and bottom and a margin on the right and left.

We must therefore start by declaring global variables (at the very top of our program) outside of any braces

```js
let marginX;
let marginY;
```

Then in setup(), we need to calculate the size of our margins. We must divide the width and height of our window respectively by the size of our boxes. We must take the entire part of this division and multiply it by the size of each of our boxes. If we subtract this result from each dimension of our window we obtain in pixels the space remaining in pixels once we have displayed a maximum of boxes, i.e. twice our margin.

```js
marginX = windowWidth - int((windowWidth / slotSize)) * slotSize;
marginY = windowHeight - int((windowHeight / slotSize)) * slotSize;
```

This calculation must be carried out in setup() so that our grid is displayed correctly when our page loads and it must be redone each time our page changes size (i.e. in the _windowResized()_ function after the _resizeCanvas call ()_ ) but also when we change the size of our boxes (i.e. in the _mousePressed()_ function after the call to _random()_ to specify a new box size).

We must now use these two new variables in the start and stop conditions of our for loop:

```js
for (let i = marginX / 2 + slotSize / 2; i < width - marginX / 2; i += slotSize) {
    for (let j = marginY / 2 + slotSize / 2; j < height - marginY / 2; j += slotSize) {
        fill(255)
        rect(i, j, slotSize, slotSize);
        fill(255)
        ellipse(i, j, slotSize, slotSize);        
    }
}
```

And here we finally arrive at the result of the gif displayed previously. From now on the code that you will write will mainly be located inside these two for loops; it is possible to do a lot of things. The code we have written so far will be your starting point for creating geometric tilings, each one more beautiful than the next!

This code will be the basis for most of the programs we create:

```js
let slotSize = 100;
let marginX;
let marginY;

function setup() {
    createCanvas(windowWidth, windowHeight);
    background(180);
    pixelDensity(1);

    marginX = windowWidth - int((windowWidth / slotSize)) * slotSize;
    marginY = windowHeight - int((windowHeight / slotSize)) * slotSize;
}


function draw() {
    background(180)
    for (let i = marginX / 2 + slotSize / 2; i < width - marginX / 2; i += slotSize) {
        for (let j = marginY / 2 + slotSize / 2; j < height - marginY / 2; j += slotSize) {
            // code here

        }
    }
}

function mousePressed(){
    slotSize = random(10, 200);
    marginX = windowWidth - int((windowWidth / slotSize)) * slotSize;
    marginY = windowHeight - int((windowHeight / slotSize)) * slotSize;
}

function windowResized() {
    resizeCanvas(windowWidth, windowHeight);
    marginX = windowWidth - int((windowWidth / slotSize)) * slotSize;
    marginY = windowHeight - int((windowHeight / slotSize)) * slotSize;
}
```

You can find the program [here](https://b2renger.github.io/p5js-designing-interactive-patterns/sketch_01_c_responsive_grid/)

As well as the code: [https://github.com/b2renger/p5js-designing-interactive-patterns/tree/master/sketch\_01\_c\_responsive\_grid](https://github.com/b2renger/p5js-designing-interactive-patterns/tree/master/sketch_01_c_responsive_grid)

[**home**](https://github.com/djsnipa1/p5js-designing-interactive-patterns#contenu)

## [](https://github.com/djsnipa1/p5js-designing-interactive-patterns#un-peu-dinteraction-avec-la-souris)A little interaction with the mouse

### [](https://github.com/djsnipa1/p5js-designing-interactive-patterns#une-grille-de-cercles-qui-changent-de-taille-en-fonction-de-la-position-de-la-souris)A grid of circles that change size depending on mouse position

Our next program is very simple and is based on the code seen previously, here it is:

[![circle grid map mouse](https://github.com/djsnipa1/p5js-designing-interactive-patterns/raw/master/images/circlegrid-size.gif)](https://github.com/djsnipa1/p5js-designing-interactive-patterns/blob/master/images/circlegrid-size.gif)

This involves drawing a circle in each box and matching its size to the distance that separates the mouse from the center of each circle: if the mouse is close, the circle is big, if it is far away, the circle is small. .

To draw circles in each box it's easy: just call the [ellipse()](https://p5js.org/reference/%23/p5/ellipse) function inside the double for loop using as coordinates of the center of each ellipse the variables i and j which vary over time. execution of loops.

```js
for (let i = marginX / 2 + slotSize / 2; i < width - marginX / 2; i += slotSize) {
        for (let j = marginY / 2 + slotSize / 2; j < height - marginY / 2; j += slotSize) {
            // code here
            ellipse(i,j, slotSize, slotSize);                                                                              
        }
}
```

To calculate the distance there is the [**dist()**](https://p5js.org/reference/%23/p5/dist) function , which allows you to calculate the distance between two points.

We need to calculate the distance between the mouse and each of the points on our grid. This will therefore have to be done for each box, so we will create a variable that we will name 'd' to store this distance.

```js
for (let i = marginX / 2 + slotSize / 2; i < width - marginX / 2; i += slotSize) {
        for (let j = marginY / 2 + slotSize / 2; j < height - marginY / 2; j += slotSize) {
            // code here
            let d = dist(mouseX,mouseY,i,j)
            ellipse(i,j, slotSize, slotSize);                       
        }
}
```

Now all we have to do is calculate the size of our circles based on the calculated distance. For this we will use a rule of three or rule of proportionality whose calculation can be carried out by the [**map()**](https://p5js.org/reference/%23/p5/map) function . **map()** takes 5 parameters, the first and the value that we wish to transform, the next two are the minimum and maximum values that this value can take, and the last two are the minimum and maximum values that we want in exit.

The minimum values we want in output are "5" pixels and "slotSize" pixels: so that if the mouse is right on the center of a circle it takes the maximum possible size in its box.

The minimum value that the distance between the mouse and the center of a circle can take is naturally zero, the maximum distance can be solved with a very simple application of the Pythagorean theorem in our drawing window. The largest possible distance in our window is the size of a diagonal (if our mouse is at the top left we want our point at the bottom right to be as small as possible). We must therefore calculate the diagonal of our window:

```js
let dmax = sqrt(width*width + height*height);
```

We can now apply our rule of three or "mapping" - paying attention to the direction in which we want it to apply (when the distance is 0, the circle must be of maximum size):

```js
let s = map(d, 0, dmax, slotSize, 1)
```

We can also combine the calculation of 'd', 'dmax' and 's' in a single line if we wish:

```js
let s = map(dist(i,j,mouseX,mouseY), 0, sqrt(width*width + height*height), slotSize, 1)
```

Here is to summarize the content of the **draw()** allowing to obtain the result presented in the preceding gif:

```js
background(0)
for (let i = marginX / 2 + slotSize / 2; i < width - marginX / 2; i += slotSize) {
    for (let j = marginY / 2 + slotSize / 2; j < height - marginY / 2; j += slotSize) {
        let s = map(dist(i, j, mouseX, mouseY), 0, sqrt(width * width + height * height), slotSize, 1);
        ellipse(i, j, s, s);
    }
}
```

You can find the program [here](https://b2renger.github.io/p5js-designing-interactive-patterns/sketch_02_a_interactive_grid/)

As well as the code: [https://github.com/b2renger/p5js-designing-interactive-patterns/tree/master/sketch\_02\_a\_interactive\_grid](https://github.com/b2renger/p5js-designing-interactive-patterns/tree/master/sketch_02_a_interactive_grid)

[**home**](https://github.com/djsnipa1/p5js-designing-interactive-patterns#contenu)

### [](https://github.com/djsnipa1/p5js-designing-interactive-patterns#une-grille-de-cercles-concentriques)A grid of concentric circles

Since the more for loops we have, the more fun we have! we are going to add a third for loop inside our two previous loops. This means that for each box drawn we will repeat the same action several times.

[![circle grid of co-centric circles](https://github.com/djsnipa1/p5js-designing-interactive-patterns/raw/master/images/circle-grid-of-circles-overlapping.gif)](https://github.com/djsnipa1/p5js-designing-interactive-patterns/blob/master/images/circle-grid-of-circles-overlapping.gif)

Starting from approximately the same base as before, we will be careful to modify the filling of our shapes to no longer have any with [\*\*noFill()](https://p5js.org/reference/%23/p5/noFill) - exactly as in processing and to have a white shape outline with [**stroke( )**](https://p5js.org/reference/%23/p5/stroke) , also as in processing.

```js
background(0)
noFill();
stroke(255)
for (let i = marginX / 2 + slotSize / 2; i < width - marginX / 2; i += slotSize) {
    for (let j = marginY / 2 + slotSize / 2; j < height - marginY / 2; j += slotSize) {
    
           
    }
}
```

Inside these two for loops we will therefore be able to add a third! This third loop will allow us to draw circles with the same center but whose size decreases with each iteration of the loop:

```js
for (let k = slotSize; k > 0; k = k - 10) {
    ellipse(i , j, k, k);                                                           
}
```

We will now ensure that this number of co-centric circles can change, notably randomly when we press the mouse.

We will therefore create a new variable at the very top of our program (apart from setup() and draw())

```js
let niterations = 5;
```

and we will use it to control the increment of "k" in our for loop. The number of times we are going to repeat the action and "niterations", we must therefore reduce the size of our ellipse by "slotSize/niterations".

```js
for (let k = slotSize; k > 0; k = k - slotSize/niterations) {
    ellipse(i , j, k, k);                                                           
}
```

Now we can call the **random()** function inside our **mousePressed()** function , but be careful this time we want an integer, while random() returns comma (or float) numbers by default. To remedy this, simply take the integer part of the number returned by random() using the [**int()**](https://p5js.org/reference/%23/p5/int) function .

```js
niterations = int(random(2, 20))
```

To achieve the result presented in the gif, we now just need to manipulate the size of the circles depending on the position of the mouse in the window. This size must change for each circle, so we will calculate it inside the three loops.

We are not going to directly calculate the size of each ellipse, but rather a multiplier coefficient by which we will multiply the size already precalculated by our for('k') loop.

```js
let s = map(mouseX, 0, width, 0.5, 5);
ellipse(i , j , k *s, k*s);
```

Here is the complete draw() code represented by the previous gif.

```js
background(0);
noFill();
stroke(255);
for (let i = marginX / 2 + slotSize / 2; i < width - marginX / 2; i += slotSize) {
    for (let j = marginY / 2 + slotSize / 2; j < height - marginY / 2; j += slotSize) {
        for (let k = slotSize; k > 0; k = k - slotSize/niteration) {
            let s = map(mouseX, 0, width, 0.5, 5);
            ellipse(i , j , k *s, k*s);
         }
    }
}
```

You can find the program [here](https://b2renger.github.io/p5js-designing-interactive-patterns/sketch_02_b_triple-for/)

As well as the code: [https://github.com/b2renger/p5js-designing-interactive-patterns/tree/master/sketch\_02\_b\_triple-for](https://github.com/b2renger/p5js-designing-interactive-patterns/tree/master/sketch_02_b_triple-for)

[**home**](https://github.com/djsnipa1/p5js-designing-interactive-patterns#contenu)

### [](https://github.com/djsnipa1/p5js-designing-interactive-patterns#une-grille-de-lignes-interactives)A grid of interactive lines

We will now focus on making this pattern:[![Moving lines patterns](https://github.com/djsnipa1/p5js-designing-interactive-patterns/raw/master/images/moving-lines-pattern.gif)](https://github.com/djsnipa1/p5js-designing-interactive-patterns/blob/master/images/moving-lines-pattern.gif)

This pattern is made by connecting each corner of each box to a point moving inside each box. The position of this point depends on the position of the mouse in the window: when the mouse is to the right of the window then the moving point is to the right of each of the boxes, when it is at the top of the window the point is also at the top of each box etc.

We therefore want to "map" (with the map() function!) the position of our mouse which moves throughout the window to the position of the moving point moving in its box.

We will therefore have to calculate an offset. In the same way as before we are not going to directly calculate the offset but rather a coefficient, i.e. a value that we are going to multiply by another to obtain this offset.

We want when our mouse moves across the width or height we have an offset centered around zero.

```js
let xOffset = map(mouseX, 0, width, -0.5, 0.5)
let yOffset = map(mouseY, 0, height, -0.5, 0.5)
```

This calculation being the same for each case we can do it in draw() but just before our for loops.

All we have to do now is draw our lines using the [**line()**](https://p5js.org/reference/%23/p5/line) function . We therefore need to define two points for each line: the corners of each box and the moving point.

The moving point always has coordinates in each box:

```
(i + xOffset * (slotSize), j + yOffset * (slotSize))
```

(i,j) being the coordinates of the center of a box we add or subtract half the size of our box, depending on the value taken by 'xOffset' and 'yOffset' which are themselves defined by the position of the mouse in the window.

The coordinates of the upper left points of each box (we shift by half the size of the box on the abscissa and on the ordinate)

```
(i - slotSize * 0.5, j - slotSize * 0.5)
```

It is then quite easy to calculate the coordinates of each of the corners of each box:

-   upper right corner:

```
(i + slotSize * 0.5, j - slotSize * 0.5)
```

-   lower right corner:

```
(i + slotSize * 0.5, j + slotSize * 0.5)
```

-   lower left corner:

```
(i - slotSize * 0.5, j + slotSize * 0.5)
```

It then remains to draw the four lines:

```js
for (let i = marginX / 2 + slotSize / 2; i < width - marginX / 2; i += slotSize) {
    for (let j = marginY / 2 + slotSize / 2; j < height - marginY / 2; j += slotSize) {

        let xOffset = map(mouseX, 0, width, -0.5, 0.5)
        let yOffset = map(mouseY, 0, height, -0.5, 0.5)
        line(i + xOffset * (slotSize), j + yOffset * (slotSize),
                i - slotSize * 0.5, j - slotSize * 0.5);
        line(i + xOffset * (slotSize), j + yOffset * (slotSize),
                i + slotSize * 0.5, j + slotSize * 0.5);
        line(i + xOffset * (slotSize), j + yOffset * (slotSize),
                i + slotSize * 0.5, j - slotSize * 0.5);
        line(i + xOffset * (slotSize), j + yOffset * (slotSize),
                i - slotSize * 0.5, j + slotSize * 0.5);

    }
}
```

You can find the program [here](https://b2renger.github.io/p5js-designing-interactive-patterns/sketch_02_d_triple-for-lines/)

As well as the code: [https://github.com/b2renger/p5js-designing-interactive-patterns/tree/master/sketch\_02\_d\_triple-for-lines](https://github.com/b2renger/p5js-designing-interactive-patterns/tree/master/sketch_02_d_triple-for-lines)

[**home**](https://github.com/djsnipa1/p5js-designing-interactive-patterns#contenu)

### [](https://github.com/djsnipa1/p5js-designing-interactive-patterns#une-grille-de-cercles-concentriques-2)A grid of concentric circles 2

We will now combine the two previous effects: we will manipulate the position of the centers of co-centric circles to give an effect of false 3D made from real 2D

[![circle grid of co-centric circles](https://github.com/djsnipa1/p5js-designing-interactive-patterns/raw/master/images/circle-grid-of-circles.gif)](https://github.com/djsnipa1/p5js-designing-interactive-patterns/blob/master/images/circle-grid-of-circles.gif)

So let's drop the part of manipulating the diameter of our circles:

```js
background(0);
noFill();
stroke(255);
for (let i = marginX / 2 + slotSize / 2; i < width - marginX / 2; i += slotSize) {
    for (let j = marginY / 2 + slotSize / 2; j < height - marginY / 2; j += slotSize) {
        for (let k = slotSize; k > 0; k = k - slotSize/niteration) {
            ellipse(i , j , k , k);
         }
    }
}
```

In the same way as before we will calculate an offset:

```js
let xOffset = map(mouseX, 0, width, -0.5, 0.5)
let yOffset = map(mouseY, 0, height, -0.5, 0.5)
```

Following this, if we observe our animation carefully, we notice that the offset is greater for the small circles - those close to the center and non-existent for the larger circles.

To be able to do this, we must ensure that when the size of our circle is maximum, the value by which we will multiply our offset is zero: to cancel the offset. And conversely when our circle size is minimum this value is larger to have the full effect of the offset; this value is therefore

```js
(slotSize - k)
```

All we have to do is apply the result of our calculations to the positions of the centers of our circles.

```js
let centerX = i + xOffset * (slotSize-k);
let centerY = j + yOffset * (slotSize-k);
```

and There you go !

```js
let xOffset = map(mouseX, 0, width, -0.5, 0.5)
let yOffset = map(mouseY, 0, height, -0.5, 0.5)
let centerX = i + xOffset * (slotSize-k);
let centerY = j + yOffset * (slotSize-k);
ellipse(centerX,centerY, k, k);
```

```js
background(0);
noFill();
stroke(255);
for (let i = marginX / 2 + slotSize / 2; i < width - marginX / 2; i += slotSize) {
    for (let j = marginY / 2 + slotSize / 2; j < height - marginY / 2; j += slotSize) {
        for (let k = slotSize; k > 0; k = k - slotSize/niteration) {
            let xOffset = map(mouseX, 0, width, -0.5, 0.5)
            let yOffset = map(mouseY, 0, height, -0.5, 0.5)
            let centerX = i + xOffset * (slotSize-k);
            let centerY = j + yOffset * (slotSize-k);
            ellipse(centerX,centerY, k, k);
         }
    }
}
```

You can find the program [here](https://b2renger.github.io/p5js-designing-interactive-patterns/sketch_02_c_triple-for/)

As well as the code: [https://github.com/b2renger/p5js-designing-interactive-patterns/tree/master/sketch\_02\_c\_triple-for](https://github.com/b2renger/p5js-designing-interactive-patterns/tree/master/sketch_02_c_triple-for)

[**home**](https://github.com/djsnipa1/p5js-designing-interactive-patterns#contenu)

## [](https://github.com/djsnipa1/p5js-designing-interactive-patterns#ecrire-des-conditions-avec-if)Write conditions with if()

We will now stay on the same principle and see how a very simple rule can give us a multitude of relatively varied patterns: the principle is that in each box we will choose to draw one of the two possible diagonals.

[![10print](https://github.com/djsnipa1/p5js-designing-interactive-patterns/raw/master/images/10print.gif)](https://github.com/djsnipa1/p5js-designing-interactive-patterns/blob/master/images/10print.gif)

As usual, we will start from our base code

```js
let slotSize = 100;
let marginX;
let marginY;

function setup() {
    createCanvas(windowWidth, windowHeight);
    background(180);
    pixelDensity(1);

    marginX = windowWidth - int((windowWidth / slotSize)) * slotSize;
    marginY = windowHeight - int((windowHeight / slotSize)) * slotSize;
}


function draw() {
    background(180)
    for (let i = marginX / 2 + slotSize / 2; i < width - marginX / 2; i += slotSize) {
        for (let j = marginY / 2 + slotSize / 2; j < height - marginY / 2; j += slotSize) {
            // code here

        }
    }
}

function mousePressed(){
    slotSize = random(10, 200);
    marginX = windowWidth - int((windowWidth / slotSize)) * slotSize;
    marginY = windowHeight - int((windowHeight / slotSize)) * slotSize;
}

function windowResized() {
    resizeCanvas(windowWidth, windowHeight);
    marginX = windowWidth - int((windowWidth / slotSize)) * slotSize;
    marginY = windowHeight - int((windowHeight / slotSize)) * slotSize;
}
```

As a reminder, this code allows us to obtain a grid that responds to changes in the size of our window.

The code that we are going to write is quite simple, it involves understanding how an **if()** condition is written.

As with the for loop, we must understand the meaning of the punctuation symbols we use: parentheses allow us to delimit a condition / a test, and braces allow us to delimit the actions to be performed if our condition is true:

```js
if( ma-condition-est-vraie ) {
    // j'execute le code écrit ici.
}
```

An **if(){}** can be followed by an \* _else{}_ in order to define another action to be performed if the condition is false.

```js
if( ma-condition-est-vraie ) {
    // j'execute le code écrit ici.
}
else{
    // j'éxecute ce code plutôt
}
```

We can also chain conditions:

```js
if( ma-condition-est-vraie ) {
    // j'execute le code écrit ici.
}
else if( une-autre-condition-est-vraie){
    // j'éxecute ceci
}
else{
    // j'éxecute ce code plutôt
}
```

Where to nest them:

```js
if( ma-condition-est-vraie ) {
    if( une-seconde-condition-est-vraie){
    // j'éxecute ceci
    }
    else {
    // j'éxecute cela
    }
}
else{
    // j'éxecute ce code plutôt
}
```

[**home**](https://github.com/djsnipa1/p5js-designing-interactive-patterns#contenu)

### [](https://github.com/djsnipa1/p5js-designing-interactive-patterns#if-else-et-random---randomseed)if-else and random() - randomSeed()

In our first example we will only have one simple condition to execute: we want to randomly draw one or the other of the diagonals.

In each box we must therefore determine the coordinates of the corners according to (i,j) the point defining the center of our box and 'slotSize' which is the size of our box.

So the first diagonal - the one starting from the lower left corner is written like this:

```js
line(i - slotSize / 2, j - slotSize / 2, i + slotSize / 2, j + slotSize / 2)
```

and the second - the one starting from the upper left corner is written like this:

```js
line(i - slotSize / 2, j + slotSize / 2, i + slotSize / 2, j - slotSize / 2)
```

So all we have to do is write a condition allowing us to draw one or the other of these diagonals. To do this we will carry out a test (ie write a condition) using the [**random()**](https://p5js.org/reference/%23/p5/random) function that we already know.

If we want an approximately uniform distribution of each of the two diagonals, we will simply check whether the result of 'random(1)' is greater than '0.5' or not

```js
if (random(1) > 0.5) {
   
} else {
    
}
```

and draw one of the two diagonals in one case, and the other otherwise:

```js
 if (random(1) > 0.5) {
    line(i - slotSize / 2, j - slotSize / 2, i + slotSize / 2, j + slotSize / 2)
} else {
    line(i - slotSize / 2, j + slotSize / 2, i + slotSize / 2, j - slotSize / 2)
}
```

Unfortunately, random() returns us random results by definition. This means that every time an image is calculated (each time draw() executes) a new value is drawn and our image keeps changing.

In reality, randomness does not really exist in computing. The random() functions of various languages all return a sequence of pseudo-random numbers, even if this may seem disappointing it is actually very practical in our case (incidentally it also allows you to recreate a specific image even with intensive use to random()).

The random() function is therefore always accompanied by a [**randomSeed()**](https://p5js.org/reference/%23/p5/randomSeed) function . This function allows us to give a "seed" to our random() function and for a given "seed" random() will always return the same sequence of random numbers.

We will therefore create a new variable at the very top of our program (apart from setup() and draw()):

```js
let seed;
```

In _setup()_ , we will give a new initial value to this variable:

```js
seed = random(9999)
```

Here we use random, but to get a precise image we can give "seed" a precise value.

Now in the _draw()_ we can use this "seed" by calling the **randomSeed()** function . This call must be made for each "frame" but does not need to be made for each box of our grid, we can therefore put it at the very top of our _draw()_

```js
randomSeed(seed)
```

Our images therefore now remain fixed whatever happens. To return to a more generative side we can now change our seed each time the user presses the mouse and therefore add a line of code allowing the "seed" to be randomly changed in the _mousePressed() function_

```js
function mousePressed(){
    seed = random(9999)
}
```

We can also randomize the thickness of the line when the user clicks the mouse

```js
strokeWeight(random(20))
```

Here is the entire generative program:

```js
let slotSize = 50;
let marginX;
let marginY;
let seed

function setup() {

    createCanvas(windowWidth, windowHeight);
    background(180);

    pixelDensity(1);

    marginX = windowWidth - int((windowWidth / slotSize)) * slotSize;
    marginY = windowHeight - int((windowHeight / slotSize)) * slotSize;

    seed = random(9999)
}


function draw() {
    randomSeed(seed)
    background(0)
    noFill();
    stroke(255)
    for (let i = marginX / 2 + slotSize / 2; i < width - marginX / 2; i += slotSize) {
        for (let j = marginY / 2 + slotSize / 2; j < height - marginY / 2; j += slotSize) {

            if (random(1) > 0.5) {
                line(i - slotSize / 2, j - slotSize / 2, i + slotSize / 2, j + slotSize / 2)
            } else {
                line(i - slotSize / 2, j + slotSize / 2, i + slotSize / 2, j - slotSize / 2)
            }

        }
    }
}

function mousePressed() {
    seed = random(9999)
    slotSize = random(10, 200)
    strokeWeight(random(10))
    marginX = windowWidth - int((windowWidth / slotSize)) * slotSize;
    marginY = windowHeight - int((windowHeight / slotSize)) * slotSize;
}


function windowResized() {
    resizeCanvas(windowWidth, windowHeight);
    marginX = windowWidth - int((windowWidth / slotSize)) * slotSize;
    marginY = windowHeight - int((windowHeight / slotSize)) * slotSize;
}
```

```
Vous pouvez retrouver le programme [ici](https://b2renger.github.io/p5js-designing-interactive-patterns/sketch_03_a_if/)

Ainsi que le code : https://github.com/b2renger/p5js-designing-interactive-patterns/tree/master/sketch_03_a_if  

[**home**](#contenu)
```

### [](https://github.com/djsnipa1/p5js-designing-interactive-patterns#variation-1-avec-if-imbriques)Variation 1 with nested if

As previously stated, we can also nest ifs together. For example, we could make some lines red and others white quite easily:

[![10-print2](https://github.com/djsnipa1/p5js-designing-interactive-patterns/raw/master/images/10print-2.png)](https://github.com/djsnipa1/p5js-designing-interactive-patterns/blob/master/images/10print-2.png)

```js
 if (random(1) > 0.5) {
                
    if (random(1) > 0.75 ){
        stroke(255,0,0)
    }
    else {
        stroke(255)
    }
    line(i - slotSize / 2, j - slotSize / 2, i + slotSize / 2, j + slotSize / 2)
                       
} else {
    if (random(1) > 0.75 ){
        stroke(255,0,0)
    }
    else {
        stroke(255)
    }              
    line(i - slotSize / 2, j + slotSize / 2, i + slotSize / 2, j - slotSize / 2)
}
```

You can find the program [here](https://b2renger.github.io/p5js-designing-interactive-patterns/sketch_03_b_if/)

As well as the code: [https://github.com/b2renger/p5js-designing-interactive-patterns/tree/master/sketch\_03\_b\_if](https://github.com/b2renger/p5js-designing-interactive-patterns/tree/master/sketch_03_b_if)

[**home**](https://github.com/djsnipa1/p5js-designing-interactive-patterns#contenu)

### [](https://github.com/djsnipa1/p5js-designing-interactive-patterns#variation-2-avec-if---else-if)Variation 2 with if - else if

With the use of several conditions linked together it is also relatively simple to draw in a labyrinth, and choosing to draw only one wall of each box (either the one above, or the one below, the one on the left or the one on the right):

[![10-pint_3](https://github.com/djsnipa1/p5js-designing-interactive-patterns/raw/master/images/10print-3.png)](https://github.com/djsnipa1/p5js-designing-interactive-patterns/blob/master/images/10print-3.png)

```js
var rd = random(1)
if (rd < 0.25) {
    line(i -slotSize/2, j - slotSize/2, i-slotSize/2, j + slotSize/2); // left
} else if (rd > 0.25 && rd < 0.50) {
    line(i + slotSize/2, j-slotSize/2, i + slotSize/2, j + slotSize/2); // down
} else if (rd > 0.50 && rd < 0.75) {
    line(i-slotSize/2, j-slotSize/2, i + slotSize/2, j-slotSize/2); // up
} else if (rd > 0.25 && rd < 0.50) {
    line(i + slotSize/2, j - slotSize/2, i + slotSize/2, j + slotSize/2); //right
}
```

You can find the program [here](https://b2renger.github.io/p5js-designing-interactive-patterns/sketch_03_c_if/)

As well as the code: [https://github.com/b2renger/p5js-designing-interactive-patterns/tree/master/sketch\_04\_a\_noise-1D](https://github.com/b2renger/p5js-designing-interactive-patterns/tree/master/sketch_04_a_noise-1D)

[**home**](https://github.com/djsnipa1/p5js-designing-interactive-patterns#contenu)

## [](https://github.com/djsnipa1/p5js-designing-interactive-patterns#make-some-noise-)Make some Noise!

We will now focus on the concept of [**noise()**](https://p5js.org/reference/%23/p5/noise)

Noise is a relatively complicated concept; it is linked to the notion of _random()_ but is intended to generate results that are less random and closer to each other. In reality noise is very imbued with the notion of "seed", mentioned previously.

It was created in 1983 by [Ken Perlin](https://en.wikipedia.org/wiki/Perlin_noise) whose goal was to create an algorithm capable of reproducing natural-looking textures or surfaces. There are several types of noise, but we will focus on the only version implemented in p5js.

If you have read the reference, you should understand that noise can be used in up to 3 dimensions (we will see this in more detail) and that it returns values between 0 and 1. A more subtle notion than we must understand and that we must "pass" at least one variable (or one dimension) to the _noise()_ function , the greater the gap between the different variables that we pass, the closer the result will be to the _random( function). )_ , the smaller the gap, the smoother the result will be.

[**home**](https://github.com/djsnipa1/p5js-designing-interactive-patterns#contenu)  

### [](https://github.com/djsnipa1/p5js-designing-interactive-patterns#noise-1-dimension)noise 1 dimension

We will start by passing only one value to our noise function, that of a time which unfolds to obtain this kind of result:

[![noise-1D](https://github.com/djsnipa1/p5js-designing-interactive-patterns/raw/master/images/noise-1D.gif)](https://github.com/djsnipa1/p5js-designing-interactive-patterns/blob/master/images/noise-1D.gif)

From the same notion of time we will create an offset in X and Y from the center of the box using the noise function. We will start from our usual code of a grid of boxes.

We must therefore start by declaring a variable which will create a flow of time. This variable will be useful to us in our _draw()_ and we want to increase it little by little, so it must be global and therefore created outside of any other block of code ( _setup()_ or _draw()_ )

```js
let time = 0;
```

Then we will increment this value at each iteration of the _draw() function_

```js
time += 0.005;
```

We are going to use this value for our _noise()_ , so remember that you can change it: if you increase the time more significantly the result will be more jerky, it will be smoother otherwise.

Now inside our double for loop and therefore for each box, we will calculate two noise values:

```
let n1 = noise(time)
let n2 = noise(time + 10)
```

We give here two different values so that the movements are not identical in fact we will use 'n1' to calculate a horizontal offset relative to the center of our box and 'n2' to calculate a vertical offset. If we had ever provided the same value (i.e. 'time' for 'n2' instead of 'time+10') our offset would have been identical in X and Y at each image and we would then only have been able to draw a diagonal.

Before drawing, all we have to do is calculate an offset so that our drawing remains inside our box, as usual for this we will use the _map()_ function , remembering that the result of _noise()_ is always between 0 and 1:

```js
let xoffset = map(n1, 0, 1, -slotSize/2, slotSize/2)
let yoffset = map(n2, 0, 1, -slotSize/2, slotSize/2)  
point(i+xoffset, j+yoffset)
```

We notice here that the drawing in each of our boxes is identical. So we can remedy this by using an extra dimension for our _noise()_ function .

You can find the program [here](https://b2renger.github.io/p5js-designing-interactive-patterns/sketch_04_a_noise-1D/)

As well as the code: [https://github.com/b2renger/p5js-designing-interactive-patterns/tree/master/sketch\_04\_a\_noise-1D](https://github.com/b2renger/p5js-designing-interactive-patterns/tree/master/sketch_04_a_noise-1D)

[**home**](https://github.com/djsnipa1/p5js-designing-interactive-patterns#contenu)  

### [](https://github.com/djsnipa1/p5js-designing-interactive-patterns#noise-2-dimensions)noise 2 dimensions

To obtain a different result in each box we will pass a second argument to our noise.

[![noise-2D](https://github.com/djsnipa1/p5js-designing-interactive-patterns/raw/master/images/noise-2D.gif)](https://github.com/djsnipa1/p5js-designing-interactive-patterns/blob/master/images/noise-2D.gif)

```js
let n1 = noise(time , i) 
let n2 = noise(time + 10 , j) 
let xoffset = map(n1, 0, 1, -slotSize/2, slotSize/2)
let yoffset = map(n2, 0, 1, -slotSize/2, slotSize/2)
point(i+xoffset, j+yoffset)
```

Here we pass 'i' and 'j' directly as arguments for each calculation, the result in each box is therefore different.

But we can achieve different results:

```js
let n1 = noise(time , i) 
let n2 = noise(time + 10 , i) 
```

For example using 'i' twice the result will be the same in each column. Similarly passing 'i' twice will result in the same result on each line. If you pass 'i+j' the result will be the same on each diagonal!

You can find the program [here](https://b2renger.github.io/p5js-designing-interactive-patterns/sketch_04_b_noise-2D/)

As well as the code: [https://github.com/b2renger/p5js-designing-interactive-patterns/tree/master/sketch\_04\_b\_noise-2D](https://github.com/b2renger/p5js-designing-interactive-patterns/tree/master/sketch_04_b_noise-2D)

[**home**](https://github.com/djsnipa1/p5js-designing-interactive-patterns#contenu)  

### [](https://github.com/djsnipa1/p5js-designing-interactive-patterns#noise-3-dimensions)noise 3 dimensions

For this 3rd dimension we are going to change the mode of representation. Instead of calculating an offset in x and y of a point that moves leaving a trail, we will now calculate the size of a rectangle that will be drawn in each box.

[![noise-3D](https://github.com/djsnipa1/p5js-designing-interactive-patterns/raw/master/images/noise-3D.gif)](https://github.com/djsnipa1/p5js-designing-interactive-patterns/blob/master/images/noise-3D.gif)

From a code perspective not much changes. We still need our 'time' variable and our double for loop.

In order to draw our squares by specifying the center rather than the upper left point we will call the [**rectMode()**](https://p5js.org/reference/%23/p5/rectMode) function in the _setup()_

```js
rectMode(CENTER)
```

In the double for loop, we can now calculate a new variable that we will use as the size of our squares, and then draw our squares:

```js
let s = noise(i, j, time) * slotSize*1.25
rect(i, j, s, s)
```

If we do this the result is relatively different from the result of the gif presented above. Looking closer at the gif you will notice that the squares that are close to each other have similar sizes, here that is not the case.

Remembering how _noise()_ works , this would mean that the values which separate successive calls to _noise()_ present too large gaps. This is not the case for time (as seen previously), but between two executions of the code inside the for loops i potentially increased by 'slotSize' and j too.

To obtain a result closer to the gif we will therefore divide i and j by a value large enough for this difference to be reduced:

```js
let s = noise(i/100, j/100, time) * slotSize*1.25
rect(i, j, s, s)
```

Finally, in order to have a different result each time we press the mouse, we will create a variable which will be called 'divisor' and which will change value each time the user presses the mouse.

```js
let slotSize = 10;
let marginX;
let marginY;
let divisor = 100
let time = 0

function setup() {

    createCanvas(windowWidth, windowHeight);
    
    pixelDensity(1);

    marginX = windowWidth - int((windowWidth / slotSize)) * slotSize;
    marginY = windowHeight - int((windowHeight / slotSize)) * slotSize;
    rectMode(CENTER)
    background(0)

}


function draw() {

    background(0)
    //noFill();
    stroke(255)
    strokeWeight(1)
    time += 0.005;
    for (let i = marginX / 2 + slotSize / 2; i < width - marginX / 2; i += slotSize) {
        for (let j = marginY / 2 + slotSize / 2; j < height - marginY / 2; j += slotSize) {
            let s = noise(i/divisor, j/divisor, time) * slotSize*1.25
            rect(i, j, s, s)
        }
    }
}

function mousePressed() {
    //background(0)
    slotSize = random(5, 100)
    divisor = random(10, 1000)
    marginX = windowWidth - int((windowWidth / slotSize)) * slotSize;
    marginY = windowHeight - int((windowHeight / slotSize)) * slotSize;
}

function keyPressed(){
    background(0)
}


function windowResized() {
    resizeCanvas(windowWidth, windowHeight);
    marginX = windowWidth - int((windowWidth / slotSize)) * slotSize;
    marginY = windowHeight - int((windowHeight / slotSize)) * slotSize;
}
}
```

You can find the program [here](https://b2renger.github.io/p5js-designing-interactive-patterns/sketch_04_c_noise-3D/)

As well as the code: [https://github.com/b2renger/p5js-designing-interactive-patterns/tree/master/sketch\_04\_c\_noise-3D](https://github.com/b2renger/p5js-designing-interactive-patterns/tree/master/sketch_04_c_noise-3D)

[**home**](https://github.com/djsnipa1/p5js-designing-interactive-patterns#contenu)  

### [](https://github.com/djsnipa1/p5js-designing-interactive-patterns#noise-et-coordonnees-polaires)Noise and polar coordinates

[![polar noise](https://github.com/djsnipa1/p5js-designing-interactive-patterns/raw/master/images/polar-noise.gif)](https://github.com/djsnipa1/p5js-designing-interactive-patterns/blob/master/images/polar-noise.gif)

Polar coordinates are another way to define the location of a point in two-dimensional space.

Instead of giving a coordinate in X (the abscissa) and one in Y (the ordinate), we will give an angle and a radius. [Polar coordinates](https://fr.wikipedia.org/wiki/Coordonn%25C3%25A9es_polaires) on Wikipedia.

This coordinate system is very practical for describing circles and other spirals. To obtain the patterns shown above, we simply vary the angle and the radius using a noise and then draw a line emanating from the center of our box towards the point that we move in the box below. help with polar coordinates.

Processing or p5js does not give us the ability to draw points using polar coordinates, so we need to convert polar coordinates to Cartesian coordinates before we can draw our lines.

Fortunately there are mathematical formulas to make this conversion. Thus a point expressed in polar coordinates with an angle 'theta' and a radius 'r' will have as Cartesian coordinates in a reference frame this center (x0, y0)

```
x = x0 + cos(theta) * r
```

And

```
y = y0 + sin(theta) * r
```

You can also refer to [this example](https://www.openprocessing.org/sketch/151087) which details the trigonometric circle and basic trigonometric functions.

Once this is established, it is quite simple to achieve the desired result:

First we must for each box (and therefore inside the double for loop) calculate a radius and an angle whose values are animated by a call to the _noise() function_

```js
let angle = noise(time/2 , i , j) 
let r = noise(time , i , j) 
```

_noise()_ returning values between 0 and 1, we will multiply these values so that our angle sweeps the entire circumference of a circle (or even two) and so that our radius can cover the entire width and height of each box

```js
let angle = noise(time/2 , i , j) * TWO_PI * 2
let r = noise(time , i , j) * slotSize *0.5 
```

then we apply our trigonometry formulas:

```js
let xpos = i + cos(angle) * r
let ypos = j + sin(angle) * r
```

then we draw our lines connecting the center of each box to our points calculated in polar coordinates

```js
line(xpos,ypos, i,j)
```

You can find the program [here](https://b2renger.github.io/p5js-designing-interactive-patterns/sketch_04_d_noise-circle-rad-angle/)

As well as the code: [https://github.com/b2renger/p5js-designing-interactive-patterns/tree/master/sketch\_04\_d\_noise-circle-rad-angle](https://github.com/b2renger/p5js-designing-interactive-patterns/tree/master/sketch_04_d_noise-circle-rad-angle)

[**home**](https://github.com/djsnipa1/p5js-designing-interactive-patterns#contenu)  

### [](https://github.com/djsnipa1/p5js-designing-interactive-patterns#noise-et-symetries)Noise and symmetries

Noise may seem a little complicated to master, but by understanding how it works, it is possible to create symmetrical behaviors.

[![symmetrical noise](https://github.com/djsnipa1/p5js-designing-interactive-patterns/raw/master/images/noise-symetric.gif)](https://github.com/djsnipa1/p5js-designing-interactive-patterns/blob/master/images/noise-symetric.gif)

In this example the principle is to draw a line animated by noise in each box without erasing the background from one repetition of _draw()_ to another.

As before we will need to create a 'time' variable at the very top of our program:

```js
let time = 0
```

Then we will increase its value little by little in _draw()_ :

```js
time += 0.005;
```

this writing is equivalent to

```js
time = time + 0.005
```

So in each box we will use a for loop to traverse the width of each of our boxes:

```js
for (let k = - slotSize * 0.5; k < slotSize *0.5 ; k ++){
    
}
```

at each iteration of this _for()_ loop we will therefore draw a point whose abscissa will be 'k' and whose ordinate will be calculated by a noise.

```js
let h = noise(time, k / 100)
point(k+i,h+j)
```

This calculation gives us, for each box, kinds of waves whose starting point (on the left) and arrival point (on the right) do not correspond from one box to another. We will therefore ensure that this is the case by using a sinusoidal function.

[![sinus](https://github.com/djsnipa1/p5js-designing-interactive-patterns/raw/master/images/sinus-wiki.png)](https://github.com/djsnipa1/p5js-designing-interactive-patterns/blob/master/images/sinus-wiki.png)

The advantage of sinusoidal functions is that they are periodic (they repeat over time at regular intervals here between sin(0) and sin(2\*PI)) and that they are symmetrical. Another advantage is that the result of these functions is necessarily between -1 and 1, the difference between two successive values is therefore relatively small and we can therefore use this result directly as a noise parameter, obtaining a relatively smooth result.

We are therefore going to use two variables to animate our noise. The first will therefore be the time and the second will be the result of calculating a sine. We will therefore 'map' our abscissa (i.e. 'k') to obtain a value between 0 and PI and use the sine of this result as a parameter of our noise. Then we will finally calculate the abscissa of our point using the map function once again.

```js
// abscisse dans notre case -> une valeur entre et PI
let inc = map(k, -slotSize*0.5, slotSize*0.5, 0, PI) 
// noise
let n = noise((sin(inc) ), time)
// résultat de noise -> une valeur comprise entre le haut et le bas de notre case
let h = map(n, 0, 1, -slotSize*0.5 , slotSize*0.5)

point(k+i, h+j)
```

To obtain the result presented at the beginning of the paragraph, however, we must draw a continuous line instead of a succession of points.

For this we will use [curveVertex()](https://p5js.org/reference/%23/p5/curveVertex) combined with [beginShape()](https://p5js.org/reference/%23/p5/beginShape) and [endShape()](https://p5js.org/reference/%23/p5/endShape) . These functions allow us to create a curve where all the points are connected to each other. _beginShape()_ allows us to specify that we are going to start drawing a shape; from calling this function we can specify the different points that make up this curve using _curveVertex()_ then we can finish our shape by calling _endShape()_ .

In our case all the points will be added in our for loop which goes through our box horizontally. We will therefore surround our for loop with _beginShape()_ and _endShape()_ and replace calls to _point()_ with calls to _curveVertex()_ .

```js
beginShape()
for (let k = - slotSize * 0.5; k < slotSize *0.5 ; k ++){
    let inc = map(k, -slotSize*0.5, slotSize*0.5, 0, PI)
    let n = noise((sin(inc) ), time) 
    let h = map(n, 0, 1, -slotSize*0.5 , slotSize*0.5)
    curveVertex(k + i, j + h)
}
endShape()
```

You can find the program [here](https://b2renger.github.io/p5js-designing-interactive-patterns/sketch_04_e_noise-symetric/)

As well as the code: [https://github.com/b2renger/p5js-designing-interactive-patterns/tree/master/sketch\_04\_e\_noise-symmetric](https://github.com/b2renger/p5js-designing-interactive-patterns/tree/master/sketch_04_e_noise-symetric)

[**home**](https://github.com/djsnipa1/p5js-designing-interactive-patterns#contenu)  

### [](https://github.com/djsnipa1/p5js-designing-interactive-patterns#noise-symetrique-et-coordonnees-polaires)Symmetric noise and polar coordinates

In this paragraph we will combine our knowledge of polar coordinates and noise to achieve this result:

[![noisy symmetric circle](https://github.com/djsnipa1/p5js-designing-interactive-patterns/raw/master/images/radial-noise.gif)](https://github.com/djsnipa1/p5js-designing-interactive-patterns/blob/master/images/radial-noise.gif)

We will start by creating a for loop to traverse the entire periphery of a circle, that is to say a loop starting at 0 and ending at 2 times pi:

```js
for (let angle = 0 ; angle <= TWO_PI *2; angle = angle + PI * 0.05){
    
}
```

in this loop we will calculate a radius value in order to be able to use the polar coordinate system to determine the position of the points. This value will depend on a noise: in each box we want a different shape, but we want a symmetrical shape. We will therefore use a parameter which will be unique for each box and which will evolve as a function of time and two parameters which will loop and therefore using sinusoidal functions.

The first parameter will therefore depend on the time 'time' and we will add 'i' and 'j' so that in each box the value of this first parameter is different:

```js
noise(time + i +j*10)
```

The next two parameters will use 'cos()' and 'sin()', then to be able to define a radius that can potentially take up the entire box we will multiply the result of _noise()_ which is between 0 and 1 by 'slotSize/ 2'

```js
let r = noise(time + i + j *10, cos(angle) , sin(angle) )* slotSize *0.5
```

Using the formula for converting polar coordinates into Cartesian coordinates, we will therefore be able to define the positions of each point which will compose our shape:

```js
let xpos = i + cos(angle) *r
let ypos = j + sin(angle) *r
```

All we have to do now is draw our shape using _curveVertex()_ :

```js
beginShape()
for (let angle = 0 ; angle <= TWO_PI *2; angle = angle + PI * 0.05){
    let r = noise(time + i + j *10, cos(angle) , sin(angle) )* slotSize *0.5
    let xpos = i + cos(angle) *r
    let ypos = j + sin(angle) *r
    curveVertex(xpos,ypos)    
}
endShape()
```

Compared to the gif, we still have to manage the color. We want a different color in each box, so we will define a list of colors from which we can draw randomly. For this we will use the colors in hexadecimal form which we will store in a table. In js to do this, simply define a new variable and store inside an array defined by an opening bracket **\[** and a closing bracket **\]** . Each color code will be framed by apostrophes and separated by commas

```js
let colors = ['#72d6c9','#ffc785', '#df7599', '#7189bf']
```

To access a color from this list we must still use brackets and put the index of the position of the color we wish to use. For example

```js
colors[0] // sera '#72d6c9'
colors[3] // sera '#7189bf'
```

Now we can in each box (and therefore inside the double for loop) and before the loop allowing us to draw our shape we will create a variable named 'c' which will be drawn randomly from our list of colors.

For the moment we have 4 colors in our list, so we need to draw an index which must be an integer:

```js
int(random(4))
```

To obtain our color we will therefore store it in our variable 'c' we will therefore use the result of this calculation and place it in square brackets:

```js
let c = colors[int(random(4))]
```

We can also automatically retrieve the size of a list (ie the number of elements in it) using 'colors.length', ideally it is a good idea to use this technique, as it will allow us to be able to add or remove colors from our table without having to modify the code:

```js
let c = colors[int(random(colors.length))]
stroke(c)
```

We will also want to use some transparency, unfortunately when we use a color in hexadecimal form, it is not possible to add a second parameter to manage transparency.

We must therefore use the classic syntax for _stroke()_ with 4 parameters, the [red()](https://p5js.org/reference/%23/p5/red) , [green()](https://p5js.org/reference/%23/p5/green) and [blue()](https://p5js.org/reference/%23/p5/blue) functions will allow us to extract the red, green and blue color components:

```js
stroke(red(c), green(c), blue(c), 25)
```

To get each color we use _random()_ in the _draw()_ , so that our colors do not change with each repetition we will therefore re-use _randomSeed()_ . We therefore need to define a 'seed' with a global variable (at the very top of our program)

```js
let seed
```

In the _setup()_ we must initialize it:

```js
seed = random(9999)
```

In the _draw()_ we can therefore use it in conjunction with _randomSeed()_

```js
randomSeed(seed)
```

and to keep our generative side we will change this value each time the user presses the mouse. So we will add the following line in _mousePressed()_ :

```js
seed = random(9999)
```

And here is the final code for our example:

```js
let slotSize = 100;
let marginX;
let marginY;
let time = 0
let seed = 123

let colors = ['#72d6c9','#ffc785', '#df7599', '#7189bf']

function setup() {

    createCanvas(windowWidth, windowHeight);
    
    pixelDensity(1);

    marginX = windowWidth - int((windowWidth / slotSize)) * slotSize;
    marginY = windowHeight - int((windowHeight / slotSize)) * slotSize;
    rectMode(CENTER)
    background(0)
}


function draw() {
    randomSeed(seed)
    noFill();
    stroke(255,25)
    strokeWeight(0.15)
    time += 0.005;
    for (let i = marginX / 2 + slotSize / 2; i < width - marginX / 2; i += slotSize) {
        for (let j = marginY / 2 + slotSize / 2; j < height - marginY / 2; j += slotSize) {
            let c = colors[int(random(colors.length))]
            stroke(red(c), green(c), blue(c), 25)
            beginShape()
            for (let angle = 0 ; angle <= TWO_PI *2; angle = angle + PI * 0.05){
                let r = noise(time + i + j *10, cos(angle) , sin(angle) )* slotSize *0.5
                let xpos = i + cos(angle) *r
                let ypos = j + sin(angle) *r
                curveVertex(xpos,ypos)
                
            }
            endShape()
        }
    }
}

function mousePressed() {
    background(0)
    seed = random(9999)
    slotSize = random(50, 400)
    marginX = windowWidth - int((windowWidth / slotSize)) * slotSize;
    marginY = windowHeight - int((windowHeight / slotSize)) * slotSize;
}

function keyPressed(){
    background(0)
}


function windowResized() {
    resizeCanvas(windowWidth, windowHeight);
    marginX = windowWidth - int((windowWidth / slotSize)) * slotSize;
    marginY = windowHeight - int((windowHeight / slotSize)) * slotSize;
}
```

You can find the program [here](https://b2renger.github.io/p5js-designing-interactive-patterns/sketch_04_f_noise-circle-symetric/)

As well as the code: [https://github.com/b2renger/p5js-designing-interactive-patterns/tree/master/sketch\_04\_f\_noise-circle-symetric](https://github.com/b2renger/p5js-designing-interactive-patterns/tree/master/sketch_04_f_noise-circle-symetric)

[**home**](https://github.com/djsnipa1/p5js-designing-interactive-patterns#contenu)  

### [](https://github.com/djsnipa1/p5js-designing-interactive-patterns#noise-asymetrique-et-coordonnees-polaires)Asymmetric noise and polar coordinates

Let's modify our code a little in order to have an asymmetric result:

[![asymmetric noise](https://github.com/djsnipa1/p5js-designing-interactive-patterns/raw/master/images/noise-asymetric.gif)](https://github.com/djsnipa1/p5js-designing-interactive-patterns/blob/master/images/noise-asymetric.gif)

_The modifications to be made are minimal, here we will just change the parameters of our noise()_ a little

```js
let r = noise(time + i + j, cos(angle) + 1, sin(angle) + 1) * slotSize * 0.5
```

We will also take advantage of this to switch to HSB color mode in _setup()_

```
colorMode(HSB, 360, 100, 100)
```

and we are going to make the color of our line depend on the value of the radius:

```js
let h = map(r, 0, slotSize * 0.5, 160, 220)
stroke(h, 50, 100, 1)
```

You can find the program [here](https://b2renger.github.io/p5js-designing-interactive-patterns/sketch_04_g_noise-circle-asymetric/)

As well as the code: [https://github.com/b2renger/p5js-designing-interactive-patterns/tree/master/sketch\_04\_g\_noise-circle-asymetric](https://github.com/b2renger/p5js-designing-interactive-patterns/tree/master/sketch_04_g_noise-circle-asymetric)

[**home**](https://github.com/djsnipa1/p5js-designing-interactive-patterns#contenu)  

### [](https://github.com/djsnipa1/p5js-designing-interactive-patterns#interlude-unknown-pleasures)Interlude unknown pleasures

Let's deviate a little from our usual concerns (grids and tilings) to continue a little on the notion of noise and recreate a visual close to the cover of the album "unknown pleasures" by Joydivision.

[![joydivision](https://github.com/djsnipa1/p5js-designing-interactive-patterns/raw/master/images/joydivision.jpg)](https://github.com/djsnipa1/p5js-designing-interactive-patterns/blob/master/images/joydivision.jpg) [![joy](https://github.com/djsnipa1/p5js-designing-interactive-patterns/raw/master/images/noise-joydivision.gif)](https://github.com/djsnipa1/p5js-designing-interactive-patterns/blob/master/images/noise-joydivision.gif)

Here we will use fixed margins, we will use a time-dependent _noise() function and we will allow the user to change the density of lines displayed horizontally with a mouse click:_

```js
let ySpacing = 25;
let marginX = 400;
let marginY = 200;
let time = 0
```

Our _setup()_ is quite classic:

```js
function setup() {
    createCanvas(windowWidth, windowHeight);
    pixelDensity(1);
    background(0)
}
```

_and we use the classic mousePressed()_ and _windowResized()_ functions :

```js
function mousePressed() {
    background(0)
    ySpacing = random(5, 20)
}

function windowResized() {
    resizeCanvas(windowWidth, windowHeight);
}
```

Our _draw()_ will include our classic drawing attributes and the increment of our 'time' variable:

```js
function draw() {

    background(0)
    fill(0);
    stroke(255)
    strokeWeight(2)
    time += 0.005;

}
```

To obtain our visual, we will recreate logic similar to an example seen previously: we must traverse the entire width of our window (minus the margins) with a for loop and create "mountains" of _noise()_ :

```js
beginShape()
for (let i = marginX / 2; i < width - marginX / 2; i += 1) {
     let n = noise(time, i/10)
    let offset = map(n, 0, 1, 0, - 100)
    curveVertex(i,j + offset)
}
endShape()
```

The trick here is to manage to squash our “waves” to the left and right of the image. We will have to multiply our 'offset' by a value which will be very close to 0 on the right and left of the image and close to 1 in the center.

To do this we will have to, as before when we wanted to obtain a symmetrical shape, map the abscissa to a value that we will be able to use in a sinusoidal function.

```js
let t = map(i, marginX/2, width-marginX/2,PI, PI*2)
```

To accentuate the curve of our sine function, we are going to multiply it several times by itself using the [pow()](https://p5js.org/reference/%23/p5/pow) function . By doing this we will have to drastically increase the output value of 'offset' to compensate for this overwriting:

```js
let offset = map(n, 0, 1, 0, - 1000000)
offset = offset *pow(sin(t)/PI, 8)
```

Each line will therefore be composed of this code:

```js
beginShape()
for (let i = marginX / 2; i < width - marginX / 2; i += 1) { 
    let n = noise(time, i/10   ,j)
    let t = map(i, marginX/2, width-marginX/2,PI, PI*2)
    let offset = map(n, 0, 1, 0, - 1000000)*pow(sin(t)/PI, 8)
    curveVertex(i,j + offset)
}
endShape()
```

Now just repeat this vertically:

```js
 for (let j = marginY / 2 + slotSize / 2; j < height - marginY / 2; j += ySpacing) {
    stroke(255)
    beginShape()
    for (let i = marginX / 2; i < width - marginX / 2; i += 1) {
       
        let n = noise(time, i/10   ,j)
        let t = map(i, marginX/2, width-marginX/2,PI, PI*2)
        let offset = map(n, 0, 1, 0, - 1000000)*pow(sin(t)/PI, 8)
        curveVertex(i,j + offset)
    }
    endShape()
}
```

You can test the program [here](https://b2renger.github.io/p5js-designing-interactive-patterns/sketch_04_h_joydivision/)

and consult the associated code: [https://github.com/b2renger/p5js-designing-interactive-patterns/tree/master/sketch\_04\_h\_joydivision](https://github.com/b2renger/p5js-designing-interactive-patterns/tree/master/sketch_04_h_joydivision)

[**home**](https://github.com/djsnipa1/p5js-designing-interactive-patterns#contenu)  

## [](https://github.com/djsnipa1/p5js-designing-interactive-patterns#rotate-translate)Rotate-translate

We will now focus on transformations of space, that is to say the use of functions which will allow us to manipulate our coordinate system to offer us more flexibility in the way in which we can position and manipulate shapes.

### [](https://github.com/djsnipa1/p5js-designing-interactive-patterns#un-exemple-basique)A basic example

We will try to recreate this example:

[![rotate basic translate](https://github.com/djsnipa1/p5js-designing-interactive-patterns/raw/master/images/rotate_translate.gif)](https://github.com/djsnipa1/p5js-designing-interactive-patterns/blob/master/images/rotate_translate.gif)

This animation is made up of two elements, two squares per box. The first rotates around its center which coincides with the center of each box according to the position of the mouse on the abscissa and changes size according to the position of the mouse on the ordinate. The second, twice as small, will rotate around the center of the box with an offset which will depend on its position in the grid.

Let's start by drawing the first square. In order to rotate a square around its center, we will use the [**rectMode()**](https://p5js.org/reference/%23/p5/rectMode) function that we have already seen, and two new functions: [**rotate()**](https://p5js.org/reference/%23/p5/rotate) and [**translate()**](https://p5js.org/reference/%23/p5/translate) .

You will have understood that **rotate()** allows you to perform rotations and **translate()** allows you to perform translations; but these rotations and rotations apply to our marker and not to the shapes that we are going to draw directly.

We can see this as having a pen above the sheet and that to draw instead of moving the pen we would move the sheet. To better understand, I invite you to watch this program:

[https://www.openprocessing.org/sketch/388513](https://www.openprocessing.org/sketch/388513)

The different squares are drawn with the same instruction each time:

```js
rect(50, 100, 25,25)
```

The black square is in the original coordinate system.

The red square is drawn after transforming this system using the function:

```js
translate(mouseX,mouseY)
```

The blue square is drawn after successively calling:

```js
translate(mouseX,mouseY)
```

And

```js
rotate(PI/5)
```

Our main problem with the **translate()** and **rotate()** functions and that they impact all the shapes we will draw after calling them. We therefore need a way to limit their field of action: this is what the [**push()**](https://p5js.org/reference/%23/p5/push) and [**pop() functions are for.**](https://p5js.org/reference/%23/p5/pop)

All calls made to _rotate()_ and _translate()_ that are located between _push()_ and _pop()_ only have an action between these two keywords.

As part of the objective that we set for ourselves, it was perfect to be able to apply transformations in each box of our grid without the others being impacted.

Inside our usually used double for loop, we will enclose all our code between a _push()_ and a _pop()_ .

```js
 for (let i = marginX / 2 + slotSize / 2; i < width - marginX / 2; i += slotSize) {
    for (let j = marginY / 2 + slotSize / 2; j < height - marginY / 2; j += slotSize) {
            push()
            
            pop()
    }
}
```

To rotate a rectangle around its center, we need to set its drawing mode using _rectMode()_ , then we will first place our mark in the center of the box and then apply a rotation to it. (If we had first applied a rotation before applying our translation our shape would have rotated around the upper left corner of our box).

To calculate the size and rotation values of our square we will use the _map()_ function to transform the mouse values into useful values to animate our rotation and our size modification.

```js
let angle = map(mouseX, 0, width, 0, TWO_PI)
let s = map(mouseY, 0, height, 25, slotSize*2)
```

Then we will apply the space transformations described just before

```js
translate(i,j) // déplacer notre repère au centre de la case
rotate(angle) // le faire tourner de la valeur 'angle'
rect(0, 0, s, s);
```

Which leaves us with this code for the first part of our animation:

```js
for (let i = marginX / 2 + slotSize / 2; i < width - marginX / 2; i += slotSize) {
        for (let j = marginY / 2 + slotSize / 2; j < height - marginY / 2; j += slotSize) {
            push()
                                                                                           
            let angle = map(mouseX, 0, width, 0, TWO_PI)
            let s = map(mouseY, 0, height, 25, slotSize*2)

            translate(i,j)
            rotate(angle)
            rect(0, 0, s, s);
            
            pop()
        }
}
```

For the second part of the animation we will create a second double loop. But this time instead of drawing our rectangle in the middle of our reference frame (ie at coordinates (0,0)) as before we are going to offset it. This offset will be proportional to its position in the grid (i.e. the box number) and we will therefore use the _map() function once again_

```js
let xOffset = map (i, marginX/2, width-marginX/2, -slotSize*0.5 , slotSize *0.5)
let yOffset = map (j, marginY/2, height-marginY/2, -slotSize*0.5 , slotSize *0.5)
```

If our square is at the very left of the grid, it will also be by default at the very left of its box and if it is at the very top it will also be at the very top of its box.

```js
for (let i = marginX / 2 + slotSize / 2; i < width - marginX / 2; i += slotSize) {
        for (let j = marginY / 2 + slotSize / 2; j < height - marginY / 2; j += slotSize) {
            push()
            translate(i,j)
            let angle = map(mouseX, 0, width, 0, TWO_PI)
            rotate(angle)
            let xOffset = map (i, marginX/2, width-marginX/2, -slotSize*0.5 , slotSize *0.5)
            let yOffset = map (j, marginY/2, height-marginY/2, -slotSize*0.5 , slotSize *0.5)
            translate(xOffset,yOffset)
            rect(xOffset, yOffset, slotSize*0.5, slotSize*0.5);
            pop()
        }
}
```

_rotate()_ and _translate()_ can be infinitely combined with _push()_ and _pop()_ to obtain all kinds of effects which can be interesting for creating brushes: [https://b2renger.github .io/Introduction\_p5js/01\_dessiner\_04/index.html](https://b2renger.github.io/Introduction_p5js/01_dessiner_04/index.html)

You can test the program [here](https://b2renger.github.io/p5js-designing-interactive-patterns/sketch_05_a_rotate/)

and view the associated code: [https://github.com/b2renger/p5js-designing-interactive-patterns/tree/master/sketch\_05\_a\_rotate](https://github.com/b2renger/p5js-designing-interactive-patterns/tree/master/sketch_05_a_rotate)

[**home**](https://github.com/djsnipa1/p5js-designing-interactive-patterns#contenu)  

### [](https://github.com/djsnipa1/p5js-designing-interactive-patterns#utilisation-de-fonts)Using fonts

We will continue in this same logic, but this time we will try to construct patterns with typography:

[![relexion typo](https://github.com/djsnipa1/p5js-designing-interactive-patterns/raw/master/images/typo_reflexion.gif)](https://github.com/djsnipa1/p5js-designing-interactive-patterns/blob/master/images/typo_reflexion.gif)

This animation is made up of two letters, which move in a box. The position of the mouse on the ordinate determines the rotation of our letters, the position of the mouse on the abscissa determines the translation of our letters along the abscissa precisely, but while remaining inside the box. These transformations apply to our first letter as is and are reflected along a horizontal axis of symmetry to draw our second letter.

Let's start with our first letter. Nothing really new here except the [**text()**](https://p5js.org/reference/%23/p5/text) , [**textSize() functions**](https://p5js.org/reference/%23/p5/textSize) and [**textAlign()**](https://p5js.org/reference/%23/p5/textAlign) functions , which are quite transparent.

As before we are going to enclose all the code that we are going to type in our double for loop between a call to _push()_ and a call to _pop()_ .

We must then specify our parameters to draw our text: its size ( _textSize()_ ) and its indentation ( _textAlign()_ )

Then we can move our marker to the center of our box (with _translate()_ ). Then we will calculate the abscissa offset (\*map()) and a rotation ( _map()_ ) which we will apply to our text:

```js
for (var x = -slotSize ; x < width + slotSize; x += slotSize) {
        for (var y = -slotSize ; y < height + slotSize; y += slotSize) {
            push()
                                                                        
            textSize(slotSize) // définir la taille du texte
            textAlign(CENTER, CENTER) // centrer le texte verticalement et horizontalement
    
            translate(x,y)
            
            let xOffset = map(mouseX, 0, windowWidth, -slotSize/2, slotSize/2)
            let angle = map(mouseY, 0, height, 0, TWO_PI)
            translate(xOffset, 0)
            rotate(angle)
            text("%", 0, 0) // dessiner le caractère '%'
  
            pop()                                                                
       }
}
```

This code therefore allows us to draw our first character in each box. We will now draw its symmetrical.

To do this we will have to carry out new transformations of the space and therefore ensure that our first transformations are well limited to our first character. We will therefore surround all the code that concerns it with a _push()_ and a _pop()_

```js
for (var x = -slotSize ; x < width + slotSize; x += slotSize) {
        for (var y = -slotSize ; y < height + slotSize; y += slotSize) {
            push()
                                                                        
            textSize(slotSize) // définir la taille du texte
            textAlign(CENTER, CENTER) // centrer le texte verticalement et horizontalement
    
            translate(x,y)
                                                                        
            let xOffset = map(mouseX, 0, windowWidth, -slotSize/2, slotSize/2)
            let angle = map(mouseY, 0, height, 0, TWO_PI)
                                                                        
            push()
            translate(xOffset, 0)
            rotate(angle)
            text("%", 0, 0) // dessiner le caractère '%'
            pop()
  
            pop()                                                                
       }
}
```

In order to carry out our reflection we will use the [**scale()**](https://p5js.org/reference/%23/p5/scale) function which allows us to carry out a scale transformation independently on the abscissa axis or on the ordoonate axis. For example

```js
scale(1,1) // correspond au mode par défaut
scale(2, 0.5) // toutes les grandeurs de l'axe des abscisses seront multipliées par deux et
              // toutes les grandeurs de l'axes des ordonnées seront divisées par deux.
```

So to perform vertical axis symmetry, simply use:

```js
scale(-1,1)
```

We therefore only have to reproduce the same operations as before but having changed the way in which the program will interpret them using scale.

```js
push()
scale(-1,1)
translate(xOffset, 0)
rotate(angle)
text("%", 0, 0) // dessiner le caractère '%'
pop()
```

We therefore obtain our two forms reflected in this way:

```js
for (var x = -slotSize ; x < width + slotSize; x += slotSize) {
        for (var y = -slotSize ; y < height + slotSize; y += slotSize) {
            push()
                                                                        
            textSize(slotSize) // définir la taille du texte
            textAlign(CENTER, CENTER) // centrer le texte verticalement et horizontalement
    
            translate(x,y)
                                                                        
            let xOffset = map(mouseX, 0, windowWidth, -slotSize/2, slotSize/2)
            let angle = map(mouseY, 0, height, 0, TWO_PI)
                                                                        
            push()
            translate(xOffset, 0)
            rotate(angle)
            text("%", 0, 0) // dessiner le caractère '%'
            pop()
                                                                        
            push()
            scale(-1,1)
            translate(xOffset, 0)
            rotate(angle)
            text("%", 0, 0) // dessiner le caractère '%'
            pop()
  
            pop()                                                                
       }
}
```

_push()_ and _pop()_ apply to all space transformations, they also apply to _scale()_ : you must therefore remember to put _scale(-1,1)_ after _push()_ and before _pop ()_

We now have to be able to dynamically change the character we draw as well as the font and the color (even if for the color this has already been done previously)

In order to be able to change the character used for drawing each time the user presses a key on the keyboard. We must declare a global variable (and therefore at the very top of our program).

```js
let c = '%'
```

We will now be able to use this variable to draw our text by replacing '%' with 'c' in the call to the _text() function._

```js
text(c, 0, 0)
```

All we have to do is modify this value when the user presses a key on the keyboard using the [**keyTyped() function**](https://p5js.org/reference/%23/p5/keyTyped)

```js
function keyTyped() {
    c = key
}
```

Now let's focus on being able to change the font used. For this we will use fonts already available online via [Google Fonts](https://fonts.google.com/) .

This site allows us to choose from a multitude of fonts and even provides us with code to insert these fonts into our web pages.

[![googlefonts](https://github.com/djsnipa1/p5js-designing-interactive-patterns/raw/master/images/googlefonts.png)](https://github.com/djsnipa1/p5js-designing-interactive-patterns/blob/master/images/googlefonts.png)

Simply click on the '+' at the top right of each box to add a font to our font list. Once our choice is made we can click on the black bar at the bottom of our window to consult the code to insert our fonts.

[![googlefonts selection](https://github.com/djsnipa1/p5js-designing-interactive-patterns/raw/master/images/googlefonts-selection.png)](https://github.com/djsnipa1/p5js-designing-interactive-patterns/blob/master/images/googlefonts-selection.png)

You notice a string of html code that we are going to use. When we code with an html file like a traditional developer, we simply add the code provided to the "index.html" file that we use.

Here, given that we are working with openprocessing, we do not have access to our html file, so we will modify it at runtime with a little javascript code.

First we need to create a new element of type "link":

```js
let link = document.createElement('link'); // on crée un nouvel 'élément link'
```

and we will populate the fields necessary for this tag with the data provided by google-fonts.

```js
let fontList  = "https://fonts.googleapis.com/css?family=Monoton|East+Sea+Dokdo|Fascinate+Inline|Righteous"; // on ajoute en source la lib (lien cdn)
link.href = fontList
link.rel="stylesheet"
```

We then have to attach the link object that we created to our web page:

```js
document.body.appendChild(link);
```

To use our fonts, we will create a table filled with the names of the fonts that interest us and then be able to draw lots which font we use.

```js
let fonts = ["Monoton", "East Sea  Dokdo", "Fascinate Inline ", "Righteous"]
```

From _setup()_ we can draw a first font to use to draw our text.

```js
let f = fonts[int(random(fonts.length))]
```

All we then have to do is apply this font using the [**textFont() function.**](https://p5js.org/reference/%23/p5/textFont)

```js
textFont(f)
```

We can repeat this action every time our user clicks on their mouse by copying these two lines of code into the already well-known _mousePressed()_ function .

By re-applying the techniques we already know to change colors randomly using a color palette we end up with this code:

```js
let link = document.createElement('link'); // on crée un nouvel 'élément link'
let fontList  = "https://fonts.googleapis.com/css?family=Monoton|East+Sea+Dokdo|Fascinate+Inline|Righteous"; // on ajoute en source la lib (lien cdn)
link.href = fontList
link.rel="stylesheet"
document.body.appendChild(link);


let slotSize = 100;
let marginX
let marginY
let step = 1
let c = '%'
let colorsfront = ["#ffd3d3", "#fcffa5", "#fc7afa", "#8fbdf6"]
let colorsback = ["#1a3a51", "#5c134a", "#3c415e", "#00677e"]

let c1
let c2

let fonts = ["Monoton", "East Sea  Dokdo", "Fascinate Inline ", "Righteous"]


function setup() {

createCanvas(windowWidth, windowHeight);

pixelDensity(1)
textSize(slotSize)
textAlign(CENTER, CENTER)

c1 = "#3c415e"
c2 = "#ffd3d3"

marginX = windowWidth - int((windowWidth / slotSize)) * slotSize;
marginY = windowHeight - int((windowHeight / slotSize)) * slotSize;

textFont('Righteous')

}


function draw() {

background(c1)


for (var x = -slotSize / 2; x < width + slotSize; x += slotSize) {
for (var y = -slotSize / 2; y < height + slotSize; y += slotSize) {
push()
textSize(slotSize)
textAlign(CENTER, CENTER)
fill(c2)
translate(x, y)

push()
scale(1, 1)
translate(map(mouseX, 0, windowWidth, -slotSize / 2, slotSize / 2), 0)
rotate(map(mouseY, 0, height, 0, TWO_PI))
text(c, 0, 0)
pop()

push()
scale(-1, 1)
translate(map(mouseX, 0, windowWidth, -slotSize / 2, slotSize / 2), 0)
rotate(map(mouseY, 0, height, 0, TWO_PI))
text(c, 0, 0)
pop()

pop()
}

}

}

function keyTyped() {
c = key
}

function mouseReleased() {
slotSize = int(random(5, 25)) * 10
step = int(random(1, 6))
c1 = colorsback[int(random(colorsback.length))]
c2 = colorsfront[int(random(colorsfront.length))]
let f = fonts[int(random(fonts.length))]
textFont(f)

marginX = windowWidth - int((windowWidth / slotSize)) * slotSize;
marginY = windowHeight - int((windowHeight / slotSize)) * slotSize;

console.log(slotSize, step, c1, c2, f)

}

function windowResized() {
resizeCanvas(windowWidth, windowHeight);
marginX = windowWidth - int((windowWidth / slotSize)) * slotSize;
marginY = windowHeight - int((windowHeight / slotSize)) * slotSize;
}
```

You can test the program [here](https://b2renger.github.io/p5js-designing-interactive-patterns/sketch_05_c_rotate_typo_polar/)

and consult the associated code: [https://github.com/b2renger/p5js-designing-interactive-patterns/tree/master/sketch\_05\_b\_rotate\_typo\_reflection](https://github.com/b2renger/p5js-designing-interactive-patterns/tree/master/sketch_05_b_rotate_typo_reflection)

I made a second variation using polar coordinates that you can test [here](https://b2renger.github.io/p5js-designing-interactive-patterns/sketch_05_c_rotate_typo_polar/)

and you can also consult the code associated with it: [https://b2renger.github.io/p5js-designing-interactive-patterns/sketch\_06\_b\_layers\_supperpositions/index.html](https://b2renger.github.io/p5js-designing-interactive-patterns/sketch_06_b_layers_supperpositions/index.html)

[**home**](https://github.com/djsnipa1/p5js-designing-interactive-patterns#contenu)  

## [](https://github.com/djsnipa1/p5js-designing-interactive-patterns#dessiner-dans-des-calques)Drawing in layers

For several reasons it may be interesting to use layers. p5js allows this using what we call "offscreen graphics": it is possible to draw in an image which is not displayed and which we can display later with the [**image() function**](https://p5js.org/reference/%23/p5/image) function .

It is possible to create such an object with the [**createGraphics() function**](https://p5js.org/reference/%23/p5/createGraphics)

We will learn how to use it to recreate this type of effect:

[![pg circles](https://github.com/djsnipa1/p5js-designing-interactive-patterns/raw/master/images/pg_circles.gif)](https://github.com/djsnipa1/p5js-designing-interactive-patterns/blob/master/images/pg_circles.gif)

To do this we will create a global variable to store our image

```js
let pg
```

Then in _setup()_ we will be able to draw an ellipse in this layer positioned at the top center of the window. Since this ellipse is drawn by specifying the coordinates of its center, it will then be cut.

Let's already initialize our layer so that it is the size of a box:

```js
pg = createGraphics(slotSize, slotSize)
pg.pixelDensity(1)
```

We can now draw inside as usual, just preceding all drawing instructions with 'pg.'. All the notions seen previously apply in the same way in a layer.

```js
pg.fill(0, 0, 0, 150)
pg.noStroke()
pg.ellipse(0, slotSize / 2, slotSize * 0.65, slotSize * 0.65)
```

This type of technique will allow us to create images that can be displayed in each box and rotated if necessary.

In our animation using circles, the principle is to draw an ellipse at the top in the middle of our box, due to the size of the layer our ellipse will be cut off. We will keep a transparent background and we will rotate our layer to draw 4 half ellipses in each box. Using a combination of _translate()_ and _rotate()_ we can achieve the desired effect.

To display our layers we will use the [**image() function**](https://p5js.org/reference/%23/p5/image) function . This function allows you to display an image on the screen. It can take up to five parameters: the first is the name of the image to display, the next two are the coordinates of the upper left point of the image and optionally we can specify the width and height of the image that you wish to display (at the risk of distorting the original image).

From the beginning we have used the center of our boxes as the drawing point, so we will use the [**imageMode()**](https://p5js.org/reference/%23/p5/imageMode) function , in order to be able to specify the center of our images as the anchor (drawing) point, rather than the upper left corner . We will carry out this manipulation in _setup()_

```js
imageMode(CENTER)
```

Then in _draw()_ we will draw our first layer in the classic way inside our double for loop

```js
 for (var x = -slotSize * 5; x < width + slotSize * 5; x += slotSize * 1) {
        for (var y = -slotSize * 5; y < height + slotSize * 5; y += slotSize * 1) {
            push()
            image(pg, x, y)
            pop()
        }
}                                                                                
```

We will now superimpose a second image but this time if it will have rotated around its center a quarter turn. Given that we are going to rotate around the center of our image we must first place ourselves in the center of our box using _translate()_ then use _rotate()_

```js
 for (var x = -slotSize * 5; x < width + slotSize * 5; x += slotSize * 1) {
        for (var y = -slotSize * 5; y < height + slotSize * 5; y += slotSize * 1) {
            push()
            image(pg, x, y)
            pop()
                            
            push()         
            translate(x, y)
            rotate(PI/2)
            image(pg,0,0)
            pop()
                                            
        }
}                                                                                
```

We will repeat this operation two more times:

```js
for (var x = -slotSize * 5; x < width + slotSize * 5; x += slotSize * 1) {
        for (var y = -slotSize * 5; y < height + slotSize * 5; y += slotSize * 1) {
            push()
            image(pg, x, y)
            pop()

            push()
            translate(x, y)
            rotate(PI)
            image(pg, 0,0)
            pop()

            push()
            translate(x, y)
            rotate(PI / 2)
            image(pg, 0,0)
            pop()

            push()
            translate(x, y)
            rotate(-PI / 2)
            image(pg, 0,0)
            pop()
        }

}
```

Now all we have to do is create our mouse position-dependent offset effect. As usual, it involves calculating two shift coefficients: one on the abscissa, and one on the ordinate. This operation must be done at the very top of the _draw()_

```js
let offsetX = map(mouseY, 0, width, -1, 1)
let offsetY = map(mouseX, 0, height, -1, 1)
```

We will therefore use them to position our images in each box, using the second and third parameters of our _image()_ function : by multiplying 'xOffset' or 'yOffset' by 'slotSize', we will obtain an image which will slide by one box to the left/up if our mouse is to the left/top of our window or one box to the right/down if our mouse is to the right/bottom of our window.

```js
offsetX = map(mouseY, 0, width, -1, 1)
offsetY = map(mouseX, 0, height, -1, 1)

for (var x = -slotSize * 5; x < width + slotSize * 5; x += slotSize * 1) {
        for (var y = -slotSize * 5; y < height + slotSize * 5; y += slotSize * 1) {
            push()
            translate(x,y)
            image(pg, slotSize * offsetX, slotSize * offsetY)
            pop()

            push()
            translate(x, y)
            rotate(PI)
            image(pg, slotSize * offsetX, slotSize * offsetY)
            pop()

            push()
            translate(x, y)
            rotate(PI / 2)
            image(pg, slotSize * offsetX, slotSize * offsetY)
            pop()

            push()
            translate(x, y)
            rotate(-PI / 2)
            image(pg, slotSize * offsetX, slotSize * offsetY)
            pop()
        }
}
```

Note, however, that when we click the mouse to resize the boxes in our grid, the layers do not automatically adjust. We could use the fourth and fifth parameters of _image()_ parameters , but this would risk producing pixelated images (especially if our layer is smaller than our boxes and the layers will therefore have to be enlarged).

We will therefore redraw the contents of our layers each time the user presses the mouse:

```js
function mouseReleased() {

    slotSize = int(random(2, 6)) * 25
    ellipseSize = random(0.125, 1)

    opacity = random(50, 200)

    console.log(slotSize, ellipseSize, opacity)

    pg = createGraphics(slotSize, slotSize)
    pg.fill(0, 0, 0, opacity)
    pg.noStroke()
    pg.ellipse(0, slotSize / 2, slotSize * ellipseSize, slotSize * ellipseSize)
    
    marginX = windowWidth - int((windowWidth / slotSize)) * slotSize;
    marginY = windowHeight - int((windowHeight / slotSize)) * slotSize;
}
```

You can find the interactive program demo [here](https://b2renger.github.io/p5js-designing-interactive-patterns/sketch_06_a_layers_half-cirdles/)

as well as the code: [https://github.com/b2renger/p5js-designing-interactive-patterns/tree/master/sketch\_06\_a\_layers\_half-cirdles](https://github.com/b2renger/p5js-designing-interactive-patterns/tree/master/sketch_06_a_layers_half-cirdles)

You can also consult a second variation around this idea of superimposing grids [here](https://b2renger.github.io/p5js-designing-interactive-patterns/sketch_06_b_layers_supperpositions/index.html)

and the associated code: [https://b2renger.github.io/p5js-designing-interactive-patterns/sketch\_06\_b\_layers\_supperpositions/index.html](https://b2renger.github.io/p5js-designing-interactive-patterns/sketch_06_b_layers_supperpositions/index.html)

[**home**](https://github.com/djsnipa1/p5js-designing-interactive-patterns#contenu)