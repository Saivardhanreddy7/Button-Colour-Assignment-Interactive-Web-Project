<!DOCTYPE html>
<html>
<head>
    <title>Button Colour Assignment</title>

    <style>
        body {
            font-family: Arial, sans-serif;
            text-align: center;
            background-color: #f5f5f5;
        }

        h1 {
            margin-top: 50px;
        }

        .buttons {
            width: 500px;
            margin: 40px auto;
            display: grid;
            grid-template-columns: repeat(3, 1fr);
            gap: 20px;
        }

        button {
            padding: 20px;
            font-size: 16px;
            border: none;
            border-radius: 8px;
            background-color: white;
            cursor: pointer;
        }

        button:disabled {
            color: white;
            cursor: not-allowed;
        }
    </style>
</head>

<body>

    <h1>Button Colour Assignment</h1>

    <div class="buttons">
        <button onclick="changeColor(this)">Button 1</button>
        <button onclick="changeColor(this)">Button 2</button>
        <button onclick="changeColor(this)">Button 3</button>
        <button onclick="changeColor(this)">Button 4</button>
        <button onclick="changeColor(this)">Button 5</button>
        <button onclick="changeColor(this)">Button 6</button>
        <button onclick="changeColor(this)">Button 7</button>
        <button onclick="changeColor(this)">Button 8</button>
        <button onclick="changeColor(this)">Button 9</button>
    </div>

    <script>
        let colors = [
            "red",
            "blue",
            "green",
            "orange",
            "purple",
            "pink",
            "yellow",
            "cyan",
            "brown"
        ];

        let index = 0;

        function changeColor(button) {

            button.style.backgroundColor = colors[index];

            button.innerText = colors[index];

            button.disabled = true;

            index++;
        }
    </script>

</body>
</html>
