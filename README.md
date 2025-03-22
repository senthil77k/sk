#TITLE: Web Activity 1

#Aim:

Design and implement an interactive image gallery using JavaScript, HTML, and CSS. The gallery should meet the following requirements.

#Algorithm:

Display multiple images in a horizontal scrollable layout.
Each image must have a caption that appears when hovered over.
Include Next and Previous buttons to navigate through the images.
Use JavaScript to enhance interactivity (e.g., smooth sliding animations, hover effects).
Style the gallery using CSS for a visually appealing and responsive design.
Include a footer at the bottom of the page with the text "Learner's Name and Register Number".
Your solution should include well-structured HTML, CSS, and JavaScript code, ensuring smooth user experience and navigation.

#Program:
1.Html
```
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Interactive Image Gallery</title>
    <link rel="stylesheet" href="styles1.css">
</head>
<body>
    <div class="gallery-container">
        <div class="gallery-wrapper">
            <div class="gallery-images">
                <div class="gallery-item">
                    <img src="c:\Users\admin\Documents\web dev\html 2\image1.jpg" alt="Sea Image 1">
                    <div class="caption">burn like a fire</div>
                </div>
                <div class="gallery-item">
                    <img src="c:\Users\admin\Documents\web dev\html 2\image2.jpg" alt="Sea Image 2">
                    <div class="caption">cold as ice</div>
                </div>
                <div class="gallery-item">
                    <img src="c:\Users\admin\Documents\web dev\html 2\image3.jpg" alt="Sea Image 3">
                    <div class="caption">wind</div>
                </div>
                <div class="gallery-item">
                    <img src="c:\Users\admin\Documents\web dev\html 2\images4.jpg" alt="Sea Image 3">
                    <div class="caption">Underwater World</div>
                </div>
                <div class="gallery-item">
                    <img src="c:\Users\admin\Documents\web dev\html 2\images5.jpg" alt="Sea Image 3">
                    <div class="caption">desert</div>
                </div>
            </div>
        </div>
        <button class="prev-btn" onclick="prevImage()">&#10094;</button>
        <button class="next-btn" onclick="nextImage()">&#10095;</button>
    </div>

    <footer>
        <p>Senthil kumaran.c 212223220103</p>
    </footer>

    <script src="script.js"></script>
</body>
</html>

```
2.Css

```

* {
    margin: 0;
    padding: 0;
    box-sizing: border-box;
}

body {
    font-family: Arial, sans-serif;
    background-color: #f0f8ff;
    display: flex;
    justify-content: center;
    align-items: center;
    min-height: 100vh;
    flex-direction: column;
}


.gallery-container {
    position: relative;
    width: 80%;
    overflow: hidden;
    margin-bottom: 20px;
}

.gallery-wrapper {
    display: flex;
    transition: transform 0.3s ease;
}

.gallery-images {
    display: flex;
}

.gallery-item {
    position: relative;
    margin: 0 10px;
    display: inline-block;
}

.gallery-item img {
    width: 300px;
    height: 200px;
    object-fit: cover;
    border-radius: 10px;
    box-shadow: 0 4px 6px rgba(0, 0, 0, 0.1);
}

.caption {
    position: absolute;
    bottom: 0;
    left: 0;
    right: 0;
    padding: 10px;
    text-align: center;
    background-color: rgba(0, 0, 0, 0.6);
    color: white;
    font-size: 16px;
    opacity: 0;
    transition: opacity 0.3s;
}

.gallery-item:hover .caption {
    opacity: 1;
}

.prev-btn, .next-btn {
    position: absolute;
    top: 50%;
    transform: translateY(-50%);
    background-color: rgba(0, 0, 0, 0.5);
    color: white;
    border: none;
    padding: 15px;
    font-size: 18px;
    cursor: pointer;
    border-radius: 50%;
    z-index: 2;
}

.prev-btn {
    left: 10px;
}

.next-btn {
    right: 10px;
}

.prev-btn:hover, .next-btn:hover {
    background-color: rgba(0, 0, 0, 0.7);
}


footer {
    text-align: center;
    border: 100px;
    padding: 10px;
    background-color: #003366;
    color: white;
    width: 100%;
}

```
3.js
```
let currentIndex = 0;

function showImage(index) {
    const galleryWrapper = document.querySelector('.gallery-wrapper');
    const totalImages = document.querySelectorAll('.gallery-item').length;

    if (index < 0) {
        currentIndex = totalImages - 1;
    } else if (index >= totalImages) {
        currentIndex = 0;
    } else {
        currentIndex = index;
    }

    galleryWrapper.style.transform = `translateX(-${currentIndex * 320}px)`; // 320px includes margin and image width
}

function nextImage() {
    showImage(currentIndex + 1);
}

function prevImage() {
    showImage(currentIndex - 1);
}
showImage(currentIndex);

```
#Output:
![image](https://github.com/user-attachments/assets/8c8cfa64-4f8b-456c-a640-6ba23a89f945)
![image](https://github.com/user-attachments/assets/8f833f8a-010b-4069-9f84-1f438537c2bf)
![image](https://github.com/user-attachments/assets/5c8b0e8c-f940-4d2f-aa0d-a4c5305a7577)
![image](https://github.com/user-attachments/assets/e26f4169-bd7a-4d9b-a14f-c1def66b7c22)





#Result:
Activity done sucessfully


