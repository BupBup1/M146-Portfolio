
# 1. M146 - Portfolio
<img src="internetanbindung.png" alt="Alt-Text" title="" />
 
## Sicherheit
### ISO Reihe 27000
Die ISO Reihe 27000 gibt einen allgemeinen Überblick über die informations-Sicherheit der Mgmt Systeme. Hier befinden die grundlegende Prinzipien, Konzepte, Begriffe und Definitionen für ISMS (Information Security Management System).

Bei der Sicherheit wird die Frage nach der Verfügbarkeit gestellt. Systeme und Rechenzentren können mit verschiedenste attacken angegriffen werden wie durch einen Denial of Service (DDOS) Attack. Die ISO 27000 beschäftigt sich genau in diesem Fachbereich. Jedoch sollte man vor Beginn des Aufbaus eines Hoch Redundantes System eine Checkliste durchführen. Anhand dieser Checkliste kann genau ermitteln, wo und welches System mit welcher Priorität eingestuft werden muss.

<img src="Bild3.png" alt="Alt-Text" title="" /> <br>
Anhand dieser Grafik kann man seine Systeme einstufen. Hier werden zum Beispiel Finanzdienstleister ganz oben links bei der Kurve eingestuft und kleine Coiffeur Betriebe ganz unten Recht in der Kurve. 

### Vertraulichkeit
Bei der Vertraulichkeit geht es um den Schutz von sensiblen Daten im Betrieb. Dies werden meisten mit “Public”, “Internal”, “Confidential” und “Secret vermerkt” Public sind diese Daten, die jeder im Netz sehen darf, also diese die schon Zum Beispiel auf einer Website zu sehen sind. Internal sind Daten, die nur Mitarbeiter vom selben Betrieb sehen dürfen. Dies können Dokumentationen, Anleitungen oder auch Kundenaccounts. Confidential sind dann schon sehr strenge Dokumenten wie Offerten, die auf keinen Fall bei der Öffentlichkeit bekannt sein dürfen. Secret Dokumente sollen sehr Geheim und in einem sehr kleinen Radius verteilt werden. Diese sind dann Geschäftskritische Daten wie Rezepte oder Bilanzen. 

### Integrität
Bei der Integrität geht es darum, wer auf welche Daten oder System Zugriffe haben sollte. Zum Beispiel dürfen Personen aus dem Kaufmännischen Bereich kein Zugriff auf Administratoren Konten oder gar auf Jumpservers haben. So könnten diese Zugriffe missbraucht werden und dies könnte dem Betrieb viel Geld und Zeit kosten. Deswegen soll man sich immer zuerst die Fragen stellen wenn es um den Zusammenhang mit den Internetanbindungen von Firmen geht:

* Wie viele Mitarbeiter müssen darauf Zugriff haben? <br>
* Arbeiten auch Externe Personen damit? <br>
* Welche Zugriffe haben Externe (VPN)?

### Authentizität und Authentisierung
Netzwerkfähige Geräte sollten immer mit starken Passwörtern gesichert sein. Es muss immer klar sein, wer und wieso hat jemand Zugriffe auf solche Systeme oder Geräten. Zudem muss man sich bei der Authentisierung diese Frage überlegen:

* Welches Verfahren soll zum Einsatz kommen? 1,2 oder 3 Stufiges Konzept?
* Sind Biometrische Daten auch erwünscht? (BSP: Physische Datacenter Zugriff) <br>

### Zurechenbarkeit:
Dateien, Mails und Briefe sollen immer einem Owner gewährleistet sein. So können bei Fragen und unklarheiten dieser Owner angefragt werden. Dieser Owner ist auch für die Annahme oder ABlehnung von Berechtigungen auf seine Dateien zuständig. Mails sollen zudem auch immer signiert werden. 

### Nicht-Abstreitbarkeit
Dieses Sicherheitsanforderung gilt an Web-Shops. Aus Sicht der Internetanbindungen soll man sich fragen, ob ein Webshop im Einsatz ist und ob Bestellungen via Mail oder via des WEB erfolgen. Dies muss man dokumentieren. 
### Verlässlichkeit
Die Verlässlichkeit spielt eine grosse Rolle mit der Wartung der Internetzugänge. Daher müssen folgende Fragen gestellt werden:

* Wie ist die Wartung organisiert?
* Sind die Systeme zuverlässig gewartet?
* Werden Backups gemacht?
* Werden Patches regelmässig eingespielt?
* Ist PKI (Public key Infrastructure) im Einsatz?
* Werden die Vulnerabilitäts Datenbanken regelmässig konsultiert?
* Werden ihre Firewalls intern oder extern gemanaged?
* Ist der BSI Grundschutz implementiert?

### Zugriffskontrolle
Bei der zugriffskontrolle geht es nicht nur um physische Berechtigung sondern auch um das surfen im Internet. Auf welche Dienste und Webseiten sollen die Mitarbeiter der Firmen zugriff haben und wie lange? Diese Regeln müssen dann überwacht und überprüft werden. 
Zudem soll man jeden Dienst und Ort und die Zugriffsart gut dokumentieren. 
 
## Sicherheitskonzept
### Technische Massnahmen
* Servers müssen durch einen USV Stromzufuhr betrieben werden. 
* Physischer Zugriff für in den DC muss über Biometrisches Verfahren gehen.
* Internetleitungen müssen Redundant sein.
* Auf Netzwerkfähige Geräte im Serverraum wie Router und Switches, muss ein sicheres admin Passwort gesetzt werden.
* Router muss Redundant sein
* Bei den Servern müssen sichere BIOS und Admin Passwörter gesetzt werden. 
* Webserver sollen in einem DMZ stehen und über einen Jump Server erreichbar sein.
* Wenn Externe Mitarbeiter auf den Servers oder Datenbanken zugriff haben sollen, muss ein sicherer VPN eingesetzt werden
* Differentials Backup müssen Täglich vom System gemacht werden.
 
### Nicht Technische Massnahmen
* Abgeschlossener Bereich für den Serverraum
* Offene Switches müssen in einem Kasten / Schrank abgeschlossen werden
* Vendor Escalation für wichtige Systeme / Server müssen genau dokumentiert werden
* Pikett Dienst muss durchgeführt und dokumentiert werden.
* Bei jeder Berechtigungsart muss ein Owner definiert und dokumentiert werden.
* Genaue Dokumentation über zugriffskontrollen auf den Servern müssen laufend gemacht werden.

Sicherheitskonzept nach ISO 27000 für unser Beispiel:
1. Vertraulichkeit: Die Daten auf der Website können als "Public" gekennzeichnet werden. Daten für Mitarbeiter wie z.B. Anleitungen und Dokumentation werden als Confidential markiert. Offerten können in die Kategorie Confidential und streng geheime Dokumente der Geschäftsleitung können als Secret vermerkt werden.
2. Integrität: Bei dem Punkt Integrität muss nur definiert werden, welcher Mitarbeiter auf welche Daten Zugriff hat. Da es keine externe Mitarbeiter gibt, kann das einfacher definiert werden.
3. Authentizität und Authentisierung: Dabei ist wichtig, dass überall sichere Passwörter verwendet werden. Für die Mitarbeiter eine Richtlinie hinzugefügt werden, damit Mitarbeiter sichere Passwörter wählen müssen.
4. Zurechenbarkeit: Hierbei müssen alle 90 Mitarbeiter mit einem persönlichen Account Arbeiten, um nachvollziehen zu können, welcher User was gemacht hat. E-Mails sollte zudem immer signiert werden.
5. Nicht-Abstreitbarkeit: Beim Webshop müsste definiert werden, ob die Bestellungen via Mail oder via Web hereinkommen sollen. 
6. Verlässlichkeit: Da die Server alle inhouse sind, müssen da natürlich die Wartungen organisiert werden, die Backups in regelmässigen Abständen gemacht werden, Datenbanken regelmässig konsulieren und Patches regelmässig eingespielt werden.
7. Zugriffskontrolle: Da alle Mitarbeiter intensiv mit dem Internet arbeiten ist es wichtig, dass diese nur auf bestimmte Websiten Zugriff haben. Diese Zugriffe müssen im Voraus definiert werden und durch Programme sollten dann die verbotenen Websiten gesperrt werden.

Wenn alle 7 Punkte eingehalten werden wird das Sicherheitskonzept nach ISO 27000 eingehalten und das Unternehmen ist Online geschützt unterwegs.