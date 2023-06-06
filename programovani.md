---
layout: default
---

# Programování

Abychom mohli přidat do stránky interaktivitu - zpracovávat formuláře a třeba propojit web s databází, potřebujeme použít nějaký programovací jazyk, v našem případě PHP.

## Proměnné

Jako vždy v programování jsou základem proměnné. Proměnná je „přihrádka“ pro ukládání hodnot.

    $jmeno = "Petr"; // Řetězec
    $vek = 35; // Celé číslo
    $prumer = 3.5; // Desetinné číslo
    $povoleno = true // Boolean

Proměnné lze vypsat do stránky:

    $mesto = "Brno";
    $ulice = "Veveří";
    echo $mesto;
    echo $mesto . " " . $ulice; // Spojovani retezcu

Proměnné mají také využití v podmínkách, které určují, co se stane při ne/splnění.

    $vek = 10;
    if ($vek >= 18) {
        echo "Můžeš vstoupit.".
    } else {
        echo "Nemůžeš vstoupit";
    }

## Pole

Jednoduché pole obsahuje prvky číslované (index) od 0 do n-1. Lze vypisovat jednotlivé prvky.

    $fruits = ["Jablko", "Hruška", "Pomeranč"];
    echo $fruits[0]; // Výstup -> Jablko

Jednoduché asociativní pole obsahuje páry s klíčem a hodnotou. Místo indexu se používá klíč.

    $student = ["name"=>"Petr","age"=>24,"grade"=>"A"];
    echo $student["name"]; // Výstup -> Petr

2D pole je stejné jako jednoduché, ale má více řádků. U každého řádku definujeme index (od 0). Pro výpis 1 prvku potřebujeme znát řádek i sloupec (tedy dva indexy).

    $pole[0] = ["Jan", "Novák", "Praha"];
    $pole[1] = ["Petr", "Veselka", "Ostrava"];
    $pole[2] = ["Josef", "Stvol", "Brno"];
    echo $pole [0][1]; // Výstup -> Novák

## Cykly

V programování využijeme také cykly, zejména foreach, který se hodí pro procházení pole. Jak už název napovídá, for each (pro každý) projde všechny prvky pole

    $fruits = ["Jablko", "Hruška", "Pomeranč"];
    foreach ($fruits as $fruit) {
        echo $fruit . "<br>; // Vypise kazdou polozku pole a odradkuje
    }

Prvky můžeme vypsat i do tabulky (zde 2D pole):

    $zamec[0] = ["Jan", "Novák" ];
    $zamec[1] = ["Petr", "Švarc"];
    echo "<table>";
    foreach($zamec as $z) { // Vybiram z pole $zamec a kazdy prvek oznacim jako $z
        echo '<tr><td>'.$z[0].'</td><td>'.$z[1].'</td></tr>';
    }
    echo "</table>";

Občas se hodí také for cyklus:

    for( $x=0; $x<9; $x++ ) {
    echo $x . ", ";
    }
