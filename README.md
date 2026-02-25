<!DOCTYPE html>
<html lang="es">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Para Mi Amor</title>
    <style>
        body {
            background-color: #ffdae0;
            display: flex;
            justify-content: center;
            align-items: center;
            height: 100vh;
            margin: 0;
            font-family: 'Segoe UI', Tahoma, Geneva, Verdana, sans-serif;
        }
        .card {
            background: white;
            padding: 2rem;
            border-radius: 20px;
            box-shadow: 0 10px 25px rgba(0,0,0,0.1);
            text-align: center;
            max-width: 350px;
            width: 90%;
        }
        h2 { color: #d63384; margin-bottom: 20px; font-size: 1.2rem; }
        .input-group {
            display: flex;
            gap: 10px;
            margin-bottom: 20px;
        }
        input {
            width: 100%;
            padding: 12px;
            border: 2px solid #ffb3c1;
            border-radius: 10px;
            outline: none;
            text-align: center;
            font-size: 1rem;
        }
        input:focus { border-color: #ff4d6d; }
        button {
            background-color: #ff4d6d;
            color: white;
            border: none;
            padding: 12px 25px;
            border-radius: 25px;
            cursor: pointer;
            font-weight: bold;
            transition: 0.3s;
            width: 100%;
        }
        button:hover { background-color: #c9184a; }
        #result {
            margin-top: 20px;
            display: none;
            animation: fadeIn 1s;
        }
        .cat-img { width: 150px; border-radius: 15px; margin-bottom: 15px; }
        .error { color: #ff4d6d; font-size: 0.9rem; margin-top: 10px; display: none; }
        @keyframes fadeIn { from { opacity: 0; } to { opacity: 1; } }
    </style>
</head>
<body>

    <div class="card" id="login-card">
        <h2>Ingresa el Día y el Año <br>En Que Nos Conocimos ❤️</h2>
        <div class="input-group">
            <input type="number" id="day" placeholder="Día (DD)">
            <input type="number" id="year" placeholder="Año (AAAA)">
        </div>
        <button onclick="verify()">Verificar</button>
        <p id="error-msg" class="error">Fecha incorrecta, inténtalo de nuevo. ❤️</p>
    </div>

    <div class="card" id="result">
        <img src="https://media.tenor.com/7S_m9V9H87MAAAAi/tkthao219-bubududu.gif" alt="Cat" class="cat-img">
        <h2 id="final-text">¡Correcto! ❤️ Te Amo Mucho.</h2>
        <p style="color: #666;">Los recuerdos de nuestro primer encuentro los guardaré bajo 7 llaves. Te amo mucho mi amor.</p>
    </div>

    <script>
        function verify() {
            const day = document.getElementById('day').value;
            const year = document.getElementById('year').value;
            const errorMsg = document.getElementById('error-msg');
            
            // --- CAMBIA EL AÑO AQUÍ ---
            const añoCorrecto = "2022"; // Pon el año real aquí
            
            if (day === "21" && year === añoCorrecto) {
                document.getElementById('login-card').style.display = 'none';
                document.getElementById('result').style.display = 'block';
            } else {
                errorMsg.style.display = 'block';
            }
        }
    </script>
</body>
</html>
