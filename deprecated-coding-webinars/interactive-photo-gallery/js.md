```javascript
var fullImgBox = document.getElementById("fullImgBox");
var currentImageIndex = 0;

var images = [
  "https://wallpaper.dog/large/993161.jpg",
  "https://i.pinimg.com/originals/d6/8c/9e/d68c9e12c06108e3a1c3c4ec87c8a134.jpg",
  "https://rare-gallery.com/uploads/posts/817236-Christmas-Holidays-Winter-Parks-Bench-Snow-Trees.jpg",
  "https://www.pixelstalk.net/wp-content/uploads/images6/Aesthetic-Christmas-Wallpaper-HD-1080p.jpg",
  "https://wallpaperaccess.com/full/1545006.jpg",
  "https://m.media-amazon.com/images/I/91+5PASgjfL.jpg",
  "https://c4.wallpaperflare.com/wallpaper/921/411/688/snow-lollipops-tree-garland-wallpaper-preview.jpg",
  "https://c4.wallpaperflare.com/wallpaper/200/502/345/winter-snow-decoration-balls-wallpaper-preview.jpg"
];

function openFullImg(pic) {
  fullImgBox.style.display = "flex";
  fullImg.src = pic;
  currentImageIndex = images.indexOf(pic);
}

function closeFullImg() {
  fullImgBox.style.display = "none";
}

function showNextImage() {
  currentImageIndex++;
  if (currentImageIndex >= images.length) {
    currentImageIndex = 0;
  }
  showImage(currentImageIndex);
}

function showPrevImage() {
  currentImageIndex--;
  if (currentImageIndex < 0) {
    currentImageIndex = images.length - 1;
  }
  showImage(currentImageIndex);
}

function showImage(index) {
  fullImg.src = images[index];
}
```