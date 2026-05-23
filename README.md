# 🟨 JavaScript — មគ្គុទ្ទេសក៍ពេញលេញ (ចាប់ផ្តើម → កម្រិតខ្ពស់)

> **ភាសា:** JavaScript (JS) &nbsp;|&nbsp; **កម្រិត:** Beginner → Advanced &nbsp;|&nbsp; **ភាសាខ្មែរ**

---

## 📋 តារាងមាតិកា

- [១. JavaScript គឺជាអ្វី?](#១-javascript-គឺជាអ្វី)
- [២. Variables — ការផ្ទុកទិន្នន័យ](#២-variables--ការផ្ទុកទិន្នន័យ)
- [៣. Data Types — ប្រភេទទិន្នន័យ](#៣-data-types--ប្រភេទទិន្នន័យ)
- [៤. Operators — ប្រមាណវិធី](#៤-operators--ប្រមាណវិធី)
- [៥. Conditionals — លក្ខខណ្ឌ](#៥-conditionals--លក្ខខណ្ឌ)
- [៦. Loops — រង្វិលជុំ](#៦-loops--រង្វិលជុំ)
- [៧. Functions — អនុគមន៍](#៧-functions--អនុគមន៍)
- [៨. Arrays — អារ៉េ](#៨-arrays--អារ៉េ)
- [៩. Objects — វត្ថុ](#៩-objects--វត្ថុ)
- [១០. DOM — ការគ្រប់គ្រងទំព័រ Web](#១០-dom--ការគ្រប់គ្រងទំព័រ-web)
- [១១. Events — ព្រឹត្តិការណ៍](#១១-events--ព្រឹត្តិការណ៍)
- [១២. Promises & Async/Await](#១២-promises--asyncawait)
- [១៣. Classes — OOP](#១៣-classes--oop)
- [១៤. Modules — ES Modules](#១៤-modules--es-modules)
- [១៥. Error Handling — ការដោះស្រាយកំហុស](#១៥-error-handling--ការដោះស្រាយកំហុស)
- [១៦. Advanced Topics — ប្រធានបទកម្រិតខ្ពស់](#១៦-advanced-topics--ប្រធានបទកម្រិតខ្ពស់)

---

## ១. JavaScript គឺជាអ្វី?

JavaScript គឺជាភាសាសរសេរកូដដែលប្រើច្រើនបំផុតនៅលើពិភពលោក។ វាអាចប្រើបាន:

- **នៅក្នុង Browser** — ធ្វើទំព័រ web ឱ្យដំណើរការ
- **នៅ Server** — ដោយប្រើ Node.js
- **Mobile Apps** — ដោយប្រើ React Native
- **Desktop Apps** — ដោយប្រើ Electron

```html
<!-- ដំណើរការ JS នៅក្នុង HTML -->
<script>
  console.log("សួស្តី ពិភពលោក! 🌍");
</script>
```

```bash
# ឬដំណើរការតាម Node.js
node my-file.js
```

---

## ២. Variables — ការផ្ទុកទិន្នន័យ

Variables ប្រើសម្រាប់ផ្ទុកទិន្នន័យ។ JavaScript មាន ៣ ពាក្យ: `let`, `const`, `var`

```js
// ✅ const — ប្រើនៅពេលតម្លៃមិនផ្លាស់ប្តូរ
const name = "សុផល";
const age = 25;

// ✅ let — ប្រើនៅពេលតម្លៃអាចផ្លាស់ប្តូរ
let score = 0;
score = 100; // ✅ អាចផ្លាស់ប្តូរបាន

// ❌ var — មិនត្រូវប្រើទៀតទេ (មានបញ្ហា scope)
var oldWay = "មិនល្អ";
```

> 💡 **គន្លឹះ:** ប្រើ `const` ជាមុន, ប្រើ `let` ពេលចាំបាច់, មិនប្រើ `var` ទេ

---

## ៣. Data Types — ប្រភេទទិន្នន័យ

```js
// String — អត្ថបទ
const greeting = "សួស្តី";
const message = 'JavaScript ល្អណាស់';
const template = `ខ្ញុំឈ្មោះ ${name}`; // Template literal

// Number — លេខ
const price = 9.99;
const count = 100;

// Boolean — ពិត/មិនពិត
const isLoggedIn = true;
const hasError = false;

// Array — បញ្ជី
const fruits = ["ស្វាយ", "ចេក", "ទុំបាវ"];

// Object — វត្ថុ
const user = {
  name: "វិចិត្រ",
  age: 22,
};

// null — គ្មានតម្លៃ (ដោយចេតនា)
const empty = null;

// undefined — មិនទាន់មានតម្លៃ
let notSet;
console.log(notSet); // undefined

// typeof — ពិនិត្យប្រភេទ
console.log(typeof "hello");  // "string"
console.log(typeof 42);       // "number"
console.log(typeof true);     // "boolean"
```

---

## ៤. Operators — ប្រមាណវិធី

```js
// ➕ គណិតវិទ្យា
console.log(5 + 3);   // 8
console.log(10 - 4);  // 6
console.log(3 * 4);   // 12
console.log(10 / 2);  // 5
console.log(10 % 3);  // 1  (ចំណែក)
console.log(2 ** 8);  // 256 (ស្វ័យគុណ)

// 📊 ប្រៀបធៀប
console.log(5 === 5);   // true  (ស្មើទាំងប្រភេទ)
console.log(5 !== 3);   // true  (មិនស្មើ)
console.log(10 > 5);    // true
console.log(3 <= 3);    // true

// ⚠️ == vs ===
console.log(5 == "5");  // true  (ប្រៀបតែតម្លៃ — ប្រថុយ!)
console.log(5 === "5"); // false (ប្រៀបទាំងប្រភេទ — ត្រឹមត្រូវ)

// 🔗 Logical (តក្កវិទ្យា)
console.log(true && false);  // false (AND)
console.log(true || false);  // true  (OR)
console.log(!true);          // false (NOT)

// ✍️ Assignment (ការប្រគល់)
let x = 10;
x += 5;  // x = x + 5 = 15
x -= 3;  // x = x - 3 = 12
x *= 2;  // x = x * 2 = 24
```

---

## ៥. Conditionals — លក្ខខណ្ឌ

### if / else if / else

```js
const score = 85;

if (score >= 90) {
  console.log("ឧត្តម A");
} else if (score >= 80) {
  console.log("ល្អ B");
} else if (score >= 70) {
  console.log("មធ្យម C");
} else {
  console.log("ត្រូវខំប្រឹងទៀត");
}
```

### Ternary Operator (សង្ខេប)

```js
const age = 20;

// ប្រៀបធៀបនឹង if/else ខ្លី
const status = age >= 18 ? "ពេញវ័យ" : "មិនទាន់ពេញវ័យ";
console.log(status); // "ពេញវ័យ"
```

### Switch

```js
const day = "ច័ន្ទ";

switch (day) {
  case "ច័ន្ទ":
    console.log("ថ្ងៃចាប់ផ្តើមសប្តាហ៍");
    break;
  case "សុក្រ":
    console.log("ជិតដល់ចុងសប្តាហ៍");
    break;
  default:
    console.log("ថ្ងៃធម្មតា");
}
```

---

## ៦. Loops — រង្វិលជុំ

### for loop

```js
// រាប់ពី 1 ដល់ 5
for (let i = 1; i <= 5; i++) {
  console.log(`លេខ: ${i}`);
}
```

### while loop

```js
let count = 0;

while (count < 3) {
  console.log(`ការរាប់: ${count}`);
  count++;
}
```

### for...of (ប្រើជាមួយ Array)

```js
const cities = ["ភ្នំពេញ", "សៀមរាប", "បាត់ដំបង"];

for (const city of cities) {
  console.log(`ទីក្រុង: ${city}`);
}
```

### for...in (ប្រើជាមួយ Object)

```js
const student = { name: "ដារ៉ា", age: 20, grade: "A" };

for (const key in student) {
  console.log(`${key}: ${student[key]}`);
}
// name: ដារ៉ា
// age: 20
// grade: A
```

---

## ៧. Functions — អនុគមន៍

### Function Declaration

```js
function greet(name) {
  return `សួស្តី ${name}!`;
}

console.log(greet("ចន្ទ​ី")); // "សួស្តី ចន្ទី!"
```

### Function Expression

```js
const add = function (a, b) {
  return a + b;
};

console.log(add(3, 7)); // 10
```

### Arrow Function (ទំនើប & ខ្លី)

```js
// ធម្មតា
const multiply = (a, b) => {
  return a * b;
};

// ខ្លីជាងនេះ (return ដោយស្វ័យប្រវត្តិ)
const square = (n) => n * n;
const double = (n) => n * 2;

console.log(square(5));  // 25
console.log(double(4));  // 8
```

### Default Parameters

```js
function welcome(name = "ភ្ញៀវ") {
  return `សូមស្វាគមន៍ ${name}!`;
}

console.log(welcome("ម៉ករា")); // "សូមស្វាគមន៍ ម៉ករា!"
console.log(welcome());        // "សូមស្វាគមន៍ ភ្ញៀវ!"
```

### Rest Parameters

```js
function sum(...numbers) {
  return numbers.reduce((total, n) => total + n, 0);
}

console.log(sum(1, 2, 3));       // 6
console.log(sum(10, 20, 30, 40)); // 100
```

---

## ៨. Arrays — អារ៉េ

```js
const fruits = ["ស្វាយ", "ចេក", "ទុំបាវ", "ល្ហុង"];

// ចូលប្រើ element
console.log(fruits[0]); // "ស្វាយ"
console.log(fruits.length); // 4

// បន្ថែម / លុប
fruits.push("ផ្លែប៉ោម");     // បន្ថែមចុងក្រោយ
fruits.pop();               // លុបចុងក្រោយ
fruits.unshift("ស្វាយចន្ទី"); // បន្ថែមដំបូង
fruits.shift();             // លុបដំបូង
```

### Array Methods សំខាន់ៗ

```js
const numbers = [1, 2, 3, 4, 5, 6, 7, 8];

// map — បំប្លែងរាល់ element
const doubled = numbers.map((n) => n * 2);
console.log(doubled); // [2, 4, 6, 8, 10, 12, 14, 16]

// filter — ត្រងរើស elements
const evens = numbers.filter((n) => n % 2 === 0);
console.log(evens); // [2, 4, 6, 8]

// reduce — ប្រមូលផ្តុំទៅជាតម្លៃតែមួយ
const total = numbers.reduce((sum, n) => sum + n, 0);
console.log(total); // 36

// find — រកទីមួយដែលត្រូវ
const firstBig = numbers.find((n) => n > 5);
console.log(firstBig); // 6

// some / every
console.log(numbers.some((n) => n > 7));  // true (មានតែមួយ)
console.log(numbers.every((n) => n > 0)); // true (ទាំងអស់)

// includes
console.log(numbers.includes(3)); // true

// flat — លើ Array ស្រទាប់
const nested = [1, [2, 3], [4, [5, 6]]];
console.log(nested.flat());    // [1, 2, 3, 4, [5, 6]]
console.log(nested.flat(2));   // [1, 2, 3, 4, 5, 6]

// sort
const names = ["ចន្ទ​ី", "ដារ៉ា", "វិចិត្រ"];
names.sort();
console.log(names); // ["ចន្ទ​ី", "ដារ៉ា", "វិចិត្រ"]
```

### Destructuring Arrays

```js
const [first, second, ...rest] = [10, 20, 30, 40, 50];

console.log(first);  // 10
console.log(second); // 20
console.log(rest);   // [30, 40, 50]
```

---

## ៩. Objects — វត្ថុ

```js
const person = {
  name: "ម៉ករា",
  age: 28,
  job: "Developer",
  address: {
    city: "ភ្នំពេញ",
    country: "កម្ពុជា",
  },
};

// ចូលប្រើ property
console.log(person.name);           // "ម៉ករា"
console.log(person.address.city);   // "ភ្នំពេញ"
console.log(person["age"]);         // 28

// បន្ថែម / ផ្លាស់ប្តូរ
person.email = "makara@example.com"; // បន្ថែម
person.age = 29;                     // ផ្លាស់ប្តូរ

// លុប property
delete person.job;
```

### Destructuring Objects

```js
const { name, age, address: { city } } = person;

console.log(name); // "ម៉ករា"
console.log(age);  // 29
console.log(city); // "ភ្នំពេញ"
```

### Spread Operator

```js
const defaults = { theme: "light", lang: "km", fontSize: 16 };
const userSettings = { lang: "en", fontSize: 18 };

// បញ្ចូលគ្នា (userSettings overrides defaults)
const settings = { ...defaults, ...userSettings };
console.log(settings);
// { theme: "light", lang: "en", fontSize: 18 }
```

### Object Methods ដែលមានប្រយោជន៍

```js
const car = { brand: "Toyota", model: "Camry", year: 2023 };

console.log(Object.keys(car));   // ["brand", "model", "year"]
console.log(Object.values(car)); // ["Toyota", "Camry", 2023]
console.log(Object.entries(car));
// [["brand", "Toyota"], ["model", "Camry"], ["year", 2023]]

// Clone object
const carCopy = { ...car };
const carCopy2 = Object.assign({}, car);
```

---

## ១០. DOM — ការគ្រប់គ្រងទំព័រ Web

DOM (Document Object Model) អនុញ្ញាតឱ្យ JS ផ្លាស់ប្តូរ HTML

```js
// ស្វែងរក elements
const title = document.getElementById("title");
const buttons = document.querySelectorAll(".btn");
const firstParagraph = document.querySelector("p");

// ផ្លាស់ប្តូរ content
title.textContent = "ចំណងជើងថ្មី";
title.innerHTML = "<strong>ចំណងជើង Bold</strong>";

// ផ្លាស់ប្តូរ style
title.style.color = "blue";
title.style.fontSize = "24px";

// CSS classes
title.classList.add("highlight");
title.classList.remove("old-class");
title.classList.toggle("active");

// បង្កើត element ថ្មី
const newDiv = document.createElement("div");
newDiv.textContent = "ខ្ញុំជា Div ថ្មី";
newDiv.className = "card";
document.body.appendChild(newDiv);

// លុប element
const oldElement = document.getElementById("remove-me");
oldElement.remove();

// getAttribute / setAttribute
const link = document.querySelector("a");
link.setAttribute("href", "https://example.com");
console.log(link.getAttribute("href"));
```

---

## ១១. Events — ព្រឹត្តិការណ៍

```js
const button = document.getElementById("myBtn");

// ស្តាប់ event
button.addEventListener("click", function () {
  console.log("ប៊ូតុងត្រូវបានចុច!");
});

// ជាមួយ Arrow Function
button.addEventListener("click", () => {
  alert("ចុចហើយ! 🎉");
});

// Event Object
button.addEventListener("click", (event) => {
  console.log(event.target);     // element ដែលត្រូវចុច
  console.log(event.type);       // "click"
  event.preventDefault();        // បញ្ឈប់ default behavior
});

// Events ប្រភេទផ្សេងៗ
document.addEventListener("keydown", (e) => {
  console.log(`គ្រាប់ចុច: ${e.key}`);
});

const input = document.querySelector("input");
input.addEventListener("input", (e) => {
  console.log(`ពាក្យ: ${e.target.value}`);
});

window.addEventListener("load", () => {
  console.log("ទំព័របានផ្ទុករួច!");
});
```

---

## ១២. Promises & Async/Await

### Promises

```js
// បង្កើត Promise
const fetchData = new Promise((resolve, reject) => {
  const success = true;

  if (success) {
    resolve("ទទួលបានទិន្នន័យ! ✅");
  } else {
    reject("មានបញ្ហា! ❌");
  }
});

// ប្រើ Promise
fetchData
  .then((data) => console.log(data))
  .catch((error) => console.error(error))
  .finally(() => console.log("រួចរាល់!"));
```

### Async / Await (ងាយស្រួលជាង)

```js
// ទម្រង់ Async Function
async function getUser(id) {
  try {
    const response = await fetch(`https://api.example.com/users/${id}`);
    const user = await response.json();
    return user;
  } catch (error) {
    console.error("ការទាញទិន្នន័យបានបរាជ័យ:", error);
  }
}

// ហៅប្រើ
getUser(1).then((user) => console.log(user));

// ឬ inside async function ផ្សេងទៀត
async function main() {
  const user = await getUser(1);
  console.log(user.name);
}

main();
```

### Promise.all — ហៅ parallel

```js
async function loadAllData() {
  const [users, posts, comments] = await Promise.all([
    fetch("/api/users").then((r) => r.json()),
    fetch("/api/posts").then((r) => r.json()),
    fetch("/api/comments").then((r) => r.json()),
  ]);

  console.log({ users, posts, comments });
}
```

---

## ១៣. Classes — OOP

### Class មូលដ្ឋាន

```js
class Animal {
  constructor(name, sound) {
    this.name = name;
    this.sound = sound;
  }

  speak() {
    return `${this.name} និយាយថា: ${this.sound}`;
  }

  // Static method (ហៅដោយមិនចាំបាច់ new)
  static describe() {
    return "ខ្ញុំជា Animal class";
  }
}

const dog = new Animal("ឆ្កែ", "ហ៊ូ! ហ៊ូ!");
console.log(dog.speak());          // "ឆ្កែ និយាយថា: ហ៊ូ! ហ៊ូ!"
console.log(Animal.describe());    // "ខ្ញុំជា Animal class"
```

### Inheritance — ការទទួលមរតក

```js
class Dog extends Animal {
  constructor(name, breed) {
    super(name, "ហ៊ូ! ហ៊ូ!"); // ហៅ constructor ឪពុក
    this.breed = breed;
  }

  fetch(item) {
    return `${this.name} ជា ${this.breed} ទៅយក ${item}!`;
  }
}

const myDog = new Dog("ស្នេហ", "Golden Retriever");
console.log(myDog.speak());         // "ស្នេហ និយាយថា: ហ៊ូ! ហ៊ូ!"
console.log(myDog.fetch("បាល់"));   // "ស្នេហ ជា Golden Retriever ទៅយក បាល់!"
```

### Private Fields (ការការពារទិន្នន័យ)

```js
class BankAccount {
  #balance = 0; // private — ចូលប្រើពីខាងក្រៅមិនបានទេ

  constructor(owner) {
    this.owner = owner;
  }

  deposit(amount) {
    if (amount > 0) this.#balance += amount;
  }

  withdraw(amount) {
    if (amount <= this.#balance) {
      this.#balance -= amount;
      return true;
    }
    return false;
  }

  getBalance() {
    return this.#balance;
  }
}

const account = new BankAccount("វិចិត្រ");
account.deposit(500);
console.log(account.getBalance()); // 500
// account.#balance  ❌ Error!
```

---

## ១៤. Modules — ES Modules

### Export

```js
// math.js
export const PI = 3.14159;

export function add(a, b) {
  return a + b;
}

export function multiply(a, b) {
  return a * b;
}

// Default export (មួយក្នុង file)
export default function greet(name) {
  return `Hello, ${name}!`;
}
```

### Import

```js
// app.js

// Named imports
import { PI, add, multiply } from "./math.js";

// Default import
import greet from "./math.js";

// Import ទាំងអស់
import * as Math from "./math.js";

console.log(PI);           // 3.14159
console.log(add(2, 3));    // 5
console.log(greet("ដារ៉ា")); // "Hello, ដារ៉ា!"
console.log(Math.multiply(4, 5)); // 20
```

---

## ១៥. Error Handling — ការដោះស្រាយកំហុស

```js
// try / catch / finally
function divide(a, b) {
  if (b === 0) {
    throw new Error("មិនអាចចែកនឹង 0 បានទេ!");
  }
  return a / b;
}

try {
  const result = divide(10, 0);
  console.log(result);
} catch (error) {
  console.error("❌ កំហុស:", error.message);
} finally {
  console.log("✅ ដំណើរការបានបញ្ចប់");
}

// Custom Error
class ValidationError extends Error {
  constructor(message, field) {
    super(message);
    this.name = "ValidationError";
    this.field = field;
  }
}

function validateEmail(email) {
  if (!email.includes("@")) {
    throw new ValidationError("Email មិនត្រឹមត្រូវ", "email");
  }
  return true;
}

try {
  validateEmail("invalid-email");
} catch (error) {
  if (error instanceof ValidationError) {
    console.error(`Field "${error.field}": ${error.message}`);
  }
}
```

---

## ១៦. Advanced Topics — ប្រធានបទកម្រិតខ្ពស់

### Closures

```js
// Function ដែលចងចាំ scope ខាងក្រៅ
function makeCounter() {
  let count = 0; // Private variable

  return {
    increment: () => ++count,
    decrement: () => --count,
    getCount: () => count,
  };
}

const counter = makeCounter();
counter.increment();
counter.increment();
counter.increment();
counter.decrement();
console.log(counter.getCount()); // 2
```

### Higher-Order Functions

```js
// Function ដែលទទួល function ជា argument
function applyTwice(fn, value) {
  return fn(fn(value));
}

const double = (n) => n * 2;
console.log(applyTwice(double, 3)); // 12  (3 → 6 → 12)

// Function ដែល return function
function multiplier(factor) {
  return (number) => number * factor;
}

const triple = multiplier(3);
const quadruple = multiplier(4);

console.log(triple(5));    // 15
console.log(quadruple(5)); // 20
```

### Currying

```js
// បំប្លែង function(a, b, c) → function(a)(b)(c)
const curry = (fn) => {
  return function curried(...args) {
    if (args.length >= fn.length) {
      return fn(...args);
    }
    return (...moreArgs) => curried(...args, ...moreArgs);
  };
};

const add = (a, b, c) => a + b + c;
const curriedAdd = curry(add);

console.log(curriedAdd(1)(2)(3)); // 6
console.log(curriedAdd(1, 2)(3)); // 6
console.log(curriedAdd(1)(2, 3)); // 6
```

### Generators

```js
function* numberGenerator() {
  yield 1;
  yield 2;
  yield 3;
  yield 4;
}

const gen = numberGenerator();
console.log(gen.next().value); // 1
console.log(gen.next().value); // 2
console.log(gen.next().value); // 3

// Infinite generator
function* infiniteCounter(start = 0) {
  while (true) {
    yield start++;
  }
}

const counter2 = infiniteCounter(10);
console.log(counter2.next().value); // 10
console.log(counter2.next().value); // 11
console.log(counter2.next().value); // 12
```

### Proxy & Reflect

```js
const handler = {
  get(target, key) {
    console.log(`អានតម្លៃ: ${key}`);
    return Reflect.get(target, key);
  },
  set(target, key, value) {
    console.log(`កំណត់ ${key} = ${value}`);
    return Reflect.set(target, key, value);
  },
};

const obj = new Proxy({}, handler);
obj.name = "JavaScript";  // "កំណត់ name = JavaScript"
console.log(obj.name);    // "អានតម្លៃ: name" → "JavaScript"
```

### WeakMap & WeakSet

```js
// WeakMap — key ត្រូវជា object, GC-friendly
const cache = new WeakMap();

function processUser(user) {
  if (cache.has(user)) {
    return cache.get(user);
  }

  const result = { processed: true, data: user.name.toUpperCase() };
  cache.set(user, result);
  return result;
}
```

### Symbol

```js
// Symbol — unique identifier
const id = Symbol("id");
const userId = Symbol("id");

console.log(id === userId); // false (unique តែងតែ)

const user = {
  name: "ម៉ករា",
  [id]: 12345, // hidden property
};

console.log(user[id]);         // 12345
console.log(Object.keys(user)); // ["name"] — Symbol មើមិនឃើញ
```

### Optional Chaining & Nullish Coalescing

```js
const user = {
  profile: {
    address: {
      city: "ភ្នំពេញ",
    },
  },
};

// Optional chaining (?.) — មិន error ទោះ undefined
console.log(user?.profile?.address?.city);     // "ភ្នំពេញ"
console.log(user?.settings?.theme);            // undefined (មិន error)

// Nullish coalescing (??) — default ពេល null/undefined
const theme = user?.settings?.theme ?? "light";
console.log(theme); // "light"

// vs || (OR) — || ក៏ replace false, 0, "" ផងដែរ
const count = 0;
console.log(count || 10);  // 10  (0 ត្រូវបាន replace ❌)
console.log(count ?? 10);  // 0   (0 ត្រូវបានរក្សា ✅)
```

---

## 🛠️ Best Practices (គន្លឹះ)

```js
// ✅ ប្រើ const ជានិច្ច លុះត្រារ៉變ចាំ
const API_URL = "https://api.example.com";

// ✅ ប្រើ descriptive names
const getUserById = (id) => fetch(`${API_URL}/users/${id}`);

// ✅ Arrow functions សម្រាប់ callbacks
const squares = [1, 2, 3].map((n) => n ** 2);

// ✅ Destructuring ជំនួស property access ច្រើនដង
const { name, email, age } = currentUser;

// ✅ Template literals ជំនួស string concatenation
const message = `សួស្តី ${name}, អ្នកមាន ${age} ឆ្នាំ`;

// ✅ Optional chaining ការពារ errors
const city = user?.address?.city ?? "មិនស្គាល់";

// ✅ Error handling ច្បាស់លាស់
async function fetchUsers() {
  try {
    const res = await fetch("/api/users");
    if (!res.ok) throw new Error(`HTTP ${res.status}`);
    return await res.json();
  } catch (err) {
    console.error("fetchUsers failed:", err.message);
    return [];
  }
}
```

---

## 📚 ធនធានសម្រាប់រៀនបន្ត

| ធនធាន | Link |
|--------|------|
| MDN Web Docs | [developer.mozilla.org](https://developer.mozilla.org) |
| JavaScript.info | [javascript.info](https://javascript.info) |
| freeCodeCamp | [freecodecamp.org](https://freecodecamp.org) |
| Eloquent JavaScript | [eloquentjavascript.net](https://eloquentjavascript.net) |
| Node.js | [nodejs.org](https://nodejs.org) |

---

<div align="center">

បង្កើតដោយ ❤️ សម្រាប់អ្នកសរសេរកូដខ្មែរ

**Happy Coding! 🚀**

</div>
