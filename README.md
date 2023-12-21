# ODD23-24-WT-JavaScript:
## AIM: To Create The Following Programs Using Java Script
## OBJECTIVE 1:
## Aim: To Create a form with java script code to calculate electricity bill.
## Step-1:  Styling (CSS):
CSS styles defining font, margins, and appearance of HTML elements.Styles for body, headings,labels, inputs, button, and result display area.

## Step-2: HTML Body:
Main content in the <body> section.Heading, form with input fields and a button, and a div for displaying results.

## Step-3: JavaScript:
JavaScript code enclosed in script tag.calculateBill() function retrieves input values, performs calculation, and displays results.

## Step-4: User Interaction:
Users input units and rate.Clicking "Calculate Bill" triggers JavaScript function, displaying the calculated bill.Styling Adjustments:CSS styles for a clean design.Adjustments include font size, button colors, and spacing.

## Step-5:
Close The HTML And Java Script Program.

## CODE:
```html
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Electricity Bill Calculator</title>
    <style>
        body {
            font-family:sans-serif;
            margin: 20px;
        }
        h2 {
            margin-bottom: 20px;
        }
        label {
            display: block;
            margin-bottom: 6px;
        }
        input {
            width: 50%; /* Set a specific width for the input elements */
            padding: 6px;
            margin-bottom: 10px;
            font-size: 14px;
        }
        button {
            padding: 8px;
            background-color:blue;
            color: white;
            border: none;
            border-radius: 4px;
            cursor: pointer;
        }
        button:hover {
            background-color: red;
        }
        #result {
            margin-top: 15px;
            font-weight: bold;
            font-size: 16px;
        }
    </style>
</head>
<body>

    <h2>Electricity Bill Calculator</h2>
    
    <form id="electricityForm">
        <label for="units">Enter Units Consumed By The Customer (kWh):</label>
        <input type="number" id="units" placeholder="Enter units" required>
<br>
        <label for="rate">Enter Rate (per kWh):</label>
        <input type="number" id="rate" placeholder="Enter rate" required>
<br>
        <button type="button" onclick="calculateBill()">Calculate Bill</button>
    </form>

    <div id="result"></div>

    <script>
        function calculateBill() {
            // Get input values
            var units = parseFloat(document.getElementById("units").value);
            var rate = parseFloat(document.getElementById("rate").value);

            // Calculate bill amount
            var billAmount = units * rate;

            // Display result
            document.getElementById("result").innerHTML = "Your Electricity Bill Amount is: ₹" + billAmount.toFixed(2);
        }
    </script>

</body>
</html>

```
## OUTPUT:
![Screenshot 2023-12-21 083910](https://github.com/saiganesh2006/ODD23-24-WT-JavaScript/assets/145742342/83e1d6d1-f7f2-4e70-99ff-29ee2f150db3)

## OBJECTIVE 2:
## AIM: To Develop a JavaScript program to compute the factorial of a given number without recursion.
## Step-1: CSS Styles:
Define styles for the body element (font, background color, text color, margin, and alignment).Specify styles for the heading (text color).Set styles for labels, input fields, and buttons (margin, padding, border, etc.).Add a hover effect for buttons.Style the result container (background color, border, padding).

## Step-2: HTML Body Content:
Display the title of the calculator using <h2>.Input, Button, and Result Display:Create a label and input field for entering a number.Include a button to trigger the factorial calculation.Display labels for the result and create a container for showing the result.

## Step-3: JavaScript Function:
Define a JavaScript function named calculateFactorial().

## Step-4: Factorial Calculation Logic:
Retrieve the input value and convert it to an integer.Check if the input is a non-negative integer.Calculate the factorial using a loop.Display the result or an error message based on the input validity.

## Step-5:
Close The HTML And Java Script Program.
## CODE:
```html
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Factorial Calculator</title>
    <style>
        body {
            font-family: 'Segoe UI', Tahoma, Geneva, Verdana, sans-serif;
            background-color:linear-gradient(135deg, #3498db, #2ecc71);
            color: #333;
            margin: 20px;
            text-align: center;
        }

        h2 {
            color: #4c54af;
        }

        label {
            display: block;
            margin-bottom: 8px;
            color: #333;
        }

        input {
            width: calc(100% - 16px);
            padding: 8px;
            margin-bottom: 16px;
            border: 1px solid #ccc;
            border-radius: 4px;
        }

        button {
            background-color: blue;
            color: white;
            padding: 10px;
            border: none;
            border-radius: 4px;
            cursor: pointer;
        }

        button:hover {
            background-color:red;
        }

        #result {
            background-color: #f0f0f0;
            border: 1px solid #ccc;
            padding: 8px;
        }
    </style>
</head>
<body>

    <h2>Factorial Calculator</h2>

    <label for="number">Enter a Number:</label>
    <input type="number" id="number" placeholder="Enter a number" required>

    <button type="button" onclick="calculateFactorial()">Calculate Factorial</button>

    <label for="result">Factorial:</label>
    <div id="result"></div>

    <script>
        function calculateFactorial() {
            // Get input value
            var number = parseInt(document.getElementById('number').value);

            // Check if the input is a non-negative integer
            if (Number.isInteger(number) && number >= 0) {
                var factorial = 1;

                // Calculate factorial
                for (var i = 2; i <= number; i++) {
                    factorial *= i;
                }

                // Display result
                document.getElementById('result').innerText =`The factorial of ${number} is: ${factorial}`;
            } else {
                // Display error for invalid input
                document.getElementById('result').innerText = 'Please enter a non-negative integer.';
            }
        }
    </script>

</body>
</html>
```
## OUTPUT:
![Screenshot 2023-12-21 092732](https://github.com/saiganesh2006/ODD23-24-WT-JavaScript/assets/145742342/cec19978-906c-40b8-8804-4506ab5dd60f)

## OBJECTIVE 3:
## AIM:


