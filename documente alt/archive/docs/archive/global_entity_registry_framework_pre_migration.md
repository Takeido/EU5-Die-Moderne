# Global Entity Registry

**Project:** EU5 Modern World Mod
**Document status:** Drive synchronization in progress
**Design phase:** World Entity Framework
**Authoritative date:** 1 January 1993
**Implementation status:** Design only
**Related document:** `EU5 Modern Day Mod > docs > design > world_entity_framework.md`

## Drive Synchronization Status

This Google Drive document currently contains the registry framework and pre-import template. It does not yet contain the full normalized 349-entry table.

The current re-review totals record **357 source rows**, **349 unique entries**, **329 LOCKED**, **0 PROVISIONAL**, **0 DEFERRED**, **20 REJECTED**, and **0 OPEN** entity-classification cases. No technical-identifier collisions remain.

Until the full table is migrated and verified here, the placeholder regional sections below are non-authoritative. The entity re-review will repopulate and confirm this Drive registry. No classification will be changed without a project-owner decision.

---

## 1. Purpose

This document is the authoritative registry of all political and territorial entities represented by the mod at the campaign start.

It consolidates the entities distributed across the regional country-list documents. The normalized table is awaiting migration and re-verification in this Drive copy.

The registry determines:

* Which entities exist at the campaign start
* What type of entity each one is
* Who legally claims each territory
* Who actually controls each territory
* Whether the entity receives direct gameplay representation
* Whether it is playable
* Which political transitions it can experience
* Which regional document contains its detailed design

Regional documents may provide additional detail, but they must not contradict this registry.

Where a conflict exists, this registry takes precedence.
Detailed country-content requirements, event-chain reminders, mechanic follow-up, and unresolved country-specific design are centralized only in `country_content_design_backlog.md`. Archived documents are read-only; synchronization and edits target only current non-archived documents.

---

## 2. Registry Authority

The global entity registry is the single authoritative source for:

* Permanent Design IDs
* Official and common names
* Canonical entity categories
* Sovereignty and recognition classes
* Territorial-control classes
* Administrative classes
* Gameplay-representation classes
* Parent-state relationships
* Sponsor relationships
* Territorial claim relationships
* Starting player availability
* Starting existence
* Cross-regional ownership
* Proposed technical identifiers
* Decision status

Country names, governments, borders, capitals, recognition, and political status may change during gameplay.

The permanent Design ID must never change.

---

## 3. Design ID Standard

Every entity must receive one permanent Design ID.

### 3.1 Format

Use:

```text
ENT_[REGION]_[NAME]
```

Examples:

```text
ENT_EUR_FRANCE
ENT_EUR_MOLDOVA
ENT_FSU_RUSSIA
ENT_MENA_PALESTINE
ENT_AFR_SOMALILAND
ENT_EAS_TAIWAN
ENT_NAM_GREENLAND
ENT_SAM_FARC
```

### 3.2 Regional codes

| Code | Region                         |
| ---- | ------------------------------ |
| EUR  | Europe                         |
| FSU  | Former Soviet Union            |
| MENA | Middle East and North Africa   |
| SSA  | Sub-Saharan Africa             |
| SAS  | South Asia                     |
| CAS  | Central Asia                   |
| EAS  | East Asia                      |
| SEA  | Southeast Asia                 |
| OCE  | Oceania                        |
| NAM  | North America                  |
| CAM  | Central America and Caribbean  |
| SAM  | South America                  |
| GLB  | Global or transregional entity |

### 3.3 ID rules

1. Every Design ID must be globally unique.
2. Design IDs must use uppercase Latin letters, numbers, and underscores only.
3. Design IDs must not contain spaces or punctuation.
4. Design IDs must describe the entity, not its current government.
5. A government change must not create a new Design ID.
6. A name change must not create a new Design ID.
7. A border change must not create a new Design ID.
8. A regime change must not create a new Design ID.
9. A complete state dissolution may create successor Design IDs.
10. Restored historical states may reuse an existing Design ID only when they are treated as the legal continuation of the same entity.
11. Armed organizations, governments in exile, and territorial administrations require separate IDs when they exist independently.
12. Proposed EU5 tags must not be used as Design IDs.

---

## 4. Required Registry Fields

Every active entry must contain the following fields.

### Identity

* Design ID
* Official name
* Common name
* Alternative names
* Regional document
* Principal region

### Classification

* Canonical category
* Recognition class
* Territorial-control class
* Administrative class
* Gameplay-representation class

### Political status

* Legal sovereign
* Parent state
* Effective controller
* Foreign sponsor
* International recognition
* International memberships
* Starting diplomatic limitations

### Territorial status

* Capital or administrative center
* Claimed territory
* Controlled territory
* Disputed territory
* Occupied territory
* External claims against the entity

### Gameplay status

* Exists at campaign start
* Player availability
* Country-actor eligibility
* Starting gameplay role
* Transition paths
* Failure or dissolution paths

### Design management

* Proposed technical identifier
* Identifier status
* Decision status
* Historical confidence
* Design notes
* Open questions
* Cross-references

---

## 5. Allowed Classification Values

### 5.1 Canonical category

Use one principal category:

* Recognized sovereign state
* Partially recognized state
* De facto state
* Dependency or overseas territory
* Associated state
* Federal constituent entity
* Autonomous region
* Occupied territory
* Disputed territory
* International administration
* Insurgent administration
* Separatist movement
* Civil-war faction
* Non-territorial political movement
* Exile government
* Transnational organization
* Background-only entity

### 5.2 Recognition class

* `R1` — Fully recognized sovereign state
* `R2` — Partially recognized state
* `R3` — Unrecognized de facto state
* `R4` — Claimed or exile government
* `R5` — Non-sovereign political entity
* `R6` — Non-state actor

### 5.3 Territorial-control class

* `C1` — Full effective control
* `C2` — Partial effective control
* `C3` — Contested control
* `C4` — External occupation
* `C5` — No territorial control
* `C6` — Mobile or irregular presence

### 5.4 Administrative class

* `A1` — Unitary national territory
* `A2` — Federal constituent entity
* `A3` — Autonomous territory
* `A4` — Dependency or overseas territory
* `A5` — Associated state
* `A6` — International administration
* `A7` — Occupied territory
* `A8` — Disputed territory
* `A9` — Separatist territory
* `A10` — No formal territorial status

### 5.5 Gameplay-representation class

* `G1` — Sovereign country actor
* `G2` — Dependent country actor
* `G3` — Autonomous regional actor
* `G4` — De facto country actor
* `G5` — Civil-war faction
* `G6` — Insurgent administration
* `G7` — Separatist movement
* `G8` — Political movement
* `G9` — Territorial status
* `G10` — Internationally administered territory
* `G11` — Event or modifier representation
* `G12` — Background-only entity

### 5.6 Player availability

* `START_PLAYABLE`
* `CONDITIONALLY_PLAYABLE`
* `RELEASABLE_PLAYABLE`
* `SIMULATED_NOT_PLAYABLE`
* `BACKGROUND_ONLY`
* `OPEN`

### 5.7 Country-actor eligibility

* `AUTOMATIC`
* `QUALIFIES`
* `BORDERLINE`
* `DOES_NOT_QUALIFY`
* `NOT_APPLICABLE`
* `OPEN`

### 5.8 Decision status

* `LOCKED`
* `PROVISIONAL`
* `OPEN`
* `DEFERRED`
* `REJECTED`

### 5.9 Historical confidence

* `HIGH`
* `MEDIUM`
* `LOW`
* `REQUIRES_RESEARCH`

---

## 6. Proposed Technical Identifier Policy

Proposed technical identifiers are design placeholders only.

They do not authorize implementation.

### Rules

1. Every proposed identifier must be globally unique.
2. The same identifier must not refer to different entities.
3. Identifiers should normally contain three uppercase letters.
4. Four-letter identifiers may be proposed where three-letter ambiguity cannot be resolved cleanly.
5. Hyphens must not be used in proposed technical identifiers.
6. Temporary suffixes such as `-X`, `-NA`, or regional notes must not appear in the final identifier.
7. Existing national abbreviations may be used where they are unambiguous.
8. Historical identifiers should not be reused for unrelated entities.
9. Movement identifiers must not collide with country identifiers.
10. Identifier approval remains provisional until the entire registry has been checked.

### Identifier status

Use:

* `UNASSIGNED`
* `PROPOSED`
* `COLLISION`
* `RESERVED`
* `APPROVED_DESIGN`
* `DEFERRED`

`APPROVED_DESIGN` means approved for the design registry. It does not mean implemented.

---

## 7. Registry Entry Template

Copy this template once for every entity.

```markdown
### ENT_REGION_ENTITY_NAME — Common Name

**Official name:**  
**Common name:**  
**Alternative names:**  
**Principal region:**  
**Regional document:**  

**Canonical category:**  
**Recognition class:**  
**Territorial-control class:**  
**Administrative class:**  
**Gameplay-representation class:**  

**Legal sovereign:**  
**Parent state:**  
**Effective controller:**  
**Foreign sponsor:**  
**International recognition:**  
**International memberships:**  
**Starting diplomatic limitations:**  

**Capital or administrative center:**  
**Claimed territory:**  
**Controlled territory:**  
**Disputed territory:**  
**Occupied territory:**  
**External claims against entity:**  

**Exists at campaign start:** YES / NO / CONDITIONAL  
**Player availability:**  
**Country-actor eligibility:**  
**Starting gameplay role:**  

**Possible transition paths:**
- 

**Failure or dissolution paths:**
- 

**Proposed technical identifier:**  
**Identifier status:**  

**Decision status:**  
**Historical confidence:**  
**Design notes:**  
**Open questions:**  
**Cross-references:**  
```

---

## 8. Entry Completion Standard

An entry is considered complete only when:

1. Its Design ID is unique.
2. Its canonical category has been assigned.
3. Legal sovereignty and effective control are separately identified.
4. Its recognition status is defined.
5. Its gameplay representation is defined.
6. Player availability is defined.
7. Its principal regional document is identified.
8. Its relevant claimants, parent states, or sponsors are recorded.
9. At least one plausible transition path is recorded where applicable.
10. Its proposed technical identifier is either unique or explicitly unassigned.
11. Open historical or design questions are clearly recorded.
12. The entry has a decision status.

An entry does not need to be locked to be considered structurally complete.

---

## 9. Registry Sections

The registry will be populated in the following order.

### Section A — Europe

Includes:

* Recognized sovereign states
* European dependencies
* Former Yugoslav entities and factions
* Cyprus-related entities
* European microstates
* European separatist and autonomy movements
* European disputed territories

### Section B — Former Soviet Union

Includes:

* Post-Soviet sovereign states
* Russian federal and autonomous entities relevant to gameplay
* Moldova internal content (Transnistria and Gagauzia)
* Georgian regional content (Abkhazia, South Ossetia, and Adjara)
* Nagorno-Karabakh as internal Azerbaijan content
* Chechen political and armed entities
* Other significant separatist administrations and movements

### Section C — Middle East and North Africa

Includes:

* Recognized sovereign states
* Palestinian entities
* Western Sahara-related entities
* Kurdish movements and administrations
* Lebanese armed and political actors where direct representation is justified
* Iraqi opposition and autonomous actors
* Gulf dependencies and disputed territories

### Section D — Sub-Saharan Africa

Includes:

* Recognized sovereign states
* Somaliland as internal Somalia content
* Civil-war factions
* Insurgent administrations
* Dependencies
* Separatist movements
* International or peacekeeping administrations where applicable

### Section E — South and Central Asia

Includes:

* Recognized sovereign states
* Afghan civil-war factions as internal Afghanistan content
* Kashmir-related entities
* Sri Lankan conflict actors
* Pakistani internal autonomy, separatism, and disputed-administration content inside Pakistan; Indian separatist movements
* Central Asian autonomous and opposition entities

### Section F — East and Southeast Asia

Includes:

* Recognized sovereign states
* Taiwan
* Hong Kong
* Macau
* Tibet
* Korean peninsula entities
* Myanmar armed and ethnic organizations
* Indonesian and Philippine separatist movements
* Territorial disputes without independent administrations

### Section G — Oceania

Includes:

* Recognized sovereign states
* Associated states
* Dependencies
* Autonomous territories
* Independence movements
* Pacific territorial arrangements

### Section H — North America

Includes:

* Recognized sovereign states
* Greenland
* Bermuda
* Caribbean dependencies administered by North American states
* Indigenous political institutions where appropriate
* Quebec and other separatist movements
* United States territories

### Section I — Central America and Caribbean

Includes:

* Recognized sovereign states
* Dependencies
* Associated territories
* Revolutionary or insurgent organizations still relevant at the campaign start
* Disputed territories

### Section J — South America

Includes:

* Recognized sovereign states
* Dependencies
* Insurgent organizations
* Peruvian insurgencies as internal Peru content
* Separatist or indigenous movements
* Disputed territories
* Transnational armed or criminal actors only where they meet representation criteria

### Section K — Global and Transregional Entities

Includes:

* Exile governments operating across regions
* Transnational armed organizations
* International administrations
* Entities whose claimed or controlled territory spans regional documents
* Global movements requiring a single authoritative entry

---

## 10. Initial Entity Register

This section will contain the migrated and verified normalized entries.

Do not place incomplete notes here.

Incomplete or disputed classifications belong in the review queue until their minimum fields have been completed.

---

# Section A — Europe

*Normalized entries pending Drive migration and re-verification.*
**Northern Cyprus decision:** Independent de facto country actor (`G4`) using `TRNC`; not a Turkish subject. Turkey guarantees its independence or provides the closest available defensive-protection relationship. International recognition remains limited to Turkey, while the Republic of Cyprus retains its claim. Detailed country-content follow-up is centralized in `country_content_design_backlog.md`. Decision status: LOCKED.

**Moldova consolidation decision:** Moldova (`MOL`) is the only starting country actor for all internationally recognized Moldovan territory, including Transnistria and Gagauzia. Neither region has a separate starting country actor, subject, or separate territorial ownership. Content follow-up is centralized in `country_content_design_backlog.md`. Decision status: LOCKED for the starting setup.

**Chechnya decision:** Chechnya begins as a separate country actor using `CHE` and the standard EU5 Vassal relationship under Russia (`RUS`). This is a temporary representation. Detailed country-content follow-up is centralized in `country_content_design_backlog.md`. Decision status: LOCKED for the temporary starting setup.

**Eritrea decision:** Eritrea begins as an independent country actor using `ERI`, with no subject relationship under Ethiopia (`ETH`). Eritrean territory is assigned directly to Eritrea at the campaign start. Detailed country-content follow-up is centralized in `country_content_design_backlog.md`. Decision status: LOCKED.

---

# Section B — Former Soviet Union

*Normalized entries pending Drive migration and re-verification.*
**Georgia regional consolidation decision:** Abkhazia, South Ossetia, and Adjara are assigned to Georgia (`GEO`) at campaign start. None has a separate starting country actor, subject, technical tag, or separate territorial ownership. Detailed follow-up is centralized in `country_content_design_backlog.md`. Decision status: LOCKED.

**Nagorno-Karabakh consolidation decision:** All Nagorno-Karabakh / Artsakh territory is assigned to Azerbaijan (`AZE`) at campaign start. Nagorno-Karabakh / Artsakh has no separate starting country actor, subject, technical identifier, or separate territorial ownership. Detailed follow-up is centralized in `country_content_design_backlog.md`. Decision status: LOCKED.

**Nakhchivan decision:** Nakhchivan begins as a separate country actor using `NAK` and the standard EU5 Vassal relationship under Azerbaijan (`AZE`). It controls the Nakhchivan exclave as an Azerbaijani subject. Detailed follow-up is centralized in `country_content_design_backlog.md`. Decision status: LOCKED.

**Tatarstan consolidation decision:** All Tatarstan territory is assigned to Russia (`RUS`) at campaign start. Tatarstan has no separate starting country actor, subject, technical identifier, or separate territorial ownership. Detailed follow-up is centralized in `country_content_design_backlog.md`. Decision status: LOCKED.

**Crimea consolidation decision:** All Crimean territory, including Sevastopol, is assigned directly to Ukraine (`UKR`) at campaign start. Crimea has no separate starting country actor, subject, technical identifier, or separate territorial ownership. Detailed follow-up is centralized in `country_content_design_backlog.md`. Decision status: LOCKED.

**Armed Islamic Group decision:** Algeria (`ALG`) remains the only starting country actor and territorial owner. The Armed Islamic Group is an internal armed organization represented through Algerian insurgency and civil-war content; it has no separate starting country actor, subject, technical identifier, or territorial ownership. Detailed follow-up is centralized in `country_content_design_backlog.md`. Decision status: LOCKED.

**Kurdish regional representation decision:** No unified Kurdish country actor begins the campaign. Kurdish-populated territory remains assigned to Iraq (`IRQ`), Turkey (`TUR`), Iran (`IRN`), and Syria (`SYR`) according to the recognized state borders. Iraqi Kurdistan and Kurdish political or armed organizations are represented through internal country content, with no separate starting country actor, subject, country tag, or territorial ownership. Detailed follow-up is centralized in `country_content_design_backlog.md`. Decision status: LOCKED.

**Western Sahara decision:** Western Sahara begins as a separate country actor using `WSA` and controls all Western Sahara territory. It uses the standard EU5 Vassal relationship under Morocco (`MOR`) under the temporary generic-subject policy. The Polisario Front is represented as internal West Saharan content and receives no separate starting actor, subject, technical identifier, or territorial ownership. Detailed follow-up is centralized in `country_content_design_backlog.md`. Decision status: LOCKED.

**Parent-state consolidation decision:** The southern Iraqi opposition is internal Iraq (`IRQ`) content; Mayotte is assigned directly to France (`FRA`); the NPFL is internal Liberia (`LBR`) content; the RUF is internal Sierra Leone (`SLE`) content; and the RPF is internal Rwanda (`RWA`) content. None of these five entries receives a separate starting country actor, subject, technical identifier, or separate territorial ownership. Detailed follow-up is centralized in `country_content_design_backlog.md`. Decision status: LOCKED for all five entries.

**Additional parent-state consolidation decision:** Réunion is assigned directly to France (`FRA`); Saint Helena, Ascension and Tristan da Cunha are assigned directly to the United Kingdom (`GBR`); the SPLA is internal Sudan (`SUD`) content; ULIMO is internal Liberia (`LBR`) content; and UNITA is internal Angola (`ANG`) content. None of these five entries receives a separate starting country actor, subject, technical identifier, or separate territorial ownership. Detailed follow-up is centralized in `country_content_design_backlog.md`. Decision status: LOCKED for all five entries.

**South Asia and Indian Ocean consolidation decision:** Azad Jammu and Kashmir and Gilgit-Baltistan are internal Pakistan (`PAK`) content; British Indian Ocean Territory / Diego Garcia is assigned directly to the United Kingdom (`GBR`); Hezb-e Islami Gulbuddin and Hezb-e Wahdat are internal Afghanistan (`AFG`) content. None of these five entries receives a separate starting country actor, subject, technical identifier, or separate territorial ownership. Detailed follow-up is centralized in `country_content_design_backlog.md`. Decision status: LOCKED for all five entries.

**Central and South Asia consolidation decision:** The precursor networks of the later Islamic Movement of Uzbekistan are internal Uzbekistan (`UZB`) content; Ittihad-i Islami, Jamiat-e Islami / the Rabbani government, and Junbish-i Milli are internal Afghanistan (`AFG`) content; and the Jammu and Kashmir government is internal India (`IND`) administration content. None of these five entries receives a separate starting country actor, subject, technical identifier, or separate territorial ownership. Detailed follow-up is centralized in `country_content_design_backlog.md`. Decision status: LOCKED for all five entries.

**South, Central, and East Asia decision:** The Liberation Tigers of Tamil Eelam are internal Sri Lanka (`LKA`) content; Northeast Indian insurgent networks are internal India (`IND`) content; the Tajik Opposition is internal Tajikistan (`TAJ`) content; and Guangxi is internal China (`CHN`) content. Hong Kong remains a separate country actor using `HKG`, controlling Hong Kong as a standard EU5 Vassal of the United Kingdom (`GBR`) under the temporary generic-subject policy. The four internal entries receive no separate starting country actor, subject, technical identifier, or separate territorial ownership. Detailed follow-up is centralized in `country_content_design_backlog.md`. Decision status: LOCKED for all five entries.

**South Lebanon security-zone decision:** Lebanon (`LEB`) remains the only starting country actor and territorial owner for all Lebanese territory, including the southern security zone. The South Lebanon Army and Israeli military presence are represented through internal Lebanon content; there is no separate starting country actor, subject, technical identifier, or territorial ownership. Detailed follow-up is centralized in `country_content_design_backlog.md`. Decision status: LOCKED.

---

# Section C — Middle East and North Africa

*Normalized entries pending Drive migration and re-verification.*

---

# Section D — Sub-Saharan Africa

*Normalized entries pending Drive migration and re-verification.*

**Somaliland consolidation decision:** Somalia (`SOM`) is the only starting country actor for all Somali territory. Somaliland receives no separate starting country actor, subject, technical tag, or separate territorial ownership. Detailed Somaliland administration, separatism, state-building, recognition, conflict, reintegration, and possible future independence paths are centralized in `country_content_design_backlog.md`. Decision status: LOCKED.

---

# Section E — South and Central Asia

*Normalized entries pending Drive migration and re-verification.*

---

# Section F — East and Southeast Asia

*Normalized entries pending Drive migration and re-verification.*

**China–Taiwan decision:** The People's Republic of China (`CHN`) and the Republic of China / Taiwan (`TWN`) are independent starting country actors. Each has claims and cores on the other's territory. Taiwan begins under a United States independence guarantee or the closest available existing EU5 defensive-protection relationship. Detailed cross-strait content is centralized in `country_content_design_backlog.md`. Decision status: LOCKED.

**China regional, Tibet, and Macau decision:** Tibet begins as a separate country actor using `TIB` and controls Tibetan territory as a standard EU5 Vassal of China (`CHN`) under the temporary generic-subject policy. Xinjiang, Inner Mongolia, and Ningxia remain internal China content with all territory assigned directly to China and no separate starting country actor, subject, technical identifier, or territorial ownership. Macau remains a separate country actor using `MAC`, controlling Macau as a standard EU5 Vassal of Portugal (`POR`). Detailed follow-up is centralized in `country_content_design_backlog.md`. The Tibetan Government-in-Exile remains separately classified. Decision status: LOCKED for all five reviewed entries.

**Southeast Asian internal-conflict consolidation decision:** The Karen National Union, Kachin Independence Organization, and Arakan / Rakhine insurgent actors are internal Myanmar (`MYA`) content; the Khmer Rouge is internal Cambodia (`CAM`) content; and the New People's Army is internal Philippines (`PHI`) content. None of these five entries receives a separate starting country actor, subject, technical identifier, or territorial ownership. Detailed follow-up is centralized in `country_content_design_backlog.md`. Decision status: LOCKED for all five entries.

**Additional Myanmar internal-conflict consolidation decision:** Shan armed groups and United Wa State Army / Wa State are internal Myanmar (`MYA`) content. Myanmar remains the only starting country actor and territorial owner; neither entry receives a separate starting country actor, subject, technical identifier, or territorial ownership. Detailed follow-up is centralized in `country_content_design_backlog.md`. Decision status: LOCKED for both entries.
**Final East Asian territorial-dispute decision:** The Senkaku / Diaoyu Islands are assigned to Japan (`JAP`) at campaign start. China (`CHN`) and Taiwan (`TWN`) retain territorial claims. The islands receive no separate starting country actor, subject, technical identifier, or territorial ownership. Detailed follow-up is centralized in `country_content_design_backlog.md`. Decision status: LOCKED.
---

# Section G — Oceania

*Normalized entries pending Drive migration and re-verification.*

**Pacific dependency representation decision:** American Samoa begins as a separate country actor using `ASM` and controls American Samoa as a standard EU5 Vassal of the United States (`USA`) under the temporary generic-subject policy. Bougainville is internal Papua New Guinea (`PNG`) content. Christmas Island, the Cocos (Keeling) Islands, and Norfolk Island are assigned directly to Australia (`AST`); New Caledonia, French Polynesia, and Wallis and Futuna directly to France (`FRA`); Guam and the Northern Mariana Islands directly to the United States (`USA`); the Cook Islands, Niue, and Tokelau directly to New Zealand (`NZL`); and the Pitcairn Islands directly to the United Kingdom (`GBR`). Except for American Samoa, none of these reviewed entries receives a separate starting country actor, subject, technical identifier, or territorial ownership. Palau's existing locked transitional classification remains unchanged. Detailed follow-up is centralized in `country_content_design_backlog.md`. Decision status: LOCKED for all fourteen reviewed Oceania entries.
---

# Section H — North America

*Normalized entries pending Drive migration and re-verification.*

---

# Section I — Central America and Caribbean

*Normalized entries pending Drive migration and re-verification.*

---

# Section J — South America

*Normalized entries pending Drive migration and re-verification.*

**South Georgia and South Sandwich Islands decision:** South Georgia and the South Sandwich Islands are assigned directly to the United Kingdom (`GBR`) at campaign start. Argentina (`ARG`) retains its territorial claim. The territory receives no separate starting country actor, subject, technical identifier, or territorial ownership. Detailed follow-up is centralized in `country_content_design_backlog.md`. Decision status: LOCKED.
---

# Section K — Global and Transregional Entities

*Normalized entries pending Drive migration and re-verification.*

---

## 11. Classification Review Queue

Use this section for entities that require additional design or historical research.

| Entity       | Region | Main question | Current proposal | Status |
| ------------ | ------ | ------------- | ---------------- | ------ |

| None | — | — | — | — |

An entity should leave this queue once the necessary decision has been recorded in its full registry entry.

---

## 12. Identifier Collision Register

All proposed-identifier collisions are resolved. The `MAC`, `MOR`, `JAM`, `SLV`, `SND`, and former `SEN` collisions have recorded resolutions.

| Identifier | Entity 1     | Entity 2                     | Resolution                                                     | Status      |
| ---------- | ------------ | ---------------------------- | -------------------------------------------------------------- | ----------- |
| MAC        | Macau        | Macedonia                    | Macau retains `MAC`; Macedonia reassigned to `MKD`             | RESOLVED    |
| MOR        | Morocco      | Moro separatist entities     | Morocco retains `MOR`; Moro separatism is internal Philippines content without a country identifier | RESOLVED    |
| JAM        | Jamaica      | Jamiat-e Islami              | Jamaica retains `JAM`; Jamiat and other Afghan factions are internal Afghanistan content without country identifiers | RESOLVED    |
| SLV        | Slovenia     | El Salvador                  | Slovenia retains `SLV`; El Salvador reassigned to `ESV`; Slovakia remains `SVK` | RESOLVED    |
| SEN        | Senegal      | Senkaku Islands concept      | Territorial dispute receives no country identifier             | RESOLVED    |
| SND        | Shining Path | Sindhi nationalist movements | Both are internal parent-country content: Shining Path and MRTA are folded into Peru; Sindhi and other Pakistan-internal entities are folded into Pakistan. No country identifier is assigned. | RESOLVED    |

### Collision-resolution priorities

Resolve collisions using this order:

1. Preserve widely recognized modern country abbreviations where practical.
2. Remove technical country identifiers from territorial disputes that are not country actors.
3. Assign movement-specific identifiers to non-state organizations.
4. Use historically meaningful alternatives.
5. Use four-letter identifiers when no clear three-letter solution exists.
6. Never distinguish two entities only by punctuation or capitalization.

---

## 13. Duplicate and Cross-Regional Register

Use this section when an entity appears in more than one regional document.

| Entity       | Authoritative region | Other references | Required action | Status |
| ------------ | -------------------- | ---------------- | --------------- | ------ |
| None entered | —                    | —                | —               | —      |

### Cross-regional rule

Every entity receives one authoritative registry entry.

Other regions may reference the entity but must not create a second independent entry.

---

## 14. Territorial Dispute Register

Territorial disputes that do not qualify as political entities should be recorded here rather than entered as countries.

| Dispute                | Claimants            | Current controller | Separate administration | Representation proposal | Status      |
| ---------------------- | -------------------- | ------------------ | ----------------------- | ----------------------- | ----------- |
| Senkaku/Diaoyu Islands | Japan, China, Taiwan | Japan              | No                      | Internal Japanese territory with Chinese and Taiwanese claims | LOCKED |

Additional disputes will be added during regional normalization.

---

## 15. Dependencies and Autonomous Territories Register

This index records entities requiring a decision between direct actor representation and parent-state representation.

| Entity       | Parent state | Current status | Proposed representation | Player availability | Status |
| ------------ | ------------ | -------------- | ----------------------- | ------------------- | ------ |
| Faroe Islands | Denmark | Autonomous territory | Standard EU5 Vassal subject (`G2`) | CONDITIONALLY_PLAYABLE | LOCKED |
| Greenland | Denmark | Autonomous territory | Standard EU5 Vassal subject (`G2`) | CONDITIONALLY_PLAYABLE | LOCKED |
| Åland | Finland | Autonomous demilitarized region | Part of Finland; no separate country or subject (`G11`) | SIMULATED_NOT_PLAYABLE | LOCKED |
| Serbia | Federal Republic of Yugoslavia | Federal constituent republic | Part of the single starting Yugoslav country; separate tag exists only as a releasable | RELEASABLE_PLAYABLE | LOCKED |
| Montenegro | Federal Republic of Yugoslavia | Federal constituent republic | Part of the single starting Yugoslav country; separate tag exists only as a releasable | RELEASABLE_PLAYABLE | LOCKED |
| Kosovo | Federal Republic of Yugoslavia | Autonomous and disputed territory represented separately for gameplay | Standard EU5 Vassal subject (`G2`) using `KOS`; temporary setup with detailed follow-up centralized in `country_content_design_backlog.md` | OPEN — see backlog | LOCKED |
| Nakhchivan | Azerbaijan | Autonomous republic and exclave | Standard EU5 Vassal subject (`G2`) using `NAK` | OPEN — see backlog | LOCKED |
| Hong Kong | United Kingdom | British dependent territory | Standard EU5 Vassal subject (`G2`) using `HKG`; controls Hong Kong under `GBR` | OPEN — see backlog | LOCKED |
| Macau | Portugal | Portuguese dependent territory | Standard EU5 Vassal subject (`G2`) using `MAC`; controls Macau under `POR` | OPEN — see backlog | LOCKED |
| Tibet | China | Autonomous subject territory | Standard EU5 Vassal subject (`G2`) using `TIB`; controls Tibetan territory under `CHN` | OPEN — see backlog | LOCKED |

| American Samoa | United States | United States dependent territory represented separately | Standard EU5 Vassal subject (`G2`) using `ASM`; controls American Samoa under `USA` | OPEN — see backlog | LOCKED |
---

## 16. Non-State Actor Register

This index records movements, factions, insurgencies, and exile organizations.

| Entity       | Operating territory | Main objective | Territorial control | Proposed representation | Status |
| ------------ | ------------------- | -------------- | ------------------- | ----------------------- | ------ |
| Afghan civil-war factions | Afghanistan | Contest government and regional control | Varied and changing within Afghanistan | Folded into Afghanistan (`AFG`); content follow-up is centralized in `country_content_design_backlog.md` | REJECTED AS SEPARATE ENTITIES |
| Pakistan internal entities | Pakistan | Autonomy, separatism, disputed administration, and regional security | Internal or locally administered areas within Pakistan | Folded into Pakistan (`PAK`); content follow-up is centralized in `country_content_design_backlog.md` | REJECTED AS SEPARATE ENTITIES |
| Peru internal insurgencies | Peru | Revolutionary insurgency and state counterinsurgency | Irregular presence within Peru | Folded into Peru (`PER`); content follow-up is centralized in `country_content_design_backlog.md` | REJECTED AS SEPARATE ENTITIES |

| Republic of Serbian Krajina | Croatia | Former separatist wartime authority | No separate territorial control in the mod setup | Folded entirely into Croatia (`CRO`); no country actor, technical tag, subject, or releasable. Content follow-up is centralized in `country_content_design_backlog.md`. | REJECTED AS SEPARATE ENTITY |
| Republika Srpska | Bosnia and Herzegovina | Former Bosnian Serb wartime authority | No separate territorial control in the mod setup | Folded entirely into Bosnia and Herzegovina (`BOS`); no country actor, technical tag, subject, releasable, or separate territorial ownership. Content follow-up is centralized in `country_content_design_backlog.md`. | REJECTED AS SEPARATE ENTITY |
| Croatian Republic of Herzeg-Bosnia | Bosnia and Herzegovina | Former Bosnian Croat wartime authority | No separate territorial control in the mod setup | Folded entirely into Bosnia and Herzegovina (`BOS`); no country actor, technical tag, subject, releasable, or separate territorial ownership. Content follow-up is centralized in `country_content_design_backlog.md`. | REJECTED AS SEPARATE ENTITY |
---

## 17. Registry Normalization Procedure

Every regional roster must be processed using the following procedure.

### Step 1 — Import

Copy every named entity from the regional document into a temporary review list.

Do not exclude questionable entries during import.

### Step 2 — Deduplicate

Check whether the entity already exists:

* In another section of the same regional document
* In another regional document
* Under an alternative name
* As both a territory and a political movement
* As both a parent state and a faction
* As both a historic and contemporary entity

### Step 3 — Assign Design ID

Create one permanent Design ID.

### Step 4 — Assign canonical category

Determine what the entity actually is at the campaign start.

### Step 5 — Separate law from control

Record:

* Legal sovereign
* Parent state
* Effective controller
* Territorial claimants

### Step 6 — Select gameplay representation

Determine whether the entity should be:

* A full country actor
* A dependent actor
* An autonomous region
* A de facto state
* A civil-war faction
* An insurgent administration
* A separatist movement
* A territorial status
* An event or modifier
* Background only

### Step 7 — Determine playability

Record whether the entity is playable at the start, conditionally playable, releasable, simulated but unavailable, or background only.

### Step 8 — Define transitions

Identify the plausible ways its status can change during the campaign.

### Step 9 — Review identifiers

Check for collisions and remove identifiers from entries that do not require country-level representation.

### Step 10 — Assign decision status

Mark the result as locked, provisional, open, deferred, or rejected.

### Step 11 — Update regional document

Replace independent classification claims in the regional document with a reference to the registry entry.

---

## 18. Regional Document Reference Format

Once an entity is registered, regional documents should use this compact format:

```markdown
### Common Name

**Registry ID:** `ENT_REGION_ENTITY_NAME`  
**Registry status:** LOCKED / PROVISIONAL / OPEN  
**Regional significance:**  
**Country-specific design:**  
```

Regional documents should not repeat all registry fields.

They should focus on:

* Regional importance
* Starting conditions
* Domestic design
* Foreign relations
* Conflict systems
* Country objectives
* Events
* Alternate paths

---

## 19. Locked Registry Policies

The following registry policies are locked:

1. The authoritative campaign start date is 1 January 1993.
2. All starting governments, borders, wars, alliances, occupations, territorial control, recognition statuses, and international memberships must represent conditions at the beginning of 1 January 1993.
3. The campaign has no fixed historical end date.
4. Reaching the end of currently designed historical content must not terminate the campaign.
5. Historical, technological, political, economic, and speculative content will continue to be expanded without a predetermined final content year until the project owner decides that the planned design is sufficient.
6. Entity transitions and global systems must support indefinite dynamic play beyond all authored historical content.
7. The registry is the authoritative source for entity classifications.
8. Every entity receives one unique permanent Design ID.
9. Design IDs remain separate from technical country identifiers.
10. Every recognized sovereign state receives an entry.
11. Recognized sovereign microstates receive entries.
12. Legal sovereignty and effective control are recorded separately.
13. Recognition and territorial control are recorded separately.
14. Territorial disputes without independent administrations are not countries.
15. Separatist movements without territorial governments are not automatically countries.
16. Autonomous status does not automatically grant country-actor status.
17. Dependencies are evaluated individually.
18. Unresolved unrecognized separatist administrations within a recognized parent state default to parent-state ownership and internal country content. A separate starting actor requires explicit project-owner approval. Existing locked exceptions remain unchanged.
19. Player availability is separate from entity existence.
20. Every proposed technical identifier must be globally unique.
21. Every cross-regional entity has one authoritative entry.
22. All unresolved cases must be visible in the review queue.
23. Regional documents must eventually reference rather than contradict the registry.
24. No implementation work begins as part of registry creation.
25. Use existing EU5 country and subject types wherever possible; custom entity or subject types require explicit project-owner approval.
26. Detailed country-content follow-up belongs only in `country_content_design_backlog.md`; registry and roster documents retain starting representation decisions and short cross-references.
27. Archived documents are read-only and are not synchronization or update targets.

28. Within the reviewed Pacific dependency block, non-sovereign island territories are represented directly within their administering state unless the project owner explicitly approves an exception. American Samoa is the locked exception as a United States Vassal; Palau's already locked transitional classification remains unchanged.
---

## 20. Completion Criteria

The global entity registry is complete when:

* Every entity from every regional roster has been reviewed.
* Every recognized sovereign state has a registry entry.
* Every dependency and autonomous territory has a recorded representation decision.
* Every de facto or partially recognized state has a recorded status.
* Every civil-war faction and insurgent organization has been classified.
* Territorial disputes have been separated from political entities.
* Duplicate entries have been removed.
* Cross-regional entities have one authoritative entry.
* Every Design ID is unique.
* Every proposed technical identifier is unique or explicitly unassigned.
* Player availability has been determined.
* Open questions have been listed.
* All classifications have been reviewed for consistency.
* The 1993 world roster has been formally locked.
