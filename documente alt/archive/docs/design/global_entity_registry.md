# Global Entity Registry

**Project:** EU5 Modern World Mod  
**Authoritative date:** 1 January 1993  
**Status:** Full 349-entry political and territorial registry migrated and owner-reviewed  
**Implementation status:** Design only  

## Import and Review Summary

- Source roster rows normalized: **357**
- Unique registry entries: **349**
- Starting country actors: **202**
- Non-country political, territorial, regional, movement, and background entries: **147**
- `LOCKED`: **329**
- `REJECTED` as separate entities: **20**
- `PROVISIONAL`: **0**
- `DEFERRED`: **0**
- `OPEN`: **0**
- International banks, trade organizations, military alliances, and other institutional organizations included in this registry: **0**

This registry covers countries, dependencies, territorial statuses, internal regions, disputed territories, political movements, armed factions, exile organizations, and background entities. International organizations and financial or trade institutions will be designed in a separate institutional registry.

## Classification Codes

- Recognition: `R1` fully recognized state; `R2` partially recognized state; `R3` unrecognized or transitional de facto state; `R4` claimed/exile government; `R5` non-sovereign entity; `R6` non-state actor.
- Control: `C1` full; `C2` partial; `C3` contested; `C4` external occupation or lease; `C5` none; `C6` mobile/irregular.
- Administration: `A1` national territory; `A2` federal constituent; `A3` autonomous; `A4` dependency; `A5` associated state; `A6` international administration; `A7` occupied/leased; `A8` disputed/strategic; `A9` separatist territory; `A10` no formal territorial status.
- Gameplay: `G1` sovereign country actor; `G2` dependent country actor; `G3` internal/releasable regional actor; `G4` de facto country actor; `G5` civil-war faction; `G7` separatist movement; `G8` political movement; `G9` territorial status; `G10` international administration; `G11` event/modifier; `G12` background only.

## Locked Cross-Registry Policies

1. All recognized sovereign states and sovereign microstates are country actors.
2. Non-sovereign island dependencies are represented directly within their administering state unless an explicit locked exception applies.
3. Locked island exceptions are the Faroe Islands, Greenland, Hong Kong, Macau, and American Samoa as standard EU5 Vassals. Palau remains a transitional international administration until its 1994 independence path.
4. The State of Palestine is a separate starting country actor. The West Bank and Gaza Strip remain separate occupied-territory records, and the PLO is internal Palestinian political content.
5. East Timor is internal Indonesian occupied/disputed regional content at campaign start. Fretilin is internal Indonesian resistance content. Neither receives a separate starting country actor or technical identifier.
6. Guantánamo Bay remains legally Cuban territory under effective United States control pursuant to the lease arrangement.
7. Legal sovereignty, recognition, effective control, claims, gameplay representation, and player availability remain separate fields.
8. Detailed country-content follow-up belongs only in `country_content_design_backlog.md`.

## Normalized Entries

### Europe (`EUR`)

| Design ID | Entity | Category | R | C | A | G | Legal sovereign / parent | Effective controller | Exists | Player | Eligibility | Decision | Tech ID |
|---|---|---|:---:|:---:|:---:|:---:|---|---|:---:|---|---|---|---|
| ENT_EUR_ALBANIA | Albania | Recognized sovereign state | R1 | C1 | A1 | G1 | Albania | Albania | YES | START_PLAYABLE | AUTOMATIC | LOCKED | ALB |
| ENT_EUR_ANDORRA | Andorra | Recognized sovereign state | R1 | C1 | A1 | G1 | Andorra | Andorra | YES | START_PLAYABLE | AUTOMATIC | LOCKED | AND |
| ENT_EUR_AUSTRIA | Austria | Recognized sovereign state | R1 | C1 | A1 | G1 | Austria | Austria | YES | START_PLAYABLE | AUTOMATIC | LOCKED | AUS |
| ENT_EUR_BELGIUM | Belgium | Recognized sovereign state | R1 | C1 | A1 | G1 | Belgium | Belgium | YES | START_PLAYABLE | AUTOMATIC | LOCKED | BEL |
| ENT_EUR_BOSNIA_AND_HERZEGOVINA | Bosnia and Herzegovina | Recognized sovereign state | R1 | C1 | A1 | G1 | Bosnia and Herzegovina | Bosnia and Herzegovina | YES | START_PLAYABLE | AUTOMATIC | LOCKED | BOS |
| ENT_EUR_BULGARIA | Bulgaria | Recognized sovereign state | R1 | C1 | A1 | G1 | Bulgaria | Bulgaria | YES | START_PLAYABLE | AUTOMATIC | LOCKED | BUL |
| ENT_EUR_CROATIA | Croatia | Recognized sovereign state | R1 | C1 | A1 | G1 | Croatia | Croatia | YES | START_PLAYABLE | AUTOMATIC | LOCKED | CRO |
| ENT_EUR_CROATIAN_REPUBLIC_OF_HERZEG_BOSNIA | Croatian Republic of Herzeg-Bosnia | Internal separatist or autonomous administration | R5 | C3 | A3/A9 | G11 | Bosnia and Herzegovina | Bosnia and Herzegovina | YES | SIMULATED_NOT_PLAYABLE | DOES_NOT_QUALIFY | REJECTED | UNASSIGNED |
| ENT_EUR_CYPRUS | Cyprus | Recognized sovereign state | R1 | C1 | A1 | G1 | Cyprus | Cyprus | YES | START_PLAYABLE | AUTOMATIC | LOCKED | CYP |
| ENT_EUR_CYPRUS_ISSUE | Cyprus issue | Disputed territory | R5 | C3 | A8 | G9 | Cyprus / Northern Cyprus | Cyprus south; Northern Cyprus north | YES | SIMULATED_NOT_PLAYABLE | NOT_APPLICABLE | LOCKED | UNASSIGNED |
| ENT_EUR_CZECH_REPUBLIC | Czech Republic | Recognized sovereign state | R1 | C1 | A1 | G1 | Czech Republic | Czech Republic | YES | START_PLAYABLE | AUTOMATIC | LOCKED | CZE |
| ENT_EUR_DENMARK | Denmark | Recognized sovereign state | R1 | C1 | A1 | G1 | Denmark | Denmark | YES | START_PLAYABLE | AUTOMATIC | LOCKED | DEN |
| ENT_EUR_ESTONIA | Estonia | Recognized sovereign state | R1 | C1 | A1 | G1 | Estonia | Estonia | YES | START_PLAYABLE | AUTOMATIC | LOCKED | EST |
| ENT_EUR_FAROE_ISLANDS | Faroe Islands | Dependent/autonomous country actor | R5 | C1 | A3 | G2 | Denmark | Faroe Islands | YES | START_PLAYABLE | QUALIFIES | LOCKED | FAR |
| ENT_EUR_FEDERAL_REPUBLIC_OF_YUGOSLAVIA | Federal Republic of Yugoslavia | Recognized sovereign state | R1 | C1 | A1 | G1 | Federal Republic of Yugoslavia | Federal Republic of Yugoslavia | YES | START_PLAYABLE | AUTOMATIC | LOCKED | YUG |
| ENT_EUR_FINLAND | Finland | Recognized sovereign state | R1 | C1 | A1 | G1 | Finland | Finland | YES | START_PLAYABLE | AUTOMATIC | LOCKED | FIN |
| ENT_EUR_FRANCE | France | Recognized sovereign state | R1 | C1 | A1 | G1 | France | France | YES | START_PLAYABLE | AUTOMATIC | LOCKED | FRA |
| ENT_EUR_GAGAUZIA | Gagauzia | Internal separatist or autonomous administration | R5 | C3 | A3/A9 | G11 | Moldova | Moldova | YES | SIMULATED_NOT_PLAYABLE | DOES_NOT_QUALIFY | REJECTED | UNASSIGNED |
| ENT_EUR_GERMANY | Germany | Recognized sovereign state | R1 | C1 | A1 | G1 | Germany | Germany | YES | START_PLAYABLE | AUTOMATIC | LOCKED | GER |
| ENT_EUR_GREECE | Greece | Recognized sovereign state | R1 | C1 | A1 | G1 | Greece | Greece | YES | START_PLAYABLE | AUTOMATIC | LOCKED | GRE |
| ENT_EUR_HUNGARY | Hungary | Recognized sovereign state | R1 | C1 | A1 | G1 | Hungary | Hungary | YES | START_PLAYABLE | AUTOMATIC | LOCKED | HUN |
| ENT_EUR_ICELAND | Iceland | Recognized sovereign state | R1 | C1 | A1 | G1 | Iceland | Iceland | YES | START_PLAYABLE | AUTOMATIC | LOCKED | ICE |
| ENT_EUR_IRELAND | Ireland | Recognized sovereign state | R1 | C1 | A1 | G1 | Ireland | Ireland | YES | START_PLAYABLE | AUTOMATIC | LOCKED | IRE |
| ENT_EUR_ITALY | Italy | Recognized sovereign state | R1 | C1 | A1 | G1 | Italy | Italy | YES | START_PLAYABLE | AUTOMATIC | LOCKED | ITA |
| ENT_EUR_KOSOVO | Kosovo | Dependent/autonomous country actor | R5 | C1 | A3 | G2 | Federal Republic of Yugoslavia | Kosovo | YES | START_PLAYABLE | QUALIFIES | LOCKED | KOS |
| ENT_EUR_KURDISTAN_WORKERS_PARTY | Kurdistan Workers' Party | Separatist or resistance movement | R6 | C6 | A10 | G7 | Turkey | Turkey | YES | SIMULATED_NOT_PLAYABLE | DOES_NOT_QUALIFY | LOCKED | UNASSIGNED |
| ENT_EUR_LATVIA | Latvia | Recognized sovereign state | R1 | C1 | A1 | G1 | Latvia | Latvia | YES | START_PLAYABLE | AUTOMATIC | LOCKED | LAT |
| ENT_EUR_LIECHTENSTEIN | Liechtenstein | Recognized sovereign state | R1 | C1 | A1 | G1 | Liechtenstein | Liechtenstein | YES | START_PLAYABLE | AUTOMATIC | LOCKED | LIE |
| ENT_EUR_LITHUANIA | Lithuania | Recognized sovereign state | R1 | C1 | A1 | G1 | Lithuania | Lithuania | YES | START_PLAYABLE | AUTOMATIC | LOCKED | LIT |
| ENT_EUR_LUXEMBOURG | Luxembourg | Recognized sovereign state | R1 | C1 | A1 | G1 | Luxembourg | Luxembourg | YES | START_PLAYABLE | AUTOMATIC | LOCKED | LUX |
| ENT_EUR_MACEDONIA | Macedonia | Recognized sovereign state | R1 | C1 | A1 | G1 | Macedonia | Macedonia | YES | START_PLAYABLE | AUTOMATIC | LOCKED | MKD |
| ENT_EUR_MALTA | Malta | Recognized sovereign state | R1 | C1 | A1 | G1 | Malta | Malta | YES | START_PLAYABLE | AUTOMATIC | LOCKED | MLT |
| ENT_EUR_MOLDOVA | Moldova | Recognized sovereign state | R1 | C1 | A1 | G1 | Moldova | Moldova | YES | START_PLAYABLE | AUTOMATIC | LOCKED | MOL |
| ENT_EUR_MONACO | Monaco | Recognized sovereign state | R1 | C1 | A1 | G1 | Monaco | Monaco | YES | START_PLAYABLE | AUTOMATIC | LOCKED | MCO |
| ENT_EUR_MONTENEGRO | Montenegro | Federal constituent / releasable | R5 | C1 | A2 | G3 | Federal Republic of Yugoslavia | Federal Republic of Yugoslavia | YES | RELEASABLE_PLAYABLE | BORDERLINE | LOCKED | MNT |
| ENT_EUR_NETHERLANDS | Netherlands | Recognized sovereign state | R1 | C1 | A1 | G1 | Netherlands | Netherlands | YES | START_PLAYABLE | AUTOMATIC | LOCKED | HOL |
| ENT_EUR_NORTHERN_CYPRUS | Northern Cyprus | De facto state | R2 | C1 | A9 | G4 | Cyprus | Northern Cyprus | YES | START_PLAYABLE | QUALIFIES | LOCKED | TRNC |
| ENT_EUR_NORWAY | Norway | Recognized sovereign state | R1 | C1 | A1 | G1 | Norway | Norway | YES | START_PLAYABLE | AUTOMATIC | LOCKED | NOR |
| ENT_EUR_POLAND | Poland | Recognized sovereign state | R1 | C1 | A1 | G1 | Poland | Poland | YES | START_PLAYABLE | AUTOMATIC | LOCKED | POL |
| ENT_EUR_PORTUGAL | Portugal | Recognized sovereign state | R1 | C1 | A1 | G1 | Portugal | Portugal | YES | START_PLAYABLE | AUTOMATIC | LOCKED | POR |
| ENT_EUR_REPUBLIC_OF_SERBIAN_KRAJINA | Republic of Serbian Krajina | Internal separatist or autonomous administration | R5 | C3 | A3/A9 | G11 | Croatia | Croatia | YES | SIMULATED_NOT_PLAYABLE | DOES_NOT_QUALIFY | REJECTED | UNASSIGNED |
| ENT_EUR_REPUBLIKA_SRPSKA | Republika Srpska | Internal separatist or autonomous administration | R5 | C3 | A3/A9 | G11 | Bosnia and Herzegovina | Bosnia and Herzegovina | YES | SIMULATED_NOT_PLAYABLE | DOES_NOT_QUALIFY | REJECTED | UNASSIGNED |
| ENT_EUR_ROMANIA | Romania | Recognized sovereign state | R1 | C1 | A1 | G1 | Romania | Romania | YES | START_PLAYABLE | AUTOMATIC | LOCKED | ROM |
| ENT_EUR_SAN_MARINO | San Marino | Recognized sovereign state | R1 | C1 | A1 | G1 | San Marino | San Marino | YES | START_PLAYABLE | AUTOMATIC | LOCKED | SMR |
| ENT_EUR_SERBIA | Serbia | Federal constituent / releasable | R5 | C1 | A2 | G3 | Federal Republic of Yugoslavia | Federal Republic of Yugoslavia | YES | RELEASABLE_PLAYABLE | BORDERLINE | LOCKED | SER |
| ENT_EUR_SLOVAKIA | Slovakia | Recognized sovereign state | R1 | C1 | A1 | G1 | Slovakia | Slovakia | YES | START_PLAYABLE | AUTOMATIC | LOCKED | SVK |
| ENT_EUR_SLOVENIA | Slovenia | Recognized sovereign state | R1 | C1 | A1 | G1 | Slovenia | Slovenia | YES | START_PLAYABLE | AUTOMATIC | LOCKED | SLV |
| ENT_EUR_SPAIN | Spain | Recognized sovereign state | R1 | C1 | A1 | G1 | Spain | Spain | YES | START_PLAYABLE | AUTOMATIC | LOCKED | SPA |
| ENT_EUR_SWEDEN | Sweden | Recognized sovereign state | R1 | C1 | A1 | G1 | Sweden | Sweden | YES | START_PLAYABLE | AUTOMATIC | LOCKED | SWE |
| ENT_EUR_SWITZERLAND | Switzerland | Recognized sovereign state | R1 | C1 | A1 | G1 | Switzerland | Switzerland | YES | START_PLAYABLE | AUTOMATIC | LOCKED | SWI |
| ENT_EUR_THRACE_TURKISH_STRAITS | Thrace / Turkish Straits | Strategic territorial status | R5 | C3 | A8 | G9 | Turkey | Turkey | YES | SIMULATED_NOT_PLAYABLE | NOT_APPLICABLE | LOCKED | UNASSIGNED |
| ENT_EUR_TRANSNISTRIA | Transnistria | Internal separatist or autonomous administration | R5 | C3 | A3/A9 | G11 | Moldova | Moldova | YES | SIMULATED_NOT_PLAYABLE | DOES_NOT_QUALIFY | REJECTED | UNASSIGNED |
| ENT_EUR_TURKEY | Turkey | Recognized sovereign state | R1 | C1 | A1 | G1 | Turkey | Turkey | YES | START_PLAYABLE | AUTOMATIC | LOCKED | TUR |
| ENT_EUR_UNITED_KINGDOM | United Kingdom | Recognized sovereign state | R1 | C1 | A1 | G1 | United Kingdom | United Kingdom | YES | START_PLAYABLE | AUTOMATIC | LOCKED | GBR |
| ENT_EUR_VATICAN_CITY | Vatican City | Recognized sovereign state | R1 | C1 | A1 | G1 | Vatican City | Vatican City | YES | START_PLAYABLE | AUTOMATIC | LOCKED | VAT |
| ENT_EUR_ALAND | Åland | Autonomous or internal region | R5 | C1 | A3 | G11 | Finland | Finland | YES | SIMULATED_NOT_PLAYABLE | DOES_NOT_QUALIFY | LOCKED | UNASSIGNED |

### Former Soviet Union (`FSU`)

| Design ID | Entity | Category | R | C | A | G | Legal sovereign / parent | Effective controller | Exists | Player | Eligibility | Decision | Tech ID |
|---|---|---|:---:|:---:|:---:|:---:|---|---|:---:|---|---|---|---|
| ENT_FSU_ABKHAZIA | Abkhazia | Internal separatist or autonomous administration | R5 | C3 | A3/A9 | G11 | Georgia | Georgia | YES | SIMULATED_NOT_PLAYABLE | DOES_NOT_QUALIFY | REJECTED | UNASSIGNED |
| ENT_FSU_ADJARA | Adjara | Autonomous or internal region | R5 | C1 | A3 | G11 | Georgia | Georgia | YES | SIMULATED_NOT_PLAYABLE | DOES_NOT_QUALIFY | REJECTED | UNASSIGNED |
| ENT_FSU_ARMENIA | Armenia | Recognized sovereign state | R1 | C1 | A1 | G1 | Armenia | Armenia | YES | START_PLAYABLE | AUTOMATIC | LOCKED | ARM |
| ENT_FSU_AZERBAIJAN | Azerbaijan | Recognized sovereign state | R1 | C1 | A1 | G1 | Azerbaijan | Azerbaijan | YES | START_PLAYABLE | AUTOMATIC | LOCKED | AZE |
| ENT_FSU_BELARUS | Belarus | Recognized sovereign state | R1 | C1 | A1 | G1 | Belarus | Belarus | YES | START_PLAYABLE | AUTOMATIC | LOCKED | BLR |
| ENT_FSU_CHECHNYA | Chechnya | Dependent/autonomous country actor | R5 | C1 | A3 | G2 | Russia | Chechnya | YES | START_PLAYABLE | QUALIFIES | LOCKED | CHE |
| ENT_FSU_CRIMEA | Crimea | Autonomous or internal region | R5 | C1 | A3 | G11 | Ukraine | Ukraine | YES | SIMULATED_NOT_PLAYABLE | DOES_NOT_QUALIFY | LOCKED | UNASSIGNED |
| ENT_FSU_GEORGIA | Georgia | Recognized sovereign state | R1 | C1 | A1 | G1 | Georgia | Georgia | YES | START_PLAYABLE | AUTOMATIC | LOCKED | GEO |
| ENT_FSU_NAGORNO_KARABAKH_ARTSAKH | Nagorno-Karabakh / Artsakh | Internal separatist or autonomous administration | R5 | C3 | A3/A9 | G11 | Azerbaijan | Azerbaijan | YES | SIMULATED_NOT_PLAYABLE | DOES_NOT_QUALIFY | REJECTED | UNASSIGNED |
| ENT_FSU_NAKHCHIVAN | Nakhchivan | Dependent/autonomous country actor | R5 | C1 | A3 | G2 | Azerbaijan | Nakhchivan | YES | START_PLAYABLE | QUALIFIES | LOCKED | NAK |
| ENT_FSU_RUSSIA | Russia | Recognized sovereign state | R1 | C1 | A1 | G1 | Russia | Russia | YES | START_PLAYABLE | AUTOMATIC | LOCKED | RUS |
| ENT_FSU_SOUTH_OSSETIA | South Ossetia | Internal separatist or autonomous administration | R5 | C3 | A3/A9 | G11 | Georgia | Georgia | YES | SIMULATED_NOT_PLAYABLE | DOES_NOT_QUALIFY | REJECTED | UNASSIGNED |
| ENT_FSU_TATARSTAN | Tatarstan | Autonomous or internal region | R5 | C1 | A3 | G11 | Russia | Russia | YES | SIMULATED_NOT_PLAYABLE | DOES_NOT_QUALIFY | LOCKED | UNASSIGNED |
| ENT_FSU_UKRAINE | Ukraine | Recognized sovereign state | R1 | C1 | A1 | G1 | Ukraine | Ukraine | YES | START_PLAYABLE | AUTOMATIC | LOCKED | UKR |

### Middle East and North Africa (`MENA`)

| Design ID | Entity | Category | R | C | A | G | Legal sovereign / parent | Effective controller | Exists | Player | Eligibility | Decision | Tech ID |
|---|---|---|:---:|:---:|:---:|:---:|---|---|:---:|---|---|---|---|
| ENT_MENA_ALGERIA | Algeria | Recognized sovereign state | R1 | C1 | A1 | G1 | Algeria | Algeria | YES | START_PLAYABLE | AUTOMATIC | LOCKED | ALG |
| ENT_MENA_ARMED_ISLAMIC_GROUP | Armed Islamic Group | Civil-war or armed faction | R6 | C6 | A10 | G5 | Algeria | Algeria | YES | SIMULATED_NOT_PLAYABLE | DOES_NOT_QUALIFY | LOCKED | UNASSIGNED |
| ENT_MENA_BAHRAIN | Bahrain | Recognized sovereign state | R1 | C1 | A1 | G1 | Bahrain | Bahrain | YES | START_PLAYABLE | AUTOMATIC | LOCKED | BHR |
| ENT_MENA_EGYPT | Egypt | Recognized sovereign state | R1 | C1 | A1 | G1 | Egypt | Egypt | YES | START_PLAYABLE | AUTOMATIC | LOCKED | EGY |
| ENT_MENA_GAZA_STRIP | Gaza Strip | Occupied or leased territorial status | R5 | C4 | A7 | G9 | State of Palestine | Israeli military/security control with Palestinian local administration | YES | SIMULATED_NOT_PLAYABLE | NOT_APPLICABLE | LOCKED | UNASSIGNED |
| ENT_MENA_GOLAN_HEIGHTS | Golan Heights | Occupied or leased territorial status | R5 | C4 | A7 | G9 | Syria | Israel | YES | SIMULATED_NOT_PLAYABLE | NOT_APPLICABLE | LOCKED | UNASSIGNED |
| ENT_MENA_IRAN | Iran | Recognized sovereign state | R1 | C1 | A1 | G1 | Iran | Iran | YES | START_PLAYABLE | AUTOMATIC | LOCKED | IRN |
| ENT_MENA_IRAQ | Iraq | Recognized sovereign state | R1 | C1 | A1 | G1 | Iraq | Iraq | YES | START_PLAYABLE | AUTOMATIC | LOCKED | IRQ |
| ENT_MENA_IRAQI_KURDISTAN | Iraqi Kurdistan | Internal separatist or autonomous administration | R5 | C3 | A3/A9 | G11 | Iraq | Iraq | YES | SIMULATED_NOT_PLAYABLE | DOES_NOT_QUALIFY | REJECTED | UNASSIGNED |
| ENT_MENA_ISLAMIC_SALVATION_FRONT_ALGERIAN_ISLAMISTS | Islamic Salvation Front / Algerian Islamists | Non-territorial political movement | R6 | C5 | A10 | G8 | Algeria | Algeria | YES | SIMULATED_NOT_PLAYABLE | DOES_NOT_QUALIFY | LOCKED | UNASSIGNED |
| ENT_MENA_ISRAEL | Israel | Recognized sovereign state | R1 | C1 | A1 | G1 | Israel | Israel | YES | START_PLAYABLE | AUTOMATIC | LOCKED | ISR |
| ENT_MENA_JORDAN | Jordan | Recognized sovereign state | R1 | C1 | A1 | G1 | Jordan | Jordan | YES | START_PLAYABLE | AUTOMATIC | LOCKED | JOR |
| ENT_MENA_KURDISTAN_DEMOCRATIC_PARTY | Kurdistan Democratic Party | Non-territorial political movement | R6 | C5 | A10 | G8 | Iraq | Iraq | YES | SIMULATED_NOT_PLAYABLE | DOES_NOT_QUALIFY | LOCKED | UNASSIGNED |
| ENT_MENA_KUWAIT | Kuwait | Recognized sovereign state | R1 | C1 | A1 | G1 | Kuwait | Kuwait | YES | START_PLAYABLE | AUTOMATIC | LOCKED | KUW |
| ENT_MENA_LEBANON | Lebanon | Recognized sovereign state | R1 | C1 | A1 | G1 | Lebanon | Lebanon | YES | START_PLAYABLE | AUTOMATIC | LOCKED | LEB |
| ENT_MENA_LIBYA | Libya | Recognized sovereign state | R1 | C1 | A1 | G1 | Libya | Libya | YES | START_PLAYABLE | AUTOMATIC | LOCKED | LBA |
| ENT_MENA_MOROCCO | Morocco | Recognized sovereign state | R1 | C1 | A1 | G1 | Morocco | Morocco | YES | START_PLAYABLE | AUTOMATIC | LOCKED | MOR |
| ENT_MENA_NEUTRAL_ZONE_DIVIDED_SAUDI_KUWAITI_AREA | Neutral Zone / divided Saudi-Kuwaiti area | Disputed territory | R5 | C3 | A8 | G9 | Saudi Arabia / Kuwait | Saudi Arabia / Kuwait | YES | SIMULATED_NOT_PLAYABLE | NOT_APPLICABLE | LOCKED | UNASSIGNED |
| ENT_MENA_OMAN | Oman | Recognized sovereign state | R1 | C1 | A1 | G1 | Oman | Oman | YES | START_PLAYABLE | AUTOMATIC | LOCKED | OMA |
| ENT_MENA_PALESTINE_LIBERATION_ORGANIZATION | Palestine Liberation Organization | Internal political organization | R6 | C5 | A10 | G8 | State of Palestine | State of Palestine | YES | SIMULATED_NOT_PLAYABLE | DOES_NOT_QUALIFY | LOCKED | UNASSIGNED |
| ENT_MENA_PATRIOTIC_UNION_OF_KURDISTAN | Patriotic Union of Kurdistan | Non-territorial political movement | R6 | C5 | A10 | G8 | Iraq | Iraq | YES | SIMULATED_NOT_PLAYABLE | DOES_NOT_QUALIFY | LOCKED | UNASSIGNED |
| ENT_MENA_POLISARIO_FRONT | Polisario Front | Non-territorial political movement | R6 | C5 | A10 | G8 | Western Sahara | Western Sahara | YES | SIMULATED_NOT_PLAYABLE | DOES_NOT_QUALIFY | LOCKED | UNASSIGNED |
| ENT_MENA_QATAR | Qatar | Recognized sovereign state | R1 | C1 | A1 | G1 | Qatar | Qatar | YES | START_PLAYABLE | AUTOMATIC | LOCKED | QAT |
| ENT_MENA_SAHRAWI_ARAB_DEMOCRATIC_REPUBLIC | Sahrawi Arab Democratic Republic | Internal claimant government | R4 | C5 | A10 | G8 | Western Sahara | Western Sahara | YES | SIMULATED_NOT_PLAYABLE | DOES_NOT_QUALIFY | LOCKED | UNASSIGNED |
| ENT_MENA_SAUDI_ARABIA | Saudi Arabia | Recognized sovereign state | R1 | C1 | A1 | G1 | Saudi Arabia | Saudi Arabia | YES | START_PLAYABLE | AUTOMATIC | LOCKED | SAU |
| ENT_MENA_SOUTH_LEBANON_ARMY | South Lebanon Army | Background-only entity | R5 | C5 | A10 | G12 | Lebanon | Lebanon | YES | BACKGROUND_ONLY | NOT_APPLICABLE | LOCKED | UNASSIGNED |
| ENT_MENA_SOUTH_LEBANON_SECURITY_ZONE | South Lebanon security zone | Disputed territory | R5 | C3 | A8 | G9 | Lebanon | Lebanon; foreign military/security presence represented internally | YES | SIMULATED_NOT_PLAYABLE | NOT_APPLICABLE | LOCKED | UNASSIGNED |
| ENT_MENA_SOUTH_YEMEN_SEPARATISTS | South Yemen separatists | Separatist or resistance movement | R6 | C6 | A10 | G7 | Yemen | Yemen | YES | SIMULATED_NOT_PLAYABLE | DOES_NOT_QUALIFY | LOCKED | UNASSIGNED |
| ENT_MENA_SOUTHERN_IRAQI_OPPOSITION | Southern Iraqi opposition | Non-territorial political movement | R6 | C5 | A10 | G8 | Iraq | Iraq | YES | SIMULATED_NOT_PLAYABLE | DOES_NOT_QUALIFY | LOCKED | UNASSIGNED |
| ENT_MENA_SPANISH_NORTH_AFRICAN_PLAZAS | Spanish North African plazas | Disputed territory | R5 | C3 | A8 | G9 | Spain | Spain | YES | SIMULATED_NOT_PLAYABLE | NOT_APPLICABLE | LOCKED | UNASSIGNED |
| ENT_MENA_STATE_OF_PALESTINE | State of Palestine | Partially recognized sovereign state | R2 | C2 | A1/A8 | G1 | State of Palestine | Palestinian institutions under Israeli occupation/security constraints | YES | START_PLAYABLE | QUALIFIES | LOCKED | PAL |
| ENT_MENA_SYRIA | Syria | Recognized sovereign state | R1 | C1 | A1 | G1 | Syria | Syria | YES | START_PLAYABLE | AUTOMATIC | LOCKED | SYR |
| ENT_MENA_TUNISIA | Tunisia | Recognized sovereign state | R1 | C1 | A1 | G1 | Tunisia | Tunisia | YES | START_PLAYABLE | AUTOMATIC | LOCKED | TUN |
| ENT_MENA_UNITED_ARAB_EMIRATES | United Arab Emirates | Recognized sovereign state | R1 | C1 | A1 | G1 | United Arab Emirates | United Arab Emirates | YES | START_PLAYABLE | AUTOMATIC | LOCKED | UAE |
| ENT_MENA_WEST_BANK | West Bank | Occupied or leased territorial status | R5 | C4 | A7 | G9 | State of Palestine | Israeli military/security control with Palestinian local administration | YES | SIMULATED_NOT_PLAYABLE | NOT_APPLICABLE | LOCKED | UNASSIGNED |
| ENT_MENA_WESTERN_SAHARA | Western Sahara | Dependent country actor | R5 | C1 | A4 | G2 | Morocco | Western Sahara | YES | START_PLAYABLE | QUALIFIES | LOCKED | WSA |
| ENT_MENA_YEMEN | Yemen | Recognized sovereign state | R1 | C1 | A1 | G1 | Yemen | Yemen | YES | START_PLAYABLE | AUTOMATIC | LOCKED | YEM |

### Sub-Saharan Africa (`SSA`)

| Design ID | Entity | Category | R | C | A | G | Legal sovereign / parent | Effective controller | Exists | Player | Eligibility | Decision | Tech ID |
|---|---|---|:---:|:---:|:---:|:---:|---|---|:---:|---|---|---|---|
| ENT_SSA_AFRICAN_NATIONAL_CONGRESS | African National Congress | Non-territorial political movement | R6 | C5 | A10 | G8 | South Africa | South Africa | YES | SIMULATED_NOT_PLAYABLE | DOES_NOT_QUALIFY | LOCKED | UNASSIGNED |
| ENT_SSA_ANGOLA | Angola | Recognized sovereign state | R1 | C1 | A1 | G1 | Angola | Angola | YES | START_PLAYABLE | AUTOMATIC | LOCKED | ANG |
| ENT_SSA_BENIN | Benin | Recognized sovereign state | R1 | C1 | A1 | G1 | Benin | Benin | YES | START_PLAYABLE | AUTOMATIC | LOCKED | BEN |
| ENT_SSA_BOTSWANA | Botswana | Recognized sovereign state | R1 | C1 | A1 | G1 | Botswana | Botswana | YES | START_PLAYABLE | AUTOMATIC | LOCKED | BOT |
| ENT_SSA_BRITISH_INDIAN_OCEAN_TERRITORY_DIEGO_GARCIA | British Indian Ocean Territory / Diego Garcia | Dependency or overseas territory | R5 | C1 | A4 | G9 | United Kingdom | United Kingdom | YES | SIMULATED_NOT_PLAYABLE | DOES_NOT_QUALIFY | LOCKED | UNASSIGNED |
| ENT_SSA_BURKINA_FASO | Burkina Faso | Recognized sovereign state | R1 | C1 | A1 | G1 | Burkina Faso | Burkina Faso | YES | START_PLAYABLE | AUTOMATIC | LOCKED | BFA |
| ENT_SSA_BURUNDI | Burundi | Recognized sovereign state | R1 | C1 | A1 | G1 | Burundi | Burundi | YES | START_PLAYABLE | AUTOMATIC | LOCKED | BDI |
| ENT_SSA_CAMEROON | Cameroon | Recognized sovereign state | R1 | C1 | A1 | G1 | Cameroon | Cameroon | YES | START_PLAYABLE | AUTOMATIC | LOCKED | CMR |
| ENT_SSA_CAPE_VERDE | Cape Verde | Recognized sovereign state | R1 | C1 | A1 | G1 | Cape Verde | Cape Verde | YES | START_PLAYABLE | AUTOMATIC | LOCKED | CPV |
| ENT_SSA_CENTRAL_AFRICAN_REPUBLIC | Central African Republic | Recognized sovereign state | R1 | C1 | A1 | G1 | Central African Republic | Central African Republic | YES | START_PLAYABLE | AUTOMATIC | LOCKED | CAR |
| ENT_SSA_CHAD | Chad | Recognized sovereign state | R1 | C1 | A1 | G1 | Chad | Chad | YES | START_PLAYABLE | AUTOMATIC | LOCKED | CHD |
| ENT_SSA_COMOROS | Comoros | Recognized sovereign state | R1 | C1 | A1 | G1 | Comoros | Comoros | YES | START_PLAYABLE | AUTOMATIC | LOCKED | COM |
| ENT_SSA_COTE_D_IVOIRE | Côte d'Ivoire | Recognized sovereign state | R1 | C1 | A1 | G1 | Côte d'Ivoire | Côte d'Ivoire | YES | START_PLAYABLE | AUTOMATIC | LOCKED | CIV |
| ENT_SSA_DJIBOUTI | Djibouti | Recognized sovereign state | R1 | C1 | A1 | G1 | Djibouti | Djibouti | YES | START_PLAYABLE | AUTOMATIC | LOCKED | DJI |
| ENT_SSA_EQUATORIAL_GUINEA | Equatorial Guinea | Recognized sovereign state | R1 | C1 | A1 | G1 | Equatorial Guinea | Equatorial Guinea | YES | START_PLAYABLE | AUTOMATIC | LOCKED | EQG |
| ENT_SSA_ERITREA | Eritrea | Independent de facto state | R3 | C1 | A1 | G1 | Eritrea | Eritrean government | YES | START_PLAYABLE | QUALIFIES | LOCKED | ERI |
| ENT_SSA_ETHIOPIA | Ethiopia | Recognized sovereign state | R1 | C1 | A1 | G1 | Ethiopia | Ethiopia | YES | START_PLAYABLE | AUTOMATIC | LOCKED | ETH |
| ENT_SSA_GABON | Gabon | Recognized sovereign state | R1 | C1 | A1 | G1 | Gabon | Gabon | YES | START_PLAYABLE | AUTOMATIC | LOCKED | GAB |
| ENT_SSA_GAMBIA | Gambia | Recognized sovereign state | R1 | C1 | A1 | G1 | Gambia | Gambia | YES | START_PLAYABLE | AUTOMATIC | LOCKED | GAM |
| ENT_SSA_GHANA | Ghana | Recognized sovereign state | R1 | C1 | A1 | G1 | Ghana | Ghana | YES | START_PLAYABLE | AUTOMATIC | LOCKED | GHA |
| ENT_SSA_GUINEA | Guinea | Recognized sovereign state | R1 | C1 | A1 | G1 | Guinea | Guinea | YES | START_PLAYABLE | AUTOMATIC | LOCKED | GUI |
| ENT_SSA_GUINEA_BISSAU | Guinea-Bissau | Recognized sovereign state | R1 | C1 | A1 | G1 | Guinea-Bissau | Guinea-Bissau | YES | START_PLAYABLE | AUTOMATIC | LOCKED | GNB |
| ENT_SSA_INKATHA_FREEDOM_PARTY | Inkatha Freedom Party | Non-territorial political movement | R6 | C5 | A10 | G8 | South Africa | South Africa | YES | SIMULATED_NOT_PLAYABLE | DOES_NOT_QUALIFY | LOCKED | UNASSIGNED |
| ENT_SSA_KENYA | Kenya | Recognized sovereign state | R1 | C1 | A1 | G1 | Kenya | Kenya | YES | START_PLAYABLE | AUTOMATIC | LOCKED | KEN |
| ENT_SSA_LESOTHO | Lesotho | Recognized sovereign state | R1 | C1 | A1 | G1 | Lesotho | Lesotho | YES | START_PLAYABLE | AUTOMATIC | LOCKED | LES |
| ENT_SSA_LIBERIA | Liberia | Recognized sovereign state | R1 | C1 | A1 | G1 | Liberia | Liberia | YES | START_PLAYABLE | AUTOMATIC | LOCKED | LBR |
| ENT_SSA_MADAGASCAR | Madagascar | Recognized sovereign state | R1 | C1 | A1 | G1 | Madagascar | Madagascar | YES | START_PLAYABLE | AUTOMATIC | LOCKED | MDG |
| ENT_SSA_MALAWI | Malawi | Recognized sovereign state | R1 | C1 | A1 | G1 | Malawi | Malawi | YES | START_PLAYABLE | AUTOMATIC | LOCKED | MWI |
| ENT_SSA_MALI | Mali | Recognized sovereign state | R1 | C1 | A1 | G1 | Mali | Mali | YES | START_PLAYABLE | AUTOMATIC | LOCKED | MLI |
| ENT_SSA_MAURITIUS | Mauritius | Recognized sovereign state | R1 | C1 | A1 | G1 | Mauritius | Mauritius | YES | START_PLAYABLE | AUTOMATIC | LOCKED | MUS |
| ENT_SSA_MAYOTTE | Mayotte | Dependency or overseas territory | R5 | C1 | A4 | G9 | France | France | YES | SIMULATED_NOT_PLAYABLE | DOES_NOT_QUALIFY | LOCKED | UNASSIGNED |
| ENT_SSA_MOZAMBIQUE | Mozambique | Recognized sovereign state | R1 | C1 | A1 | G1 | Mozambique | Mozambique | YES | START_PLAYABLE | AUTOMATIC | LOCKED | MOZ |
| ENT_SSA_NAMIBIA | Namibia | Recognized sovereign state | R1 | C1 | A1 | G1 | Namibia | Namibia | YES | START_PLAYABLE | AUTOMATIC | LOCKED | NAM |
| ENT_SSA_NATIONAL_PATRIOTIC_FRONT_OF_LIBERIA | National Patriotic Front of Liberia | Civil-war or armed faction | R6 | C6 | A10 | G5 | Liberia | Liberia | YES | SIMULATED_NOT_PLAYABLE | DOES_NOT_QUALIFY | LOCKED | UNASSIGNED |
| ENT_SSA_NIGER | Niger | Recognized sovereign state | R1 | C1 | A1 | G1 | Niger | Niger | YES | START_PLAYABLE | AUTOMATIC | LOCKED | NGR |
| ENT_SSA_NIGERIA | Nigeria | Recognized sovereign state | R1 | C1 | A1 | G1 | Nigeria | Nigeria | YES | START_PLAYABLE | AUTOMATIC | LOCKED | NGA |
| ENT_SSA_PUNTLAND | Puntland | Background-only entity | R5 | C5 | A10 | G12 | Somalia | Somalia | NO | BACKGROUND_ONLY | NOT_APPLICABLE | LOCKED | UNASSIGNED |
| ENT_SSA_RENAMO | RENAMO | Non-territorial political movement | R6 | C5 | A10 | G8 | Mozambique | Mozambique | YES | SIMULATED_NOT_PLAYABLE | DOES_NOT_QUALIFY | LOCKED | UNASSIGNED |
| ENT_SSA_REPUBLIC_OF_THE_CONGO | Republic of the Congo | Recognized sovereign state | R1 | C1 | A1 | G1 | Republic of the Congo | Republic of the Congo | YES | START_PLAYABLE | AUTOMATIC | LOCKED | COG |
| ENT_SSA_REVOLUTIONARY_UNITED_FRONT | Revolutionary United Front | Civil-war or armed faction | R6 | C6 | A10 | G5 | Sierra Leone | Sierra Leone | YES | SIMULATED_NOT_PLAYABLE | DOES_NOT_QUALIFY | LOCKED | UNASSIGNED |
| ENT_SSA_RWANDA | Rwanda | Recognized sovereign state | R1 | C1 | A1 | G1 | Rwanda | Rwanda | YES | START_PLAYABLE | AUTOMATIC | LOCKED | RWA |
| ENT_SSA_RWANDAN_PATRIOTIC_FRONT | Rwandan Patriotic Front | Civil-war or armed faction | R6 | C6 | A10 | G5 | Rwanda | Rwanda | YES | SIMULATED_NOT_PLAYABLE | DOES_NOT_QUALIFY | LOCKED | UNASSIGNED |
| ENT_SSA_REUNION | Réunion | Dependency or overseas territory | R5 | C1 | A4 | G9 | France | France | YES | SIMULATED_NOT_PLAYABLE | DOES_NOT_QUALIFY | LOCKED | UNASSIGNED |
| ENT_SSA_SAINT_HELENA_ASCENSION_AND_TRISTAN_DA_CUNHA | Saint Helena, Ascension and Tristan da Cunha | Dependency or overseas territory | R5 | C1 | A4 | G9 | United Kingdom | United Kingdom | YES | SIMULATED_NOT_PLAYABLE | DOES_NOT_QUALIFY | LOCKED | UNASSIGNED |
| ENT_SSA_SENEGAL | Senegal | Recognized sovereign state | R1 | C1 | A1 | G1 | Senegal | Senegal | YES | START_PLAYABLE | AUTOMATIC | LOCKED | SEN |
| ENT_SSA_SEYCHELLES | Seychelles | Recognized sovereign state | R1 | C1 | A1 | G1 | Seychelles | Seychelles | YES | START_PLAYABLE | AUTOMATIC | LOCKED | SEY |
| ENT_SSA_SIERRA_LEONE | Sierra Leone | Recognized sovereign state | R1 | C1 | A1 | G1 | Sierra Leone | Sierra Leone | YES | START_PLAYABLE | AUTOMATIC | LOCKED | SLE |
| ENT_SSA_SOMALIA | Somalia | Recognized sovereign state | R1 | C1 | A1 | G1 | Somalia | Somalia | YES | START_PLAYABLE | AUTOMATIC | LOCKED | SOM |
| ENT_SSA_SOMALILAND | Somaliland | Internal separatist or autonomous administration | R5 | C3 | A3/A9 | G11 | Somalia | Somalia | YES | SIMULATED_NOT_PLAYABLE | DOES_NOT_QUALIFY | REJECTED | UNASSIGNED |
| ENT_SSA_SOUTH_AFRICA | South Africa | Recognized sovereign state | R1 | C1 | A1 | G1 | South Africa | South Africa | YES | START_PLAYABLE | AUTOMATIC | LOCKED | SAF |
| ENT_SSA_SUDAN | Sudan | Recognized sovereign state | R1 | C1 | A1 | G1 | Sudan | Sudan | YES | START_PLAYABLE | AUTOMATIC | LOCKED | SUD |
| ENT_SSA_SUDAN_PEOPLE_S_LIBERATION_ARMY | Sudan People's Liberation Army | Civil-war or armed faction | R6 | C6 | A10 | G5 | Sudan | Sudan | YES | SIMULATED_NOT_PLAYABLE | DOES_NOT_QUALIFY | LOCKED | UNASSIGNED |
| ENT_SSA_SWAZILAND | Swaziland | Recognized sovereign state | R1 | C1 | A1 | G1 | Swaziland | Swaziland | YES | START_PLAYABLE | AUTOMATIC | LOCKED | SWZ |
| ENT_SSA_SAO_TOME_AND_PRINCIPE | São Tomé and Príncipe | Recognized sovereign state | R1 | C1 | A1 | G1 | São Tomé and Príncipe | São Tomé and Príncipe | YES | START_PLAYABLE | AUTOMATIC | LOCKED | STP |
| ENT_SSA_TANZANIA | Tanzania | Recognized sovereign state | R1 | C1 | A1 | G1 | Tanzania | Tanzania | YES | START_PLAYABLE | AUTOMATIC | LOCKED | TZA |
| ENT_SSA_TOGO | Togo | Recognized sovereign state | R1 | C1 | A1 | G1 | Togo | Togo | YES | START_PLAYABLE | AUTOMATIC | LOCKED | TOG |
| ENT_SSA_UGANDA | Uganda | Recognized sovereign state | R1 | C1 | A1 | G1 | Uganda | Uganda | YES | START_PLAYABLE | AUTOMATIC | LOCKED | UGA |
| ENT_SSA_ULIMO | ULIMO | Civil-war or armed faction | R6 | C6 | A10 | G5 | Liberia | Liberia | YES | SIMULATED_NOT_PLAYABLE | DOES_NOT_QUALIFY | LOCKED | UNASSIGNED |
| ENT_SSA_UNITA | UNITA | Civil-war or armed faction | R6 | C6 | A10 | G5 | Angola | Angola | YES | SIMULATED_NOT_PLAYABLE | DOES_NOT_QUALIFY | LOCKED | UNASSIGNED |
| ENT_SSA_ZAIRE | Zaire | Recognized sovereign state | R1 | C1 | A1 | G1 | Zaire | Zaire | YES | START_PLAYABLE | AUTOMATIC | LOCKED | ZAI |
| ENT_SSA_ZAMBIA | Zambia | Recognized sovereign state | R1 | C1 | A1 | G1 | Zambia | Zambia | YES | START_PLAYABLE | AUTOMATIC | LOCKED | ZMB |
| ENT_SSA_ZIMBABWE | Zimbabwe | Recognized sovereign state | R1 | C1 | A1 | G1 | Zimbabwe | Zimbabwe | YES | START_PLAYABLE | AUTOMATIC | LOCKED | ZIM |

### South Asia (`SAS`)

| Design ID | Entity | Category | R | C | A | G | Legal sovereign / parent | Effective controller | Exists | Player | Eligibility | Decision | Tech ID |
|---|---|---|:---:|:---:|:---:|:---:|---|---|:---:|---|---|---|---|
| ENT_SAS_AFGHAN_REFUGEE_NETWORKS | Afghan refugee networks | Background-only entity | R5 | C5 | A10 | G12 | Afghanistan/Pakistan/Iran | Afghanistan/Pakistan/Iran | YES | BACKGROUND_ONLY | NOT_APPLICABLE | LOCKED | UNASSIGNED |
| ENT_SAS_AFGHANISTAN | Afghanistan | Recognized sovereign state | R1 | C1 | A1 | G1 | Afghanistan | Afghanistan | YES | START_PLAYABLE | AUTOMATIC | LOCKED | AFG |
| ENT_SAS_AZAD_JAMMU_AND_KASHMIR | Azad Jammu and Kashmir | Internal separatist or autonomous administration | R5 | C3 | A3/A9 | G11 | Pakistan | Pakistan | YES | SIMULATED_NOT_PLAYABLE | DOES_NOT_QUALIFY | REJECTED | UNASSIGNED |
| ENT_SAS_BALOCH_SEPARATISM | Baloch separatism | Separatist or resistance movement | R6 | C6 | A10 | G7 | Pakistan | Pakistan | YES | SIMULATED_NOT_PLAYABLE | DOES_NOT_QUALIFY | LOCKED | UNASSIGNED |
| ENT_SAS_BANGLADESH | Bangladesh | Recognized sovereign state | R1 | C1 | A1 | G1 | Bangladesh | Bangladesh | YES | START_PLAYABLE | AUTOMATIC | LOCKED | BGD |
| ENT_SAS_BHUTAN | Bhutan | Recognized sovereign state | R1 | C1 | A1 | G1 | Bhutan | Bhutan | YES | START_PLAYABLE | AUTOMATIC | LOCKED | BHU |
| ENT_SAS_CHAGOS_EXILES_SOVEREIGNTY_CLAIM | Chagos exiles / sovereignty claim | Exile or claim movement | R4 | C5 | A10 | G8 | Mauritius/United Kingdom | Mauritius/United Kingdom | YES | SIMULATED_NOT_PLAYABLE | DOES_NOT_QUALIFY | LOCKED | UNASSIGNED |
| ENT_SAS_CHITTAGONG_HILL_TRACTS_INSURGENTS | Chittagong Hill Tracts insurgents | Separatist or resistance movement | R6 | C6 | A10 | G7 | Bangladesh | Bangladesh | YES | SIMULATED_NOT_PLAYABLE | DOES_NOT_QUALIFY | LOCKED | UNASSIGNED |
| ENT_SAS_DURAND_LINE_DISPUTE | Durand Line dispute | Disputed territory | R5 | C3 | A8 | G9 | Afghanistan / Pakistan | Afghanistan / Pakistan | YES | SIMULATED_NOT_PLAYABLE | NOT_APPLICABLE | LOCKED | UNASSIGNED |
| ENT_SAS_GILGIT_BALTISTAN | Gilgit-Baltistan | Internal separatist or autonomous administration | R5 | C3 | A3/A9 | G11 | Pakistan | Pakistan | YES | SIMULATED_NOT_PLAYABLE | DOES_NOT_QUALIFY | REJECTED | UNASSIGNED |
| ENT_SAS_HEZB_E_ISLAMI_GULBUDDIN | Hezb-e Islami Gulbuddin | Civil-war or armed faction | R6 | C6 | A10 | G5 | Afghanistan | Afghanistan | YES | SIMULATED_NOT_PLAYABLE | DOES_NOT_QUALIFY | REJECTED | UNASSIGNED |
| ENT_SAS_HEZB_E_WAHDAT | Hezb-e Wahdat | Civil-war or armed faction | R6 | C6 | A10 | G5 | Afghanistan | Afghanistan | YES | SIMULATED_NOT_PLAYABLE | DOES_NOT_QUALIFY | REJECTED | UNASSIGNED |
| ENT_SAS_INDIA | India | Recognized sovereign state | R1 | C1 | A1 | G1 | India | India | YES | START_PLAYABLE | AUTOMATIC | LOCKED | IND |
| ENT_SAS_ITTIHAD_I_ISLAMI | Ittihad-i Islami | Civil-war or armed faction | R6 | C6 | A10 | G5 | Afghanistan | Afghanistan | YES | SIMULATED_NOT_PLAYABLE | DOES_NOT_QUALIFY | REJECTED | UNASSIGNED |
| ENT_SAS_JAMIAT_E_ISLAMI_RABBANI_GOVERNMENT | Jamiat-e Islami / Rabbani government | Civil-war or armed faction | R6 | C6 | A10 | G5 | Afghanistan | Afghanistan | YES | SIMULATED_NOT_PLAYABLE | DOES_NOT_QUALIFY | REJECTED | UNASSIGNED |
| ENT_SAS_JAMMU_AND_KASHMIR_GOVERNMENT | Jammu and Kashmir government | Autonomous or internal region | R5 | C1 | A3 | G11 | India | India | YES | SIMULATED_NOT_PLAYABLE | DOES_NOT_QUALIFY | LOCKED | UNASSIGNED |
| ENT_SAS_JUNBISH_I_MILLI | Junbish-i Milli | Civil-war or armed faction | R6 | C6 | A10 | G5 | Afghanistan | Afghanistan | YES | SIMULATED_NOT_PLAYABLE | DOES_NOT_QUALIFY | REJECTED | UNASSIGNED |
| ENT_SAS_KASHMIR | Kashmir | Internal disputed or strategic region | R5 | C3 | A8 | G9 | India | India | YES | SIMULATED_NOT_PLAYABLE | NOT_APPLICABLE | LOCKED | UNASSIGNED |
| ENT_SAS_KHALISTAN_MILITANTS | Khalistan militants | Separatist or resistance movement | R6 | C6 | A10 | G7 | India | India | YES | SIMULATED_NOT_PLAYABLE | DOES_NOT_QUALIFY | LOCKED | UNASSIGNED |
| ENT_SAS_LIBERATION_TIGERS_OF_TAMIL_EELAM | Liberation Tigers of Tamil Eelam | Separatist or resistance movement | R6 | C6 | A10 | G7 | Sri Lanka | Sri Lanka | YES | SIMULATED_NOT_PLAYABLE | DOES_NOT_QUALIFY | LOCKED | UNASSIGNED |
| ENT_SAS_MALDIVES | Maldives | Recognized sovereign state | R1 | C1 | A1 | G1 | Maldives | Maldives | YES | START_PLAYABLE | AUTOMATIC | LOCKED | MDV |
| ENT_SAS_NEPAL | Nepal | Recognized sovereign state | R1 | C1 | A1 | G1 | Nepal | Nepal | YES | START_PLAYABLE | AUTOMATIC | LOCKED | NEP |
| ENT_SAS_NORTHEAST_INDIAN_INSURGENTS | Northeast Indian insurgents | Separatist or resistance movement | R6 | C6 | A10 | G7 | India | India | YES | SIMULATED_NOT_PLAYABLE | DOES_NOT_QUALIFY | LOCKED | UNASSIGNED |
| ENT_SAS_PAKISTAN | Pakistan | Recognized sovereign state | R1 | C1 | A1 | G1 | Pakistan | Pakistan | YES | START_PLAYABLE | AUTOMATIC | LOCKED | PAK |
| ENT_SAS_PASHTUN_BORDERLANDS | Pashtun borderlands | Internal disputed or strategic region | R5 | C3 | A8 | G9 | Afghanistan/Pakistan | Afghanistan/Pakistan | YES | SIMULATED_NOT_PLAYABLE | NOT_APPLICABLE | LOCKED | UNASSIGNED |
| ENT_SAS_SIKKIM | Sikkim | Autonomous or internal region | R5 | C1 | A3 | G11 | India | India | YES | SIMULATED_NOT_PLAYABLE | DOES_NOT_QUALIFY | LOCKED | UNASSIGNED |
| ENT_SAS_SINDHI_NATIONALIST_MOVEMENTS | Sindhi nationalist movements | Separatist or resistance movement | R6 | C6 | A10 | G7 | Pakistan | Pakistan | YES | SIMULATED_NOT_PLAYABLE | DOES_NOT_QUALIFY | LOCKED | UNASSIGNED |
| ENT_SAS_SRI_LANKA | Sri Lanka | Recognized sovereign state | R1 | C1 | A1 | G1 | Sri Lanka | Sri Lanka | YES | START_PLAYABLE | AUTOMATIC | LOCKED | LKA |
| ENT_SAS_TALIBAN_MOVEMENT | Taliban movement | Non-territorial political movement | R6 | C5 | A10 | G8 | Afghanistan | Afghanistan | NO | SIMULATED_NOT_PLAYABLE | DOES_NOT_QUALIFY | LOCKED | UNASSIGNED |
| ENT_SAS_TIBETAN_GOVERNMENT_IN_EXILE | Tibetan Government-in-Exile | Exile or claim movement | R4 | C5 | A10 | G8 | Tibet | Tibet | YES | SIMULATED_NOT_PLAYABLE | DOES_NOT_QUALIFY | LOCKED | UNASSIGNED |

### Central Asia (`CAS`)

| Design ID | Entity | Category | R | C | A | G | Legal sovereign / parent | Effective controller | Exists | Player | Eligibility | Decision | Tech ID |
|---|---|---|:---:|:---:|:---:|:---:|---|---|:---:|---|---|---|---|
| ENT_CAS_ISLAMIC_MOVEMENT_OF_UZBEKISTAN_PRECURSOR_NETWORKS | Islamic Movement of Uzbekistan precursor networks | Non-territorial political movement | R6 | C5 | A10 | G8 | Uzbekistan | Uzbekistan | YES | SIMULATED_NOT_PLAYABLE | DOES_NOT_QUALIFY | LOCKED | UNASSIGNED |
| ENT_CAS_KAZAKHSTAN | Kazakhstan | Recognized sovereign state | R1 | C1 | A1 | G1 | Kazakhstan | Kazakhstan | YES | START_PLAYABLE | AUTOMATIC | LOCKED | KAZ |
| ENT_CAS_KYRGYZSTAN | Kyrgyzstan | Recognized sovereign state | R1 | C1 | A1 | G1 | Kyrgyzstan | Kyrgyzstan | YES | START_PLAYABLE | AUTOMATIC | LOCKED | KYR |
| ENT_CAS_TAJIK_OPPOSITION | Tajik Opposition | Non-territorial political movement | R6 | C5 | A10 | G8 | Tajikistan | Tajikistan | YES | SIMULATED_NOT_PLAYABLE | DOES_NOT_QUALIFY | LOCKED | UNASSIGNED |
| ENT_CAS_TAJIKISTAN | Tajikistan | Recognized sovereign state | R1 | C1 | A1 | G1 | Tajikistan | Tajikistan | YES | START_PLAYABLE | AUTOMATIC | LOCKED | TAJ |
| ENT_CAS_TURKMENISTAN | Turkmenistan | Recognized sovereign state | R1 | C1 | A1 | G1 | Turkmenistan | Turkmenistan | YES | START_PLAYABLE | AUTOMATIC | LOCKED | TKM |
| ENT_CAS_UZBEKISTAN | Uzbekistan | Recognized sovereign state | R1 | C1 | A1 | G1 | Uzbekistan | Uzbekistan | YES | START_PLAYABLE | AUTOMATIC | LOCKED | UZB |

### East Asia (`EAS`)

| Design ID | Entity | Category | R | C | A | G | Legal sovereign / parent | Effective controller | Exists | Player | Eligibility | Decision | Tech ID |
|---|---|---|:---:|:---:|:---:|:---:|---|---|:---:|---|---|---|---|
| ENT_EAS_CHINA | China | Recognized sovereign state | R1 | C1 | A1 | G1 | China | China | YES | START_PLAYABLE | AUTOMATIC | LOCKED | CHN |
| ENT_EAS_GUANGXI_ZHUANG_AUTONOMY | Guangxi / Zhuang autonomy | Autonomous or internal region | R5 | C1 | A3 | G11 | China | China | YES | SIMULATED_NOT_PLAYABLE | DOES_NOT_QUALIFY | LOCKED | UNASSIGNED |
| ENT_EAS_HONG_KONG | Hong Kong | Dependent country actor | R5 | C1 | A4 | G2 | United Kingdom | Hong Kong | YES | START_PLAYABLE | QUALIFIES | LOCKED | HKG |
| ENT_EAS_INNER_MONGOLIA | Inner Mongolia | Autonomous or internal region | R5 | C1 | A3 | G11 | China | China | YES | SIMULATED_NOT_PLAYABLE | DOES_NOT_QUALIFY | LOCKED | UNASSIGNED |
| ENT_EAS_JAPAN | Japan | Recognized sovereign state | R1 | C1 | A1 | G1 | Japan | Japan | YES | START_PLAYABLE | AUTOMATIC | LOCKED | JAP |
| ENT_EAS_KOREAN_DEMILITARIZED_ZONE | Korean Demilitarized Zone | Strategic territorial status | R5 | C3 | A8 | G9 | North Korea / South Korea | Armistice administrations | YES | SIMULATED_NOT_PLAYABLE | NOT_APPLICABLE | LOCKED | UNASSIGNED |
| ENT_EAS_KURIL_ISLANDS_NORTHERN_TERRITORIES | Kuril Islands / Northern Territories | Disputed territory | R5 | C3 | A8 | G9 | Russia; claimed by Japan | Russia | YES | SIMULATED_NOT_PLAYABLE | NOT_APPLICABLE | LOCKED | UNASSIGNED |
| ENT_EAS_MACAU | Macau | Dependent country actor | R5 | C1 | A4 | G2 | Portugal | Macau | YES | START_PLAYABLE | QUALIFIES | LOCKED | MAC |
| ENT_EAS_MANCHURIA_REGIONAL_IDENTITY | Manchuria regional identity | Background-only entity | R5 | C5 | A10 | G12 | China | China | YES | BACKGROUND_ONLY | NOT_APPLICABLE | LOCKED | UNASSIGNED |
| ENT_EAS_MONGOLIA | Mongolia | Recognized sovereign state | R1 | C1 | A1 | G1 | Mongolia | Mongolia | YES | START_PLAYABLE | AUTOMATIC | LOCKED | MON |
| ENT_EAS_NINGXIA_HUI_AUTONOMY | Ningxia Hui autonomy | Autonomous or internal region | R5 | C1 | A3 | G11 | China | China | YES | SIMULATED_NOT_PLAYABLE | DOES_NOT_QUALIFY | LOCKED | UNASSIGNED |
| ENT_EAS_NORTH_KOREA | North Korea | Recognized sovereign state | R1 | C1 | A1 | G1 | North Korea | North Korea | YES | START_PLAYABLE | AUTOMATIC | LOCKED | PRK |
| ENT_EAS_SENKAKU_DIAOYU_ISLANDS | Senkaku / Diaoyu Islands | Disputed territory | R5 | C3 | A8 | G9 | Japan; claimed by China and Taiwan | Japan | YES | SIMULATED_NOT_PLAYABLE | NOT_APPLICABLE | LOCKED | UNASSIGNED |
| ENT_EAS_SOUTH_KOREA | South Korea | Recognized sovereign state | R1 | C1 | A1 | G1 | South Korea | South Korea | YES | START_PLAYABLE | AUTOMATIC | LOCKED | KOR |
| ENT_EAS_TAIWAN | Taiwan | Partially recognized sovereign state | R2 | C1 | A1 | G1 | Taiwan | Taiwan | YES | START_PLAYABLE | QUALIFIES | LOCKED | TWN |
| ENT_EAS_TAIWAN_STRAIT | Taiwan Strait | Strategic territorial status | R5 | C3 | A8 | G9 | China / Taiwan | China and Taiwan in respective waters | YES | SIMULATED_NOT_PLAYABLE | NOT_APPLICABLE | LOCKED | UNASSIGNED |
| ENT_EAS_TAKESHIMA_DOKDO | Takeshima / Dokdo | Disputed territory | R5 | C3 | A8 | G9 | South Korea; claimed by Japan | South Korea | YES | SIMULATED_NOT_PLAYABLE | NOT_APPLICABLE | LOCKED | UNASSIGNED |
| ENT_EAS_TIBET | Tibet | Dependent/autonomous country actor | R5 | C1 | A3 | G2 | China | Tibet | YES | START_PLAYABLE | QUALIFIES | LOCKED | TIB |
| ENT_EAS_XINJIANG | Xinjiang | Autonomous or internal region | R5 | C1 | A3 | G11 | China | China | YES | SIMULATED_NOT_PLAYABLE | DOES_NOT_QUALIFY | LOCKED | UNASSIGNED |

### Southeast Asia (`SEA`)

| Design ID | Entity | Category | R | C | A | G | Legal sovereign / parent | Effective controller | Exists | Player | Eligibility | Decision | Tech ID |
|---|---|---|:---:|:---:|:---:|:---:|---|---|:---:|---|---|---|---|
| ENT_SEA_ACEH_SEPARATISTS_FREE_ACEH_MOVEMENT | Aceh separatists / Free Aceh Movement | Separatist or resistance movement | R6 | C6 | A10 | G7 | Indonesia | Indonesia | YES | SIMULATED_NOT_PLAYABLE | DOES_NOT_QUALIFY | LOCKED | UNASSIGNED |
| ENT_SEA_ARAKAN_RAKHINE_INSURGENT_ACTORS | Arakan / Rakhine insurgent actors | Civil-war or armed faction | R6 | C6 | A10 | G5 | Myanmar | Myanmar | YES | SIMULATED_NOT_PLAYABLE | DOES_NOT_QUALIFY | LOCKED | UNASSIGNED |
| ENT_SEA_BRUNEI | Brunei | Recognized sovereign state | R1 | C1 | A1 | G1 | Brunei | Brunei | YES | START_PLAYABLE | AUTOMATIC | LOCKED | BRU |
| ENT_SEA_CAMBODIA | Cambodia | Recognized sovereign state | R1 | C1 | A1 | G1 | Cambodia | Cambodia | YES | START_PLAYABLE | AUTOMATIC | LOCKED | CAM |
| ENT_SEA_CAMBODIAN_PEOPLE_S_PARTY | Cambodian People's Party | Non-territorial political movement | R6 | C5 | A10 | G8 | Cambodia | Cambodia | YES | SIMULATED_NOT_PLAYABLE | DOES_NOT_QUALIFY | LOCKED | UNASSIGNED |
| ENT_SEA_EAST_TIMOR | East Timor | Occupied/internal disputed region | R5 | C4 | A7 | G9 | Indonesia | Indonesia | YES | SIMULATED_NOT_PLAYABLE | NOT_APPLICABLE | LOCKED | UNASSIGNED |
| ENT_SEA_FRETILIN_EAST_TIMORESE_RESISTANCE | Fretilin / East Timorese resistance | Separatist or resistance movement | R6 | C6 | A10 | G7 | Indonesia | Indonesia | YES | SIMULATED_NOT_PLAYABLE | DOES_NOT_QUALIFY | LOCKED | UNASSIGNED |
| ENT_SEA_FUNCINPEC_ROYALIST_FACTION | FUNCINPEC / royalist faction | Non-territorial political movement | R6 | C5 | A10 | G8 | Cambodia | Cambodia | YES | SIMULATED_NOT_PLAYABLE | DOES_NOT_QUALIFY | LOCKED | UNASSIGNED |
| ENT_SEA_INDONESIA | Indonesia | Recognized sovereign state | R1 | C1 | A1 | G1 | Indonesia | Indonesia | YES | START_PLAYABLE | AUTOMATIC | LOCKED | IDN |
| ENT_SEA_KACHIN_INDEPENDENCE_ORGANIZATION | Kachin Independence Organization | Civil-war or armed faction | R6 | C6 | A10 | G5 | Myanmar | Myanmar | YES | SIMULATED_NOT_PLAYABLE | DOES_NOT_QUALIFY | LOCKED | UNASSIGNED |
| ENT_SEA_KAREN_NATIONAL_UNION | Karen National Union | Civil-war or armed faction | R6 | C6 | A10 | G5 | Myanmar | Myanmar | YES | SIMULATED_NOT_PLAYABLE | DOES_NOT_QUALIFY | LOCKED | UNASSIGNED |
| ENT_SEA_KHMER_ROUGE | Khmer Rouge | Civil-war or armed faction | R6 | C6 | A10 | G5 | Cambodia | Cambodia | YES | SIMULATED_NOT_PLAYABLE | DOES_NOT_QUALIFY | LOCKED | UNASSIGNED |
| ENT_SEA_LAOS | Laos | Recognized sovereign state | R1 | C1 | A1 | G1 | Laos | Laos | YES | START_PLAYABLE | AUTOMATIC | LOCKED | LAO |
| ENT_SEA_MALAYSIA | Malaysia | Recognized sovereign state | R1 | C1 | A1 | G1 | Malaysia | Malaysia | YES | START_PLAYABLE | AUTOMATIC | LOCKED | MYS |
| ENT_SEA_MORO_SEPARATISM | Moro separatism | Separatist or resistance movement | R6 | C6 | A10 | G7 | Philippines | Philippines | YES | SIMULATED_NOT_PLAYABLE | DOES_NOT_QUALIFY | LOCKED | UNASSIGNED |
| ENT_SEA_MYANMAR | Myanmar | Recognized sovereign state | R1 | C1 | A1 | G1 | Myanmar | Myanmar | YES | START_PLAYABLE | AUTOMATIC | LOCKED | MYA |
| ENT_SEA_NATUNA_SEA_INDONESIAN_EEZ_DISPUTE_AREA | Natuna Sea / Indonesian EEZ dispute area | Disputed territory | R5 | C3 | A8 | G9 | Indonesia; overlapping Chinese claim | Indonesia | YES | SIMULATED_NOT_PLAYABLE | NOT_APPLICABLE | LOCKED | UNASSIGNED |
| ENT_SEA_NEW_PEOPLE_S_ARMY | New People's Army | Civil-war or armed faction | R6 | C6 | A10 | G5 | Philippines | Philippines | YES | SIMULATED_NOT_PLAYABLE | DOES_NOT_QUALIFY | LOCKED | UNASSIGNED |
| ENT_SEA_PARACEL_ISLANDS_DISPUTE | Paracel Islands dispute | Disputed territory | R5 | C3 | A8 | G9 | China; claimed by Vietnam and Taiwan | China | YES | SIMULATED_NOT_PLAYABLE | NOT_APPLICABLE | LOCKED | UNASSIGNED |
| ENT_SEA_PHILIPPINES | Philippines | Recognized sovereign state | R1 | C1 | A1 | G1 | Philippines | Philippines | YES | START_PLAYABLE | AUTOMATIC | LOCKED | PHI |
| ENT_SEA_SCARBOROUGH_SHOAL | Scarborough Shoal | Disputed territory | R5 | C3 | A8 | G9 | Philippines; claimed by China and Taiwan | Disputed | YES | SIMULATED_NOT_PLAYABLE | NOT_APPLICABLE | LOCKED | UNASSIGNED |
| ENT_SEA_SHAN_ARMED_GROUPS | Shan armed groups | Civil-war or armed faction | R6 | C6 | A10 | G5 | Myanmar | Myanmar | YES | SIMULATED_NOT_PLAYABLE | DOES_NOT_QUALIFY | LOCKED | UNASSIGNED |
| ENT_SEA_SINGAPORE | Singapore | Recognized sovereign state | R1 | C1 | A1 | G1 | Singapore | Singapore | YES | START_PLAYABLE | AUTOMATIC | LOCKED | SGP |
| ENT_SEA_SOUTH_CHINA_SEA | South China Sea | Disputed territory | R5 | C3 | A8 | G9 | Multiple claimants | Multiple claimants | YES | SIMULATED_NOT_PLAYABLE | NOT_APPLICABLE | LOCKED | UNASSIGNED |
| ENT_SEA_SPRATLY_ISLANDS_DISPUTE | Spratly Islands dispute | Disputed territory | R5 | C3 | A8 | G9 | Multiple claimants | Multiple claimant outposts | YES | SIMULATED_NOT_PLAYABLE | NOT_APPLICABLE | LOCKED | UNASSIGNED |
| ENT_SEA_STRAIT_OF_MALACCA | Strait of Malacca | Strategic territorial status | R5 | C3 | A8 | G9 | Indonesia / Malaysia / Singapore | Indonesia / Malaysia / Singapore | YES | SIMULATED_NOT_PLAYABLE | NOT_APPLICABLE | LOCKED | UNASSIGNED |
| ENT_SEA_THAILAND | Thailand | Recognized sovereign state | R1 | C1 | A1 | G1 | Thailand | Thailand | YES | START_PLAYABLE | AUTOMATIC | LOCKED | THA |
| ENT_SEA_VIETNAM | Vietnam | Recognized sovereign state | R1 | C1 | A1 | G1 | Vietnam | Vietnam | YES | START_PLAYABLE | AUTOMATIC | LOCKED | VIE |
| ENT_SEA_WA_STATE_UNITED_WA_STATE_ARMY | Wa State / United Wa State Army | Civil-war or armed faction | R6 | C6 | A10 | G5 | Myanmar | Myanmar | YES | SIMULATED_NOT_PLAYABLE | DOES_NOT_QUALIFY | LOCKED | UNASSIGNED |
| ENT_SEA_WEST_PAPUA_PAPUAN_INDEPENDENCE_MOVEMENT | West Papua / Papuan independence movement | Separatist or resistance movement | R6 | C6 | A10 | G7 | Indonesia | Indonesia | YES | SIMULATED_NOT_PLAYABLE | DOES_NOT_QUALIFY | LOCKED | UNASSIGNED |

### Oceania (`OCE`)

| Design ID | Entity | Category | R | C | A | G | Legal sovereign / parent | Effective controller | Exists | Player | Eligibility | Decision | Tech ID |
|---|---|---|:---:|:---:|:---:|:---:|---|---|:---:|---|---|---|---|
| ENT_OCE_AMERICAN_SAMOA | American Samoa | Dependent country actor | R5 | C1 | A4 | G2 | United States | American Samoa | YES | START_PLAYABLE | QUALIFIES | LOCKED | ASM |
| ENT_OCE_AUSTRALIA | Australia | Recognized sovereign state | R1 | C1 | A1 | G1 | Australia | Australia | YES | START_PLAYABLE | AUTOMATIC | LOCKED | AST |
| ENT_OCE_BOUGAINVILLE | Bougainville | Separatist or resistance movement | R6 | C6 | A10 | G7 | Papua New Guinea | Papua New Guinea | YES | SIMULATED_NOT_PLAYABLE | DOES_NOT_QUALIFY | LOCKED | UNASSIGNED |
| ENT_OCE_CHRISTMAS_ISLAND | Christmas Island | Dependency or overseas territory | R5 | C1 | A4 | G9 | Australia | Australia | YES | SIMULATED_NOT_PLAYABLE | DOES_NOT_QUALIFY | LOCKED | UNASSIGNED |
| ENT_OCE_COCOS_KEELING_ISLANDS | Cocos (Keeling) Islands | Dependency or overseas territory | R5 | C1 | A4 | G9 | Australia | Australia | YES | SIMULATED_NOT_PLAYABLE | DOES_NOT_QUALIFY | LOCKED | UNASSIGNED |
| ENT_OCE_COOK_ISLANDS | Cook Islands | Dependency or overseas territory | R5 | C1 | A4 | G9 | New Zealand | New Zealand | YES | SIMULATED_NOT_PLAYABLE | DOES_NOT_QUALIFY | LOCKED | UNASSIGNED |
| ENT_OCE_FEDERATED_STATES_OF_MICRONESIA | Federated States of Micronesia | Recognized sovereign state | R1 | C1 | A1 | G1 | Federated States of Micronesia | Federated States of Micronesia | YES | START_PLAYABLE | AUTOMATIC | LOCKED | FSM |
| ENT_OCE_FIJI | Fiji | Recognized sovereign state | R1 | C1 | A1 | G1 | Fiji | Fiji | YES | START_PLAYABLE | AUTOMATIC | LOCKED | FIJ |
| ENT_OCE_FRENCH_POLYNESIA | French Polynesia | Dependency or overseas territory | R5 | C1 | A4 | G9 | France | France | YES | SIMULATED_NOT_PLAYABLE | DOES_NOT_QUALIFY | LOCKED | UNASSIGNED |
| ENT_OCE_GUAM | Guam | Dependency or overseas territory | R5 | C1 | A4 | G9 | United States | United States | YES | SIMULATED_NOT_PLAYABLE | DOES_NOT_QUALIFY | LOCKED | UNASSIGNED |
| ENT_OCE_KANAK_INDEPENDENCE_MOVEMENT | Kanak independence movement | Separatist or resistance movement | R6 | C6 | A10 | G7 | France/New Caledonia | France/New Caledonia | YES | SIMULATED_NOT_PLAYABLE | DOES_NOT_QUALIFY | LOCKED | UNASSIGNED |
| ENT_OCE_KIRIBATI | Kiribati | Recognized sovereign state | R1 | C1 | A1 | G1 | Kiribati | Kiribati | YES | START_PLAYABLE | AUTOMATIC | LOCKED | KIR |
| ENT_OCE_MARSHALL_ISLANDS | Marshall Islands | Recognized sovereign state | R1 | C1 | A1 | G1 | Marshall Islands | Marshall Islands | YES | START_PLAYABLE | AUTOMATIC | LOCKED | MHL |
| ENT_OCE_NAURU | Nauru | Recognized sovereign state | R1 | C1 | A1 | G1 | Nauru | Nauru | YES | START_PLAYABLE | AUTOMATIC | LOCKED | NAU |
| ENT_OCE_NEW_CALEDONIA | New Caledonia | Dependency or overseas territory | R5 | C1 | A4 | G9 | France | France | YES | SIMULATED_NOT_PLAYABLE | DOES_NOT_QUALIFY | LOCKED | UNASSIGNED |
| ENT_OCE_NEW_ZEALAND | New Zealand | Recognized sovereign state | R1 | C1 | A1 | G1 | New Zealand | New Zealand | YES | START_PLAYABLE | AUTOMATIC | LOCKED | NZL |
| ENT_OCE_NIUE | Niue | Dependency or overseas territory | R5 | C1 | A4 | G9 | New Zealand | New Zealand | YES | SIMULATED_NOT_PLAYABLE | DOES_NOT_QUALIFY | LOCKED | UNASSIGNED |
| ENT_OCE_NORFOLK_ISLAND | Norfolk Island | Dependency or overseas territory | R5 | C1 | A4 | G9 | Australia | Australia | YES | SIMULATED_NOT_PLAYABLE | DOES_NOT_QUALIFY | LOCKED | UNASSIGNED |
| ENT_OCE_NORTHERN_MARIANA_ISLANDS | Northern Mariana Islands | Dependency or overseas territory | R5 | C1 | A4 | G9 | United States | United States | YES | SIMULATED_NOT_PLAYABLE | DOES_NOT_QUALIFY | LOCKED | UNASSIGNED |
| ENT_OCE_PALAU | Palau | International administration / transitional territory | R5 | C1 | A6 | G10 | United States-administered UN trust territory | United States trust administration | YES | SIMULATED_NOT_PLAYABLE | NOT_APPLICABLE | LOCKED | UNASSIGNED |
| ENT_OCE_PAPUA_NEW_GUINEA | Papua New Guinea | Recognized sovereign state | R1 | C1 | A1 | G1 | Papua New Guinea | Papua New Guinea | YES | START_PLAYABLE | AUTOMATIC | LOCKED | PNG |
| ENT_OCE_PITCAIRN_ISLANDS | Pitcairn Islands | Dependency or overseas territory | R5 | C1 | A4 | G9 | United Kingdom | United Kingdom | YES | SIMULATED_NOT_PLAYABLE | DOES_NOT_QUALIFY | LOCKED | UNASSIGNED |
| ENT_OCE_SAMOA_WESTERN_SAMOA | Samoa / Western Samoa | Recognized sovereign state | R1 | C1 | A1 | G1 | Samoa / Western Samoa | Samoa / Western Samoa | YES | START_PLAYABLE | AUTOMATIC | LOCKED | SAM |
| ENT_OCE_SOLOMON_ISLANDS | Solomon Islands | Recognized sovereign state | R1 | C1 | A1 | G1 | Solomon Islands | Solomon Islands | YES | START_PLAYABLE | AUTOMATIC | LOCKED | SOL |
| ENT_OCE_TOKELAU | Tokelau | Dependency or overseas territory | R5 | C1 | A4 | G9 | New Zealand | New Zealand | YES | SIMULATED_NOT_PLAYABLE | DOES_NOT_QUALIFY | LOCKED | UNASSIGNED |
| ENT_OCE_TONGA | Tonga | Recognized sovereign state | R1 | C1 | A1 | G1 | Tonga | Tonga | YES | START_PLAYABLE | AUTOMATIC | LOCKED | TON |
| ENT_OCE_TUVALU | Tuvalu | Recognized sovereign state | R1 | C1 | A1 | G1 | Tuvalu | Tuvalu | YES | START_PLAYABLE | AUTOMATIC | LOCKED | TUV |
| ENT_OCE_VANUATU | Vanuatu | Recognized sovereign state | R1 | C1 | A1 | G1 | Vanuatu | Vanuatu | YES | START_PLAYABLE | AUTOMATIC | LOCKED | VAN |
| ENT_OCE_WALLIS_AND_FUTUNA | Wallis and Futuna | Dependency or overseas territory | R5 | C1 | A4 | G9 | France | France | YES | SIMULATED_NOT_PLAYABLE | DOES_NOT_QUALIFY | LOCKED | UNASSIGNED |

### North America (`NAM`)

| Design ID | Entity | Category | R | C | A | G | Legal sovereign / parent | Effective controller | Exists | Player | Eligibility | Decision | Tech ID |
|---|---|---|:---:|:---:|:---:|:---:|---|---|:---:|---|---|---|---|
| ENT_NAM_ALASKA | Alaska | Territorial or strategic status | R5 | C3 | A8 | G9 | United States | United States | YES | SIMULATED_NOT_PLAYABLE | NOT_APPLICABLE | LOCKED | UNASSIGNED |
| ENT_NAM_BERMUDA | Bermuda | Dependency or overseas territory | R5 | C1 | A4 | G9 | United Kingdom | United Kingdom | YES | SIMULATED_NOT_PLAYABLE | DOES_NOT_QUALIFY | LOCKED | UNASSIGNED |
| ENT_NAM_CANADA | Canada | Recognized sovereign state | R1 | C1 | A1 | G1 | Canada | Canada | YES | START_PLAYABLE | AUTOMATIC | LOCKED | CAN |
| ENT_NAM_CARIBBEAN_REGION | Caribbean region | Strategic territorial status | R5 | C3 | A8 | G9 | Multiple sovereigns | Multiple sovereigns | YES | SIMULATED_NOT_PLAYABLE | NOT_APPLICABLE | LOCKED | UNASSIGNED |
| ENT_NAM_CUBA | Cuba | Recognized sovereign state | R1 | C1 | A1 | G1 | Cuba | Cuba | YES | START_PLAYABLE | AUTOMATIC | LOCKED | CUB |
| ENT_NAM_FIRST_NATIONS_INDIGENOUS_SOVEREIGNTY_ISSUES | First Nations / Indigenous sovereignty issues | Non-territorial political movement | R6 | C5 | A10 | G8 | Canada/United States | Canada/United States | YES | SIMULATED_NOT_PLAYABLE | DOES_NOT_QUALIFY | LOCKED | UNASSIGNED |
| ENT_NAM_GREENLAND | Greenland | Dependent/autonomous country actor | R5 | C1 | A3 | G2 | Denmark | Greenland | YES | START_PLAYABLE | QUALIFIES | LOCKED | GRL |
| ENT_NAM_GUANTANAMO_BAY_NAVAL_BASE | Guantánamo Bay Naval Base | Occupied or leased territorial status | R5 | C4 | A7 | G9 | Cuba | United States under lease | YES | SIMULATED_NOT_PLAYABLE | NOT_APPLICABLE | LOCKED | UNASSIGNED |
| ENT_NAM_HAITI | Haiti | Recognized sovereign state | R1 | C1 | A1 | G1 | Haiti | Haiti | YES | START_PLAYABLE | AUTOMATIC | LOCKED | HAI |
| ENT_NAM_MEXICO | Mexico | Recognized sovereign state | R1 | C1 | A1 | G1 | Mexico | Mexico | YES | START_PLAYABLE | AUTOMATIC | LOCKED | MEX |
| ENT_NAM_NUNAVUT | Nunavut | Autonomous or internal region | R5 | C1 | A3 | G11 | Canada | Canada | YES | SIMULATED_NOT_PLAYABLE | DOES_NOT_QUALIFY | LOCKED | UNASSIGNED |
| ENT_NAM_PUERTO_RICO | Puerto Rico | Dependency or overseas territory | R5 | C1 | A4 | G9 | United States | United States | YES | SIMULATED_NOT_PLAYABLE | DOES_NOT_QUALIFY | LOCKED | UNASSIGNED |
| ENT_NAM_QUEBEC_SOVEREIGNTY_MOVEMENT | Quebec sovereignty movement | Separatist or resistance movement | R6 | C6 | A10 | G7 | Canada | Canada | YES | SIMULATED_NOT_PLAYABLE | DOES_NOT_QUALIFY | LOCKED | UNASSIGNED |
| ENT_NAM_SAINT_PIERRE_AND_MIQUELON | Saint Pierre and Miquelon | Dependency or overseas territory | R5 | C1 | A4 | G9 | France | France | YES | SIMULATED_NOT_PLAYABLE | DOES_NOT_QUALIFY | LOCKED | UNASSIGNED |
| ENT_NAM_UNITED_STATES | United States | Recognized sovereign state | R1 | C1 | A1 | G1 | United States | United States | YES | START_PLAYABLE | AUTOMATIC | LOCKED | USA |
| ENT_NAM_US_VIRGIN_ISLANDS | US Virgin Islands | Dependency or overseas territory | R5 | C1 | A4 | G9 | United States | United States | YES | SIMULATED_NOT_PLAYABLE | DOES_NOT_QUALIFY | LOCKED | UNASSIGNED |
| ENT_NAM_ZAPATISTA_MOVEMENT | Zapatista movement | Separatist or resistance movement | R6 | C6 | A10 | G7 | Mexico | Mexico | YES | SIMULATED_NOT_PLAYABLE | DOES_NOT_QUALIFY | LOCKED | UNASSIGNED |

### Central America and Caribbean (`CAM`)

| Design ID | Entity | Category | R | C | A | G | Legal sovereign / parent | Effective controller | Exists | Player | Eligibility | Decision | Tech ID |
|---|---|---|:---:|:---:|:---:|:---:|---|---|:---:|---|---|---|---|
| ENT_CAM_ANGUILLA | Anguilla | Dependency or overseas territory | R5 | C1 | A4 | G9 | United Kingdom | United Kingdom | YES | SIMULATED_NOT_PLAYABLE | DOES_NOT_QUALIFY | LOCKED | UNASSIGNED |
| ENT_CAM_ANTIGUA_AND_BARBUDA | Antigua and Barbuda | Recognized sovereign state | R1 | C1 | A1 | G1 | Antigua and Barbuda | Antigua and Barbuda | YES | START_PLAYABLE | AUTOMATIC | LOCKED | ATG |
| ENT_CAM_ARUBA | Aruba | Dependency or overseas territory | R5 | C1 | A4 | G9 | Netherlands | Netherlands | YES | SIMULATED_NOT_PLAYABLE | DOES_NOT_QUALIFY | LOCKED | UNASSIGNED |
| ENT_CAM_BAHAMAS | Bahamas | Recognized sovereign state | R1 | C1 | A1 | G1 | Bahamas | Bahamas | YES | START_PLAYABLE | AUTOMATIC | LOCKED | BHS |
| ENT_CAM_BARBADOS | Barbados | Recognized sovereign state | R1 | C1 | A1 | G1 | Barbados | Barbados | YES | START_PLAYABLE | AUTOMATIC | LOCKED | BRB |
| ENT_CAM_BELIZE | Belize | Recognized sovereign state | R1 | C1 | A1 | G1 | Belize | Belize | YES | START_PLAYABLE | AUTOMATIC | LOCKED | BLZ |
| ENT_CAM_BRITISH_VIRGIN_ISLANDS | British Virgin Islands | Dependency or overseas territory | R5 | C1 | A4 | G9 | United Kingdom | United Kingdom | YES | SIMULATED_NOT_PLAYABLE | DOES_NOT_QUALIFY | LOCKED | UNASSIGNED |
| ENT_CAM_CAYMAN_ISLANDS | Cayman Islands | Dependency or overseas territory | R5 | C1 | A4 | G9 | United Kingdom | United Kingdom | YES | SIMULATED_NOT_PLAYABLE | DOES_NOT_QUALIFY | LOCKED | UNASSIGNED |
| ENT_CAM_COSTA_RICA | Costa Rica | Recognized sovereign state | R1 | C1 | A1 | G1 | Costa Rica | Costa Rica | YES | START_PLAYABLE | AUTOMATIC | LOCKED | CRC |
| ENT_CAM_DOMINICA | Dominica | Recognized sovereign state | R1 | C1 | A1 | G1 | Dominica | Dominica | YES | START_PLAYABLE | AUTOMATIC | LOCKED | DMA |
| ENT_CAM_DOMINICAN_REPUBLIC | Dominican Republic | Recognized sovereign state | R1 | C1 | A1 | G1 | Dominican Republic | Dominican Republic | YES | START_PLAYABLE | AUTOMATIC | LOCKED | DOM |
| ENT_CAM_EL_SALVADOR | El Salvador | Recognized sovereign state | R1 | C1 | A1 | G1 | El Salvador | El Salvador | YES | START_PLAYABLE | AUTOMATIC | LOCKED | ELS |
| ENT_CAM_FMLN | FMLN | Non-territorial political movement | R6 | C5 | A10 | G8 | El Salvador | El Salvador | YES | SIMULATED_NOT_PLAYABLE | DOES_NOT_QUALIFY | LOCKED | UNASSIGNED |
| ENT_CAM_GRENADA | Grenada | Recognized sovereign state | R1 | C1 | A1 | G1 | Grenada | Grenada | YES | START_PLAYABLE | AUTOMATIC | LOCKED | GRD |
| ENT_CAM_GUADELOUPE | Guadeloupe | Dependency or overseas territory | R5 | C1 | A4 | G9 | France | France | YES | SIMULATED_NOT_PLAYABLE | DOES_NOT_QUALIFY | LOCKED | UNASSIGNED |
| ENT_CAM_GUATEMALA | Guatemala | Recognized sovereign state | R1 | C1 | A1 | G1 | Guatemala | Guatemala | YES | START_PLAYABLE | AUTOMATIC | LOCKED | GTM |
| ENT_CAM_HONDURAS | Honduras | Recognized sovereign state | R1 | C1 | A1 | G1 | Honduras | Honduras | YES | START_PLAYABLE | AUTOMATIC | LOCKED | HON |
| ENT_CAM_JAMAICA | Jamaica | Recognized sovereign state | R1 | C1 | A1 | G1 | Jamaica | Jamaica | YES | START_PLAYABLE | AUTOMATIC | LOCKED | JAM |
| ENT_CAM_MARTINIQUE | Martinique | Dependency or overseas territory | R5 | C1 | A4 | G9 | France | France | YES | SIMULATED_NOT_PLAYABLE | DOES_NOT_QUALIFY | LOCKED | UNASSIGNED |
| ENT_CAM_MONTSERRAT | Montserrat | Dependency or overseas territory | R5 | C1 | A4 | G9 | United Kingdom | United Kingdom | YES | SIMULATED_NOT_PLAYABLE | DOES_NOT_QUALIFY | LOCKED | UNASSIGNED |
| ENT_CAM_NETHERLANDS_ANTILLES | Netherlands Antilles | Dependency or overseas territory | R5 | C1 | A4 | G9 | Netherlands | Netherlands | YES | SIMULATED_NOT_PLAYABLE | DOES_NOT_QUALIFY | LOCKED | UNASSIGNED |
| ENT_CAM_NICARAGUA | Nicaragua | Recognized sovereign state | R1 | C1 | A1 | G1 | Nicaragua | Nicaragua | YES | START_PLAYABLE | AUTOMATIC | LOCKED | NIC |
| ENT_CAM_PANAMA | Panama | Recognized sovereign state | R1 | C1 | A1 | G1 | Panama | Panama | YES | START_PLAYABLE | AUTOMATIC | LOCKED | PAN |
| ENT_CAM_SAINT_KITTS_AND_NEVIS | Saint Kitts and Nevis | Recognized sovereign state | R1 | C1 | A1 | G1 | Saint Kitts and Nevis | Saint Kitts and Nevis | YES | START_PLAYABLE | AUTOMATIC | LOCKED | SKN |
| ENT_CAM_SAINT_LUCIA | Saint Lucia | Recognized sovereign state | R1 | C1 | A1 | G1 | Saint Lucia | Saint Lucia | YES | START_PLAYABLE | AUTOMATIC | LOCKED | LCA |
| ENT_CAM_SAINT_VINCENT_AND_THE_GRENADINES | Saint Vincent and the Grenadines | Recognized sovereign state | R1 | C1 | A1 | G1 | Saint Vincent and the Grenadines | Saint Vincent and the Grenadines | YES | START_PLAYABLE | AUTOMATIC | LOCKED | VCT |
| ENT_CAM_TRINIDAD_AND_TOBAGO | Trinidad and Tobago | Recognized sovereign state | R1 | C1 | A1 | G1 | Trinidad and Tobago | Trinidad and Tobago | YES | START_PLAYABLE | AUTOMATIC | LOCKED | TTO |
| ENT_CAM_TURKS_AND_CAICOS_ISLANDS | Turks and Caicos Islands | Dependency or overseas territory | R5 | C1 | A4 | G9 | United Kingdom | United Kingdom | YES | SIMULATED_NOT_PLAYABLE | DOES_NOT_QUALIFY | LOCKED | UNASSIGNED |
| ENT_CAM_URNG | URNG | Non-territorial political movement | R6 | C5 | A10 | G8 | Guatemala | Guatemala | YES | SIMULATED_NOT_PLAYABLE | DOES_NOT_QUALIFY | LOCKED | UNASSIGNED |

### South America (`SAM`)

| Design ID | Entity | Category | R | C | A | G | Legal sovereign / parent | Effective controller | Exists | Player | Eligibility | Decision | Tech ID |
|---|---|---|:---:|:---:|:---:|:---:|---|---|:---:|---|---|---|---|
| ENT_SAM_ARGENTINA | Argentina | Recognized sovereign state | R1 | C1 | A1 | G1 | Argentina | Argentina | YES | START_PLAYABLE | AUTOMATIC | LOCKED | ARG |
| ENT_SAM_BOLIVIA | Bolivia | Recognized sovereign state | R1 | C1 | A1 | G1 | Bolivia | Bolivia | YES | START_PLAYABLE | AUTOMATIC | LOCKED | BOL |
| ENT_SAM_BRAZIL | Brazil | Recognized sovereign state | R1 | C1 | A1 | G1 | Brazil | Brazil | YES | START_PLAYABLE | AUTOMATIC | LOCKED | BRA |
| ENT_SAM_CHILE | Chile | Recognized sovereign state | R1 | C1 | A1 | G1 | Chile | Chile | YES | START_PLAYABLE | AUTOMATIC | LOCKED | CHL |
| ENT_SAM_COLOMBIA | Colombia | Recognized sovereign state | R1 | C1 | A1 | G1 | Colombia | Colombia | YES | START_PLAYABLE | AUTOMATIC | LOCKED | COL |
| ENT_SAM_ECUADOR | Ecuador | Recognized sovereign state | R1 | C1 | A1 | G1 | Ecuador | Ecuador | YES | START_PLAYABLE | AUTOMATIC | LOCKED | ECU |
| ENT_SAM_ELN | ELN | Civil-war or armed faction | R6 | C6 | A10 | G5 | Colombia | Colombia | YES | SIMULATED_NOT_PLAYABLE | DOES_NOT_QUALIFY | LOCKED | UNASSIGNED |
| ENT_SAM_FALKLAND_ISLANDS_MALVINAS | Falkland Islands / Malvinas | Dependency or overseas territory | R5 | C1 | A4 | G9 | United Kingdom | United Kingdom | YES | SIMULATED_NOT_PLAYABLE | DOES_NOT_QUALIFY | LOCKED | UNASSIGNED |
| ENT_SAM_FARC | FARC | Civil-war or armed faction | R6 | C6 | A10 | G5 | Colombia | Colombia | YES | SIMULATED_NOT_PLAYABLE | DOES_NOT_QUALIFY | LOCKED | UNASSIGNED |
| ENT_SAM_FRENCH_GUIANA | French Guiana | Dependency or overseas territory | R5 | C1 | A4 | G9 | France | France | YES | SIMULATED_NOT_PLAYABLE | DOES_NOT_QUALIFY | LOCKED | UNASSIGNED |
| ENT_SAM_GUYANA | Guyana | Recognized sovereign state | R1 | C1 | A1 | G1 | Guyana | Guyana | YES | START_PLAYABLE | AUTOMATIC | LOCKED | GUY |
| ENT_SAM_MRTA | MRTA | Civil-war or armed faction | R6 | C6 | A10 | G5 | Peru | Peru | YES | SIMULATED_NOT_PLAYABLE | DOES_NOT_QUALIFY | REJECTED | UNASSIGNED |
| ENT_SAM_PARAGUAY | Paraguay | Recognized sovereign state | R1 | C1 | A1 | G1 | Paraguay | Paraguay | YES | START_PLAYABLE | AUTOMATIC | LOCKED | PRY |
| ENT_SAM_PERU | Peru | Recognized sovereign state | R1 | C1 | A1 | G1 | Peru | Peru | YES | START_PLAYABLE | AUTOMATIC | LOCKED | PER |
| ENT_SAM_SHINING_PATH | Shining Path | Civil-war or armed faction | R6 | C6 | A10 | G5 | Peru | Peru | YES | SIMULATED_NOT_PLAYABLE | DOES_NOT_QUALIFY | REJECTED | UNASSIGNED |
| ENT_SAM_SOUTH_GEORGIA_AND_SOUTH_SANDWICH_ISLANDS | South Georgia and South Sandwich Islands | Dependency or overseas territory | R5 | C1 | A4 | G9 | United Kingdom | United Kingdom | YES | SIMULATED_NOT_PLAYABLE | DOES_NOT_QUALIFY | LOCKED | UNASSIGNED |
| ENT_SAM_SURINAME | Suriname | Recognized sovereign state | R1 | C1 | A1 | G1 | Suriname | Suriname | YES | START_PLAYABLE | AUTOMATIC | LOCKED | SUR |
| ENT_SAM_URUGUAY | Uruguay | Recognized sovereign state | R1 | C1 | A1 | G1 | Uruguay | Uruguay | YES | START_PLAYABLE | AUTOMATIC | LOCKED | URU |
| ENT_SAM_VENEZUELA | Venezuela | Recognized sovereign state | R1 | C1 | A1 | G1 | Venezuela | Venezuela | YES | START_PLAYABLE | AUTOMATIC | LOCKED | VEN |

## Institutional Scope Boundary

No banks, development banks, trade organizations, customs unions, military alliances, or general international organizations are part of these 349 entries. The first institutional-design block identified in the Design Bible contains thirteen organization complexes: the United Nations, NATO, European Union, Commonwealth of Independent States, OSCE, OAU/African Union, ASEAN, Arab League, Gulf Cooperation Council, OPEC, NAFTA, Mercosur, and GATT/WTO. Financial institutions such as the IMF, World Bank, regional development banks, and central-bank cooperation bodies still require a separate owner-reviewed roster.
