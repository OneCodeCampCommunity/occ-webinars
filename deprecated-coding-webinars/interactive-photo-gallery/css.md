```css
* {
  margin: 0;
  padding: 0;
  font-family: sans-serif;
}

body {
  background: #ecf4fb;
}

h1 {
  text-align: center;
  margin-top: 50px;
}

.img-gallery {
  width: 80%;
  margin: 50px auto 50px;
  display: grid;
  grid-template-columns: repeat(auto-fit, minmax(200px, 1fr));
  grid-gap: 30px;
}

.img-gallery img {
  width: 100%;
  height: 100%;
  cursor: pointer;
}

.img-gallery img:hover {
  transform: scale(0.8);
  border-radius: 20px;
  box-shadow: 0 42px 75px rgba(26, 29, 43, 0.2);
}

.full-img {
  width: 100%;
  height: 100vh;
  background-color: rgba(0, 0, 0, 0.9);
  position: fixed;
  top: 0;
  left: 0;
  display: flex;
  flex-direction: column;
  align-items: center;
  justify-content: center;
  z-index: 100;
}

.full-img img {
  max-width: 80%;
  max-height: 80%;
}

.full-img span {
  position: absolute;
  top: 5%;
  right: 5%;
  font-size: 30px;
  color: #fff;
  cursor: pointer;
}

.full-img .prev,
.full-img .next {
  position: absolute;
  top: 50%;
  transform: translateY(-50%);
  font-size: 30px;
  color: #fff;
  cursor: pointer;
  background-color: rgba(0, 0, 0, 0.5);
  padding: 10px;
  border: none;
  outline: none;
}

.full-img .prev {
  left: 5%;
}

.full-img .next {
  right: 5%;
}
```