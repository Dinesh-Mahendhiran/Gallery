# Ex.08 Design of Interactive Image Gallery
# Date:13.12.2025
# AIM:
To design a web application for an inteactive image gallery with minimum five images.

# DESIGN STEPS:
## Step 1:
Clone the github repository and create Django admin interface.

## Step 2:
Change settings.py file to allow request from all hosts.

## Step 3:
Use CSS for positioning and styling.

## Step 4:
Write JavaScript program for implementing interactivity.

## Step 5:
Validate the HTML and CSS code.

## Step 6:
Publish the website in the given URL.

# PROGRAM :
{% load static %}
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Image Gallery</title>
<style>
            body{
                background-image: linear-gradient(90deg,red,orange,yellow,orange,red);
            }
            h1{
                text-align: center;
                text-transform: uppercase;
            }
        	.gallery-container {
            position: relative;
            max-width: 600px;
            margin-top: 100px ;
            margin-left: 530px;
            background-image: linear-gradient(90deg,green,yellow,green);
            padding: 10px;
            border-radius: 10px;
            box-shadow: 0 0 10px rgba(0, 0, 0, 0.2);
        	}
        	.gallery-image {
            width: 100%;
            height: 400px;
            object-fit: cover;
            border-radius: 10px;
        	}
        	.caption {
            margin-top: 10px;
            font-size: 2.5em;
            font-family: Cambria, Cochin, Georgia, Times, 'Times New Roman', serif;
            text-align: center;
        	}
        	.gallery-buttons {
            display: flex;
            justify-content: space-between;
            margin-top: 15px;
        	}
        	button {
            padding: 10px 20px;
            cursor: pointer;
            border: none;
            border-radius: 5px;
            background-color: #ff16d0ff;
            color: white;
            transition: 0.3s;
        	}
</style>
</head>
<body>
    <h1><u>7 Wonders of the world</u></h1>
    	<div class="gallery-container">
        		<img id="galleryImage" class="gallery-image" src="image1.jpg">
        		<div id="caption" class="caption">Caption for Image 1</div>
        		<div class="gallery-buttons">
            		<button onclick="prevImage()">Previous</button>
            		<button onclick="nextImage()">Next</button>
        		</div>
    	</div>

    	<script>
        		const images = [
{ src: "{% static "greatwall.png" %}", caption: "Great Wall of China" },
{ src: "{% static "petra.png" %}", caption: "Petra" },
{ src: "{% static "Colosseum.png" %}", caption: "Colosseum" },
{ src: "{% static "chichenitza.png" %}", caption: "Chichen Itza" },
{ src: "{% static "taj.png" %}", caption: "Taj Mahal" },
{ src: "{% static "machu.png" %}", caption: "Machu Picchu" },
{ src: "{% static "christ.png" %}", caption: "Christ the Redeemer" },
];
let currentIndex = 0;
        
function updateGallery( ) 
{
document.getElementById("galleryImage").src = images[currentIndex].src;
document.getElementById("caption").textContent = images[currentIndex].caption;
}

function nextImage( ) 
{
currentIndex = (currentIndex + 1) % images.length;
updateGallery( );
}

function prevImage( ) 
{
currentIndex = (currentIndex - 1 + images.length) % images.length;
updateGallery( );
}

</script>
</body>
</html>
# OUTPUT:
<img width="1035" height="662" alt="image" src="https://github.com/user-attachments/assets/01f2e4ac-4ffe-4d00-bca8-fc8267daf2fa" />
<img width="1034" height="580" alt="image" src="https://github.com/user-attachments/assets/7a302848-488d-40e6-82b5-63585f53c0a1" />
<img width="1031" height="595" alt="image" src="https://github.com/user-attachments/assets/b7e3acb2-658e-4d2f-874d-105c0d971466" />
<img width="1038" height="584" alt="image" src="https://github.com/user-attachments/assets/766f4a43-1a2b-49f9-836b-bf1c983bdee8" />
<img width="1038" height="588" alt="image" src="https://github.com/user-attachments/assets/62611cf8-1aa5-408a-b71b-2b6120316284" />
<img width="1039" height="583" alt="image" src="https://github.com/user-attachments/assets/7c58a28d-a80b-4281-abb9-1a1e8ced40c9" />
<img width="1034" height="595" alt="image" src="https://github.com/user-attachments/assets/1bcbea74-71d4-44f8-a101-acc8619e3aae" />

# RESULT:
The program for designing an interactive image gallery using HTML, CSS and JavaScript is executed successfully.
