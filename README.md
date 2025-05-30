# A-cademia-das-guias-
<!DOCTYPE html>
<html lang="pt-br">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Quiz Interativo</title>
    <style>
        body {
            font-family: Arial, sans-serif;
            margin: 40px;
        }
        .option {
            display: block;
            margin: 10px 0;
            padding: 10px;
            width: 300px;
            border: 2px solid #ccc;
            border-radius: 5px;
            cursor: pointer;
            background-color: white;
            transition: background-color 0.3s, color 0.3s;
        }
        .correct {
            background-color: #4CAF50;
            color: white;
            border-color: #4CAF50;
        }
        .incorrect {
            background-color: #f44336;
            color: white;
            border-color: #f44336;
        }
    </style>
</head>
<body>

    <h2>Pergunta:</h2>
    <p>Qual é a capital do Brasil?</p>

    <div id="options">
        <div class="option" onclick="checkAnswer(this, 'b')">a) Buenos Aires</div>
        <div class="option" onclick="checkAnswer(this, 'c')">b) Santiago</div>
        <div class="option" onclick="checkAnswer(this, 'a')">c) Brasília</div>
        <div class="option" onclick="checkAnswer(this, 'd')">d) Lima</div>
    </div>

    <script>
        const correctAnswer = 'a';

        function checkAnswer(element, answer) {
            const options = document.querySelectorAll('.option');
            options.forEach(option => {
                option.onclick = null; // desativa clique após resposta
                if (option.innerText.startsWith(correctAnswer)) {
                    option.classList.add('correct');
                } else {
                    option.classList.add('incorrect');
                }
            });

            if (answer === correctAnswer) {
                element.classList.add('correct');
            } else {
                element.classList.add('incorrect');
            }
        }
    </script>

</body>
</html>
