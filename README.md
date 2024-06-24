# Домашнє завдання 1

## Крок 1

1. Створи репозиторій з назвою `goit-node-cli`, склонуй та ініціалізуй в ньому проєкт за допомогою команди `npm init`. Встанови як залежність проєкту пакет `commander`.

2. В корінь проєкту помісти файли з папки `src`.

## Крок 2

1. У файл `contacts.js` зроби імпорт модулів `fs` (у версії, яка працює з промісами - `fs/promises`) і `path` для роботи з файловою системою.

2. Створи змінну `contactsPath` і запиши в неї шлях до файлу `contacts.json`. Для складання шляху використовуй методи модуля `path`.

3. Додай асинхронні функції для роботи з колекцією контактів. У функціях використовуй модуль `fs` та його методи `readFile()` і `writeFile()`. Відповідні функції мають повертати необхідні дані за допомогою оператора `return`. Вивід в консоль в написаних функціях здійснюватись не повинен.

4. Зроби експорт створених функцій.

```javascript
// contacts.js

/*
 * Розкоментуй і запиши значення
 * const contactsPath = ;
 */

async function listContacts() {
  // ...твій код. Повертає масив контактів.
}

async function getContactById(contactId) {
  // ...твій код. Повертає об'єкт контакту з таким id. Повертає null, якщо контакт з таким id не знайдений.
}

async function removeContact(contactId) {
  // ...твій код. Повертає об'єкт видаленого контакту. Повертає null, якщо контакт з таким id не знайдений.
}

async function addContact(name, email, phone) {
  // ...твій код. Повертає об'єкт доданого контакту (з id).
}
```

## Крок 3

1. Зроби імпорт функцій з файла `contacts.js` в файл `index.js`.

2. Далі використовуй готову функцію `invokeAction()`, яка отримує тип виконуваної дії і необхідні аргументи. Функція має викликати відповідний метод з файлу `contacts.js`, передаючи йому необхідні аргументи. Результат роботи викликаної функції слід вивести в консоль.

## Крок 4

Запусти команди в терміналі і переконайся, що код працює належним чином.

```bash
# Отримуємо і виводимо весь список контактів у вигляді таблиці (console.table)
node index.js -a list

# Отримуємо контакт по id і виводимо у консоль об'єкт контакту або null, якщо контакту з таким id не існує.
node index.js -a get -i 05olLMgyVQdWRwgKfg5J6

# Додаємо контакт та виводимо в консоль об'єкт новоствореного контакту
node index.js -a add -n Mango -e mango@gmail.com -p 322-22-22

# Видаляємо контакт та виводимо в консоль об'єкт видаленого контакту або null, якщо контакту з таким id не існує.
node index.js -a remove -i qdggE76Jtbfd9eWJHrssH
```

## Критерії прийому

1. Створено репозиторій з домашнім завданням.

2. Посилання на репозиторій надіслане ментору на перевірку.

3. Код відповідає технічному завданню проєкту.

4. У коді немає закоментованих ділянок коду.

5. Проєкт коректно працює з актуальною LTS-версією Node.