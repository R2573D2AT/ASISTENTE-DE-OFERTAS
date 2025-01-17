<html lang="es">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Ofertas de Préstamos y Minicréditos</title>
    <style>
        body {
            font-family: Arial, sans-serif;
            display: flex;
            justify-content: center;
            align-items: center;
            height: 100vh;
            margin: 0;
            background-color: #1d0552;
            color: #fff;
        }
        .container {
            text-align: center;
            background-color: #1d0552;
            padding: 20px;
            border-radius: 10px;
            box-shadow: 0 4px 8px rgba(0, 0, 0, 0.2);
            width: 300px;
            height: 300px;
            display: flex;
            flex-direction: column;
            justify-content: center;
        }
        h1 {
            font-size: 22px;
            margin: 0;
        }
        button {
            font-size: 18px;
            padding: 10px 20px;
            background-color: #f39c12;
            color: #1d0552;
            border: none;
            cursor: pointer;
            margin-top: 20px;
            border-radius: 5px;
            transition: background-color 0.3s ease;
        }
        button:hover {
            background-color: #e67e22;
        }
        #processing {
            display: none;
            margin-top: 20px;
        }
        #processing img {
            width: 50px;
            height: 50px;
        }
        @media (max-width: 600px) {
            .container {
                width: 90%;
                height: auto;
            }
            button {
                width: 100%;
                font-size: 16px;
                padding: 15px;
            }
        }
    </style>
</head>
<body>
    <div class="container">
        <h1>Mejor oferta de préstamo del momento</h1>
        <button id="btnRedirect" onclick="redirectRandom()">Iniciar búsqueda</button>
        <div id="processing">
            <img src="https://i.imgur.com/llF5iyg.gif" alt="Procesando">
            <p>Procesando...</p>
        </div>
    </div>

    <script>
        function redirectRandom() {
            // Mostrar el mensaje de procesamiento
            document.getElementById('btnRedirect').style.display = 'none';
            document.getElementById('processing').style.display = 'block';

            // Simular un tiempo de espera de 5 segundos antes de redirigir
            setTimeout(function() {
                // Array de enlaces disponibles
                var links = [
                    "https://track.adtraction.com/t/t?a=1497931818&as=1889896122&t=2&tk=1",
                    "https://track.adtraction.com/t/t?a=1871477504&as=1889896122&t=2&tk=1",
                    "https://track.adtraction.com/t/t?a=1811017073&as=1889896122&t=2&tk=1",
                    "https://track.adtraction.com/t/t?a=1267998741&as=1889896122&t=2&tk=1",
                    "https://track.adtraction.com/t/t?a=1280180470&as=1889896122&t=2&tk=1",
                    "https://track.adtraction.com/t/t?a=1176089862&as=1889896122&t=2&tk=1",
                    "https://track.adtraction.com/t/t?a=1788792702&as=1889896122&t=2&tk=1",
                    "https://track.adtraction.com/t/t?a=1864612129&as=1889896122&t=2&tk=1",
                    "https://track.adtraction.com/t/t?a=1871477291&as=1889896122&t=2&tk=1",
                    "https://track.adtraction.com/t/t?a=1650383167&as=1889896122&t=2&tk=1",
                    "https://track.adtraction.com/t/t?a=1727514780&as=1889896122&t=2&tk=1",
                    "https://track.adtraction.com/t/t?a=1871477911&as=1889896122&t=2&tk=1",
                    "https://track.adtraction.com/t/t?a=1497934340&as=1889896122&t=2&tk=1",
                    "https://track.adtraction.com/t/t?a=1179627405&as=1889896122&t=2&tk=1",
                    "https://track.adtraction.com/t/t?a=1882452491&as=1889896122&t=2&tk=1",
                    "https://track.adtraction.com/t/t?a=1498404511&as=1889896122&t=2&tk=1",
                    "https://track.adtraction.com/t/t?a=1871477231&as=1889896122&t=2&tk=1"
                ];

                // Elegir un enlace aleatorio
                var randomIndex = Math.floor(Math.random() * links.length);
                var randomLink = links[randomIndex];

                // Abrir el enlace en una nueva ventana
                var newWindow = window.open(randomLink, '_blank');

                // Mostrar un botón en caso de que la ventana emergente sea bloqueada
                if (!newWindow || newWindow.closed || typeof newWindow.closed == 'undefined') {
                    document.getElementById('processing').innerHTML = '<p>La ventana emergente fue bloqueada. Haga clic en el botón de abajo para abrir la oferta.</p><button onclick="window.open(\'' + randomLink + '\', \'_blank\')">Abrir oferta</button>';
                } else {
                    // Ocultar el mensaje de procesamiento si la ventana emergente se abrió correctamente
                    document.getElementById('processing').style.display = 'none';
                    document.getElementById('btnRedirect').style.display = 'inline-block';
                }
            }, 5000); // 5000 milisegundos = 5 segundos
        }
    </script>
</body>
</html>

