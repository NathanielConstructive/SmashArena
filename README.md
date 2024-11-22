# Projekt-Dokumentation

☝️ Alle Text-Stellen, welche mit einem ✍️ beginnen, können Sie löschen, sobald Sie die entsprechende Stellen ausgefüllt haben.

✍️ Ihr Gruppenname und Ihre Nachnamen

| Datum | Version | Zusammenfassung                                              |
| ----- | ------- | ------------------------------------------------------------ |
|   01.11.2024    | 0.0.1   | Projektbeginn, Informieren und Planen |
|     08.11.2024    | 0.0.2     |      verzögerung wegen Kickoff IDPA,  ànderung von Plan, zuerst Hauptmenu und settings , danach select screen, Hauptscreen erstellt und implementiert.                                                     |
|   15.11.2024      | 0.0.3      |    Settingsmenu erstellt und implementiert, verzögerung mit verbindung der Hauptmenu und settings, da one dirve ablage nicht synchronisiert hat                                                        |
|    22.11.2024     | 0.0.4      |                                                              |
|       | ...     |                                                              |
|       | ...     |                                                              |
|       | ...     |                                                              |
|       | 1.0.0   |                                                              |

## 1 Informieren

### 1.1 Ihr Projekt
Wir wollen mithilfe von Unity eine Art Smash Bros machen, wie es Nintendo schon erstellt hat. 

In diesem Projekt wollen wir ein spannendes Multiplayer-Spiel erschaffen, das ähnlich wie „Super Smash Bros“ funktioniert und den Spielern verschiedene Charaktere sowie Power-Ups für taktische und actiongeladene Kämpfe bietet. Unser Ziel ist ein vollständig spielbares und stabiles Spiel, das sowohl KI-gesteuerte Gegner als auch menschliche Mitspieler unterstützt. Dabei möchten wir unsere Kenntnisse in Unity, C#-Programmierung und Game Design erweitern. Durch die Entwicklung von Netzwerk- und KI-Funktionen erwarten wir zudem, praktische Erfahrungen in diesen anspruchsvollen Bereichen zu sammeln.


### 1.2 User Stories

| US-№ | Verbindlichkeit | Typ          | Beschreibung                                                                                                           |
|------|------------------|--------------|------------------------------------------------------------------------------------------------------------------------|
| 1    | Muss            | Funktional   | Als Spieler möchte ich zwischen verschiedenen Charakteren wählen können, um verschiedene Spielstile zu testen.        |
| 2    | Muss            | Funktional   | Als Spieler möchte ich, dass sich die Charaktere unterschiedlich verhalten und verschiedene Attacken besitzen.        |
| 3    | Muss            | Funktional   | Als Spieler möchte ich Power-Ups nutzen können, die mir kurzzeitig Vorteile im Spiel bieten.                          |
| 4    | Muss            | Funktional   | Als Spieler möchte ich ein Multiplayer-Spiel spielen können, um gegen andere Spieler anzutreten.                       |
| 5    | Muss            | Funktional   | Als Spieler möchte ich am Ende einer Runde meine Statistiken sehen, um meine Leistung zu analysieren.                  |
| 6    | Muss            | Funktional   | Als Spieler möchte ich gegen KI-gesteuerte Gegner spielen können, wenn keine anderen Spieler verfügbar sind.           |
| 7    | Kann            | Funktional   | Als Spieler möchte ich während des Spiels mit anderen Spielern im Chat kommunizieren können.                           |
| 8    | Muss            | Funktional   | Als Spieler möchte ich eine Auswahl an Power-Ups haben, die das Gameplay abwechslungsreicher machen.                   |
| 9   | Kann            | Funktional   | Als Spieler möchte ich vor Spielbeginn einen Charakter aus mehreren Optionen auswählen können.                         |
| 10   | Muss            | Funktional   | Als Spieler möchte ich am Rundenende meine Statistiken zu Kills, Toden und gesammelten Power-Ups sehen.                |



### 1.3 Testfälle

| TC-№ | Ausgangslage                                   | Eingabe                                       | Erwartete Ausgabe                                                                                                             |
|------|------------------------------------------------|-----------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------|
| 1.1  | Der Charakterauswahlbildschirm wird angezeigt  | Auswahl eines Charakters                      | Der Bildschirm zeigt mehrere Charaktere zur Auswahl und ermöglicht die Auswahl sowohl mit Tastatur als auch mit Gamepad.      |
| 2.1  | Ein Charakter ist ausgewählt                   | Nutzung der Angriffe                          | Jeder Charakter hat verschiedene Angriffe, die korrekt ausgeführt werden.                                                     |
| 2.2  | Ein Charakter ist ausgewählt                   | Zweiten Angriff ausführen                     | Jeder Charakter kann mindestens zwei unterschiedliche Angriffe ausführen.                                                     |
| 3.1  | Eine Runde läuft                               | Ein Power-Up erscheint                        | Der Spieler kann das Power-Up nutzen, und es gewährt einen kurzzeitigen Vorteil.                                              |
| 4.1  | Zwei Spieler sind verbunden                    | Spiel starten                                 | Beide Spieler können dem Spiel beitreten und in Echtzeit interagieren.                                                        |
| 5.1  | Eine Runde ist beendet                         | Anzeigen der Statistiken                      | Die Statistiken (Kills, Tode, gesammelte Power-Ups) des Spielers werden am Rundenende korrekt angezeigt.                      |
| 6.1  | Kein anderer Spieler ist verfügbar             | KI-Spieler wird hinzugefügt                   | Die KI bewegt sich und greift den Spieler an.                                                                                 |
| 7.1  | Zwei Spieler sind im Spiel                     | Nutzung des Ingame-Chats                      | Beide Spieler können Nachrichten senden und empfangen.                                                                        |
| 8.1  | Power-Up auf Spielfeld vorhanden               | Power-Up einsammeln                           | Das eingesammelte Power-Up beeinflusst das Gameplay und bringt Abwechslung ins Spiel.                                         |
| 9.1  | Der Charakterauswahlbildschirm wird angezeigt  | Charakter oder Fähigkeit auswählen            | Der Spieler kann einen Charakter oder eine Fähigkeit aus mehreren Optionen auswählen.                                         |
| 10.1 | Eine Runde ist beendet                         | Rundenstatistik anzeigen                      | Statistiken wie Kills, Tode und gesammelte Power-Ups des Spielers werden korrekt aktualisiert und angezeigt.                  |




## 2 Planen

| AP-№ | Frist      | Zuständig | Beschreibung                                                                                      | geplante Zeit |
|------|------------|-----------|--------------------------------------------------------------------------------------------------|---------------|
| 1.A  | 15.11.2024 | Kamil     | Erstellung des Charakterauswahlbildschirms                                                        | 45'           |
| 1.B  | 15.11.2024 | Kamil     | Implementierung der Tastatur- und Gamepad-Unterstützung für Charakterauswahl                      | 45'           |
| 2.A  | 15.11.2024 | Mirhan    | Entwicklung von Charakter 1 mit individuellen Attacken                                           | 45'           |
| 2.B  | 15.11.2024 | Mirhan    | Entwicklung von Charakter 2 mit individuellen Attacken                                           | 45'           |
| 2.C  | 15.11.2024 | Mirhan    | Entwicklung von Charakter 3 mit individuellen Attacken                                           | 45'           |
| 2.D  | 15.11.2024 | Mirhan    | Entwicklung von Charakter 4 mit individuellen Attacken                                           | 45'           |
| 3.A  | 15.11.2024 | Kamil     | Design und Implementierung des ersten Power-Ups                                                  | 45'           |
| 3.B  | 15.11.2024 | Kamil     | Design und Implementierung des zweiten Power-Ups                                                 | 45'           |
| 3.C  | 15.11.2024 | Kamil     | Design und Implementierung des dritten Power-Ups                                                 | 45'           |
| 4.A  | 15.11.2024 | Lukas     | Grundstruktur für Multiplayer-Interaktionen                                                      | 45'           |
| 4.B  | 15.11.2024 | Lukas     | Synchronisation zwischen zwei Spielern                                                           | 45'           |
| 4.C  | 15.11.2024 | Lukas     | Testen und Debuggen der Multiplayer-Funktion                                                     | 45'           |
| 4.D  | 22.11.2024 | Lukas     | Einbauen von Host und Join Button / Joinen per Code einbauen anstelle von IP eingeben                                                      | 90'           |
| 4.E  | 22.11.2024 | Lukas     | Multiplayer vereinfachen, ausschalten der Firewall verhindern um zu Joinen                                                | 90'           |
| 5.A  | 29.11.2024 | Kamil     | Anzeige der Kills pro Spieler am Rundenende                                                      | 45'           |
| 5.B  | 29.11.2024 | Kamil     | Anzeige der Tode pro Spieler am Rundenende                                                       | 45'           |
| 5.C  | 29.11.2024 | Kamil     | Anzeige der gesammelten Power-Ups pro Spieler am Rundenende                                      | 45'           |
| 6.A  | 29.11.2024 | Kamil     | Erstellung des Hauptmenüs                                                                        | 45'           |
| 6.B  | 29.11.2024 | Kamil     | Erstellung der Charakterauswahlliste                                                             | 45'           |
| 6.C  | 29.11.2024 | Kamil     | Erstellung des Game Over-Screens                                                                 | 45'           |
| 6.D  | 29.11.2024 | Kamil     | Erstellung des Pausenmenüs                                                                      | 45'           |
| 7.A  | 29.11.2024 | Lukas     | Implementierung einer einfachen KI, die sich bewegen kann                                       | 45'           |
| 7.B  | 29.11.2024 | Lukas     | Implementierung der Angriffsfunktion für die KI                                                  | 45'           |
| 7.C  | 29.11.2024 | Lukas     | Testen und Feinabstimmung der KI                                                                 | 45'           |
| 8.A  | 29.11.2024 | Mirhan    | Implementierung der Grundstruktur für den Ingame-Chat                                           | 45'           |
| 8.B  | 29.11.2024 | Mirhan    | Testen und Debuggen des Ingame-Chats                                                             | 45'           |
| 9.A  | 29.11.2024 | Kamil     | Erstellung des Power-Up-Spawning-Systems                                                         | 45'           |
| 9.B  | 29.11.2024 | Kamil     | Gestaltung und Positionierung der Power-Ups auf der Karte                                       | 45'           |
| 9.C  | 29.11.2024 | Kamil     | Implementierung von Effekten der Power-Ups auf die Spieler                                       | 45'           |
| 10.A | 29.11.2024 | Kamil     | Anzeigen der aktuellen Kills während des Spiels                                                  | 45'           |
| 10.B | 29.11.2024 | Kamil     | Anzeigen der gesammelten Power-Ups während des Spiels                                            | 45'           |
| 10.C | 29.11.2024 | Kamil     | Aktualisierung der Spielerstatistiken nach jedem Power-Up                                        | 45'           |
| 10.D | 29.11.2024 | Kamil     | Implementierung der Rundenstatistik auf dem Game Over-Screen                                     | 45'           |
| 11.A | 29.11.2024 | Kamil     | Design und Implementierung der Karte                                                             | 45'           |
| 11.B | 29.11.2024 | Kamil     | Hinzufügen von Hindernissen und Plattformen zur Karte                                           | 45'           |
| 11.C | 29.11.2024 | Kamil     | Testen der Karte im Zusammenhang mit Charakterbewegungen                                        | 45'           |
| 11.D | 29.11.2024 | Kamil     | Optimierung und Anpassung der Karte für bessere Spielerfahrung                                  | 45'           |

Total: 36 Arbeitspakete

## 3 Entscheiden
- Anstatt den Charakterauswahlbildschirm zu erstellen, hat Kamil sich entschieden zuerst das Haupt Menü und Einstellungen des Menüs erstellt.
- Kamil lässt die Gamepad-Unterstützung gerade weg, vielleicht wird er es kurz vor dem Ende vom Projekt wieder aufnehmen.  

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
