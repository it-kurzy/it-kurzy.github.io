# Úvodní lekce - HTML a CSS

HTML je jazyk webových stránek. Je doplňován CSS (kaskádové styly) a dalšími jazyky, např. PHP, které umožňuje tvorbu dynamických stránek (zpracování formuláře, připojení k databázi).

## HTML

Nezbytnou součástí HTML jsou značky, rozlišujeme **párové** a **nepárové**. Většina značek je párových (mají konec i začátek), např. `<h1>Nadpis</h1>`
Lomítko u druhé značky označuje její uzavření. Nepárové značky se používají např. u obrázků `<img>` či polí formuláře `<input>`

### Příklad - soubor index.html

    <!DOCTYPE html>
    <html>
    	<head>
    		<title>Seznam, najdu tam co neznám</title>
    	</head>
    	<body>
    	<!-- Obsah webové stránky -->
    </body>
    </html>

| Značka            | Popis                                                      |
| ----------------- | ---------------------------------------------------------- |
| `<!DOCTYPE html>` | Říká prohlížeči, že jde o dokument typu HTML               |
| `<html>`          | Určuje začátek a konec HTML dokumentu                      |
| `<head>`          | Obsahuje informace pro prohlížeč a vyhledávače             |
| `<title>`         | Název stránky, který se zobrazuje v záhlaví prohlížeče     |
| `<body>`          | Viditelný obsah stránky, jako jsou texty, obrázky a odkazy |
| `<h1>` až `<h6>`  | Nadpisy různých úrovní (h1 je nejvyšší)                    |
| `<p>`             | Odstavec textu                                             |
| `<a>`             | Vytváří odkaz na jinou stránku nebo zdroj                  |
| `<img>`           | Vkládá obrázek na stránku                                  |
| `<ul>`            | Vytváří seznam                                             |
| `<li>`            | Položka seznamu uvnitř `<ul>`                              |
| `<table>`         | Vytváří tabulku                                            |
| `<tr>`            | Řádek tabulky                                              |
| `<td>`            | Buňka tabulky                                              |
| `<form>`          | Vytváří formulář pro zadávání dat                          |
| `<input>`         | Vytváří vstupní pole v rámci formuláře                     |
| `<button>`        | Vytváří tlačítko                                           |
| `<div>`           | Slouží k logickému seskupení a formátování obsahu          |
| `<span>`          | Slouží k logickému seskupení a formátování textu           |
| `<!--Text-->`     | Text, který je vidět POUZE v kódu, ne na stránce           |

## CSS

Kaskádové styly (CSS) slouží pro změnu vzhledu prvků stránky (pozadí, barva, výška, šířka, ...).
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

Pro stylování slouží pravidla - základní zápis je: selektor {vlastnost: hodnota;}
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


[Domů](./)