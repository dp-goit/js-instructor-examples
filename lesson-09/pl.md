# Moduł 5 - Lekcja 9 - Kontekst wywołania funkcji i słowo kluczowe this

## Zadanie 1 - Warsztat jubilerski

Napisz metodę `calcTotalPrice(stoneName)`, która przyjmuje nazwę kamienia, oblicza i zwraca całkowity koszt kamieni o tej nazwie, ceny i ilości z właściwości `stones`.

```js
const chopShop = {
  stones: [
    { name: 'Emerald', price: 1300, quantity: 4 },
    { name: 'Diamond', price: 2700, quantity: 3 },
    { name: 'Sapphire', price: 1400, quantity: 7 },
    { name: 'Ruby', price: 800, quantity: 2 },
  ],
  calcTotalPrice(stoneName) {},
};

console.log(chopShop.calcTotalPrice('Emerald')); // 5200
console.log(chopShop.calcTotalPrice('Diamond')); // 8100
console.log(chopShop.calcTotalPrice('Sapphire')); // 9800
console.log(chopShop.calcTotalPrice('Ruby')); // 1600
```

## Zadanie 2 -  Książka telefoniczna

Przerób metody obiektu `phonebook`, aby kod działał.

```js
const phonebook = {
  contacts: [],
  add(contact) {
    const newContact = {
      list: 'default',
      ...contact,
      id: generateId(),
      createdAt: getDate(),
    };
    contacts.push(newContact);
  },
  generateId() {
    return '_' + Math.random().toString(36).substr(2, 9);
  },
  getDate() {
    return Date.now();
  },
};

console.log(
  phonebook.add({
    name: 'Mango',
    email: 'mango@mail.com',
    list: 'friends',
  })
);
console.log(
  phonebook.add({
    name: 'Poly',
    email: 'poly@hotmail.com',
  })
);
```

## Zadanie 3 - Kalkulator

Utwórz obiekt `calculator` z trzema metodami:

- `read(a, b)`- przyjmuje dwie wartości i przechowuje je jako właściwości obiektu.
- `add()` - zwraca sumę przechowywanych wartości.
- `mult()` - mnoży przechowywane wartości i zwraca wynik.

```js
const calculator = {};
```
