# Ex.08 Design of a Standard Calculator
## Date:

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
```
<html>
<head>

   <title>Simple Calculator</title>
   <style>
       #calc {
           text-align: center;
           margin: auto;
           width: 240px;
       }
       .button {
           margin-left: 550px;
           margin-right: 550px;
           padding: 30px;
           background-color:floralwhite(235, 228, 235);
           color: rgb(234, 241, 14);
           border:5px solid rgb(13, 1, 19)
       }

       .button input[type="button"] {
           background-color: white;
           height: 50px;
           width: 50px;
           margin: 0 2px;
           border: 3px solid rgb(12, 11, 9);
       }
   </style>
</head>

<body style="background-color: rgb(206, 235, 23);">
       <h1 align="center" style="color: rgb(24, 47, 222);">SHYAM KUMAR E 23004557</h1>
<h1 align="center" style="color: rgb(40, 93, 250);">SIMPLE CALCULATOR</h1>
       <div class="button">
           <center>
           <input type="text" id="t1" style="width:270px; height:30px;"><br><br>
           <input type="button" onkeydown="op(event)" onclick="f('7')" value="7">
           <input type="button" onkeydown="op(event)" onclick="f('8')" value="8">
           <input type="button" onkeydown="op(event)" onclick="f('9')" value="9">
           <input type="button" onkeydown="op(event)" onclick="f('+')" value="+">
           <input type="button" onkeydown="op(event)" value="C"  onclick="clr()"><br><br>

           <input type="button" onkeydown="op(event)" onclick="f('4')" value="4">
           <input type="button" onkeydown="op(event)" onclick="f('5')" value="5">
           <input type="button" onkeydown="op(event)" onclick="f('6')" value="6">
           <input type="button" onkeydown="op(event)" onclick="f('*')" value="x">
           <input type="button" onkeydown="op(event)" onclick="f('^0.5')" value="&radic;"><br><br>
   
           <input type="button" onkeydown="op(event)" onclick="f('1')" value="1">
           <input type="button" onkeydown="op(event)" onclick="f('2')" value="2">
           <input type="button" onkeydown="op(event)" onclick="f('3')" value="3">
           <input type="button" onkeydown="op(event)" onclick="f('-')" value="-">
           <input type="button" onkeydown="op(event)" onclick="f('/')" value="%"><br><br>
       
           <input type="button" onkeydown="op(event)" onclick="f('0')" value="0">
           <input type="button" onkeydown="op(event)" onclick="f('.')"
               value=".">
           
           <input type="button" onkeydown="op(event)" onclick="f('ANS')" value="ANS">
           <input type="button" onclick="solve()" value="=" style="color: rgb(239, 12, 216); width:110px;font-weight:bolder;">
       </center>
       </div>
</body>
<script src="https://cdnjs.cloudflare.com/ajax/libs/mathjs/9.4.4/math.js"></script>

<script>
   function f(val) {
       document.getElementById('t1').value += val;
   }

   function clr() {
       document.getElementById('t1').value = "";
   }

   function op(event) {
       if (event.key == '7' || event.key == '8' || event.key == '9' || event.key == '+' || event.key == '+/-' || event.key == '4' ||
           event.key == '5' || event.key == '6' || event.key == '*' || event.key == '^0.5' || event.key == '1' ||
           event.key == '2' || event.key == '3' || event.key == '-' || event.key == '/' || event.key == '0' || event.key == '.') {
           document.getElementById('t1').value += event.key;
       }
   }

   var cal = document.getElementById('calc');
   cal.onkeyup = function (event) {
       if (event.keyCode == 13) {
           console.log("Enter");
           solve();
       }
   }

   function solve() {
       let x = document.getElementById('t1').value;
       let y = math.evaluate(x); // Assuming you have included the math.js library
       document.getElementById('t1').value = y;
   }
</script>

</html>
```


## OUTPUT:
![Screenshot 2024-04-27 085638](https://github.com/Romanshyam/Calc/assets/123962992/10f286e2-a360-4eb5-9ae0-9039980adf96)

## RESULT:
The program for designing a standard calculator using HTML and CSS is executed successfully.
