## Programming Paradigms

### Declarative Programming

- You say **what you want**, not how to get it.
- e.g. `background-color: tomato;` in CSS
```js
const numbers = [1, 2, 3, 4];
const doubled = numbers.map(n => n * 2);
```

### Imperative Programming

- You tell the computer **how** to do something, step-by-step.
- e.g. setting variables, loops, conditionals, etc.
- Functions passed as arguments, functions returned from other functions.
```js
const numbers = [1, 2, 3, 4];
const doubled = [];
for (let i = 0; i < numbers.length; i++) {
  doubled.push(numbers[i] * 2); // imperative
}
```

### Functional Programming

- Functions are **first-class citizens** (can be stored in variables, passed around).
- Avoids changing states or mutable data.
- Relies heavily on **pure functions** and **higher-order functions**.
```js
const add = (a, b) => a + b; // pure function
const apply = (fn, x, y) => fn(x, y); // higher-order function
console.log(apply(add, 3, 5)); // 8
```
