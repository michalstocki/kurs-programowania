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
  width: 100px;
  height: 100px;
  background-color: #ECBE13;
  border: 2px #046D8B solid;
  border-radius: 10%;
  position: absolute;
  cursor: move;
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

#### Rozmiar elementu
```css
.box {
  width: 100px;
  height: 100px;
  (...)
}
```
Fragment `.box` to selektor klasy elementu. Oznacza, że wymienione dalej właściwości zostaną przypisane do elementu o klasie `box` czyli do elementu który ma atrybut `class="box"`.

`width` i `height` to oczywiście rozmiar elementu. W tym przypadku wielkość jest podana w pixelach (px).

#### Obramowanie elementu

```css
.box {
  (...)
  border: 2px #046D8B solid;
  border-radius: 10%;
  (...)
}
```
Ten fragment określa wygląd ramki elementu. `border: 2px #046D8B solid` oznacza, że ramka będzie miała grubość 2 pixeli, że będzie koloru o kodzie `#046D8B` oraz, że będzie linią ciągłą (`solid`).

`border-radius: 10%` określa, że ramka elementu ma zaokrąglone narożniki. W tym przypadku promień zaokrąglenia wynosi 10% długości boku.

:bulb: _Eksperyment:_ Spróbuj zmienić promień zaokrąglenia narożników na połowę długości boku elementu.

#### Cień elementu

```css
.box.moving {
  box-shadow: rgba(0,0,0,0.5) 0 0 15px;
}
```
W tym fragmencie zwróćmy uwagę na selektor użyty w tym bloku stylów. `.box.moving` oznacza, że podajemy listę właściwości obiektu, który posiada dwie klasy jednocześnie: "box" i "moving". Odpowiada to elementowi, który ma atrybut `class="box moving"`. Zastosowaliśmy taki zabieg aby nadać specjalny wygląd elementu w trakcie kiedy jest przesuwany. Samym przesuwaniem zajmiemy się jednak za chwilę.


