## Immutable Way (Array) - Add

```js
const books = [
  { id: 1, title: 'Eat That Frog!'},
  { id: 2, title: 'Thinking, Fast and Slow'}
];

const book = { id: 3, title: 'The Millionaire Fastlane'};

const updatedBooks = [ ...books, book];

console.log('ORIGINAL:', books);
console.log('UPDATED: ', updatedBooks);
```

output: 
```
Info: Start process (7:20:12 PM)
ORIGINAL: [
  { id: 1, title: 'Eat That Frog!' },
  { id: 2, title: 'Thinking, Fast and Slow' }
]
UPDATED:  [
  { id: 1, title: 'Eat That Frog!' },
  { id: 2, title: 'Thinking, Fast and Slow' },
  { id: 3, title: 'The Millionaire Fastlane' }
]
Info: End process (7:20:12 PM)
```

---

## Immutable Way (Array) - Update

```js
const books = [
  { id: 1, title: 'Eat That Frog!'},
  { id: 2, title: 'Thinking, Fast and Slow'}
];


const updatedBooks = books.map(updateTitle);

function updateTitle(book) {
  if (book.id === 2) {
    return { ...book, title: 'The Millionaire Fastlane' };
  }
  return book;
}

console.log('ORIGINAL:', books);
console.log('UPDATED: ', updatedBooks);
```

output: 
```
Info: Start process (7:23:38 PM)
ORIGINAL: [
  { id: 1, title: 'Eat That Frog!' },
  { id: 2, title: 'Thinking, Fast and Slow' }
]
UPDATED:  [
  { id: 1, title: 'Eat That Frog!' },
  { id: 2, title: 'The Millionaire Fastlane' }
]
Info: End process (7:23:38 PM)

```

---

## Immutable Way (Array) - Delete

```js
const books = [
  { id: 1, title: 'Eat That Frog!'},
  { id: 2, title: 'Thinking, Fast and Slow'},
  { id: 3, title: 'The Millionaire Fastlane'}
];


const filterBooks = books.filter(deleteBook);

function deleteBook(book) {
  return book.id !== 2;
}

console.log('ORIGINAL:', books);
console.log('UPDATED: ', filterBooks);
```

output: 
```
Info: Start process (7:26:46 PM)
ORIGINAL: [
  { id: 1, title: 'Eat That Frog!' },
  { id: 2, title: 'Thinking, Fast and Slow' },
  { id: 3, title: 'The Millionaire Fastlane' }
]
UPDATED:  [
  { id: 1, title: 'Eat That Frog!' },
  { id: 3, title: 'The Millionaire Fastlane' }
]
Info: End process (7:26:46 PM)

```

---

## Immutable Way (Array) - Sum

```js
const books = [
  { id: 1, title: 'Eat That Frog!', price: 250},
  { id: 2, title: 'Thinking, Fast and Slow', price: 250},
  { id: 3, title: 'The Millionaire Fastlane', price: 400}
];


const sumPrice = books.reduce((result, book) => {
  return result + book.price;
}, 0);


console.log('ORIGINAL:', books);
console.log('sumPrice: ', sumPrice);
```

output: 
```
Info: Start process (7:29:24 PM)
ORIGINAL: [
  { id: 1, title: 'Eat That Frog!', price: 250 },
  { id: 2, title: 'Thinking, Fast and Slow', price: 250 },
  { id: 3, title: 'The Millionaire Fastlane', price: 400 }
]
sumPrice:  900
Info: End process (7:29:24 PM)

```

---

## Summary

- Add -> spread syntax
- Update -> map()
- Delete -> filter()
- sum -> reduce()