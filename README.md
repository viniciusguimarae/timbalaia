# timbalaia<!DOCTYPE html>
<html lang="pt-br">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Proposta de Casamento</title>
    <style>
        body {
            font-family: Arial, sans-serif;
            background-color: #f4f4f9;
            display: flex;
            justify-content: center;
            align-items: center;
            height: 100vh;
            margin: 0;
            text-align: center;
        }

        .container {
            background-color: white;
            padding: 30px;
            border-radius: 10px;
            box-shadow: 0 0 15px rgba(0, 0, 0, 0.1);
        }

        h1 {
            font-size: 36px;
            color: #333;
        }

        .buttons {
            margin-top: 20px;
        }

        .button {
            font-size: 20px;
            padding: 10px 20px;
            margin: 10px;
            border: none;
            border-radius: 5px;
            cursor: pointer;
            transition: 0.3s;
        }

        .yes {
            background-color: #4CAF50;
            color: white;
        }

        .no {
            background-color: #f44336;
            color: white;
            position: relative;
        }

        .no:hover {
            background-color: #e53935;
        }

        .no.flee {
            position: absolute;
            transition: transform 0.1s ease;
        }
    </style>
</head>
<body>

<div class="container">
    <h1>Você quer casar comigo?</h1>
    <div class="buttons">
        <button class="button yes">Sim</button>
        <button class="button no">Não</button>
    </div>
</div>

<script>
    const noButton = document.querySelector('.no');
    const yesButton = document.querySelector('.yes');

    noButton.addEventListener('mouseover', () => {
        noButton.classList.add('flee');
        const randomX = Math.random() * 200 - 100; // Movimenta entre -100 e 100px
        const randomY = Math.random() * 200 - 100; // Movimenta entre -100 e 100px
        noButton.style.transform = `translate(${randomX}px, ${randomY}px)`;
    });

    noButton.addEventListener('mouseleave', () => {
        noButton.classList.remove('flee');
        noButton.style.transform = 'translate(0, 0)';
    });

    yesButton.addEventListener('click', () => {
        alert('Que bom! 💍');
    });

    noButton.addEventListener('click', () => {
        alert('Que pena, mas tudo bem! 💔');
    });
</script>

</body>
</html>
