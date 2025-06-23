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

Переменные
Объявление переменных возможно с помощью ключевых слов:

let — современный способ объявления переменных.

var — устаревший способ, не рекомендуется к использованию.

const — объявляет константу, значение которой нельзя изменить после инициализации.

Пример:

javascript
let message = "hello";
message = 123456; // Ошибки не будет
Типизация и преобразование типов
JavaScript динамически типизирован. Преобразование типов может происходить неявно:

javascript
"" == 0;      // true
"0" == 0;     // true
"" == "0";    // false
"0" == false; // true
Математические операции
Основные операции:

Сложение (+), вычитание (-), умножение (*), деление (/).

Остаток от деления (%).

Инкремент (++), декремент (--).

Пример:

javascript
const a = 3 + 2; // 5
a += 2;          // 7
a++;             // 8
Операторы сравнения
Сравнение: >, <, >=, <=.

Равенство: == (нестрогое), === (строгое).

Неравенство: !=, !==.

Пример:

javascript
3 > 2;        // true
false == "";  // true
false !== true; // true
Условные операторы
if...else:

javascript
if (year == 2007) {
  alert('Верните меня туда');
} else {
  alert('Эх...');
}
Тернарный оператор:

javascript
const year = (условие) ? 2007 : 2023;
Циклы
while:

javascript
while (condition) {
  // тело цикла
}
do...while:

javascript
do {
  // тело цикла
} while (condition);
for:

javascript
for (начало; условие; шаг) {
  // тело цикла
}
Функции
Function Declaration:

javascript
function sum(a, b) {
  return a + b;
}
Function Expression:

javascript
let sum = function(a, b) {
  return a + b;
};
Стрелочные функции:

javascript
const sum = (a, b) => a + b;
const sum2 = (a, b) => {
  let result = a + b;
  return result;
};
Объекты
Объекты — это структуры "ключ-значение".

Создание:

javascript
let user = {}; // литерал объекта
let user = new Object(); // конструктор
Доступ к свойствам:

javascript
user.name;     // через точку
user["age"];   // через квадратные скобки
Методы объектов:

javascript
let user = {
  name: "John",
  sayHi() {
    alert(this.name);
  }
};
Массивы
Создание:

javascript
let arr = [];
let fruits = ["Яблоко", "Апельсин"];
Методы:

push/pop — добавление/удаление с конца.

shift/unshift — добавление/удаление с начала.

slice — создание подмассива.

forEach — перебор элементов.

map/filter/reduce — преобразование массива.

Пример:

javascript
let lengths = ["Бильбо", "Гэндальф"].map(item => item.length); // [6, 8]
Деструктуризация
Массивы:

javascript
let [firstName, surname] = ["Ilya", "Kantor"];
Объекты:

javascript
let {title, width, height} = {title: "Menu", width: 100, height: 200};
Коллекции: Map и Set
Map — коллекция ключ-значение:

javascript
let map = new Map();
map.set("1", "str1");
map.get("1"); // "str1"
Set — коллекция уникальных значений:

javascript
let set = new Set();
set.add("John");
set.add("Pete");
JSON
JSON.stringify — преобразование объекта в строку JSON.

JSON.parse — преобразование строки JSON в объект.

Пример:

javascript
let student = {name: "John", age: 30};
let json = JSON.stringify(student);
let parsed = JSON.parse(json);
Классы
Создание класса:

javascript
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
Наследование:

javascript
class Animal {
  run() { alert("Бежит"); }
}
class Rabbit extends Animal {
  hide() { alert("Прячется"); }
}
Приватные свойства:

javascript
class CoffeeMachine {
  #waterLimit = 200;
  #checkWater() { ... }
}

## Лекция №3

Продвинутая работа с функциями
Rest-оператор
Позволяет собирать неограниченное количество аргументов функции в массив:

javascript
function sumAll(...args) {
  let sum = 0;
  for (let arg of args) sum += arg;
  return sum;
}
Spread-оператор
Разворачивает массив в список аргументов:

javascript
const arr1 = [0, -2, 1, 5];
const arr2 = [100, 200, 300, -322];
console.log(Math.max(...arr1, ...arr2));
Замыкания
Функция запоминает свое лексическое окружение:

javascript
function makeWorker() {
  let name = "Pete";
  return function() { alert(name); };
}
let name = "John";
let work = makeWorker();
work(); // "Pete"
Лексическое окружение
Каждая функция, блок кода и скрипт имеют связанный объект LexicalEnvironment, состоящий из:

Environment Record - хранилище локальных переменных

Ссылки на внешнее окружение

Особенности:

Function Declaration инициализируются сразу при создании окружения

var не имеет блочной области видимости, поднимается в начало функции

IIFE (Immediately-Invoked Function Expression) создает изолированное окружение

Декораторы и контекст вызова
Декоратор с кешированием
javascript
function cachingDecorator(func) {
  let cache = new Map();
  return function(x) {
    if (cache.has(x)) return cache.get(x);
    let result = func.call(this, x);
    cache.set(x, result);
    return result;
  };
}
Привязка контекста
func.call(context, ...args) - вызывает функцию с указанным контекстом

func.apply(context, args) - аналогично, но аргументы передаются массивом

func.bind(context) - создает новую функцию с привязанным контекстом

Прототипы и наследование
Прототипное наследование
javascript
let animal = { eats: true };
let rabbit = { jumps: true };
rabbit.__proto__ = animal; 
alert(rabbit.eats); // true
Классы и наследование
javascript
class Animal {
  constructor(name) {
    this.name = name;
  }
  run() { alert(`${this.name} бежит`); }
}

class Rabbit extends Animal {
  hide() { alert(`${this.name} прячется`); }
}
Модули (ES Modules)
Экспорт и импорт
javascript
// say.js
export function sayHi(user) { alert(`Hello, ${user}!`); }

// main.js
import {sayHi} from './say.js';
sayHi('John');
Особенности модулей:
Каждый модуль выполняется только один раз

Имеют свою область видимости

Поддерживают экспорт по умолчанию (export default)

Позволяют реэкспорт (export {x} from './module')

Обработка ошибок
Try...catch
javascript
try {
  // код
} catch(err) {
  alert(err.name);    // тип ошибки
  alert(err.message); // сообщение
  alert(err.stack);   // стек вызовов
} finally {
  // выполнится в любом случае
}
Пользовательские ошибки
javascript
class ValidationError extends Error {
  constructor(message) {
    super(message);
    this.name = "ValidationError";
  }
}
Регулярные выражения
Создание и использование
javascript
let regexp = /шаблон/gi;
let str = "Любо, братцы, любо!";
let result = str.match(regexp);
str.replace(regexp, "замена");
regexp.test(str); // true/false
События
Обработчики событий
javascript
element.onclick = function(event) {
  alert(`Клик на ${event.target.tagName}`);
};

element.addEventListener("click", handler);
element.removeEventListener("click", handler);
Всплытие и погружение
События сначала идут вниз (погружение), затем вверх (всплытие). Можно:

Остановить всплытие: event.stopPropagation()

Отменить действие по умолчанию: event.preventDefault()

Настроить обработку на фазе погружения: addEventListener(..., true)

Пользовательские события
javascript
let event = new Event("click");
element.dispatchEvent(event);

## Лекция №4

## Лекция №5

## Лекция №6

## Лекция №7
