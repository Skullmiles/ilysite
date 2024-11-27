<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Do You Love Me?</title>
    <style>
        body {
            font-family: Arial, sans-serif;
            display: flex;
            justify-content: center;
            align-items: center;
            height: 100vh;
            margin: 0;
            background-color: #f9f9f9;
        }
        h1 {
            color: red;
            margin-bottom: 20px;
        }
        .container {
            text-align: center;
        }
        .button {
            padding: 10px 20px;
            margin: 10px;
            font-size: 18px;
            border: none;
            border-radius: 5px;
            cursor: pointer;
            transition: transform 0.3s ease, top 0.3s ease, left 0.3s ease;
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
    </style>
</head>
<body>
    <div class="container">
        <h1>Do you love me?</h1>
        <button class="button yes" onclick="alert('I love you too! 😊')">Yes</button>
        <button class="button no" onmouseover="moveButton()">No</button>
    </div>

    <script>
        const noButton = document.querySelector('.no');
        function moveButton() {
            const container = document.querySelector('.container');
            const containerRect = container.getBoundingClientRect();
            const buttonRect = noButton.getBoundingClientRect();

            const newTop = Math.random() * (containerRect.height - buttonRect.height);
            const newLeft = Math.random() * (containerRect.width - buttonRect.width);

            noButton.style.position = 'absolute';
            noButton.style.top = `${newTop}px`;
            noButton.style.left = `${newLeft}px`;
        }
    </script>
</body>
</html>