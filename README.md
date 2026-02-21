# Async Operation Demo (Node.js)

## Опис

Цей проєкт демонструє порядок виконання асинхронних операцій у Node.js
за допомогою:

-   process.nextTick
-   setImmediate
-   setTimeout

Функція asyncOperationDemo ілюструє роботу Event Loop та порядок
виконання мікро- і макротасків.

## Мета роботи

-   Зрозуміти різницю між nextTick, setImmediate та setTimeout
-   Побачити реальний порядок їх виконання
-   Навчитися тестувати асинхронний код за допомогою Vitest
-   Попрактикувати використання ES Modules
-   Додати кольорове логування через chalk

## Технології

-   Node.js
-   ES Modules (type: module)
-   Vitest
-   Chalk

## Встановлення

``` bash
npm install
```

Якщо потрібно окремо встановити кольори:

``` bash
npm install chalk
```

## Запуск

### Запуск файлу вручну:

``` bash
node src/main.js
```

### Запуск тестів:

``` bash
npm test
```

## Очікуваний порядок виконання

1.  Перший виклик (синхронний код)
2.  Останній виклик (синхронний код)
3.  nextTick
4.  setImmediate
5.  setTimeout

Порядок викликів callback:

    ['nextTick', 'setImmediate', 'setTimeout']

## Структура проєкту

    src/
     ├── main.js
     └── __test__/
          └── task1.test.js
