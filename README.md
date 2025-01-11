<!DOCTYPE html>
<html lang="pt-BR">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Quiz com Namorada</title>
    <style>
        body {
            font-family: Arial, sans-serif;
            text-align: center;
            margin: 0;
            padding: 0;
            background-color: #fce4ec;
        }
        h1 {
            margin-top: 20%;
            font-size: 24px;
            color: #d81b60;
        }
        .buttons {
            margin-top: 20px;
        }
        button {
            font-size: 18px;
            padding: 10px 20px;
            margin: 10px;
            border: none;
            border-radius: 5px;
            cursor: pointer;
            transition: transform 0.2s;
        }
        .yes {
            background-color: #4caf50;
            color: white;
        }
        .no {
            background-color: #f44336;
            color: white;
            position: absolute;
        }
    </style>
</head>
<body>
    <h1>Me dá o bumbum?</h1>
    <div class="buttons">
        <button class="yes">Sim</button>
        <button class="no" id="noButton">Não</button>
    </div>

    <script>
        const noButton = document.getElementById('noButton');

        noButton.addEventListener('mouseover', () => {
            const viewportWidth = window.innerWidth;
            const viewportHeight = window.innerHeight;

            const randomX = Math.floor(Math.random() * (viewportWidth - noButton.offsetWidth));
            const randomY = Math.floor(Math.random() * (viewportHeight - noButton.offsetHeight));

            noButton.style.left = randomX + 'px';
            noButton.style.top = randomY + 'px';
        });

        noButton.addEventListener('click', () => {
            alert('Hmmm, tenta de novo!');
        });
    </script>
</body>
</html>
