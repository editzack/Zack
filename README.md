# Zack
Website 
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8" />
    <meta name="viewport" content="width=device-width, initial-scale=1.0" />
    <title>My Cinematic Website</title>
    <style>
        * {
            margin: 0;
            padding: 0;
            box-sizing: border-box;
            font-family: Arial, sans-serif;
        }

        body, html {
            height: 100%;
            overflow: hidden;
        }

        /* Background Video */
        .bg-video {
            position: fixed;
            top: 0;
            left: 0;
            width: 100%;
            height: 100%;
            object-fit: cover;
            z-index: -1;
            filter: brightness(60%);
        }

        /* Main Content */
        .content {
            position: absolute;
            top: 50%;
            left: 50%;
            transform: translate(-50%, -50%);
            text-align: center;
            color: white;
            animation: fadeIn 2s ease-in-out;
        }

        h1 {
            font-size: 3rem;
            font-weight: bold;
            text-transform: uppercase;
            letter-spacing: 3px;
        }

        p {
            margin-top: 15px;
            font-size: 1.2rem;
        }

        /* Button */
        button {
            margin-top: 20px;
            padding: 12px 25px;
            font-size: 1.1rem;
            border: none;
            border-radius: 5px;
            background: #ff0055;
            color: white;
            cursor: pointer;
            transition: 0.3s ease;
        }

        button:hover {
            background: #ff336e;
            transform: scale(1.05);
        }

        /* Fade In Animation */
        @keyframes fadeIn {
            from { opacity: 0; transform: translate(-50%, -60%); }
            to { opacity: 1; transform: translate(-50%, -50%); }
        }
    </style>
</head>
<body>
    <!-- Background Video -->
    <video autoplay loop muted playsinline class="bg-video">
        <source src="background.mp4" type="video/mp4" />
    </video>

    <!-- Background Music -->
    <audio id="bg-music" src="music.mp3" autoplay loop></audio>

    <div class="content">
        <h1>Welcome to My Website</h1>
        <p>Cinematic • Stylish • Animated</p>
        <button onclick="toggleMusic()">Toggle Music</button>
    </div>

    <script>
        const music = document.getElementById("bg-music");

        function toggleMusic() {
            if (music.paused) {
                music.play();
            } else {
                music.pause();
            }
        }
    </script>
</body>
</html>
