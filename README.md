# practika

Автор: Кирилин ИПО-21.23

# Лекции

## Если вы это читаете, это не конечная версия. Я потом закончу

## Лекция №1

### Web

#### Базовый сценарий работы веб-приложения:

Пользователь вводит URL.

Браузер загружает HTML-документ.

Браузер парсит HTML и загружает дополнительные ресурсы.

Браузер рендерит страницу.


#### URL (Unified Resource Locator):

http — протокол.

mi-ami.ru — доменное имя.

8080 — TCP-порт.

/profile/account.html — путь к документу.

?gender=male&age=13 — query-параметры.

#comments — якорь.

#### Документы

Документ - тело ответа HTTP-запроса

MIME-типы: text/html, text/css, text/javascript, image/png, video/mp4 и др.

*Документы делятся на статистические и динамические*

Статические: Файлы на дисках сервера с постоянным адресом.

Динамические: Создаются при каждом запросе, зависят от внешних факторов (пользователь, время и т. д.), адресможет меняться.

### HTTP

Основные протоколы: TCP, UDP, HTTP, FTP, SSH.

Структура HTTP-запроса: Метод (GET, POST, PUT, DELETE и др.), URL, Заголовки, Тело (может отсутствовать

Структура HTTP-ответа: Тело, Заголовки.

*Статус ответа:*

1xx — информационные.

2xx — успешные.

3xx — перенаправления.

4xx — ошибки клиента.

5xx — ошибки сервера.

### HTML

*теги HTML:*

html - обёртка.

head - заголовок.

body - тело.

h1–h6 - Определяет HTML-заголовки (от первого до шестого уровня).

p - Определяет параграф.

br - Устанавливает перевод строки.

hr - Создаёт горизонтальную линию или определяет тематическое разделение контента на странице.

a - Используется для создания гиперссылок, позволяющих переходить с одной страницы на другую.

img - Используется для вставки изображений.

### CSS

*Стили:*

width, height — размеры.

margin, padding — отступы.

display — тип отображения.

color — цвет текста.

background — фон.

font — шрифт.

text-align — выравнивание текста.

*Селекторы:*

Универсальный: *.

По тегу: p.

По классу: .btn.

По ID: #userpic.

Контекстные: div.article a.

Дочерние: a > img.

Соседние: h2.sic + p.

Группировка: h1, h2.

*Стили наследуются от родительских элементов.*

Приоритеты: !important > ID > класс > тег.

### JavaScript

*Способы подключения:*

Внешний файл: <script src="./jquery.js"></script>.

В HTML: <script>...</script>.

## Лекция №2

### Основы JavaScript

Объявление переменных возможно с помощью ключевых слов:

let — современный способ объявления переменных.

var — устаревший способ, не рекомендуется к использованию.

const — объявляет константу, значение которой нельзя изменить после инициализации.

Пример:

let message = "hello";

message = 123456; // Ошибки не будет

JavaScript строго не типизированный язык. Преобразование типов может происходить неявно:

"" == 0;      // true

"0" == 0;     // true

"" == "0";    // false

"0" == false; // true

Основные математические операции: Сложение (+), вычитание (-), умножение (*), деление (/), Остаток от деления (%), Инкремент (++), декремент (--).

Пример:

const a = 3 + 2; // 5
a += 2;          // 7
a++;             // 8


Операторы сравнения: >, <, >=, <=.

Равенство: == (нестрогое), === (строгое).

Неравенство: !=, !==.

Пример:

3 > 2;        // true

false == "";  // true

false !== true; // true

### Условные операторы: 

if...else:

```javascript
if (year == 2007) {
  alert('Верните меня туда');
} else {
  alert('Эх...');
}
```

Тернарный оператор:

const year = (условие) ? 2007 : 2023;

Цикл while:

```javascript
while (condition) {
  // тело цикла
}
```

do...while:

```javascript
do {
  // тело цикла
} while (condition);
```

for:

```javascript
for (начало; условие; шаг) {
  // тело цикла
}
```

### Функции

Function Declaration:

```javascript
function sum(a, b) {
  return a + b;
}
```

Function Expression:

```javascript
let sum = function(a, b) {
  return a + b;
};
```

Стрелочные функции:

```javascript
const sum = (a, b) => a + b;
const sum2 = (a, b) => {
  let result = a + b;
  return result;
};
```

### Объекты

Объекты — это структуры "ключ-значение".

Создание:

```javascript
let user = {}; // литерал объекта
let user = new Object(); // конструктор
```

Доступ к свойствам:

```javascript
user.name;     // через точку
user["age"];   // через квадратные скобки
```

Методы объектов:

```javascript
let user = {
  name: "John",
  sayHi() {
    alert(this.name);
  }  
};
```javascript

### Массивы

Создание:

```javascript
let arr = [];
let fruits = ["Яблоко", "Апельсин"];
```

Методы:

push/pop — добавление/удаление с конца.

shift/unshift — добавление/удаление с начала.

slice — создание подмассива.

forEach — перебор элементов.

map/filter/reduce — преобразование массива.

Пример:

let lengths = ["Бильбо", "Гэндальф"].map(item => item.length); // [6, 8]

### Деструктуризация

Массивы:

let [firstName, surname] = ["Ilya", "Kantor"];

Объекты:

let {title, width, height} = {title: "Menu", width: 100, height: 200};

### Коллекции: Map и Set

**Map** — коллекция ключ-значение:

```javascript
let map = new Map();
map.set("1", "str1");
map.get("1"); // "str1"
```

**Set** — коллекция уникальных значений:

```javascript
let set = new Set();
set.add("John");
set.add("Pete");
```

### JSON

JSON.stringify — преобразование объекта в строку JSON.

JSON.parse — преобразование строки JSON в объект.

Пример:

```javascript
let student = {name: "John", age: 30};
let json = JSON.stringify(student);
let parsed = JSON.parse(json);
```

### Классы

Создание класса:

```javascript
class User {
  constructor(name) {
    this.name = name;  
  }  
  sayHi() { 
    alert(this.name);    
  }  
}
let user = new User("Иван");
user.sayHi(); // Иван
```

Наследование:

```javascript
class Animal {
  run() { alert("Бежит"); }
}
class Rabbit extends Animal {
  hide() { alert("Прячется"); } 
}
```

Приватные свойства:

```javascript
class CoffeeMachine {
  #waterLimit = 200; 
  #checkWater() { ... } 
}
```

## Лекция №3

### Продвинутая работа с функциями

Rest-оператор позволяет собирать неограниченное количество аргументов функции в массив:

```javascript
function sumAll(...args) {
  let sum = 0;
  for (let arg of args) sum += arg;
  return sum; 
}
```

Spread-оператор разворачивает массив в список аргументов:

```javascript
const arr1 = [0, -2, 1, 5];
const arr2 = [100, 200, 300, -322];
console.log(Math.max(...arr1, ...arr2));
```

Замыкания: Функция запоминает свое лексическое окружение:

```javascript
function makeWorker() {
  let name = "Pete";
  return function() { alert(name); };
}
let name = "John";
let work = makeWorker();
work(); // "Pete"
```

Лексическое окружение: Каждая функция, блок кода и скрипт имеют связанный объект LexicalEnvironment, состоящий из:

Environment Record - хранилище локальных переменных

Ссылки на внешнее окружение

Особенности:

Function Declaration инициализируются сразу при создании окружения;
var не имеет блочной области видимости, поднимается в начало функции;
IIFE (Immediately-Invoked Function Expression) создает изолированное окружение

### Декораторы и контекст вызова

Декоратор с кешированием:

```javascript
function cachingDecorator(func) {
  let cache = new Map();
  return function(x) {
    if (cache.has(x)) return cache.get(x);
    let result = func.call(this, x);
    cache.set(x, result);
    return result;
  };
}
```

Привязка контекста:

func.call(context, ...args) - вызывает функцию с указанным контекстом

func.apply(context, args) - аналогично, но аргументы передаются массивом

func.bind(context) - создает новую функцию с привязанным контекстом

### Прототипы и наследование

Прототипное наследование:

```javascript
let animal = { eats: true };
let rabbit = { jumps: true };
rabbit.__proto__ = animal; 
alert(rabbit.eats); // true
```

Классы и наследование

```javascript
class Animal {
  constructor(name) {
    this.name = name;
  }
  run() { alert(`${this.name} бежит`); }
}

class Rabbit extends Animal {
  hide() { alert(`${this.name} прячется`); }
}
```

### Модули (ES Modules)

Экспорт и импорт:

```javascript
// say.js
export function sayHi(user) { alert(`Hello, ${user}!`); }

// main.js
import {sayHi} from './say.js';
sayHi('John');
```

Особенности модулей:

Каждый модуль выполняется только один раз;

Имеют свою область видимости;

Поддерживают экспорт по умолчанию (export default);

Позволяют реэкспорт (export {x} from './module');

### Обработка ошибок

Try...catch:

```javascript
try {
  // код
} catch(err) {
  alert(err.name);    // тип ошибки
  alert(err.message); // сообщение
  alert(err.stack);   // стек вызовов
} finally {
  // выполнится в любом случае
}
```

Пользовательские ошибки:

```javascript
class ValidationError extends Error {
  constructor(message) {
    super(message);
    this.name = "ValidationError";
  }
}
```

### Регулярные выражения

Создание и использование:

```javascript
let regexp = /шаблон/gi;
let str = "Любо, братцы, любо!";
let result = str.match(regexp);
str.replace(regexp, "замена");
regexp.test(str); // true/false
```

### События

Обработчики событий:

```javascript
element.onclick = function(event) {
  alert(`Клик на ${event.target.tagName}`);
};

element.addEventListener("click", handler);
element.removeEventListener("click", handler);
```

### Всплытие и погружение
События сначала идут вниз (погружение), затем вверх (всплытие). Можно:

Остановить всплытие: event.stopPropagation();

Отменить действие по умолчанию: event.preventDefault();

Настроить обработку на фазе погружения: addEventListener(..., true);

Пользовательские события:

```javascript
let event = new Event("click");
element.dispatchEvent(event);
```

## Лекция №4

Внутреннее устройство браузера
Процессы браузера:
Network Process - обработка сетевых запросов

Renderer Process - рендеринг страницы (по одному на вкладку)

GPU Process - обработка графики

Plugin Process - управление плагинами

Storage Process - работа с хранилищами данных

Критические этапы рендеринга (Critical Rendering Path):
Загрузка HTML

Построение DOM (Document Object Model)

Построение CSSOM (CSS Object Model)

Формирование Render Tree

Компоновка (Layout)

Отрисовка (Paint)

DOM и CSSOM
DOM:
HTML преобразуется в токены, затем в узлы (nodes)

Формируется иерархическое дерево элементов

Инкрементальное построение (может отображаться частично)

CSSOM:
Содержит все стили страницы

Блокирует рендер до полной загрузки

Не инкрементальный (нужно ждать полной загрузки)

Архитектурные принципы
Основные методологии:
DRY (Don't Repeat Yourself) - избегание дублирования кода

KISS (Keep It Simple Stupid) - простота решений

SOLID - пять принципов ООП:

Single Responsibility

Open-Closed

Liskov Substitution

Interface Segregation

Dependency Inversion

Декомпозиция:
Функциональная: разделение на модули с инкапсуляцией данных

Компонентная: независимые, переиспользуемые компоненты

Паттерны проектирования
MVC (Model-View-Controller):
Модель: бизнес-логика и данные

Представление: отображение данных (HTML, CSS)

Контроллер: связующее звено между моделью и представлением

Роутинг:
Соответствие между URL и View

Использование History API для навигации в SPA:

javascript
window.history.pushState(state, title, url);
window.history.replaceState(state, title, url);
Архитектура CSS
Проблемы традиционных подходов:
Сильная связанность со структурой документа

Конфликты имен классов

Трудности поддержки и масштабирования

Современные решения:
CSS Modules: автоматическая генерация уникальных имен классов

javascript
import styles from './Button.module.css';
<button className={styles.primary}>Click</button>
CSS-in-JS: стили как JavaScript-объекты

javascript
const styles = {
  button: {
    backgroundColor: 'blue',
    color: 'white'
  }
};
OOCSS (Object-Oriented CSS):

Разделение структуры и оформления

Переиспользуемые компоненты

Инструменты разработки
NPM (Node Package Manager):
Управление зависимостями проекта

Инициализация проекта: npm init

Установка пакетов: npm install <package>

Файлы конфигурации:

package.json - метаданные проекта

package-lock.json - точные версии зависимостей

Подключение библиотек:
Через CDN:

html
<script src="https://cdn.jsdelivr.net/npm/bootstrap@5.3.0/dist/js/bootstrap.min.js"></script>
Через npm:

javascript
import { Component } from 'bootstrap';

## Лекция №5

Основы клиент-серверного взаимодействия
DNS и TCP соединение:
Браузер получает IP-адрес сервера через DNS (Domain Name System)

Устанавливается TCP соединение через "тройное рукопожатие":

Клиент → Сервер: SYN

Сервер → Клиент: SYN-ACK

Клиент → Сервер: ACK

HTTP запросы:
Браузер отправляет HTTP-запрос

Сервер обрабатывает запрос (бизнес-логика, рендеринг)

Сервер отправляет ответ (HTML, JSON, файлы)

Браузер отображает полученный контент

Архитектурные модели
Эволюция веб-приложений:
Статические страницы: только HTML/CSS

SSR (Server-Side Rendering): динамическая генерация HTML на сервере

Веб-сервисы:

Frontend: SPA (Single Page Application)

Backend: REST API

REST принципы:
Stateless (каждый запрос содержит всю необходимую информацию)

Единообразие интерфейса

Кэшируемость

Клиент-серверное разделение

Node.js основы
Особенности Node.js:
Среда выполнения JavaScript на движке V8

Асинхронная, событийно-ориентированная архитектура

Однопоточная модель с Event Loop

Богатая стандартная библиотека (http, fs, path и др.)

Пример простого сервера:
javascript
const http = require('http');
const server = http.createServer((req, res) => {
  res.writeHead(200);
  res.end('Hello World!');
});
server.listen(8000, () => console.log('Server running'));
TypeScript vs JavaScript
Преимущества TypeScript:
Статическая типизация

Интерфейсы и декораторы

Поддержка ООП

Лучшая поддержка IDE

Совместимость с JavaScript

Пример типизации:
typescript
interface Person {
  name: string;
  age: number;
}

function greet(person: Person): string {
  return `Hello, ${person.name}`;
}
Nest.js - фреймворк для Node.js
Особенности Nest.js:
Архитектура, вдохновленная Angular

Встроенная поддержка TypeScript

Dependency Injection

Модульная структура

Готовые решения для:

Валидации

Аутентификации

Работы с базами данных

Основные компоненты:
Контроллеры - обработка HTTP запросов

typescript
@Controller('stocks')
export class StocksController {
  @Get()
  findAll() { return this.stocksService.findAll(); }
}
Сервисы - бизнес-логика

typescript
@Injectable()
export class StocksService {
  findAll() { return this.stocks; }
}
Модули - организация кода

typescript
@Module({
  controllers: [StocksController],
  providers: [StocksService],
})
export class StocksModule {}
Практическая работа с API
CRUD операции:
GET /stocks - получить все записи

POST /stocks - создать новую запись

GET /stocks/:id - получить запись по ID

PATCH /stocks/:id - обновить запись

DELETE /stocks/:id - удалить запись

Тестирование с Postman:
Создание запроса (метод, URL, headers)

Отправка тела запроса (JSON)

Анализ ответа (статус код, тело ответа)

Работа с данными
Хранение данных:
В памяти (массивы, объекты)

В файлах (JSON)

В базах данных (MongoDB, PostgreSQL)

Пример сервиса для работы с данными:
typescript
@Injectable()
export class StocksService {
  private stocks: Stock[] = [];

  create(stock: CreateStockDto) {
    const newStock = { ...stock, id: this.stocks.length + 1 };
    this.stocks.push(newStock);
    return newStock;
  }
}

## Лекция №6

Основы AJAX
Что такое AJAX:
Асинхронный JavaScript и XML (Asynchronous JavaScript and XML)

Технология для обмена данными с сервером без перезагрузки страницы

Основана на объекте XMLHttpRequest (XHR)

Поддерживает различные форматы данных: XML, JSON, HTML, текстовые файлы

Основные принципы работы:
Создание XHR-объекта

Настройка запроса (метод, URL)

Отправка запроса

Обработка ответа

javascript
const xhr = new XMLHttpRequest();
xhr.open('GET', '/api/data');
xhr.send();

xhr.onload = function() {
  if (xhr.status === 200) {
    console.log(xhr.response);
  }
};
Форматы данных
JSON (JavaScript Object Notation):
Легковесный формат обмена данными

Поддерживается всеми современными языками

Пример:

json
{
  "name": "John",
  "age": 30,
  "courses": ["HTML", "CSS", "JS"]
}
Blob и FormData:
Blob - для работы с бинарными данными

FormData - для отправки форм и файлов

XMLHttpRequest
Методы и свойства:
open(method, url) - инициализация запроса

send(body) - отправка запроса

responseType - тип ожидаемого ответа (text, json, blob и др.)

status - HTTP-код ответа

response - тело ответа

Состояния запроса (readyState):
0 (UNSET) - инициализация

1 (OPENED) - вызван open()

2 (HEADERS_RECEIVED) - получены заголовки

3 (LOADING) - загрузка данных

4 (DONE) - запрос завершен

Безопасность: Same Origin Policy и CORS
Same Origin Policy (SOP):
Ограничивает кросс-доменные запросы

URL считаются одного источника, если совпадают:

Протокол (http/https)

Домен (example.com)

Порт (80, 443 и др.)

CORS (Cross-Origin Resource Sharing):
Механизм для безопасного кросс-доменного взаимодействия

Сервер должен включать заголовки:

Access-Control-Allow-Origin

Access-Control-Allow-Methods

Access-Control-Allow-Headers

Типы запросов:
Простые (GET, POST, HEAD с ограниченными заголовками)

Предварительные (preflight) - для сложных запросов (OPTIONS)

Хранение данных на клиенте
Варианты хранения:
Cookies:

Маленький размер (до 4KB)

Отправляются с каждым запросом

Параметры: Expires, Domain, Path, Secure, HttpOnly

Web Storage:

localStorage - постоянное хранение

sessionStorage - хранение на время сессии

До 5MB данных

IndexedDB:

Клиентская NoSQL база данных

Подходит для сложных структур данных

Практические примеры
Отправка POST-запроса:
javascript
const xhr = new XMLHttpRequest();
xhr.open('POST', '/api/create');
xhr.setRequestHeader('Content-Type', 'application/json');
xhr.send(JSON.stringify({ name: 'John' }));

xhr.onload = function() {
  if (xhr.status === 201) {
    console.log('Created:', xhr.response);
  }
};
Работа с CORS:
javascript
fetch('https://api.example.com/data', {
  method: 'GET',
  mode: 'cors',
  headers: {
    'Content-Type': 'application/json'
  }
})
.then(response => response.json())
.then(data => console.log(data));

## Лекция №7

Основы асинхронности в JavaScript
Проблема синхронного кода:
JavaScript выполняется однопоточно

Долгие операции (загрузка скриптов, запросы к серверу) блокируют выполнение кода

Пример:

javascript
loadScript('script.js'); // Долгая операция
alert('Скрипт загружен!'); // Выполнится ДО загрузки
Решение через колбэки:
javascript
function loadScript(src, callback) {
  let script = document.createElement('script');
  script.src = src;
  script.onload = () => callback(script);
  document.head.append(script);
}

loadScript('script.js', (script) => {
  alert(`Загружен: ${script.src}`);
});
Event Loop и очередь задач
Принцип работы:
Call Stack - стек вызовов синхронных функций

Macrotask Queue - очередь макрозадач (setTimeout, setInterval)

Microtask Queue - очередь микрозадач (Promise, MutationObserver)

Event Loop - управляет порядком выполнения

Порядок выполнения:
Синхронный код

Микрозадачи (полностью очищается очередь)

Макрозадачи (по одной за цикл)

Рендеринг (при необходимости)

Проблемы колбэков и Promise
Callback Hell:
javascript
loadScript('script1.js', () => {
  loadScript('script2.js', () => {
    loadScript('script3.js', () => {
      // Глубокий уровень вложенности
    });
  });
});
Решение через Promise:
javascript
function loadScript(src) {
  return new Promise((resolve, reject) => {
    let script = document.createElement('script');
    script.src = src;
    script.onload = () => resolve(script);
    script.onerror = () => reject(new Error('Ошибка загрузки'));
    document.head.append(script);
  });
}

loadScript('script.js')
  .then(script => console.log('Загружен:', script.src))
  .catch(err => console.error('Ошибка:', err));
Современные подходы
Async/Await:
javascript
async function loadAllScripts() {
  try {
    const script1 = await loadScript('script1.js');
    const script2 = await loadScript('script2.js');
    console.log('Все скрипты загружены');
  } catch (err) {
    console.error('Ошибка:', err);
  }
}
Параллельное выполнение:
javascript
Promise.all([
  loadScript('script1.js'),
  loadScript('script2.js'),
  loadScript('script3.js')
]).then((scripts) => {
  console.log('Все скрипты загружены');
});
Fetch API
Основы работы:
javascript
async function fetchData() {
  try {
    const response = await fetch('https://api.example.com/data');
    if (!response.ok) throw new Error('Ошибка сети');
    const data = await response.json();
    console.log(data);
  } catch (error) {
    console.error('Ошибка:', error);
  }
}
Настройки запроса:
javascript
fetch('https://api.example.com/data', {
  method: 'POST',
  headers: {
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({ key: 'value' })
});
Совместимость и транспиляция
Babel:
Транспилирует современный JS в старый формат

Конфигурация в .babelrc:

json
{
  "presets": [
    ["@babel/preset-env", {
      "targets": {
        "edge": "17",
        "firefox": "60",
        "chrome": "67"
      }
    }]
  ]
}
Сборщики (Vite, Webpack):
Объединяют множество файлов в один bundle

Оптимизируют код для production

Пример Vite конфига:

javascript
export default {
  build: {
    outDir: './public',
    emptyOutDir: true,
  }
};
