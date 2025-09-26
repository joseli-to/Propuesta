<!DOCTYPE html>
<html lang="es">
<head>
    <meta charset="UTF-8">
    <title>Pregunta Especial</title>
    <style>
        body {
            margin: 0;
            padding: 0;
            font-family: 'Arial', sans-serif;
            text-align: center;
            background: linear-gradient(135deg, #ff9a9e, #fad0c4);
            height: 100vh;
            overflow: hidden;
            display: flex;
            justify-content: center;
            align-items: center;
            position: relative;
        }

        .heart {
            position: absolute;
            color: rgba(255, 0, 100, 0.7);
            font-size: 20px;
            animation: floatUp 6s linear infinite;
        }

        @keyframes floatUp {
            0% { transform: translateY(100vh) scale(1); opacity: 1; }
            100% { transform: translateY(-10vh) scale(1.5); opacity: 0; }
        }

        .container {
            background: rgba(255, 255, 255, 0.9);
            padding: 40px;
            border-radius: 15px;
            box-shadow: 0 4px 20px rgba(0,0,0,0.2);
            animation: fadeIn 2s ease-in-out;
            z-index: 10;
        }

        h1 {
            color: #e63946;
            font-size: 2.5rem;
            margin-bottom: 20px;
            animation: heartbeat 1.5s infinite;
        }

        .button {
            padding: 12px 24px;
            margin: 15px;
            font-size: 18px;
            font-weight: bold;
            cursor: pointer;
            border: none;
            border-radius: 8px;
            transition: transform 0.2s, background 0.3s;
        }

        .yes {
            background-color: #06d6a0;
            color: white;
        }

        .yes:hover {
            background-color: #05c08c;
            transform: scale(1.1);
        }

        .no {
            background-color: #ef476f;
            color: white;
        }

        .no:hover {
            background-color: #d43f63;
            transform: scale(1.1);
        }

        @keyframes heartbeat {
            0%, 100% { transform: scale(1); }
            50% { transform: scale(1.1); }
        }

        @keyframes fadeIn {
            from { opacity: 0; transform: translateY(-20px); }
            to { opacity: 1; transform: translateY(0); }
        }
    </style>
</head>
<body>
    <div class="container">
        <h1>Valeria ❤️ ¿Quieres ser mi novia?</h1>
        <button class="button yes" onclick="respuesta('sí')">Sí</button>
        <button class="button no" onclick="respuesta('no')">No</button>
    </div>

    <script>
        function respuesta(opcion) {
            if (opcion === 'sí') {
                alert("💖 ¡Qué felicidad, Valeria! Sabía que dirías que sí 💖");
                setTimeout(() => {
                    // Redirige al video de TikTok si dice 'sí'
                    window.location.href = "https://vt.tiktok.com/ZSDqG8vCT/";
                }, 1000);
            } else {
                alert("😢 Oh no, Valeria... igual te aprecio mucho.");
                setTimeout(() => {
                    // Redirige al video de Instagram si dice 'no'
                    window.location.href = "https://www.instagram.com/reel/DJ7Z2rTyJzL/?igsh=ZDhheDYzem05ZW5r";
                }, 1000);
            }
        }

        // Crear corazones flotantes
        function crearCorazon() {
            const corazon = document.createElement("div");
            corazon.classList.add("heart");
            corazon.innerHTML = "❤️";
            corazon.style.left = Math.random() * 100 + "vw";
            corazon.style.fontSize = (Math.random() * 20 + 15) + "px";
            document.body.appendChild(corazon);

            setTimeout(() => { corazon.remove(); }, 6000);
        }

        // Iniciar la animación de corazones
        setInterval(crearCorazon, 500);
    </script>
</body>
</html>
