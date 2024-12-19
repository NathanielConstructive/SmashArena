# Projekt-Dokumentation



| Datum       | Version | Zusammenfassung                                                                                                                                               |
|-------------|---------|----------------------------------------------------------------------------------------------------------------------------------------------------------------|
| 01.11.2024  | 0.0.1   | Projektbeginn, Informieren und Planen                                                                                                                          |
| 08.11.2024  | 0.0.2   | Verzögerung wegen Kickoff IDPA, Änderung von Plan, zuerst Hauptmenü und Settings, danach Select Screen, Hauptscreen erstellt und implementiert, sowie einen Character mit Hitboxes erstellt. |
| 15.11.2024  | 0.0.3   | Settingsmenu erstellt und implementiert, Verzögerung mit Verbindung der Hauptmenü und Settings, da OneDrive-Ablage nicht synchronisiert hat. Der Charakter kann sich mittlerweile auch bewegen und springen. |
| 22.11.2024  | 0.0.4   | Der Charakter kann jetzt Schaden ausliefern und hat Animationen. Implementierung einer einfachen KI, die sich bewegen kann und Angriffsfunktion für die KI. |
| 29.11.2024  | 0.0.5   | Charakter Auswahl Menu erstellt, neues Powerup implementiert, einfache KI (bewegend, angreifend) entwickelt, Charakter 2 und 3 hinzugefügt.                   |
| 06.12.2024  | 0.0.6   | Entwicklung der Singleplayer-Funktion (Charakterauswahl und Kampf gegen einen Bot), dmgboost und speedboost Powerups, Ingame-Timer, KI verfeinert.              |
| 13.12.2024  | 0.0.7   | Attacken mit verändertem AttackPoint implementiert, Angriffsanzeige verbessert, Multiplayer in Grundfunktion, statsscreen und random boost spawner.             |
| 20.12.2024  | 1.0.0   |    |


## 1 Informieren

### 1.1 Ihr Projekt
Wir wollen mithilfe von Unity eine Art Smash Bros machen, wie es Nintendo schon erstellt hat. 

In diesem Projekt wollen wir ein spannendes Multiplayer-Spiel erschaffen, das ähnlich wie „Super Smash Bros“ funktioniert und den Spielern verschiedene Charaktere sowie Power-Ups für taktische und actiongeladene Kämpfe bietet. Unser Ziel ist ein vollständig spielbares und stabiles Spiel, das sowohl KI-gesteuerte Gegner als auch menschliche Mitspieler unterstützt. Dabei möchten wir unsere Kenntnisse in Unity, C#-Programmierung und Game Design erweitern. Durch die Entwicklung von Netzwerk- und KI-Funktionen erwarten wir zudem, praktische Erfahrungen in diesen anspruchsvollen Bereichen zu sammeln.

### 1.2 User Stories

| US-№ | Verbindlichkeit | Typ          | Beschreibung                                                                                                           |
|------|------------------|--------------|------------------------------------------------------------------------------------------------------------------------|
| 1    | Muss            | Funktional   | Als Spieler möchte ich zwischen verschiedenen Charakteren wählen können, um verschiedene Spielstile zu testen.        |
| 2    | Muss            | Funktional   | Als Spieler möchte ich, dass sich die Charaktere verschiedene Attacken besitzen.        |
|3|Muss|Funktional|Als Spieler möchte ich, dass ich mit meinem Charakter laufen kann, damit ich angreifen kann.|
|4|Muss|Funktional|Als Spieler möchte ich, dass ich mit meinem Charakter springen kann, um Angriffe auszuweichen.|
|5|Muss|Funktional|Als Spieler möchte ich angreifen können, damit ich gewinnen kann.|
|6|Muss|Qualität|Als Spieler möchte ich je nach Eingabe eine Animation haben, damit das Spiel anschaulich aussieht.|
| 7    | Muss            | Funktional   | Als Spieler möchte ich Power-Ups nutzen können, die mir kurzzeitig Vorteile im Spiel bieten.                          |
| 8    | Muss            | Funktional   | Als Spieler möchte ich ein Multiplayer-Spiel spielen können, um gegen andere Spieler anzutreten.                       |
| 9    | Muss            | Funktional   | Als Spieler möchte ich am Ende einer Runde meine Statistiken sehen, um meine Leistung zu analysieren.                  |
|10|Muss|Funktional|Als Spieler möchte ich Menüs haben, wie ein Hauptmenü oder Pausenmenü, um das Spiel zu starten und Einstellungen vorzunehmen.|
| 11    | Muss            | Funktional   | Als Spieler möchte ich gegen KI-gesteuerte Gegner spielen können, wenn keine anderen Spieler verfügbar sind.           |
| 12    | Kann            | Funktional   | Als Spieler möchte ich während des Spiels mit anderen Spielern im Chat kommunizieren können.                           |
| 13   | Muss            | Funktional   | Als Spieler möchte ich eine Auswahl an Power-Ups haben, die das Gameplay abwechslungsreicher machen.                   |
| 14  | Kann            | Funktional   | Als Spieler möchte ich vor Spielbeginn einen Charakter aus mehreren Optionen auswählen können.                         |
| 15   | Muss            | Funktional   | Als Spieler möchte ich am Rundenende meine Statistiken zu Kills, Toden und gesammelten Power-Ups sehen.                |



### 1.3 Testfälle

| TC-№ | Ausgangslage                                   | Eingabe                                       | Erwartete Ausgabe                                                                                                             |
|------|------------------------------------------------|-----------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------|
| 1.1  | Der Charakterauswahlbildschirm wird angezeigt  | Auswahl eines Charakters                      | Der Bildschirm zeigt mehrere Charaktere zur Auswahl und ermöglicht die Auswahl sowohl mit Tastatur als auch mit Gamepad.      |
| 2.1  | Ein Charakter ist ausgewählt                   | Nutzung der Angriffe                          | Jeder Charakter hat verschiedene Angriffe, die korrekt ausgeführt werden.                                                     |
| 2.2  | Ein Charakter ist ausgewählt                   | Zweiten Angriff ausführen                     | Jeder Charakter kann mindestens zwei unterschiedliche Angriffe ausführen.                                                     |
|3.1| Die Runde läuft| A (Damit man nach links läuft) oder D (Damit man nach rechts läuft)|Charakter bewegt sich nach links|
|4.1|Die Runde läuft|Leertaste wird gedrückt|Charakter springt|
|5.1|Die Runde läuft|Die linke Maustaste wird gedrückt|Gegner erhält Schaden|
|6.1|Die Runde läuft|A,D,Leertaste oder Linksklick|Eine Animation wird ausgelöst|
| 7.1  | Eine Runde läuft                               | Ein Power-Up erscheint                        | Der Spieler kann das Power-Up nutzen, und es gewährt einen kurzzeitigen Vorteil.                                              |
| 8.1  | Zwei Spieler sind verbunden                    | Spiel starten                                 | Beide Spieler können dem Spiel beitreten und in Echtzeit interagieren.                                                        |
| 9.1  | Eine Runde ist beendet                         | Anzeigen der Statistiken                      | Die Statistiken (Kills, Tode, gesammelte Power-Ups) des Spielers werden am Rundenende korrekt angezeigt.                      |
|10||||
| 11.1  | Kein anderer Spieler ist verfügbar             | KI-Spieler wird hinzugefügt                   | Die KI bewegt sich und greift den Spieler an.                                                                                 |
| 12.1  | Zwei Spieler sind im Spiel                     | Nutzung des Ingame-Chats                      | Beide Spieler können Nachrichten senden und empfangen.                                                                        |
| 13.1  | Power-Up auf Spielfeld vorhanden               | Power-Up einsammeln                           | Das eingesammelte Power-Up beeinflusst das Gameplay und bringt Abwechslung ins Spiel.                                         |
| 14.1  | Der Charakterauswahlbildschirm wird angezeigt  | Charakter oder Fähigkeit auswählen            | Der Spieler kann einen Charakter oder eine Fähigkeit aus mehreren Optionen auswählen.                                         |
| 15.1 | Eine Runde ist beendet                         | Rundenstatistik anzeigen                      | Statistiken wie Kills, Tode und gesammelte Power-Ups des Spielers werden korrekt aktualisiert und angezeigt.                  |




## 2 Planen

| AP-№ | Frist      | Zuständig | Beschreibung                                                                                      | geplante Zeit |
|------|------------|-----------|--------------------------------------------------------------------------------------------------|---------------|
| 1.A  | 15.11.2024 | Kamil     | Erstellung des Charakterauswahlbildschirms                                                        | 45'           |
| 1.B  | 15.11.2024 | Kamil     | Implementierung der Tastatur- und Gamepad-Unterstützung für Charakterauswahl                      | 45'           |
| 3.A  | 15.11.2024 | Mirhan    | Entwicklung der Bewegung für die Charaktere                                          | 45'           |
| 4.A  | 15.11.2024 | Mirhan    | Entwicklung des Springens                                            | 45'           |
| 5.A  | 15.11.2024 | Mirhan    | Entwicklung der Attacken                                          | 90'           |
|6.A|22.11.2024|Mirhan|Entwicklung von Animationen|90'|
| 7.A  | 15.11.2024 | Kamil     | Design und Implementierung des ersten Power-Ups                                                  | 45'           |
| 7.B  | 15.11.2024 | Kamil     | Design und Implementierung des zweiten Power-Ups                                                 | 45'           |
| 7.C  | 15.11.2024 | Kamil     | Design und Implementierung des dritten Power-Ups                                                 | 45'           |
| 8.A  | 15.11.2024 | Lukas     | Grundstruktur für Multiplayer-Interaktionen                                                      | 45'           |
| 8.B  | 15.11.2024 | Lukas     | Synchronisation zwischen zwei Spielern                                                           | 45'           |
| 8.C  | 15.11.2024 | Lukas     | Testen und Debuggen der Multiplayer-Funktion                                                     | 45'           |
| 8.D  | 22.11.2024 | Lukas     | Einbauen von Host und Join Button / Joinen per Code einbauen anstelle von IP eingeben                                                      | 90'           |
| 8.E  | 22.11.2024 | Lukas     | Multiplayer vereinfachen, ausschalten der Firewall verhindern um zu Joinen                                                | 90'           |
| 9.A  | 29.11.2024 | Kamil     | Anzeige der Kills pro Spieler am Rundenende                                                      | 45'           |
| 9.B  | 29.11.2024 | Kamil     | Anzeige der Tode pro Spieler am Rundenende                                                       | 45'           |
| 9.C  | 29.11.2024 | Kamil     | Anzeige der gesammelten Power-Ups pro Spieler am Rundenende                                      | 45'           |
| 10.A  | 29.11.2024 | Kamil     | Erstellung des Hauptmenüs                                                                        | 45'           |
| 10.B  | 29.11.2024 | Kamil     | Erstellung der Charakterauswahlliste                                                             | 45'           |
| 10.C  | 29.11.2024 | Kamil     | Erstellung des Game Over-Screens                                                                 | 45'           |
| 10.D  | 29.11.2024 | Kamil     | Erstellung des Pausenmenüs                                                                      | 45'           |
| 11.A  | 29.11.2024 | Lukas     | Implementierung einer einfachen KI, die sich bewegen kann                                       | 45'           |
| 11.B  | 29.11.2024 | Lukas     | Implementierung der Angriffsfunktion für die KI                                                  | 45'           |
| 11.C  | 29.11.2024 | Lukas     | Testen und Feinabstimmung der KI                                                                 | 45'           |
| 12.A  | 29.11.2024 | Mirhan    | Implementierung der Grundstruktur für den Ingame-Chat                                           | 45'           |
| 12.B  | 29.11.2024 | Mirhan    | Testen und Debuggen des Ingame-Chats                                                             | 45'           |
|2.A|29.11.2024|Mirhan| Verschiedene Attacken implementieren|90'|
| 13.A  | 29.11.2024 | Kamil     | Erstellung des Power-Up-Spawning-Systems                                                         | 45'           |
| 13.B  | 29.11.2024 | Kamil     | Gestaltung und Positionierung der Power-Ups auf der Karte                                       | 45'           |
| 13.C  | 29.11.2024 | Kamil     | Implementierung von Effekten der Power-Ups auf die Spieler                                       | 45'           |
| 14.A | 29.11.2024 | Kamil     | Anzeigen der aktuellen Kills während des Spiels                                                  | 45'           |
| 14.B | 29.11.2024 | Kamil     | Anzeigen der gesammelten Power-Ups während des Spiels                                            | 45'           |
| 14.C | 29.11.2024 | Kamil     | Aktualisierung der Spielerstatistiken nach jedem Power-Up                                        | 45'           |
| 14.D | 29.11.2024 | Kamil     | Implementierung der Rundenstatistik auf dem Game Over-Screen                                     | 45'           |
| 15.A | 29.11.2024 | Kamil     | Design und Implementierung der Karte                                                             | 45'           |
| 15.B | 29.11.2024 | Kamil     | Hinzufügen von Hindernissen und Plattformen zur Karte                                           | 45'           |
| 15.C | 29.11.2024 | Kamil     | Testen der Karte im Zusammenhang mit Charakterbewegungen                                        | 45'           |
| 15.D | 29.11.2024 | Kamil     | Optimierung und Anpassung der Karte für bessere Spielerfahrung                                  | 45'           |


Total: 36 Arbeitspakete

## 3 Entscheiden
- Anstatt den Charakterauswahlbildschirm zu erstellen, hat Kamil sich entschieden, zuerst das Hauptmenü und das Einstellungsmenü zu erstellen.
- Kamil lässt die Gamepad-Unterstützung vorerst weg, vielleicht wird er es kurz vor dem Ende des Projekts wieder aufnehmen.
- Die User Stories für die Charaktere wurden überarbeitet und in kleinere User Stories aufgeteilt, um sie besser abarbeiten zu können.
- Mirhan hat entschieden, die Charaktere und den Bot von Lukas in Kamils Projekt zu übertragen, um einen Prototypen zu erstellen, statt zwei Arbeitspakete zu bearbeiten.
- Mirhan hat zusätzlich eine Abblinkzeit nach dem Schlagen eingebaut, die je nach Charakter variiert, um den Angriffsausgleich zu verbessern.
- Bei der Angriffsfunktion wurde eine visuelle Anzeige hinzugefügt, um besser zu sehen, wann der Angriff ausgeführt wird.



Neue Arbeitspakete für Lukas:
- Einbauen von Host und Join Button / Joinen per Code einbauen anstelle von IP eingeben                                                     
- Multiplayer vereinfachen, ausschalten der Firewall verhindern um zu Joinen     
## 4 Realisieren

## 5 Kontrollieren

| TC-№ | Datum | Resultat | Tester |
| ---- | ----- | -------- | ------ |
| 1.1  |       |          |        |
| ...  |       |          |        |

✍️ Vergessen Sie nicht, ein Fazit hinzuzufügen, welches das Test-Ergebnis einordnet.

## 6 Auswerten

✍️ Fügen Sie hier eine Verknüpfung zu Ihrem Lern-Bericht ein.
