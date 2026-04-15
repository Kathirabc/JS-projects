# Clean E-Commerce Site (Vanilla JS)

This project is a clean and responsive E-Commerce UI built using HTML,
CSS, and JavaScript. It dynamically fetches product data and displays it
in a structured layout.

------------------------------------------------------------------------

## Features

-   Dynamic product rendering
-   Skeleton loading animation
-   Responsive grid layout
-   Add to cart functionality
-   Clean UI design

------------------------------------------------------------------------

## Script Explanation (Line by Line)

### DOM Selection

const container = document.getElementById("container"); Selects the
product container

const cart = document.getElementById("cart"); Selects the cart button

let count = 0; Stores cart count

------------------------------------------------------------------------

### Skeleton Loader

function showSkeleton() { Defines loading UI

for (let i = 0; i \< 8; i++) { Loops 8 times

let sk = document.createElement("div"); Creates div

sk.className = "skeleton"; Adds skeleton class

container.appendChild(sk); Adds to UI

------------------------------------------------------------------------

### Fetch Products

async function loadProducts() { Async function

showSkeleton(); Displays loading

const res = await
fetch("https://dummyjson.com/products/category/mobile-accessories");
Fetch API call

const data = await res.json(); Convert to JSON

container.innerHTML = ""; Remove skeleton

------------------------------------------------------------------------

### Loop Products

data.products.forEach(p =\> { Iterate products

Create card, image, text, price, rating

------------------------------------------------------------------------

### Cart Logic

add.onclick = () =\> { count++; cart.innerText = `🛒 Cart: ${count}`; };
Updates cart

------------------------------------------------------------------------

### Final Render

container.appendChild(card); Adds card

loadProducts(); Initial call

------------------------------------------------------------------------

## CSS Explanation

-   Reset removes default spacing
-   Header uses flexbox and sticky positioning
-   Grid creates responsive layout
-   Cards use shadow and hover effects
-   Media queries adjust for mobile
-   Skeleton adds loading animation

------------------------------------------------------------------------

## Tech Stack

HTML, CSS, JavaScript

------------------------------------------------------------------------

## Author

Kathirvel
