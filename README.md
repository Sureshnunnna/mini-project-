#Simple Calculator Project

Description:
This project is a browser-based calculator application designed for basic mathematical operations such as addition, subtraction, multiplication, and division. It provides an intuitive user interface that allows users to input two numbers and perform operations at the click of a button. The project is lightweight and built entirely using HTML, CSS, and JavaScript.

Key Features:

User Input Fields: Two fields for entering numbers.
Operation Buttons: Buttons for each arithmetic operation (+, -, *, /).
Dynamic Results Display: Displays the calculation results instantly.
Error Handling: Ensures appropriate validation for inputs like division by zero.
Demonstrated proficiency in front-end development and JavaScript programming.
Built an interactive tool to practice logical thinking and problem-solving skills.
Improved understanding of DOM manipulation and real-time event handling.

<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Simple Calculator</title>
    <style>
        body { font-family: Arial, sans-serif; background-color: #f4f4f4; margin: 0; padding: 20px; }
        h1 { text-align: center; }
        .calculator { max-width: 300px; margin: auto; padding: 20px; background-color: white; border-radius: 8px; box-shadow: 0 2px 5px rgba(0,0,0,0.1); }
        input, button { width: 100%; margin: 5px 0; padding: 10px; border-radius: 5px; border: 1px solid #ccc; }
        button { background-color: #28a745; color: white; border: none; cursor: pointer; }
        button:hover { background-color: #218838; }
        #result { margin-top: 20px; font-size: 1.2em; text-align: center; }
    </style>
</head>
<body>
    <div class="calculator">
        <h1>Simple Calculator</h1>
        <input type="number" id="num1" placeholder="Enter first number" required>
        <input type="number" id="num2" placeholder="Enter second number" required>
        <br>
        <button onclick="calculate('+')">Add</button>
        <button onclick="calculate('-')">Subtract</button>
        <button onclick="calculate('*')">Multiply</button>
        <button onclick="calculate('/')">Divide</button>
        <h2 id="result">Result: </h2>
    </div>

    <script>
        function calculate(operation) {
            const num1 = parseFloat(document.getElementById("num1").value);
            const num2 = parseFloat(document.getElementById("num2").value);
            let result;

            if (isNaN(num1) || isNaN(num2)) {
                alert("Please enter valid numbers.");
                return;
            }

            switch (operation) {
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
                    if (num2 === 0) {
                        alert("Cannot divide by zero.");
                        return;
                    }
                    result = num1 / num2;
                    break;
                default:
                    alert("Invalid operation.");
                    return;
            }

            document.getElementById("result").innerText = "Result: " + result;
        }
    </script>
</body>
</html>

output

![image](https://github.com/user-attachments/assets/fe00b3d9-1715-47ae-afe0-f8d4e84d6d75)
![image](https://github.com/user-attachments/assets/9d656122-0ec5-46d5-8c47-acd17853516a)
![image](https://github.com/user-attachments/assets/78356791-447a-45dc-8e6a-c77c1902539a)
![image](https://github.com/user-attachments/assets/7d5e2852-c2d5-4f36-b718-e51953781c91)




