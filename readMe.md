
<details>
<summary><h2>JavaScript</h2></summary>

Na początek należy odpowiednio przygotować strukturę HTML. Należy pamiętać o załączeniu skryptu przed końcem znacznika `body`.

```html
<form>
    <input type = "text" id = "pole">
    <button type = "button" id = "przycisk">Przycisk</button>
</form>

<p id = "akapit"></p>

<script src = "script.js"></script>
```

W *JavaScript* pobieramy wszystkie interesujące nas elementy, do których będziemy się chcieli później odwoływać.

```js
const pole = document.querySelector('#pole')
const przycisk = document.querySelector('#przycisk')
const akapit = document.querySelector('#akapit')
```

Następnie przygotowujemy funkcję, która ma zostać wywołana po naciśnięciu przycisku. Wewnątrz pobieramy wartości pól i ustalamy dalsze działanie.

```js
function poKliknieciu () {

    const wartosc = pole.value

    // Zarządzanie wartościami (wewnątrz funkcji)
}
```

Możemy dowolnie zarządzać własnościami danego elementu.

```js
    akapit.classList.add('nazwaKlasy') // Dodanie klasy
    akapit.classList.remove('nazwaKlasy') // Usunięcie klasy

    akapit.textContent = 'Nowa zawartość' // Wpisanie tekstu

    akapit.style.backgroundColor = 'red' // Zmiana stylu
```

Lub tworzyć nowe elementy.

```js
    const nowyElement = document.createElement('div')

    nowyElement.textContent = 'Zawartość elementu'

    document.body.appendChild(nowyElement)
```

Na koniec należy pamiętać o przypisaniu obsługi zdarzenia do przycisku.

```js
przycisk.addEventListener('click', poKliknieciu)
```

</details>

# Projekty

## 1. Lista zadań

Prosta aplikacja webowa do zarządzania listą zadań, wykonana z wykorzystaniem **HTML**, **CSS** i **JavaScript**. Aplikacja umożliwia dodawanie zadań, oznaczanie ich jako wykonane oraz usuwanie z listy.

### Funkcjonalności

* wyświetlanie listy zadań,
* dodawanie nowych zadań,
* oznaczanie zadań jako wykonane,
* usuwanie zadań,
* wyświetlanie liczby zadań z podziałem na wykonane i niewykonane,
* przechowywanie zadań w `localStorage`.
