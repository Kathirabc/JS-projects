#  Kathirvel's Todo App (LocalStorage Powered)

**"A simple yet powerful Todo App that remembers everything---even after
refresh."**

This project is a fully functional Todo application built using
**JavaScript, HTML, and LocalStorage**.

------------------------------------------------------------------------

## 🌟 Features

-    Add new tasks\
-    Edit tasks\
-    Delete tasks\
-    Mark tasks complete\
-    LocalStorage persistence\
-    Enter key support

------------------------------------------------------------------------

## 💻 Script Explanation (Line-by-Line)

### Load Data

``` javascript
let todos = JSON.parse(localStorage.getItem("vals")) || [];
```

Loads saved tasks or initializes empty array.

``` javascript
let editIndex = -1;
```

Tracks edit mode (-1 = no edit).

------------------------------------------------------------------------

### DOM Access

``` javascript
const userinput = document.getElementById("userinput");
const btn = document.getElementById("btn");
const logg = document.getElementById("logg");
```

Gets elements from HTML.

------------------------------------------------------------------------

### Save Data

``` javascript
function savedata() {
    localStorage.setItem("vals", JSON.stringify(todos));
}
```

Stores tasks in browser.

------------------------------------------------------------------------

### Render Function

``` javascript
function renderTodos() {
    logg.innerHTML = "";
```

Clears UI before re-render.

``` javascript
todos.forEach((todo, index) => {
```

Loops through tasks.

``` javascript
const li = document.createElement("li");
```

Creates list item.

``` javascript
const span = document.createElement("span");
span.innerText = todo.text;
```

Displays text.

``` javascript
if (todo.done) span.classList.add("done");
```

Marks completed tasks.

``` javascript
span.addEventListener("click", () => {
    todo.done = !todo.done;
    savedata();
    renderTodos();
});
```

Toggles completion.

------------------------------------------------------------------------

### Edit

``` javascript
edit.addEventListener("click", () => {
    userinput.value = todo.text;
    editIndex = index;
    btn.innerText = "Update";
});
```

------------------------------------------------------------------------

### Delete

``` javascript
del.addEventListener("click", () => {
    todos.splice(index, 1);
    savedata();
    renderTodos();
});
```

------------------------------------------------------------------------

### Add / Update

``` javascript
function handleTask() {
    const val = userinput.value.trim();
```

``` javascript
if (val === "") return;
```

``` javascript
if (editIndex === -1) {
    todos.push({ text: val, done: false });
} else {
    todos[editIndex].text = val;
    editIndex = -1;
    btn.innerText = "Add";
}
```

``` javascript
userinput.value = "";
savedata();
renderTodos();
```

------------------------------------------------------------------------

### Events

``` javascript
btn.addEventListener("click", handleTask);
```

``` javascript
userinput.addEventListener("keypress", (e) => {
    if (e.key === "Enter") handleTask();
});
```

``` javascript
renderTodos();
```

------------------------------------------------------------------------

## Tech Stack

-   HTML
-   CSS
-   JavaScript
-   LocalStorage

------------------------------------------------------------------------

## Author

Kathirvel
