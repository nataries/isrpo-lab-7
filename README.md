# Лабораторная работа №7. Адаптивная верстка: Flexbox

Цель работы: освоить современные технологии CSS-разметки — Flexbox.

**Flexbox** — одномерная система компоновки для размещения элементов в строку или столбец.

## Flex-контейнер

Flex-контейнер выстраивает элементы в одну строку. Это является поведением flex-direction, в котором row стоит по умолчанию. Создать flex-контейнер можно, написав следующий код:

```
.container {
    display: flex;
}
```

## Flex-direction

Flex-direction имеет 4 возможных значения, которые изменяют расположение элементов:

1. `flex-direction: row` - располагает элементы в строку
2. `flex-direction: column` - расположение элементов в строку справа налево
3. `flex-direction: row-reverse` - располагает элементы в столбец
4. `flex-direction: column-reverse` - расположение элементов в столбец снизу вверх

## Justify-content

Выравнивает по главной оси 
1. `justify-content: center;`  — по центру
2. `justify-content: flex-start;` — в начале (по умолчанию)
3. `justify-content: flex-end;`— в конце
4. `justify-content: space-between;`— равномерно, первый и последний у краёв
5. `justify-content: space-around;`— равномерно, с отступами по краям
6. `justify-content: space-evenly;`  — равномерно, одинаковые отступы везде
## Align-items
Выравнивает по поперечной оси:
1. `align-items: stretch;`— растягивает элементы (по умолчанию)
2.  `align-items: flex-start;`— в начале
3.  `align-items: flex-end;`— в конце
4.  `align-items: center;`— по центру
5.  `align-items: baseline;` — по базовой линии текста
## Flex-wrap
Переносит элементы
1. `flex-wrap: nowrap;` — без переноса (по умолчанию)
2. `flex-wrap: wrap;` — перенос на новую строку
3. `flex-wrap: wrap-reverse;` — перенос в обратном направлении
## Gap
Создаёт отступы между элементами, команда `gap: 10px;`
## Основные свойства элементов
1. Flex-grow — растягивание элемента. Элемент займёт свободное пространство
`flex-grow: 1;`
2.  Flex-basis — базовый размер (ширина) элемента
`flex-basis: 150px;`
3. Flex-shrink — сжатие элемента
`flex-shrink: 0;`
4. Flex — краткая запись
`flex: 1;`
5. Align-self — индивидуальное выравнивание
`align-self: flex-end;`
## Пример 1. Создание навигационного меню
Код:
```html
<nav class="navbar">
    <a href="#">Главная</a>
    <a href="#">О нас</a>
    <a href="#">Услуги</a>
    <a href="#">Контакты</a>
</nav>
```
## Пример 2. Карточки товаров
Пример оформления карточек, используя Flexbox:
```css
.cards {
    display: flex;
    gap: 20px;
    flex-wrap: wrap;
}
.card {
    flex: 1 1 250px;
    background-color: #f0f0f0;
    padding: 20px;
    border-radius: 10px;
    display: flex;
    flex-direction: column;
}
.card p {
    flex-grow: 1;
}
.card button {
    align-self: flex-start;
}
```
## Пример 3. Центрирование элемента
Центрирование элемента можно выполнить через ** Flexbox**:
```css
.centered-box {
    display: flex;
    justify-content: center;
    align-items: center;
    height: 300px;
    background-color: #e0e0e0;
}
```
## Общие стили страницы
```css
body {
    font-family: Arial, sans-serif;
    padding: 20px;
}
section {
    margin-bottom: 40px;
}
h1,h2 {
    margin-bottom: 20px;
}
```