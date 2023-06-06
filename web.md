---
layout: default
---

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
