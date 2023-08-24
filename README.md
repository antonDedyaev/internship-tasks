# Задание 2

Необходимо реализовать верстку нескольких UI-элементов с проработкой всех предусмотренных состояний. Смена состояний должна производиться плавно с использованием css-правила [transition](https://developer.mozilla.org/ru/docs/Web/CSS/transition)   
Также, используя [@keyframes](https://developer.mozilla.org/en-US/docs/Web/CSS/@keyframes) создать анимацию в соответствии с [видео-примером](#todo)

> Дополнительно:
> 
> С помощью [медиавыражений](https://developer.mozilla.org/ru/docs/Web/CSS/CSS_media_queries/Using_media_queries) реализовать адаптивные стили под все разрешения экрана, указанные в макете

Каждый UI-элемент должен быть выполнен отдельным компонентом и вставлен на страницу с использованием [pug-миксинов](https://pugjs.org/language/mixins.html)

## Работа с компонентами

### Создание компонента

Для генерации pug, scss файлов компонента необходимо ввести команду:
```shell
npm run component:create [название-компонента]
```
**[название-компонента]** - произвольное название компонента, записанное латиницей  

Например:
```shell
npm run component:create example-button
```
Таким образом в папке `src/components` будет создана папка `example-button` с готовыми для работы pug, scss файлами внутри.  
Все созданные файлы будут добавлены в сборщик автоматически

### Удаление компонента
Для удаления существующего компонента необходимо ввести команду:
```shell
npm run component:remove [название-компонента]
```
**[название-компонента]** - произвольное название компонента, записанное латиницей

Например:
```shell
npm run component:remove example-button
```
Таким образом в папке `src/components` будет удалена папка `example-button`  
Все pug, scss файлы, относящиеся к компоненту будут удалены из сборщика автоматически

## Работа с проектом

### Требования к системе
- Node.js (v.16+)
- npm (v.7+)

### Запуск проекта
1) Установить зависимости
    ```shell
    npm i
    ```
2) Запустить локальную dev-сборку
    ```shell
    npm run dev
    ```
    Запущенный локальный сервер будет доступен в браузере по адресу [localhost:3000](http://localhost:3000/)

### Краткое описание файловой структуры
```
/
├── build_modules
└── src
    ├── assets
    │   ├── fonts
    │   ├── icons
    │   ├── images
    │   └── videos
    ├── components
    └── pages
```
- `build_modules` - служебная директория, необходимая для сборки и запуска проекта. **В рамках задания изменять содержимое папки нельзя**
- `src` - основная рабочая директория, содержащая исходный код проекта
- `src/assets` - необязательная директория для хранения статичных ресурсов (шрифты, изображения, видео, иконки)
- `src/components` - директория для хранения исходного кода компонентов. Каждый компонент располагается в отдельной папке и может состоять из pug, scss и ts файлов
- `src/pages` - директория для хранения статичных страниц
