# AREA-CALCULATOR-
AREA CALCULATOR FOR RECTANGLES OR SQUARES IN MATHEMATICS

<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Rectangle or Square Area Calculator</title>
    <style>
        body {
            font-family: Arial, sans-serif;
            text-align: center;
            padding: 20px;
        }

        label {
            font-size: 18px;
            margin-bottom: 10px;
            display: block;
        }

        input {
            padding: 10px;
            font-size: 16px;
            margin-bottom: 10px;
        }

        button {
            padding: 10px;
            font-size: 16px;
            cursor: pointer;
        }

        #result {
            font-size: 18px;
            margin-top: 20px;
            color: green;
        }
    </style>
</head>
<body>

<h1>Rectangle or Square Area Calculator</h1>
<label for="lengthInput">Enter length: </label>
<input type="number" id="lengthInput" placeholder="Enter length">
<br>
<label for="widthInput">Enter width: </label>
<input type="number" id="widthInput" placeholder="Enter width">
<br>
<button onclick="calculateArea()">Calculate Area</button>
<p id="result"></p>

<script>
    function calculateArea() {
        var lengthInput = document.getElementById("lengthInput");
        var widthInput = document.getElementById("widthInput");
        var resultElement = document.getElementById("result");

        var length = parseFloat(lengthInput.value);
        var width = parseFloat(widthInput.value);

        if (isNaN(length) || isNaN(width) || length <= 0 || width <= 0) {
            alert("Please enter valid positive numbers for length and width.");
            return;
        }

        var area = length * width;
        resultElement.innerText = "The area of the rectangle or square is: " + area;
    }
</script>

</body>
</html>
