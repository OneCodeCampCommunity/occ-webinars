```css
#word-container {
  display: flex;
  flex-wrap: wrap;
  background-color: azure;
  margin: auto;
  border-radius: 20px;
  padding: 10px;
  margin: 0 60px;
}

.word-box {
  display: flex;
  flex-wrap: wrap;
  margin: 10px;
}

.letter-box {
  width: 60px;
  height: 60px;
  display: flex;
  align-items: center;
  justify-content: center;
  border: 2px solid #8d8d8d;
  margin: 2px;
  background-color: azure;
  border-radius: 10px;
  font-weight: bolder;
  font-size: larger;
  box-shadow: 10px 10px 5px 0px rgba(0, 0, 0, 0.4);
  -webkit-box-shadow: 10px 10px 5px 0px rgba(0, 0, 0, 0.4);
  -moz-box-shadow: 10px 10px 5px 0px rgba(0, 0, 0, 0.4);
}

#game-container {
  background-color: azure;
  margin: 60px;
  padding: 20px;
  border-radius: 10px;
  display: flex;
  justify-content: center;
}

#word-to-guess {
  display: flex;
  justify-content: center;
  margin: 25px;
}

body {
  background: rgb(255, 255, 255);
  background: linear-gradient(
    90deg,
    rgba(255, 255, 255, 1) 0%,
    rgba(38, 95, 192, 1) 0%,
    rgba(0, 212, 255, 1) 100%
  );
  font-family: Arial, Helvetica, sans-serif;
  padding: 0;
  margin: 0;
}

h2 {
  color: white;
}

h1 {
  font-weight: bolder;
  color: #265fc0;
}

input {
  height: 60px;
  width: 600px;
  border-radius: 15px;
  font-size: 50px;
}

button {
  height: 50px;
  width: 200px;
  font-size: xx-large;
  cursor: pointer;
  border-radius: 10px;
  background-color: #5a2e9a;
  color: azure;
}

p {
  color: #265fc0;
  font-size: 50px;
  font-weight: 200;
  font-weight: bolder;
}

span {
  color: azure;
}
```
