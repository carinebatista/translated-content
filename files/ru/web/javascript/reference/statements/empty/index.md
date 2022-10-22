---
title: Пустая инструкция
slug: Web/JavaScript/Reference/Statements/Empty
tags:
  - Statement, инструкция, пустая инструкция
translation_of: Web/JavaScript/Reference/Statements/Empty
---
{{jsSidebar("Statements")}}

**Пустая инструкция** используется, когда инструкция не нужна, хотя синтаксис JavaScript будет предполагать её.

## Синтаксис

```
;
```

## Описание

Пустая инструкция - точка с запятой (;) оповещает о том, что ни одно выражение не будет выполняться, даже если синтаксис JavaScript ожидает этого.

Противоположное поведение, где вы хотите использовать несколько заявлений, но JavaScript позволяет только одно, можно сделать используя [блок](/ru/docs/Web/JavaScript/Reference/Statements/block); он комбинирует несколько инструкций в одно.

## Примеры

Пустая инструкция используется в выражениях циклов. Смотрите следующий пример с пустым телом цикла:

```js
var arr = [1, 2, 3];

// Приравняет все значения массива к 0
for (i = 0; i < arr.length; arr[i++] = 0) /* выражения */ ;

console.log(arr)
// [0, 0, 0]
```

**Заметьте:** Это хорошая идея: комментировать намеренное использование пустых инструкций, т.к. не очевидно отличить их от нормальной точки с запятой. В следующем примере использование, вероятно, ненамеренное:

```js
if (condition);       // Внимание, этот if ничего не делает!
   killTheUniverse()  // Это всегда выполняется!!!
```

Другой пример: [`if...else`](/ru/docs/Web/JavaScript/Reference/Statements/if...else) без фигурных скобок (`{}`). Если `three` истинно, ничего не произойдёт, `four` не важна, и функция `launchRocket()` тоже не запустится.

```js
if (one)
  doOne();
else if (two)
  doTwo();
else if (three)
  ; // nothing here
else if (four)
  doFour();
else
  launchRocket();
```

## Спецификации

| Спецификация                                                                             | Статус                       | Комментарий             |
| ---------------------------------------------------------------------------------------- | ---------------------------- | ----------------------- |
| {{SpecName('ESDraft', '#sec-empty-statement', 'Empty statement')}} | {{Spec2('ESDraft')}} |                         |
| {{SpecName('ES6', '#sec-empty-statement', 'Empty statement')}}     | {{Spec2('ES6')}}         |                         |
| {{SpecName('ES5.1', '#sec-12.3', 'Empty statement')}}                 | {{Spec2('ES5.1')}}     |                         |
| {{SpecName('ES3', '#sec-12.3', 'Empty statement')}}                     | {{Spec2('ES3')}}         |                         |
| {{SpecName('ES1', '#sec-12.3', 'Empty statement')}}                     | {{Spec2('ES1')}}         | Изначальное определение |

## Поддержка браузерами

{{Compat}}

## Смотрите также

- {{jsxref("Statements/block", "Блок")}}