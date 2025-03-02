# Descifra-el-mensaje
<html lang="es">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Desbloquea el mensaje</title>
    <style>
        body {
            font-family: Arial, sans-serif;
            text-align: center;
            margin: 50px;
            transition: background-color 0.5s;
        }
        #mensaje {
            display: none;
            margin-top: 20px;
            font-size: 1.2em;
            color: green;
        }
    </style>
</head>
<body>
    <h2>Introduce el código para desbloquear el mensaje</h2>
    <input type="password" id="codigo" placeholder="Ingresa el código" maxlength="4">
    <button onclick="verificarCodigo()">Desbloquear</button>
    <p id="mensaje"></p>
    <audio id="alarma" src="https://www.soundjay.com/button/beep-10.mp3"></audio>
    <script>
        function verificarCodigo() {
            var codigoIngresado = document.getElementById("codigo").value;
            if (codigoIngresado === "2014") {
                document.getElementById("mensaje").innerText = "¡Bien hecho! Pero, ¿te recuerda a algo ese año?";
                document.getElementById("mensaje").style.display = "block";
                document.body.style.backgroundColor = "white";
            } else {
                document.body.style.backgroundColor = "red";
                document.getElementById("alarma").play();
                setTimeout(() => { document.body.style.backgroundColor = "white"; }, 500);
                alert("Código incorrecto, intenta de nuevo.");
            }
        }
    </script>
</body>
</html>
