<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Do You Love Me?</title>
    <style>
        @import url('https://fonts.googleapis.com/css2?family=Ghibli&display=swap');
        body, html {
            margin: 0;
            padding: 0;
            width: 100%;
            height: 100vh;
            overflow: hidden;
            display: flex;
            justify-content: center;
            align-items: center;
            font-family: 'Ghibli', sans-serif;
            text-align: center;
            background-color: black;
            color: white;
        }
        .slide-container {
            position: absolute;
            width: 100%;
            height: 100%;
            display: flex;
            justify-content: center;
            align-items: center;
        }
        .slide {
            position: absolute;
            width: 100%;
            height: 100%;
            background-size: cover;
            background-position: center;
            display: none;
        }
        .active {
            display: flex;
            justify-content: center;
            align-items: center;
            text-align: center;
            font-size: 30px;
            font-weight: bold;
        }
        .text-overlay {
            position: absolute;
            top: 10px;
            left: 50%;
            transform: translateX(-50%);
            font-size: 28px;
            color: white;
            text-shadow: 2px 2px 4px rgba(0, 0, 0, 0.7);
        }
        .buttons {
            position: absolute;
            bottom: 20px;
            width: 100%;
            text-align: center;
        }
        button {
            font-size: 20px;
            padding: 12px 24px;
            margin: 10px;
            border: none;
            cursor: pointer;
            border-radius: 20px;
            transition: transform 0.2s ease, background-color 0.3s;
        }
        #next {
            background-color: #28a745;
            color: white;
        }
        #prev {
            background-color: #dc3545;
            color: white;
        }
    </style>
</head>
<body>
    <div class="slide-container">
        <div class="slide active" id="slide1">I HAVE A LITTLE MESSAGE FOR MY BUSY TRAVELING BUTTERFLY 🦋</div>
        <div class="slide" id="slide2" style="background-image: url('https://i.ibb.co/N2pLxkKc/53765747-1a77-47e8-b11e-75b61adb209d.png');">
            <div class="text-overlay">WE (YOU & ME)</div>
        </div>
        <div class="slide" id="slide3" style="background-image: url('https://i.ibb.co/MyHVPFPq/Chat-GPT-Image-Apr-5-2025-07-00-50-PM.png');">
            <div class="text-overlay">MEANT TO BE</div>
        </div>
        <div class="slide" id="slide4" style="background-image: url('https://i.ibb.co/WNFGhLch/enhanced-image.png');">
            <div class="text-overlay">TOGETHER</div>
        </div>
        <div class="slide" id="slide5" style="background-image: url('https://i.ibb.co/PGFCbQFR/7ed6165f-be01-417c-a687-89cad13f9d34.png');">
            <div class="text-overlay">FOREVER</div>
        </div>
        <div class="slide" id="slide6">
            <div style="font-size: 40px; color: white; text-shadow: 2px 2px 4px rgba(0, 0, 0, 0.7);">MY LOVE 💕</div>
        </div>
    </div>
    
    <div class="buttons">
        <button id="prev" onclick="prevSlide()">Previous</button>
        <button id="next" onclick="nextSlide()">Next</button>
    </div>
    
    <script>
        let currentSlide = 1;
        const totalSlides = 6;
        
        function showSlide(index) {
            document.querySelectorAll('.slide').forEach(slide => slide.classList.remove('active'));
            document.getElementById('slide' + index).classList.add('active');
        }

        function nextSlide() {
            currentSlide = currentSlide === totalSlides ? 1 : currentSlide + 1;
            showSlide(currentSlide);
        }

        function prevSlide() {
            currentSlide = currentSlide === 1 ? totalSlides : currentSlide - 1;
            showSlide(currentSlide);
        }
    </script>
</body>
</html>
