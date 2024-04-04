# Moduł 4. Lekcja 7. Wywołania zwrotne. Funkcje strzałkowe. forEach

## Przykład 1 - Funkcja zwrotna

Napisz następujące funkcje:

- `createProduct(obj, callback)` - przyjmuje obiekt produktu bez identyfikatora (`id`), a także funkcję zwrotną. Funkcja tworzy obiekt produktu dodając do niego unikalny identyfikator w właściwości `id` i wywołuje funkcję zwrotną,
  przekazując jej utworzony obiekt.
- `logProduct(product)` - funkcja zwrotna przyjmująca obiekt produktu i logująca go do konsoli
- `logTotalPrice(product)` - funkcja zwrotna przyjmująca obiekt produktu i logująca całkowitą wartość produktu w konsoli

```js
// Rozwiązanie
function createProduct(partialProduct, callback) {
  const product = { id: Date.now(), ...partialProduct };
  callback(product);
}

function logProduct(product) {
  console.log(product);
}

function logTotalPrice(product) {
  console.log(product.price * product.quantity);
}

createProduct({ name: '🍎', price: 30, quantity: 3 }, logProduct);
createProduct({ name: '🍋', price: 20, quantity: 5 }, logTotalPrice);
```

## Przykład 2 - Funkcja zwrotna

Dodaj metody `withdraw(amount, onSuccess, onError)` do obiektu account oraz `deposit(amount, onSuccess, onError)`, gdzie pierwszy parametr to kwota operacji, a drugi i trzeci to funkcje zwrotne.

Metoda `withdraw` wywołuje błąd `onError`, jeśli kwota przekracza LIMIT_TRANSAKCJI lub saldo konta, a w przeciwnym razie wywołuje `onSuccess`. Metoda `deposit` wywołuje błąd `onError`, jeśli kwota przekracza LIMIT_TRANSAKCJI lub jest mniejsza lub równa zero, a w przeciwnym razie wywołuje `onSuccess`.

```js
// Rozwiązanie
const TRANSACTION_LIMIT = 1000;

const account = {
  username: 'Jacob',
  balance: 400,
  withdraw(amount, onSuccess, onError) {
    if (amount > TRANSACTION_LIMIT) {
      onError(`Kwota nie powinna przekraczać ${TRANSACTION_LIMIT} kredytów`);
    } else if (amount > this.balance) {
      onError(
        `Amount can't exceed account balance of ${this.balance} kredytów`
      );
    } else {
      this.balance -= amount;
      onSuccess(`Account balance: ${this.balance}`);
    }
  },
  deposit(amount, onSuccess, onError) {
    if (amount > TRANSACTION_LIMIT) {
      onError(`Kwota nie powinna przekraczać ${TRANSACTION_LIMIT} kredytów`);
    } else if (amount <= 0) {
      onError(`Kwota powinna być większa niż 0 kredytów`);
    } else {
      this.balance += amount;
      onSuccess(`Account balance: ${this.balance}`);
    }
  },
};

function handleSuccess(message) {
  console.log(`✅ Success! ${message}`);
}
function handleError(message) {
  console.log(`❌ Error! ${message}`);
}

account.withdraw(2000, handleSuccess, handleError);
account.withdraw(600, handleSuccess, handleError);
account.withdraw(300, handleSuccess, handleError);
account.deposit(1700, handleSuccess, handleError);
account.deposit(0, handleSuccess, handleError);
account.deposit(-600, handleSuccess, handleError);
account.deposit(600, handleSuccess, handleError);
```

## Przykład 3 - Funkcja zwrotna

Napisz funkcję `each(array, callback)`, która jako pierwszy parametr przyjmuje tablicę, a jako drugi - funkcję, która zostanie zastosowana do każdego elementu tablicy. Funkcja each musi zwrócić nową tablicę, której elementami będą wyniki
wywołania funkcji zwrotnej.

```js
// Rozwiązanie
function each(array, callback) {
  const newArr = [];
  for (const el of array) {
    newArr.push(callback(el));
  }
  return newArr;
}

console.log(
  each([64, 49, 36, 25, 16], function (value) {
    return value * 2;
  })
);
console.log(
  each([64, 49, 36, 25, 16], function (value) {
    return value - 10;
  })
);
console.log(
  each([64, 49, 36, 25, 16], function (value) {
    return Math.sqrt(value);
  })
);
console.log(
  each([1.5, 2.1, 16.4, 9.7, 11.3], function (value) {
    return Math.ceil(value);
  })
);
console.log(
  each([1.5, 2.1, 16.4, 9.7, 11.3], function (value) {
    return Math.floor(value);
  })
);
```

## Przykład 4 - Funkcje strzałkowe

Przeprowadź refaktoryzację kodu, używając funkcji strzałkowych.

```js
function createProduct(partialProduct, callback) {
  const product = { id: Date.now(), ...partialProduct };
  callback(product);
}

function logProduct(product) {
  console.log(product);
}

function logTotalPrice(product) {
  console.log(product.price * product.quantity);
}

createProduct({ name: '🍎', price: 30, quantity: 3 }, logProduct);
createProduct({ name: '🍋', price: 20, quantity: 5 }, logTotalPrice);
```

## Przykład 5 - Funkcje strzałkowe

Przeprowadź refaktoryzację kodu, używając funkcji strzałkowych.

```js
const TRANSACTION_LIMIT = 1000;

const account = {
  username: 'Jacob',
  balance: 400,
  withdraw(amount, onSuccess, onError) {
    if (amount > TRANSACTION_LIMIT) {
      onError(`Kwota nie powinna przekraczać ${TRANSACTION_LIMIT} kredytów`);
    } else if (amount > this.balance) {
      onError(
        `Amount can't exceed account balance of ${this.balance} kredytów`
      );
    } else {
      this.balance -= amount;
      onSuccess(`Account balance: ${this.balance}`);
    }
  },
  deposit(amount, onSuccess, onError) {
    if (amount > TRANSACTION_LIMIT) {
      onError(`Kwota nie powinna przekraczać ${TRANSACTION_LIMIT} kredytów`);
    } else if (amount <= 0) {
      onError(`Kwota powinna być większa niż 0 kredytów`);
    } else {
      this.balance += amount;
      onSuccess(`Account balance: ${this.balance}`);
    }
  },
};

function handleSuccess(message) {
  console.log(`✅ Success! ${message}`);
}
function handleError(message) {
  console.log(`❌ Error! ${message}`);
}

account.withdraw(2000, handleSuccess, handleError);
account.withdraw(600, handleSuccess, handleError);
account.withdraw(300, handleSuccess, handleError);
account.deposit(1700, handleSuccess, handleError);
account.deposit(0, handleSuccess, handleError);
account.deposit(-600, handleSuccess, handleError);
account.deposit(600, handleSuccess, handleError);
```

## Przykład 6 - Wbudowane funkcje strzałkowe

Przeprowadź refaktoryzację kodu, używając funkcji strzałkowych.

```js
function each(array, callback) {
  const newArr = [];
  for (const el of array) {
    newArr.push(callback(el));
  }
  return newArr;
}

console.log(
  each([64, 49, 36, 25, 16], function (value) {
    return value * 2;
  })
);
console.log(
  each([64, 49, 36, 25, 16], function (value) {
    return value - 10;
  })
);
console.log(
  each([64, 49, 36, 25, 16], function (value) {
    return Math.sqrt(value);
  })
);
console.log(
  each([1.5, 2.1, 16.4, 9.7, 11.3], function (value) {
    return Math.ceil(value);
  })
);
console.log(
  each([1.5, 2.1, 16.4, 9.7, 11.3], function (value) {
    return Math.floor(value);
  })
);
```

## Przykład 7 - Metoda forEach

Przeprowadź refaktoryzację kodu, używając metody `forEach` i funkcji
strzałkowych.

```js
function logItems(items) {
  console.log(items);
  for (let i = 0; i < items.length; i += 1) {
    console.log(`${i + 1} - ${items[i]}`);
  }
}

logItems(['Mango', 'Poly', 'Ajax']);
logItems(['🍎', '🍇', '🍑', '🍌', '🍋']);
```

## Przykład 8 - Metoda forEach

Przeprowadź refaktoryzację kodu, używając metody `forEach` i funkcji
strzałkowych.

```js
function printContactsInfo({ names, phones }) {
  const nameList = names.split(',');
  const phoneList = phones.split(',');
  for (let i = 0; i < nameList.length; i += 1) {
    console.log(`${nameList[i]}: ${phoneList[i]}`);
  }
}

printContactsInfo({
  names: 'Jacob,William,Solomon,Artemis',
  phones: '89001234567,89001112233,890055566377,890055566300',
});
```

## Przykład 9 - Metoda forEach

Przeprowadź refaktoryzację kodu, używając metody `forEach` i funkcji
strzałkowych.

```js
function calсulateAverage(...args) {
  let total = 0;
  for (let i = 0; i < args.length; i++) {
    total += args[i];
  }
  return total / args.length;
}

console.log(calсulateAverage(1, 2, 3, 4)); // 2.5
console.log(calсulateAverage(14, 8, 2)); // 8
console.log(calсulateAverage(27, 43, 2, 8, 36)); // 23.2
```
