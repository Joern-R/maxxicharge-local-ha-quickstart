# maxxicharge-local-ha-quickstart
Homeassistant Backup/Image als Grundlage einer Integration mit dem Lokalen API der Maxxicharge CCU V1 (ab Firmware 0.41)

**Disclaimer:**

Die Nutzung der bereitgestellten Konfiguration erfolgt auf eigene Verantwortung und ohne die implizite oder explizite Zusicherung von bestimmten Eigenschaften und Funktionalitäten, sowie ohne Gewähr und Support. 

Die Lösung ist Community basiert und wird von der Firma Maxxisun weder unterstützt noch supported. Alles was hier beschrieben und genutzt wird, sind Homeassistant Technologien und Konzepte sowie Open Source 
Komponenten anderer User, die Homeassistant mittels Home Assistant Community Store (HACS) hinzugefügt werden können. Diese unterliegen den Copyright Regelungen des jeweiligen Repositories.

In der nachfolgenden Beschreibung sind alle im Backup/Image verwendenten Komponenten, die einer "leeren" Homeassistant Neuinstallation hinzugefügt werden aufgeführt. Etwaige, evtl. inkompatibele Änderungen
der Komponenten und daraus folgend notwendige Anpassungen liegen in der Verantwortung des Nutzers. Das gleiche gilt auch für Updates an der Homeassistant Installation.

# Ziel

Ein "Backup/Image" für Homeassistant Neuinstallationen bereitzustellen, dass nach Installation von Homeassistant auf einem geeignenten Geräte folgende Maxxicharge bezogenen Funktionen ohne weitere Konfiguration
im Homeassistant bereitstellt:

1. Integration der Maxxicharge Daten aus dem "Lokalen API" als Sensoren
2. Helfer Entitäten um die Daten die in Watt (W) gelieferten Daten im HA in Kilowattstunden (kwH) aufzusummieren
3. Die unter 2. erzeugten Helfer Entitäten als Grundkonfiguration des HA Energie Dashboard einzustellen
4. Mind. ein HA Dashbaord mit allen Maxxicharge Entitäten basierend auf HA Standard Dashboard Möglichkeiten

# Technische Vorgehensweise

Da Sensoren/Entitäten im HA komplett individuell benannt werden können, gibt es (m.W.n.) derzeit keine Möglichkeit einzelne, spezifische Konfigurationensteile für spezifischen Zwecke
von einenm System auf ein anderes System zu übertragen. Stattdessen müssen alle enthaltenen Komponenten (Sensoren, HACS Lovelace Dashboard Komponenten, Configuration.YAML Abschnitte,..) manuell im neuen System 
angelegt werden und mit Hilfe dieser Komponenten können die Dashboards angelegt und konfiguriert werden.

Für jemanden, der neu mit dem HA anfängt stellt dies oftmal eine unerwartet hohe Anfangshürde dar, insbesondere dann, wenn man direkt mit der Konfiguration für eine System wie Maxxicharge starten will.

Für eine **Komplette Neuinstalltion** des HA gibt es allerdings die Möglichkeit komplette Konfigurationen des System per Backup/Image in HA einzuspielen. Solche Backup's überschreiben alle Daten und Konfigurationen,
die im jeweiligen HA System gemacht worden sind. Der Ansatz ist somit nur für die Erstkonfiguration in einer neu bereitgestellten und noch nicht genutzen HA Instanz geeignet.

**Hinweis:**

Die Konfiguration der Entitäten/Sensoren ist für eine Maxxicharge System mit EINER Batterie ausgelegt. Wer mehr als eine Batterie hat, muss weitere Sensoren für die 2. Batterie in der Konfiguration anlegen,
um die Daten auslesen zu können.

**Warnung:** 

Bei Nutzung des Backup zur Installtion von Maxxicharge spezfischer Konfiguration werden **ALLE** bisher evtl. in dem System vorhandenen Konfgurationen sowie **ALLE** Systemdaten gelöscht. 

**Disclaimer:**

Keine Verantwortung für verlorene Daten und evtl. nicht funktionsfähige HA Installation. Das Einspielen der Backups wurde mit mehrenen HA Systemen auf unterschiedlicher Hardware getestet, allerdings
aufgrund der Anzahl von Hardware- und Systemoptionen natürlich nicht auf allen möglichen Varianten. Daher unbedingt ein neues, noch nicht konfiguriertes, leeres System nehmen.

# ... und wo ist das jetzt im Detail beschrieben ?

Beschreibung der Vorgehensweise und Details findet sich im Wiki des Repositories: 

https://github.com/Joern-R/maxxicharge-local-ha-quickstart/wiki







