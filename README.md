<!DOCTYPE html>
<html lang="es">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Animación de Corazón</title>
    <style>
        body {
            background-color: black;
            display: flex;
            justify-content: center;
            align-items: center;
            flex-direction: column;
            height: 100vh;
            color: white;
            font-family: Arial, sans-serif;
        }
        canvas {
            background-color: black;
        }
    </style>
</head>
<body>
    <canvas id="canvas" width="400" height="400"></canvas>
    <p><strong>Animos licencia no.1</strong></p>

    <script>
        const canvas = document.getElementById("canvas");
        const ctx = canvas.getContext("2d");

        function drawHeart(x, y, size) {
            ctx.fillStyle = "red";
            ctx.beginPath();
            ctx.moveTo(x, y);
            ctx.bezierCurveTo(x - size, y - size, x - size * 2, y + size, x, y + size * 2);
            ctx.bezierCurveTo(x + size * 2, y + size, x + size, y - size, x, y);
            ctx.fill();
        }

        drawHeart(200, 150, 50);
    </script>
</body>
</html>
