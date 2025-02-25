<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Image Carousel</title>
    <style>
        * { margin: 0; padding: 0; box-sizing: border-box; }
        body { 
            display: flex; 
            justify-content: center; 
            align-items: center; 
            height: 100vh; 
            background: url('https://i.pinimg.com/474x/5d/10/28/5d10286a60b3b79c34928fde1aa83eee.jpg') no-repeat center center/cover;
            position: relative;
        }
        body::before {
            content: "";
            position: absolute;
            top: 0;
            left: 0;
            width: 100%;
            height: 100%;
            background: rgba(0, 0, 0, 0.5);
            backdrop-filter: blur(10px);
            z-index: -1;
        }
        .carousel { position: relative; width: 80%; display: flex; justify-content: center; align-items: center; }
        .carousel-container { display: flex; gap: 15px; justify-content: center; align-items: center; }
        .slide { width: 35%; position: relative; text-align: center; transition: transform 0.5s ease-in-out; cursor: pointer; perspective: 1000px; }
        .slide img { width: 100%; border-radius: 15px; transition: transform 0.3s ease-in-out; transform: rotateY(20deg) scale(1); }
        .slide:nth-child(2) img { transform: rotateY(0) scale(1.1); }
        .slide:nth-child(3) img { transform: rotateY(-20deg) scale(1); }
        .slide:hover img { transform: rotateY(0) scale(1.2); z-index: 2; }
        .caption { position: absolute; bottom: 20px; left: 50%; transform: translateX(-50%); color: white; font-size: 24px; font-weight: bold; background: rgba(0, 0, 0, 0.5); padding: 10px 20px; border-radius: 5px; transition: opacity 0.5s ease-in-out; }
    </style>
</head>
<body>
    <div class="carousel">
        <div class="carousel-container">
            <div class="slide" onclick="displayImage(this)"><img src="https://i.pinimg.com/474x/ce/79/e3/ce79e354617b85b364c34922a9c0dae3.jpg" alt="cycle"><div class="caption">Life</div></div>
            <div class="slide" onclick="displayImage(this)"><img src="https://i.pinimg.com/474x/cc/4c/1c/cc4c1c51c1d17752384d180678c83593.jpg" alt="girl"><div class="caption">Cafe</div></div>
            <div class="slide" onclick="displayImage(this)"><img src="https://i.pinimg.com/474x/52/d5/e1/52d5e168e93923b522bff0d0a4515c71.jpg" alt="shop"><div class="caption">Explore</div></div>
        </div>
    </div>
    <script>
        function displayImage(element) {
            const imgSrc = element.querySelector('img').src;
            const newWindow = window.open("", "_blank");
            newWindow.document.write('<html><head><title>Image View</title></head><body style="display:flex; justify-content:center; align-items:center; height:100vh; background:black;">');
            newWindow.document.write('<img src="' + imgSrc + '" style="max-width:90%; max-height:90%; border-radius:10px;">');
            newWindow.document.write('</body></html>');
        }
    </script>
</body>
</html>
