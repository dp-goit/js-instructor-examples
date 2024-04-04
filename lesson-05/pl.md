# Moduł 3. Lekcja 1. Obiekty

<!-- https://github.com/luxplanjay/js-33-qna/blob/03-%D0%BE%D0%B1%D1%8A%D0%B5%D0%BA%D1%82%D1%8B/js/vehicles.js -->

## Zadanie 1 - Podstawy obiektów

Napisz skrypt, który do obiektu `user`:

- dodaje pole `mood` z wartością `'happy'`,
- zmianie wartość `hobby` na `'skydiving'`,
- zmienia wartość `premium` na `false`,
- wyświetla zawartość obiektu `user` w formacie `key:value`, używając `Object.keys()` oraz `for...of`.

### Kod

```js
const user = {
  name: 'Mango',
  age: 20,
  hobby: 'html',
  premium: true,
};
```

## Zadanie 2 -  Metoda Object.values()

Mamy obiekt, który zwiera informacje o wypłatach zespołu. Napisz kod, który sumuje wszystkie wypłaty i przechowuje wynik w zmiennej `sum`. Poprawny wynik to 390. Jeżeli obiekt `salaries` jest pusty, wynik powinien wynosić 0.

### Kod

```js
const salaries = {
  John: 100,
  Ann: 160,
  Pete: 130,
};
```

## Zadanie 3 - Tablica obiektów

Napisz funkcję `calcTotalPrice(stones, stoneName)`, która przyjmuje tablicę obiektów oraz zmienną tekstową z nazwą kamienia. Funkcja powinna obliczyć i zwrócić całkowity koszt kamieni o danej nazwie, bazując na `quantity` oraz `price`.
### Code

```js
const stones = [
  { name: 'Emerald', price: 1300, quantity: 4 },
  { name: 'Diamond', price: 2700, quantity: 3 },
  { name: 'Sapphire', price: 400, quantity: 7 },
  { name: 'Rubble', price: 200, quantity: 2 },
];
```

## Zadanie 4 - Zaawansowane zadania

Napisz skrypt, umożliwiający zarządzanie bankiem internetowym. Obiekt `account` wymaga uzupełnienia metod, które umożliwią wykonywanie operacji na koncie.

```js
/*
 * Są tylko 2 typy transakcji.
 * Możesz wpłacić (deposit) lub wypłacić (withdraw) pieniądze z konta.
 */
const Transaction = {
  DEPOSIT: 'deposit',
  WITHDRAW: 'withdraw',
};

/*
 * Każda transakcja jest obiektem z właściwościami: id, type (typ) oraz amount (ilość / wartość)
 */

const account = {
  // Aktualny stan konta
  balance: 0,

  // Historia transakcji
  transactions: [],

  /*
   * Metoda tworzy i zwraca obiekt transakcji.
   * Jako parametry przyjmuje wartość oraz typ transakcji.
   */
  createTransaction(amount, type) {},

  /*
   * Ta metoda jest odpowiedzialna za dodawanie wartości do balansu konta,
   * przyjmuje wartość wpłaty,
   * wywołuje createTransaction, aby stworzyć obiekt transakcji,
   * na koniec dodaje go do historii transakcji
   */
  deposit(amount) {},

  /*
   * Ta metoda jest odpowiedzialna za wypłacanie wartości z konta.
   * przyjmuje wartość wypłaty,
   * wywołuje createTransaction, aby stworzyć obiekt transakcji,
   * na koniec dodaje go do historii transakcji.
   *
   * Jeżeli wartość wypłaty przekracza aktualny stan konta, wyświtla wiadomość,
   * że ze względu na niewystarczające środki na koncie, wypłata jest niemożliwa.
   */
  withdraw(amount) {},

  /*
   * Metoda zwraca aktualną wartość konta.
   */
  getBalance() {},

  /*
   * Metoda wyszukuje oraz zwraca obiekt transakcji na podstawie id.
   */
  getTransactionDetails(id) {},

  /*
   * Metoda zwraca sumę wartości transakcji
   * dla konkretnego typu transakcji z całej historii.
   */
  getTransactionTotal(type) {},
};
```
