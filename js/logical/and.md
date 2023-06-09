# Логический оператор `И` [ && ]

::: danger 🟥 ВАЖНО
Оператор И `&&` требует правдивости в обоих выражениях
:::

Оператор И пишется как два амперсанда `&&`:

```js
result = a && b;
```

В традиционном программировании И возвращает `true`, если оба аргумента истинны, а иначе – `false`:

```js
alert( true && true );   // true
alert( false && true );  // false
alert( true && false );  // false
alert( false && false ); // false
```

Пример с `if`:

```js
let hour = 12;
let minute = 30;

if (hour == 12 && minute == 30) {
alert( 'The time is 12:30' );
}
```

Как и в случае с ИЛИ, любое значение допускается в качестве операнда И:

```js
if (1 && 0) { // вычисляется как true && false
alert( "не сработает, так как результат ложный" );
}
```

И `&&` находит первое ложное значение
При нескольких подряд операторах И:

```js
result = value1 && value2 && value3;
```

Оператор `&&` выполняет следующие действия:

Вычисляет операнды слева направо.
Каждый операнд преобразует в логическое значение. Если результат `false`, останавливается и возвращает исходное значение этого операнда.
Если все операнды были истинными, возвращается последний.
Другими словами, И возвращает первое ложное значение. Или последнее, если ничего не найдено.

Вышеуказанные правила схожи с поведением ИЛИ. Разница в том, что И возвращает первое ложное значение, а ИЛИ — первое истинное.

Примеры:

```js
// Если первый операнд истинный,
// И возвращает второй:
alert( 1 && 0 ); // 0
alert( 1 && 5 ); // 5

// Если первый операнд ложный,
// И возвращает его. Второй операнд игнорируется
alert( null && 5 ); // null
alert( 0 && "no matter what" ); // 0
```

Можно передать несколько значений подряд. В таком случае возвратится первое «ложное» значение, на котором остановились вычисления.

```js
alert( 1 && 2 && null && 3 ); // null
```

Когда все значения верны, возвращается последнее

```js
alert( 1 && 2 && 3 ); // 3
```

::: danger ℹ️ Приоритет оператора `&&` больше, чем у `||`
Приоритет оператора И && больше, чем ИЛИ ||, так что он выполняется раньше.

Таким образом, код a && b || c && d по существу такой же, как если бы выражения && были в круглых скобках: (a && b) || (c && d).
:::

Как и оператор ИЛИ `||`, И `&&` иногда может заменять `if`.

К примеру:

```js
let x = 1;

(x > 0) && alert( 'Greater than zero!' );
```

Действие в правой части `&&` выполнится только в том случае, если до него дойдут вычисления. То есть, `alert` сработает, если в левой части `(x > 0)` будет true.

Получился аналог:

```js
let x = 1;

if (x > 0) {
alert( 'Greater than zero!' );
}
```

Однако, как правило, вариант с `if` лучше читается и воспринимается.

Он более очевиден, поэтому лучше использовать его.

---

## Задачи по теме

<details>
<summary>Вопрос [пример...]</summary>

Ответ
</details>

---
