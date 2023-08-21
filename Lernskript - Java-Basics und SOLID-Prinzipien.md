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

## Teil 4 Beispiele
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

```java

```

