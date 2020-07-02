# Master-Worker-Pattern with RMI
Das Ziel dieser Aufgabe ist es, ein Framework zu schreiben, das ein Problem (Aufgabe) in Teilprobleme
(Teilaufgaben) zerlegt und dieses Teilprobleme dann verteilt berechnen lässt. Es soll wie folgt funktionieren:

- Der __Master__ wird auf einem bekannten Rechner gestartet. Er stellt zwei Schnittstellen (interfaces) bereit.
Eine Schnittstelle interagiert mit den Workern (Master-Interface), die andere Schnittstelle mit einem
Client(Server-Interface).

- Der __Client__ kann dem Master einen Auftrag (Job) übergeben. Dieser Job besteht aus einer Funktion
(Code), die es dem Master erlaubt, anhand der Anzahl der vorhandenen Worker Teilaufgaben zu erstellen.

- Die __Worker__ registrieren sich bei dem Master. Nun laden die Worker nach Aufforderung durch den Master
eine Teilaufgabe über das Task-Interface (Code und Parameter) herunter und führen diesen Code lokal
aus. Die Ergebnisse liefern sie dem Master zurück. Dies geschieht so lange, bis es keine Teilaufgaben mehr
bei dem Server gibt

---

__Reihenfolge der Ausführung:__
Server starten --> beliebig viele Worker starten --> Client starten

__Achten: Bitte öffenen mehrere Terminals, um Programme auszuführen !!__

1. javac mwp/Main.java 		--> Gesamtes package kompilieren
2. java mwp/Main.java Server  		--> Server starten
3. java mwp/Main.java Worker		--> Ein Worker starten(natürlich können mehrere Worker gestartet werden) 
4. java mwp/Main.java Client 		--> Ein Client starten

In Server: Wenn 'q' eingegeben wird, wird der Server geschlossen. Wenn 's' eingegeben wird, wird die Anzahl von Servern ausgegeben. 

In Worker: Wenn 'quit' eingegeben wird, wird der Worker geschlossen. 

In Client: Das Ergebnis wird in Client ausgegeben. 
