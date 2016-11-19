1 Schritt BlackMagic

2 Schritt ???

3 Schritt das Pr0gramm läuft aka PROFIT schekel schekel

alternativ folgendes:



Quelle: http://javaschubla.de/2007/javaerst0020.html



#Javaschubla.de - Java als erste Programmiersprache

##Java-Programme kompilieren und ausführen

In dieser Lektion wird das erste einfache Java-Programm vorgestellt und erklärt, wie man Java-Programme kompiliert und ausführt.

###Vorarbeit unter Windows

Voraussetzung ist, dass die PATH-Variable wie beschrieben geändert wurde. Zusätzlich sollten unbedingt folgende Einstellungen vorgenommen werden:

Einen beliebigen Ordner (z.B. durch Doppelklick auf Arbeitsplatz) öffnen
auf Extras > Ordneroptionen klicken (bei Win9x Ansicht > Ordneroptionen)
Dort Ansicht (den mittleren der drei Reiter) wählen und folgende Einstellungen vornehmen
Dateinamen in Großbuchstaben erlauben
Dateiendungen von bekannten Dateien NICHT verstecken
Unter Linux sind keine Vorarbeiten notwendig.

Los geht's

Man startet einen Texteditor (Notepad, Editor, TextPad, UltraEdit, kate, gedit, emacs, vi oder ein anderes Programm, das "plain text" (unformatierten Text) speichern kann) und tippt das Java-Programm ein. Auf keinen Fall Wordpad, Word oder OpenOffice verwenden, denn wenn man die Datei mit Formatierungen speichern würde, wäre sie unbrauchbar.

Folgendes Programm wird einfach Hallo Welt! im DOS-Fenster / auf der Konsole ausgeben:

class HalloWelt
{
  public static void main(String[] args)
  {
    System.out.println("Hallo Welt!");
  }
}
Der Datei- und Klassenname

Man speichert es unter dem Namen der Hauptklasse, hier also HalloWelt.java. (Je nach Windowsversion ist es evtl. notwendig, beim Speichern Anführungszeichen um den Namen zu setzen, damit Notepad/Editor kein .txt anhängt.)

Der Name darf keine Leerzeichen und keine Sonderzeichen enthalten (außer _ und $, die aber auch nicht erwünscht sind). Umlaute sind zwar erlaubt, sollten aber vermieden werden, falls man nicht der einzige ist, der diese Klasse benutzen wird, denn auf anderen Betriebs- oder Dateisystemen kann es sonst zu Problemen kommen. Achtung: Java unterscheidet Groß- und Kleinschreibung! HalloWelt, Hallowelt, hallowelt und HALLOWELT sind für Java 4 verschiedene Klassen/Programme.

Kompilieren (javac)

Nun müssen wir mit dem Java-Compiler, javac genannt, aus der Quelltextdatei HalloWelt.java eine Byte-Code-Datei HalloWelt.class machen.

javac ist ein Kommandozeilenprogramm, d.h. wir müssen erstmal ein DOS-Fenster (unter Windows) oder eine Konsole (unter Linux) öffnen.

Windows: MS-DOS-Eingabeaufforderung (Überspringen)

Die MS-DOS-Eingabeaufforderung (DOS-Prompt, DOS-Fenster, DOS-Box) befindet sich je nach Windows-Version unter Start > Programme oder Start > Programme > Zubehör. Man kann auch auf Start > Ausführen gehen und unter Windows 9x/ME COMMAND oder unter Windows NT/2000/XP CMD eingeben.

Jetzt sieht man ein DOS-Fenster, ein schwarzes Fenster mit weißer Schrift. Dort steht voraussichtlich

C:\Windows>
oder etwas Ähnliches. Das ist die Eingabeaufforderung oder Prompt. Man muss nun in das Verzeichnis wechseln, in dem die Datei HalloWelt.java gespeichert ist. Verzeichnisse wechselt man mit dem Befehl cd (change directory). Mit cd.. geht man ein Level nach oben (mit cd... zwei Level etc.). Ist die java-Datei beispielsweise im Verzeichnis C:\Java, gibt man also

cd..
cd java
ein (und drückt natürlich jeweils Enter). Ist die java-Datei im Verzeichnis D:\Java, muss erst das Laufwerk gewechselt werden. Dazu gibt man einfach

D:
ein, und dann wie oben

cd java
Um Verzeichnisnamen mit Leerzeichen muss man Anführungszeichen setzen, z.B.

cd "Eigene Dateien"
Eine Möglichkeit, schnell in einen Ordner zu wechseln, ist, cd (mit Leerzeichen nach cd) einzutippen und dann das Ordnersymbol von der linken oberen Ecke des Ordnerfensters in das DOS-Fenster zu ziehen.

Hat man nun zum Verzeichnis mit der HalloWelt.java-Datei navigiert, kann man dir (für directory) eingeben - das listet die Dateien im Verzeichnis auf, da sollte auch HalloW~1.jav oder HalloWelt.java zu sehen sein.

Linux: Konsole (Überspringen)

Die meisten Linux-Nutzer haben die Konsole vermutlich schon einmal benutzt. Falls nicht: im Menü unter System nach Konsole, Terminal (auch X-Terminal oder GNOME-Terminal ist richtig), Shell oder Bash suchen. Je nach System ist das Terminal-Fenster meist entweder schwarz mit weißer Schrift oder auch weiß mit schwarzer Schrift, aber es gibt auch andere Farben und durchscheinende Fenster.

Je nach System steht in diesem Fenster etwas wie

benutzername@computername:~$
benutzername ist der Name, mit dem man gerade eingeloggt ist, der computername wurde meist bei der Installation vergeben. ~ steht für das Homeverzeichnis, dort erscheint stets das jeweils aktuelle Verzeichnis. Das $ ist die Prompt (Eingabeaufforderung). Je nach System kann es sein, dass der Benutzername und/oder der Computername und/oder das aktuelle Verzeichnis nicht angezeigt wird, so dass unter Umständen nur die Prompt angezeigt wird. Statt $ kann die Prompt auch %, # oder ein anderes Symbol sein.

Man muss nun in das Verzeichnis wechseln, in dem die Datei HalloWelt.java gespeichert ist. Verzeichnisse wechselt man mit dem Befehl cd (change directory). Mit cd .. geht man ein Level nach oben (mit cd ../.. zwei Level etc.). Beachte das Leerzeichen nach cd.

Ist die java-Datei beispielsweise im Verzeichnis /home/benutzername/meinjava, gibt man also

cd meinjava
ein (und drückt natürlich Enter). Um Verzeichnisnamen mit Leerzeichen muss man Anführungszeichen setzen, z.B.

cd "Meine Javadateien"
oder die Leerzeichen mit einem Backslash (\) escapen (maskieren):

cd Meine\ Javadateien
Man gelangt schneller in den gewünschten Ordner, wenn man jeweils nur die Anfangsbuchstaben tippt und dann die Tabulatortaste drückt (das ist die Taste links neben dem Q mit den beiden entgegengesetzten Pfeilen). Unter KDE ist es auch möglich, im Konqueror rechtszuklicken und Aktion -> Terminal öffnen zu wählen.

Hat man nun zum Verzeichnis mit der HalloWelt.java-Datei navigiert, kann man ls (für list) eingeben - das listet die Dateien im Verzeichnis auf, da sollte auch HalloWelt.java zu sehen sein.

javac

Nun ist man im DOS-Fenster / in der Konsole im richtigen Verzeichnis mit der zu kompilierenden Datei HalloWelt.java. Jetzt einfach

javac HalloWelt.java
eingeben.

Wenn keine Fehlermeldung kommt und einfach wieder die Eingabeaufforderung erscheint, ist alles in Ordnung. Wenn nicht, sollte man überprüfen, ob man javac und nicht java geschrieben hat, an das .java am Ende gedacht und sich auch sonst nicht vertippt hat. Typische Fehlerquellen im Programmtext, die es zu überprüfen gilt: Groß- und Kleinschreibung (String, nicht string, System, nicht system), das Semikolon (;) nach System.out.println("Hallo Welt!") und dass sowohl vor als auch nach Hallo Welt! ein Anführungszeichen (Shift+2) steht.

Wenn also alles glatt geht, erscheint eine Datei namens HalloWelt.class im selben Verzeichnis. Das ist die Byte-Code-Datei. Die kann jetzt weitergegeben werden und unverändert unter Windows, Linux, Mac und auf Solaris-Rechnern laufen. (Wenn in der .java-Datei mehrere Klassen sind, entstehen mehrere .class-Dateien.)

Ausführen (java)

Jetzt wollen wir die Datei natürlich auch ausführen. Dafür ist die JRE (Java Runtime Environment) bzw. JVM (Java Virtual Machine, in der JRE enthalten) zuständig. Diese wird einfach mit dem Befehl java aufgerufen.

Man gibt also in der DOS-Eingabeaufforderung bzw. in der Konsole

java HalloWelt
ein. (Es ist darauf zu achten, dass es hier java, nicht javac heißt, auf die Groß- und Kleinschreibung, und dass es einfach HalloWelt, nicht HalloWelt.class oder HalloWelt.java heißt.)

Jetzt wird das Programm ausgeführt und es erscheint Hallo Welt! im DOS-Fenster / auf der Konsole. Danach ist es sofort zu Ende und es folgt wieder die Eingabeaufforderung.

Änderungen

Wenn man etwas am Programm ändert, muss man es erneut kompilieren (mit javac), bevor man es ausführt (mit java). Es gibt Entwicklungsumgebungen wie Eclipse, die einem das abnehmen, so dass man nur noch einen Button drücken muss, aber für den Anfang wollen wir es von Hand machen.

Übung 1

Fehler einbauen und sich anschauen (und möglichst merken oder evtl. sogar notieren) bei was für Fehlern der Compiler welche Fehlermeldung ausgibt. Dann kommt man später viel leichter mit den Fehlermeldungen zurecht. Also einfach mal ausprobieren, was entweder der Compiler oder aber erst die JRE sagt

wenn man das ; weglässt
wenn man versehentlich ein ; hinter public static void main(String[] args) setzt
wenn man Class statt class schreibt
wenn man Main statt main schreibt
wenn man string statt String schreibt
wenn man system statt System schreibt
wenn man die [] hinter String weglässt
wenn man eine { und/oder eine } zu viel oder zu wenig hat (man probiert am besten alle Kombinationen aus, die Fehlermeldungen sind sehr verwirrend und man sollte später unbedingt wissen, dass man bei solchen Fehlermeldungen nach seinen geschweiften Klammern schauen sollte)
wenn man an verschiedene Stellen einfach lgjklgja hinschreibt
wenn man das erste, das zweite oder beide Anführungszeichen vergisst
args (für arguments) kann man übrigens beliebig umbenennen, manche Leute schreiben argv, und man könnte auch hugo nehmen. Das ist bloß ein Variablenname. args ist am üblichsten.

Übung 2

Man kann nicht nur Strings (Zeichenketten, eingeschlossen in Anführungszeichen) mit println ausgeben, sondern z.B. auch Berechnungen. Probiere etwa

    System.out.println(1+2);
    System.out.println(1-2);
    System.out.println(3*4);
    System.out.println(12/4);
    System.out.println(12.345/3.4);
Dort werden keine Anführungszeichen gesetzt! System.out.println("1+2") würde 1+2 ausgeben, während System.out.println(1+2) 3 ausgibt.

Man kann um Zahlen und Operatoren herum beliebig Leerzeichen setzen, etwa

    System.out.println( 1 + 2 );
Diese werden nicht mit ausgegeben. Sie würden nur ausgegeben werden, wenn sie innerhalb eines Strings, also zwischen zwei Anführungszeichen wären, etwa das Leerzeichen zwischen Hallo und Welt!.

println steht für print-line, also ausgeben und eine Zeile tiefer gehen. Man kann auch System.out.print("...") verwenden, dann kommt die nächste Ausgabe auf dieselbe Zeile.

    System.out.println("Hallo");
    System.out.println("Welt!");
gibt

Hallo
Welt!
aus, während

    System.out.print("Hallo");
    System.out.println("Welt!");
HalloWelt!
ausgibt.

Probier damit etwas herum. Vorwiegend hilft es dir, mit dem Kompilieren und Ausführen vertraut zu werden.

Übung 3

Ruf die Java-API auf, die du entweder heruntergeladen hast oder von der du dir den Link gespeichert hast. Falls du das vergessen hast, nimm diesen Link: Java-API. Oben links ist ein kleiner Frame mit den Packages, unten links ist ein längerer Frame mit den Klassen und Interfaces im aktuellen Package (so lange noch kein Package ausgewählt ist, alle Klassen und Interfaces), rechts ist ein großer Frame mit der aktuell angeklickten Klasse (oder Interface, im Moment noch Package-Übersicht). Wähle links oben das Package java.lang. Das ist das Standard-Package, das immer automatisch importiert wird. Im Frame links unten findest du die Klasse String. Außerdem siehst du dort die Klasse System. Klick sie an. Sie erscheint rechts. Dort siehst du, dass sie ein Attribut namens out hat. Klick auf den Typ davor, also auf PrintStream. Du gelangst zur Klasse java.io.PrintStream. Dort siehst du, dass diese Klasse viele print- und printlnfile:///home/monika/Javatutorial/Website/2007/javaerst0020.html-Methoden (Funktionen) hat.

Erläuterungen zum HalloWelt-Programm (Überspringen)

Sich merken muss man eigentlich erstmal nur

dass man mit System.out.println etwas auf dem Bildschirm ausgibt
dass man seine Befehle in ein class Name { public static void main(String[] args) { ... } } einpackt
dass man nach jedem Befehl ein Semikolon setzt.
Aber manche Leser sind jetzt vielleicht von Neugier geplagt, was der Rest heißt. Wie gesagt ist es nicht schlimm, wenn man das anfangs nicht genau versteht, einiges kann man jetzt noch gar nicht verstehen.

public static void main(String[] args)

Mit

Rückgabetyp Name(Typ1 name1, Typ2 name2, ...)
{
  ... Befehle hier ...
}
definiert man eine Methode (= Funktion, Prozedur, Subroutine, Unterprogramm, ...) mit dem Namen Name, dem Rückgabetyp Rückgabetyp und den Parametern name1, name2, ... vom Typ Typ1, Typ2, ...

Im Beispiel

void main(String[] args)
{
  ...
}
ist der Name der Methode main, ihr Rückgabetyp ist void (was bedeutet, dass sie nichts zurückgibt), sie erhält einen Parameter namens args vom Typ String-Array (String[]). Dieser Parameter enthält übrigens die auf der Kommandozeile übergebenen Argumente (Kommandozeilenparameter).

public ist ein Access Modifier (Zugriffsmodifizierer), der öffentlich bedeutet. Es gibt außerdem private, protected und wenn man nichts hinschreibt "package level access".

static kann man erst verstehen, wenn man Objektorientierung ein bisschen versteht. Auf eine static Methode oder Variable kann man einfach über den Klassennamen zugreifen, man muss nicht erst ein Objekt erzeugen. Wenn das Programm gerade gestartet wird, gibt es noch keine Objekte, deshalb muss main static sein. (Bei Applets ist das anders, deren Methoden sind nicht static, es gibt von Anfang an ein Applet-Objekt.)

Wenn man java Klassenname aufruft, sucht die JRE in der Klassenname.class eine Methode mit Namen main, Rückgabetyp void und einem Parameter vom Typ String[] und ruft diese auf.

Konvention: Methodennamen werden klein geschrieben, innere Wörter aber groß, z.B. lastIndexOf. Das nennt man Camel Case.

class

In Java besteht alles aus Klassen. Eine Klasse ist ein Programm, eine Sammlung von Methoden, ein Typ, eine Datenstruktur und mehr.

Mit

class Klassenname
{
  ... Variablen hier ...
  ... Methoden hier ...
}
definiert man eine Klasse namens Klassenname. So haben wir im Beispiel eine Klasse namens HalloWelt definiert.

Konvention: Klassennamen werden groß geschrieben, innere Worte ebenfalls.

System.out.println

System ist, wie String auch, eine der vordefinierten Klassen im Standardpackage java.lang. Dieses Package muss man nicht explizit importieren, es wird immer automatisch importiert. Man hätte auch java.lang.System.out.println und java.lang.String[] schreiben können (tut man aber nicht).

out ist eine Variable in der Klasse System. Sie ist vom Typ PrintStream. (PrintStream ist eine Klasse im Package java.util.)

println() ist eine Methode in der Klasse PrintStream.

Konvention: Variablennamen (wie out) werden klein geschrieben, innere Worte wiederum groß.

Konstantennamen werden in ALL_CAPS (komplett groß mit Unterstrichen zur Unterteilung) geschrieben. Ansonsten werden keine Unterstriche zur Unterteilung verwendet.

Zu merken

Klassen sind (unter anderem) Programme. Die einfachste Form eines Programms ist:
class Klassenname
{
  public static void main(String[] args)
  {
    ... Anweisungen hier ...
  }
}
System.out.println(...) gibt etwas aus und geht eine Zeile tiefer, System.out.print(...) gibt etwas aus, ohne eine Zeile tiefer zu gehen.
Nach einer Anweisung folgt ein Semikolon (;).
Man kompiliert mit javac Dateiname und führt mit java Klassenname aus.
Man schreibt Klassennamen groß und innere Worte groß (CamelCase)
Man rückt nach einer öffnenden geschweiften Klammer ein (z.B. um zwei Leerzeichen) und bei der schließenden geschweiften Klammer um die gleiche Anzahl Leerzeichen wieder aus.
Java unterscheidet Groß- und Kleinbuchstaben.
In der nächsten Lektion geht es um Sonderzeichen in Strings (Zeichenketten)