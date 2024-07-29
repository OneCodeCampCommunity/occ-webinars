```javascript
const measurementButton = document.getElementById("measurement-button");
const height = document.getElementById("height");
const weight = document.getElementById("weight");
const calculateButton = document.getElementById("calculate-button");
const result = document.getElementById("result");
let inputCm, inputFt, inputIn;
let inputKg, inputLb;

const cmkg = "CM/KG";
const inlb = "IN/LB";

let heightValue, weightValue;

measurementButton.addEventListener("click", toggleMeasurement);

function toggleMeasurement(e) {
  if (e.target.textContent == cmkg) {
    e.target.textContent = inlb;
  } else {
    e.target.textContent = cmkg;
  }
  displayInput();
}

window.addEventListener("load", displayInput);

function displayInput() {
  if (measurementButton.textContent == cmkg) {
    height.innerHTML = `
            <span class="label">Height (in centimeters): </span>
            <input class="height-input" id="height-cm" type="number" required>
        `;
    weight.innerHTML = `
            <span class="label">Weight (in kilograms): </span>
            <input class="weight-input" id="weight-kg" type="number" required>
        `;
    inputCm = document.getElementById("height-cm");
    inputKg = document.getElementById("weight-kg");
  } else {
    height.innerHTML = `
            <span class="label">Height (in feet and inches): </span>
            <input class="height-input" id="height-ft" type="number" required>
            <input class="height-input" id="height-in" type="number" required>
        `;
    weight.innerHTML = `
            <span class="label">Weight (in pounds): </span>
            <input class="weight-input" id="weight-lb" type="number" required>
        `;
    inputFt = document.getElementById("height-ft");
    inputIn = document.getElementById("height-in");
    inputLb = document.getElementById("weight-lb");
  }
}
calculateButton.addEventListener("click", calculate);

function calculate() {
  let bmi;
  if (measurementButton.textContent == cmkg) {
    if (inputCm.value == "" || inputKg.value == "") {
      alert("Please enter a value in the height and weight field.");
      return;
    } else {
      // convert height into meters
      heightValue = parseInt(inputCm.value) / 100;
      weightValue = parseInt(inputKg.value);
    }
  } else {
    if (inputFt.value == "" || inputIn.value == "" || inputLb.value == "") {
      alert("Please enter a value in the height and weight field.");
      return;
    } else {
      // convert height into meters
      heightValue =
        (parseInt(inputFt.value) * 12 + parseInt(inputIn.value)) * 0.0254;
      // convert weight into kilograms
      weightValue = parseInt(inputLb.value) / 2.2;
    }
  }

  bmi = weightValue / (heightValue * heightValue);
  classifyBMI(bmi);
}

function classifyBMI(bmi) {
  let bmiClass;

  if (bmi < 18.5) bmiClass = "Underweight";
  else if (bmi < 25) bmiClass = "Normal";
  else if (bmi < 30) bmiClass = "Overweight";
  else bmiClass = "Obese";

  result.innerHTML = `<h1 id="result-text">Your BMI Is: ${bmi.toFixed(
    1
  )} (${bmiClass}).</h1>`;
}
```
