# Datentypen

Python unterstützt die folgenden "built-in" Datentypen.

- Wahrheitswerte: **bool**
- Zahlen: **int**,**float**,complex
- Sequentielle Daten: **string**, tuple, **list**
- Dictionary(Wörterbuch): **dict**
- Mengen: set

Die hervorgehobenen Datentypen schauen wir uns im folgenden genauer an.

Welchen Datentyp ein Ausdruck hat kann durch Funktion **type** ausgewertet werden.

### Aufgabe

Ermittelt den Datentypen der folgenden Werte (in der interaktiven Python Shell):

- 10
- 10.0
- -10
- "10"
- []
- {}

## Bool

Die Wahrheitswerte sind bei bool klar definiert.

- true
- false


Auf dem Datentyp **bool** sind die folgenden mathematischen boolschen Operatoren spezifiert.

- X **or** Y: Logisches ODER
- X **AND** Y: Logisches UND
- **not** X: Logische Negierung

### Aufgabe 

Erstellt eine Wahrheitstabelle mit den Variablen x und y, sowie den boolschen Operatoren **or**, **and** und **not**.

| x | y | x and y | x or y | not x |
|---|---| ---     | ---    | --- |
| false | false | | | |
| false | true  | | | |
| true  | false | | | |
| true  | true  | | | |

Nutzt die interaktive Python Shell um die Tabelle auszufüllen, bzw. die Werte zu überprüfen.


### Was ist Wahrheit in Python?

Alle Werte die nach 0 ausgewertet werden sind in Pythin per Definition **false**.
- 0, 0.0 
- "" (leere Zeichenkette)
- [] (leere Liste)
- {} (leeres Wörtbuch)

Alle anderen Werte evalulieren zu **true**.


## Zahlen

- int : Ganzahlen
- float: Fließkommazahlen

Die folgenden Operatoren werden auf Zahlen unterstützt:

- **+**,**-**, **\***, **/** - Addition, Subtraktion, Multiplikation, Division
- **//** - ganzahler Anteil der Division
- **%** - modulo, Rest der Division
- **Y\*\*Z** - Y hoch Z

### Wichtige Funktionen

- abs(__Ausdruck__)
- int(__Ausdruck__)
- float(__Ausdruck__)

Viele mathematische Funktionen auf Zahlen sind in ein eigenes Modul (**math**) ausgelagert. Um diese Nutzen zu können muss da Modul vorher importiert werden.

```python
>>> import math
>>> math.pi
3.141592653589793
>>> math.sqrt(9)
3.0
```

Was fällt euch an dem Ausdruck **math.pi** auf ?

### Aufgabe 

Berechnet die folgenden Ausdrücke. Wie ist die Reihenfolge in welche die Operatoren ausgewertet werden ?

```python
>>> 4 * 3 + 6
>>> 4 + 4 * 6
>>> 2 * 2 ** 2
```

## Sequentielle Datentypen

Sequentielle Datentypen können allgemein als Container für Abfolgen
von Variablen eines beliebigen Datentyps gesehen werden. Für Strings,
Listen und Tupel gelten dieselben Standardzugriffsoperatoren.

```python
>>> s = "Hallo Du!"
         012345678
>>> s[0]
    "H"
>>> s[2:7]
    "llo D"

>>> l = [1,2,4,9,16,25]
         0 1 2 3  4  5
>>> l[0]
    1
```

### Operanden auf sequentiellen Datentypen

- x **in** s - wahr wenn das Element x in s vorkommt
- x **not in** s - falsch, wenn das Element x in s vorkommt
- len(s) - Länge von s
- s.index(i) - Erstes Auftreten von i in s
- s + t - Konkatination von s und t
- min(s) - kleinstes Element in s
- max(s) - größtes ELement in s

### String

Strings sind Zeichenketten beliebiger Länge und stehen zwischen **'** oder **"**. Die Zeichenindizes beginnen bei `0`, letzter Index: `len(string)-1`. Das Escapezeichen ist der Backslash "\\". Ein Zeichenkette welche aus drei Anführungszeichen besteht wird `"\\"\\"\\""` definiert.

- str() - wandelt x in einen String um
- 


### Listen
Listen können beliebig lang werden und können Elemente unterschiedlichen Typs beinhalten.

```python
l1 = (1,2,3,4,5,6,7,8,9)
l2 = ("Hallo", "Du", "!")
l3 = (1,true,"true")
```

Listen sind im Gegensatz zu Strings veränderbar, d.h. man kann die Elemente verändern.

#### Aufgabe 

Erstellt eine in der interaktiven Shell eine Liste mit den Elementen "Hallo", "Du" und "!". Ersetzt danach das "Du" durch euren Namen.


#### Funktionen auf Listen

| Name | Funktion |
| --- | ---|
| s.append(x)  | fügt x an s an |
| s.pop | gibt letztes Element von s zurück und löscht es |
| s.reverse() | Reihenfolge umkehren |


#### Aufgabe 

Überlegt euch ein kurzes Skript, das einen String mit den bisher kennengelernten Funktionen umkehrt.

Aus "Hier bin ich!" soll "!hci nib reiH" werden.


## Wörterbuch -  Dictionary

Der Datentyp **dict** bisher einziger Mapping-Datentyp in Python.  Der Datentyp besteht aus ungeordneten **Key** -> **Value** Paaren. 

```python
d = { Kind1: 12, Kind2: 15, Vater: 49}
```

Der Key besteht idealerweise aus einem String oder einer Zahl. Jeder Key darf nur einmal vorkommen, d.h. 

```python
>>> d = { Kind1: 12, Kind2: 15, Vater: 49, Vater: 48} 
>>> d
{Kind1: 12, Kind2: 15, Vater: 48}
```

Die Values können von einem beliebigen Typ sein.

Auf die Values wird direkt über den Key zugegriffen (auslesen, ändern, neues Mapping hinzufügen).

```python
>>> d[Kind1]
12
>>> d[Vater] = 49
>>> d
{Kind1: 12, Kind2: 15, Vater: 49}
>>> d[Mutter] = 50
>>> d
{Kind1: 12, Kind2: 15, Vater: 49, Mutter: 50}
```


