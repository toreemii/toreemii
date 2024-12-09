# РАСЧЁТНАЯ РАБОТА

## Задание РР
5.28 (нг,си): Найти звёзды с заданным числом листьев

---

## Описание кода и алгоритма

### Ключевые элементы кода на языке C++

1. **Подключение стандартных библиотек:**
   - `iostream` — для ввода и вывода данных через консоль.
   - `vector` — для хранения списков смежности.
   - `unordered_map` — для представления графа через списки смежности.
   - `sstream` — для парсинга пользовательского ввода рёбер.
   
   <img src="https://i.ibb.co/f0wh4fH/FE09-B931-9-ED2-4017-BD29-D5-D71115-CD10.png" width="200" />
   
2. **Структура `Graph`:**
   - Используется для представления графа через списки смежности.
   - Содержит метод `addEdge()`, который добавляет неориентированные рёбра между вершинами \(u\) и \(v\).

3. **Функция `findStars(Graph& graph, int k)`:**
   - Принимает граф и заданное число листьев \(k\).
   - Для каждой вершины проверяет, имеет ли она хотя бы \(k\) листьев.
   - Возвращает вектор пар, где каждая пара содержит центр "звезды" и её листья.

4. **Функция `main()`:**
   - Читает ввод пользователя:
     - Количество рёбер.
     - Список рёбер в формате `u v`.
     - Заданное число листьев \(k\).
   - Ищет "звёзды" в графе с использованием функции `findStars`.
   - Выводит найденные "звёзды" в консоль.

---

## Пример использования

### Пример входных данных

