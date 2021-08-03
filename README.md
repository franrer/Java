# Java Projekt 2021 SOSE Lagerspiel
Allgemeine Hinweise:

    Zu Implementieren ist die Programmieraufgabe in Java (Lauffähig in Java SE 15)
    Die im Java JDK enthaltenen Bibliotheken dürfen Sie verwenden. Weitere Bibliotheken sind vorab mit dem Dozenten abzustimmen. 
    Wenn Sie externe Bibliotheken verwenden, geben Sie bitte zusätzlich zu den Quelldateien eine lauffähige .jar ab
    Zu den Aufgaben ist eine entsprechende grafische Benutzeroberfläche zu entwickeln
    Arbeiten Sie mit den Prinzipien der objektorientierten Programmierung wie in der Vorlesung behandelt
    Abzugeben sind alle Quelldateien (*.java) in einem Zip gepackt über Moodle
    Es muss eine Klasse "Start.java" mit einer main-Methode geben - hier wird das Programm gestartet
    Start ist der 11.06.2021
    Abgabeschluss ist der 02.08.2021, 23:59 Uhr
    In die Bewertung fließen funktionale Anforderungen (wie unten beschrieben), aber auch subjektive Faktoren wie die Strukturierung des Codes oder 
    die Gestaltung der GUI ein.
    Die Arbeit ist keine Gruppenarbeit. Jeder muss einen individuellen Programmentwurf anfertigen
    
Allgemeines:

Entwickeln Sie ein Spiel, in der Sie in die Rolle eines Lageristen schlüpfen. Sie haben ein Lager und bekommen Aufträge, Waren einzulagern oder auszulagern. 
Für erledigte Aufträge bekommen Sie Geld. Ziel des Spiels ist es, so viel wie möglich einzunehmen.


    Das Lager:

Spiel startet, das Lager wird angelegt. Sie besitzen ein Hochregallager mit zwei Lagerplätzen Breite und fünf Lagerplätzen Höhe. Auf einem Lagerplatz finden zwei Paletten hintereinander Platz. Sie haben also insgesamt für 20 Paletten Platz. Ihr Lager ist aktuell leer.

    Der Auftrag:

Über den Button "Neuer Auftrag" kann ein neuer Auftrag abgerufen werden. Es kann sich um einen Einlagerungsauftrag oder einen Auslagerungsauftrag handeln. Der Auftrag beinhaltet folgende Informationen: Produkt (siehe 3.), Belohnung (Wert in EUR). Es gibt keine Menge, es handelt sich immer um eine Einheit. 
Für die Erzeugung der Aufträge wird eine CSV-Datei bereitgestellt. Wenn das Ende der Datei erreicht ist, kann wieder mit Auftrag 1 begonnen werden. Falls Änderungen / Ergänzungen des CSV Datei notwendig werden, dokumentieren Sie dies in einer separaten Datei und geben Sie beide Dateien mit ab.

    Die Produkte:

Es gibt verschiedene Produkte mit jeweils verschiedenen Eigenschaften.

a) Papier:
Eigenschaften: Farbe (Weiß, Grün, Blau), Größe (A3, A4, A5)
Besonderheiten: Keine

b) Holz:
Eigenschaften: Art (Kiefer, Buche, Eiche), Form (Bretter, Balken, Scheit)
Besonderheiten: Holzbalken sind lang und werden daher auf zwei Paletten verteilt. Ein gesamter Lagerplatz wird notwendig

c) Stein:
Eigenschaften: Art (Marmor, Granit, Sandstein), Gewicht (Leicht, Mittel, Schwer)
Besonderheiten: Schwere Steine sind zu Schwer für das Regal und können nur auf den unteren beiden Etagen eingelagert werden. Mittelschwere können nicht in der obersten Etage eingelagert werden.

    Die Abwicklung:

Einlagerungsauftrag: Zu einem Auftrag werden die möglichen Lagerplätze dargestellt, also freie Lagerplätze. Nach Wahl eines Lagerplatzes wird die Palette eingelagert und die Belohnung gutgeschrieben.
Auslagerungsauftrag: Zu einem Auftrag werden die möglichen Lagerplätze dargestellt, also Lagerplätze, an dem genau dieses Produkt eingelagert ist. Nach Wahl eines Lagerplatzes wird die Palette ausgelagert und die Belohnung wird gutgeschrieben.

    Die Lagerverwaltung:

Es ist möglich, dass ein Produkt zwar im Lager vorhanden ist, aber es wird durch ein anderes Produkt weiter vorne blockiert. Um dennoch an dieses Produkt heranzukommen, muss umgelagert werden. Dazu wird die gewünschte Palette ausgewählt. Wenn nicht durch andere Waren blockiert, kann die Palette einen Platz nach rechts, links, oben, unten, hinten oder vorne verschoben werden. Umlagerungen kosten 50 EUR. Des weiteren kann ein Produkt auch verschrottet werden, das kostet 300 EUR. Verschrottet werden kann nur, was sich auf der untersten Etage befindet.

    Das Auftragsmanagement:

Es können maximal vier Aufträge gleichzeitig bearbeitet werden (weitere Klicks auf "Neuer Auftrag"). So können Sie einen Auftrag auch zunächst einmal zurückstellen. Ein Auftrag kann auch abgelehnt werden, allerdings wird die Belohnung als Vertragsstrafe vom Kontostand abgezogen.

    Die Bilanz:

Natürlich muss immer der Kontostand sichtbar sein. Zusätzlich gibt es einen Button "Bilanz". Die Bilanz öffnet sich in separatem Fenster und zeigt folgende Informationen: Umsätze (Summe), Kosten (Summe) und Einzelbuchungen, also eine Tabelle mit jeder Veränderung des Kontostands. Jede Buchung ist mit einem Text (Einlagerungsauftrag, Auslagerungsauftrag, Umlagerung usw.) und einem Betrag versehen.
