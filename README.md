<!DOCTYPE html>
<html lang="id">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>For My Favorite Person</title>
    <style>
        body {
            margin: 0;
            padding: 0;
            font-family: 'Segoe UI', Tahoma, Geneva, Verdana, sans-serif;
            background: linear-gradient(135deg, #fce4ec, #e3f2fd); /* Pink & Blue Soft Mix */
            height: 100vh;
            display: flex;
            justify-content: center;
            align-items: center;
            text-align: center;
            color: #5c6bc0;
            overflow: hidden;
        }

        /* Halaman Depan (Homepage) */
        #homepage {
            display: block;
        }

        /* Halaman Galeri (Hidden by default) */
        #contentPage {
            display: none;
            animation: fadeIn 2s ease-in;
        }

        h1 {
            font-size: 2rem;
            margin-bottom: 20px;
            color: #f06292;
        }

        .btn-container {
            display: flex;
            gap: 20px;
            justify-content: center;
        }

        button {
            padding: 15px 35px;
            font-size: 1.1rem;
            border: none;
            border-radius: 50px;
            cursor: pointer;
            transition: 0.3s;
            font-weight: bold;
        }

        .btn-yes {
            background-color: #f06292;
            color: white;
            box-shadow: 0 4px 15px rgba(240, 98, 146, 0.3);
        }

        .btn-no {
            background-color: #90caf9;
            color: white;
            box-shadow: 0 4px 15px rgba(144, 202, 249, 0.3);
        }

        button:hover {
            transform: scale(1.1);
        }

        /* Style Foto */
        .photo-frame {
            width: 80%;
            max-width: 500px;
            border: 8px solid white;
            border-radius: 15px;
            box-shadow: 0 10px 30px rgba(0,0,0,0.1);
            margin-bottom: 20px;
        }

        .note {
            font-style: italic;
            font-size: 1.2rem;
            color: #64b5f6;
            margin-top: 15px;
        }

        @keyframes fadeIn {
            from { opacity: 0; }
            to { opacity: 1; }
        }
    </style>
</head>
<body>

    <audio id="myAudio" loop>
        <source src="https://www.bensound.com/bensound-music/bensound-love.mp3" type="audio/mpeg">
    </audio>

    <div id="homepage">
        <h1>Mau buka pesan ini? ❤️</h1>
        <div class="btn-container">
            <button class="btn-yes" onclick="openMessage()">Yes</button>
            <button class="btn-no" onclick="alert('Yah, kok No? Pilih Yes dong! ✨')">No</button>
        </div>
    </div>

    <div id="contentPage">
        <img src="https://via.placeholder.com/600x400/f8bbd0/ffffff?text=Foto+Horizontal+Kamu" alt="Our Memories" class="photo-frame">
        <p class="note">"Terima kasih sudah selalu ada di setiap warnanya hariku. I love you!"</p>
    </div>

    <script>
        function openMessage() {
            // Putar Lagu
            var audio = document.getElementById("myAudio");
            audio.play();

            // Pindah Halaman
            document.getElementById("homepage").style.display = "none";
            document.getElementById("contentPage").style.display = "block";
        }
    </script>

</body>
</html>
