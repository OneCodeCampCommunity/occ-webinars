```css
* {
  margin: 0 auto;
  padding: 0 auto;
  font-family: Arial;
}

body {
  background-color: #097102;
}

#inner-box {
  border: 3px solid black;
  border-radius: 10px;
  width: 850px;
  height: 450px;
  position: relative;
  top: 15px;
  background-color: white;
}

#header {
  position: relative;
  top: 10px;
  text-align: center;
  font-size: 45px;
}

button {
  border: 2px solid black;
  border-radius: 6px;
  background-color: white;
}

button:hover {
  cursor: pointer;
  border-color: black;
  color: white;
  background-color: black;
}

#measurement {
  position: relative;
  top: 15px;
  left: 10px;
  height: 40px;
}

#measurement-label {
  position: relative;
  top: 6px;
  font-size: 28px;
}

#measurement-button {
  height: 38px;
  position: relative;
  top: 1px;
  width: 85px;
  font-size: 18px;
}

input {
  border: 2px solid black;
  background-color: white;
  color: black;
  position: relative;
  top: 1px;
  height: 33px;
  width: 65px;
  font-size: 16px;
}

#measurement-input {
  position: relative;
  top: 40px;
}

#height,
#weight {
  position: relative;
  height: 35px;
  left: 10px;
}

.label {
  position: relative;
  top: 4px;
  height: 27px;
}

#height-feet,
#height-inch {
  width: 45px;
}

#calculate {
  position: relative;
  top: 60px;
  left: 10px;
  height: 40px;
}

#calculate-button {
  position: relative;
  top: 1px;
  height: 38px;
  width: 105px;
  font-size: 18px;
}

#result {
  position: relative;
  top: 120px;
}

#result-text {
  text-align: center;
}
```