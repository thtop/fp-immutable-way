## Immutable way (Object) - Add

```js
const book = {
  id: 1,
  title: 'Eat That Frog!'
}

const updateBook = {
  ...book, // spread syntax
  price: 500
}

console.log('ORIGINAL: ', book);
console.log('UPDATED: ', updateBook);
```

**output:**
```
Info: Start process (7:05:20 PM)
ORIGINAL:  { id: 1, title: 'Eat That Frog!' }
UPDATED:  { id: 1, title: 'Eat That Frog!', price: 500 }
Info: End process (7:05:21 PM)

```

---

## Immutable way (Object) - Update

```js
const book = {
  id: 1,
  title: 'Eat That Frog!'
}

const updateBook = {
  ...book, // spread syntax
  title: 'Thinking, Fast and Slow'
}

console.log('ORIGINAL: ', book);
console.log('UPDATED: ', updateBook);
```

**output:**
```
Info: Start process (7:06:51 PM)
ORIGINAL:  { id: 1, title: 'Eat That Frog!' }
UPDATED:  { id: 1, title: 'Thinking, Fast and Slow' }
Info: End process (7:06:51 PM)

```

---

## Immutable way (Object) - Delete

```js
const book = {
  id: 1,
  title: 'Eat That Frog!',
  price: 500
}

// destructuring & rest parameter
const { id, ...bookWithoutId } = book;

console.log('ORIGINAL: ', book);
console.log('UPDATED: ', bookWithoutId);
```

**output:**
```
Info: Start process (7:09:24 PM)
ORIGINAL:  { id: 1, title: 'Eat That Frog!', price: 500 }
UPDATED:  { title: 'Eat That Frog!', price: 500 }
Info: End process (7:09:24 PM)
```

## Summary

- Add -> spread syntax
- Update -> spread syntax
- Delete -> destructuring & rest parameter