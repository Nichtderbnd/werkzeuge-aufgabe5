


Evtl. muss eine path Variable für Windwos Nutzer gesetzt werden um auf den korrekten Java Compiler hinzu weisen. 
(Windows 10 und Windows 8
Suchen Sie in der Suche, und wählen Sie dann: System (Systemsteuerung)
Klicken Sie auf den Link Erweiterte Systemeinstellungen.
Klicken Sie auf Umgebungsvariablen. Suchen Sie im Abschnitt Systemvariablen die Umgebungsvariable PATH, und wählen Sie sie. Klicken Sie auf Bearbeiten. Wenn die Umgebungsvariable PATH nicht vorhanden ist, klicken Sie auf Neu.
Geben Sie im Fenster Systemvariable bearbeiten (bzw. Neue Systemvariable) den Wert für die Umgebungsvariable PATH an. Klicken Sie auf OK. Schließen Sie alle verbleibenden Fenster durch Klicken auf OK.
Öffnen Sie das Fenster zur Eingabeaufforderung erneut, und führen Sie den Java-Code aus.Quelle https://www.java.com/de/download/help/path.xml) 


Mit Javac erzeugen wird aus unserem Quelltext Bytecode. Wir öffnen in unserem entsprechenden Verzeichnis in dem HelloWorld liegt eine Eingabeaufforderung (cmd)
Mit javac HelloWorld.java wird der Bytecode erzeugt. Nun haben wird eine HelloWorld.class Datei. Diese kann unter Windos, Linux etc. mittels JRE direkt ausgeführt werden. (Per cmd: java HelloWorld eingeben)









