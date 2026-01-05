# Kontrollstrukturen

Kontrollstrukturen ermöglichen es den Programmablauf inklusive Verzweigungen und Schleifen zu steuern.

Wir beschäftigen uns mit den folgenden Kontrollstrukturen.

- **Bedingte Anweisungen** führen den Codeblock nach der ersten wahren Bedingung einer if- oder elif-Anweisung aus. Wenn keine der Bedingungen wahr ist, wird der Codeblock nach dem else ausgeführt.

- **Schleifen** werden entweder so lange ausgeführt wie eine Bedingung wahr ist (_While_) oder iterieren über sequenzielle Datentypen wie Listen.

## Bedingte Anweisungen:

Mittels `if` wird ein Ausdruck auf _wahr_ oder _falsch_ überprüft. Ist der Ausdruck wahr wird der nachfolgende Block ausgeführt.

```python
>>> def emptyList(l):
>>>     if len(l) == 0:
>>>         print("Die Liste ist leer.")
>>> emptyList([])
>>> Die Liste ist leer.
>>> emptyList([1,2,3)
>>> 
```

Die Funktion emptyList teste ob das Argument eine leere Liste ist und gibt in dem Fall den String "Die Liste ist leer."  aus. 

Ein angehängter `else` Block wird ausgeführt falls  der Ausdruck nach _falsch_ ausgewertet wird.

```python
>>> def emptyList(l):
>>>     if len(l) == 0:
>>>         print("Die Liste ist leer.")
>>>     else:
>>>         print("Die Liste ist nicht leer.")
>>> emptyList([])
>>> Die Liste ist leer.
>>> emptyList([1,2,3])
>>> Die Liste ist nicht leer.
>>> 
```

Sollen mehrere Ausdrucke ausgwertet werden, dann kann `elif`genutzt werden.

```python
>>> def thermostat(temperatur):
>>>     if temperatur < 0:
>>>         print("Ich stelle die Heizung auf volle Pulle.")
>>>     elif temperatur < 10:
>>>         print("Etwas frisch. Ich lasse die Heizung mal laufen.")
>>>     else:
>>>         print("Wir brauchen keine Heizung.")
>>> thermostat(-5)
>>> Ich stelle die Heizung auf volle Pulle.
>>> thermostat(5)
>>> Etwas frisch. Ich lasse die Heizung mal laufen.
>>> thermostat(25)
>>> Wir brauchen keine Heizung.
>>> 
```

### Aufgabe

Die Implementierung der Funktion `emptyList` ist unvollständig, warum ?

- Was passiert wenn ich einen String, eine Zahl oder einen Wahrheitswert anstatt einer Liste an die Funktion übergebe ?
- Wie kannst Du die Funktion typsicher machen ? _Hinweis: Die Python Funktion **type(x)** gibt den Datentypen von X zurück._





