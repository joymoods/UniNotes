- [[#Teil 1: Java-Basics|Teil 1: Java-Basics]]
	- [[#Teil 1: Java-Basics#1.1 Einführung in Java|1.1 Einführung in Java]]
	- [[#Teil 1: Java-Basics#1.2 Datentypen und Variablen|1.2 Datentypen und Variablen]]
	- [[#Teil 1: Java-Basics#1.3 Kontrollstrukturen|1.3 Kontrollstrukturen]]
	- [[#Teil 1: Java-Basics#1.4 Arrays|1.4 Arrays]]
	- [[#Teil 1: Java-Basics#1.5 Funktionen (Methoden)|1.5 Funktionen (Methoden)]]
	- [[#Teil 1: Java-Basics#1.6 Objektorientierte Programmierung (OOP)|1.6 Objektorientierte Programmierung (OOP)]]
	- [[#Teil 1: Java-Basics#1.7 Vererbung und Polymorphismus|1.7 Vererbung und Polymorphismus]]
		- [[#1.7 Vererbung und Polymorphismus#Beispiel|Beispiel]]
- [[#Teil 2: SOLID-Prinzipien|Teil 2: SOLID-Prinzipien]]
	- [[#Teil 2: SOLID-Prinzipien#2.1 SOLID-Grundlagen|2.1 SOLID-Grundlagen]]
	- [[#Teil 2: SOLID-Prinzipien#2.2 Anwendung der SOLID-Prinzipien|2.2 Anwendung der SOLID-Prinzipien]]
	- [[#Teil 2: SOLID-Prinzipien#2.3 S.O.L.I.D.|2.3 S.O.L.I.D.]]
		- [[#2.3 S.O.L.I.D.#S - SRP (Single Responsibility Principle)|S - SRP (Single Responsibility Principle)]]
		- [[#2.3 S.O.L.I.D.#O - OCP (Open-Closed Principle)|O - OCP (Open-Closed Principle)]]
		- [[#2.3 S.O.L.I.D.#L - LSP (Liskov Substitution Principle)|L - LSP (Liskov Substitution Principle)]]
		- [[#2.3 S.O.L.I.D.#I - ISP (Interface Segregation Principle)|I - ISP (Interface Segregation Principle)]]
		- [[#2.3 S.O.L.I.D.#D - DIP (Dependency Inversion Principle)|D - DIP (Dependency Inversion Principle)]]
- [[#Teil 3: Übungen und Projekte|Teil 3: Übungen und Projekte]]
	- [[#Teil 3: Übungen und Projekte#3.1 Übungen zu Java-Basics|3.1 Übungen zu Java-Basics]]
	- [[#Teil 3: Übungen und Projekte#3.2 Mini-Projekt: Online-Shop|3.2 Mini-Projekt: Online-Shop]]
- [[#Teil 4: Beispiele|Teil 4: Beispiele]]
	- [[#Teil 4: Beispiele#BMI Rechner|BMI Rechner]]
	- [[#Teil 4: Beispiele#Boolean|Boolean]]
	- [[#Teil 4: Beispiele#Debugübung|Debugübung]]
	- [[#Teil 4: Beispiele#For / While Schleife|For / While Schleife]]
		- [[#For / While Schleife#While|While]]
		- [[#For / While Schleife#For|For]]

## Teil 1: Java-Basics

### 1.1 Einführung in Java

- **Java-Grundlagen**: Was ist Java und warum wird es verwendet?
- **Installation**: Installation von Java Development Kit (JDK) und Entwicklungsumgebung (IDE).
- **Hello World**: Schreiben und Ausführen eines einfachen Java-Programms.

### 1.2 Datentypen und Variablen

- **Variablen**: Deklaration, Initialisierung und Zuweisung.
- **Datentypen**: Ganzzahlen (int, long), Gleitkommazahlen (float, double), Zeichen (char), Booleans.
- **Operatoren**: Arithmetische, Vergleichs- und logische Operatoren.

### 1.3 Kontrollstrukturen

- **Bedingungen**: `if`, `else if`, `else` Anweisungen.
- **Schleifen**: `for`, `while`, `do-while` Schleifen.
- **Schalter-Anweisung**: `switch` für mehrere Fallunterscheidungen.

### 1.4 Arrays

- **Arrays erstellen**: Deklaration, Initialisierung und Zugriff auf Array-Elemente.
- **Schleifen und Arrays**: Iteration durch Arrays mit Schleifen.

### 1.5 Funktionen (Methoden)

- **Methoden definieren und aufrufen**: Parameter, Rückgabewerte.
- **Rekursion**: Grundlagen der rekursiven Methoden.

### 1.6 Objektorientierte Programmierung (OOP)

- **Klassen und Objekte**: Definition von Klassen, Erzeugung von Objekten.
- **Eigenschaften und Methoden**: Klassenattribute und -methoden.
- **Konstruktoren**: Erstellen von Konstruktoren für Klassen.

### 1.7 Vererbung und Polymorphismus

- **Vererbung**: Erstellen von Subklassen und Ableiten von Eigenschaften und Methoden.
- **Polymorphismus**: Verwendung von Schnittstellen und abstrakten Klassen.
#### Beispiel
```java
// Die Elternklasse (Superklasse)
class Fahrzeug {
    String marke;
    int baujahr;

    public Fahrzeug(String marke, int baujahr) {
        this.marke = marke;
        this.baujahr = baujahr;
    }

    public void starten() {
        System.out.println("Das Fahrzeug startet.");
    }

    public void stoppen() {
        System.out.println("Das Fahrzeug stoppt.");
    }
}

// Die Kindklasse (Unterklasse) erbt von der Superklasse Fahrzeug
class Auto extends Fahrzeug {
    int anzahlTueren;

    public Auto(String marke, int baujahr, int anzahlTueren) {
        super(marke, baujahr); // Aufruf des Konstruktors der Superklasse
        this.anzahlTueren = anzahlTueren;
    }

    // Überschreiben der starten-Methode aus der Superklasse
    @Override
    public void starten() {
        System.out.println("Das Auto mit " + anzahlTueren + " Türen startet.");
    }

    public void hupen() {
        System.out.println("Das Auto hupt.");
    }
}

public class VererbungUndPolymorphismus {
    public static void main(String[] args) {
        // Erzeugen eines Fahrzeugs (Objekts der Superklasse)
        Fahrzeug fahrzeug = new Fahrzeug("Fahrzeug A", 2020);
        fahrzeug.starten();
        fahrzeug.stoppen();

        // Erzeugen eines Autos (Objekts der Kindklasse)
        Auto auto = new Auto("Auto X", 2022, 4);
        auto.starten();
        auto.stoppen();
        auto.hupen();

        // Polymorphismus: Ein Auto-Objekt kann in einer Fahrzeug-Variablen gespeichert werden
        Fahrzeug autoAlsFahrzeug = new Auto("Auto Y", 2021, 2);
        autoAlsFahrzeug.starten();
        autoAlsFahrzeug.stoppen();

        // Beachten Sie, dass die starten-Methode je nach tatsächlichem Objekt aufgerufen wird
        // und die Methode der jeweiligen Klasse verwendet wird.
    }
}

```

## Teil 2: SOLID-Prinzipien

### 2.1 SOLID-Grundlagen

- **Single Responsibility Principle (SRP)**: Die Verantwortung einer Klasse sollte auf eine einzige Aufgabe begrenzt sein.
- **Open-Closed Principle (OCP)**: Klassen sollten für Erweiterungen offen, aber für Änderungen geschlossen sein.
- **Liskov Substitution Principle (LSP)**: Subtypen müssen sich nahtlos durch ihre Basistypen ersetzen lassen.
- **Interface Segregation Principle (ISP)**: Clienten sollten nicht von Schnittstellen abhängig sein, die sie nicht nutzen.
- **Dependency Inversion Principle (DIP)**: Abhängigkeiten sollten von abstrakten Klassen und Schnittstellen statt von konkreten Klassen abgeleitet werden.

### 2.2 Anwendung der SOLID-Prinzipien

- **SRP in Java**: Aufteilung von Klassen in kleinere, spezifische Klassen.
- **OCP in Java**: Verwendung von abstrakten Klassen und Schnittstellen für Erweiterbarkeit.
- **LSP in Java**: Sicherstellung, dass Subtypen die Verträge ihrer Basistypen einhalten.
- **ISP in Java**: Aufteilung von großen Schnittstellen in kleinere, spezifischere Schnittstellen.
- **DIP in Java**: Verwendung von Abhängigkeitsinjektion für lose Kopplung.

### 2.3 S.O.L.I.D.

#### S - SRP (Single Responsibility Principle)

Das SRP besagt, dass eine Klasse nur eine Verantwortung haben sollte. In diesem Beispiel haben wir zwei Klassen, jede mit einer separaten Verantwortung.
```java
// Verletzung des SRP: Eine Klasse mit zwei Verantwortlichkeiten
class Task {
    public void createTask() {
        // Erstellen einer Aufgabe in der Datenbank
    }
    
    public void printTaskReport() {
        // Drucken eines Aufgabenberichts
    }
}
```

Verbesserte Version:
```java
// Anwendung des SRP: Aufteilung der Verantwortlichkeiten auf zwei Klassen
class TaskCreator {
    public void createTask() {
        // Erstellen einer Aufgabe in der Datenbank
    }
}

class TaskReporter {
    public void printTaskReport() {
        // Drucken eines Aufgabenberichts
    }
}
```

#### O - OCP (Open-Closed Principle)

Das OCP besagt, dass Klassen offen für Erweiterungen, aber geschlossen für Änderungen sein sollten. Hier ist ein Beispiel, das das OCP verwendet:
```java
// Verletzung des OCP: Änderungen an der Klasse erforderlich, um einen neuen Task-Typ hinzuzufügen
class Task {
    public void performTask() {
        // Führe eine allgemeine Aufgabe aus
    }
}

class NewTask extends Task {
    public void performTask() {
        // Führe eine spezielle Aufgabe aus
    }
}
```

Verbesserte Version:
```java
// Anwendung des OCP: Verwendung von abstrakten Klassen und Erweiterung für neue Task-Typen
abstract class Task {
    public abstract void performTask();
}

class GeneralTask extends Task {
    public void performTask() {
        // Führe eine allgemeine Aufgabe aus
    }
}

class NewTask extends Task {
    public void performTask() {
        // Führe eine spezielle Aufgabe aus
    }
}
```

#### L - LSP (Liskov Substitution Principle)

Das LSP besagt, dass Subtypen sich nahtlos durch ihre Basistypen ersetzen lassen sollten. Hier ist ein einfaches Beispiel:
```java
// Verletzung des LSP: Subtyp bricht die Verträge des Basistyps
class Bird {
    public void fly() {
        // Fliege
    }
}

class Ostrich extends Bird {
    public void fly() {
        // Ein Strauß kann nicht fliegen, aber diese Methode ist geerbt
    }
}
```

Verbesserte Version:
```java
// Anwendung des LSP: Subtyp hält sich an die Verträge des Basistyps
abstract class Bird {
    public abstract void move();
}

class Sparrow extends Bird {
    public void move() {
        // Fliege
    }
}

class Ostrich extends Bird {
    public void move() {
        // Laufe, aber nicht fliegen
    }
}
```

#### I - ISP (Interface Segregation Principle)

Das ISP besagt, dass Clients nicht von Schnittstellen abhängig sein sollten, die sie nicht nutzen. Hier ist ein Beispiel:
```java
// Verletzung des ISP: Eine umfangreiche Schnittstelle, die nicht alle Clients benötigen
interface Worker {
    void work();
    void eat();
    void sleep();
}

class Robot implements Worker {
    public void work() {
        // Arbeite
    }

    public void eat() {
        // Essen (nicht relevant für einen Roboter)
    }

    public void sleep() {
        // Schlafen (nicht relevant für einen Roboter)
    }
}
```

Verbessert Version:
```java
// Anwendung des ISP: Aufteilung der Schnittstellen für verschiedene Clients
interface Workable {
    void work();
}

interface Eatable {
    void eat();
}

interface Sleepable {
    void sleep();
}

class Robot implements Workable {
    public void work() {
        // Arbeite
    }
}
```

#### D - DIP (Dependency Inversion Principle)

Das DIP besagt, dass Abhängigkeiten von abstrakten Klassen und Schnittstellen abgeleitet werden sollten, nicht von konkreten Klassen. Hier ist ein Beispiel:
```java
// Verletzung des DIP: Hohe Ebene hängt von niedriger Ebene ab
class LightBulb {
    public void turnOn() {
        // Schalte die Glühbirne ein
    }
}

class Switch {
    private LightBulb bulb;

    public Switch() {
        this.bulb = new LightBulb();
    }

    public void operate() {
        bulb.turnOn();
    }
}
```

Verbesserte Version:
```java
// Anwendung des DIP: Abhängigkeit von abstrakten Klassen/Schnittstellen
interface Switchable {
    void turnOn();
}

class LightBulb implements Switchable {
    public void turnOn() {
        // Schalte die Glühbirne ein
    }
}

class Switch {
    private Switchable device;

    public Switch(Switchable device) {
        this.device = device;
    }

    public void operate() {
        device.turnOn();
    }
}
```
## Teil 3: Übungen und Projekte

### 3.1 Übungen zu Java-Basics

- Schreiben Sie ein Java-Programm, das den Benutzer nach seinem Namen fragt und ihn dann mit "Hallo [Name]!" begrüßt.
    
- Erstellen Sie eine Klasse, die einen einfachen Taschenrechner darstellt. Die Klasse sollte Methoden zum Addieren, Subtrahieren, Multiplizieren und Teilen von Zahlen haben.
    
- Implementieren Sie eine Schleife, die die ersten 20 Fibonacci-Zahlen generiert und ausgibt.
    

### 3.2 Mini-Projekt: Online-Shop

**Beschreibung**: Sie sollen einen einfachen Online-Shop erstellen, der Produkte anzeigt, in den Warenkorb legt und den Gesamtbetrag berechnet. Dabei sollen Sie die SOLID-Prinzipien anwenden, um den Code erweiterbar und wartbar zu gestalten.

**Anforderungen**:

1. **Produkte**: Erstellen Sie eine Klasse `Product`, die Produkteigenschaften wie Name, Preis und Verfügbarkeit enthält.
    
2. **Warenkorb**: Implementieren Sie eine Warenkorb-Klasse, die Produkte hinzufügen, entfernen und den Gesamtbetrag berechnen kann.
    
3. **Benutzeroberfläche**: Erstellen Sie eine einfache Benutzeroberfläche, die dem Benutzer ermöglicht, Produkte anzuzeigen, zum Warenkorb hinzuzufügen und den Gesamtbetrag anzuzeigen.
    
4. **SOLID-Prinzipien**: Stellen Sie sicher, dass Ihr Code die SOLID-Prinzipien berücksichtigt. Trennen Sie Verantwortlichkeiten, erlauben Sie Erweiterungen und vermeiden Sie harte Abhängigkeiten.
    
5. **Testen**: Schreiben Sie Testfälle, um sicherzustellen, dass Ihr Online-Shop wie erwartet funktioniert.
    

**Bonus**:

- Fügen Sie die Möglichkeit hinzu, Benutzerkonten zu erstellen und sich anzumelden.
    
- Implementieren Sie eine Bestellfunktion, um Produkte zu kaufen und Bestellungen zu verfolgen.

## Teil 4: Beispiele
### BMI Rechner
```java
import java.util.Scanner;

  

public class bmiChat {

    public static void main(String[] args) {

        Scanner scanner = new Scanner(System.in);

        System.out.println("Wie ist dein Name? ");

        String name = scanner.next();

  

        System.out.println("Wie groß bist du (in Metern)? ");

        float height = scanner.nextFloat();

  

        System.out.println("Und wie schwer bist du (in Kilogramm)? ");

        float weight = scanner.nextFloat();

  

        scanner.close();

  

        float bmi = weight / (height * height);

  

        String formattedBMI = String.format("%.1f", bmi);

  

        System.out.println("Hey " + name + ", dein BMI beträgt " + formattedBMI);

  

        if (bmi < 18.5) {

            System.out.println("Du bist untergewichtig.");

        } else if (bmi >= 18.5 && bmi < 24.9) {

            System.out.println("Du hast Normalgewicht.");

        } else if (bmi >= 25 && bmi < 29.9) {

            System.out.println("Du bist übergewichtig.");

        } else if (bmi >= 30 && bmi < 34.9) {

            System.out.println("Du hast den Adipositas Grad I");

        } else if (bmi >= 35 && bmi < 39.9) {

            System.out.println("Du hast den Adipositas Grad II");

        } else {

            System.out.println("Du hast den Adipositas Grad III");

        }

    }

}
```

### Boolean
```java
import java.util.Scanner;

  

public class bool {

    public static void main(String[] args) {

        Scanner scanner = new Scanner(System.in);

        System.out.println("Sind Sie 18?");

        System.out.println("1. Ja");

        System.out.println("2. Nein");

        int Alter = scanner.nextInt();

  

        scanner.close();

        boolean ü18;

  

        switch (Alter) {

            case 1:

                ü18 = true;

                break;

            case 2:

                ü18 = false;

                break;

            default:

                System.out.println("Eingabe ungültig! Bitte versuchen Sie es erneut");

                return;

        }

  

        if (ü18) {

            ü18 = true;

            System.out.println("Glückwunsch! Du bist drin ;)");

        } else {

            ü18 = false;

            System.out.println("Du kommst net rin!");

        }

    }

}
```
### Debugübung
Mit Fehler:
```java
public class DebuggingÜbung {
    public static void main(String[] args) {
        int zahl1 = 5;
        int zahl2 = 0;
        
        int ergebnis = divide(zahl1, zahl2);
        
        System.out.println("Das Ergebnis der Division ist: " + ergebnis);
    }
    
    public static int divide(int a, int b) {
        int result = a / b;
        return result;
    }
}
```

Gelöst:
```java
public class DebuggingÜbung {
    public static void main(String[] args) {
        double zahl1 = 5;
        double zahl2 = 2;
        double ergebnis = divide(zahl1, zahl2);
        System.out.println("Das Ergebnis der Division ist: " + ergebnis);
    }
    public static double divide(double zahl1, double zahl2) {
        double result = zahl1 / zahl2;
        return result;
    }
}
```
### For / While Schleife

#### While

- Die `while`-Schleife wird verwendet, wenn die Anzahl der Schleifenwiederholungen im Voraus nicht bekannt ist oder wenn die Schleife von einer Bedingung abhängt.
- Sie hat nur eine Bedingung in der Kopfzeile, und solange diese Bedingung wahr (true) ist, wird die Schleife weiterhin wiederholt.
- Die Initialisierung und Aktualisierung müssen manuell im Schleifenkörper durchgeführt werden.
- `while`-Schleifen eignen sich gut, wenn du eine Schleife ausführen möchtest, solange eine bestimmte Bedingung erfüllt ist.
```java
public class whileschleife {
    public static void main(String[] args) {
        int i = 0;
            while (i < 5) {
                System.out.println("Hallo, die Schleife ist an.");
                try {
                    Thread.sleep(500);
                } catch (InterruptedException e) {
                    e.printStackTrace();
                }
                i++;
            }  
    }
}
```

#### For

- Die `for`-Schleife wird normalerweise verwendet, wenn die Anzahl der Schleifenwiederholungen im Voraus bekannt ist oder wenn eine spezifische Anzahl von Iterationen durchgeführt werden soll.
- Sie hat eine Initialisierung, eine Bedingung und eine Aktualisierung in der Schleifenkopfzeile, die die Schleifensteuerung regeln. Zum Beispiel: `for (int i = 0; i < 5; i++)`.
- Die Initialisierung wird nur einmal am Anfang ausgeführt, die Bedingung wird vor jeder Iteration überprüft, und die Aktualisierung wird nach jeder Iteration durchgeführt.
- Ein Vorteil der `for`-Schleife ist, dass die Schleifenkontrollelemente (Initialisierung, Bedingung, Aktualisierung) an einer Stelle klar definiert sind.
```java
public class forschleife {
    public static void main(String[] args) {
            for (int i = 0; i < 5; i++) {
                System.out.println("Hallo, die Schleife ist an.");
                try {
                    Thread.sleep(500);
                } catch (InterruptedException e) {
                    e.printStackTrace();
                }
            }  
    }
}
```