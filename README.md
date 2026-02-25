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
            padding: 2.5rem;
            border-radius: 25px;
            box-shadow: 0 15px 35px rgba(214, 51, 132, 0.2);
            text-align: center;
            max-width: 380px;
            width: 90%;
            border: 2px solid #fff;
        }
        h2 { color: #d63384; margin-bottom: 20px; font-size: 1.2rem; line-height: 1.4; }
        .input-group {
            display: flex;
            gap: 15px;
            margin-bottom: 25px;
        }
        .input-box {
            flex: 1;
        }
        label {
            display: block;
            font-size: 0.8rem;
            color: #ff4d6d;
            margin-bottom: 5px;
            font-weight: bold;
        }
        input {
            width: 80%;
            padding: 12px;
            border: 2px solid #ffb3c1;
            border-radius: 12px;
            outline: none;
            text-align: center;
            font-size: 1.1rem;
            transition: 0.3s;
        }
        input:focus { border-color: #ff4d6d; box-shadow: 0 0 8px rgba(255, 77, 109, 0.3); }
        
        button {
            background-color: #ff4d6d;
            color: white;
            border: none;
            padding: 14px;
            border-radius: 30px;
            cursor: pointer;
            font-weight: bold;
            font-size: 1rem;
            width: 100%;
            box-shadow: 0 4px 15px rgba(255, 77, 109, 0.4);
            transition: 0.3s;
        }
        button:hover { background-color: #c9184a; transform: translateY(-2px); }
        
        #result {
            display: none;
            animation: heartBeat 1.2s infinite, fadeIn 0.8s;
        }
        .cat-img { width: 180px; border-radius: 20px; margin-bottom: 20px; }
        .error { color: #ff4d6d; font-size: 0.85rem; margin-top: 15px; display: none; font-weight: 500; }
        
        @keyframes fadeIn { from { opacity: 0; transform: scale(0.9); } to { opacity: 1; transform: scale(1); } }
    </style>
</head>
<body>

    <div class="card" id="login-card">
        <h2>Ingresa El Día Y El Año <br>En Que Nos Conocimos ❤️</h2>
        <div class="input-group">
            <div class="input-box">
                <label>Día</label>
                <input type="number" id="day" placeholder="21">
            </div>
            <div class="input-box">
                <label>Año</label>
                <input type="number" id="year" placeholder="2025">
            </div>
        </div>
        <button onclick="verify()">Verificar ❤️</button>
        <p id="error-msg" class="error">¡Ups! Esa no es la fecha. <br>Inténtalo de nuevo, amor. 🥺</p>
    </div>

    <div class="card" id="result">
        <img src="https://media.tenor.com/7S_m9V9H87MAAAAi/tkthao219-bubududu.gif" alt="Cat" class="cat-img">
        <h2 style="color: #ff4d6d;">¡Correcto! ❤️ Te Amo Mucho.</h2>
        <p style="color: #666; line-height: 1.5;">Los recuerdos de nuestro primer encuentro los guardaré bajo 7 llaves. <br><b>Te amo mucho mi Amor.</b></p>
    </div>

    <script>
        function verify() {
            const dayInput = document.getElementById('day').value;
            const yearInput = document.getElementById('year').value;
            const errorMsg = document.getElementById('error-msg');
            
            // CONFIGURACIÓN DE LA FECHA
            const diaCorrecto = "21";
            const anioCorrecto = "2025";
            
            if (dayInput === diaCorrecto && yearInput === anioCorrecto) {
                document.getElementById('login-card').style.display = 'none';
                document.getElementById('result').style.display = 'block';
            } else {
                errorMsg.style.display = 'block';
                // Animación de vibración para el error
                document.getElementById('login-card').style.animation = "shake 0.4s";
                setTimeout(() => { document.getElementById('login-card').style.animation = ""; }, 400);
            }
        }
    </script>

    <style>
        @keyframes shake {
            0%, 100% { transform: translateX(0); }
            25% { transform: translateX(-8px); }
            75% { transform: translateX(8px); }
        }
    </style>
</body>
</html>
