Cel: Poznanie obiektów typu tablica (Array) w JavaScripcie wraz z przykładami ich użycia.

## Przykłady użycia tablic

1. Tworzenie obiektu typu tablica (Array).
  ```javascript
  var students = ["Mateusz", "Ignacy", "Maria"];
  
  console.log(students.length); // zwróci w konsoli: 3
  ```
  [Zobacz jak to działa](https://jsbin.com/qagolu/1/edit?js,console)

2. Dodawanie nowego elementu na końcu tablicy
  ```javascript
  var students = ["Mateusz", "Ignacy", "Maria"];
  students.push("Joanna");
  
  console.log(students.length); // zwróci w konsoli: 4
  console.log(students); // zwróci w konsoli ["Mateusz", "Ignacy", "Maria", "Joanna"]
  ```
  [Zobacz jak to działa](https://jsbin.com/kemoci/edit?js,console)
  
3. Pobieranie konkretnego elementu z listy
  ```javascript
  var students = ["Mateusz", "Ignacy", "Maria", "Joanna"];
  
  console.log(students[0]); // zwróci w konsoli "Mateusz"
  console.log(students[1]); // zwróci w konsoli "Ignacy"
  ```
  [Zobacz jak to działa](https://jsbin.com/kemoci/edit?js,console)
  
  **Zauważ:** kiedy wywołaliśmy popranie elementu z tablicy `students[1]`, został zwrócony **drugi** element tablicy. 
