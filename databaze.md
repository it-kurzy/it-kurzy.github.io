---
layout: default
---

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

| Typ           | Popis                                              |
| ------------- | -------------------------------------------------- |
| Bit           | 0-1                                                |
| Int (integer) | celá čísla                                         |
| Float         | čísla s desetinnou čárkou (tečkou)                 |
| Double        | Float s větší přesností a velikostí                |
| Char          | ukládá po jednom znaku (resp. kolik se mu přiřadí) |
| Varchar       | uchovává textové řetězce                           |
| Date          | datum ve formátu Y-m-d (rok-měsíc-den)             |
| Timestamp     | časové razítko                                     |


## SQL dotazy

Používáme databázi MySQL. Pro spuštění klikneme na **START** v rozhraní XAMPP. Do administrace se dostaneme přes tlačítko **ADMIN** 
### Správa databáze 
Používáme **phpMyAdmin**.  V levém postranním panelu můžeme zakládat nové tabulky a databáze (ikonka tabulky/databáze).

Pro založení databáze zvolte **Nová** (šedá ikonka).

![Seznam databází](/img/db1.png)

Nyní zadejte název databáze a klikněte **Vytvořit**.

![alt](/img/db2.png)


Teď nám phpMyAdmin říká, že databáze neobsahuje tabulky. Zadejte název tabulky a potvrďte.

![alt](/img/db3.png)

V prvním řádku zadejte id, u sloupce index vyberte PRIMARY, potvrďte, dále zaškrtněte volbu A_I.
U ostatních hodnot (například jméno, příjmení, věk) změňte pouze typ (INT pro čísla, VARCHAR pro text). U textových hodnot zadejte délku.

![alt](/img/db4.png)

Potvrďte kliknutím na tlačítko **Proveď** dole.

## PHP a SQL - ukázka
    // Propojeni na databazi
    include "conn.php";
    // SQL dotaz
    $sql = "SELECT Id, Prijmeni, Jmeno
        FROM spisovatele";
    // Vysledek dotazu
    $autori = fetchAll( $sql, $conn );
    // Vypis do seznamu
    echo "<ul>";
    // Kazdeho autora vypis jako - jmeno a prijmeni
    foreach( $autori as $a ){
    
    echo "<li>" . $a[ "Prijmeni" ] . " " . $a["Jmeno"] . "</li>";
    }
    echo "</ul>";