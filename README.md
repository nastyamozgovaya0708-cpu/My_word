# My_word
<!DOCTYPE html>
<html lang="ru">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Моя страница</title>
    <style>
        * {
            margin: 0;
            padding: 0;
            box-sizing: border-box;
        }

        body {
            font-family: 'Segoe UI', Tahoma, Geneva, Verdana, sans-serif;
            background: linear-gradient(135deg, #667eea 0%, #764ba2 100%);
            min-height: 100vh;
            display: flex;
            justify-content: center;
            align-items: center;
            padding: 20px;
        }

        .container {
            background: #fff;
            border-radius: 20px;
            box-shadow: 0 20px 60px rgba(0, 0, 0, 0.3);
            padding: 40px;
            max-width: 600px;
            width: 100%;
            text-align: center;
        }

        h1 {
            color: #333;
            margin-bottom: 20px;
            font-size: 2.5em;
        }

        p {
            color: #666;
            line-height: 1.6;
            margin-bottom: 20px;
        }

        button {
            background: linear-gradient(135deg, #667eea 0%, #764ba2 100%);
            color: white;
            border: none;
            padding: 15px 40px;
            font-size: 1.1em;
            border-radius: 50px;
            cursor: pointer;
            transition: transform 0.2s, box-shadow 0.2s;
        }

        button:hover {
            transform: translateY(-2px);
            box-shadow: 0 10px 25px rgba(102, 126, 234, 0.5);
        }

        button:active {
            transform: translateY(0);
        }

        #counter {
            font-size: 2em;
            font-weight: bold;
            color: #667eea;
            margin: 20px 0;
            min-height: 50px;
        }
    </style>
</head>
<body>
    <div class="container">
        <h1>👋 Привет, мир!</h1>
        <p>Это простая страница с интерактивной кнопкой. Нажмите на кнопку ниже, чтобы увеличить счётчик.</p>
        
        <div id="counter">0</div>
        
        <button id="clickBtn">Нажми меня</button>
    </div>

    <script>
        let count = 0;
        const counter = document.getElementById('counter');
        const button = document.getElementById('clickBtn');

        button.addEventListener('click', () => {
            count++;
            counter.textContent = count;
            
            if (count % 10 === 0) {
                counter.style.color = '#e74c3c';
                setTimeout(() => {
                    counter.style.color = '#667eea';
                }, 500);
            }
        });
    </script>
</body>
</html>
