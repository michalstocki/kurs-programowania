Data: 15 października 2015

Cel: Poznanie powiązania pomiędzy HTML, CSS, JavaScript. Struktura dokumentu HTML.

## Zagadnienia

### Dokument HTML jako szkielet
Dokument HTML porównać można do szkieletu lub ramy na którą nałożyć możemy różne *skórki* graficzne. HTML koncentruje się na przekazaniu *treści* w postaci czytelnej struktury.

### CSS jako skórka graficzna
(ang. Cascading Style Sheets - Kaskadowe arkusze stylów)

http://www.csszengarden.com/

### JavaScript jako warstwa interaktywna
JavaScript pozwala zamienić coś co przypomina zwykły dokument tekstowy w... program. Od momentu kiedy mamy JavaScript, każda strona internetowa może stać się skomplikowanym programem!

## W praktyce

### Brackets
Edytor webowy umożliwiający obserwowanie na żywo zmian w HTML/CSS oraz przeglądanie struktury dokumentu, przez podświetlanie fragmentów kodu HTML. Możemy się trochę po eksperymentować z demonstracyjną stroną, która wita nas po otwarciu edytora.

http://brackets.io/

### Projekt demo

Przycisk (błyskawica) otwiera szybki podgląd w przeglądarce [Google Chrome](https://www.google.pl/chrome/browser/desktop/).

Warto zwrócić uwagę na:
- `index.html` w linii 7 jest tag `<title>` - zmień jego zawartość i znajdź różnicę na stronie
- `index.html` w linii 9 jest tag `<link>`, dzięki któremu do naszej strony zostaje podłączony arkusz CSS

### Edycja CSS
Spróbuj odnaleźć zadanie zaszyte w kodzie HTML, który *nie jest* widoczny w przeglądarce. Wykonaj polecane tam zmiany w kodzie CSS.

### Szczypta JavaScriptu
1. Utwórz plik `main.js` (klinknij prawym przyciskiem w listę plików po lewej stronie i wybierz "Nowy plik")
2. w `index.html` dodaj następującą linię zaraz przed tagiem zamykającym `</body>`:
  
    ```html
    <script src="main.js"></script>
    ```
3. Dodaj następujący kod w utworzonym `main.js`:
    ```javascript
    var header = document.querySelector("h3");
    
    header.addEventListener("click", function () {
        header.classList.toggle("askew");
    });
    ```
4. W pliku `main.css` w lini 26 dodaj następujący fragment:
    ```css
    h3 {
        transition: transform 200ms ease-in-out;
        transform-origin: left bottom;
        transform: rotate(0deg);
    }
    
    h3.askew {
        transform-origin: left bottom;
        transform: rotate(5deg);
        transition: transform 200ms ease-in-out;
    }
    ```
  
**Dobrej zabawy!**
