Cel: Umiejętność posługiwania się tablicami w praktyce

# Latający obiekt

W tej lekcji napiszemy program, który będzie umożliwiał przesuwanie prostokąta za pomocą myszki. W tym celu załóż nowy projekt projekt postępując zgodnie ze [wskazówkami z lekcji 4](lekcja-0004.md).

## Tworzymy arkusz CSS
W tym programie bardzo przydatne będą nam style CSS, dlatego musimy zadbać o to, żeby w projekcie znazał się odpowiedni plik.

W projekcie utwórz plik o nazwie `main.css`. Następnie podłącz go do strony HTML dodając w pliku `index.html` pomiędzy znacznikiem `<head>` a `</head>` następującą linijkę:

```html
<link rel="stylesheet" href="main.css">
```
Dzięki temu style zdefiniowane w pliku `main.css` będą miały zastosowanie do elementów znajdujących się w pliku `index.html`.

## Dodajemy element `div`

Potrzebny jest nam element, który będziemy przesuwać. Pierwszy krok jaki musimy wykonać to dodać odpowiedni tag do naszego pliku `index.html`. Nowy element musi trwafić wewnątrz `body` czyli pomiędzy tagiem `<body>` a tagiem `</body>`. Definicja nowego elementu może wyglądać następująco:

```html
<div class="box"></div>
```

Atrybut `class="box"` dodaliśmy dlatego, aby móc wygodnie definiować wygląd naszego elementu za pomocą CSS-a.

## Stylujemy

Aby nadać naszemu elementowi (i jego otoczeniu) odpowiedni wygląd, wypełnijmy więc plik `main.css` następującą treścią:

```css
body {
  background-color: rgb(252, 252, 244);
}

.box {
  cursor: move;
  width: 100px;
  height: 100px;
  background-color: #ECBE13 ;
  border: 2px #046D8B solid;
  border-radius: 10%;
  position: absolute;
}

.box.moving {
  box-shadow: rgba(0,0,0,0.5) 0 0 15px;
}
```

Przeanalizujmy w skrócie co znajduje się w tym fragmencie kodu.

#### Tło strony
```css
body {
  background-color: rgb(252, 252, 244);
}
```
Ten fragment to styl dla tagu `<body>` czyli dla całej zawartości naszej strony. Korzystamy z właściwości `background-color` aby ustalić kolor tła. Wartość `rgb(252, 252, 244)` to kod koloru. "rgb" to skrót od "red, green, blue".
