---
layout: default
---

## CSS

Kaskádové styly (CSS) slouží pro změnu vzhledu prvků stránky (pozadí, barva, výška, šířka, ...).

<a href="./samples/sample1.html" target="_blank">Ukázka - bez CSS</a>

<a href="./samples/sample2.html" target="_blank">Ukázka - s CSS</a>

Příklad napojení stylů a třídy:

    <!DOCTYPE html>
    <html>
        <head>
        	<title>Titulek</title>
        	<!-- Napojení stylů -->
        	<link rel="stylesheet" href="styl.css">
        </head>
        <body>
        	<!—- Třída(viz níže) -->
        	<p class="modry">Odstavec</p>
        	<!—- Tento odstavec bude mít výchozí barvu -->
        	<p>
        </body>
    </html>

Pro stylování slouží pravidla - základní zápis je: `selektor {vlastnost: hodnota;}`
Selektor je to, co stylujeme. Lze vybrat více elementů, stačí oddělit čárkou, viz níže, nebo třídu (class) – ty lze použít pro vizuální odlišení prvků – měníme jen ty se stejnou třídou: `<p class="trida">Odstavec</p>`.

Příklad CSS dokumentu - `style.css` (název a přípona souboru)

    /*Komentář*/
    h1, h2 { /* Elementy h1 a h2 */
      color: red;
    }
    .modry { /* Třída modry */
      color: blue;
    }
    /*Vycentrování prvku*/
    .stred {margin-left: auto; margin-right: auto;}

### Základní vlastnosti CSS

| Vlastnost      | Název v CSS        | Příklady hodnot                       |
| -------------- | ------------------ | ------------------------------------- |
| Pozadí         | `background-color` | red, #00ff00, rgb(255, 0, 0)          |
| Barva fontu    | `color`            | black, #333333, rgba(0, 0, 0, 0.8)    |
| Rodina písma   | `font-family`      | Arial, Verdana, Helvetica, sans-serif |
| Velikost písma | `font-size`        | 12px, 14px, 16px                      |
| Výška          | `height`           | 100px, 50%, auto                      |
| Šířka          | `width`            | 200px, 50%, auto                      |
| Rámeček        | `border`           | 1px solid black, 2px dashed #333333   |
