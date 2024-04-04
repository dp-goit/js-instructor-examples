# Moduł 2 - Lekcja 4 - Funkcje

## Zadanie 1 - BMI
Napisz funkcję `calcBMI(weight, height)`, która obliczy i zwróci BMI użytownika. Aby to zrobić, podzielwagę użytkowinika w kilogramach przez kwadrat wzrostu w metrach.

Waga oraz wzrost będą przekazane do fukncji jako tekst. W związku z tym mogą mieć one format `24.7` oraz `24,7`, przecinek także może być użyty to jako separator części ułamkowej.

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

Write a function `getRectArea(dimensions)` to calculate the area of a rectangle
with sides, the values of which will be passed to the `dimensions` parameter as a string.
Values are guaranteed to be separated by a space.

```js
function getRectArea(dimensions) {}

console.log(getRectArea('8 11'));
```

## Zadanie 4 - Element logging

Write a function `logItems(items)` that takes an array and uses a `for` loop
that for each element of the array will print a message to the console
in the format `<item number> - <item value>`. The numbering
of elements should start with `1`.

For Zadanie, for the first element of the array `['Mango', 'Poly', 'Ajax']` with index `0`
will print `1 - Mango` and for index 2 will print `3 - Ajax`.

```js
function logItems(items) {}

logItems(['Mango', 'Poly', 'Ajax']);
logItems(['🍎', '🍇', '🍑', '🍌', '🍋']);
```

## Zadanie 5 - Contact logging

Write a function `printContactsInfo(names, phones)` that prints  to the console the name
and the user's phone number. The `names` and `phones` parameters will be passed
strings of names and phone numbers separated by commas. Sequence number of names and
phone numbers in the rows indicate a match. Number of names and phones
guaranteed to be the same.

```js
function printContactsInfo(names, phones) {}

printContactsInfo(
  'Jacob,William,Solomon,Artemis',
  '89001234567,89001112233,890055566377,890055566300',
);
```

## Zadanie 6 - Finding the largest element

Write a function `findLargestNumber(numbers)` that looks for the largest number in
array.

```js
function findLargestNumber(numbers) {}

console.log(findLargestNumber([2, 17, 94, 1, 23, 37])); // 94
console.log(findLargestNumber([49, 4, 7, 83, 12])); // 83
```

## Zadanie 7 - Average value

Write a `calAverage()` function that takes an arbitrary number of arguments
and returns their average. All arguments will be only numbers.

```js
function calAverage() {}

console.log(calAverage(1, 2, 3, 4)); // 2.5
console.log(calAverage(14, 8, 2)); // 8
console.log(calAverage(27, 43, 2, 8, 36)); // 23.2
```

## Zadanie 8 - Time Formatting

Write a function `formatTime(minutes)` that will translate the value of `minutes`
(number of minutes) to a string in hour and minute format `HH:MM`.

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

## Zadanie 9 -Collection of courses (includes, indexOf, push, etc.)

Write functions to work with the `courses` collection of training courses:

- `addCourse(name)` - adds a course to the end of the collection
- `removeCourse(name)` - removes a course from the collection
- `updateCourse(oldName, newName)` - changes the name to a new one

```js
const courses = ['HTML', 'CSS', 'JavaScript', 'React', 'PostgreSQL'];

addCourse('Express');
console.log(courses); // ['HTML', 'CSS', 'JavaScript', 'React', 'PostgreSQL', 'Express']
addCourse('CSS'); // ' You already have this course'

removeCourse('React');
console.log(courses); // ['HTML', 'CSS', 'JavaScript', 'PostgreSQL', 'Express']
removeCourse('Vue'); // 'Course with this name was not found'

updateCourse('Express', 'NestJS');
console.log(courses); // ['HTML', 'CSS', 'JavaScript', 'PostgreSQL', 'NestJS']
```
