# Projektstand – 9. Oktober 2026

## Ergebnis der Bestandsaufnahme

Die EU5 Modern World Mod befindet sich in einer umfangreichen Designphase. Der Stand ist deutlich weiter als in der unvollständigen Übergabe beschrieben. Eine spielbare Implementierung lässt sich aus den gelieferten Dateien nicht belegen.

Das ZIP enthält Google-Verweise statt der eigentlichen Texte. Alle 23 unterschiedlichen verlinkten Dateien konnten gelesen werden. Die drei Bankentabellen wurden zusätzlich über ihre vollständigen nativen Blattbereiche geprüft. Die erreichbaren Inhalte sind im neuen Arbeitsordner als Markdown bzw. CSV rekonstruiert. Zwei Quellen waren leer: der Verbindungstest und `metadata.json`.

Die jüngste gemeldete Änderung der eingelesenen Fachunterlagen ist vom 25. Juli 2026 und betrifft die Wirtschaftsgrundlagen. Das Abrufdatum 9. Oktober 2026 bedeutet nicht, dass die Konzepte an diesem Tag überarbeitet wurden.

## Dokumentierter Entwurf

- Total Conversion für Europa Universalis V.
- Kampagnenbeginn: **1. Januar 1993**, bezogen auf den Tagesbeginn.
- Kein festes historisches Enddatum und kein verbindlicher abschließender Inhaltshorizont.
- Historisch gerichtete Sandbox: Entwicklungen werden erwartet, dürfen bei veränderten Ursachen anders verlaufen oder ausbleiben.
- Der Spieler verkörpert den Staat und bleibt normalerweise durch Wahlen, Regierungswechsel, Putsche und Revolutionen beim selben Staat.
- EU5-Systeme werden möglichst erhalten, modern interpretiert und angepasst.
- Die bisherigen Unterlagen sehen vollständiges Design und einen Design Freeze vor der Implementierung vor. Das ist dokumentierter Projektkontext, kein im Rahmen der Rekonstruktion neu eingeführter Auftrag.
- Version 0.1 ist als erste spielbare Grundlage mit besonderem Fokus auf Europa und die frühere Sowjetunion vorgesehen.

Quelle: [Design Bible](design/design_bible.md).

## Bereits geleistete Arbeit

### Welt und Länder

Sieben regionale Länderlisten, ein World Entity Framework und das aktive Global Entity Registry liegen vor. Die registrierten Designentscheidungen trennen Anerkennung, rechtliche Souveränität, tatsächliche Kontrolle, Verwaltungsstatus und Spielbarkeit.

Die tatsächlichen Tabellenzeilen wurden nachgezählt:

| Prüfung | Ergebnis |
|---|---:|
| Eindeutige Registereinträge | 349 |
| Am Start spielbare Länderakteure | 202 |
| Übrige politische/territoriale Einträge | 147 |
| LOCKED | 329 |
| Als separate Entität REJECTED | 20 |
| PROVISIONAL / DEFERRED / OPEN | 0 |
| Doppelte Design-IDs | 0 |
| Doppelte zugewiesene technische Kennungen | 0 |

Das ist eine Prüfung der vorhandenen Tabelle, keine vollständige historische Verifikation jedes Eintrags und keine Engine-Prüfung der Kennungen. `LOCKED` beschreibt Designentscheidungen. Es bedeutet nicht, dass die jeweiligen Länder oder Systeme implementiert sind.

Abhängige Akteure verwenden im Entwurf teilweise den EU5-Vassal als vorläufige Darstellung. Die spätere moderne Behandlung ist noch offen. Internationale Organisationen und Banken sind ausdrücklich außerhalb des 349er-Registers vorgesehen.

Quellen: [aktives Register](design/global_entity_registry.md), [Länderindex](country_design/world_1993_country_list_index.md).

### Politik und Regierung

Die fünf technischen EU5-Regierungstypen bleiben im Entwurf erhalten. Ihre modernen Interpretationen sind Monarchie, republikanisch basierte Systeme, Theokratie, Clan-/Stammesstaat und Warlord-Regime.

Acht grundlegende Regierungsstruktur-Reformen sind vorgesehen: parlamentarisches, präsidentielles, semipräsidentielles, monarchisches, kollegiales, klerikales und tribales System sowie Warlord-Regime. Die acht ergänzenden Designkategorien sind keine neu erfundenen technischen Reformstufen.

Noch offen sind konkrete Voraussetzungen, Wirkungen, Ausschlüsse, Übergänge, Wahlen, Parteien, Gesetze und länderspezifische Zuordnungen. Auch dynamische Ressourcenbezeichnungen sind ein Designziel, keine hier technisch bestätigte Umsetzung.

Quelle: [Politikgrundlagen](design/politics_and_government_foundations.md).

### Wirtschaft – jüngster dokumentierter Arbeitsstand

- Geldskalierung: **1 Gold = 500 reale US-Dollar auf 2026-Dollar-Basis**.
- Reservenkonzept: ein Gold-Cap-Stapel repräsentiert **90.000.000 Gold**.
- Flüssige Reserven, gespeicherte Reserven, Vermögen und Schulden werden getrennt.
- Arbeitsliste mit 75 Rohstoffen: laut Konzept 52 Vanilla-Rohstoffe plus 23 moderne Ergänzungen. Die Vanilla-Zahl ist dort auf EU5 1.2.1 bezogen und wurde hier nicht gegen eine installierte Version geprüft.
- Acht Ergänzungen sind als genehmigt markiert: Schwefel, Platingruppenmetalle, Titanminerale, Wolfram, Molybdän, Graphit, Flussspat und Sammelkategorie Specialty Ores.
- Weitere 15 Ergänzungen bleiben Kandidaten.
- Stahl und Aluminium sind als produzierte Güter genehmigt; grundlegende Produktionsketten sind notiert.
- Qualitäts- und Technologieunterschiede sollen bevorzugt über Produktionsmethoden statt über zusätzliche Warenvarianten abgebildet werden.

Der letzte Abschnitt endet mit Stahl und Aluminium. Das Dokument enthält zugleich noch die ältere Aussage, die Arbeit beginne bei der Rohstoffliste. Der genaue letzte Gesprächsschritt ist deshalb nicht rekonstruierbar; die beiden genehmigten verarbeiteten Güter sind aber ausdrücklich vorhanden.

Das Gold-Cap-Konzept setzt noch ungeprüfte Engine-Eigenschaften voraus. Schatzkammergrenze, Stapelung, Werterhaltung, Einlösung, KI, Speichern/Laden und große Transaktionen müssen EU5-spezifisch geprüft werden.

Quelle: [Wirtschaftsgrundlagen](design/economic_system_foundations.md).

### Banken, Länderinhalte und Forschung

Die Bankentabellen enthalten eine Kandidatenliste mit 372 belegten Einträgen sowie zwei unterschiedliche Final-Fassungen mit 100 bzw. 135 Einträgen. Welche Final-Fassung verbindlich sein soll, ist nicht eindeutig dokumentiert. Eine historische Prüfung auf den Starttermin ist erforderlich.

Ein umfangreicher Country Content Design Backlog sammelt noch zu entwerfende Konflikte, Übergänge und besondere Ländermechaniken. Die Klassifikation dieser Akteure kann abgeschlossen sein, während ihr konkreter Inhalt weiterhin offen ist.

Das Modding-Paper ist ältere zusammenfassende Recherche und keine technische Ersatzautorität für die EU5-Dokumentation. Der Weltraum-ROI-Bericht ist Hintergrundmaterial für mögliche Zukunftsinhalte, keine beschlossene Implementierung oder ein festes Kampagnenende.

## Technischer und organisatorischer Abgleich

1. Die alte Design Bible enthält ein generisches Mod-Ordnerbeispiel mit `common/history/events/map` direkt unter `mod`. Es wird nicht als geprüfte EU5-Struktur übernommen. Das vorhandene Gerüst mit `in_game`, `main_menu`, `loading_screen` und `.metadata` ist separat erhalten.
2. Konkrete Syntax, Ladeverhalten und Scopes werden ausschließlich anhand EU5-spezifischer Dokumentation und der verwendeten Spielversion entschieden. Keine Übertragung aus Victoria 3, Stellaris, CK3 oder anderen Spielen.
3. EU5-Dokumentation zu [Laws](https://eu5.paradoxwikis.com/Law_modding), [Advances](https://eu5.paradoxwikis.com/Advance_modding) und [Modifiers](https://eu5.paradoxwikis.com/Modifier_modding) konnte über die Web-Recherche eingesehen werden. Mehrere direkte Wiki-Aufrufe, darunter Mod Structure, wurden mit 401 abgewiesen. Eine vollständige aktuelle technische Prüfung ist daher nicht abgeschlossen.
4. Ältere Listen enthalten doppelte Dokumentblöcke, veraltete Empfehlungen und teilweise noch vorläufige Kennungen. Diese wurden bei der Textrekonstruktion nicht stillschweigend gelöscht oder als neue Entscheidungen ausgewertet.
5. Die lokale Dateirekonstruktion ist abgeschlossen. Die ursprüngliche Drive-Synchronisierung ist dadurch nicht repariert und der lokale neue Ordner ist nicht automatisch mit Drive verbunden.

## Empfohlene nächste Schritte

1. Mit dem rekonstruierten VS-Code-Workspace weiterarbeiten; die echte lokale Markdown-/CSV-Fassung als Arbeitsbestand verwenden.
2. Im jüngsten Wirtschaftskonzept die noch offenen Rohstoffentscheidungen klären und anschließend die Liste verarbeiteter Güter ab Stahl/Aluminium fortsetzen. Danach Produktionsketten und Gebäude konkretisieren.
3. Politikgrundlagen durch konkrete Regierungsstruktur-Reformen, Gesetze und Übergänge ergänzen.
4. Ein getrenntes institutionelles Register für Organisationen, Bündnisse und Banken entwerfen; zuerst die verbindliche Bankenfassung und deren zeitliche Gültigkeit klären.
5. Ältere Übersichten mit den neueren Fachkonzepten abgleichen, ohne dokumentierte Entscheidungen eigenmächtig zu ändern.
6. Vor Implementierung die Designanforderungen gegen die konkrete EU5-Version prüfen. Danach den vorgesehenen Design Freeze und die erste spielbare Version vorbereiten.

Diese Reihenfolge ist eine Empfehlung aus dem Dateistand, keine neu festgelegte Projektentscheidung.

