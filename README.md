# Valentine-
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <title>Isha ❤️ Chaitanya</title>
    <meta name="viewport" content="width=device-width, initial-scale=1.0">

    <style>
        body {
            margin: 0;
            height: 100vh;
            background: linear-gradient(135deg, #ff9a9e, #fad0c4);
            display: flex;
            justify-content: center;
            align-items: center;
            font-family: 'Poppins', sans-serif;
            overflow: hidden;
        }

        .container {
            background: white;
            padding: 40px 30px;
            border-radius: 22px;
            text-align: center;
            box-shadow: 0 15px 40px rgba(0,0,0,0.2);
            width: 90%;
            max-width: 420px;
            position: relative;
            z-index: 2;
        }

        h1 {
            color: #ff4b6e;
            font-size: 28px;
            margin-bottom: 10px;
        }

        h2 {
            color: #ff6f91;
            font-size: 20px;
            margin-bottom: 15px;
        }

        p {
            color: #555;
            font-size: 16px;
            margin-bottom: 25px;
        }

        .buttons {
            position: relative;
            height: 60px;
        }

        button {
            padding: 12px 25px;
            border: none;
            border-radius: 30px;
            font-size: 16px;
            cursor: pointer;
            transition: 0.3s;
        }

        #yes {
            background: #ff4b6e;
            color: white;
        }

        #yes:hover {
            transform: scale(1.1);
        }

        #no {
            background: #eee;
            color: #333;
            position: absolute;
            right: 0;
        }

        .love {
            display: none;
            margin-top: 25px;
            font-size: 18px;
            color: #ff4b6e;
            font-weight: 600;
        }

        .signature {
            display: none;
            margin-top: 20px;
            font-size: 20px;
            color: #ff4b6e;
            font-weight: bold;
        }

        .heart {
            position: absolute;
            font-size: 22px;
            animation: float 4s infinite;
        }

        @keyframes float {
            0% { transform: translateY(0); opacity: 1; }
            100% { transform: translateY(-100vh); opacity: 0; }
        }
    </style>
</head>

<body>

<!-- Romantic background music -->
<audio autoplay loop>
    <source src="https://www.soundhelix.com/examples/mp3/SoundHelix-Song-1.mp3" type="audio/mp3">
</audio>

<div class="container">
    <h1>Hey Isha 💖</h1>
    <h2>You are my favorite feeling 🥰✨</h2>

    <p>Will you be my Valentine? 🌹❤️</p>

    <div class="buttons">
        <button id="yes" onclick="sayYes()">Yes 💕</button>
        <button id="no">No 🙈</button>
    </div>

    <div class="love" id="loveMessage">
        I love you precious ❤️💘  
        You make my world more beautiful 🌍✨
    </div>

    <div class="signature" id="signature">
        Isha ❤️ Chaitanya
    </div>
</div>

<script>
    const noBtn = document.getElementById("no");

    noBtn.addEventListener("mouseover", moveButton);
    noBtn.addEventListener("click", moveButton);

    function moveButton() {
        const x = Math.random() * (window.innerWidth - 120);
        const y = Math.random() * (window.innerHeight - 120);
        noBtn.style.left = x + "px";
        noBtn.style.top = y + "px";
    }

    function sayYes() {
        document.getElementById("loveMessage").style.display = "block";
        document.getElementById("signature").style.display = "block";
        createHearts();
    }

    function createHearts() {
        const emojis = ["❤️","💖","💕","💘","💞","🌹","✨"];
        for (let i = 0; i < 30; i++) {
            const heart = document.createElement("div");
            heart.classList.add("heart");
            heart.innerHTML = emojis[Math.floor(Math.random() * emojis.length)];
            heart.style.left = Math.random() * window.innerWidth + "px";
            heart.style.bottom = "0px";
            heart.style.animationDuration = (Math.random() * 3 + 2) + "s";
            document.body.appendChild(heart);

            setTimeout(() => heart.remove(), 5000);
        }
    }
</script>

</body>
</html>
