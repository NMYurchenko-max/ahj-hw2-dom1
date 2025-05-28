# Домашнее задание к занятию 2 «Dom»

Бейджик сборки Action GitHub

[![CI/CD GitHud Actions](https://github.com/NMYurchenko-max/ahj-hw2-dom1/actions/workflows/web.yml/badge.svg)](https://github.com/NMYurchenko-max/ahj-hw2-dom1/actions/workflows/web.yml)

[deploy](https://nmyurchenko-max.github.io/ahj-hw2-dom1/)

[ISC License](LICENSE)

## Описание задания

[AHJ-hw-dom](https://github.com/netology-code/ahj-homeworks/tree/AHJ-50/dom)

## Реализация

```plaintext
gnome-game/
├── src/
|   ├── index.html
│   ├── index.js
|   ├── __mocks__/
│   │   └── fileMock.js (для имитации картинки при тестировании)
│   ├── /js
│   │   └──__tests__/ app.test/js/
│   │   └──app.js
│   ├── /css
│   │   └── style.css
│   └── img/
│       └── goblin.png
├── dist/
├──.github/
|     └──workflow/
|       └──web.yml
├── .husky/
|     └── pre-commit
├── .appveyor.yml
├── .babelrc
├── babel.config.json
├── .browserslistrc
├── .editorconfig
├── eslint.config.mjs
├── .gitignore
├── .gitkeep
├── jest.config.js
├── .prettierignore
├── package.json
└── webpack.config.js (можно обойтись 1 файлом)
```

### Описание

Игра представляет собой поле 4x4, на котором находится персонаж в виде картинки.
Персонаж перемещается по полю в случайном порядке каждую секунду.

## Использование

Клонировать репозиторий
`git clone https://github.com/NMYurchenko-max/ahj-hw2-dom1.git`

Проект собирается с помощью Webpack и публикуется на GitHub Pages с помощью GitHub Actions.

Я использую yarn вместо npm для выполнения скриптов, вы можете использовать аналогичные команды.

Запуск сервера разработки: `yarn start`  / `npm start`
Сборка проекта: `yarn build` / `npm run build`
Просмотр собранного приложения: `yarn show:dist` / `npm run show:dist`

Тестирование: `yarn test` / `npm test`
Проверка кода: `yarn lint` / `npm run lint`

Установка Husky:

```bash
yarn add husky --dev
yarn husky init //  создание конфигурации `pre-commit`
yarn prepare  //  запуска скрипта 

```

## Скрипты

В файле `package.json` описаны следующие скрипты:
"start": Запускает сервер разработки с использованием Webpack Dev Server и конфигурации webpack.dev.js.
"build": Выполняет сборку проекта для продакшена с использованием Webpack и конфигурации webpack.prod.js.
"lint": Запускает ESLint для проверки и исправления стиля кода.
"test": Запускает тесты с использованием Jest.
"coverage": Генерирует отчет о покрытии тестов с использованием Jest.
"preshow:coverage": Подготавливает отчет о покрытии тестов.
"show:coverage": Запускает live-server для отображения отчета о покрытии тестов.
"preshow:dist": Выполняет сборку проекта перед его раздачей.
"show:dist": Запускает http-server для раздачи собранного проекта из директории dist.
