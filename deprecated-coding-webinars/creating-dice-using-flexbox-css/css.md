```css
body {
  display: flex;
  align-items: center;
  justify-content: center;
  vertical-align: center;
  flex-wrap: wrap;
  align-content: center;
}

/* code starts here */
.dice {
  padding: 4px;
  background-color: #2c3433;
  width: 104px;
  height: 104px;
  border-radius: 10%;
  margin-right: 10px;
}
#first-face {
  display: flex;
  justify-content: center;
  align-items: center;
}

.dot {
  display: block;
  width: 24px;
  height: 24px;
  border-radius: 50%;
  background-color: #daedeb;
}

#second-face {
  display: flex;
  justify-content: space-between;
}

#second-face .dot:nth-of-type(2) {
  align-self: flex-end;
}

#third-face {
  display: flex;
  justify-content: space-between;
}

#third-face .dot:nth-of-type(1) {
  align-self: flex-end;
}

#third-face .dot:nth-of-type(2) {
  align-self: center;
}

#fourth-face,
#sixth-face,
#fifth-face {
  display: flex;
  justify-content: space-between;
}

#fourth-face .column,
#sixth-face .column,
#fifth-face .column {
  display: flex;
  flex-direction: column;
  justify-content: space-between;
}

#fifth-face .column:nth-of-type(2) {
  justify-content: center;
}
```