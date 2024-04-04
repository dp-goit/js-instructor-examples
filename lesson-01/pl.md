# Moduł 1. Lekcja 1. Zmienne, typy i operatory 

## Zadanie 1 - Operacje matematyczna

Wyświetl sumę jabłek i wynogron oraz różnicę w ilości jabłek i winogron w konsoli.

```js
const apples = 47;
const grapes = 135;
const total = ;
console.log(total)
const diff = ;
console.log(diff)
```

## Zadanie 2 - Operatory złożone

Zmień wyrażenie nadpisujące wartość zmiennej `student` na operator złożony `+=`.

```js
let students = 100;
students = students + 50;
console.log(students);
```

## Zadanie 3 - Kolejność operatorów

Rozpisz kolejność wykonywania działań podczas przypisania wartości do zmiennej `result`.

```js
const result = 108 + 223 - 2 * 5;
console.log(result);
```

## Zadanie 4 - Zaokrąglanie liczb

Napisz skrypt, wyświetlający w konsoli zaokrągloną w górę, w dół oraz wg zasad matematyki, wartość zmiennej `value`. Użyj metod `Math.floor()`, `Math.ceil()` oraz `Math.round()`. Sprawdź także wyniki dla wartości 27.3 oraz 27.9.

```js
const value = 27.5;
```

## Zadanie 5 - Interpolacja ciągów znaków

Stwórz frazę, korzystając z interpolacji cjągów: `A has B bots in stock`, gdzie A oraz B to zmienne variables inserted into a line.

```js
const companyName = 'Cyberdyne Systems';
const repairBots = 150;
const defenceBots = 50;
const message = ``;
console.log(message); // "Cyberdyne Systems has 200 bots in stock"
```

## Zadanie 6 - Metody ciągów znakowych

Napisz skrypt, który oblicza BMI użytkownika. W tym celu musimy podzielić wagę w kilogramach przez kwadrat wzrostu w centymetrach.

Waga i wzrost są zadeklarowane w zmiennych `weight` and `height`, lecz jako ciągi znaków, nie liczby (celowo na potrzeby zadania). Wartości nieliczbowe mogą być podane jako `24.7` lub `24,7`, separatorem części dziesiętnej może być przecinek.

BMI powinien być zaokrąglony do jednej liczby po przecinku.

```js
let weight = '88,3';
let height = '1.75';

const bmi = ;
console.log(bmi); // 28.8
```

## Zadanie 7 - Operatory porównania oraz rzutowanie typów

Jaki będzie wynik tych operacji?

```js
console.log(5 > 4);

console.log(10 >= '7');

console.log('2' > '12');

console.log('2' < '12');

console.log('4' == 4);

console.log('6' === 6);

console.log('false' === false);

console.log(1 == true);

console.log(1 === true);

console.log('0' == false);

console.log('0' === false);

console.log('Papaya' < 'papaya');

console.log('Papaya' === 'papaya');

console.log(undefined == null);

console.log(undefined === null);
```

## Zadanie 8 - Operatory logiczne

Jaki będzie wynik tych wyrażeń?

```js
console.log(true && 3);

console.log(false && 3);

console.log(true && 4 && 'kiwi');

console.log(true && 0 && 'kiwi');

console.log(true || 3);

console.log(true || 3 || 4);

console.log(true || false || 7);

console.log(null || 2 || undefined);

console.log((1 && null && 2) > 0);

console.log(null || (2 && 3) || 4);
```

## Zadanie 9 - Wartości domyślne 

Zmodyfikuj kod, aby do zmiennej `value` była przypisana wartość `incomingValue`, pod warunkiem, że wartością tej zmiennej nie jest `undefined` lub `null`. 
W takim przypadku do zmiennej `value` musi być przypisana wartość zmiennej `defaultValue`. Sprawdź działanie skryptu, przypisując do `incomingValue` wartości: null, undefined, 0, false.
Użyj operatora `??` (nullish coalescing operator).

```js
const incomingValue = 5;
const defaultValue = 10;
const value = incomingValue || defaultValue;
console.log(value);
```

## Zadanie 10 - Operator modulo oraz metody ciągów znaków

Napisz skrypt, który zamieni wartość `totalMinutes` (ilość minut) na godzinę w formacie `HH:MM`.

- 70 na 01:10
- 450 na 07:30
- 1441 na 24:01

```js
const totalMinutes = 70;

const hours = Math.floor(totalMinutes / 60);
const minutes = totalMinutes % 60;
console.log(hours);
console.log(minutes);

const doubleDigitHours = String(hours).padStart(2, 0);
const doubleDigitMinutes = String(minutes).padStart(2, 0);
console.log(`${doubleDigitHours}:${doubleDigitMinutes}`);
```
