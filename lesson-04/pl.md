# Moduł 2 - Lekcja 4 - Funkcje

## Zadanie 1 - BMI

Napisz funkcję `calcBMI(weight, height)`, która obliczy i zwróci BMI użytownika. Aby to zrobić, podziel wagę użytkowinika w kilogramach przez kwadrat wzrostu w metrach.

Waga oraz wzrost będą przekazane do fukncji jako tekst. W związku z tym mogą mieć one format `24.7` oraz `24,7`, przecinek także może być użyty jako separator części ułamkowej.

BMI powinno być zaokrąglone do jednego miejsca po przecinku.

```js
const bmi = calcBMI('88,3', '1.75');
console.log(bmi); // 28.8
```

## Zadanie 2 - Mniejsza liczba

Napisz funkcję `min(a,b)` która zwróci mniejszą z liczb `a` oraz `b`.

```js
console.log(min(2, 5)); // 2
console.log(min(3, -1)); // -1
console.log(min(1, 1)); // 1
```

## Zadanie 3 - Powierzchnia prostokąta

Napisz funkcję `getRectArea(dimensions)`, która obliczy powierzchnię prostokąta, którego długość boków zostanie przekazana w parametrze `dimensions` jako tekst.

Wartości zawsze będą rozdzielone spacjami.

```js
function getRectArea(dimensions) {}

console.log(getRectArea('8 11'));
```

## Zadanie 4 - Wyświetlanie elementów

Napisz funkcję `logItems(items)` która przyjmuje tablicę i korzystając z pętli `for`, wyświetla dla każdego elementu wiadomość w konsoli wg formatu `<item number> - <item value>`. Numereacja elementów rozpoczyna się od `1`.

Na przykład, w tablicy `['Mango', 'Poly', 'Ajax']` dla elementu z indeksem `0` wyświetlimy `1 - Mango` a dla indeksu 2, wyświetlimy `3 - Ajax`.

```js
function logItems(items) {}

logItems(['Mango', 'Poly', 'Ajax']);
logItems(['🍎', '🍇', '🍑', '🍌', '🍋']);
```

## Zadanie 5 - Wyświetlanie kontaktów

Napisz funkcję `printContactsInfo(names, phones)` która wyświetli w konsoli imię oraz numer telefonu. Parametry `names` oraz `phones` zostaną przekazane do funkcji w formie ciągów znaków, rozdzielone przecinkami. Kolejność imion, odpowiada kolejności numerów telefonów oraz zakładamy, że ilość imion i numerów jest taka sama.

```js
function printContactsInfo(names, phones) {}

printContactsInfo(
  'Jacob,William,Solomon,Artemis',
  '89001234567,89001112233,890055566377,890055566300',
);
```

## Zadanie 6 - Szukanie największego elementu

Napisz funkcję `findLargestNumber(numbers)` która zwraca największą liczbę w tablicy.

```js
function findLargestNumber(numbers) {}

console.log(findLargestNumber([2, 17, 94, 1, 23, 37])); // 94
console.log(findLargestNumber([49, 4, 7, 83, 12])); // 83
```

## Zadanie 7 - Średnia wartość

Napisz funkcję `calAverage()` która przyjmuje stałą liczbę argumentów oraz zwraca ich średnią wartość. Zakładamy, że wszystkie argumenty przekazane do funkcji są zawsze liczbami.

```js
function calAverage() {}

console.log(calAverage(1, 2, 3, 4)); // 2.5
console.log(calAverage(14, 8, 2)); // 8
console.log(calAverage(27, 43, 2, 8, 36)); // 23.2
```

## Zadanie 8 - Formatowanie czasu

Napisz funkcję `formatTime(minutes)` która zamieni wartość argumentu `minutes`
(ilość minut) na godzinę w formacie `HH:MM`.

```js
const hours = Math.floor(totalMinutes / 60);
const minutes = totalMinutes % 60;
console.log(hours);
console.log(minutes);

const doubleDigitHours = String(hours).padStart(2, 0);
const doubleDigitMinutes = String(minutes).padStart(2, 0);
console.log(`${doubleDigitHours}:${doubleDigitMinutes}`);

function formatTime(minutes) {}

console.log(formatTime(70)); // "01:10"
console.log(formatTime(450)); // "07:30"
console.log(formatTime(1441)); // "24:01"
```

## Zadanie 9 - Kolekcja kursów (includes, indexOf, push, itd.)

Napisz funkcje do pracy z tablicą `courses`:

- `addCourse(name)` - dodaje nowy kurs na końcu tablicy,
- `removeCourse(name)` - usuwa dany element z tablicy,
- `updateCourse(oldName, newName)` - zmienia nazwę kursu na nową.

```js
const courses = ['HTML', 'CSS', 'JavaScript', 'React', 'PostgreSQL'];

addCourse('Express');
console.log(courses); // ['HTML', 'CSS', 'JavaScript', 'React', 'PostgreSQL', 'Express']
addCourse('CSS'); // 'You already have this course'

removeCourse('React');
console.log(courses); // ['HTML', 'CSS', 'JavaScript', 'PostgreSQL', 'Express']
removeCourse('Vue'); // 'Course with this name was not found'

updateCourse('Express', 'NestJS');
console.log(courses); // ['HTML', 'CSS', 'JavaScript', 'PostgreSQL', 'NestJS']
```
