Cel: Poznanie obiektów typu tablica (Array) w JavaScripcie wraz z przykładami ich użycia.

## Przykłady użycia tablic

1. Tworzenie obiektu typu tablica (Array).
  ```javascript
  var students = ["Mateusz", "Ignacy", "Maria"];
  
  console.log(students.length); // zwróci w konsoli: 3
  ```
  [:arrow_forward: Zobacz jak to działa](https://jsbin.com/qagolu/edit?js,console)

2. Dodawanie nowego elementu na końcu tablicy
  ```javascript
  var students = ["Mateusz", "Ignacy", "Maria"];
  students.push("Joanna");
  
  console.log(students.length); // zwróci w konsoli: 4
  console.log(students); // zwróci w konsoli ["Mateusz", "Ignacy", "Maria", "Joanna"]
  ```
  [:arrow_forward: Zobacz jak to działa](https://jsbin.com/kemoci/edit?js,console)
  
3. Pobieranie konkretnego elementu z tablicy
  ```javascript
  var students = ["Mateusz", "Ignacy", "Maria", "Joanna"];
  
  console.log(students[0]); // zwróci w konsoli "Mateusz"
  console.log(students[1]); // zwróci w konsoli "Ignacy"
  ```
  [:arrow_forward: Zobacz jak to działa](https://jsbin.com/tuvaqu/edit?js,console)
  
  :heavy_exclamation_mark:  **Zauważ:** kiedy wywołaliśmy pobranie elementu z tablicy `students[1]`, został zwrócony **drugi** element tablicy. Dzieje się tak dlatego, że liczba podana w nawiasach kwadratowych to "index" elementu. Tak działają tablice w większości języków programowania. Mówimy wtedy, że "tablice są indeksowane od zera".

4. Nadpisywanie (podmienianie) elementy w tablicy
  ```javascript
  var students = ["Mateusz", "Ignacy", "Maria"];
  students[1] = "Bonifacy";
  
  console.log(students); // zwróci w konsoli: ["Mateusz", "Bonifacy", "Maria"]
  ```
  [:arrow_forward: Zobacz jak to działa](https://jsbin.com/nuxime/edit?js,console)
  
  :point_right: **Zauważ:** przypisanie wartości do elementu tablicy (`students[1] = "Ignacy"`) wygląda bardzo podobnie do przypisania wartości do zmiennej (`student = "Ignacy"`).
  
5. Usuwanie ostatniego elementu z tablicy
  ```javascript
  var students = ["Mateusz", "Ignacy", "Maria"];
  students.pop();
  
  console.log(students.length); // zwróci w konsoli: 2
  console.log(students); // zwróci w konsoli: ["Mateusz", "Bonifacy"]
  ```
  [:arrow_forward: Zobacz jak to działa](https://jsbin.com/hofago/edit?js,console)

6. Tablica z różnymi typami elementów 
  ```javascript
  var stuff = [154, "koza", null];
  stuff[4] = false;
  
  console.log(stuff.length); // zwróci w konsoli: 5
  console.log(stuff); // zwróci w konsoli: [154, "koza", null, undefined, false]
  ```
  [:arrow_forward: Zobacz jak to działa](https://jsbin.com/jiqeqo/edit?js,console)
  
  :question: *Zagadka:* dlaczego jako czwarty element tablicy `stuff` pojawia się obiekt typu `undefined`?

7. Użycie zmiennych jako elementów tablic
  ```javascript
  var kindOfDog = "pieseł";
  var stuff = [kindOfDog, "kitten"];
  var kindOfMonkey = "gibbon";
  stuff[1] = kindOfMonkey;
  
  console.log(stuff.length); // zwróci w konsoli: 2
  console.log(stuff); // zwróci w konsoli: ["pieseł", "gibbon"]
  ```
  [:arrow_forward: Zobacz jak to działa](https://jsbin.com/gugesa/edit?js,console)
  
## Obserwacje i wnioski

1. Tablica jest czymś w rodzaju *uporządkowanej listy elementów*.
2. Elementy możemy dodawać, wymieniać i usuwać.
3. Tablica zawsze jest w stanie dostarczyć nam aktualną informację o ilości elementów jakie zawiera.
4. Tablica może zawierać elementy różnego typu
5. Tablice są indeksowane od zera. Indeks jest nam niezbędny do tego, aby odwołać się do konkretnego elementu tablicy.

## Zadania
Zadania można wykonać w nowm lub w istniejącym projekcie w programie Brackets.
### Zadanie 7.
Utwórz funkcję `putToArray(a, b, c)`, która przyjmie trzy argumenty i zwróci tablicę zawierającą te trzy elementy w kolejności w jakiej zostały podane.

### Zadanie 8.
Utwórz funkcję `getLastFrom(array)`, króra przyjmie tablicę i zwróci ostatni z jej elementów nie usuwając go.

### Zadanie 9.
Posługując się [dokumentacją tablicy dostępną na stronie Mozilla Developer Network](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/Array), utwórz funkcję `peel(array)`, która przyjmie tablicę elementów i usunie pierwszy oraz ostatni element tej tablicy a następnie zwróci nową długość (liczbę elementów) tej tablicy.

### Zadanie 10.
Posługując się [dokumentacją tablicy dostępną na stronie Mozilla Developer Network](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/Array), utwórz funkcję `doesArrayContainElement(array, element)`, która przymie tablicę oraz element i zwróci `true` jeśli element znajduje się w podanej tablicy lub `false` jeśli elemet nie znajduje się w podanej tablicy.

Podpowiedź: Użyj funkcji `indexOf`.
