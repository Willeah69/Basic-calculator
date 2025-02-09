<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Number Addition Calculator</title>
    <link rel="stylesheet" href="style.css"> <!-- Link to the CSS file -->
</head>
<body>
    <div class="container">
        <div class="title">Number Addition</div>
       
        <div class="input-group">
            <label for="num1">First Number:</label>
            <input type="text" id="num1" placeholder="Enter first number">
        </div>
       
        <div class="input-group">
            <label for="num2">Second Number:</label>
            <input type="text" id="num2" placeholder="Enter second number">
        </div>
       
        <div class="input-group">
            <label for="result">Result:</label>
            <input type="text" id="result" readonly>
        </div>

        <div class="button-group">
            <button id="clearBtn">Clear</button>
            <button id="addBtn">Add</button>
        </div>
    </div>

    <script src="script.js"></script> <!-- Link to the JavaScript file -->
</body>
</html>

body {
    font-family: Arial, sans-serif;
    display: flex;
    justify-content: center;
    align-items: center;
    height: 100vh;
    margin: 0;
    background-color: #f0f0f0;
}

.container {
    border: 1px solid #ccc;
    border-radius: 4px;
    padding: 20px;
    background-color: white;
    box-shadow: 0 2px 4px rgba(0,0,0,0.1);
    width: 300px; /* Set a fixed width for better layout */
}

.title {
    font-size: 18px;
    font-weight: bold;
    margin-bottom: 15px;
    color: #333;
    text-align: center; /* Center the title */
}

.input-group {
    display: flex;
    align-items: center;
    margin-bottom: 10px;
}

.input-group label {
    width: 120px;
    text-align: right;
    margin-right: 10px;
}

input[type="text"] {
    width: 150px;
    padding: 4px;
    border: 1px solid #ccc;
    border-radius: 3px;
}

.button-group {
    margin-top: 15px;
    display: flex;
    gap: 10px;
    justify-content: center; /* Center the buttons */
}

button {
    padding: 6px 12px;
    border: 1px solid #ccc;
    border-radius: 3px;
    background-color: #f8f8f8;
    cursor: pointer;
}

button:hover {
    background-color: #e8e8e8;
}
// Add button functionality
document.getElementById('addBtn').addEventListener('click', function() {
    const num1 = parseFloat(document.getElementById('num1').value) || 0;
    const num2 = parseFloat(document.getElementById('num2').value) || 0;
    const result = num1 + num2;
    document.getElementById('result').value = result;
});

// Clear button functionality
document.getElementById('clearBtn').addEventListener('click', function() {
    document.getElementById('num1').value = '';
    document.getElementById('num2').value = '';
    document.getElementById('result').value = '';
});
