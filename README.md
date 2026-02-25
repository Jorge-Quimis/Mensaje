<!DOCTYPE html>
<html lang="es">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Para Mi Amor</title>
    <style>
        body { background-color: #ffdae0; display: flex; justify-content: center; align-items: center; height: 100vh; margin: 0; font-family: sans-serif; }
        .card { background: white; padding: 2rem; border-radius: 20px; box-shadow: 0 10px 25px rgba(0,0,0,0.1); text-align: center; max-width: 350px; width: 90%; }
        h2 { color: #d63384; font-size: 1.1rem; }
        .input-group { display: flex; gap: 10px; margin: 20px 0; }
        input { width: 100%; padding: 12px; border: 2px solid #ffb3c1; border-radius: 10px; text-align: center; font-size: 1rem; }
        button { background-color: #ff4d6d; color: white; border: none; padding: 12px; border-radius: 25px; cursor: pointer; width: 100%; font-weight: bold; }
        #result { display: none; animation: fadeIn 1s; }
        .cat-img { width: 150px; border-radius: 15px; }
        @keyframes fadeIn { from { opacity: 0; } to { opacity: 1; } }
    </style>
</head>
<body>

    <div class="card" id="login-card">
        <h2>Ingresa El Día Y El Año <br> En Que Nos Conocimos ❤️</h2>
        <div class="input-group">
            <input type="number" id="day" placeholder="Día (21)">
            <input type="number" id="year" placeholder="Año (AAAA)">
        </div>
        <button onclick="verify()">Verificar</button>
        <p id="error" style="color: red; display: none; font-size: 0.8rem; margin-top: 10px;">Fecha incorrecta, intenta de nuevo.</p>
    </div>

    <div class="card" id="result">
        <img src="https://media.tenor.com/7S_m9V9H87MAAAAi/tkthao219-bubududu.gif" class="cat-img">
        <h2>¡Correcto! ❤️ Te Amo Mucho</h2>
        <p>Los recuerdos de nuestro primer encuentro los guardaré bajo 7 llaves.</p>
    </div>

    <script>
        function verify() {
            const d = document.getElementById('day').value;
            const y = document.getElementById('year').value;
            // CAMBIA EL "2022" POR EL AÑO REAL DE USTEDES
            if(d === "21" && y === "2025") { 
                document.getElementById('login-card').style.display = 'none';
                document.getElementById('result').style.display = 'block';
            } else {
                document.getElementById('error').style.display = 'block';
            }
        }
    </script>
</body>
</html>
