<!DOCTYPE html>
<html lang="pt-BR">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Declaração</title>
    <style>
        body {
            background-color: lightblue;
            display: flex;
            justify-content: center;
            align-items: center;
            height: 100vh;
            margin: 0;
            font-family: Arial, sans-serif;
            text-align: center;
        }
        .message {
            font-size: 1.5em;
            margin-bottom: 20px;
            white-space: pre-wrap;
        }
        .buttons {
            display: flex;
            justify-content: space-around;
        }
        .button {
            padding: 10px 20px;
            font-size: 1em;
            cursor: pointer;
            border: none;
            border-radius: 5px;
            transition: background-color 0.3s;
        }
        .yes-button {
            background-color: green;
            color: white;
        }
        .no-button {
            background-color: red;
            color: white;
        }
        .yes-button:hover {
            background-color: darkgreen;
        }
        .no-button:hover {
            background-color: darkred;
        }
    </style>
</head>
<body>
    <div>
        <div class="message">
Awani, meu amor, eu te acho uma mulher linda,
inteligente, elegante, perfeita, incrível.
Adoraria tentar te fazer feliz um dia.
Prometo que você não vai se arrepender.
Quer namorar comigo?😋😋
        </div>
        <div class="buttons">
            <button class="button yes-button" onclick="yesClick()">Sim</button>
            <button class="button no-button" onmouseover="moveButton()">Não</button>
        </div>
    </div>

    <script>
        function yesClick() {
            alert("Você aceitou namorar comigo <3");
            window.location.href = "https://www.youtube.com/watch?v=izGwDsrQ1eQ";
        }

        function moveButton() {
            var button = document.querySelector('.no-button');
            var container = document.querySelector('body');
            var containerRect = container.getBoundingClientRect();
            var buttonRect = button.getBoundingClientRect();
            
            var newTop = Math.random() * (containerRect.height - buttonRect.height);
            var newLeft = Math.random() * (containerRect.width - buttonRect.width);
            
            button.style.position = 'absolute';
            button.style.top = newTop + 'px';
            button.style.left = newLeft + 'px';
        }
    </script>
</body>
</html>

