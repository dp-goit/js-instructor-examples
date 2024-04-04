# Moduł 4 - Lekcja 8 - Metody iterujące po tablicy

## Kolekcja obiektów dla wszystkich przykładów z samochodami

```js
const cars = [
  {
    make: 'Honda',
    model: 'CR-V',
    type: 'suv',
    amount: 14,
    price: 24045,
    onSale: true,
  },
  {
    make: 'Honda',
    model: 'Accord',
    type: 'sedan',
    amount: 2,
    price: 22455,
    onSale: true,
  },
  {
    make: 'Mazda',
    model: 'Mazda 6',
    type: 'sedan',
    amount: 8,
    price: 24195,
    onSale: false,
  },
  {
    make: 'Mazda',
    model: 'CX-9',
    type: 'suv',
    amount: 7,
    price: 31520,
    onSale: true,
  },
  {
    make: 'Toyota',
    model: '4Runner',
    type: 'suv',
    amount: 19,
    price: 34210,
    onSale: false,
  },
  {
    make: 'Toyota',
    model: 'Sequoia',
    type: 'suv',
    amount: 16,
    price: 45560,
    onSale: false,
  },
  {
    make: 'Toyota',
    model: 'Tacoma',
    type: 'truck',
    amount: 4,
    price: 24320,
    onSale: true,
  },
  {
    make: 'Ford',
    model: 'F-150',
    type: 'truck',
    amount: 11,
    price: 27110,
    onSale: true,
  },
  {
    make: 'Ford',
    model: 'Fusion',
    type: 'sedan',
    amount: 13,
    price: 22120,
    onSale: true,
  },
  {
    make: 'Ford',
    model: 'Explorer',
    type: 'suv',
    amount: 6,
    price: 31660,
    onSale: false,
  },
];
```

## Przykład 1 - Metoda Mapująca

Niech funkcja `getModels` zwraca tablicę modeli (pole model) wszystkich samochodów.

```js
const getModels = cars => {};

console.table(getModels(cars));
```

## Przykład 2 - Metoda Mapująca

Niech funkcja `makeCarsWithDiscount` zwraca nową tablicę obiektów z zmienioną wartością właściwości `price` w zależności od przekazanej zniżki.

```js
const makeCarsWithDiscount = (cars, discount) => {};

console.table(makeCarsWithDiscount(cars, 0.2));
console.table(makeCarsWithDiscount(cars, 0.4));
```

## Przykład 3 - Metoda Filtrująca

Niech funkcja `filterByPrice` zwraca tablicę samochodów, których cena jest mniejsza niż wartość parametru `threshold`.

```js
const filterByPrice = (cars, threshold) => {};

console.table(filterByPrice(cars, 30000));
console.table(filterByPrice(cars, 25000));
```

## Przykład 4 - Metoda Filtrująca

Niech funkcja `getCarsWithDiscount` zwraca tablicę samochodów, których właściwość onSale ma wartość true.

```js
const getCarsWithDiscount = cars => {};

console.table(getCarsWithDiscount(cars));
```

## Przykład 5 - Metoda Filtrująca

Niech funkcja `getCarsWithType` zwraca tablicę samochodów, których typ zgadza się z wartością parametru `type`.

```js
const getCarsWithType = (cars, type) => {};

console.table(getCarsWithType(cars, 'suv'));
console.table(getCarsWithType(cars, 'sedan'));
```

## Przykład 6 - Metoda Szukająca

```js
const getCarByModel = (cars, model) => {};

console.log(getCarByModel(cars, 'F-150'));
console.log(getCarByModel(cars, 'CX-9'));
```

## Przykład 7 - Metoda Sortująca

Niech funkcja `sortByAscendingAmount` zwraca nową tablicę samochodów posortowaną rosnąco według wartości właściwości `amount`.

```js
const sortByAscendingAmount = cars => {};

console.table(sortByAscendingAmount(cars));
```

## Przykład 8 - Metoda Sortująca

Niech funkcja `sortByDescendingPrice` zwraca nową tablicę samochodów posortowaną malejąco według wartości właściwości `price`.

```js
const sortByDescendingPrice = cars => {};

console.table(sortByDescendingPrice(cars));
```

## Przykład 9 - Metoda Sortująca

Niech funkcja `sortByModel` zwraca nową tablicę samochodów posortowaną według nazwy modelu alfabetycznie i odwrotnie alfabetycznie, w zależności od wartości parametru `order`.

```js
const sortByModel = (cars, order) => {};

console.table(sortByModel(cars, 'asc'));
console.table(sortByModel(cars, 'desc'));
```

## Przykład 10 - Metoda Agregacyjna

Niech funkcja `getTotalAmount` zwraca całkowitą liczbę samochodów (wartość właściwości `amount`).

```js
const getTotalAmount = cars => {};

console.log(getTotalAmount(cars));
```

## Przykład 11 - Łańcuchy metod

Niech funkcja `getModelsOnSale` zwraca tablicę modeli samochodów, ale tylko tych, które aktualnie są na sprzedaż.

```js
const getModelsOnSale = cars => {};

console.table(getModelsOnSale(cars));
```

## Przykład 12 - Łańcuchy metod

Niech funkcja `getSortedCarsOnSale` zwraca tablicę samochodów na sprzedaż (właściwość onSale), posortowaną rosnąco według ceny.

```js
const getSortedCarsOnSale = cars => {};

console.table(getSortedCarsOnSale(cars));
```
