---
toc: true
comments: false
layout: post
title: Javascript Calculator
description: JavaScript Calculator from Nighthawk Coders
permalink: /javascript/project/calculator
type: tangibles
---

<html lang="en">
<head>
   <meta charset="UTF-8">
   <meta name="viewport" content="width=device-width, initial-scale=1.0">
   <title>Javascript Calculator</title>
   <style>
       /* Basic styling to center the content */
       body {
           display: flex;
           flex-direction: column;
           align-items: center;
           height: 100vh;
           margin: 0;
           background-color: black; /* Set the background color to black */
           color: #C8A2C8;
       }
       #calculator-container {
           display: grid;
           grid-template-columns: repeat(4, 1fr);
           grid-gap: 5px;
           max-width: 2500px; /* Adjust as needed */
       }
       /* Styles for calculator buttons */
       .calculator-number,
       .calculator-operation,
       .calculator-clear,
       .calculator-equals {
           width: 100%;
           height: 50px;
           font-size: 20px;
           text-align: center;
           cursor: pointer;
           border: 1px solid #ccc;
           background-color: #f0f0f0; /* Default background color */
           color: black; /* Default text color */
       }
       /* Styles for specific button types */
       .calculator-number {
           background-color: #36b8de; /* Blue for numbers */
           color: white;
       }
       .calculator-operation {
           background-color: #9933FF; /* dark purple for operations */
           color: white;
       }
       .calculator-clear,
       .calculator-equals {
           background-color: #00FFCC; /* Light teal clear and equals buttons */
           color: black;
       }
        .calculator-output {
          grid-column: span 4;
          grid-row: span 1;
          padding: 0.25em;
          font-size: 20px;
          background-color: #2c3e50;
          color: #ecf0f1;
          box-shadow: 0 0 100px rgba(204, 153, 255, 1);
          display: flex;
          align-items: center;
       }
</style>




<!-- Add a containter for the animation -->
 <div id="animation">
 <div class="calculator-container">
<!-- Add a containter for the animation -->
 <div id="animation">
 <div class="calculator-container">
   <!--result-->
   <div class="calculator-output" id="output">0</div>
   <!--row 1-->
   <div class="calculator-number">1</div>
   <div class="calculator-number">2</div>
   <div class="calculator-number">3</div>
   <div class="calculator-operation">+</div>
   <!--row 2-->
   <div class="calculator-number">4</div>
   <div class="calculator-number">5</div>
   <div class="calculator-number">6</div>
   <div class="calculator-operation">-</div>
   <!--row 3-->
   <div class="calculator-number">7</div>
   <div class="calculator-number">8</div>
   <div class="calculator-number">9</div>
   <div class="calculator-operation">*</div>
   <!--row 4-->
   <div class="calculator-number">0</div>
   <div class="calculator-number">.</div>
   <div class="calculator-operation">sqrt</div>
   <div class="calculator-operation">/</div>
   <!--row 5-->
   <div class="calculator-operation">^</div>
   <div class="calculator-operation">%</div>
    <div class="calculator-equals">=</div>
   <div class="calculator-clear">A/C</div>
 </div>
<!-- JavaScript (JS) implementation of the calculator. -->
<script>
 // initialize important variables to manage calculations
 var firstNumber = null;
 var operator = null;
 var nextReady = true;
 // build objects containing key elements
 const output = document.getElementById("output");
 const numbers = document.querySelectorAll(".calculator-number");
 const operations = document.querySelectorAll(".calculator-operation");
 const clear = document.querySelectorAll(".calculator-clear");
 const equals = document.querySelectorAll(".calculator-equals");
 // Number buttons listener
 numbers.forEach(button => {
   button.addEventListener("click", function() {
     number(button.textContent);
   });
 });
 // Number action
 function number (value) { // function to input numbers into the calculator
     if (value != ".") {
         if (nextReady == true) { // nextReady is used to tell the computer when the user is going to input a completely new number
             output.innerHTML = value;
             if (value != "0") { // if statement to ensure that there are no multiple leading zeroes
                 nextReady = false;
             }
         } else {
             output.innerHTML = output.innerHTML + value; // concatenation is used to add the numbers to the end of the input
         }
     } else { // special case for adding a decimal; can't have two decimals
         if (output.innerHTML.indexOf(".") == -1) {
             output.innerHTML = output.innerHTML + value;
             nextReady = false;
         }
     }
 }
 // Operation buttons listener
 operations.forEach(button => {
   button.addEventListener("click", function() {
     operation(button.textContent);
   });
   });
 // Operator action
 function operation (choice) { // function to input operations into the calculator
     if (firstNumber == null) { // once the operation is chosen, the displayed number is stored into the variable firstNumber
         firstNumber = parseInt(output.innerHTML);
         nextReady = true;
         operator = choice;
         return; // exits function
     }
     // occurs if there is already a number stored in the calculator
     firstNumber = calculate(firstNumber, parseFloat(output.innerHTML));
     operator = choice;
     output.innerHTML = firstNumber.toString();
     nextReady = true;
     }
 // Calculator
 function calculate (first, second) { // function to calculate the result of the equation
     let result = 0;
     switch (operator) {
         case "+":
             result = first + second;
             break;
         case "-":
             result = first - second;
             break;
         case "*":
             result = first * second;
             break;
         case "/":
             result = first / second;
             break;
         case "^":
             result = first ** second;
             break;
         case "%":
             result = (first/100) * second
         case "sqrt":
              result = Math.sqrt(first);
              break;
         default:
             break;
     }
     return result;
 }
 // Equals button listener
 equals.forEach(button => {
   button.addEventListener("click", function() {
     equal();
   });
 });
 // Equal action
 function equal () { // function used when the equals button is clicked; calculates equation and displays it
     firstNumber = calculate(firstNumber, parseFloat(output.innerHTML));
     output.innerHTML = firstNumber.toString();
     nextReady = true;
 }
 // Clear button listener
 clear.forEach(button => {
   button.addEventListener("click", function() {
     clearCalc();
   });
 });
 // A/C action
 function clearCalc () { // clears calculator
     firstNumber = null;
     output.innerHTML = "0";
     nextReady = true;
 }


</script>
