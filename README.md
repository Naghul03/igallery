# Ex.08 Design of Interactive Image Gallery
## Date:

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
```
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Interactive Image Gallery</title>
    <style>
        body {
            font-family: Arial, sans-serif;
            margin: 0;
            padding: 0;
            background-color: rgb(76, 71, 144);
        }

        .gallery {
            display: grid;
            grid-template-columns: repeat(auto-fit, minmax(150px, 1fr));
            gap: 10px;
            padding: 20px;
        }

        .gallery img {
            width: 100%;
            height: auto;
            border-radius: 10px;
            cursor: pointer;
            transition: transform 0.3s ease, box-shadow 0.3s ease;
        }

        .gallery img:hover {
            transform: scale(1.1);
            box-shadow: 0 4px 15px rgba(0, 0, 0, 0.2);
        }

        .modal {
            display: none;
            position: fixed;
            top: 0;
            left: 0;
            width: 100%;
            height: 100%;
            background: rgba(0, 0, 0, 0.8);
            justify-content: center;
            align-items: center;
            z-index: 1000;
        }

        .modal img {
            max-width: 90%;
            max-height: 90%;
            border-radius: 10px;
        }

        .modal-close {
            position: absolute;
            top: 20px;
            right: 30px;
            font-size: 2rem;
            color: white;
            cursor: pointer;
        }
        footer {
            text-align: center;
            font-size: 16px;
            margin-top: 40px; 
            color: burlywood;
        }
        header {
            background-color: rgba(0, 0, 0, 0.6); 
            color: white;
            text-align: center;
            padding: 20px;
            font-size: 1rem;
            font-family: 'Segoe UI', Tahoma, Geneva, Verdana, sans-serif;
            letter-spacing: 2px;
            box-shadow: 0 2px 10px rgba(0,0,0,0.5);
        }


    </style>
</head>
<body>
<header>
    <h1>Anime Image Gallery</h1>
</header>
<div class="gallery">
    <img src="1.png" alt="Image 1">
    <img src="2.png" alt="Image 2">
    <img src="3.png" alt="Image 3">
    <img src="4.png" alt="Image 4">
    <img src="5.png" alt="Image 5">
    <img src="6.png" alt="Image 6">
    <img src="7.png" alt="Image 7">
    <img src="8.png" alt="Image 8">

</div>

<div class="modal" id="modal">
    <span class="modal-close" id="modalClose">&times;</span>
    <img id="modalImage" src="" alt="Expanded Image">
</div>
<footer >
    Designed and developed by N Naghul varshan &copy; 2025
</footer>


<script>
    const gallery = document.querySelector('.gallery');
    const modal = document.getElementById('modal');
    const modalImage = document.getElementById('modalImage');
    const modalClose = document.getElementById('modalClose');

    gallery.addEventListener('click', (e) => {
        if (e.target.tagName === 'IMG') {
            modalImage.src = e.target.src;
            modal.style.display = 'flex';
        }
    });

    modalClose.addEventListener('click', () => {
        modal.style.display = 'none';
    });

    modal.addEventListener('click', (e) => {
        if (e.target === modal) {
            modal.style.display = 'none';
        }
    });

</script>

</body>
</html>
```
## OUTPUT:
![image](https://github.com/user-attachments/assets/b84e52e5-acd4-42b0-bd85-6d206d05ee1e)
![image](https://github.com/user-attachments/assets/df597b06-1c1f-4eea-84b1-7a6c9c981cd9)
![image](https://github.com/user-attachments/assets/6c18b790-a777-4be0-b46c-56d2ce7eaae3)



## RESULT:
The program for designing an interactive image gallery using HTML, CSS and JavaScript is executed successfully.
