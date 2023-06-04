# Databáze

Databáze je soubor tabulek. V tabulkách jsou uložena data, název tabulky by měl souviset s jejich obsahem.
Řádky v tabulkách reprezentují jednotlivé záznamy a sloupce tabulky udávají, jaká data sloupec
obsahuje (např. Jmeno, Prijmeni či Id).

Každá tabulka by měla mít tzv. primární klíč, který se přiřadí většinou sloupci ID, nebo jinému, ve
kterém jsou ukládány jedinečné (neopakující-se) hodnoty. Poté lze např. vybrat řádek s ID 23 a jasně
lze identifikovat, který to je.

Pracovní postup je: vytvořit databázi, přidat do ní tabulky a ty poté plnit daty, nejjednodušeji to lze
provést v rozhraní phpMyAdmin.

## Datové typy
Při výběru datového typu se vždy řídíme povahou ukládaných dat (vybíráme datově nejúspornější
způsob uložení informací)

|Typ|Popis|
|-------------|---------|
| Bit |0-1|
| Int (integer)| celá čísla|
| Float| čísla s desetinnou čárkou (tečkou)|
| Double| Float s větší přesností a velikostí|
| Char |ukládá po jednom znaku (resp. kolik se mu přiřadí)|
| Varchar| uchovává textové řetězce|
| Date |datum ve formátu Y-m-d (rok-měsíc-den)|
| Timestamp |časové razítko|
