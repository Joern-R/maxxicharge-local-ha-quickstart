# maxxicharge-local-ha-quickstart
Homeassistant "Backup" als Grundlage einer Integration mit dem Lokalen API der Maxxicharge CCU V1 (ab Firmware 0.41)

**Disclaimer:**

Die Nutzung der bereitgestellten Konfiguration per Homeassistant Backup erfolgt auf eigene Verantwortung und ohne die implizite oder explizite Zusicherung von bestimmten Eigenschaften und Funktionalitäten, sowie ohne Gewähr und Support. 

Die Lösung ist Community basiert und wird von der Firma Maxxisun weder unterstützt noch supported. Alles was hier beschrieben und genutzt wird, sind Homeassistant Technologien und Konzepte sowie Open Source 
Komponenten anderer User, die Homeassistant mittels Home Assistant Community Store (HACS) hinzugefügt werden können. Diese unterliegen den Copyright Regelungen des jeweiligen Repositories.

In der nachfolgenden Beschreibung sind alle im "Backup" verwendenten Komponenten, die einer "leeren" Homeassistant Neuinstallation hinzugefügt werden, aufgeführt. Etwaige, evtl. inkompatibele Änderungen
der Komponenten und daraus folgend notwendige Anpassungen liegen in der Verantwortung des Nutzers. Das gleiche gilt auch für Updates an der Homeassistant Installation.

# Inhalt

Ein "Backup" für Homeassistant Neuinstallationen, dass nach Installation von Homeassistant auf einem geeignenten Geräte folgende Maxxicharge bezogenen Funktionen ohne weitere Konfiguration
im Homeassistant bereitstellt:

1. Integration der Maxxicharge Daten aus dem "Lokalen API" als Sensoren
2. Helfer Entitäten, um die Daten die in Watt (W) gelieferten Daten im HA in Kilowattstunden (kwh) umzuwandeln
3. Die unter 2. erzeugten Helfer Entitäten als Grundkonfiguration des HA Energie Dashboard einrichten
4. Mind. ein HA Dashbaord mit allen Maxxicharge Entitäten basierend auf HA Standard Dashboard Möglichkeiten

# Technische Vorgehensweise

Da Sensoren/Entitäten im HA komplett individuell benannt werden können, gibt es (m.W.n.) derzeit keine Möglichkeit einzelne, spezifische Konfigurationensteile für spezifischen Zwecke
von einem HA-System auf ein anderes HA-System zu übertragen. Stattdessen müssen alle enthaltenen Komponenten (Sensoren, HACS Lovelace Dashboard Komponenten, Configuration.YAML Abschnitte,..) manuell im neuen System 
angelegt werden. Mit Hilfe dieser Komponenten können dann die Dashboards angelegt und konfiguriert werden.

Für jemanden, der neu mit dem HA anfängt stellt dies oftmal eine unerwartet hohe Anfangshürde dar, insbesondere dann, wenn man direkt mit der Konfiguration für ein System wie Maxxicharge starten will.

Die "Backup Funktionalität" im HA (gedacht für Datensicherung und die Übertragung eines komplettes Systems auf andere Hardare), erlaubt es bei einer **Komplette Neuinstallation** des HA Systems eine eine 
Basiskonfiguration (ohne Daten) einzuspielen. Wichtig: Ein Backup überschreibt alle Daten und Konfigurationen, die im jeweiligen HA System gemacht worden sind. Der Ansatz ist somit nur für die Erstkonfiguration 
in einer neu bereitgestellten und noch nicht genutzen HA Instanz geeignet.

**Hinweis:**

Die Konfiguration der Entitäten/Sensoren ist für eine Maxxicharge System mit EINER Batterie ausgelegt. Wer mehr als eine Batterie hat, muss weitere Sensoren für die 2. Batterie in der Konfiguration anlegen,
um die Daten auslesen zu können.

**Warnung:** 

Bei Nutzung des Backup zur Installation von Maxxicharge spezfischer Konfiguration werden **ALLE** bisher evtl. in dem System vorhandenen Konfgurationen sowie **ALLE** evtl. schon vorhandenen Daten gelöscht. 

**Disclaimer:**

Keine Verantwortung für verlorene Daten und evtl. nicht funktionsfähige HA Installation. Das Einspielen der Backups wurde mit mehrenen HA Systemen auf unterschiedlicher Hardware getestet, allerdings
aufgrund der Anzahl von Hardware- und Systemoptionen natürlich nicht auf allen möglichen Varianten. Daher unbedingt ein neues, noch nicht konfiguriertes, leeres HA System nehmen.

# ... und wo ist das jetzt im Detail beschrieben ?

Beschreibung der Vorgehensweise und Details findet sich im Wiki des Repositories: 

https://github.com/Joern-R/maxxicharge-local-ha-quickstart/wiki







