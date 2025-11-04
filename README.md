# MWAD-EXP_04-Simple-caluculator
## Date:

## AIM
To  develop a Simple Calculator using React.js with clean and responsive design, ensuring a smooth user experience across different screen sizes.

## ALGORITHM
### STEP 1
Create a React App.

### STEP 2
Open a terminal and run:
  <ul><li>npx create-react-app simple-calculator</li>
  <li>cd simple-calculator</li>
  <li>npm start</li></ul>

### STEP 3
Inside the src/ folder, create a new file Calculator.js and define the basic structure.

### STEP 4
Plan the UI: Display screen, number buttons (0-9), operators (+, -, *, /), clear (C), and equal (=).

### STEP 5
Create a new file Calculator.css in src/ and add the styling.

### STEP 6
Open src/App.js and modify it.

### STEP 7
Start the development server.
  npm start

### STEP 8
Open http://localhost:3000/ in the browser.

### STEP 9
Test the calculator by entering numbers and operations.

### STEP 10
Fix styling issues and refine content placement.

### STEP 11
Deploy the website.

### STEP 12
Upload to GitHub Pages for free hosting.

## PROGRAM:
# App.js
```
import React from "react";
import Calculator from "./components/Calculator";
import "./App.css";

function App() {
  return (
    <div className="app">
      <h1>Simple Calculator</h1>
      <Calculator />
    </div>
  );
}

export default App;
```
# Calcultor.js
```
import React, { useState } from "react";

const Calculator = () => {
  const [input, setInput] = useState("");

  const handleClick = (value) => {
    setInput(input + value);
  };

  const clearInput = () => {
    setInput("");
  };

  const deleteLast = () => {
    setInput(input.slice(0, -1));
  };

  const calculateResult = () => {
    try {
      setInput(eval(input).toString());
    } catch {
      setInput("Error");
    }
  };

  return (
    <div className="calculator">
      <input type="text" value={input} readOnly className="display" />
      <div className="buttons">
        <button onClick={clearInput} className="span-two">C</button>
        <button onClick={deleteLast}>DEL</button>
        <button onClick={() => handleClick("/")}>÷</button>

        <button onClick={() => handleClick("7")}>7</button>
        <button onClick={() => handleClick("8")}>8</button>
        <button onClick={() => handleClick("9")}>9</button>
        <button onClick={() => handleClick("*")}>×</button>

        <button onClick={() => handleClick("4")}>4</button>
        <button onClick={() => handleClick("5")}>5</button>
        <button onClick={() => handleClick("6")}>6</button>
        <button onClick={() => handleClick("-")}>−</button>

        <button onClick={() => handleClick("1")}>1</button>
        <button onClick={() => handleClick("2")}>2</button>
        <button onClick={() => handleClick("3")}>3</button>
        <button onClick={() => handleClick("+")}>+</button>

        <button onClick={() => handleClick("0")} className="span-two">0</button>
        <button onClick={() => handleClick(".")}>.</button>
        <button onClick={calculateResult}>=</button>
      </div>
    </div>
  );
};

export default Calculator;
```
# App.css
```
{
  box-sizing: border-box;
  font-family: sans-serif;
}

body {
  margin: 0;
  background: rgb(254, 143, 143);
  display: flex;
  justify-content: center;
  align-items: center;
  height: 100vh;
}

.app {
  text-align: center;
  color: #fbf9f9;
}

h1 {
  margin-bottom: 20px;
}

.calculator {
  width: 320px;
  background: #fff;
  padding: 20px;
  border-radius: 20px;
  box-shadow: 0 10px 25px rgba(0, 0, 0, 0.2);
}

.display {
  width: 100%;
  height: 60px;
  font-size: 1.5rem;
  text-align: right;
  padding: 10px;
  border: none;
  border-radius: 10px;
  background: #b7b6b6;
  margin-bottom: 20px;
}

.buttons {
  display: grid;
  grid-template-columns: repeat(4, 1fr);
  gap: 10px;
}

button {
  padding: 20px;
  font-size: 1.2rem;
  border: none;
  border-radius: 10px;
  background-color: #323232;
  color: rgb(248, 249, 250);
  cursor: pointer;
  transition: all 0.2s;
}

button:hover {
  background-color: #afd3ee;}

.span-two {
  grid-column: span 2;
}

@media (max-width: 400px) {
  .calculator {
    width: 90%;
  }

  button {
    padding: 15px;
    font-size: 1rem;
  }
}
```


## OUTPUT
<img width="1918" height="1078" alt="image" src="https://github.com/user-attachments/assets/bc95ba81-f46e-44fa-9b03-65e0e1e44649" />
<img width="1918" height="1078" alt="image" src="https://github.com/user-attachments/assets/c81eef2e-5288-4093-ae22-dee73b22f43c" />
<img width="1918" height="1078" alt="image" src="https://github.com/user-attachments/assets/0fefaf85-688a-4802-85e1-4e676afd3d75" />



## RESULT
The program for developing a simple calculator in React.js is executed successfully.
