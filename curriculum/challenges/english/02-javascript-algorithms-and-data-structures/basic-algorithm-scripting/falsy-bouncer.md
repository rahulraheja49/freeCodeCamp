---
id: adf08ec01beb4f99fc7a68f2
title: Falsy Bouncer
challengeType: 1
forumTopicId: 16014
dashedName: falsy-bouncer
---

# --description--

Remove all falsy values from an array. Return a new array and do not mutate the original array.

Falsy values in JavaScript are `false`, `null`, `0`, `""`, `undefined`, and `NaN`.

Hint: Try converting each value to a Boolean.

# --hints--

`bouncer([7, "ate", "", false, 9])` should return `[7, "ate", 9]`.

```js
assert.deepEqual(bouncer([7, 'ate', '', false, 9]), [7, 'ate', 9]);
```

`bouncer(["a", "b", "c"])` should return `["a", "b", "c"]`.

```js
assert.deepEqual(bouncer(['a', 'b', 'c']), ['a', 'b', 'c']);
```

`bouncer([false, null, 0, NaN, undefined, ""])` should return `[]`.

```js
assert.deepEqual(bouncer([false, null, 0, NaN, undefined, '']), []);
```

`bouncer([null, NaN, 1, 2, undefined])` should return `[1, 2]`.

```js
assert.deepEqual(bouncer([null, NaN, 1, 2, undefined]), [1, 2]);
```

`bouncer(['a', false, 0, 'John', 3])` should return `['a', 'John', 3]`.

```js
const arr = ['a', false, 0, 'John', 3];
bouncer(arr);
assert.deepEqual(arr, ['a', false, 0, 'John', 3]);
```

# --seed--

## --seed-contents--

```js
function bouncer(arr) {
  return arr;
}

bouncer([7, "ate", "", false, 9]);
```

# --solutions--

```js
function bouncer(arr) {
  return arr.filter(e => e);
}

bouncer([7, "ate", "", false, 9]);
```
