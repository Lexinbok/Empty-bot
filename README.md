# Empty-bot
Empty-bot: A kid-friendly learning website that combines interactive games and engaging content to inspire a lifelong love for learning. This repository contains the code and assets for the Empty-bot website, designed to make learning as fun as playtime.
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Kids Word Learning Game</title>
    <style>
        body {
            text-align: center;
            font-family: Arial, sans-serif;
        }
        h1 {
            color: #333;
        }
        .shape {
            width: 100px;
            height: 100px;
            margin: 20px;
            display: inline-block;
            cursor: pointer;
            border-radius: 50%;
        }
        #circle {
            background-color: red;
        }
        #square {
            background-color: blue;
        }
        #triangle {
            width: 0;
            height: 0;
            border-left: 50px solid transparent;
            border-right: 50px solid transparent;
            border-bottom: 100px solid green;
        }
    </style>
</head>
<body>
    <h1>Click on the Correct Shape!</h1>
    <div class="shape" id="circle"></div>
    <div class="shape" id="square"></div>
    <div class="shape" id="triangle"></div>
    
    <p id="result"></p>

    <h1>Learn Two-Letter Words</h1>
    <p>Click on the correct two-letter word:</p>
    <button class="word-button">_a</button>
    <button class="word-button">_o</button>
    <button class="word-button">_i</button>
    <!-- Add more buttons for other two-letter words -->

    <script>
        const shapes = document.querySelectorAll('.shape');
        const result = document.getElementById('result');
        const wordButtons = document.querySelectorAll('.word-button');

        shapes.forEach(shape => {
            shape.addEventListener('click', () => {
                if (shape.id === 'circle') {
                    result.textContent = 'Correct Shape! 🎉';
                } else {
                    result.textContent = 'Try again with shapes! ❌';
                }
            });
        });

        wordButtons.forEach(button => {
            button.addEventListener('click', () => {
                if (button.textContent === '_a') {
                    result.textContent = 'Correct Word! 🎉';
                } else {
                    result.textContent = 'Try again with words! ❌';
                }
            });
        });
    </script>
</body>
</html>
