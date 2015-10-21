Data: 22 pażdziernika 2015

Cel: Uporządkowanie wiedzy związanej ze zmiennymi i funkcjami.

# Powtórka
## Zmienne

Utwórzmy przykładową zmienną o nazwie `number` i wartości `0`.
```javascript
var number = 0;
```
Możemy też utworzyć zmienną a dopiero potem przypisać do niej wartość:
```javascript
var number;             // tutaj wartość zmiennej `number` jest równa `undefined`
number = 0;             // tutaj już wartość zmiennej `number` jest równa `0` (liczba zero)
```

Możemy wielokrotnie zmieniać wartość tej samej zmiennej:
```javascript
var number = 0;         // inicjujemy zmienną z wartością `0`
number = 1;             // tutaj nie używamy już słowa `var` bo zmienna została już wcześniej utworzona 
```

Zmienna może mieć zarówno typ liczbowy (`number = 1`), tekstowy (`number = "one"`) jak i logiczny (`number = false`). W JavaScripcie możemy do tej samej zmiennej przypisywać wartości różnych typów:
```javascript
var value = 123;        // zmienna zainicjowana z wartością liczbową
value = "a hundred twenty three"; // wartość zmiennej została zmieniona na typ tekstowy
value = false;          // wartość zmiennej zmieniona na wartość logiczną "fałsz"
value = true;           // wartość zmiennej zmieniona na wartość logiczną "prawda"
```

### Zadanie 1.

1. do pliku `main.js` utworzonego na poprzedniej lekcji dodaj na końcu (od nowej linii) następujący fragment:
  
  ```javascript
  var number = 12;
  alert(number);
  ```
2. Odśwież przeglądarkę (lub uruchom podgląd przyciskiem błyskawicy na prawym panelu).

  **Zauważ:** Zmienne przypominają pudełka, które "przenoszą" swoje wartości. Jeśli do jakiejś zmiennej przpiszemy wartość, następnie możemy używać jej wielokrotnie używając tej samej wartości.

3. Spróbuj zmodyfikować swój kod do następującej postaci:
  
  ```javascript
  var number = 12;
  alert(number);
  number = 1 + 2;
  alert(number);
```

## Funkcje

Funkcja to fragment kodu wyodrębniony do wykonywania konkretej operacji. Aby zdefiniować ciało funkcji musimy posłużyć się następującym zapisem:

```javascript
function() {
  // tutaj kod funkcji
}
```

Łatwiej jest posługiwać się funkjcą, która ma swoją nazwę, możemy nadać funkcji nazwę posługując się jednym z poniższych zapisów.

Nazwana funkcja (deklaracja funkcji):
```javascript
function someOperation() {

} // tutaj nie dajemy średnika na końcu linii.
```

Anonimowa funkcja w zmiennej (wyrażenie funkcyjne):
```javascript
var someOperation = function() {

}; // tutaj powinniśmy dać średnik na końcu linii.
```

### Przykłady funkcji z lekcji pierwszej:

Dodawanie

```javascript
function add(a, b) {        // deklaracja funkcji o nazwie `add`, przyjmującej argumenty `a` i `b`.
  var result = a + b;       // wnętrze funkcji; tworzymy zmienną `result`, której wartość ustawiamy na wynik dodawania
  return result;            // słowo kluczowe `return` zwraca podaną wartość.
}

var sum = add(1, 7);        // wywołanie funkcji `add` z argumentami `1` i `7`.
alert(sum);                 // wywołanie systemowej funkcji `alert` w celu wyświetlenia wartości zmiennej `sum`
```

Zwracanie mniejszej liczby z dwóch podanych

```javascript
function min(c, d) {
  var result;               // tworzymy zmienną `result` bez wartości
  if (c < d) {              // konstrukcja warunkowa z wyrażeniem logicznym
    result = c;             // w przypadku spełnienia warunku przypisujemy wartość argumentu `c` do zmiennej
  } else {
    result = d;             // w przypadku, gdy warunek jest nie spełniony przypisujemy wartość argmentu `d` do zmiennej
  }
  return result;            // zwracamy wartość zmiennej `result`
}

alert(min(12, 34));         // wyświetlenie na ekranie wyniku funkcji `min` bez przypisywania go do zmiennej.
```

### Zadanie 2.

Utwórz funkcję o nazwie `isPositive`, która sporawdzi, czy liczba podana jako argument jest liczbą dodatnią i zwróci wartość logiczną (`true` lub `false`). Utwórz kilka wersji tej funkcji:
  - z użyciem zmiennej `result` przechowującej wynik i konstrukją `if`
  - bez użycia zmiennej `result` ale z wykorzystaniem konstrukcji `if`
  - bez użycia zmiennej `result` ani konstrukcji `if` - spróbuj zapisać to jak najkrócej

### Zadanie 3.

Utwórz funkcję o nazwie `isNatural`, która sprawdzi, czy liczba podana jako argument, należy do zbioru liczb naturalnych i zwróci wartość logiczną (`true` lub `false`). Podpowiedź: możesz wykorzystać operator `%`, który zwraca modulo - resztę z dzielenia dwóch liczb. Wyrażenie `12 % 3` zwróci wartość `0` ale wyrażenie `5 % 2` zwróci wartość `1`. 

