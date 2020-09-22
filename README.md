## Условия

Данное задание разработано АйТи-бюро «Зебра» для проверки уровня и сроков исполнения работ. Данная работа не оплачивается и не представляет коммерческой ценности для АйТи-бюро «Зебра». АйТи-бюро «Зебра» не принимает претензии от участников и не комментирует принятые решения.

## Команды

- `npm i` - установка пакетов
- `gulp build` - сборка фронта
- `gulp` - сборка фронта и отслеживание изменений

## Макет

[Figma](https://www.figma.com/file/uOILcSVyOalI3qHhTIyRbU/Tasks?node-id=317%3A956)

Чтобы полноценно работать с макетом нужно авторизоваться под свои аккаунтом в Figma (или завести его). Если возникнут проблемы - написать автору задания.

## Задачи

### 2. Список

В Figma есть отрисованный макет списка новостей для desktop и mobile версии (Dynamic lists и Dynamic lists mobile)

Логика работы функционала:  
При первой загрузке страницы мы отсылаем AJAX запрос на обработчик ([#1](https://my-json-server.typicode.com/bigfootdary/json-news/news)) и получаем данные в виде JSON. Эти данные мы обрабатываем и выводим новости на страницу. Если есть возможность загрузить следующую страницу, то появляется кнопка "Загрузить еще".

При работе с фильтром (поле "Поиск") мы также отсылаем запрос на обработчик (уже [#2](https://my-json-server.typicode.com/bigfootdary/json-news/news-filtered)), и также по аналогии обрабатываем. При изменении фильтра все новости должны заменяться на странице.

При работе с кнопкой "Загрузить еще" мы загружаем следующую "страницу" данных, пока не загрузим все доступные страницы (параметр total). Когда загрузили все страницы - кнопка исчезает, для теста можно использовать [#3](https://my-json-server.typicode.com/bigfootdary/json-news/news-last-page). Данные при загрузке новой страницы должны вставлятся после последней отрендеренной новости, не удаляя уже выведенных новостей.

Также необходимо обработать ситуацию (обработчик [#4](https://my-json-server.typicode.com/bigfootdary/json-news/news-not-found)), когда данных нет. Можно вывести вместо плиток новостей произвольных текст ошибки.

### 3. Схема

Макет в Figma - SVG

В рамках задачи нужно реализовать интерактивную векторную схему. На макете отрисовано состояние hover на цветной квадрат. Хранение содержимого попапа значения не имеет.

## Требования

Работаем в рамках сборщика. Допускается (но не желательна) установка дополнительных библиотек.

### Браузеры

Chrome, FF, Opera, Safari - последние 3 версии. IE10+

## Примечание

Верстаем только то, что отрисовано в макете. Прорабатывать состояния всех элементов, если они не отрисованы, не нужно. Все вопросы пишем мне ответным сообщением.
