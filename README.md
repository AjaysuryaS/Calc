# Ex.08 Design of a Standard Calculator
## Date:
17/04/23

## AIM:
To design a web application for a standard calculator with minimum five operations.

## DESIGN STEPS:

### Step 1:
Clone the github repository and create Django admin interface.

### Step 2:
Change settings.py file to allow request from all hosts.

### Step 3:
Use CSS for creating attractive colors.

### Step 4:
Write JavaScript program for implementing five different operations.

### Step 5:
Validate the HTML and CSS code.

### Step 6:
Publish the website in the given URL.

## PROGRAM :
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Calculator</title>
    <style>
        .calculator {
            width: 300px;
            margin: 50px auto;
            background-color: #f3f3f3;
            border-radius: 10px;
            padding: 20px;
            box-shadow: 0 0 10px rgba(0, 0, 0, 0.1);
        }
        .output {
            width: 100%;
            height: 50px;
            border: 1px solid #ccc;
            border-radius: 5px;
            margin-bottom: 10px;
            padding: 5px;
            font-size: 20px;
            text-align: right;
        }
        .button {
            width: 50px;
            height: 50px;
            margin: 5px;
            font-size: 20px;
            border: none;
            border-radius: 5px;
            cursor: pointer;
            outline: none;
        }
        .button.operator {
            background-color: #ff7f50; /* Coral */
        }
        .button.number {
            background-color: #87ceeb; /* SkyBlue */
        }
        .button.special {
            background-color: #32cd32; /* LimeGreen */
        }
    </style>
</head>
<body>
<div class="calculator">
    <input type="text" class="output" id="output" readonly>
    <div>
        <button class="button special" onclick="fn(this)">C</button>
        <button class="button special" onclick="fn(this)" id="back">←</button>
        <button class="button special" onclick="fn(this)">%</button>
        <button class="button operator" onclick="fn(this)">/</button>
    </div>
    <div>
        <button class="button number" onclick="fn(this)">7</button>
        <button class="button number" onclick="fn(this)">8</button>
        <button class="button number" onclick="fn(this)">9</button>
        <button class="button operator" onclick="fn(this)">*</button>
    </div>
    <div>
        <button class="button number" onclick="fn(this)">4</button>
        <button class="button number" onclick="fn(this)">5</button>
        <button class="button number" onclick="fn(this)">6</button>
        <button class="button operator" onclick="fn(this)">-</button>
    </div>
    <div>
        <button class="button number" onclick="fn(this)">1</button>
        <button class="button number" onclick="fn(this)">2</button>
        <button class="button number" onclick="fn(this)">3</button>
        <button class="button operator" onclick="fn(this)">+</button>
    </div>
    <div>
        <button class="button number" onclick="fn(this)">0</button>
        <button class="button number" onclick="fn(this)">.</button>
        <button class="button operator" onclick="fn(this)">=</button>
    </div>
</div>
<script>
    function fn(e) {
        var output = document.getElementById('output');
        if (e.innerHTML == '=') {
            output.value = eval(output.value);
        } else if (e.id == 'back') {
            var v = output.value;
            output.value = v.substring(0, v.length - 1);
        } else if (e.innerHTML == 'C') {
            output.value = '';
        } else {
            output.value += e.innerHTML;
        }
    }
</script>
</body>
</html>

## OUTPUT:
![Screenshot 2024-04-17 142858](https://github.com/AjaysuryaS/Calc/assets/114158396/22158b7c-f4ca-4adc-af5d-bee46f59cd17)
![Screenshot 2024-04-17 142914](https://github.com/AjaysuryaS/Calc/assets/114158396/c8779270-b4de-47f6-b6c4-32e18b263acb)

## RESULT:
The program for designing a standard calculator using HTML and CSS is executed successfully.
