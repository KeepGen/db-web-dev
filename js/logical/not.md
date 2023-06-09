# Логический оператор `НЕ` [ ! ]

Оператор НЕ представлен восклицательным знаком `!`

Синтаксис довольно прост:

```js
result = !value;
```

Оператор принимает один аргумент и выполняет следующие действия:

- Сначала приводит аргумент к логическому типу `true/false`.
- Затем возвращает противоположное значение.

Например:

```js
alert( !true ); // false
alert( !0 ); // true
```

В частности, двойное НЕ `!!` используют для преобразования значений к логическому типу:

```js
alert( !!"non-empty string" ); // true
alert( !!null ); // false
```

То есть первое НЕ преобразует значение в логическое значение и возвращает обратное, а второе НЕ снова инвертирует его. В конце мы имеем простое преобразование значения в логическое.

Есть немного более подробный способ сделать то же самое – встроенная функция `Boolean`:

```js
alert( Boolean("non-empty string") ); // true
alert( Boolean(null) ); // false
```

Приоритет НЕ `!` является наивысшим из всех логических операторов, поэтому он всегда выполняется первым, перед `&&` или `||`.

---

## Задачи по теме

<details>
<summary>Вопрос [пример...]</summary>

Ответ
</details>

---
