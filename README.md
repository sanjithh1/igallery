# Ex.07 Design of Interactive Image Gallery
## Date:11/11/2024

## AIM:
To design a web application for an inteactive image gallery with minimum five images.

## DESIGN STEPS:

### Step 1:
Clone the github repository and create Django admin interface.

### Step 2:
Change settings.py file to allow request from all hosts.

### Step 3:
Use CSS for positioning and styling.

### Step 4:
Write JavaScript program for implementing interactivity.

### Step 5:
Validate the HTML and CSS code.

### Step 6:
Publish the website in the given URL.

## PROGRAM :
## index.html
```
<!DOCTYPE html>
<html lang="en">

<head>
  <meta charset="UTF-8">
  <meta name="viewport" content="width=device-width, initial-scale=1.0">
  <title>Interactive Photo Gallery</title>
  <link rel="stylesheet" href="style.css">
</head>

<body>
  <h1>Interactive Photo Gallery</h1>
  <div id="image">Hover over an image below to display here.</div>

  <div class="gallery">
    <img class="preview" alt="Styling with a Bandana" src="https://s3-us-west-2.amazonaws.com/s.cdpn.io/389177/bacon.jpg" onmouseover="upDate(this)" onmouseout="unDo()">
    <img class="preview" alt="With My Boy" src="https://s3-us-west-2.amazonaws.com/s.cdpn.io/389177/bacon2.JPG" onmouseover="upDate(this)" onmouseout="unDo()">
    <img class="preview" src="https://s3-us-west-2.amazonaws.com/s.cdpn.io/389177/bacon3.jpg" alt="Young Puppy" onmouseover="upDate(this)" onmouseout="unDo()">
  </div>

  <script src="script.js"></script>
</body>
</html>
```
## style.css
```
body {
    margin: 2%;
    border: 1px solid black;
    background-color: #b3b3b3;
  }
  #image {
    line-height: 650px;
    width: 575px;
    height: 650px;
    border: 5px solid black;
    margin: 0 auto;
    background-color: #8e68ff;
    background-image: url("");
    background-repeat: no-repeat;
    color: #ffffff;
    text-align: center;
    background-size: 100%;
    margin-bottom: 25px;
    font-size: 150%;
  }
  .preview {
    width: 10%;
    margin-left: 17%;
    border: 10px solid black;
  }
  img {
    width: 95%;
  }
```
## script.js
```
const imageDiv = document.getElementById("image");
const originalImageUrl = ""; // Set this to the URL of your original image
const originalText = "Hover over an image below to display here."; // Original text

function upDate(previewPic) {
  // Change the background image to the source of the hovered image
  imageDiv.style.backgroundImage = `url('${previewPic.src}')`;

  // Update the text to the alt text of the hovered image
  imageDiv.innerHTML = previewPic.alt;
}

function unDo() {
  // Reset the background image to the original URL
  imageDiv.style.backgroundImage = `url('${originalImageUrl}')`; // Use the original image URL here

  // Change the text back to the original text
  imageDiv.innerHTML = originalText;
}
```
## OUTPUT:
![Untitled design](https://github.com/user-attachments/assets/cbcc6e3f-78a9-4e24-99f5-cd538cc3beb3)
 ![image](https://github.com/user-attachments/assets/efa4e088-3cb5-4f92-bb7a-033fa5d475eb)

## RESULT:
The program for designing an interactive image gallery using HTML, CSS and JavaScript is executed successfully.
