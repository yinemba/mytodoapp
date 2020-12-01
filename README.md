# html

<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
     <link rel="stylesheet" href="styles.css">      
</head>
<body>

    <form id="ourForm">
        <input id="ourField" type="text" autocomplete="off">
        <button>Create item</button>
    </form>

    <h3>Need To Doo</h3>
    <ul id="ourList">  
    </ul>
</body>
<script src="todo.js"></script>
</html>

# js

let ourForm = document.getElementById('ourForm');
let ourField = document.getElementById('ourField');
let ourList = document.getElementById('ourList');

ourForm.addEventListener('submit', (e) => {
    e.preventDefault()
    createItem(ourField.value)
});

function createItem(x) {
    let ourHTML = ` <li>${x} <button onclick='deleteItem(this)' >Delete</button></li>`
    ourList.insertAdjacentHTML('beforeend', ourHTML)
    ourField.value = ''
    ourField.focus()
};

function deleteItem(elementToDelete) {
    elementToDelete.parentElement.remove()
} 

# css
body {
  background-color: rgb(234, 239, 241);
}



