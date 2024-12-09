# РАСЧЁТНАЯ РАБОТА

## Задание РР
5.28 (нг,си): Найти звёзды с заданным числом листьев

---

## Алгоритм выполнения задания

1. **Создание структуры графа**
- Определение структуры графа с использованием списка смежности;
- Реализация метода для добавления ребра между двумя вершинами.

2. **Поиск звёзд с заданным числом листьев**
- Итерация по всем вершинам графа;
- Проверка, что число соседей вершины больше или равно заданному числу листьев;
- Поиск всех листьев (соседние вершины с одним ребром) для данной вершины;
- Добавление вершины и первых найденных листьев в результат при условии, что число листьев больше или равно заданному числу.

3. **Главная программа**
- Создание экземпляра графа;
- Запрос у пользователя количества рёбер с проверкой на неравенство нулю;
- Вывод сообщения о пустом графе и завершение программы при нулевом количестве рёбер;
- Запрос у пользователя ввода рёбер и добавление их в граф;
- Запрос у пользователя заданного числа листьев.

4. **Поиск и вывод звёзд**
- Поиск звёзд с заданным числом листьев;
- Вывод информации о каждой звезде с указанием центра и листьев при наличии совпадений;
- Вывод сообщения о ненахождении совпадений.

## Описание кода

### Ключевые элементы кода на языке C++

1. **Подключение стандартных библиотек:**
   - `iostream` — для ввода и вывода данных через консоль;
   - `vector` — для хранения списков смежности;
   - `unordered_map` — для представления графа через списки смежности;
   - `sstream` — для парсинга пользовательского ввода рёбер.
   
     <img src="https://i.ibb.co/f0wh4fH/FE09-B931-9-ED2-4017-BD29-D5-D71115-CD10.png" width="200" />
   
2. **Структура `Graph`:**
   - Используется для представления графа через списки смежности;
   - Содержит метод `addEdge()`, который добавляет неориентированные рёбра между вершинами \(u\) и \(v\);
   
     <img src="https://i.ibb.co/C0sKfT6/20-C43-D35-61-E0-49-B3-BA7-C-9-B46807-E9579.png" width="400" />
     
3. **Функция `findStars(Graph& graph, int k)`:**
   - Принимает граф и заданное число листьев \(k\);
   - Для каждой вершины проверяет, имеет ли она хотя бы \(k\) листьев;
   - Возвращает вектор пар, где каждая пара содержит центр "звезды" и её листья. 
   
     <img src="https://i.ibb.co/9tdy5gT/08578-E7-E-FA20-4333-B7-E4-FD733-AF2-E274.png" width="700" />
 
4. **Функция `main()`:**
   - Читает ввод пользователя:
     - Количество рёбер;
     - Список рёбер в формате `u v`;
     - Заданное число листьев \(k\);
   - Ищет "звёзды" в графе с использованием функции `findStars`;
   - Выводит найденные "звёзды" в консоль.
   
     <img src="https://i.ibb.co/9tVR3RK/9-C185394-B9-AB-41-B4-BD0-E-62982-F252-AB5.png" width="700" />

## Пример выполнения задачи
<img src="https://i.ibb.co/MZ0JHY0/46959-D1-D-DBB8-45-B9-A1-FC-F4-C7-DFBE7-A83.png" width="600" />

## Вывод
Программа эффективно решает задачу поиска "звёзд" в неориентированном графе с заданным числом листьев 𝑘, используя списки смежности и итеративный перебор соседних вершин.

