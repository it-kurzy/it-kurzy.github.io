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

    $fruits = array("Jablko", "Hruška", "Pomeranč");

Jednoduché asociativní pole obsahuje páry s klíčem a hodnotou. Místo indexu se používá klíč.

    $student = array("name"=>"Petr","age"=>24,"grade"=>"A");
    echo $student["name"]; // Výstup -> Petr

## Cykly

V programování využijeme také cykly, zejména foreach, který se hodí pro procházení pole. Jak už název napovídá, for each (pro každý) projde všechny prvky pole

    $fruits = array("Jablko", "Hruška", "Pomeranč");
    foreach ($fruits as $fruit) {
        echo $fruit . "<br>;
    }

[Domů](./)