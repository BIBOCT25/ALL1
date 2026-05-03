https://biboct25.github.io/ALL/

**Основные различия методов:**

| Метод | Что возвращает | Как обращаемся к 4-му полю | Как обращаемся к результату |
|:------|:--------------|:--------------------------|:---------------------------|
| getElementById | Один элемент | `getElementById('num4')` | `getElementById('result')` |
| getElementsByName | "Живая" коллекция | `getElementsByName('numInput')[3]` | `getElementsByName('result')[0]` |
| getElementsByClassName | "Живая" коллекция | `getElementsByClassName('numInput')[3]` | `getElementsByClassName('result')[0]` |
| getElementsByTagName | "Живая" коллекция | `getElementsByTagName('input')[3]` | `getElementsByTagName('p')[0]` |
| querySelector | Один элемент (первый) | `querySelectorAll('.numInput')[3]` | `querySelector('.result')` |
| querySelectorAll | Статическая коллекция | `querySelectorAll('.numInput')[3]` | `querySelectorAll('.result')[0]` |

**1. document.getElementById(id)**

```html
<!DOCTYPE html>
<html lang="ru">
<head>
    <meta charset="UTF-8">
    <title>getElementById</title>
</head>
<body>

    <input type="text" id="input1" value="первый">
    <input type="text" id="input2" value="второй">
    <input type="text" id="input3" value="третий">
    <input type="text" id="input4" value="четвёртый">

    <br><br>

    <a id="a1">первый</a><br>
    <a id="a2">второй</a><br>
    <a id="a3">третий</a><br>
    <a id="a4">четвёртый</a>

    <script>
        document.getElementById('input4').style.color = 'yellow';
        document.getElementById('a4').style.color = 'yellow';
    </script>

</body>
</html>
```
2. document.getElementsByName(name)

```html
<!DOCTYPE html>
<html lang="ru">
<head>
    <meta charset="UTF-8">
    <title>getElementsByName</title>
</head>
<body>

    <input type="text" name="myInput" value="первый">
    <input type="text" name="myInput" value="второй">
    <input type="text" name="myInput" value="третий">
    <input type="text" name="myInput" value="четвёртый">

    <br><br>

    <a name="myLink">первый</a><br>
    <a name="myLink">второй</a><br>
    <a name="myLink">третий</a><br>
    <a name="myLink">четвёртый</a>

    <script>
        document.getElementsByName('myInput')[3].style.color = 'yellow';
        document.getElementsByName('myLink')[3].style.color = 'yellow';
    </script>

</body>
</html>
```
3. document.getElementsByClassName(className)

```html
<!DOCTYPE html>
<html lang="ru">
<head>
    <meta charset="UTF-8">
    <title>getElementsByClassName</title>
</head>
<body>

    <input type="text" class="inp" value="первый">
    <input type="text" class="inp" value="второй">
    <input type="text" class="inp" value="третий">
    <input type="text" class="inp" value="четвёртый">

    <br><br>

    <a class="lnk">первый</a><br>
    <a class="lnk">второй</a><br>
    <a class="lnk">третий</a><br>
    <a class="lnk">четвёртый</a>

    <script>
        document.getElementsByClassName('inp')[3].style.color = 'yellow';
        document.getElementsByClassName('lnk')[3].style.color = 'yellow';
    </script>

</body>
</html>
```
4. document.getElementsByTagName(tagName)

```html
<!DOCTYPE html>
<html lang="ru">
<head>
    <meta charset="UTF-8">
    <title>getElementsByTagName</title>
</head>
<body>

    <input type="text" value="первый">
    <input type="text" value="второй">
    <input type="text" value="третий">
    <input type="text" value="четвёртый">

    <br><br>

    <a>первый</a><br>
    <a>второй</a><br>
    <a>третий</a><br>
    <a>четвёртый</a>

    <script>
        document.getElementsByTagName('input')[3].style.color = 'yellow';
        document.getElementsByTagName('a')[3].style.color = 'yellow';
    </script>

</body>
</html>
```
5. document.querySelector(selector)

```html
<!DOCTYPE html>
<html lang="ru">
<head>
    <meta charset="UTF-8">
    <title>querySelector</title>
</head>
<body>

    <input type="text" id="input1" value="первый">
    <input type="text" id="input2" value="второй">
    <input type="text" id="input3" value="третий">
    <input type="text" id="input4" value="четвёртый">

    <br><br>

    <a id="a1">первый</a><br>
    <a id="a2">второй</a><br>
    <a id="a3">третий</a><br>
    <a id="a4">четвёртый</a>

    <script>
        document.querySelector('#input4').style.color = 'yellow';
        document.querySelector('#a4').style.color = 'yellow';
    </script>

</body>
</html>
```
6. document.querySelectorAll(selector)

```html
<!DOCTYPE html>
<html lang="ru">
<head>
    <meta charset="UTF-8">
    <title>querySelectorAll</title>
</head>
<body>

    <input type="text" class="inp" value="первый">
    <input type="text" class="inp" value="второй">
    <input type="text" class="inp" value="третий">
    <input type="text" class="inp" value="четвёртый">

    <br><br>

    <a class="lnk">первый</a><br>
    <a class="lnk">второй</a><br>
    <a class="lnk">третий</a><br>
    <a class="lnk">четвёртый</a>

    <script>
        document.querySelectorAll('.inp')[3].style.color = 'yellow';
        document.querySelectorAll('.lnk')[3].style.color = 'yellow';
    </script>

</body>
</html>
```

**1. document.getElementById(id)**

```html
<!DOCTYPE html>
<html lang="ru">
<head>
    <meta charset="UTF-8">
    <title>Калькулятор кредита - getElementById</title>
</head>
<body>

    <h2>Калькулятор кредита</h2>
    
    <label>Сумма кредита:</label>
    <input type="number" id="amount" placeholder="100000"><br><br>
    
    <label>Процентная ставка (%):</label>
    <input type="number" id="rate" placeholder="12"><br><br>
    
    <label>Срок (месяцев):</label>
    <input type="number" id="months" placeholder="24"><br><br>
    
    <button id="calc">Рассчитать</button><br><br>
    
    <label>Всего отдадите:</label>
    <input type="text" id="result" readonly>

    <script>
        document.getElementById('calc').addEventListener('click', function() {
            let amount = document.getElementById('amount').value;
            let rate = document.getElementById('rate').value;
            let months = document.getElementById('months').value;
            let total = amount * (1 + rate / 100 * months / 12);
            document.getElementById('result').value = total.toFixed(2);
        });
    </script>

</body>
</html>
```
**2. document.getElementsByName(name)**

```html
<!DOCTYPE html>
<html lang="ru">
<head>
    <meta charset="UTF-8">
    <title>Калькулятор кредита - getElementsByName</title>
</head>
<body>

    <h2>Калькулятор кредита</h2>
    
    <label>Сумма кредита:</label>
    <input type="number" name="amount" placeholder="100000"><br><br>
    
    <label>Процентная ставка (%):</label>
    <input type="number" name="rate" placeholder="12"><br><br>
    
    <label>Срок (месяцев):</label>
    <input type="number" name="months" placeholder="24"><br><br>
    
    <button name="calc">Рассчитать</button><br><br>
    
    <label>Всего отдадите:</label>
    <input type="text" name="result" readonly>

    <script>
        document.getElementsByName('calc')[0].addEventListener('click', function() {
            let amount = document.getElementsByName('amount')[0].value;
            let rate = document.getElementsByName('rate')[0].value;
            let months = document.getElementsByName('months')[0].value;
            let total = amount * (1 + rate / 100 * months / 12);
            document.getElementsByName('result')[0].value = total.toFixed(2);
        });
    </script>

</body>
</html>
```
**3. document.getElementsByClassName(className)**

```html
<!DOCTYPE html>
<html lang="ru">
<head>
    <meta charset="UTF-8">
    <title>Калькулятор кредита - getElementsByClassName</title>
</head>
<body>

    <h2>Калькулятор кредита</h2>
    
    <label>Сумма кредита:</label>
    <input type="number" class="amount" placeholder="100000"><br><br>
    
    <label>Процентная ставка (%):</label>
    <input type="number" class="rate" placeholder="12"><br><br>
    
    <label>Срок (месяцев):</label>
    <input type="number" class="months" placeholder="24"><br><br>
    
    <button class="calc">Рассчитать</button><br><br>
    
    <label>Всего отдадите:</label>
    <input type="text" class="result" readonly>

    <script>
        document.getElementsByClassName('calc')[0].addEventListener('click', function() {
            let amount = document.getElementsByClassName('amount')[0].value;
            let rate = document.getElementsByClassName('rate')[0].value;
            let months = document.getElementsByClassName('months')[0].value;
            let total = amount * (1 + rate / 100 * months / 12);
            document.getElementsByClassName('result')[0].value = total.toFixed(2);
        });
    </script>

</body>
</html>
```
**4. document.getElementsByTagName(tagName)**

```html
<!DOCTYPE html>
<html lang="ru">
<head>
    <meta charset="UTF-8">
    <title>Калькулятор кредита - getElementsByTagName</title>
</head>
<body>

    <h2>Калькулятор кредита</h2>
    
    <label>Сумма кредита:</label>
    <input type="number" placeholder="100000"><br><br>
    
    <label>Процентная ставка (%):</label>
    <input type="number" placeholder="12"><br><br>
    
    <label>Срок (месяцев):</label>
    <input type="number" placeholder="24"><br><br>
    
    <button>Рассчитать</button><br><br>
    
    <label>Всего отдадите:</label>
    <input type="text" readonly>

    <script>
        let inputs = document.getElementsByTagName('input');
        let buttons = document.getElementsByTagName('button');
        
        buttons[0].addEventListener('click', function() {
            let amount = inputs[0].value;
            let rate = inputs[1].value;
            let months = inputs[2].value;
            let total = amount * (1 + rate / 100 * months / 12);
            inputs[3].value = total.toFixed(2);
        });
    </script>

</body>
</html>
```
**5. document.querySelector(selector)**

```html
<!DOCTYPE html>
<html lang="ru">
<head>
    <meta charset="UTF-8">
    <title>Калькулятор кредита - querySelector</title>
</head>
<body>

    <h2>Калькулятор кредита</h2>
    
    <label>Сумма кредита:</label>
    <input type="number" id="amount" placeholder="100000"><br><br>
    
    <label>Процентная ставка (%):</label>
    <input type="number" id="rate" placeholder="12"><br><br>
    
    <label>Срок (месяцев):</label>
    <input type="number" id="months" placeholder="24"><br><br>
    
    <button id="calc">Рассчитать</button><br><br>
    
    <label>Всего отдадите:</label>
    <input type="text" id="result" readonly>

    <script>
        document.querySelector('#calc').addEventListener('click', function() {
            let amount = document.querySelector('#amount').value;
            let rate = document.querySelector('#rate').value;
            let months = document.querySelector('#months').value;
            let total = amount * (1 + rate / 100 * months / 12);
            document.querySelector('#result').value = total.toFixed(2);
        });
    </script>

</body>
</html>
```
**6. document.querySelectorAll(selector)**

```html
<!DOCTYPE html>
<html lang="ru">
<head>
    <meta charset="UTF-8">
    <title>Калькулятор кредита - querySelectorAll</title>
</head>
<body>

    <h2>Калькулятор кредита</h2>
    
    <label>Сумма кредита:</label>
    <input type="number" class="amount" placeholder="100000"><br><br>
    
    <label>Процентная ставка (%):</label>
    <input type="number" class="rate" placeholder="12"><br><br>
    
    <label>Срок (месяцев):</label>
    <input type="number" class="months" placeholder="24"><br><br>
    
    <button class="calc">Рассчитать</button><br><br>
    
    <label>Всего отдадите:</label>
    <input type="text" class="result" readonly>

    <script>
        document.querySelectorAll('.calc')[0].addEventListener('click', function() {
            let amount = document.querySelectorAll('.amount')[0].value;
            let rate = document.querySelectorAll('.rate')[0].value;
            let months = document.querySelectorAll('.months')[0].value;
            let total = amount * (1 + rate / 100 * months / 12);
            document.querySelectorAll('.result')[0].value = total.toFixed(2);
        });
    </script>

</body>
</html>
```

**1. document.getElementById — lab1_getElementById.html**

```html
<!DOCTYPE html>
<html lang='ru'>
<head>
    <meta charset='UTF-8'>
    <title>Метод: getElementById</title>
</head>
<body>
    <h2>Анализ числа (getElementById)</h2>
    <input type='number' id='num1' placeholder='Введите число 1'>
    <input type='number' id='num2' placeholder='Введите число 2'>
    <input type='number' id='num3' placeholder='Введите число 3'>
    <input type='number' id='num4' placeholder='Введите число 4'>
    <button onclick='analyzeNumber()'>Анализировать 4-е число</button>
    <p id='result'></p>

    <script>
        function analyzeNumber() {
            // Обращаемся к 4-му элементу по уникальному id
            let input = document.getElementById('num4').value;
            let num = Number(input);
            
            if (input === '' || isNaN(num)) {
                document.getElementById('result').textContent = 
                    'Ошибка: введите корректное число в 4-е поле!';
                return;
            }
            
            let sign = '';
            if (num > 0) {
                sign = 'положительное';
            } else if (num < 0) {
                sign = 'отрицательное';
            } else {
                sign = 'нулевое';
            }
            
            let parity = (num % 2 === 0) ? 'чётное' : 'нечётное';
            
            document.getElementById('result').textContent = 
                `Число ${num}: ${sign}, ${parity}.`;
        }
    </script>
</body>
</html>
```
**2. document.getElementsByName — lab1_getElementsByName.html**

```html
<!DOCTYPE html>
<html lang='ru'>
<head>
    <meta charset='UTF-8'>
    <title>Метод: getElementsByName</title>
</head>
<body>
    <h2>Анализ числа (getElementsByName)</h2>
    <input type='number' name='numInput' placeholder='Введите число 1'>
    <input type='number' name='numInput' placeholder='Введите число 2'>
    <input type='number' name='numInput' placeholder='Введите число 3'>
    <input type='number' name='numInput' placeholder='Введите число 4'>
    <button onclick='analyzeNumber()'>Анализировать 4-е число</button>
    <p name='result'></p>

    <script>
        function analyzeNumber() {
            // Получаем коллекцию элементов по атрибуту name
            let allInputs = document.getElementsByName('numInput');
            
            // Обращаемся к 4-му элементу (индекс 3)
            let input = allInputs[3].value;
            let num = Number(input);
            
            // Для вывода результата получаем первый элемент с name='result'
            let resultElement = document.getElementsByName('result')[0];
            
            if (input === '' || isNaN(num)) {
                resultElement.textContent = 
                    'Ошибка: введите корректное число в 4-е поле!';
                return;
            }
            
            let sign = '';
            if (num > 0) {
                sign = 'положительное';
            } else if (num < 0) {
                sign = 'отрицательное';
            } else {
                sign = 'нулевое';
            }
            
            let parity = (num % 2 === 0) ? 'чётное' : 'нечётное';
            
            resultElement.textContent = 
                `Число ${num}: ${sign}, ${parity}.`;
        }
    </script>
</body>
</html>
```
**3. document.getElementsByClassName — lab1_getElementsByClassName.html**

```html
<!DOCTYPE html>
<html lang='ru'>
<head>
    <meta charset='UTF-8'>
    <title>Метод: getElementsByClassName</title>
</head>
<body>
    <h2>Анализ числа (getElementsByClassName)</h2>
    <input type='number' class='numInput' placeholder='Введите число 1'>
    <input type='number' class='numInput' placeholder='Введите число 2'>
    <input type='number' class='numInput' placeholder='Введите число 3'>
    <input type='number' class='numInput' placeholder='Введите число 4'>
    <button onclick='analyzeNumber()'>Анализировать 4-е число</button>
    <p class='result'></p>

    <script>
        function analyzeNumber() {
            // Получаем "живую" коллекцию элементов по классу
            let allInputs = document.getElementsByClassName('numInput');
            
            // Обращаемся к 4-му элементу (индекс 3)
            let input = allInputs[3].value;
            let num = Number(input);
            
            // Для вывода результата получаем первый элемент с классом 'result'
            let resultElement = document.getElementsByClassName('result')[0];
            
            if (input === '' || isNaN(num)) {
                resultElement.textContent = 
                    'Ошибка: введите корректное число в 4-е поле!';
                return;
            }
            
            let sign = '';
            if (num > 0) {
                sign = 'положительное';
            } else if (num < 0) {
                sign = 'отрицательное';
            } else {
                sign = 'нулевое';
            }
            
            let parity = (num % 2 === 0) ? 'чётное' : 'нечётное';
            
            resultElement.textContent = 
                `Число ${num}: ${sign}, ${parity}.`;
        }
    </script>
</body>
</html>
```
**4. document.getElementsByTagName — lab1_getElementsByTagName.html**

```html
<!DOCTYPE html>
<html lang='ru'>
<head>
    <meta charset='UTF-8'>
    <title>Метод: getElementsByTagName</title>
</head>
<body>
    <h2>Анализ числа (getElementsByTagName)</h2>
    <input type='number' placeholder='Введите число 1'>
    <input type='number' placeholder='Введите число 2'>
    <input type='number' placeholder='Введите число 3'>
    <input type='number' placeholder='Введите число 4'>
    <button onclick='analyzeNumber()'>Анализировать 4-е число</button>
    <p></p>

    <script>
        function analyzeNumber() {
            // Получаем "живую" коллекцию всех элементов <input>
            let allInputs = document.getElementsByTagName('input');
            
            // Обращаемся к 4-му элементу (индекс 3)
            let input = allInputs[3].value;
            let num = Number(input);
            
            // Получаем коллекцию всех <p> и берём первый
            let resultElement = document.getElementsByTagName('p')[0];
            
            if (input === '' || isNaN(num)) {
                resultElement.textContent = 
                    'Ошибка: введите корректное число в 4-е поле!';
                return;
            }
            
            let sign = '';
            if (num > 0) {
                sign = 'положительное';
            } else if (num < 0) {
                sign = 'отрицательное';
            } else {
                sign = 'нулевое';
            }
            
            let parity = (num % 2 === 0) ? 'чётное' : 'нечётное';
            
            resultElement.textContent = 
                `Число ${num}: ${sign}, ${parity}.`;
        }
    </script>
</body>
</html>
```
**5. document.querySelector — lab1_querySelector.html**

```html
<!DOCTYPE html>
<html lang='ru'>
<head>
    <meta charset='UTF-8'>
    <title>Метод: querySelector</title>
</head>
<body>
    <h2>Анализ числа (querySelector)</h2>
    <input type='number' class='numInput' placeholder='Введите число 1'>
    <input type='number' class='numInput' placeholder='Введите число 2'>
    <input type='number' class='numInput' placeholder='Введите число 3'>
    <input type='number' class='numInput' placeholder='Введите число 4'>
    <button onclick='analyzeNumber()'>Анализировать 4-е число</button>
    <p class='result'></p>

    <script>
        function analyzeNumber() {
            // Используем CSS-селектор :nth-child(4) для выбора 4-го input
            // или можно использовать querySelectorAll и взять индекс
            let allInputs = document.querySelectorAll('.numInput');
            
            // Обращаемся к 4-му элементу (индекс 3)
            let input = allInputs[3].value;
            let num = Number(input);
            
            // querySelector возвращает первый элемент, соответствующий селектору
            let resultElement = document.querySelector('.result');
            
            if (input === '' || isNaN(num)) {
                resultElement.textContent = 
                    'Ошибка: введите корректное число в 4-е поле!';
                return;
            }
            
            let sign = '';
            if (num > 0) {
                sign = 'положительное';
            } else if (num < 0) {
                sign = 'отрицательное';
            } else {
                sign = 'нулевое';
            }
            
            let parity = (num % 2 === 0) ? 'чётное' : 'нечётное';
            
            resultElement.textContent = 
                `Число ${num}: ${sign}, ${parity}.`;
        }
    </script>
</body>
</html>
```
**6. document.querySelectorAll — lab1_querySelectorAll.html**

```html
<!DOCTYPE html>
<html lang='ru'>
<head>
    <meta charset='UTF-8'>
    <title>Метод: querySelectorAll</title>
</head>
<body>
    <h2>Анализ числа (querySelectorAll)</h2>
    <input type='number' class='numInput' placeholder='Введите число 1'>
    <input type='number' class='numInput' placeholder='Введите число 2'>
    <input type='number' class='numInput' placeholder='Введите число 3'>
    <input type='number' class='numInput' placeholder='Введите число 4'>
    <button onclick='analyzeNumber()'>Анализировать 4-е число</button>
    <p class='result'></p>

    <script>
        function analyzeNumber() {
            // Получаем статическую коллекцию всех элементов с классом 'numInput'
            let allInputs = document.querySelectorAll('.numInput');
            
            // Обращаемся к 4-му элементу (индекс 3)
            let input = allInputs[3].value;
            let num = Number(input);
            
            // querySelectorAll возвращает коллекцию, берём первый элемент
            let resultElement = document.querySelectorAll('.result')[0];
            
            if (input === '' || isNaN(num)) {
                resultElement.textContent = 
                    'Ошибка: введите корректное число в 4-е поле!';
                return;
            }
            
            let sign = '';
            if (num > 0) {
                sign = 'положительное';
            } else if (num < 0) {
                sign = 'отрицательное';
            } else {
                sign = 'нулевое';
            }
            
            let parity = (num % 2 === 0) ? 'чётное' : 'нечётное';
            
            resultElement.textContent = 
                `Число ${num}: ${sign}, ${parity}.`;
        }
    </script>
</body>
</html>
```

**1. document.getElementById — lab1_getElementById.html**
```html
<!DOCTYPE html>
<html lang='ru'>
<head>
    <meta charset='UTF-8'>
    <title>Метод: getElementById</title>
</head>
<body>
    <h2>Кредитный калькулятор (getElementById)</h2>
    
    <label>Сумма кредита:</label>
    <input type='number' id='amount' placeholder='100000'><br><br>
    
    <label>Процентная ставка (%):</label>
    <input type='number' id='rate' placeholder='12'><br><br>
    
    <label>Срок (месяцев):</label>
    <input type='number' id='months' placeholder='24'><br><br>
    
    <button onclick='calculate()'>Рассчитать</button><br><br>
    
    <label>Всего отдадите:</label>
    <input type='text' id='result' readonly>

    <script>
        function calculate() {
            let amount = document.getElementById('amount').value;
            let rate = document.getElementById('rate').value;
            let months = document.getElementById('months').value;
            
            if (amount === '' || rate === '' || months === '') {
                document.getElementById('result').value = 'Заполните все поля!';
                return;
            }
            
            let total = amount * (1 + rate / 100 * months / 12);
            document.getElementById('result').value = total.toFixed(2) + ' руб.';
        }
    </script>
</body>
</html>
```
**2. document.getElementsByName — lab1_getElementsByName.html**
```html
<!DOCTYPE html>
<html lang='ru'>
<head>
    <meta charset='UTF-8'>
    <title>Метод: getElementsByName</title>
</head>
<body>
    <h2>Кредитный калькулятор (getElementsByName)</h2>
    
    <label>Сумма кредита:</label>
    <input type='number' name='amount' placeholder='100000'><br><br>
    
    <label>Процентная ставка (%):</label>
    <input type='number' name='rate' placeholder='12'><br><br>
    
    <label>Срок (месяцев):</label>
    <input type='number' name='months' placeholder='24'><br><br>
    
    <button onclick='calculate()'>Рассчитать</button><br><br>
    
    <label>Всего отдадите:</label>
    <input type='text' name='result' readonly>

    <script>
        function calculate() {
            let amount = document.getElementsByName('amount')[0].value;
            let rate = document.getElementsByName('rate')[0].value;
            let months = document.getElementsByName('months')[0].value;
            
            if (amount === '' || rate === '' || months === '') {
                document.getElementsByName('result')[0].value = 'Заполните все поля!';
                return;
            }
            
            let total = amount * (1 + rate / 100 * months / 12);
            document.getElementsByName('result')[0].value = total.toFixed(2) + ' руб.';
        }
    </script>
</body>
</html>
```
**3. document.getElementsByClassName — lab1_getElementsByClassName.html**
```html
<!DOCTYPE html>
<html lang='ru'>
<head>
    <meta charset='UTF-8'>
    <title>Метод: getElementsByClassName</title>
</head>
<body>
    <h2>Кредитный калькулятор (getElementsByClassName)</h2>
    
    <label>Сумма кредита:</label>
    <input type='number' class='amount' placeholder='100000'><br><br>
    
    <label>Процентная ставка (%):</label>
    <input type='number' class='rate' placeholder='12'><br><br>
    
    <label>Срок (месяцев):</label>
    <input type='number' class='months' placeholder='24'><br><br>
    
    <button onclick='calculate()'>Рассчитать</button><br><br>
    
    <label>Всего отдадите:</label>
    <input type='text' class='result' readonly>

    <script>
        function calculate() {
            let amount = document.getElementsByClassName('amount')[0].value;
            let rate = document.getElementsByClassName('rate')[0].value;
            let months = document.getElementsByClassName('months')[0].value;
            
            if (amount === '' || rate === '' || months === '') {
                document.getElementsByClassName('result')[0].value = 'Заполните все поля!';
                return;
            }
            
            let total = amount * (1 + rate / 100 * months / 12);
            document.getElementsByClassName('result')[0].value = total.toFixed(2) + ' руб.';
        }
    </script>
</body>
</html>
```
**4. document.getElementsByTagName — lab1_getElementsByTagName.html**
```html
<!DOCTYPE html>
<html lang='ru'>
<head>
    <meta charset='UTF-8'>
    <title>Метод: getElementsByTagName</title>
</head>
<body>
    <h2>Кредитный калькулятор (getElementsByTagName)</h2>
    
    <label>Сумма кредита:</label>
    <input type='number' placeholder='100000'><br><br>
    
    <label>Процентная ставка (%):</label>
    <input type='number' placeholder='12'><br><br>
    
    <label>Срок (месяцев):</label>
    <input type='number' placeholder='24'><br><br>
    
    <button onclick='calculate()'>Рассчитать</button><br><br>
    
    <label>Всего отдадите:</label>
    <input type='text' readonly>

    <script>
        function calculate() {
            let inputs = document.getElementsByTagName('input');
            let amount = inputs[0].value;
            let rate = inputs[1].value;
            let months = inputs[2].value;
            
            if (amount === '' || rate === '' || months === '') {
                inputs[3].value = 'Заполните все поля!';
                return;
            }
            
            let total = amount * (1 + rate / 100 * months / 12);
            inputs[3].value = total.toFixed(2) + ' руб.';
        }
    </script>
</body>
</html>
```
**5. document.querySelector — lab1_querySelector.html**
```html
<!DOCTYPE html>
<html lang='ru'>
<head>
    <meta charset='UTF-8'>
    <title>Метод: querySelector</title>
</head>
<body>
    <h2>Кредитный калькулятор (querySelector)</h2>
    
    <label>Сумма кредита:</label>
    <input type='number' id='amount' placeholder='100000'><br><br>
    
    <label>Процентная ставка (%):</label>
    <input type='number' id='rate' placeholder='12'><br><br>
    
    <label>Срок (месяцев):</label>
    <input type='number' id='months' placeholder='24'><br><br>
    
    <button onclick='calculate()'>Рассчитать</button><br><br>
    
    <label>Всего отдадите:</label>
    <input type='text' id='result' readonly>

    <script>
        function calculate() {
            let amount = document.querySelector('#amount').value;
            let rate = document.querySelector('#rate').value;
            let months = document.querySelector('#months').value;
            
            if (amount === '' || rate === '' || months === '') {
                document.querySelector('#result').value = 'Заполните все поля!';
                return;
            }
            
            let total = amount * (1 + rate / 100 * months / 12);
            document.querySelector('#result').value = total.toFixed(2) + ' руб.';
        }
    </script>
</body>
</html>
```
**6. document.querySelectorAll — lab1_querySelectorAll.html**
```html
<!DOCTYPE html>
<html lang='ru'>
<head>
    <meta charset='UTF-8'>
    <title>Метод: querySelectorAll</title>
</head>
<body>
    <h2>Кредитный калькулятор (querySelectorAll)</h2>
    
    <label>Сумма кредита:</label>
    <input type='number' class='amount' placeholder='100000'><br><br>
    
    <label>Процентная ставка (%):</label>
    <input type='number' class='rate' placeholder='12'><br><br>
    
    <label>Срок (месяцев):</label>
    <input type='number' class='months' placeholder='24'><br><br>
    
    <button onclick='calculate()'>Рассчитать</button><br><br>
    
    <label>Всего отдадите:</label>
    <input type='text' class='result' readonly>

    <script>
        function calculate() {
            let amount = document.querySelectorAll('.amount')[0].value;
            let rate = document.querySelectorAll('.rate')[0].value;
            let months = document.querySelectorAll('.months')[0].value;
            
            if (amount === '' || rate === '' || months === '') {
                document.querySelectorAll('.result')[0].value = 'Заполните все поля!';
                return;
            }
            
            let total = amount * (1 + rate / 100 * months / 12);
            document.querySelectorAll('.result')[0].value = total.toFixed(2) + ' руб.';
        }
    </script>
</body>
</html>
```

```textВсе 6 кодов считают по формуле простых процентов: 
общая сумма = кредит × (1 + ставка/100 × срок/12). Результат выводится с двумя знаками после запятой.
```

**Основные различия методов:**

| Метод | Что возвращает | Как обращаемся к 4-му полю | Как обращаемся к результату |
|:------|:--------------|:--------------------------|:---------------------------|
| getElementById | Один элемент | `getElementById('num4')` | `getElementById('result')` |
| getElementsByName | "Живая" коллекция | `getElementsByName('numInput')[3]` | `getElementsByName('result')[0]` |
| getElementsByClassName | "Живая" коллекция | `getElementsByClassName('numInput')[3]` | `getElementsByClassName('result')[0]` |
| getElementsByTagName | "Живая" коллекция | `getElementsByTagName('input')[3]` | `getElementsByTagName('p')[0]` |
| querySelector | Один элемент (первый) | `querySelectorAll('.numInput')[3]` | `querySelector('.result')` |
| querySelectorAll | Статическая коллекция | `querySelectorAll('.numInput')[3]` | `querySelectorAll('.result')[0]` |



```html
<!DOCTYPE html>
<html lang="ru">
<head>
    <meta charset="UTF-8">
    <title>Все методы доступа к DOM</title>
    <style>
        body {
            font-family: Arial, sans-serif;
            max-width: 900px;
            margin: 20px auto;
            padding: 0 20px;
        }
        section {
            border: 1px solid #ccc;
            border-radius: 8px;
            padding: 15px;
            margin-bottom: 20px;
            background: #fafafa;
        }
        h2 {
            margin-top: 0;
            color: #333;
            font-size: 18px;
        }
        label {
            display: inline-block;
            width: 180px;
            margin-bottom: 5px;
        }
        input[type="number"] {
            width: 150px;
            padding: 4px;
        }
        input[type="text"][readonly] {
            width: 180px;
            padding: 4px;
            background: #eee;
            font-weight: bold;
        }
        button {
            padding: 6px 20px;
            cursor: pointer;
        }
    </style>
</head>
<body>

    <h1>Изучаем JS: 6 методов доступа к DOM</h1>
    <p>Кредитный калькулятор. Формула: <b>общая сумма = кредит × (1 + ставка/100 × срок/12)</b></p>

    <!-- 1. getElementById -->
    <section>
        <h2>1. document.getElementById(id)</h2>
        <label>Сумма кредита:</label>
        <input type="number" id="amount1" placeholder="100000"><br>
        <label>Процентная ставка (%):</label>
        <input type="number" id="rate1" placeholder="12"><br>
        <label>Срок (месяцев):</label>
        <input type="number" id="months1" placeholder="24"><br>
        <button id="calc1">Рассчитать</button><br><br>
        <label>Всего отдадите:</label>
        <input type="text" id="result1" readonly>
    </section>

    <!-- 2. getElementsByName -->
    <section>
        <h2>2. document.getElementsByName(name)</h2>
        <label>Сумма кредита:</label>
        <input type="number" name="amount2" placeholder="100000"><br>
        <label>Процентная ставка (%):</label>
        <input type="number" name="rate2" placeholder="12"><br>
        <label>Срок (месяцев):</label>
        <input type="number" name="months2" placeholder="24"><br>
        <button name="calc2">Рассчитать</button><br><br>
        <label>Всего отдадите:</label>
        <input type="text" name="result2" readonly>
    </section>

    <!-- 3. getElementsByClassName -->
    <section>
        <h2>3. document.getElementsByClassName(className)</h2>
        <label>Сумма кредита:</label>
        <input type="number" class="amount3" placeholder="100000"><br>
        <label>Процентная ставка (%):</label>
        <input type="number" class="rate3" placeholder="12"><br>
        <label>Срок (месяцев):</label>
        <input type="number" class="months3" placeholder="24"><br>
        <button class="calc3">Рассчитать</button><br><br>
        <label>Всего отдадите:</label>
        <input type="text" class="result3" readonly>
    </section>

    <!-- 4. getElementsByTagName -->
    <section>
        <h2>4. document.getElementsByTagName(tagName)</h2>
        <label>Сумма кредита:</label>
        <input type="number" placeholder="100000"><br>
        <label>Процентная ставка (%):</label>
        <input type="number" placeholder="12"><br>
        <label>Срок (месяцев):</label>
        <input type="number" placeholder="24"><br>
        <button>Рассчитать</button><br><br>
        <label>Всего отдадите:</label>
        <input type="text" readonly>
    </section>

    <!-- 5. querySelector -->
    <section>
        <h2>5. document.querySelector(selector)</h2>
        <label>Сумма кредита:</label>
        <input type="number" id="amount5" placeholder="100000"><br>
        <label>Процентная ставка (%):</label>
        <input type="number" id="rate5" placeholder="12"><br>
        <label>Срок (месяцев):</label>
        <input type="number" id="months5" placeholder="24"><br>
        <button id="calc5">Рассчитать</button><br><br>
        <label>Всего отдадите:</label>
        <input type="text" id="result5" readonly>
    </section>

    <!-- 6. querySelectorAll -->
    <section>
        <h2>6. document.querySelectorAll(selector)</h2>
        <label>Сумма кредита:</label>
        <input type="number" class="amount6" placeholder="100000"><br>
        <label>Процентная ставка (%):</label>
        <input type="number" class="rate6" placeholder="12"><br>
        <label>Срок (месяцев):</label>
        <input type="number" class="months6" placeholder="24"><br>
        <button class="calc6">Рассчитать</button><br><br>
        <label>Всего отдадите:</label>
        <input type="text" class="result6" readonly>
    </section>

    <script>
        // =============================================
        // 1. document.getElementById
        // =============================================
        document.getElementById('calc1').addEventListener('click', function() {
            let amount = document.getElementById('amount1').value;
            let rate = document.getElementById('rate1').value;
            let months = document.getElementById('months1').value;
            let resultField = document.getElementById('result1');

            if (amount === '' || rate === '' || months === '') {
                resultField.value = 'Заполните все поля!';
                return;
            }
            let total = amount * (1 + rate / 100 * months / 12);
            resultField.value = total.toFixed(2) + ' руб.';
        });

        // =============================================
        // 2. document.getElementsByName
        // =============================================
        document.getElementsByName('calc2')[0].addEventListener('click', function() {
            let amount = document.getElementsByName('amount2')[0].value;
            let rate = document.getElementsByName('rate2')[0].value;
            let months = document.getElementsByName('months2')[0].value;
            let resultField = document.getElementsByName('result2')[0];

            if (amount === '' || rate === '' || months === '') {
                resultField.value = 'Заполните все поля!';
                return;
            }
            let total = amount * (1 + rate / 100 * months / 12);
            resultField.value = total.toFixed(2) + ' руб.';
        });

        // =============================================
        // 3. document.getElementsByClassName
        // =============================================
        document.getElementsByClassName('calc3')[0].addEventListener('click', function() {
            let amount = document.getElementsByClassName('amount3')[0].value;
            let rate = document.getElementsByClassName('rate3')[0].value;
            let months = document.getElementsByClassName('months3')[0].value;
            let resultField = document.getElementsByClassName('result3')[0];

            if (amount === '' || rate === '' || months === '') {
                resultField.value = 'Заполните все поля!';
                return;
            }
            let total = amount * (1 + rate / 100 * months / 12);
            resultField.value = total.toFixed(2) + ' руб.';
        });

        // =============================================
        // 4. document.getElementsByTagName
        // =============================================
        // Ищем все <section>, берём 4-й (индекс 3), внутри него ищем input и button
        (function() {
            let sections = document.getElementsByTagName('section');
            let section4 = sections[3]; // 4-я секция (индекс 3)
            let inputs = section4.getElementsByTagName('input');
            let buttons = section4.getElementsByTagName('button');

            buttons[0].addEventListener('click', function() {
                let amount = inputs[0].value;
                let rate = inputs[1].value;
                let months = inputs[2].value;
                let resultField = inputs[3];

                if (amount === '' || rate === '' || months === '') {
                    resultField.value = 'Заполните все поля!';
                    return;
                }
                let total = amount * (1 + rate / 100 * months / 12);
                resultField.value = total.toFixed(2) + ' руб.';
            });
        })();

        // =============================================
        // 5. document.querySelector
        // =============================================
        document.querySelector('#calc5').addEventListener('click', function() {
            let amount = document.querySelector('#amount5').value;
            let rate = document.querySelector('#rate5').value;
            let months = document.querySelector('#months5').value;
            let resultField = document.querySelector('#result5');

            if (amount === '' || rate === '' || months === '') {
                resultField.value = 'Заполните все поля!';
                return;
            }
            let total = amount * (1 + rate / 100 * months / 12);
            resultField.value = total.toFixed(2) + ' руб.';
        });

        // =============================================
        // 6. document.querySelectorAll
        // =============================================
        document.querySelectorAll('.calc6')[0].addEventListener('click', function() {
            let amount = document.querySelectorAll('.amount6')[0].value;
            let rate = document.querySelectorAll('.rate6')[0].value;
            let months = document.querySelectorAll('.months6')[0].value;
            let resultField = document.querySelectorAll('.result6')[0];

            if (amount === '' || rate === '' || months === '') {
                resultField.value = 'Заполните все поля!';
                return;
            }
            let total = amount * (1 + rate / 100 * months / 12);
            resultField.value = total.toFixed(2) + ' руб.';
        });
    </script>

</body>
</html>
```

**Что сделано:**

- Все 6 методов работают независимо в своих секциях
- Ни в одном элементе HTML нет `onclick` или `onchange`
- Обработчики событий навешиваются через `addEventListener` в чистом JS
- Для `getElementsByTagName` использован дополнительный приём: сначала находим 4-ю секцию, а внутри неё ищем `input` и `button` по тегу — чтобы не затронуть элементы других секций
- Результат везде выводится по формуле: `кредит × (1 + ставка/100 × срок/12)` с двумя знаками после запятой

---

## Раздел 4: Кредитный калькулятор — отдельные файлы (addEventListener)

> Все 6 HTML-файлов без `onclick` и `onchange`. Обработчики навешиваются через `addEventListener` в JS. Формула: `сумма = кредит × (1 + ставка/100 × срок/12)`.

### 1. `document.getElementById(id)`

```html
<!DOCTYPE html>
<html lang="ru">
<head>
    <meta charset="UTF-8">
    <title>Метод: getElementById</title>
</head>
<body>

    <h2>Кредитный калькулятор (getElementById)</h2>

    <label>Сумма кредита:</label>
    <input type="number" id="amount" placeholder="100000"><br><br>

    <label>Процентная ставка (%):</label>
    <input type="number" id="rate" placeholder="12"><br><br>

    <label>Срок (месяцев):</label>
    <input type="number" id="months" placeholder="24"><br><br>

    <button id="calc">Рассчитать</button><br><br>

    <label>Всего отдадите:</label>
    <input type="text" id="result" readonly>

    <script>
        document.getElementById('calc').addEventListener('click', function() {
            let amount = document.getElementById('amount').value;
            let rate = document.getElementById('rate').value;
            let months = document.getElementById('months').value;
            let resultField = document.getElementById('result');

            if (amount === '' || rate === '' || months === '') {
                resultField.value = 'Заполните все поля!';
                return;
            }
            let total = amount * (1 + rate / 100 * months / 12);
            resultField.value = total.toFixed(2) + ' руб.';
        });
    </script>

</body>
</html>
```

### 2. `document.getElementsByName(name)`

```html
<!DOCTYPE html>
<html lang="ru">
<head>
    <meta charset="UTF-8">
    <title>Метод: getElementsByName</title>
</head>
<body>

    <h2>Кредитный калькулятор (getElementsByName)</h2>

    <label>Сумма кредита:</label>
    <input type="number" name="amount" placeholder="100000"><br><br>

    <label>Процентная ставка (%):</label>
    <input type="number" name="rate" placeholder="12"><br><br>

    <label>Срок (месяцев):</label>
    <input type="number" name="months" placeholder="24"><br><br>

    <button name="calc">Рассчитать</button><br><br>

    <label>Всего отдадите:</label>
    <input type="text" name="result" readonly>

    <script>
        document.getElementsByName('calc')[0].addEventListener('click', function() {
            let amount = document.getElementsByName('amount')[0].value;
            let rate = document.getElementsByName('rate')[0].value;
            let months = document.getElementsByName('months')[0].value;
            let resultField = document.getElementsByName('result')[0];

            if (amount === '' || rate === '' || months === '') {
                resultField.value = 'Заполните все поля!';
                return;
            }
            let total = amount * (1 + rate / 100 * months / 12);
            resultField.value = total.toFixed(2) + ' руб.';
        });
    </script>

</body>
</html>
```

### 3. `document.getElementsByClassName(className)`

```html
<!DOCTYPE html>
<html lang="ru">
<head>
    <meta charset="UTF-8">
    <title>Метод: getElementsByClassName</title>
</head>
<body>

    <h2>Кредитный калькулятор (getElementsByClassName)</h2>

    <label>Сумма кредита:</label>
    <input type="number" class="amount" placeholder="100000"><br><br>

    <label>Процентная ставка (%):</label>
    <input type="number" class="rate" placeholder="12"><br><br>

    <label>Срок (месяцев):</label>
    <input type="number" class="months" placeholder="24"><br><br>

    <button class="calc">Рассчитать</button><br><br>

    <label>Всего отдадите:</label>
    <input type="text" class="result" readonly>

    <script>
        document.getElementsByClassName('calc')[0].addEventListener('click', function() {
            let amount = document.getElementsByClassName('amount')[0].value;
            let rate = document.getElementsByClassName('rate')[0].value;
            let months = document.getElementsByClassName('months')[0].value;
            let resultField = document.getElementsByClassName('result')[0];

            if (amount === '' || rate === '' || months === '') {
                resultField.value = 'Заполните все поля!';
                return;
            }
            let total = amount * (1 + rate / 100 * months / 12);
            resultField.value = total.toFixed(2) + ' руб.';
        });
    </script>

</body>
</html>
```

### 4. `document.getElementsByTagName(tagName)`

```html
<!DOCTYPE html>
<html lang="ru">
<head>
    <meta charset="UTF-8">
    <title>Метод: getElementsByTagName</title>
</head>
<body>

    <h2>Кредитный калькулятор (getElementsByTagName)</h2>

    <label>Сумма кредита:</label>
    <input type="number" placeholder="100000"><br><br>

    <label>Процентная ставка (%):</label>
    <input type="number" placeholder="12"><br><br>

    <label>Срок (месяцев):</label>
    <input type="number" placeholder="24"><br><br>

    <button>Рассчитать</button><br><br>

    <label>Всего отдадите:</label>
    <input type="text" readonly>

    <script>
        let inputs = document.getElementsByTagName('input');
        let buttons = document.getElementsByTagName('button');

        buttons[0].addEventListener('click', function() {
            let amount = inputs[0].value;
            let rate = inputs[1].value;
            let months = inputs[2].value;
            let resultField = inputs[3];

            if (amount === '' || rate === '' || months === '') {
                resultField.value = 'Заполните все поля!';
                return;
            }
            let total = amount * (1 + rate / 100 * months / 12);
            resultField.value = total.toFixed(2) + ' руб.';
        });
    </script>

</body>
</html>
```

### 5. `document.querySelector(selector)`

```html
<!DOCTYPE html>
<html lang="ru">
<head>
    <meta charset="UTF-8">
    <title>Метод: querySelector</title>
</head>
<body>

    <h2>Кредитный калькулятор (querySelector)</h2>

    <label>Сумма кредита:</label>
    <input type="number" id="amount" placeholder="100000"><br><br>

    <label>Процентная ставка (%):</label>
    <input type="number" id="rate" placeholder="12"><br><br>

    <label>Срок (месяцев):</label>
    <input type="number" id="months" placeholder="24"><br><br>

    <button id="calc">Рассчитать</button><br><br>

    <label>Всего отдадите:</label>
    <input type="text" id="result" readonly>

    <script>
        document.querySelector('#calc').addEventListener('click', function() {
            let amount = document.querySelector('#amount').value;
            let rate = document.querySelector('#rate').value;
            let months = document.querySelector('#months').value;
            let resultField = document.querySelector('#result');

            if (amount === '' || rate === '' || months === '') {
                resultField.value = 'Заполните все поля!';
                return;
            }
            let total = amount * (1 + rate / 100 * months / 12);
            resultField.value = total.toFixed(2) + ' руб.';
        });
    </script>

</body>
</html>
```

### 6. `document.querySelectorAll(selector)`

```html
<!DOCTYPE html>
<html lang="ru">
<head>
    <meta charset="UTF-8">
    <title>Метод: querySelectorAll</title>
</head>
<body>

    <h2>Кредитный калькулятор (querySelectorAll)</h2>

    <label>Сумма кредита:</label>
    <input type="number" class="amount" placeholder="100000"><br><br>

    <label>Процентная ставка (%):</label>
    <input type="number" class="rate" placeholder="12"><br><br>

    <label>Срок (месяцев):</label>
    <input type="number" class="months" placeholder="24"><br><br>

    <button class="calc">Рассчитать</button><br><br>

    <label>Всего отдадите:</label>
    <input type="text" class="result" readonly>

    <script>
        document.querySelectorAll('.calc')[0].addEventListener('click', function() {
            let amount = document.querySelectorAll('.amount')[0].value;
            let rate = document.querySelectorAll('.rate')[0].value;
            let months = document.querySelectorAll('.months')[0].value;
            let resultField = document.querySelectorAll('.result')[0];

            if (amount === '' || rate === '' || months === '') {
                resultField.value = 'Заполните все поля!';
                return;
            }
            let total = amount * (1 + rate / 100 * months / 12);
            resultField.value = total.toFixed(2) + ' руб.';
        });
    </script>

</body>
</html>
```

**Сводная таблица методов доступа к DOM:**

| Метод | Что принимает | Что возвращает | Как обратиться к элементу |
|:------|:-------------|:--------------|:--------------------------|
| `getElementById` | `id` | один элемент | `getElementById('id')` |
| `getElementsByName` | `name` | живая коллекция | `getElementsByName('name')[индекс]` |
| `getElementsByClassName` | `class` | живая коллекция | `getElementsByClassName('class')[индекс]` |
| `getElementsByTagName` | тег | живая коллекция | `getElementsByTagName('tag')[индекс]` |
| `querySelector` | CSS-селектор | первый подходящий элемент | `querySelector('селектор')` |
| `querySelectorAll` | CSS-селектор | статическая коллекция | `querySelectorAll('селектор')[индекс]` |

> Все файлы полностью независимы, не используют `onclick`/`onchange`, обработчики навешиваются через `addEventListener`. Формула расчёта: `сумма = кредит × (1 + ставка/100 × срок/12)`.

---

## Раздел 5: Анализ числа — отдельные файлы (addEventListener)

> Та же задача (анализ числа: положительное/отрицательное, чётное/нечётное) для каждого из 6 методов. В HTML нет `onclick`, всё навешивается через `addEventListener`.

### 1. `document.getElementById(id)`

```html
<!DOCTYPE html>
<html lang="ru">
<head>
    <meta charset="UTF-8">
    <title>Метод: getElementById</title>
</head>
<body>

    <h2>Анализ числа (getElementById)</h2>

    <input type="number" id="num1" placeholder="Введите число 1">
    <input type="number" id="num2" placeholder="Введите число 2">
    <input type="number" id="num3" placeholder="Введите число 3">
    <input type="number" id="num4" placeholder="Введите число 4">

    <br><br>

    <button id="analyzeBtn">Анализировать 4-е число</button>

    <p id="result"></p>

    <script>
        document.getElementById('analyzeBtn').addEventListener('click', function() {
            let input = document.getElementById('num4').value;
            let num = Number(input);
            let resultField = document.getElementById('result');

            if (input === '' || isNaN(num)) {
                resultField.textContent = 'Ошибка: введите корректное число в 4-е поле!';
                return;
            }

            let sign = '';
            if (num > 0) {
                sign = 'положительное';
            } else if (num < 0) {
                sign = 'отрицательное';
            } else {
                sign = 'нулевое';
            }

            let parity = (num % 2 === 0) ? 'чётное' : 'нечётное';

            resultField.textContent = `Число ${num}: ${sign}, ${parity}.`;
        });
    </script>

</body>
</html>
```

### 2. `document.getElementsByName(name)`

```html
<!DOCTYPE html>
<html lang="ru">
<head>
    <meta charset="UTF-8">
    <title>Метод: getElementsByName</title>
</head>
<body>

    <h2>Анализ числа (getElementsByName)</h2>

    <input type="number" name="numInput" placeholder="Введите число 1">
    <input type="number" name="numInput" placeholder="Введите число 2">
    <input type="number" name="numInput" placeholder="Введите число 3">
    <input type="number" name="numInput" placeholder="Введите число 4">

    <br><br>

    <button name="analyzeBtn">Анализировать 4-е число</button>

    <p name="result"></p>

    <script>
        document.getElementsByName('analyzeBtn')[0].addEventListener('click', function() {
            let allInputs = document.getElementsByName('numInput');
            let input = allInputs[3].value;
            let num = Number(input);
            let resultField = document.getElementsByName('result')[0];

            if (input === '' || isNaN(num)) {
                resultField.textContent = 'Ошибка: введите корректное число в 4-е поле!';
                return;
            }

            let sign = '';
            if (num > 0) {
                sign = 'положительное';
            } else if (num < 0) {
                sign = 'отрицательное';
            } else {
                sign = 'нулевое';
            }

            let parity = (num % 2 === 0) ? 'чётное' : 'нечётное';

            resultField.textContent = `Число ${num}: ${sign}, ${parity}.`;
        });
    </script>

</body>
</html>
```

### 3. `document.getElementsByClassName(className)`

```html
<!DOCTYPE html>
<html lang="ru">
<head>
    <meta charset="UTF-8">
    <title>Метод: getElementsByClassName</title>
</head>
<body>

    <h2>Анализ числа (getElementsByClassName)</h2>

    <input type="number" class="numInput" placeholder="Введите число 1">
    <input type="number" class="numInput" placeholder="Введите число 2">
    <input type="number" class="numInput" placeholder="Введите число 3">
    <input type="number" class="numInput" placeholder="Введите число 4">

    <br><br>

    <button class="analyzeBtn">Анализировать 4-е число</button>

    <p class="result"></p>

    <script>
        document.getElementsByClassName('analyzeBtn')[0].addEventListener('click', function() {
            let allInputs = document.getElementsByClassName('numInput');
            let input = allInputs[3].value;
            let num = Number(input);
            let resultField = document.getElementsByClassName('result')[0];

            if (input === '' || isNaN(num)) {
                resultField.textContent = 'Ошибка: введите корректное число в 4-е поле!';
                return;
            }

            let sign = '';
            if (num > 0) {
                sign = 'положительное';
            } else if (num < 0) {
                sign = 'отрицательное';
            } else {
                sign = 'нулевое';
            }

            let parity = (num % 2 === 0) ? 'чётное' : 'нечётное';

            resultField.textContent = `Число ${num}: ${sign}, ${parity}.`;
        });
    </script>

</body>
</html>
```

### 4. `document.getElementsByTagName(tagName)`

```html
<!DOCTYPE html>
<html lang="ru">
<head>
    <meta charset="UTF-8">
    <title>Метод: getElementsByTagName</title>
</head>
<body>

    <h2>Анализ числа (getElementsByTagName)</h2>

    <input type="number" placeholder="Введите число 1">
    <input type="number" placeholder="Введите число 2">
    <input type="number" placeholder="Введите число 3">
    <input type="number" placeholder="Введите число 4">

    <br><br>

    <button>Анализировать 4-е число</button>

    <p></p>

    <script>
        let allInputs = document.getElementsByTagName('input');
        let buttons = document.getElementsByTagName('button');
        let paragraphs = document.getElementsByTagName('p');

        buttons[0].addEventListener('click', function() {
            let input = allInputs[3].value;
            let num = Number(input);
            let resultField = paragraphs[0];

            if (input === '' || isNaN(num)) {
                resultField.textContent = 'Ошибка: введите корректное число в 4-е поле!';
                return;
            }

            let sign = '';
            if (num > 0) {
                sign = 'положительное';
            } else if (num < 0) {
                sign = 'отрицательное';
            } else {
                sign = 'нулевое';
            }

            let parity = (num % 2 === 0) ? 'чётное' : 'нечётное';

            resultField.textContent = `Число ${num}: ${sign}, ${parity}.`;
        });
    </script>

</body>
</html>
```

### 5. `document.querySelector(selector)`

```html
<!DOCTYPE html>
<html lang="ru">
<head>
    <meta charset="UTF-8">
    <title>Метод: querySelector</title>
</head>
<body>

    <h2>Анализ числа (querySelector)</h2>

    <input type="number" class="numInput" placeholder="Введите число 1">
    <input type="number" class="numInput" placeholder="Введите число 2">
    <input type="number" class="numInput" placeholder="Введите число 3">
    <input type="number" class="numInput" placeholder="Введите число 4">

    <br><br>

    <button class="analyzeBtn">Анализировать 4-е число</button>

    <p class="result"></p>

    <script>
        document.querySelector('.analyzeBtn').addEventListener('click', function() {
            let allInputs = document.querySelectorAll('.numInput');
            let input = allInputs[3].value;
            let num = Number(input);
            let resultField = document.querySelector('.result');

            if (input === '' || isNaN(num)) {
                resultField.textContent = 'Ошибка: введите корректное число в 4-е поле!';
                return;
            }

            let sign = '';
            if (num > 0) {
                sign = 'положительное';
            } else if (num < 0) {
                sign = 'отрицательное';
            } else {
                sign = 'нулевое';
            }

            let parity = (num % 2 === 0) ? 'чётное' : 'нечётное';

            resultField.textContent = `Число ${num}: ${sign}, ${parity}.`;
        });
    </script>

</body>
</html>
```

### 6. `document.querySelectorAll(selector)`

```html
<!DOCTYPE html>
<html lang="ru">
<head>
    <meta charset="UTF-8">
    <title>Метод: querySelectorAll</title>
</head>
<body>

    <h2>Анализ числа (querySelectorAll)</h2>

    <input type="number" class="numInput" placeholder="Введите число 1">
    <input type="number" class="numInput" placeholder="Введите число 2">
    <input type="number" class="numInput" placeholder="Введите число 3">
    <input type="number" class="numInput" placeholder="Введите число 4">

    <br><br>

    <button class="analyzeBtn">Анализировать 4-е число</button>

    <p class="result"></p>

    <script>
        document.querySelectorAll('.analyzeBtn')[0].addEventListener('click', function() {
            let allInputs = document.querySelectorAll('.numInput');
            let input = allInputs[3].value;
            let num = Number(input);
            let resultField = document.querySelectorAll('.result')[0];

            if (input === '' || isNaN(num)) {
                resultField.textContent = 'Ошибка: введите корректное число в 4-е поле!';
                return;
            }

            let sign = '';
            if (num > 0) {
                sign = 'положительное';
            } else if (num < 0) {
                sign = 'отрицательное';
            } else {
                sign = 'нулевое';
            }

            let parity = (num % 2 === 0) ? 'чётное' : 'нечётное';

            resultField.textContent = `Число ${num}: ${sign}, ${parity}.`;
        });
    </script>

</body>
</html>
```

**Таблица выполненных вариантов (12 файлов):**

| # | Задача | Метод |
|:--|:-------|:------|
| 1 | Кредитный калькулятор | `getElementById` |
| 2 | Кредитный калькулятор | `getElementsByName` |
| 3 | Кредитный калькулятор | `getElementsByClassName` |
| 4 | Кредитный калькулятор | `getElementsByTagName` |
| 5 | Кредитный калькулятор | `querySelector` |
| 6 | Кредитный калькулятор | `querySelectorAll` |
| 7 | Анализ числа | `getElementById` |
| 8 | Анализ числа | `getElementsByName` |
| 9 | Анализ числа | `getElementsByClassName` |
| 10 | Анализ числа | `getElementsByTagName` |
| 11 | Анализ числа | `querySelector` |
| 12 | Анализ числа | `querySelectorAll` |

> Все файлы чистые: ни одного `onclick` в HTML, только `addEventListener` в JS.

---

## Раздел 6: Конвертер валют — отдельные файлы (addEventListener)

> 6 новых вариантов с задачей «конвертер валют (рубли → доллары по курсу)». В HTML нет `onclick`, всё через `addEventListener`. Формула: `доллары = рубли / курс`.

### 1. `document.getElementById(id)`

```html
<!DOCTYPE html>
<html lang="ru">
<head>
    <meta charset="UTF-8">
    <title>Метод: getElementById</title>
</head>
<body>

    <h2>Конвертер валют (getElementById)</h2>

    <label>Сумма в рублях:</label>
    <input type="number" id="rubles" placeholder="1000"><br><br>

    <label>Курс доллара (₽):</label>
    <input type="number" id="exchangeRate" placeholder="90"><br><br>

    <button id="convertBtn">Конвертировать</button><br><br>

    <label>Сумма в долларах:</label>
    <input type="text" id="dollars" readonly>

    <script>
        document.getElementById('convertBtn').addEventListener('click', function() {
            let rubles = document.getElementById('rubles').value;
            let rate = document.getElementById('exchangeRate').value;
            let resultField = document.getElementById('dollars');

            if (rubles === '' || rate === '' || Number(rate) <= 0) {
                resultField.value = 'Заполните все поля корректно!';
                return;
            }

            let dollars = rubles / rate;
            resultField.value = '$' + dollars.toFixed(2);
        });
    </script>

</body>
</html>
```

### 2. `document.getElementsByName(name)`

```html
<!DOCTYPE html>
<html lang="ru">
<head>
    <meta charset="UTF-8">
    <title>Метод: getElementsByName</title>
</head>
<body>

    <h2>Конвертер валют (getElementsByName)</h2>

    <label>Сумма в рублях:</label>
    <input type="number" name="rubles" placeholder="1000"><br><br>

    <label>Курс доллара (₽):</label>
    <input type="number" name="exchangeRate" placeholder="90"><br><br>

    <button name="convertBtn">Конвертировать</button><br><br>

    <label>Сумма в долларах:</label>
    <input type="text" name="dollars" readonly>

    <script>
        document.getElementsByName('convertBtn')[0].addEventListener('click', function() {
            let rubles = document.getElementsByName('rubles')[0].value;
            let rate = document.getElementsByName('exchangeRate')[0].value;
            let resultField = document.getElementsByName('dollars')[0];

            if (rubles === '' || rate === '' || Number(rate) <= 0) {
                resultField.value = 'Заполните все поля корректно!';
                return;
            }

            let dollars = rubles / rate;
            resultField.value = '$' + dollars.toFixed(2);
        });
    </script>

</body>
</html>
```

### 3. `document.getElementsByClassName(className)`

```html
<!DOCTYPE html>
<html lang="ru">
<head>
    <meta charset="UTF-8">
    <title>Метод: getElementsByClassName</title>
</head>
<body>

    <h2>Конвертер валют (getElementsByClassName)</h2>

    <label>Сумма в рублях:</label>
    <input type="number" class="rubles" placeholder="1000"><br><br>

    <label>Курс доллара (₽):</label>
    <input type="number" class="exchangeRate" placeholder="90"><br><br>

    <button class="convertBtn">Конвертировать</button><br><br>

    <label>Сумма в долларах:</label>
    <input type="text" class="dollars" readonly>

    <script>
        document.getElementsByClassName('convertBtn')[0].addEventListener('click', function() {
            let rubles = document.getElementsByClassName('rubles')[0].value;
            let rate = document.getElementsByClassName('exchangeRate')[0].value;
            let resultField = document.getElementsByClassName('dollars')[0];

            if (rubles === '' || rate === '' || Number(rate) <= 0) {
                resultField.value = 'Заполните все поля корректно!';
                return;
            }

            let dollars = rubles / rate;
            resultField.value = '$' + dollars.toFixed(2);
        });
    </script>

</body>
</html>
```

### 4. `document.getElementsByTagName(tagName)`

```html
<!DOCTYPE html>
<html lang="ru">
<head>
    <meta charset="UTF-8">
    <title>Метод: getElementsByTagName</title>
</head>
<body>

    <h2>Конвертер валют (getElementsByTagName)</h2>

    <label>Сумма в рублях:</label>
    <input type="number" placeholder="1000"><br><br>

    <label>Курс доллара (₽):</label>
    <input type="number" placeholder="90"><br><br>

    <button>Конвертировать</button><br><br>

    <label>Сумма в долларах:</label>
    <input type="text" readonly>

    <script>
        let inputs = document.getElementsByTagName('input');
        let buttons = document.getElementsByTagName('button');

        buttons[0].addEventListener('click', function() {
            let rubles = inputs[0].value;
            let rate = inputs[1].value;
            let resultField = inputs[2];

            if (rubles === '' || rate === '' || Number(rate) <= 0) {
                resultField.value = 'Заполните все поля корректно!';
                return;
            }

            let dollars = rubles / rate;
            resultField.value = '$' + dollars.toFixed(2);
        });
    </script>

</body>
</html>
```

### 5. `document.querySelector(selector)`

```html
<!DOCTYPE html>
<html lang="ru">
<head>
    <meta charset="UTF-8">
    <title>Метод: querySelector</title>
</head>
<body>

    <h2>Конвертер валют (querySelector)</h2>

    <label>Сумма в рублях:</label>
    <input type="number" id="rubles" placeholder="1000"><br><br>

    <label>Курс доллара (₽):</label>
    <input type="number" id="exchangeRate" placeholder="90"><br><br>

    <button id="convertBtn">Конвертировать</button><br><br>

    <label>Сумма в долларах:</label>
    <input type="text" id="dollars" readonly>

    <script>
        document.querySelector('#convertBtn').addEventListener('click', function() {
            let rubles = document.querySelector('#rubles').value;
            let rate = document.querySelector('#exchangeRate').value;
            let resultField = document.querySelector('#dollars');

            if (rubles === '' || rate === '' || Number(rate) <= 0) {
                resultField.value = 'Заполните все поля корректно!';
                return;
            }

            let dollars = rubles / rate;
            resultField.value = '$' + dollars.toFixed(2);
        });
    </script>

</body>
</html>
```

### 6. `document.querySelectorAll(selector)`

```html
<!DOCTYPE html>
<html lang="ru">
<head>
    <meta charset="UTF-8">
    <title>Метод: querySelectorAll</title>
</head>
<body>

    <h2>Конвертер валют (querySelectorAll)</h2>

    <label>Сумма в рублях:</label>
    <input type="number" class="rubles" placeholder="1000"><br><br>

    <label>Курс доллара (₽):</label>
    <input type="number" class="exchangeRate" placeholder="90"><br><br>

    <button class="convertBtn">Конвертировать</button><br><br>

    <label>Сумма в долларах:</label>
    <input type="text" class="dollars" readonly>

    <script>
        document.querySelectorAll('.convertBtn')[0].addEventListener('click', function() {
            let rubles = document.querySelectorAll('.rubles')[0].value;
            let rate = document.querySelectorAll('.exchangeRate')[0].value;
            let resultField = document.querySelectorAll('.dollars')[0];

            if (rubles === '' || rate === '' || Number(rate) <= 0) {
                resultField.value = 'Заполните все поля корректно!';
                return;
            }

            let dollars = rubles / rate;
            resultField.value = '$' + dollars.toFixed(2);
        });
    </script>

</body>
</html>
```

**Итоговая таблица всех вариантов (18 файлов):**

| # | Задача | Метод |
|:--|:-------|:------|
| 1 | Кредитный калькулятор | `getElementById` |
| 2 | Кредитный калькулятор | `getElementsByName` |
| 3 | Кредитный калькулятор | `getElementsByClassName` |
| 4 | Кредитный калькулятор | `getElementsByTagName` |
| 5 | Кредитный калькулятор | `querySelector` |
| 6 | Кредитный калькулятор | `querySelectorAll` |
| 7 | Анализ числа | `getElementById` |
| 8 | Анализ числа | `getElementsByName` |
| 9 | Анализ числа | `getElementsByClassName` |
| 10 | Анализ числа | `getElementsByTagName` |
| 11 | Анализ числа | `querySelector` |
| 12 | Анализ числа | `querySelectorAll` |
| 13 | Конвертер валют | `getElementById` |
| 14 | Конвертер валют | `getElementsByName` |
| 15 | Конвертер валют | `getElementsByClassName` |
| 16 | Конвертер валют | `getElementsByTagName` |
| 17 | Конвертер валют | `querySelector` |
| 18 | Конвертер валют | `querySelectorAll` |

> Формула конвертера: `доллары = рубли / курс`. Все файлы без `onclick`, только `addEventListener` в JS.

---

## Раздел 7: Сокращённые версии JS (стрелочные функции и тернарные операторы)

> Те же 6 методов для «Анализа числа» с компактной записью JS: переменные вне обработчика, стрелочные функции, тернарные операторы. Никаких `onclick` в HTML.

### 1. `document.getElementById(id)` — коротко

```html
<!DOCTYPE html>
<html lang="ru">
<head>
    <meta charset="UTF-8">
    <title>getElementById (коротко)</title>
</head>
<body>

    <h2>Анализ числа (getElementById)</h2>

    <input type="number" id="num1" placeholder="Число 1">
    <input type="number" id="num2" placeholder="Число 2">
    <input type="number" id="num3" placeholder="Число 3">
    <input type="number" id="num4" placeholder="Число 4">

    <br><br>

    <button id="btn">Анализировать 4-е число</button>
    <p id="out"></p>

    <script>
        const num4 = document.getElementById('num4');
        const btn = document.getElementById('btn');
        const out = document.getElementById('out');

        btn.addEventListener('click', () => {
            let n = +num4.value;
            out.textContent = (num4.value === '' || isNaN(n))
                ? 'Ошибка!'
                : `Число ${n}: ${n > 0 ? 'положительное' : n < 0 ? 'отрицательное' : 'нулевое'}, ${n % 2 === 0 ? 'чётное' : 'нечётное'}.`;
        });
    </script>

</body>
</html>
```

### 2. `document.getElementsByName(name)` — коротко

```html
<!DOCTYPE html>
<html lang="ru">
<head>
    <meta charset="UTF-8">
    <title>getElementsByName (коротко)</title>
</head>
<body>

    <h2>Анализ числа (getElementsByName)</h2>

    <input type="number" name="num" placeholder="Число 1">
    <input type="number" name="num" placeholder="Число 2">
    <input type="number" name="num" placeholder="Число 3">
    <input type="number" name="num" placeholder="Число 4">

    <br><br>

    <button name="btn">Анализировать 4-е число</button>
    <p name="out"></p>

    <script>
        const nums = document.getElementsByName('num');
        const btn = document.getElementsByName('btn')[0];
        const out = document.getElementsByName('out')[0];

        btn.addEventListener('click', () => {
            let n = +nums[3].value;
            out.textContent = (nums[3].value === '' || isNaN(n))
                ? 'Ошибка!'
                : `Число ${n}: ${n > 0 ? 'положительное' : n < 0 ? 'отрицательное' : 'нулевое'}, ${n % 2 === 0 ? 'чётное' : 'нечётное'}.`;
        });
    </script>

</body>
</html>
```

### 3. `document.getElementsByClassName(className)` — коротко

```html
<!DOCTYPE html>
<html lang="ru">
<head>
    <meta charset="UTF-8">
    <title>getElementsByClassName (коротко)</title>
</head>
<body>

    <h2>Анализ числа (getElementsByClassName)</h2>

    <input type="number" class="num" placeholder="Число 1">
    <input type="number" class="num" placeholder="Число 2">
    <input type="number" class="num" placeholder="Число 3">
    <input type="number" class="num" placeholder="Число 4">

    <br><br>

    <button class="btn">Анализировать 4-е число</button>
    <p class="out"></p>

    <script>
        const nums = document.getElementsByClassName('num');
        const btn = document.getElementsByClassName('btn')[0];
        const out = document.getElementsByClassName('out')[0];

        btn.addEventListener('click', () => {
            let n = +nums[3].value;
            out.textContent = (nums[3].value === '' || isNaN(n))
                ? 'Ошибка!'
                : `Число ${n}: ${n > 0 ? 'положительное' : n < 0 ? 'отрицательное' : 'нулевое'}, ${n % 2 === 0 ? 'чётное' : 'нечётное'}.`;
        });
    </script>

</body>
</html>
```

### 4. `document.getElementsByTagName(tagName)` — коротко

```html
<!DOCTYPE html>
<html lang="ru">
<head>
    <meta charset="UTF-8">
    <title>getElementsByTagName (коротко)</title>
</head>
<body>

    <h2>Анализ числа (getElementsByTagName)</h2>

    <input type="number" placeholder="Число 1">
    <input type="number" placeholder="Число 2">
    <input type="number" placeholder="Число 3">
    <input type="number" placeholder="Число 4">

    <br><br>

    <button>Анализировать 4-е число</button>
    <p></p>

    <script>
        const inputs = document.getElementsByTagName('input');
        const btn = document.getElementsByTagName('button')[0];
        const out = document.getElementsByTagName('p')[0];

        btn.addEventListener('click', () => {
            let n = +inputs[3].value;
            out.textContent = (inputs[3].value === '' || isNaN(n))
                ? 'Ошибка!'
                : `Число ${n}: ${n > 0 ? 'положительное' : n < 0 ? 'отрицательное' : 'нулевое'}, ${n % 2 === 0 ? 'чётное' : 'нечётное'}.`;
        });
    </script>

</body>
</html>
```

### 5. `document.querySelector(selector)` — коротко

```html
<!DOCTYPE html>
<html lang="ru">
<head>
    <meta charset="UTF-8">
    <title>querySelector (коротко)</title>
</head>
<body>

    <h2>Анализ числа (querySelector)</h2>

    <input type="number" class="num" placeholder="Число 1">
    <input type="number" class="num" placeholder="Число 2">
    <input type="number" class="num" placeholder="Число 3">
    <input type="number" class="num" placeholder="Число 4">

    <br><br>

    <button class="btn">Анализировать 4-е число</button>
    <p class="out"></p>

    <script>
        const nums = document.querySelectorAll('.num');
        const btn = document.querySelector('.btn');
        const out = document.querySelector('.out');

        btn.addEventListener('click', () => {
            let n = +nums[3].value;
            out.textContent = (nums[3].value === '' || isNaN(n))
                ? 'Ошибка!'
                : `Число ${n}: ${n > 0 ? 'положительное' : n < 0 ? 'отрицательное' : 'нулевое'}, ${n % 2 === 0 ? 'чётное' : 'нечётное'}.`;
        });
    </script>

</body>
</html>
```

### 6. `document.querySelectorAll(selector)` — коротко

```html
<!DOCTYPE html>
<html lang="ru">
<head>
    <meta charset="UTF-8">
    <title>querySelectorAll (коротко)</title>
</head>
<body>

    <h2>Анализ числа (querySelectorAll)</h2>

    <input type="number" class="num" placeholder="Число 1">
    <input type="number" class="num" placeholder="Число 2">
    <input type="number" class="num" placeholder="Число 3">
    <input type="number" class="num" placeholder="Число 4">

    <br><br>

    <button class="btn">Анализировать 4-е число</button>
    <p class="out"></p>

    <script>
        const nums = document.querySelectorAll('.num');
        const btn = document.querySelectorAll('.btn')[0];
        const out = document.querySelectorAll('.out')[0];

        btn.addEventListener('click', () => {
            let n = +nums[3].value;
            out.textContent = (nums[3].value === '' || isNaN(n))
                ? 'Ошибка!'
                : `Число ${n}: ${n > 0 ? 'положительное' : n < 0 ? 'отрицательное' : 'нулевое'}, ${n % 2 === 0 ? 'чётное' : 'нечётное'}.`;
        });
    </script>

</body>
</html>
```

**Что сокращено:**
---
| Было | Стало |
|:-----|:------|
| `function() { ... }` | `() => { ... }` |
| `Number(num)` | `+num` |
| `if...else if...else` (3 блока) | Вложенный тернарный оператор |
| `if...else` для чётности | Тернарный оператор |
| `document.getElementById('x').value` внутри обработчика | Переменная объявлена заранее вне обработчика |
| Многострочный `if` с проверкой | Тернарный оператор в одну строку |
---
> Все файлы без `onclick`, только `addEventListener` в чистом JS.
