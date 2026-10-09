# World Entity Framework

**Project:** EU5 Modern World Mod
**Document status:** Draft 0.1
**Design phase:** World Entity Framework
**Applies to:** All regions and all campaign dates
**Implementation status:** Design only; no implementation decisions are made by this document

---

## 1. Purpose

This document defines how the mod classifies and represents states, territories, dependencies, disputed regions, de facto governments, autonomous regions, separatist movements, insurgencies, and civil-war factions.

It is the authoritative framework for deciding what each entity in the global country roster represents.

The framework must be applied consistently across every regional country-list document before detailed country design begins.

This document does not determine technical EU5 implementation. It determines the intended gameplay role and political status of each entity. Technical implementation will be considered only after Design Freeze.

---

## 2. Core Design Rule

The following concepts must always be treated separately:

1. **Legal sovereignty**
2. **International recognition**
3. **Territorial control**
4. **Domestic constitutional status**
5. **Political organization**
6. **Gameplay representation**
7. **Player availability**

An entity controlling territory is not automatically a recognized state.

A recognized state does not necessarily control all territory legally belonging to it.

An autonomous region is not automatically a separatist state.

A separatist movement is not automatically a territorial government.

A disputed territory is not automatically an independent political actor.

Every entity record must answer these questions:

* Who is internationally recognized as the legal sovereign?
* Who actually controls the territory?
* Does the entity possess a functioning territorial administration?
* How widely is the entity recognized?
* Is it constitutionally part of another state?
* Does it possess independent political or military leadership?
* How should it be represented in gameplay?
* Should it be selectable by the player at campaign start?
* What political transitions can change its status?

---

## 3. Authoritative Classification Axes

Every entity must be classified across four independent axes.

### 3.1 Sovereignty and Recognition

This axis describes the entity’s international legal and diplomatic position.

| Code | Classification                   | Definition                                                                                                |
| ---- | -------------------------------- | --------------------------------------------------------------------------------------------------------- |
| R1   | Fully recognized sovereign state | A sovereign state with broad international recognition and normal diplomatic participation                |
| R2   | Partially recognized state       | A self-governing state recognized by some governments but lacking broad international recognition         |
| R3   | Unrecognized de facto state      | A territorial state administration with effective independence but little or no international recognition |
| R4   | Claimed or exile government      | A government claiming sovereignty without stable control of its claimed territory                         |
| R5   | Non-sovereign political entity   | An entity that does not claim or possess normal sovereign statehood                                       |
| R6   | Non-state actor                  | A political, military, social, or ideological organization that is not a territorial state                |

Recognition must not be reduced to a simple yes-or-no status.

Where relevant, recognition should be tracked through:

* Recognition by the parent or claimant state
* Recognition by neighboring states
* Recognition by major powers
* Recognition by international organizations
* General international recognition
* Diplomatic isolation
* Informal relations without formal recognition

---

### 3.2 Territorial Control

This axis describes control at the campaign start.

| Code | Classification               | Definition                                                                                               |
| ---- | ---------------------------- | -------------------------------------------------------------------------------------------------------- |
| C1   | Full effective control       | The entity controls nearly all territory it claims                                                       |
| C2   | Partial effective control    | The entity controls only part of its claimed territory                                                   |
| C3   | Contested control            | Control is actively disputed through war, insurgency, or competing administrations                       |
| C4   | External occupation          | The territory is controlled by a foreign state or military administration                                |
| C5   | No territorial control       | The entity exists politically but does not administer territory                                          |
| C6   | Mobile or irregular presence | The entity operates through dispersed bases, cells, or temporary zones rather than stable administration |

Territorial control and legal ownership must be recorded separately.

A state may legally own a territory while another entity controls it.

A military occupation must not automatically transfer legal sovereignty.

---

### 3.3 Constitutional and Administrative Status

This axis describes the entity’s formal relationship with a larger state.

| Code | Classification                   | Definition                                                                             |
| ---- | -------------------------------- | -------------------------------------------------------------------------------------- |
| A1   | Unitary national territory       | An ordinary administrative part of a unitary sovereign state                           |
| A2   | Federal constituent entity       | A constitutionally recognized member of a federation                                   |
| A3   | Autonomous territory             | A region possessing legally defined self-government                                    |
| A4   | Dependency or overseas territory | A non-sovereign territory constitutionally subordinate to another state                |
| A5   | Associated state                 | A self-governing entity linked to another state through a formal association agreement |
| A6   | International administration     | A territory administered or supervised by an international institution                 |
| A7   | Occupied territory               | A territory under foreign control without an accepted transfer of sovereignty          |
| A8   | Disputed territory               | Territory claimed by two or more political entities                                    |
| A9   | Separatist territory             | Territory claimed by a movement seeking independence or union with another state       |
| A10  | No formal territorial status     | Used for non-territorial movements and organizations                                   |

An entity can have more than one relevant status.

For example, a territory may be legally autonomous, internationally disputed, and partially controlled by a separatist administration.

---

### 3.4 Gameplay Representation

This axis determines the entity’s design-level gameplay form.

| Code | Representation                         | Intended use                                                                                          |
| ---- | -------------------------------------- | ----------------------------------------------------------------------------------------------------- |
| G1   | Sovereign country actor                | Full diplomatic, political, economic, and military actor                                              |
| G2   | Dependent country actor                | Distinct territorial actor with restricted sovereignty or a parent-state relationship                 |
| G3   | Autonomous regional actor              | Internal entity with meaningful self-government but no normal independent diplomacy                   |
| G4   | De facto country actor                 | Territorial state actor whose practical independence exceeds its international recognition            |
| G5   | Civil-war faction                      | Organized contender for control of an existing state                                                  |
| G6   | Insurgent administration               | Armed movement that governs stable territory but is not yet treated as a normal state                 |
| G7   | Separatist movement                    | Independence or secession movement represented primarily through internal politics and unrest         |
| G8   | Political movement                     | Non-territorial ideological, ethnic, religious, or political organization                             |
| G9   | Territorial status                     | Territory represented through ownership, control, claims, autonomy, occupation, or dispute rules      |
| G10  | Internationally administered territory | Territory governed through a special international arrangement                                        |
| G11  | Event or modifier representation       | Entity represented indirectly because direct political representation would add little gameplay value |
| G12  | Background-only entity                 | Recorded for historical completeness but not actively simulated                                       |

Gameplay representation does not automatically determine technical implementation.

---

## 4. Canonical Entity Categories

Each entity must receive one principal canonical category.

### 4.1 Recognized Sovereign State

A recognized sovereign state is the default full country actor.

Recognized sovereign states should normally possess:

* A national government
* A defined capital
* A resident population
* Recognized territory
* Independent diplomatic relations
* National economic policy
* Armed forces or security institutions
* Membership or participation in international organizations

### Locked policy

Every generally recognized sovereign state existing at the campaign start should be represented as a country actor.

This includes recognized sovereign microstates.

Microstates must not be removed merely because of their physical size. Where geographic scale creates difficulties, territorial representation may be abstracted, but their sovereignty and diplomatic role should remain represented.

---

### 4.2 Partially Recognized State

A partially recognized state claims sovereign independence and exercises substantial self-government but lacks broad recognition.

Its gameplay should emphasize:

* Recognition campaigns
* Diplomatic isolation
* Dependence on foreign sponsors
* Trade and travel restrictions
* Security guarantees
* Parent-state claims
* Reintegration or negotiated settlement
* Risk of blockade or intervention

Partially recognized states may be playable when they possess a functioning government and meaningful strategic choices.

---

### 4.3 De Facto State

A de facto state controls territory and operates state institutions without broad international recognition.

A de facto state should normally qualify as a country actor when it has:

* Stable territorial control
* A permanent administrative center
* A functioning political leadership
* Independent security or military forces
* A population governed by its institutions
* A demonstrated ability to survive independently
* A meaningful role in regional politics

A de facto state does not need to meet every condition, but direct country representation should produce more useful gameplay than representing it as unrest or a temporary rebel faction.

Its design should distinguish:

* Practical independence
* International recognition
* Legal claims
* Foreign sponsorship
* Economic dependency
* Military dependency
* Negotiation with the parent state

---

### 4.4 Dependency or Overseas Territory

A dependency is governed under the sovereignty of another state but possesses a distinct territorial, legal, cultural, economic, or administrative identity.

A dependency may be represented as a dependent country actor when it has several of the following:

* A separate local government
* A distinct legal status
* A substantial resident population
* A separate economic or customs system
* Strategic military importance
* A plausible independence or integration path
* Distinct diplomatic relevance
* Meaningful internal political choices

Smaller dependencies without sufficient independent gameplay should be represented through regional status, autonomy, or parent-state mechanics.

Dependencies must not automatically conduct normal independent diplomacy.

Possible long-term outcomes include:

* Continued dependency
* Greater autonomy
* Free association
* Full integration
* Negotiated independence
* Unilateral independence
* Transfer to another sovereign state

---

### 4.5 Federal Constituent Entity

A federal constituent entity is an internal political unit protected or recognized by a federal constitution.

Federal units should not normally be treated as independent countries.

They may require direct regional representation when:

* They possess constitutionally significant powers
* Their leadership influences national politics
* They maintain separate security institutions
* They have strong separatist or sovereignty movements
* Their relationship with the federal government is central to gameplay
* Federal collapse is a plausible campaign outcome

Federal units should normally act through autonomy, domestic politics, and constitutional conflict rather than normal foreign diplomacy.

---

### 4.6 Autonomous Region

An autonomous region has legally recognized self-government within a sovereign state.

Autonomous regions should normally be represented through:

* Regional autonomy
* Local political leadership
* Cultural or linguistic rights
* Fiscal arrangements
* Regional institutions
* Local security powers
* Separatist pressure
* Negotiations with the central government

Autonomous status alone does not justify country-actor representation.

An autonomous region may become a country actor through:

* Constitutional separation
* Successful secession
* State collapse
* Foreign intervention
* Referendum
* Negotiated independence
* Transformation into a de facto state

---

### 4.7 Occupied Territory

An occupied territory is controlled by a political or military actor other than the entity recognized as its legal sovereign.

Occupation must track:

* Legal sovereign
* Current controller
* Civil administration
* Military presence
* Resistance
* International recognition
* Humanitarian conditions
* Negotiation status
* Annexation claims

Occupation must not immediately produce accepted sovereignty.

Prolonged occupation may lead to:

* Withdrawal
* Restored sovereignty
* International administration
* Negotiated territorial transfer
* Unrecognized annexation
* Recognized annexation
* Independence
* Continuing frozen conflict

---

### 4.8 Disputed Territory

A disputed territory is land or maritime space claimed by multiple entities.

A disputed territory is not a country merely because it has multiple claimants.

It should normally be represented through:

* Competing claims
* Diplomatic tension
* Military presence
* Access restrictions
* Resource rights
* Negotiation
* Arbitration
* Demilitarization
* Escalation risk

A disputed territory should receive a separate country actor only when it also possesses a distinct territorial government or organized political community acting independently of the claimants.

Uninhabited islands, maritime claims, and border zones should never be treated as countries solely for roster completeness.

---

### 4.9 International Administration

An internationally administered territory is governed, supervised, or protected by an international institution or multinational arrangement.

Its design may include:

* Mandate legitimacy
* Peacekeeping forces
* Local provisional government
* Refugee return
* Reconstruction
* Elections
* Constitutional negotiations
* Transfer of authority
* Independence referendum
* Reintegration with a claimant state

International administrations should be temporary or transitional unless the campaign creates conditions that prolong them.

---

### 4.10 Insurgent Administration

An insurgent administration is an armed movement that controls territory and performs some functions of government.

It differs from a de facto state because its institutions, territorial control, or political durability remain limited or unstable.

Direct territorial representation is appropriate when the movement:

* Holds identifiable territory
* Governs a resident population
* Collects revenue or resources
* Maintains armed forces
* Possesses a leadership structure
* Conducts negotiations or foreign relations
* Can plausibly win, lose, fragment, or transform into a state

Possible transitions include:

* Defeat
* Peace agreement
* Autonomy
* Participation in national government
* Transformation into a recognized opposition
* Establishment of a de facto state
* Successful national takeover
* Fragmentation into rival factions

---

### 4.11 Separatist Movement

A separatist movement seeks independence, autonomy, or union with another state but does not necessarily control stable territory.

It should normally be represented through:

* Regional political support
* Organization strength
* Popular legitimacy
* Militancy
* Foreign support
* Government repression
* Negotiation
* Autonomy demands
* Referendums
* Insurgency risk

A separatist movement should not become a country actor until it acquires a territorial administration or achieves a formal political settlement.

---

### 4.12 Civil-War or Rebel Faction

A civil-war faction competes for control of an existing state or seeks to replace its government.

Civil-war factions should be distinguished from separatists.

A civil-war faction may seek:

* Control of the national government
* Regime change
* Ideological revolution
* Restoration of a former government
* Military rule
* Regional control
* Partition
* Secession

Civil-war factions should have:

* A political objective
* Leadership
* Territorial or organizational strength
* Sources of support
* Foreign relationships
* Victory and defeat conditions
* Rules for fragmentation or coalition-building

They should not be treated as ordinary permanent states unless they create a durable territorial government.

---

### 4.13 Non-Territorial Movement

Non-territorial movements include political organizations, ideological networks, ethnic advocacy movements, religious movements, exile organizations, and transnational armed groups without stable territorial government.

They should be represented through:

* Political influence
* Support networks
* Funding
* Public sympathy
* Recruitment
* Foreign sponsorship
* Terrorism or armed activity where relevant
* Negotiations
* Legalization or prohibition
* Integration into formal politics
* Suppression or fragmentation

They should not receive territorial country representation merely because they are historically important.

---

## 5. Country-Actor Eligibility Test

Recognized sovereign states automatically qualify as country actors.

Other entities should be evaluated using the following criteria:

1. Does the entity control identifiable territory?
2. Does it govern a resident population?
3. Does it possess an organized and durable government?
4. Does it maintain independent security or military forces?
5. Does it conduct meaningful external relations?
6. Does it pursue policies independently of a parent state?
7. Is its continued existence a significant regional issue?
8. Would direct representation create meaningful player decisions?

### Decision guideline

* **Six or more criteria:** Normally represent as a country actor.
* **Four or five criteria:** Consider a de facto actor, dependent actor, or insurgent administration.
* **Two or three criteria:** Normally represent as an autonomous region, movement, faction, or territorial status.
* **Zero or one criterion:** Normally use event, modifier, claim, or background representation.

This test is a design guideline, not a mathematical rule. Historically and strategically important exceptions may be approved through the decision log.

---

## 6. Player Availability

### Normally playable

* Fully recognized sovereign states
* Partially recognized states with functioning governments
* Durable de facto states
* Dependencies with substantial self-government and meaningful political paths

### Conditionally playable

* Insurgent administrations controlling meaningful territory
* Civil-war factions in active conflict scenarios
* International administrations
* Federal entities during constitutional crises
* Autonomous regions with developed independence paths

### Normally not directly playable

* Ordinary administrative regions
* Territorial disputes without their own government
* Separatist movements without territorial control
* Temporary rebel groups
* Exile organizations
* Uninhabited disputed islands
* Maritime claims
* Background-only political movements

Player availability must be recorded independently from entity classification.

An entity may exist in the simulation without being selectable at campaign start.

---

## 7. Claims, Control, and Sovereignty

The mod must treat the following as separate concepts:

* **Recognized sovereignty:** Who international actors generally consider the legal owner
* **Constitutional ownership:** Which state claims the territory under domestic law
* **Territorial claim:** Which entities formally demand the territory
* **Effective control:** Which entity currently administers or occupies it
* **Popular preference:** What the local population supports
* **International position:** Whether outside actors support, reject, or avoid taking a position

A change in one category must not automatically change all others.

For example:

* Military occupation changes effective control.
* Annexation claims change the claimant’s legal position.
* Recognition changes diplomatic treatment.
* A peace treaty may change recognized sovereignty.
* A referendum may affect popular legitimacy.
* None of these individually guarantees universal acceptance.

---

## 8. Recognition

Recognition should be a diplomatic process rather than a permanent label.

Recognition decisions may be influenced by:

* Relations with the parent state
* Relations with the breakaway entity
* Great-power pressure
* Regional organizations
* International law
* Military control
* Democratic legitimacy
* Peace agreements
* Human-rights conditions
* Strategic interests
* Economic interests
* Previous recognition commitments

Recognition may produce:

* Formal diplomatic relations
* Access to international organizations
* Trade opportunities
* Financial access
* Arms purchases
* Security guarantees
* Legitimacy
* Sanctions from opposing states
* Deteriorating relations with the claimant state

Derecognition must also be possible under exceptional circumstances.

---

## 9. Independence and Secession

Independence should not occur through a single generic action.

Possible independence paths include:

* Negotiated independence
* Constitutional referendum
* Decolonization
* Federal dissolution
* Peace agreement
* Successful separatist war
* State collapse
* Foreign-imposed settlement
* Unilateral declaration followed by de facto survival
* Internationally supervised transition

Independence outcomes must separately determine:

* Territorial control
* Recognition
* Borders
* Citizenship
* Armed forces
* State assets
* Debt
* Currency
* International membership
* Security guarantees
* Foreign military presence
* Refugees and displaced populations

---

## 10. Annexation and Integration

Military control must not create immediate, universally accepted annexation.

Possible territorial outcomes include:

* Temporary occupation
* Military administration
* Puppet or dependent government
* Unrecognized annexation
* Partially recognized annexation
* Internationally recognized territorial transfer
* Reintegration with an existing state
* Creation of an autonomous territory
* Creation of an independent state
* International administration

Integration should require time, administrative capacity, political acceptance, and control.

Resistance should be influenced by:

* Local identity
* Previous sovereignty
* Cultural and linguistic differences
* Conduct during occupation
* Economic conditions
* International support
* Forced displacement
* Local political institutions
* Security conditions

---

## 11. State Collapse

State collapse must not automatically delete a country.

Possible consequences include:

* Loss of central authority
* Regional autonomy
* Rival governments
* Military factions
* Separatist administrations
* Foreign intervention
* International peacekeeping
* Humanitarian crisis
* Refugee flows
* Informal economies
* Criminal or militant control
* Negotiated reconstruction
* Federalization
* Partition
* Restoration of central authority

A collapsed state may remain internationally recognized even while lacking effective control.

---

## 12. Dependencies and Microstates

### Locked microstate policy

All recognized sovereign microstates should remain sovereign actors in the world design.

Their gameplay should emphasize:

* Diplomacy
* Finance
* Tourism
* International institutions
* Legal and tax policy
* Relations with neighboring protectors
* Security dependence
* Soft power
* Specialized economic roles

### Locked dependency policy

Dependencies should not automatically be treated as sovereign states.

They should receive direct political representation when their separate administration, population, strategic importance, or constitutional future creates meaningful gameplay.

Dependencies without sufficient independent gameplay should remain part of their parent state while retaining appropriate territorial and autonomy distinctions.

---

## 13. Indigenous and Stateless Nations

An ethnic, cultural, religious, or indigenous nation must not automatically be represented as a territorial country.

Possible representations include:

* Recognized minority
* Indigenous political institution
* Autonomous region
* Federal constituent entity
* Cultural movement
* Separatist movement
* Transnational population
* Exile organization
* Territorial government
* De facto state

Direct country representation requires a political or territorial institution, not only a distinct identity.

The design must avoid treating populations as politically uniform.

---

## 14. Territorial Duplication Rule

The same territory must not be simultaneously assigned as ordinary uncontested territory to multiple actors.

Contested territory must explicitly record:

* Recognized legal sovereign
* Current controller
* Additional claimants
* Local administration
* Conflict status
* Population status
* Applicable peace or ceasefire arrangements

Competing political entities may claim the same territory, but the global registry must identify one current controller for every location at the start date.

---

## 15. Global Entity Registry

A separate global entity registry will become the authoritative roster.

Each entry must contain:

| Field                            | Required information                                    |
| -------------------------------- | ------------------------------------------------------- |
| Design ID                        | Unique permanent internal design identifier             |
| Official name                    | Formal name at the campaign start                       |
| Common name                      | Standard display name                                   |
| Region                           | Primary regional document                               |
| Canonical category               | Principal category from this framework                  |
| Recognition class                | R1–R6                                                   |
| Control class                    | C1–C6                                                   |
| Administrative class             | A1–A10                                                  |
| Gameplay representation          | G1–G12                                                  |
| Legal sovereign                  | Recognized sovereign or parent state                    |
| Current controller               | Entity exercising effective control                     |
| Capital or administrative center | Political center at campaign start                      |
| Claimed territory                | Territory officially claimed                            |
| Controlled territory             | Territory actually controlled                           |
| Parent or sponsor                | Relevant parent state or foreign patron                 |
| Player availability              | Playable, conditional, or unavailable                   |
| Starting relationships           | Parent, subject, sponsor, claimant, rival, or guarantor |
| Transition paths                 | Possible changes in political status                    |
| Regional cross-references        | Related entities in other regional documents            |
| Decision status                  | Locked, provisional, open, or deferred                  |
| Notes                            | Historical and design clarification                     |

Names and proposed game tags must not replace the permanent Design ID.

The Design ID should remain stable even when names, borders, governments, or eventual technical tags change.

---

## 16. Decision Status Labels

Every unresolved classification must use one of these labels:

| Label       | Meaning                                                    |
| ----------- | ---------------------------------------------------------- |
| LOCKED      | Approved design decision; change requires explicit review  |
| PROVISIONAL | Current preferred design pending wider integration review  |
| OPEN        | Decision has not yet been made                             |
| DEFERRED    | Intentionally postponed to a later release or design phase |
| REJECTED    | Considered and intentionally excluded                      |

Regional documents should not use vague terms such as “maybe a tag” once the registry review has been completed.

---

## 17. Consistency Rules

The following rules apply to every regional roster:

1. Every entity must have one permanent Design ID.
2. Every entity must have one principal canonical category.
3. Legal sovereignty and effective control must be recorded separately.
4. Recognition and territorial control must not be treated as the same mechanic.
5. Disputed territory without an independent government must not be classified as a country.
6. An ethnic or separatist movement must not be classified as a territorial state without territorial administration.
7. An autonomous region must not be classified as independent solely because it possesses a proposed country tag.
8. Dependencies must identify their parent state.
9. De facto states must identify the state or states claiming their territory.
10. Civil-war factions must identify whether they seek national control, secession, autonomy, or ideological change.
11. Country playability must be recorded separately from political existence.
12. Proposed technical tags remain placeholders until the global roster is normalized.
13. No proposed tag may be reused by multiple entities.
14. Cross-regional entities must have one authoritative record and references elsewhere.
15. Every contested location must have one recorded controller at the start date.
16. All exceptions must be documented in the decision log.

---

## 18. Design Boundaries

This framework determines:

* What kinds of political entities exist
* How they are classified
* Which entities deserve direct representation
* Which entities should be playable
* How legal status differs from territorial control
* Which political transitions must be supported
* What data the global roster must contain

This framework does not yet determine:

* EU5 file structure
* Technical country tags
* Script syntax
* Map implementation
* Province or location ownership
* Subject-type implementation
* Event implementation
* AI scripting
* Localization structure
* Performance limitations

Those questions belong to the later implementation-planning phase after Design Freeze.

---

## 19. Required Follow-Up Work

After approving this framework:

1. Create the global entity registry.
2. Import every entity from the regional country lists.
3. Assign a permanent Design ID to every entity.
4. Identify duplicate entries and cross-regional references.
5. Resolve proposed tag collisions.
6. Assign recognition, control, administrative, and gameplay classifications.
7. Determine player availability.
8. Identify all disputed territories lacking an independent political actor.
9. Separate states, dependencies, autonomous regions, and movements.
10. Record every unresolved case in the decision log.
11. Update the regional files to reference the authoritative registry.
12. Lock the final 1993 world roster before detailed country design begins.

---

## 20. Initial Framework Decisions

The following decisions are locked unless later design review identifies a major contradiction:

* Full design will be completed before implementation begins.
* Every generally recognized sovereign state at the start date will be represented.
* Recognized sovereign microstates will not be excluded solely because of size.
* Recognition, sovereignty, claims, and territorial control will be separate concepts.
* Military occupation will not create immediate accepted sovereignty.
* Disputed islands and maritime claims will not be treated as countries without independent political administrations.
* Autonomous regions will not automatically become country actors.
* Separatist movements without stable territorial governments will normally use movement or regional mechanics.
* Durable de facto states may receive full country-level representation.
* Dependencies will be evaluated according to their political distinctiveness and gameplay value.
* Civil-war factions will be distinguished from separatist movements.
* Indigenous and stateless nations will require political or territorial institutions for direct country representation.
* The global entity registry will become the single authoritative source for the world roster.
* Technical implementation constraints will not determine the initial design classification.
