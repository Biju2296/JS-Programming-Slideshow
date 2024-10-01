Q2: The implementation for your asynchronous JavaScript slideshow project, including HTML, CSS, and JavaScript files.

1.index.html

<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Movie Slideshow</title>
    <link rel="stylesheet" href="styles.css">
</head>
<body>
    <div class="slideshow-container">
        <img id="slideshow" src="" alt="Movie Slideshow">
    </div>
    <script src="script.js"></script>
</body>
</html>

2.styles.css

body {
    display: flex;
    justify-content: center;
    align-items: center;
    height: 100vh;
    background-color: #000;
}

.slideshow-container {
    width: 80%;
    max-width: 600px;
    position: relative;
}

#slideshow {
    width: 100%;
    border-radius: 10px;
    box-shadow: 0 4px 20px rgba(0, 0, 0, 0.5);
}

3.script.js

const images = [
    "https://via.placeholder.com/600x400?text=Movie+1",
    "https://via.placeholder.com/600x400?text=Movie+2",
    "https://via.placeholder.com/600x400?text=Movie+3",
    "https://via.placeholder.com/600x400?text=Movie+4",
    "https://via.placeholder.com/600x400?text=Movie+5"
];

let currentIndex = 0;
const slideshow = document.getElementById("slideshow");

// Set the first image as the default image
slideshow.src = images[currentIndex];

// Function to change the image
function changeImage() {
    currentIndex = (currentIndex + 1) % images.length; // Loop back to the first image
    slideshow.src = images[currentIndex];
}

// Set an interval for the slideshow
setInterval(changeImage, 2000);
