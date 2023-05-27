# Ui-Kit

![image](https://github.com/BatyrbekWebDev/uikit-vue3/assets/43727077/9f7f654b-a755-4f4b-b7df-c46f40e3a39d)

**Ui-Kit** - это проект, который предоставляет готовые дизайн компоненты для использования в веб-разработке. В комплекте есть различные элементы, такие как кнопки, поля ввода, индикаторы прогресса, радиокнопки, таблицы.

## Установка

Для установки необходимо использовать NPM, запустив команду в консоли:

```
npm install uikit
```

## Использование

Подключить **uikit** очень просто. Вам необходимо добавить ссылку на CSS-файл в разделе **head**:

```html
<head>
    <link rel="stylesheet" type="text/css" href="path/to/uikit.min.css">
</head>
```

Для того чтобы начать использовать компоненты, вам также необходимо подключить **Vue** и **Vue Router**:

```html
<div id="app">
  <router-view></router-view>
</div>

<script src="https://cdn.jsdelivr.net/npm/vue"></script>
<script src="https://unpkg.com/vue-router/dist/vue-router.js"></script>
<script src="path/to/uikit.min.js"></script>
<script src="./router.js"></script>
```

Далее вы можете использовать компоненты **uikit** в своих шаблонах **Vue**:

```html
<template>
  <div>
    <h1>Пример использования компонентов uikit</h1>
    <button class="uk-button">Кнопка</button>
    <input class="uk-input" type="text" placeholder="Введите текст">
    <div class="uk-progress">
      <div class="uk-progress-bar" style="width: 50%;">50%</div>
    </div>
    <label><input class="uk-radio" type="radio" name="radio"> Radio 1</label>
    <label><input class="uk-radio" type="radio" name="radio"> Radio 2</label>
    <table class="uk-table">
      <thead>
        <tr>
          <th>Заголовок таблицы 1</th>
          <th>Заголовок таблицы 2</th>
          <th>Заголовок таблицы 3</th>
        </tr>
      </thead>
      <tbody>
        <tr>
          <td>Содержимое ячейки 1</td>
          <td>Содержимое ячейки 2</td>
          <td>Содержимое ячейки 3</td>
        </tr>
        <tr>
          <td>Содержимое ячейки 4</td>
          <td>Содержимое ячейки 5</td>
          <td>Содержимое ячейки 6</td>
        </tr>
      </tbody>
    </table>
  </div>
</template>

<script>
export default {
  name: 'MyComponent'
}
</script>
```

## Запуск проекта

Для запуска проекта необходимо выполнить следующие действия:

1. Склонировать репозиторий:
```
git clone https://github.com/user/uikit.git
```
2. Установить зависимости:
```
cd uikit
npm install
```
3. Запустить проект:
```
npm run dev
```
После этого проект будет запущен на локальном сервере по адресу http://localhost:8080/.
