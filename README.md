# Gamedev Job Interview Task

## Тестовое задание

### Задача

Есть множество (массив, где порядок не важен) целых чисел в диапазоне от 1 до 300. 
Количество чисел - до 1000. Напишите функцию сериализации / десериализации в строку, чтобы итоговая строка была компактной.
Цель задачи - максимально сжать данные относительно простой сериализации без алгоритма сжатия (хотя бы 50% в среднем). 
Сериализованная строка должна содержать только ASCII символы. Можно использовать любой язык программирования.
Вместе с решением нужно прислать набор тестов  - исходная строка, сжатая строка, коэффициент сжатия.
Примеры тестов: простейшие короткие, случайные - 50 чисел, 100 чисел, 500 чисел, 1000 чисел, граничные - все числа 1 знака, все числа из 2х знаков, все числа из 3х знаков, каждого числа по 3 - всего чисел 900.

### Решение

Число сериализируется последовательностью из одного или двух символов [d1]d0, где d1: 0..51 ('A'..'Z','a'..'z'), d2: 0..9 ('0'..'9'). Максимальное значение целого d1d0 - 1 = 520 - 1 = 519. Таблицы кодировки d1 и d0 не пересекающиеся, поэтому при сериализации последовательности целых чисел отсутствует необходимость в символе-разделителе.

### Язык программирования

python 2.7.17

### Использование

python serialize_numbers.py arg, где arg - список чисел, разделенных пробелами

