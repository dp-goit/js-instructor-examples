# Moduł 3. Lekcja 1. Obiekty

<!-- https://github.com/luxplanjay/js-33-qna/blob/03-%D0%BE%D0%B1%D1%8A%D0%B5%D0%BA%D1%82%D1%8B/js/vehicles.js -->

## Zadanie 1 - Podstawy obiektów

Napisz skrypt, który do obiektu `user`:

- dodaje pole `mood` z wartością `'happy'`,
- zmianie wartość `hobby` na `'skydiving'`,
- zmienia wartość `premium` na `false`,
- wyświetla zarwartość obiektu `user` w formacie `key:value`, używając `Object.keys()` oraz `for...of`.

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

Mamy obiektu, który zwiera informacje o wypłatach zespołu. Napisz kod, który sumuje wszystkie wypłaty i przechowuje wynik w zmiennej `sum`. Poprawny wynik to 390. Jeżeli obiekt `salaries` jest pusty, wynik powinien wynosić 0.

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
 * There are only two types of transaction.
 * You can deposit or withdraw money from your account.
 */
const Transaction = {
  DEPOSIT: 'deposit',
  WITHDRAW: 'withdraw',
};

/*
 * Each transaction is an object with properties: id, type and amount
 */

const account = {
  // Current account balance
  balance: 0,

  // Transaction History
  transactions: [],

  /*
   * Method creates and returns a transaction object.
   * Accepts amount and type of transaction.
   */
  createTransaction(amount, type) {},

  /*
   * The method responsible for adding the amount to the balance..
   * Accepts the amount of the transaction.
   * Calls createTransaction to create a transaction object
   * then adds it to the transaction history
   */
  deposit(amount) {},

  /*
   *The method responsible for withdrawing the amount from the balance.
   * Принимает сумму танзакции.
   * Calls createTransaction to create a transaction object
   * then adds it to the transaction history.
   *
   * If amount is greater than the current balance, display a message
   * about the fact that the withdrawal of such an amount is not possible, there are not enough funds.
   */
  withdraw(amount) {},

  /*
   * The method returns the current balance
   */
  getBalance() {},

  /*
   * The method searches and returns the transaction object by id
   */
  getTransactionDetails(id) {},

  /*
   * The method returns the amount of funds
   *a specific type of transaction from the entire history of transactions
   */
  getTransactionTotal(type) {},
};
```
