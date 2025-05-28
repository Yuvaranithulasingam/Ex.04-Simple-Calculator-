![image](https://github.com/user-attachments/assets/641397b6-fd46-4091-ac21-6b52cc419e4e)# EXP_04-Simple-caluculator

#### NAME: YUVARANI T
#### REG. NO: 212222110057

### Date:

### AIM:
To develop a Simple Calculator using React.js with clean and responsive design, ensuring a smooth user experience across different screen sizes.

### ALGORITHM:

#### STEP 1
Create a React App.

#### STEP 2
Open a terminal and run:
npx create-react-app simple-calculator
cd simple-calculator
npm start

#### STEP 3
Inside the src/ folder, create a new file Calculator.js and define the basic structure.

#### STEP 4
Plan the UI: Display screen, number buttons (0-9), operators (+, -, *, /), clear (C), and equal (=).

#### STEP 5
Create a new file Calculator.css in src/ and add the styling.

#### STEP 6
Open src/App.js and modify it.

#### STEP 7
Start the development server. npm start

#### STEP 8
Open http://localhost:3000/ in the browser.

#### STEP 9
Test the calculator by entering numbers and operations.

#### STEP 10
Fix styling issues and refine content placement.

#### STEP 11
Deploy the website.

#### STEP 12
Upload to GitHub Pages for free hosting.

### PROGRAM:
App.jsx
```
import React from "react";
import Calculator from "./calculator";
function App() {
  return (
    <div className="App">
      <h1>Simple Calculator</h1>
      <Calculator />
    </div>
  );
}

export default App;
```
calculator.jsx
```
import React, { useState } from "react";
import "./Calculator.css";

function Calculator() {
  const [input, setInput] = useState("");

  const handleClick = (value) => {
    setInput((prev) => prev + value);
  };

  const handleClear = () => {
    setInput("");
  };

  const handleEqual = () => {
    try {
      setInput(eval(input).toString());
    } catch {
      setInput("Error");
    }
  };

  return (
    <div className="calculator">
      <input type="text" value={input} readOnly />
      <div className="buttons">
        {["7", "8", "9", "/", "4", "5", "6", "*", "1", "2", "3", "-", "0", ".", "=", "+"].map((btn) =>
          btn === "=" ? (
            <button key={btn} onClick={handleEqual}>{btn}</button>
          ) : (
            <button key={btn} onClick={() => handleClick(btn)}>{btn}</button>
          )
        )}
        <button className="clear" onClick={handleClear}>C</button>
      </div>
    </div>
  );
}

export default Calculator;
```
calculator.css
```
/* src/Calculator.css */
.calculator {
    width: 300px;
    margin: 50px auto;
    padding: 20px;
    background: #f4f4f4;
    border-radius: 10px;
    box-shadow: 0 0 10px gray;
    text-align: center;
  }
  
  .calculator input {
    width: 100%;
    height: 50px;
    font-size: 1.5rem;
    text-align: right;
    margin-bottom: 10px;
    padding: 5px;
    box-sizing: border-box;
  }
  
  .buttons {
    display: grid;
    grid-template-columns: repeat(4, 1fr);
    gap: 10px;
  }
  
  button {
    padding: 15px;
    font-size: 1.2rem;
    border: none;
    border-radius: 5px;
    background-color: #2e86de;
    color: white;
    cursor: pointer;
  }
  
  button:hover {
    background-color: #1b4f72;
  }
  
  button.clear {
    grid-column: span 4;
    background-color: #e74c3c;
  }
```
### OUTPUT:
![image](https://github.com/user-attachments/assets/5f9c9d7a-be63-487f-b262-ac6de6dfd1f1)
![image](https://github.com/user-attachments/assets/df796aaa-6986-4719-929f-b24a5a01202e)
![image](https://github.com/user-attachments/assets/9535bffd-1f96-473d-b1f7-095dcd0ee84c)

### RESULT:
The program for developing a simple calculator in React.js is executed successfully.
