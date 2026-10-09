# Rekonstruktion – 9. Oktober 2026

## Umfang und Grenzen

- 23 unterschiedliche Drive-Dateien anhand der im ZIP gespeicherten IDs abgerufen.
- 17 inhaltliche Dokumente als Markdown, drei Bankentabellen als CSV, die Git-Attribute als Text und zwei leere Quellen wiederhergestellt.
- Die ursprüngliche Übergabe zusätzlich als Markdown kopiert.
- Inhaltssprache, Tabellen, Entscheidungen, bestehende Widersprüche und Archivstatus erhalten. UTF-8/LF vereinheitlicht, führende BOM und überzählige Leerzeilen normalisiert.
- Alle Google-Tabellen hatten ein Blatt. Die vollen Blattbereiche wurden als native Werte/Formeln gelesen; keine Formeln in den gelesenen Bankendaten gefunden. CSV enthält nur die tatsächlichen Quellspalten, nicht die künstliche Zeilenindexspalte der ersten Textansicht.
- Ursprüngliche Google-Formatierung, Kommentare, Smart Chips, Freigaben und Versionshistorie werden nicht rekonstruiert. PDF-benannte Dokumente liegen als extrahierter Markdown-Text vor; ursprüngliches PDF-Layout wird nicht vorgetäuscht.
- `metadata.json` und der Verbindungstest hatten keinen Inhalt. Die leeren Dateien werden ausdrücklich bewahrt. Die Metadaten sind damit nicht gültig oder lauffähig.
- .DS_Store, __MACOSX-Ressourcen und alte .gdoc/.gsheet-Verweise sind kein Bestandteil des Arbeitsordners.
- Die alte .git-Historie besteht aus einem Initial Commit mit Verweisdateien. Sie bleibt im Original-ZIP erhalten und wird nicht als brauchbare Entwicklungshistorie des neuen Arbeitsbestands ausgegeben.
- Original-ZIP, Desktop-Dateien, Drive-Originale und synchronisierte Projektdateien blieben unverändert.
- Der neue Ordner ist eine Arbeitskopie, keine automatische Drive-Synchronisierung.

## Nachweis je Quelldatei

| Arbeitsdatei | Quelle | Ergebnis |
|---|---|---|
| [docs/design/politics_and_government_foundations.md](../docs/design/politics_and_government_foundations.md) | [EU5 Modern World Mod – Politics and Government Foundations](https://drive.google.com/file/d/1o9izY2yPIgmulK6PSIq5gZtBMKaiEZqsOLyi9p2TCLk/view) | Inhalt wiederhergestellt |
| [docs/data/banks/final_bank_list.csv](../docs/data/banks/final_bank_list.csv) | [final_bank_list](https://drive.google.com/file/d/1c4Ro-BKV75rU6QInbtFr3FqYYamsw6Oq14b0CZ53Sl4/view) | Inhalt wiederhergestellt |
| [docs/design/economic_system_foundations.md](../docs/design/economic_system_foundations.md) | [EU5 Modern World Mod – Economic System Foundations](https://drive.google.com/file/d/1B1Naq8fP5LXvboIPLIUscvWlOPbjsK3bEjcHajfR2M4/view) | Inhalt wiederhergestellt |
| [docs/data/banks/worldwide_bank_candidates.csv](../docs/data/banks/worldwide_bank_candidates.csv) | [Banken-Entitäten – weltweite Kandidatenliste](https://drive.google.com/file/d/1C482i_fexoHUSe-C_-ez7tjpp13xiJvb8M74MDmCjg8/view) | Inhalt wiederhergestellt |
| [docs/archive/test_ob_connect_laeuft.md](../docs/archive/test_ob_connect_laeuft.md) | [test ob connect läuft](https://drive.google.com/file/d/1_-BI1NKBuuG4bN7hUezRR4P5W5YwtRjgRJ42bbVYnIw/view) | Quelle leer |
| [docs/research/Europa_Universalis_V_Modding_Paper.md](../docs/research/Europa_Universalis_V_Modding_Paper.md) | [Europa_Universalis_V_Modding_Paper.pdf](https://drive.google.com/file/d/1hohJ-AkQw77ajADGuyeU1_7QqXYZQBB3V2vqn18xuiU/view) | Inhalt wiederhergestellt |
| [docs/data/banks/final_bank_list_alternative_135.csv](../docs/data/banks/final_bank_list_alternative_135.csv) | [final_bank_list](https://drive.google.com/file/d/1opQy4ERSxacyJhIS198tdnA17A0k6tzrnFsuXacT_8I/view) | Inhalt wiederhergestellt |
| [.gitattributes](../.gitattributes) | [.gitattributes](https://drive.google.com/file/d/1dwHnuYl4woa8_X0YeQtsZl1fxoaeYcxjD9UQ6-w8zuI/view) | Inhalt wiederhergestellt |
| [docs/design/design_bible.md](../docs/design/design_bible.md) | [EU5 Modern World Mod — Design Bible](https://drive.google.com/file/d/1HSQml6yVFalANsq73JMugyvq4OO_sId5Rvy8ipTn_ec/view) | Inhalt wiederhergestellt |
| [docs/design/global_entity_registry.md](../docs/design/global_entity_registry.md) | [global_entity_registry.md](https://drive.google.com/file/d/1OrZlleWq934rmDakZWk1errdFjkmp3YKG0d9ddo5RCE/view) | Inhalt wiederhergestellt |
| [docs/archive/global_entity_registry_framework_pre_migration.md](../docs/archive/global_entity_registry_framework_pre_migration.md) | [ARCHIVED — global_entity_registry_framework_pre_migration.md](https://drive.google.com/file/d/1iHPMXWL6UA6fqlgMRVYhriah6Ii2rn9pCsz798O-2Yc/view) | Inhalt wiederhergestellt |
| [docs/design/world_entity_framework.md](../docs/design/world_entity_framework.md) | [world_entity_framework.md](https://drive.google.com/file/d/1hhw87qYV93nxR7Mw_dsaszn5bpsS20xC5Mf-Ge6OpMs/view) | Inhalt wiederhergestellt |
| [docs/country_design/south_asia_1993_country_list.md](../docs/country_design/south_asia_1993_country_list.md) | [south_asia_1993_country_list.md](https://drive.google.com/file/d/15qLHKBwFIQSm4x-ig1SYhHV-oxh6qsULl6KZlOwWkxU/view) | Inhalt wiederhergestellt |
| [docs/country_design/middle_east_north_africa_1993_country_list.md](../docs/country_design/middle_east_north_africa_1993_country_list.md) | [middle_east_north_africa_1993_country_list.md](https://drive.google.com/file/d/1xWimccisJSlHAFsLPn_Pf34NNRFPDxK-CLuO4tT2Nl0/view) | Inhalt wiederhergestellt |
| [docs/country_design/north_america_1993_country_list.md](../docs/country_design/north_america_1993_country_list.md) | [north_america_1993_country_list.md](https://drive.google.com/file/d/1XFQZ4bv-inx1t3UeJOVShZ8fdJ59dfKUuqfkOanatUE/view) | Inhalt wiederhergestellt |
| [docs/country_design/east_southeast_asia_oceania_1993_country_list.md](../docs/country_design/east_southeast_asia_oceania_1993_country_list.md) | [east_southeast_asia_oceania_1993_country_list.md](https://drive.google.com/file/d/1e5VqMeIpVOFkBdZaoZJaSdpnFxJDfT2TrBJGiYocNE4/view) | Inhalt wiederhergestellt |
| [docs/country_design/europe_fsu_1993_country_list.md](../docs/country_design/europe_fsu_1993_country_list.md) | [europe_fsu_1993_country_list.md](https://drive.google.com/file/d/1aT8ZMfFykfvWiEHgGFZEjZJOrdlHyWmEF87U7AckHeU/view) | Inhalt wiederhergestellt |
| [docs/country_design/country_content_design_backlog.md](../docs/country_design/country_content_design_backlog.md) | [country_content_design_backlog.md](https://drive.google.com/file/d/1MwwoOINKBGhxo9jDztBHw31HJN8HzOb5EY7h1e0SVT8/view) | Inhalt wiederhergestellt |
| [docs/country_design/world_1993_country_list_index.md](../docs/country_design/world_1993_country_list_index.md) | [world_1993_country_list_index.md](https://drive.google.com/file/d/1pDwFI01q3K9ZdB6KtAiVyKCn54LWpMNMSJYgOdHtPBw/view) | Inhalt wiederhergestellt |
| [docs/country_design/sub_saharan_africa_1993_country_list.md](../docs/country_design/sub_saharan_africa_1993_country_list.md) | [sub_saharan_africa_1993_country_list.md](https://drive.google.com/file/d/1HnMe0txHIW0epbBcemEDzMUbRLctOxTPLpP4G8n-Txs/view) | Inhalt wiederhergestellt |
| [docs/country_design/latin_america_caribbean_1993_country_list.md](../docs/country_design/latin_america_caribbean_1993_country_list.md) | [latin_america_caribbean_1993_country_list.md](https://drive.google.com/file/d/1BzY5gTKLaghyjsY4rxWTjbT2PQdQ_kNCtKRMrvbuauQ/view) | Inhalt wiederhergestellt |
| [mod/.metadata/metadata.json](../mod/.metadata/metadata.json) | [metadata.json](https://drive.google.com/file/d/1uFrL0CAwC1bNHijDv7IEKVCCODlXsliRDAwBykV6MN4/view) | Quelle leer |
| [docs/research/future/space_exploration_roi_report.md](../docs/research/future/space_exploration_roi_report.md) | [space_exploration_roi_report.pdf](https://drive.google.com/file/d/12e02n_gL5STzLzBAKkeQSQf6KLjDRhgsr-zsYFpbtns/view) | Inhalt wiederhergestellt |

Die maschinenlesbare Zuordnung und Prüfsummen stehen in `reconstruction_manifest.json`. Die ältere Übergabe ist separat archiviert; ihr unvollständiger Entwicklungsstand wird durch die aktuelle Bestandsaufnahme ergänzt.

