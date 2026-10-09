EU5 Modern World Mod – Politics and Government Foundations

Project: EU5 Modern World Mod
Document status: Working design record
Design phase: Politics and Government
Implementation status: Design only

1. Purpose and Status
This document records the politics-and-government decisions that have already been approved for the EU5 Modern World Mod. It is an authoritative design record for the current design phase, but it is not a design freeze and does not yet specify every reform, law, event, trigger, or numerical effect.

The political conversion must remain grounded in Europa Universalis V. The objective is to modernize the existing EU5 government framework rather than build a separate political simulation beside it.

2. Governing Design Principle
The mod should change as little of EU5’s underlying political architecture as reasonably possible.

* Retain an existing EU5 system when its underlying function still works.
* Prefer renaming, reinterpretation, adjusted availability, and rebalancing over replacement.
* Use existing government types, government resources, reforms, laws, succession rules, parliaments, estates, and related systems wherever possible.
* Do not add a parallel political value or mechanic when EU5 already provides a usable equivalent.
* Create a new mechanic only when an essential modern function cannot be represented convincingly through the existing framework.

The player represents the state rather than a specific governing party, leader, dynasty, junta, or revolutionary faction. Normal elections, leadership changes, coups, and regime transitions should therefore not automatically change the player-controlled country.

3. Technical Government-Type Framework
All five existing EU5 government types remain in the mod. Their modern meaning is determined by political reality and by visible government reforms rather than only by a state’s official constitutional name.

3.1 Monarchy
The technical EU5 type monarchy represents every regime in which the leadership is genuinely hereditary or institutionally dynastic.

* It includes formal monarchies such as kingdoms, emirates, sultanates, and principalities.
* It also includes officially republican regimes when succession is effectively institutionalized within a ruling family.
* A dictatorship does not become a technical monarchy merely because a relative is informally favored as successor. Dynastic succession must be politically institutionalized, generally expected, or successfully established.
* The existing government resource remains Legitimacy for all technical monarchies. No dynamic resource name is required.

3.2 Republic
The visible concept of a republic is kept narrower than EU5’s technical use of the republic type. Genuine parliamentary, presidential, semi-presidential, and other republican systems use this type directly.

Non-dynastic regular autocracies also remain technically based on republic when this allows EU5’s existing succession, reform, law, and event structure to be retained. Their visible government form is defined by reforms such as one-party rule, military rule, personalist autocracy, or a revolutionary regime; they are not presented to the player simply as republics.

The resource republican_tradition remains one technical value, but its visible name is dynamic according to the active government reform.

* Genuine republic: Republican Tradition.
* One-party state: Party Cohesion.
* Military regime: Junta Cohesion.
* Personalist autocracy: Regime Stability.
* Revolutionary regime: Revolutionary Legitimacy.

3.3 Theocracy
The technical EU5 type theocracy is determined by the institution that possesses the final political authority.

* A dynastic government that controls the religious establishment remains a monarchy.
* A secular elected or appointed government that controls the religious establishment remains a republic-based regime.
* A state is a theocracy when a religious leadership or clerical institution can ultimately control the government, legislation, elections, or selection of the head of state.
* A state religion, religious law, or symbolic religious legitimacy alone does not make a state a theocracy.

The existing resource devotion is retained with its vanilla visible meaning. In German localization it remains Frömmigkeit.

3.4 Tribe
The technical EU5 type tribe is reinterpreted as a Clan or Tribal State.

* It represents systems in which clans, tribes, extended families, and local traditional elites are central to political authority.
* The existing resource tribal_cohesion is retained as Tribal Cohesion; in German localization it remains Stammeskohäsion.

3.5 Steppe Horde
The technical EU5 type steppe_horde is reinterpreted as a Warlord Regime.

* It represents rule based on armed commanders, militias, personal military networks, and territorial control rather than a fully functioning central state.
* It may be used for complete state collapse and for an internationally recognized state whose government is effectively only one of several competing armed factions.
* A normal military dictatorship with a functioning central state apparatus is not automatically a Warlord Regime; it normally remains technically republic-based or, when genuinely dynastic, monarchy-based.
* The existing resource horde_unity is renamed Regime Cohesion; in German localization it is Regimekohäsion.

4. Government Resources
The technical resource framework remains tied to the five EU5 government types.

* monarchy: Legitimacy.
* republic: one technical republican_tradition value with reform-dependent visible localization.
* theocracy: Devotion / Frömmigkeit.
* tribe: Tribal Cohesion / Stammeskohäsion.
* steppe_horde: Regime Cohesion / Regimekohäsion.

5. Government-Reform Architecture
Modern political systems are represented through a multi-layered set of existing or reworked EU5 government reforms. The design deliberately uses several reforms when necessary instead of compressing every political feature into one single regime label.

Eight reform categories are used for design and documentation:

1. Government structure.
2. Regime form.
3. State structure.
4. Political representation.
5. Civil–military relations.
6. Relationship between executive and legislature.
7. Judicial order.
8. Administrative model.

These categories are not new hard-coded reform tiers. They are an organizational framework for designers. Technically, the entries remain normal EU5 government reforms.

* Only the government-structure reform is mandatory for every state.
* All other categories are optional and are used only when they add meaningful political or mechanical information.
* A state is not incomplete merely because it lacks a reform in an optional category.
* More than one compatible reform from the same design category may be active.
* Mutual exclusions are added only for genuine contradictions, not merely because two reforms share a documentation category.
* Laws, succession rules, parliaments, estates, privileges, and other EU5 systems should carry details that do not need a dedicated reform.

6. Mandatory Government-Structure Reform List
Every country must have at least one government-structure reform. The approved basic list is intentionally compact:

* Parliamentary System.
* Presidential System.
* Semi-Presidential System.
* Monarchical Government.
* Collegial Government.
* Clerical Government.
* Tribal Government.
* Warlord Regime.

Special cases and finer distinctions should be created through compatible additional reforms, laws, succession rules, and other existing EU5 systems rather than by expanding the mandatory base list without a demonstrated need.

7. Interpretation Rules
* Official constitutional terminology does not override the actual political structure.
* Government type and visible government reform must be distinguished. A country may be technically republic-based while visibly represented as a military regime or personalist autocracy.
* Dynastic succession takes precedence for the technical monarchy classification when it is genuinely institutionalized.
* Religious classification follows the location of final political authority rather than the mere presence of religion in public law.
* Military rule is not the same as a Warlord Regime. The decisive question is whether a functioning central state apparatus still exists.
* The reform framework should describe meaningful political differences without forcing every state into eight compulsory labels.

8. Matters Not Yet Decided
The following areas remain open and must not be treated as approved design:

* The detailed definitions, prerequisites, effects, incompatibilities, and transition rules for each mandatory government-structure reform.
* The complete reform lists for regime form, state structure, representation, civil–military relations, executive–legislative relations, judiciary, and administration.
* The precise law structure for elections, term limits, succession, party systems, civil rights, and emergency rule.
* The treatment of parliaments, estates, political power groups, parties, armed forces, bureaucracies, business interests, trade unions, religious institutions, regional elites, media, and civil society.
* The numerical effects and balance of Legitimacy, Republican Tradition and its dynamic names, Devotion, Tribal Cohesion, and Regime Cohesion.
* Country-by-country classifications for the 1 January 1993 start.

9. Next Design Task
The next task is to define the approved mandatory government-structure reforms one by one, beginning with their political meaning, compatible technical government types, mutual exclusions, and the EU5 mechanics they should reuse.
