# Moduł 5 - Lekcja 10 - Prototypy i klasy

## Zadanie 1 - Bloger

Napisz klasę `Blogger`, aby stworzyć obiekt blogera z następującymi
właściwościami:

- `email` - adres e-mail
- `age` - wiek
- `numberOfPosts` - liczba postów
- `topics` - tablica tematów, w których specjalizuje się bloger

Klasa oczekuje jednego parametru - obiektu ustawień z takimi samymi
właściwościami.

Dodaj metodę `getInfo()`, która zwraca ciąg znaków:
`Użytkownik ${email} ma ${wiek} lat, i ma ${liczba postów}` postów.

Dodaj metodę updatePostCount(value), która w parametrze value przyjmuje liczbę
postów do dodania do użytkownika.

```js
const mango = new User({
  name: 'mango@mail.com',
  age: 24,
  numberOfPosts: 20,
  topics: ['tech', 'cooking'],
});
console.log(mango.getInfo()); // Użytkownik mango@mail.com ma 24 lat, i ma  20 postów.
mango.updatePostCount(5);
console.log(mango.getInfo()); // Użytkownik mango@mail.com ma 24 lat, i ma 25 postów.

const poly = new User({
  name: 'poly@mail.com',
  age: 19,
  numberOfPosts: 17,
  topics: ['sports', 'gaming', 'health'],
});
console.log(poly.getInfo()); // Użytkownik poly@mail.com ma 19 lat, i ma 17 postów.
poly.updatePostCount(4);
console.log(poly.getInfo()); // Użytkownik poly@mail.com ma 19 lat, i ma 21 postów.
```

## Zadanie 2 - Magazyn

Napisz klasę `Storage`, która tworzy obiekty do zarządzania magazynem towarów. Przy wywołaniu otrzyma jeden argument - początkową tablicę towarów i zapisze ją do właściwości `items`.

Dodaj metody klasy:

- `getItems()` - zwraca tablicę produktów.
- `addItem(item)` - przyjmuje nowy produkt i dodaje go do obecnych.
- `removeItem(item)` - przyjmuje produkt i, jeśli istnieje, usuwa go z aktualnych.

```js
const storage = new Storage(['🍎', '🍋', '🍇', '🍑']);

const items = storage.getItems();
console.table(items); // [ '🍎', '🍋', '🍇', '🍑' ]

storage.addItem('🍌');
console.table(storage.items); // [ '🍎', '🍋', '🍇', '🍑', '🍌' ]

storage.removeItem('🍋');
console.table(storage.items); // [ '🍎', '🍇', '🍑', '🍌' ]
```

## Zadanie 3 - Użytkownik

Napisz klasę `User`, która tworzy obiekt z właściwościami `login` i `email`. Zadeklaruj prywatne właściwości `#login` i `#email`, które można uzyskać za pomocą gettera i settera `login` i `email`.

```js
const mango = new User({
  login: 'Mango',
  email: 'mango@dog.woof',
});

console.log(mango.login); // Mango
mango.login = 'Mangodoge';
console.log(mango.login); // Mangodoge

const poly = new User({
  login: 'Poly',
  email: 'poly@mail.com',
});

console.log(poly.login); // Poly
poly.login = 'Polycutie';
console.log(poly.login); // Polycutie
```

## Zadanie 4 - Notatki

Napisz klasę `Notes`, która zarządza kolekcją notatek w właściwości `items`. Notatka to obiekt z właściwościami `text` i `priority`. Dodaj właściwość statyczną `Priority` do klasy, która będzie przechowywać obiekt z priorytetami.

```js
{
  LOW: 'low',
  NORMAL: 'normal',
  HIGH: 'high'
}
```

Dodaj metody `addNote(note)`, `removeNote(text)` i `updatePriority(text, newPriority)`.

```js
const myNotes = new Notes([]);

myNotes.addNote({ text: 'My first note', priority: Notes.Priority.LOW });
console.log(myNotes.items);

myNotes.addNote({
  text: 'My second note',
  priority: Notes.Priority.NORMAL,
});
console.log(myNotes.items);

myNotes.removeNote('My first note');
console.log(myNotes.items);

myNotes.updateNote('My second note', Notes.Priority.HIGH);
console.log(myNotes.items);
```

## Zadanie 5 - Przełącznik

Napisz klasę `Toggle`, która przyjmuje obiekt ustawień `{isOpen: boolean}` i deklaruje jedną właściwość `on` - stan włączony/wyłączony (true/false). Domyślnie wartość właściwości `on` powinna być `false`.

```js
const firstToggle = new Toggle({ isOpen: true });
console.group('firstToggle');
console.log(firstToggle.on);
firstToggle.toggle();
console.log(firstToggle.on);
console.groupEnd('firstToggle');

const secondToggle = new Toggle();
console.group('secondToggle');
console.log(secondToggle.on);
secondToggle.toggle();
console.log(secondToggle.on);
console.groupEnd('secondToggle');
```
