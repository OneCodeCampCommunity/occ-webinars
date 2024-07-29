```html
<head>
  <link
    rel="stylesheet"
    href="https://fonts.googleapis.com/css2?family=Material+Symbols+Outlined:opsz,wght,FILL,GRAD@20..48,100..700,0..1,-50..200"
  />
</head>

<body>
  <div>
    <h1>Interactive Photo Gallery</h1>
  </div>
  <div class="full-img" id="fullImgBox" style="display: none;">
    <img src="images/img1.jpg" id="fullImg" />
    <span onclick="closeFullImg()">
      <span class="material-symbols-outlined"> cancel </span></span
    >
    <button class="prev" onclick="showPrevImage()">
      <span class="material-symbols-outlined"> arrow_back_ios </span>
    </button>
    <button class="next" onclick="showNextImage()">
      <span class="material-symbols-outlined"> arrow_forward_ios </span>
    </button>
  </div>

  <div class="img-gallery">
    <img
      src="https://wallpaper.dog/large/993161.jpg"
      onclick="openFullImg(this.src)"
    />
    <img
      src="https://i.pinimg.com/originals/d6/8c/9e/d68c9e12c06108e3a1c3c4ec87c8a134.jpg"
      onclick="openFullImg(this.src)"
    />
    <img
      src="https://rare-gallery.com/uploads/posts/817236-Christmas-Holidays-Winter-Parks-Bench-Snow-Trees.jpg"
    />
    <img
      src="https://www.pixelstalk.net/wp-content/uploads/images6/Aesthetic-Christmas-Wallpaper-HD-1080p.jpg"
      onclick="openFullImg(this.src)"
    />
    <img
      src="https://wallpaperaccess.com/full/1545006.jpg"
      onclick="openFullImg(this.src)"
    />
    <img
      src="https://m.media-amazon.com/images/I/91+5PASgjfL.jpg"
      onclick="openFullImg(this.src)"
    />
    <img
      src="https://c4.wallpaperflare.com/wallpaper/921/411/688/snow-lollipops-tree-garland-wallpaper-preview.jpg"
      onclick="openFullImg(this.src)"
    />
    <img
      src="https://c4.wallpaperflare.com/wallpaper/200/502/345/winter-snow-decoration-balls-wallpaper-preview.jpg"
      onclick="openFullImg(this.src)"
    />
  </div>
</body>
```
