# Java cheatsheet

:information_source: Basierend auf dem Original von [LeCoupa/awesome-cheatsheets](https://github.com/LeCoupa/awesome-cheatsheets/blob/master/languages/java.md)


## Hallo Welt

```java
// Datei: HalloWelt.java
public class HalloWelt {
  // main() ist der Startpunkt
  public static void main (String[] args){
    // gibt "Hallo Welt" auf der Konsole aus
    System.out.println("Hallo Welt");
  }
}
```

# Übesetzen und ausführen von Java-Code

Einen Terminal öffnen und un das Quell-Code-Verzeichnis wechseln

```bash
# Java Code compilieren:
javac HalloWelt.java

# Programm starten
java HelloWorld
```


## Datentypen

|   Type  |      Art                |            Wertebereich      | Operatoren |
|:-------:|:-----------------------:|:----------------------------:|:---------:|
| int     | Ganze Zahlen (Integer)| zwischen -2^31 und + (2^31)-1 | + - * / % |
| double  | Gleitkommazahlen      |         Realezahlen           |  + - * /  |
| boolean |      boolean Werte    |         true oder false       | && \|\| ! |
| char    |        Zeichen        |     abc...z und Satzzeichen   |           |
| String  | Zeichenketten         |                               |           |


## Deklaration und Wertzuweisung

```java
// Allgemein
// <Datentyp> <Variablenname>;

// Deklaration einfach
int a;

// Deklaration mehrfach
int a,c;

// Deklaration und gleichzeitge Wertzuweisung
int a = 23;

// Wertezuweisung
a = 13212;

// Deklaration und Zuweisung durch Berechnung
int c = a + b;
```

## Vergleichsoperatoren

| Operator  |        Bedeutung    |
|:---------:|:-------------------:|
|     ==    |         gleich      |
|     !=    |       ungleich      |
|     <     |       kleiner als   |
|     >     |      größer als     |
|     <=    |   kleiner gleich    |
|     >=    | größer gleich       |


## Konsolenausgabe

```java
// Variablen Deklaration und Zuweisung
String s = "Happy Hacking!"

// einfache Ausgabe
System.out.print(s);

// Ausgabe mit Zeilenumbruch
System.out.println(s);

// Verknüpfung von Strings
System.out.println("Hallo Welt!" + s);

// Leerzeile
System.out.println();
```

## Typenumwandlung (Casting)
```java
// Variablen Deklaration und Zuweisung
String s = "Java 101"

// Konvertierung in "Java 101" zu einem Ganzzahlenwert
int Integer.parseInt(String s);

// Konvertierung in "Java 101" zu einem Double-Wert
double Double.parseDouble(s);

// Konvertierung in "Java 101" zu einem Long-Wert
long Long.parseLong(String s);
```

## Programmfluss und Kontrollstrukturen

### Kontrollstruktur
> IF Statement
```java
// Wenn x größer als y ist, dann...
if (x > y) {
  // ...führe den Code in dem Block aus
}
```

> IF-ELSE STATEMENT
```java
// Wenn x größer als y ist, dann...
if (x > y) {
  // ...führe den Code in dem Block aus
}else{
  // ... sonst führe diesen Block aus
}
```

> Verschachtelte Bedingungen
```java
// Wenn x größer als y ist, dann...
if (x > y) {
  // ...führe den Code in dem Block aus

// wenn x gleich y ist...
}else if(x == y){
  // .. führe diesen Block aus
}else{
  // ... sonst führe diesen Block aus
}
```

> SWITCH STATEMENT
```java
switch (VARIABLE-ZUM-AUSWERTEN) {
  case value:
    Statement;
    break;
  ...
  ...
  ...
  default:
    Statement;
    break;
}
```

#### ANATOMY OF A LOOP  STATEMENT
> FOR LOOP STATEMENT
```java
for (zaehlvariable; Abbruchbedingung; Schrittweite){
  // Code
}
```
**Beispiel:**

_Zähle von 0 bis 10 in Einer-Schritten und gib die Zahl auf der Konsole aus_:

```java
for (int i = 0; i <= 10; i++) {
    System.out.println(i);
}
```

> FOR-EACH STATEMENT
```java
for(dataType item : array) {
    // code
}
```
**Beispiel:**

_gib alle Elemente aus dem Array numbers aus_

```java
// array of numbers
int[] numbers = {100, 200, 300, 400};

// for each loop
for (int number: numbers) {
  System.out.println(number);
}
```

> WHILE LOOP STATEMENT
```java
while(Abbruchbedingung){
  // code
}
```
**Beispiel:**

_Zähle von 0 bis 10 in Einer-Schritten und gib die Zahl auf der Konsole aus_:

```java
// Zählvariable
int i = 0;

while (i <= 10){
  System.out.println(i);
  i++;    // i = i +1 ;
}
```

> DO-WHILE LOOP STATEMENT

Fußgesteuert -> der Block wird immer mind. einmal ausgeführt.

```java
do{
  // code
} while(Abbruchbedingung);
```

**Beispiel:**

_Zähle von 0 bis 10 in Einer-Schritten und gib die Zahl auf der Konsole aus_:

```java
int i = 0;
do{
  System.out.println(i);
  i++;
} while(i <= 10);
```

## ARRAY

```java
int[]           ai;        // array of int
Object[]        ao;        // array of Object
```

> DECLARATION OF ARRAY VARIABLE

```java
// Deklaration und Zuweisung
int[] zahlen = { 1, 1, 2, 6, 24, 120, 720, 5040 };
String[] aas    = { "array", "of", "String", };
```

## Zugriffsbeschränkungen

* default (No keyword required)
* `private`
* `public`
* `protected`

### NON ACCESS MODIFIERS

* `static`
* `final`
* `transient`
* `abstract`
* `synchronized`
* `volatile`

## Object Oriented Programming (OOPs) Concept :clipboard:

### OBJECT

```java
// Deklaration einer Variable vom Objekt-Typ "String"
String s;

// Konstruktur aufrufen
s = new String ("Hallo Welt");

// Klassenmethode ausführen die sich auf den Inhalt der Variable bezieht
char c = s.chartAt(4);
```
### Instanzvariablen

* Instanzvariablen sind nur innerhalb der Klasse _sichtbar_
* mit Hilfe von _getter_ und _setter_ können diese abgerufen oder verändert werden
  * `setter` sind vom typ `void` und sollten als Argument den Datentyp der jeweiligen Instanzvariable haben
  * `getter` geben den Datentyp zurück der Instanzvariable und sollten keine Argumente haben
* durch den `this` Operator kann man auf die Instanzvariablen direkt zugreifen

**Beispiel: Einfache Klasse:**
```java
public class Fahrzeug {
  private String name;
}
```

**Beispiel Klasse mit getter und setter:**
```java
public class Fahrzeug {
  private String name;

  public void setName(String name){
    this.name = name;
  }

  public String getName(){
    return this.name;
  }
}
```

### Methoden

* Code wiederverwenden statt neuschreiben
* Testbarkeit erhöhen
* Lesbarkeit verbessern

> Allgemein
```
<Sichtbarkeit> <Rückgabewert> <Methodenname>(<Parameter>){
  // Code
}
```

**Beispiel:**
```java
// addition zweier Zahlen a und b
public int sum (int a, int b) {
  // lokale variable
  int result;

  // Berechnung
  result = a + b;

  // Ergebnis zurückgeben
  return result;
}
```

Vereinfacht:

```java
// addition zweier Zahlen a und b
public int sum (int a, int b) {
  // Ergebnis direkt zurückgeben
  return (a + b);
}
```

### Klassendeklaration
```java
class MyClass {
    // Instanzvariablen
    // Instanzmethoden
}
```
**Beispiel:**

```java
public class Fahrzeug {
  private String name;

  public void fahr(){
    // code
  }
}
```
### Klassen Deklaration mit Vererbung
```java
class Auto extends Fahrzeug {
  private String nummernSchild;

  public void abs(){
    // code
  }
}
```
* Die Klasse `Auto` ist eine Unterklasse von der Klasse `Fahrzeug` (Spezialisierung)
* Die Klasse `Auto` übernimmt automatisch alle Funktionen und Attribute der Klasse `Fahrzeug`
* Die Klasse `Auto` kann die Funktionen der Klasse `Fahrzeug` erweitern und/oder überschreiben
* mit `super` können Methoden und Variablen der Basis-Klasse direkt aufgerufen werden
  * dies gilt auch für den Konstruktor
#### Konstruktoren

* Jede Klasse hat automatisch einen gleichnamigen Konstruktor
  * dieser kann explizt sein (angegeben) oder implizit (nicht angegeben) sein
* Der Konstruktor wird automatisch beim Erstellen eines Objekt ausgeführt
* Konstruktoren haben keinen `return` Wert


**Beispiel:**
```java
public class Fahrzeug {
  private String name;

  // Konstruktor ohne Argumente
  public Fahrzeug(){
    // code
  }

  // Konstruktor mit Argumenten
  public Fahrzeug(String name){
    // code
    this.name = name;
  }

}
```

### Polymorphismus

* Die _Vielfältigkeit_ bei der Objekte in verschiedenen Situationen verschieden reagieren können
#### Variante 1: Methodenüberladung
* Deklaration einer Methode mit verschiedenen übergabe Parametern
* je nachdem mit wie viel Parametern die Methode aufgerufen wird, verändert sie das _Verhalten_ der Klasse

```java
public class Fahrzeug {
  private String name;

  // Methode ohne Argumente
  public faehrt(){
    // code
  }

  // Methode mit Argumenten
  public faehrt(String Richtung){
    // code
  }

  // Methode mit Argumenten
  public faehrt(String Richtung, int Geschwindigkeit){
    // code
  }

}
```
#### Variante 2: Methodenüberschreibung
* Die Subklasse (Kindklasse) kann Methoden der Basisklasse (Eltern-Klasse) überschreiben

> Basis-Klasse Fahrzeug
```java
public class Fahrzeug {
  private String name;

  // Methode ohne Argumente
  public faehrt(){
    // code
    System.out.println("Das Fahrzeug fährt");
  }
}
```

> Sub-Klasse erbt alle Funktionen und überschreibt die "faehrt" Methode
```java
public class Auto implements Fahrzeug{

  @Override
  public void faehrt(){
    System.out.println("Das Auto fährt");
  }

}
```

> Beispiel aufruf
```java
// Basis-Klasse
// gibt "Das Fahrzeug fährt" auf der Konsole aus
Fahrzeug fahrzeug = new Fahrzeug();
fahrzeug.faehrt();

// Sub-Klasse
// gibt "Das Auto fährt" auf der Konsole aus
Fahrzeug auto = new Auto();
auto.faehrt();
```

### Abstraktion

* Abstraktion _versteckt_ Implementierungsdetails und gibt nur die Schnittstellen bekannt
* Erbende Klasse müssen diese Schnittstellen selbst implementieren
* Abstraktionen können sein:
  1. Abstract Class
  2. Interface
  3. Abstract Methods (in einer Klasse)

#### Abstract Class
* Eine _abstract class_ muss mit dem Schlüsselwort `abstract` deklariert werden
* Die Klasse kann `abstract` und `non-abstract` Methoden beinhalten
* Kann nicht Initialisiert werden
* Kann Konstruktoren und `static` Methoden beinhalten


```java
abstract class Blume{
  // Abstrakte Methode "duft()" - muss dann von jeder Subklasse implementiert werden
  abstract String duft();

  // nicht abstrakte Methode kann von jeder Subklasse genutzt werden
  public String pflanzen(){
      System.out.println("Ich werden gepflanzt");
  }
}

public class Rose extends Blume{
  // Implementierung der "duft()" Methode
  private String duft(){
    System.out.println("Rosen duften gut!");
  }
}
```

#### Interface
* `Interface` ist a blueprint (Bauplan) einer **class**.
* Beinhaltet nur Abstrakte Methoden

**Beispiel:**
```java
// Interface gibt die Methoden vor die Implementiert werden müssen
interface Papier{
    void drucken();
}

// Sub-Klasse implementiert die Vorgaben
public class A4 implements Papier{
    public void drucken(){
      System.out.println("Seite wird gedruckt");
    }
}
```
