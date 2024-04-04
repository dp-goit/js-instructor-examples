# Moduł 1. Lekcja 2. Rozgałęzienia, cykle

## Zadanie 1 - Dane wejściowe oraz rozgałęzianie

Korzystając z if..else oraz okna dialogowego prompt, napisz kod, który zapyta: `"What is the official name of JavaScript?"`.

Jeżeli użytkownik odpowie `ECMAScript`, Wyświetl alert `"Correct!"`, w przeciwnym razie - `"Do not know? ECMAScript!"`

## Zadanie 2 - Time display (if...else)

Napisz skrypt, który wyświetli godziny oraz minuty w konsoli jako tekst w formacie: `"14 hours 26 minutes."`.

Jeżeli wartość `minutes` jest równa `0`, wtedy użyj formatu `"14 o'clock"`, bez minut.

```js
const hours = 14;
const minutes = 26;
let timestring;

if (minutes > 0) {
  timestring = `${hours} h. ${minutes} min.`;
} else {
  timestring = `${hours} h.`;
}
console.log(timestring);
```

## Zadanie 3 - Rozgałęzianie

Napisz skrypt, wyświetlający w konsoli tekst `"This is a positive number"`, jeżeli użytkownik wprowadził w oknie dialogowym prompt, liczbę większą od zera. 
Jeżeli użytkownik wprowadzi zero, wyświetl `"This is zero"`.
Jeżeli użytkownik wprowadzi liczbę ujemną wyświetl `"This is a negative number"`.

```js
const userInput = prompt('Enter the number');
```

## Zadanie 4 - Nested branches

Napisz skrypt porównujący wartości zmiennych `a` oraz `b`. Jeżeli obie wartości są większe niż `100`, wyświetl w konsoli większą z nich. W przeciwnym razie wyświetl sumę wartości `b` oraz liczby 512.

```js
const a = 120;
const b = 180;
```

## Zadanie 5 - Formatowanie linków (endsWith)

Napisz skrypt, który sprawdza czy wartość zmiennej `link` kończy się znakiem `/`. jeżeli nie, dodaj ten znak na końcu ciągu znaków `link`. Użyj `if...else`.

```js
let link = 'https://my-site.com/about';
// Write code below this line

// Write code above this line
console.log(link);
```

## Zadanie 6 - Formatowanie linków (includes oraz AND)

Napisz skrypt, który sprawdza czy wartość zmiennej `link` kończy się znakiem `/`. jeżeli nie, dodaj ten znak na końcu ciągu znaków `link`, ale tylko w przypadku, gdy `link` zawiera ciąg `"my-site"`. Użyj `if...else`.


```js
let link = 'https://somesite.com/about';
// Write code below this line

// Write code above this line
console.log(link);
```

## Zadanie 7 - Formatowanie linków (ternary operator)

Zmodyfikuj kod z zadania 4, korzystając z operatora warunkowego ternary.

```js
let link = 'https://somesite.com/about';
if (link.includes('my-site') && !link.endsWith('/')) {
  link += '/';
}
console.log(link);
```

## Zadanie 8 - if...else oraz operatory logiczne 

Napisz skrypt, który zwróci w konsoli tekst w zależności od wartości zmiennej `hours`.

Jeżeli wartość zmiennej `hours`:

- jest mniejsza niż `17`, zwróć `"Pending"`,
- jest większa lub równa `17` oraz mniejsza lub równa `24`, zwróć `"Expires"`,
- jest więszka niż `24`, zwróć `"Overdue"`.

```js
const hours = 10;
```

## Zadanie 9 - Termin przesłania projektu (if...else)

Napisz skrypt, wyświetlający termin przesłania projektu wg wzoru poniżej, używając konstrukcji
`if...else`.

- Jeżeli jest 0 dni: `"Today"`.
- Jeżeli jest 1 dzień: `"Tomorrow"`.
- Jeżeli są 2 dni:  `"The day after tomorrow"`.
- Jeżeli jest 3 lub więcej dni `"Date in the future"`.

```js
const daysUntilDeadline = 5;
// Write code below this line
```

## Zadanie 10 - Project submission deadline (switch)

Zmodyfikuj kod z poprzedniego zadania, wykorzystując instrukcję `switch`.

```js
const daysUntilDeadline = 5;

if (daysUntilDeadline === 0) {
  console.log('Today');
} else if (daysUntilDeadline === 1) {
  console.log('Tomorrow');
} else if (daysUntilDeadline === 2) {
  console.log('The day after tomorrow');
} else {
  console.log('Date in the future');
}
```

## Zadanie 11 - The for loop 

Napisz pętlę for, która wyświetla w konsoli rosnąco liczby podzielne przez 5 z zakresu od `min` do `max`.

```js
const max = 100;
const min = 20;
```

## Zadanie 12 - User Input and Branching 

Napisz skrypt, który zapyta o login używając okna dialogowego prompt i wyświetl wynik w konsoli.

- Jeżeli użytkownik wprowadzi `"Admin"`, wyświetl prompt z pytaniem o hasło.
- Jeżeli użytkownik nie wprowadzi żadnych znaków lub kliknie Esc, wyświetl `"Canceled"`.
- W przeciwnym razie wyświetl `"I don't know you"`.

Hasło sprawdź następująco:

- Jeżeli użytkownik wprowadzi `"I'm an admin"`, wyświetl `"Hello!"`.
- W przeciwnym razie wyświetl `"Wrong password"`.
