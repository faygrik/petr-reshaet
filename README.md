<!DOCTYPE html>
<html lang="ru">
<head>
    <meta charset="UTF-8">
    <title>Калькулятор</title>
    <style>
        /* Простейший стиль для калькулятора */
        #calculator {
            width: 200px;
            text-align: center;
            margin: auto;
        }
    </style>
</head>
<body>
    <div id="calculator">
        <input type="text" id="display" disabled>
        <br>
        <button onclick="appendToDisplay('1')">1</button>
        <button onclick="appendToDisplay('2')">2</button>
        <button onclick="appendToDisplay('3')">3</button>
        <button onclick="appendToDisplay('+')">+</button>
        <br>
        <button onclick="appendToDisplay('4')">4</button>
        <button onclick="appendToDisplay('5')">5</button>
        <button onclick="appendToDisplay('6')">6</button>
        <button onclick="appendToDisplay('-')">-</button>
        <br>
        <button onclick="appendToDisplay('7')">7</button>
        <button onclick="appendToDisplay('8')">8</button>
        <button onclick="appendToDisplay('9')">9</button>
        <button onclick="appendToDisplay('*')">*</button>
        <br>
        <button onclick="clearDisplay()">C</button>
        <button onclick="appendToDisplay('0')">0</button>
        <button onclick="calculate()">=</button>
        <button onclick="appendToDisplay('/')">/</button>
    </div>

    <script>
        function appendToDisplay(value) {
            document.getElementById("display").value += value;
        }

        function clearDisplay() {
            document.getElementById("display").value = '';
        }

        function calculate() {
            try {
                document.getElementById("display").value = eval(document.getElementById("display").value);
            } catch (e) {
                alert("Ошибка!");
            }
        }
    </script>
</body>
</html>
