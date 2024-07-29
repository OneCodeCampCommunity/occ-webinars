```js
document.addEventListener("DOMContentLoaded", function () {
  var mainBox = document.getElementById("main_box");
  var miniBoxes = document.querySelectorAll(".mini_boxes");

  mainBox.addEventListener("click", function () {
    mainBox.style.background = "lightgray";
    var children = mainBox.children;
    for (var i = 0; i < children.length; i++) {
      children[i].style.border = "none";
    }
  });

  miniBoxes.forEach(function (miniBox) {
    miniBox.addEventListener("click", function (event) {
      event.stopPropagation();
      this.style.border = "2px solid yellow";
      var bg = this.getAttribute("src");
      mainBox.style.backgroundImage = "url(" + bg + ")";

      var siblings = Array.from(this.parentElement.children);
      siblings.forEach(function (sibling) {
        if (sibling !== miniBox) {
          sibling.style.border = "0";
        }
      });
    });
  });
});
```