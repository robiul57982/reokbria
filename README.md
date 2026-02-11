# reokbria
Our Love
<!DOCTYPE html>
<html>
<head>
    <title>❤️ Our Love Story ❤️</title>
    <style>
        body {
            margin: 0;
            font-family: Arial, sans-serif;
            background: linear-gradient(to right, #ff9a9e, #fad0c4);
            text-align: center;
            color: white;
        }

        #login {
            position: fixed;
            width: 100%;
            height: 100%;
            background: #000000dd;
            display: flex;
            justify-content: center;
            align-items: center;
            flex-direction: column;
        }

        input {
            padding: 10px;
            border-radius: 5px;
            border: none;
        }

        button {
            padding: 10px 20px;
            margin-top: 10px;
            border: none;
            border-radius: 5px;
            cursor: pointer;
        }

        .gallery {
            width: 80%;
            margin: 20px auto;
            position: relative;
        }

        .gallery img {
            width: 100%;
            height: 400px;
            object-fit: cover;
            border-radius: 15px;
        }

        .date {
            margin-top: 10px;
            font-size: 18px;
        }

        .counter {
            font-size: 22px;
            margin-top: 20px;
        }
    </style>
</head>

<body>

<div id="login">
    <h2>Enter Password 💕</h2>
    <input type="password" id="password" placeholder="Enter Password">
    <button onclick="checkPassword()">Enter</button>
</div>

<h1>❤️ Our Beautiful Memories ❤️</h1>

<div class="counter" id="loveCounter"></div>

<div class="gallery">
    <img id="slideImage" src="photo1.jpg">
    <div class="date" id="photoDate"></div>
</div>

<audio autoplay loop>
    <source src="music.mp3" type="audio/mpeg">
</audio>

<script>

    // 🔒 Password System
    function checkPassword() {
        var pass = document.getElementById("password").value;
        if(pass === "love123") {
            document.getElementById("login").style.display = "none";
        } else {
            alert("Wrong Password 💔");
        }
    }

    // ❤️ Love Counter (Start Date Change Here)
    var startDate = new Date("2024-01-01");
    var today = new Date();
    var diffTime = today - startDate;
    var diffDays = Math.floor(diffTime / (1000 * 60 * 60 * 24));
    document.getElementById("loveCounter").innerHTML = 
        "💕 We have been together for " + diffDays + " days 💕";

    // 🖼 Slideshow Gallery
    var images = [
        {src: "photo1.jpg", date: "14 February 2025"},
        {src: "photo2.jpg", date: "20 March 2025"},
        {src: "photo3.jpg", date: "10 April 2025"}
    ];

    var current = 0;

    function changeSlide() {
        document.getElementById("slideImage").src = images[current].src;
        document.getElementById("photoDate").innerHTML = "📅 " + images[current].date;
        current++;
        if(current >= images.length) {
            current = 0;
        }
    }

    setInterval(changeSlide, 3000);
    changeSlide();

</script>

</body>
</html>
