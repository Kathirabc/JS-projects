# Calculator App 

**"A calculator that feels as smooth as your thoughts---fast,
responsive, and mobile-ready."**

This isn't just any calculator. It's **Kathirvel's Calculator**, crafted
with HTML, CSS Grid, and JavaScript. Built to fit your screen perfectly,
whether you're on a tiny phone or a big desktop monitor.

 [Click to see my Project](https://frontend-project-5e1776.gitlab.io/Calculator_App/)

------------------------------------------------------------------------

## Features That Shine

-   **Fully Responsive Layout** -- Looks perfect on any screen: mobile,
    tablet, or desktop\
-   **Intuitive Grid Layout** -- Buttons are logically placed, just like
    a real calculator\
-   **All Basic Operations** -- Addition, subtraction, multiplication,
    division\
-   **AC & Delete** -- Clear everything or fix mistakes without
    frustration\
-   **Touch-Friendly Buttons** -- Large, rounded, and satisfying to
    press\
-   **Quick Results** -- Get calculations instantly with a single tap

------------------------------------------------------------------------

##  Layout That Talks

This calculator is powered by **CSS Grid**, making it clean, modern, and
scalable.

### How the grid works:

``` css
div {
    display: grid;
    grid-template-columns: repeat(4, 1fr); /* Four equal columns */
    gap: 10px;                             /* Space between buttons */
}
```

-   Input & AC buttons span all 4 columns → full-width display\
-   Equal button spans two rows → stands out for quick access\
-   Other buttons fit neatly into the remaining grid, maintaining
    symmetry

Think of it as a digital playground: every button has its place, every
function is just a tap away.

------------------------------------------------------------------------

##  JavaScript Magic Behind the Scenes

### Enter Input

``` javascript
function enterinput(val) {
    userinput.value += val;
}
```

Adds numbers or operators to the screen as you click them.\
Example: Click `2`, `+`, `3` → **"2+3"**

------------------------------------------------------------------------

### Calculate Result

``` javascript
function finalResult() {
    userinput.value = eval(userinput.value);
}
```

Turns your input string into a real calculation.

⚠️ **Note:** `eval()` is convenient but risky in large apps. Use a
custom parser for production apps.

------------------------------------------------------------------------

### Clear Everything

``` javascript
function clearInput() {
    userinput.value = "";
}
```

Reset your screen instantly.

------------------------------------------------------------------------

### Delete Last Entry

``` javascript
function deleteLast() {
    userinput.value = userinput.value.slice(0, -1);
}
```

Fix mistakes without clearing everything.

------------------------------------------------------------------------

## Responsiveness That Feels Alive

``` css
@media (max-width: 480px) {
    button { height: 55px; font-size: 1.8rem; }
    input { height: 45px; font-size: 1.8rem; }
}

@media (min-width: 768px) {
    div { max-width: 500px; }
    button { height: 70px; font-size: 1.9rem; }
    input { height: 60px; font-size: 1.8rem; }
}
```

-   Buttons stay finger-friendly on small screens\
-   Desktop users get larger, more comfortable controls

------------------------------------------------------------------------

## ⚡ Why This Calculator Stands Out

-   Grid-first design → Clean and modern\
-   Fully responsive → Works on every device\
-   Interactive JS → Smooth and intuitive\
-   Touch-friendly UI → Designed for real users

------------------------------------------------------------------------

##  Future Upgrades

-    Safe Calculation Engine (Replace `eval()`)\
-    Keyboard Support\
-    Dark Mode\
-   Animations & Feedback

------------------------------------------------------------------------

##  Tech Stack

-   HTML\
-   CSS (Grid + Media Queries)\
-   JavaScript

------------------------------------------------------------------------

## Author

**Kathirvel**

------------------------------------------------------------------------

⭐ If you like this project, consider giving it a star!