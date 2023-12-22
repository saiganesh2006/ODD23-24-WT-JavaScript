# ODD23-24-WT-JavaScript:
## AIM: 
To Create The Following Programs Using Java Script
## OBJECTIVE 1:
## Aim: 
To Create a form with java script code to calculate electricity bill.
## Step-1: 
Styling (CSS):
CSS styles defining font, margins, and appearance of HTML elements.Styles for body, headings,labels, inputs, button, and result display area.

## Step-2: 
HTML Body:
Main content in the <body> section.Heading, form with input fields and a button, and a div for displaying results.

## Step-3:
JavaScript:
JavaScript code enclosed in script tag.calculateBill() function retrieves input values, performs calculation, and displays results.

## Step-4:
User Interaction:
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
## AIM:
To Develop a JavaScript program to compute the factorial of a given number without recursion.
## Step-1: 
CSS Styles:
Define styles for the body element (font, background color, text color, margin, and alignment).Specify styles for the heading (text color).Set styles for labels, input fields, and buttons (margin, padding, border, etc.).Add a hover effect for buttons.Style the result container (background color, border, padding).

## Step-2: 
HTML Body Content:
Display the title of the calculator using <h2>.Input, Button, and Result Display:Create a label and input field for entering a number.Include a button to trigger the factorial calculation.Display labels for the result and create a container for showing the result.

## Step-3: 
JavaScript Function:
Define a JavaScript function named calculateFactorial().

## Step-4: 
Factorial Calculation Logic:
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
To Construct a JavaScript code to generate ‘N’ prime numbers.
## Step-1:
User Input:
Users input the number of prime numbers they want in the designated input field with the id "count."

## Step-2:
Generate Primes Button:
Clicking the "Generate Primes" button, which triggers the generatePrimes() function,initiating the prime number generation process.

## Step-3:
Prime Number Generation:
The script validates the entered count to ensure it is a valid positive integer.Utilizing the isPrime() function, the script generates prime numbers until the specified count is reached.

## Step-4:
Result Display:
The generated prime numbers are displayed in the "result" div, providing a visual representation of the outcome.

## Step-5:
Close the HTML and Java Script Program.
## CODE:
```html
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Prime Number Generator</title>
    <style>
        body {
            font-family: 'Segoe UI', Tahoma, Geneva, Verdana, sans-serif;
            background-color: #f4f4f4;
            color: #333;
            margin: 20px;
            text-align: center;
        }

        h2 {
            color: red;
        }

        form {
            background-color: #fff;
            border: 2px solid #3498db; /* Blue border */
            border-radius: 8px;
            box-shadow: 0 0 10px rgba(0, 0, 0, 0.1);
            padding: 20px;
            max-width: 400px;
            margin: auto;
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
            background-color:indigo;
            color: white;
            padding: 10px 15px;
            border: none;
            border-radius: 4px;
            cursor: pointer;
        }

        button:hover {
            background-color: green;
        }

        #result {
            background-color: #f0f0f0;
            border: 1px solid #ccc;
            padding: 8px;
            margin-top: 16px;
        }
    </style>
</head>
<body>

    <h2>Prime Number Generator</h2>

    <form id="primeForm">
        <label for="count">Enter the number of prime numbers :</label>
        <input type="number" id="count" placeholder="Enter N" required>

        <button type="button" onclick="generatePrimes()">Generate Primes</button>

        <label for="result">Prime Numbers:</label>
        <div id="result"></div>
    </form>

    <script>
        function isPrime(num) {
            for (var i = 2; i < num; i++) {
                if (num % i === 0) {
                    return false;
                }
            }
            return num > 1;
        }

        function generatePrimes() {
            var count = parseInt(document.getElementById('count').value);
            var primeNumbers = [];

            if (count > 0) {
                var num = 2; // Start with the first prime number

                while (primeNumbers.length < count) {
                    if (isPrime(num)) {
                        primeNumbers.push(num);
                    }
                    num++;
                }

                document.getElementById('result').innerText = primeNumbers.join(', ');
            } else {
                document.getElementById('result').innerText = 'Please enter a valid count.';
            }
        }
    </script>

</body>
</html>
```
## OUTPUT:
![Screenshot 2023-12-21 204350](https://github.com/saiganesh2006/ODD23-24-WT-JavaScript/assets/145742342/0a54eca8-c67e-4ff7-8a08-3621740899a9)

## OBJECTIVE 4:
## AIM:
To Construct a JavaScript program to implement a simple calculator.
## Step-1:
JavaScript Function:
The calculate() function retrieves input values and the selected operator.It performs calculations based on the operator and displays the result in the designated div.

## Step-2:
User Interaction:
Users input numerical values and select an operator from the dropdown.Clicking the "Calculate" button triggers the calculate() function for real-time interaction.

## Step-3:
Result Display:
The result is dynamically displayed in the "result" div.Special handling prevents division by zero and informs the user of an invalid operator.

## Step-4:
Styling Highlights:
The styling emphasizes a dark background with contrasting text and button colors.Subtle shadow effects and hover states enhance the visual appeal and interactivity of the calculator.

## Step-5:
Close the HTML and Java Script program.
## CODE:
```html
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Simple Calculator</title>
    <style>
        body {
            font-family: 'Segoe UI', Tahoma, Geneva, Verdana, sans-serif;
            color: #fff;
            margin: 0;
            padding: 0;
            display: flex;
            justify-content: center;
            align-items: center;
            height: 100vh;
        }

        form {
            background-color: #444;
            border: 2px solid lightblue;
            border-radius: 8px;
            box-shadow: 0 0 20px rgba(0, 0, 0, 0.5);
            padding: 20px;
            max-width: 400px;
            width: 100%;
            text-align: center;
        }

        h2 {
            color: blue; /* Blue color for the heading */
            text-shadow: 2px 2px 4px rgba(0, 0, 0, 0.5);
        }

        label {
            display: block;
            margin-bottom: 8px;
            color: #fff;
        }

        input, select {
            width: calc(100% - 16px);
            padding: 8px;
            margin-bottom: 16px;
            border: 1px solid #ccc;
            border-radius: 4px;
            background: black; /* Dark input background */
            color: #fff;
        }

        button {
            background-color:blueviolet; /* Blueviolet color for the button */
            color: white;
            padding: 10px 15px;
            border: none;
            border-radius: 4px;
            cursor: pointer;
        }

        button:hover {
            background-color: #2071a8; /* Darker shade of blue on hover */
        }

        #result {
            background-color: #333;
            border: 1px solid #3498db;
            padding: 8px;
            margin-top: 16px;
            font-weight: bold;
            color: #fff;
        }
    </style>
</head>
<body>

    <form id="calculatorForm">
        <h2>Simple Calculator</h2>

        <label for="num1">Enter number 1:</label>
        <input type="number" id="num1" placeholder="Enter number 1" required>

        <label for="num2">Enter number 2:</label>
        <input type="number" id="num2" placeholder="Enter number 2" required>

        <label for="operator">Select operator:</label>
        <select id="operator" required>
            <option value="+">+</option>
            <option value="-">-</option>
            <option value="*">*</option>
            <option value="/">/</option>
        </select>
        <button type="button" onclick="calculate()">Calculate</button>

        <div id="result"></div>
    </form>

    <script>
        function calculate() {
            var num1 = parseFloat(document.getElementById('num1').value);
            var num2 = parseFloat(document.getElementById('num2').value);
            var operator = document.getElementById('operator').value;

            var result;

            switch (operator) {
                case '+':
                    result = num1 + num2;
                    break;
                case '-':
                    result = num1 - num2;
                    break;
                case '*':
                    result = num1 * num2;
                    break;
                case '/':
                    if (num2 !== 0) {
                        result = num1 / num2;
                    } else {
                        document.getElementById('result').innerText = 'Cannot divide by zero.';
                        return;
                    }
                    break;
                default:
                    document.getElementById('result').innerText = 'Invalid operator.';
                    return;
            }

            document.getElementById('result').innerText = `Result: ${result}`;
        }
    </script>

</body>
</html>
```
## OUTPUT:
![image](https://github.com/saiganesh2006/ODD23-24-WT-JavaScript/assets/145742342/38149818-8166-40bd-9b68-60d2de8df896)
## OBJECTIVE 5:
## AIM:
To Design a simple text editor JavaScript application where we can manipulate the user input in different styles, edit the input, capitalize, and many string operations.

## Step-1:
Body Styles:
body styles include font family, background gradient, and flex layout.h2 styles define text color and shadow for the heading.Textarea and Button Styles:textarea styles specify width, height, padding, and border for the input area.button styles define appearance, padding, and cursor for the buttons.

## Step-2:
JavaScript:
Buttons have onclick attributes triggering specific functions when clicked.Functions like capitalizeText(), makeUppercase(), etc., handle button actions.

## Step-3:
Functionality:
capitalizeText() capitalizes the first letter of each word.makeUppercase() converts input text to uppercase.

## Step-4:
User Input:
Users type text into the textarea.The textarea is styled with specific dimensions and appearance.Clicking buttons performs actions like capitalization or reversal.Results are displayed in the output div with specified styles.
## Step-5:
Close the HTML and Java Script Program.
## CODE:
```html
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Simple Text Editor</title>
    <style>
        body {
            font-family: 'Segoe UI', Tahoma, Geneva, Verdana, sans-serif;
            background: linear-gradient(to right, red, black, #bcb8b1);
            color: #fff;
            margin: 0;
            padding: 0;
            display: flex;
            flex-direction: column;
            align-items: center;
            justify-content: center;
            height: 100vh;
        }

        h2 {
            color: #fff;
            text-shadow: 2px 2px 4px rgba(0, 0, 0, 0.5);
        }

        textarea {
            width: 80%;
            height: 150px;
            padding: 12px;
            margin-bottom: 16px;
            border: 2px solid #3498db;
            border-radius: 8px;
            resize: none;
            font-size: 16px;
            color: #333;
            background-color: #fff;
        }

        button {
            background-color:indigo;
            color: white;
            padding: 12px 20px;
            border: none;
            border-radius: 4px;
            cursor: pointer;
            margin-right: 8px;
            margin-bottom: 8px; /* Added margin for spacing */
            font-size: 16px;
        }
        button:hover {
            background-color: green; /* Darker shade of blue on hover */
        }

        #output {
            background-color: #fff;
            border: 2px solid #3498db;
            padding: 12px;
            text-align: left;
            border-radius: 8px;
            width: 80%;
            font-size: 16px;
            color: #333;
        }
    </style>
</head>
<body>

    <h2>Simple Text Editor</h2>

    <textarea id="inputText" placeholder="Type your text here..."></textarea>

    <div>
        <button onclick="capitalizeText()">Capitalize</button>
        <button onclick="makeUppercase()">Uppercase</button>
        <button onclick="makeLowercase()">Lowercase</button>
        <button onclick="reverseText()">Reverse</button>
        <button onclick="clearText()">Clear</button>
    </div>

    <div id="output"></div>

    <script>
        function capitalizeText() {
            var inputText = document.getElementById('inputText').value;
            var outputDiv = document.getElementById('output');

            var capitalizedText = inputText.replace(/\b\w/g, function (char) {
                return char.toUpperCase();
            });

            outputDiv.innerText = capitalizedText;
        }

        function makeUppercase() {
            var inputText = document.getElementById('inputText').value;
            var outputDiv = document.getElementById('output');

            outputDiv.innerText = inputText.toUpperCase();
        }

        function makeLowercase() {
            var inputText = document.getElementById('inputText').value;
            var outputDiv = document.getElementById('output');

            outputDiv.innerText = inputText.toLowerCase();
        }

        function reverseText() {
            var inputText = document.getElementById('inputText').value;
            var outputDiv = document.getElementById('output');

            outputDiv.innerText = inputText.split('').reverse().join('');
        }

        function clearText() {
            document.getElementById('inputText').value = '';
            document.getElementById('output').innerText = '';
        }
    </script>

</body>
</html>
```

## OUTPUT:
## (i) To Make Tent To Capitalize:
![Screenshot 2023-12-22 100629](https://github.com/saiganesh2006/ODD23-24-WT-JavaScript/assets/145742342/f1f3259e-a7c5-48c4-b812-00408daf38bd)
## (ii) To Make Text To Upper Case:
![Screenshot 2023-12-22 100640](https://github.com/saiganesh2006/ODD23-24-WT-JavaScript/assets/145742342/06a95cfd-e58e-4580-af29-cbabba5238b1)
## (iii) To Make Text To lower Case:
![Screenshot 2023-12-22 100650](https://github.com/saiganesh2006/ODD23-24-WT-JavaScript/assets/145742342/4c2b61e5-a8ca-4506-a047-b20ef717d9a0)
## (iv) To make Text To Reverse Order:
![Screenshot 2023-12-22 100659](https://github.com/saiganesh2006/ODD23-24-WT-JavaScript/assets/145742342/6c4a7046-06ba-4f20-b192-005ab212a900)
## (v) To Make Text Clear:
![Screenshot 2023-12-22 100711](https://github.com/saiganesh2006/ODD23-24-WT-JavaScript/assets/145742342/2f8f8d4f-cc47-4750-b347-b9a0cc2eb618)

## OJECTIVE 6:
## AIM:
To Design a JavaScript program which displays error messages when a field in form is entered incorrectly.
## Step-1 :
JavaScript Validation:
Write JavaScript functions to validate form inputs. Include checks for required fields, email format, or any custom validation.

## Step-2 :
CSS Styling (Optional):
Enhance the form's visual appeal by applying CSS styles. Customize colors, fonts, and layouts to create an attractive user interface.

## Step-3 :
Testing and Debugging:
Test the form by entering values and submitting. Debug any issues with the validation logic or styling.

## Step-4 :
Refinement and Deployment:
Iterate on the code, refining validation, styling, and functionality as needed. Deploy the form on a web server or integrate it into your project.

## Step-5:
Close the HTML and Java Script Program.

## CODE:
```html
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Form Validation</title>
    <style>
        body {
            font-family: 'Segoe UI', Tahoma, Geneva, Verdana, sans-serif;
            background: linear-gradient(to right, red,black,blue,yellow);
            color: #fff;
            margin: 0;
            padding: 0;
            display: flex;
            flex-direction: column;
            align-items: center;
            justify-content: center;
            height: 100vh;
        }

        h2 {
            color: #fff;
            text-shadow: 2px 2px 4px rgba(0, 0, 0, 0.5);
            margin-bottom: 30px;
        }

        form {
            width: 80%;
            max-width: 400px;
            margin: 0 auto;
            background-color: #fff;
            padding: 20px;
            border-radius: 8px;
            box-shadow: 0 0 20px rgba(0, 0, 0, 0.3);
        }

        label {
            display: block;
            margin-bottom: 8px;
            color: #333;
        }

        input {
            width: calc(100% - 16px);
            padding: 12px;
            margin-bottom: 16px;
            border: 2px solid #3498db;
            border-radius: 4px;
            box-sizing: border-box;
            font-size: 16px;
            color: #333;
        }

        button {
            background-color: indigo;
            color: white;
            padding: 12px 20px;
            border: none;
            border-radius: 4px;
            cursor: pointer;
            font-size: 16px;
        }

        button:hover {
            background-color: #45a049;
        }

        .error-message {
            color: blue;
            margin-top: -8px;
            margin-bottom: 16px;
            text-align: left;
        }
    </style>
</head>
<body>

    <h2>Validation Form</h2>

    <form id="myForm" onsubmit="validateForm(); return false;">
        <label for="name">Name:</label>
        <input type="text" id="name" name="name">
        <div id="nameError" class="error-message"></div>

        <label for="email">Email:</label>
        <input type="email" id="email" name="email">
        <div id="emailError" class="error-message"></div>

        <button type="submit">Submit</button>
    </form>

    <script>
        function validateForm() {
            // Reset error messages
            document.getElementById('nameError').innerText = '';
            document.getElementById('emailError').innerText = '';

            // Get form values
            var name = document.getElementById('name').value;
            var email = document.getElementById('email').value;

            // Validate name
            if (name.trim() === '') {
                document.getElementById('nameError').innerText = 'Name is required.';
            }

            // Validate email
            if (email.trim() === '') {
                document.getElementById('emailError').innerText = 'Email is required.';
            } else if (!isValidEmail(email)) {
                document.getElementById('emailError').innerText = 'Invalid email format.';
            }
        }

        function isValidEmail(email) {
            // Basic email validation regex
            var emailRegex = /^[^\s@]+@[^\s@]+\.[^\s@]+$/;
            return emailRegex.test(email);
        }
    </script>

</body>
</html>
```

## OUTPUT:
![Screenshot 2023-12-22 104706](https://github.com/saiganesh2006/ODD23-24-WT-JavaScript/assets/145742342/0676ced5-6d08-485a-95e4-7a2654f184b8)

![Screenshot 2023-12-22 104722](https://github.com/saiganesh2006/ODD23-24-WT-JavaScript/assets/145742342/dc1c68c3-0d45-491a-983a-8f149899dfdd)

![Screenshot 2023-12-22 104737](https://github.com/saiganesh2006/ODD23-24-WT-JavaScript/assets/145742342/48899b64-5c5c-4f39-a528-f6ba02613532)


## REUSLT:
Succesfully Executed all the Given JAVA SCRIPT Programs.

## DEVELOPED BY: D.B.V.SAI GANESH
## REGISTER NO: 212223240025
