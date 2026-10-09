# Europa Universalis V: Modern World Mod
## Mod Design Bible

**Working title:** EU5 Modern World Mod  
**Genre:** Total conversion / modern-era grand strategy  
**Start date:** 1993  
**Planned timeframe:** 1993 onwards  
**Base game:** Europa Universalis V by Paradox Interactive  
**Project status:** Global 349-entry political-territorial registry migrated and verified; institutional-entity design and full mechanical design in progress; implementation intentionally not started  

---

## 1. Purpose of this Document

This document is the central design bible for the EU5 Modern World Mod. It should collect the broad context, design philosophy, gameplay goals, historical assumptions, system translations, implementation notes, visual references, and major decisions for the entire project.

This non-archived document is the current high-level design-bible source of truth. Files whose titles begin `ARCHIVED —` are read-only historical copies and must not be updated or synchronized. Detailed country-content follow-up, event-chain reminders, mechanic work, and unresolved country-specific design belong only in `country_content_design_backlog.md`; this design bible should retain decisions and short cross-references.

---

## 2. Core Concept

The EU5 Modern World Mod is a total conversion mod that moves Europa Universalis V from its early-modern and pre-modern historical setting into the post-Cold-War world beginning in 1993.

The mod aims to simulate modern statecraft, globalization, regional integration, demographic change, internal politics, ideological conflict, economic development, international organizations, technological transformation, and modern warfare.

### Core fantasy

> What if Europa Universalis began after the collapse of the Soviet Union and allowed the player to reshape the modern world from 1993 onwards?

---
### Locked Campaign Start Date

The campaign begins on **1 January 1993**.

All starting political leaders, governments, borders, territorial control, active wars, ceasefires, diplomatic relations, international memberships, economic conditions, and military deployments must reflect conditions at the beginning of that date.

Events occurring later on 1 January 1993 or during the remainder of 1993 are post-start developments and should occur dynamically rather than being treated as completed starting conditions.
### Locked Campaign End-Date and Content-Horizon Policy

The campaign has **no fixed historical end date**.

Players may continue the campaign indefinitely, subject only to technical limitations that may be discovered during implementation.

The project also has **no predetermined historical-content or technology-design horizon**. Historical, technological, political, economic, social, and speculative content will continue to be designed from 1 January 1993 onward until the project owner decides that the planned content is sufficient.

The latest year for which detailed content has been designed may therefore change throughout development. Reaching that year must not end the campaign.

Beyond the currently authored material, the world should continue through reusable, systemic, and dynamically generated gameplay rather than relying exclusively on predetermined historical events.

The design must therefore support:

* Governments and leaders changing without a finite historical database
* Continuing demographic and economic development
* Repeatable elections and political succession
* Dynamic wars, alliances, organizations, and diplomatic realignments
* Continuing technological and institutional development
* Procedurally selected or systemic global crises
* Formation, collapse, division, and reunification of states
* Long-term climate, resource, migration, and social pressures
* Continued play after all named historical event chains have concluded

No victory screen or forced campaign termination should occur merely because a particular calendar year has been reached.

### Locked Historical-Direction Policy

The campaign uses a **historically directed sandbox**.

Major historical events and developments should normally be expected to occur near their historical dates. History should exert strong pressure on the campaign, particularly when the political, economic, diplomatic, military, social, and technological conditions that produced the real event still exist.

Historical outcomes must not be completely predetermined. Events should provide meaningful choices, alternate outcomes, and opportunities for players or AI-controlled countries to change their course.

The governing principle is:

> Historical events should normally happen, but their causes, timing, outcomes, participants, and consequences may change.

The mod uses **plausible cancellation**.

A historical event should be cancelled, delayed, replaced, or substantially transformed when earlier developments have removed its principal causes or made its historical form implausible.

An event must not occur merely because its historical date has arrived.

Plausible cancellation may apply when:

* A necessary country, government, organization, movement, or political leader no longer exists
* The relevant war, dispute, alliance, occupation, or diplomatic confrontation has already been resolved
* The political ideology or government responsible for the event has been removed or fundamentally changed
* The required economic, social, military, technological, or diplomatic conditions are absent
* Earlier alternate events have already produced an incompatible outcome
* The event’s intended objective has already been achieved through another path
* The historical participants have developed substantially different interests or relationships
* Triggering the event would contradict the current state of the campaign

Historical events should be divided into four design classes:

1. **Starting realities** — Conditions already active on 1 January 1993. These are part of the starting world rather than future events.
2. **Scheduled historical events** — Major events that should normally be presented near their real dates when their essential conditions remain plausible.
3. **Historically expected developments** — Developments strongly encouraged by existing pressures but allowed to occur earlier, later, differently, or not at all.
4. **Fully conditional developments** — Events that occur only when their required campaign conditions emerge.

Scheduled historical events may still produce alternate outcomes. Plausible cancellation determines whether the event or crisis should arise at all; player and AI choices determine how it develops once active.

When a historical event is cancelled, the design should use one of the following responses where appropriate:

* Allow the event to disappear without replacement
* Delay it until its conditions return
* Replace it with an alternate version suited to the current world
* Convert it into a broader dynamic crisis
* Transfer its role to different countries, organizations, or leaders
* Record that the historical development has been peacefully or indirectly resolved

The strength of historical direction may decrease naturally as the campaign diverges further from real history. However, later historical events should still be considered whenever their underlying causes remain present.

### Locked Player-Role Policy

The player represents **the state itself**, following the normal Europa Universalis model.

The player does not exclusively represent the current leader, government, ruling party, political movement, dynasty, military command, or regime.

The player normally continues controlling the same state through:

* Elections and peaceful transfers of power
* Changes of prime minister, president, monarch, or other national leader
* Coalition changes
* Constitutional reform
* Coups and countercoups
* Revolutions
* Democratization
* Authoritarian consolidation
* Military rule
* Restoration of civilian government
* Changes in ideology or economic policy
* Temporary occupation
* Government collapse and reconstruction

A change of government must not normally end the campaign or remove the player’s control of the state.

Domestic political actors should still possess their own interests, influence, and objectives. The player directs the state but cannot assume that every political faction, institution, region, or population group automatically supports state policy.

The state may impose costs, restrictions, or resistance on the player through:

* Institutional limits
* Public opposition
* Coalition disputes
* Legislative obstruction
* Military disloyalty
* Regional resistance
* Elite conflict
* Strikes and civil unrest
* Separatism
* Coups and revolutions

When a state experiences civil war, fragmentation, or dissolution, the design must provide a clear continuity rule.

The default principle is:

> The player remains associated with the original state or its principal legal continuation unless a specific crisis design provides a meaningful choice of successor.

Possible crisis outcomes include:

* Retaining control of the internationally recognized government
* Continuing as the principal successor state
* Choosing between rival successor states when no single continuation is clear
* Continuing as a government in exile where that remains a meaningful state-level campaign
* Selecting a successor entity after complete and irreversible dissolution

Switching to rebels, separatists, coup leaders, or opposition movements should not happen automatically merely because they oppose the current government. Such a switch requires an explicit crisis rule or player choice.

### Locked Core Gameplay Activities Policy

The mod will include all of the following as principal parts of the modern-state gameplay loop:

1. Domestic politics and institutional reform
2. Economic management and development
3. Diplomacy and international organizations
4. Trade, foreign investment, sanctions, and economic influence
5. Military modernization and warfare
6. Intelligence, covert action, counterintelligence, and foreign interference
7. Technology, research, and modernization
8. Demographics, migration, and social policy
9. Regional integration and leadership of international blocs
10. Crisis management and historically directed events
11. Territorial expansion, reunification, independence, and state formation
12. Soft power, culture, information, and global influence

No single activity should completely dominate every campaign.

Countries should provide different balances between these activities according to their size, political system, economic structure, security environment, geography, international position, and historical circumstances.

The mod should adapt existing EU5 systems wherever they provide a suitable foundation. Systems should be expanded, reinterpreted, or replaced when their original early-modern assumptions cannot convincingly represent modern statecraft.

The following broad EU5 foundations are expected to be reusable:

* Governments, laws, reforms, parliaments, estates, and political power groups
* Population, culture, religion, language, and regional identity
* Production, goods, buildings, markets, taxation, budgets, debt, and inflation
* Diplomacy, subjects, alliances, guarantees, international organizations, and diplomatic influence
* Warfare, military forces, mobilization, occupation, rebels, and peace agreements
* Spy networks, covert actions, counterespionage, and intelligence-related policies
* Advances, institutions, research, societal development, and technological diffusion
* Situations, disasters, missions, events, and other crisis frameworks
* Cultural influence, prestige, and other foundations for soft power

The following modern activities will require substantial redesign or additional mechanics:

* Political parties, elections, coalitions, public opinion, and modern institutional legitimacy
* Government budgets, central banking, modern finance, unemployment, and macroeconomic policy
* Foreign direct investment, multinational corporations, development assistance, and economic dependency
* Comprehensive sanctions, export controls, asset restrictions, and financial isolation
* Modern welfare, healthcare, education, citizenship, immigration, and demographic policy
* Modern intelligence agencies, cyber operations, disinformation, election interference, and proxy networks
* NATO-style collective defence, European integration, supranational law, and modern international governance
* Nuclear deterrence, missile forces, escalation control, and weapons proliferation
* Global media, cultural exports, public diplomacy, information control, and modern soft power
* Climate policy, pandemics, global supply chains, digitalization, and other modern systemic crises

A mechanic must not be excluded merely because it is not already represented perfectly by vanilla EU5.

The design goal is to preserve EU5’s state-level grand-strategy structure while extending it into a comprehensive modern-world simulation.

### Locked Simulation-Depth Policy

The mod follows a **simulation-heavy design approach because it preserves and modernizes the full simulation framework of Europa Universalis V**.

Simulation-heavy design does not mean discarding EU5 systems and replacing them with separate custom systems.

The governing principle is:

> Use EU5’s existing simulation wherever possible, transform it for the modern era, and add new mechanics only where the existing framework cannot represent an essential modern function.

The mod should retain the depth created by EU5’s interacting systems, including:

* Population and demographic simulation
* Political power groups and internal competition
* Government institutions, laws, reforms, and legitimacy
* Production, buildings, goods, markets, trade, prices, taxation, budgets, debt, and inflation
* Locations, provinces, regions, ownership, control, autonomy, claims, and occupation
* Diplomacy, alliances, subjects, treaties, international organizations, and influence
* Military recruitment, manpower, logistics, professionalism, morale, occupation, rebels, and peace agreements
* Research, advances, institutions, technological diffusion, and societal development
* Culture, religion, identity, migration, assimilation, and social change
* Espionage, covert action, events, situations, disasters, missions, and AI behavior

These systems should remain connected to one another after conversion.

Modernization may change their names, variables, balance, timescales, content, interfaces, or exact behavior, but should preserve their systemic purpose wherever that purpose remains useful.

Examples include:

* EU5 political power groups becoming modern political parties, trade unions, business interests, armed forces, bureaucracies, religious institutions, civil society, media interests, regional elites, or oligarchic networks
* EU5 population systems representing modern employment, education, income, urbanization, migration, citizenship, identity, aging, and living standards
* EU5 markets and production becoming modern industrial, service, financial, energy, technological, agricultural, and supply-chain systems
* EU5 diplomatic and international-organization systems becoming modern alliances, security organizations, economic unions, customs areas, supranational institutions, and international governance
* EU5 military systems becoming modern professional forces, conscription systems, reserves, equipment categories, readiness, procurement, logistics, air power, naval power, and missile forces
* EU5 institutions and advances becoming globalization, digitalization, financial integration, biotechnology, climate governance, automation, artificial intelligence, and future technological development
* EU5 cultural, religious, and legitimacy systems expanding to include ideology, citizenship, secularism, national identity, social values, information control, and soft power
* EU5 colonization-related mechanics being reassigned where suitable to foreign investment, strategic influence, development assistance, settlement policy, peacekeeping, military basing, or territorial administration

Modern terminology must not be cosmetic.

A renamed system must also be adjusted so that its incentives, effects, interactions, and outcomes make sense in the modern world.

Custom mechanics should be added when an essential modern system has no adequate EU5 equivalent or when conversion would distort the original system beyond usefulness.

Possible examples include:

* Nuclear deterrence and escalation
* Central-bank and monetary policy
* Detailed sanctions and financial isolation
* Cyber operations and digital infrastructure
* Modern media and information warfare
* Supranational law
* Global supply-chain dependency
* Modern air, missile, and strategic-weapons systems where the existing military framework is insufficient

New mechanics must connect to EU5’s wider simulation rather than operating as isolated minigames.

For example:

* Economic decline should affect government revenue, political legitimacy, migration, military readiness, and technological investment
* Education and research should affect productivity, innovation, political expectations, and modernization
* War should affect casualties, population displacement, debt, trade, public opinion, infrastructure, and international relations
* Sanctions should affect markets, finance, technology access, government revenue, elite interests, and living standards
* Demographic decline should affect labour, taxation, welfare expenditure, recruitment, and economic growth
* Corruption should affect state capacity, investment efficiency, political legitimacy, military procurement, and diplomacy
* Migration should affect population growth, labour markets, identity politics, social policy, and relations between states

Abstraction remains acceptable for individual details that EU5 already handles through aggregate simulation or where further detail would create repetitive administrative micromanagement without meaningful state-level choices.

The player represents the state rather than every individual official, company, soldier, or citizen.

The objective is therefore detailed systemic simulation at the state, regional, population-group, institution, market, and military-formation levels—not manual control of every individual transaction or administrative action.

All major converted or newly added systems must eventually document:

* Their EU5 mechanical foundation
* Their modern interpretation
* Their retained mechanics
* Their renamed or rebalanced elements
* Their expansions or structural changes
* Their underlying variables
* Their inputs and outputs
* Their player decisions
* Their AI behavior
* Their interactions with other systems
* Their short-term and long-term consequences
* Their failure states
* Their technical uncertainties

Technical limitations may affect the eventual implementation method, but the initial design should assume that the full EU5 simulation remains active unless later technical research proves that a specific element cannot be converted safely.

### Locked EU5 Full-System Conversion Policy

The mod will make full use of Europa Universalis V as its mechanical foundation.

EU5 is already a simulation-heavy grand-strategy game with interconnected political, economic, demographic, diplomatic, military, technological, cultural, religious, institutional, and territorial systems.

The mod should not discard those systems merely because they were originally designed for an earlier historical period.

The governing principle is:

> Preserve the full depth and interconnection of EU5, then rename, redesign, rebalance, expand, and reinterpret its systems for the modern world.

Every major EU5 system should be reviewed for modern conversion.

A system may be:

1. **Retained** — Used largely as designed because its underlying function remains appropriate.
2. **Renamed** — Given modern terminology while retaining most of its original behavior.
3. **Rebalanced** — Adjusted to reflect modern timescales, institutions, economies, populations, and military conditions.
4. **Reinterpreted** — Used to represent a modern concept that performs a comparable strategic role.
5. **Expanded** — Given additional variables, interactions, content, or mechanics needed for modern simulation.
6. **Restructured** — Substantially redesigned while preserving its place within EU5’s wider simulation.
7. **Replaced** — Rebuilt only when the original system cannot adequately represent the modern concept.
8. **Supplemented** — Supported by new mechanics where EU5 does not contain a sufficient equivalent.

The preferred order is:

1. Retain
2. Rename
3. Rebalance
4. Reinterpret
5. Expand
6. Restructure
7. Replace or supplement only when necessary

Replacement should not be the default approach.

The mod should preserve and modernize, where applicable:

* Countries, governments, laws, reforms, legitimacy, stability, and state capacity
* Estates, political power groups, privileges, influence, loyalty, and internal competition
* Cabinets, offices, leaders, parliaments, succession, and political institutions
* Population groups, cultures, languages, religions, classes, employment, migration, and social change
* Locations, provinces, regions, ownership, control, occupation, autonomy, and territorial claims
* Buildings, production methods, goods, resources, infrastructure, markets, prices, trade, taxation, and finance
* Government income, expenditure, debt, inflation, investment, and economic policy
* Diplomacy, alliances, subjects, guarantees, favors, influence, treaties, and diplomatic reputation
* International organizations and their membership, rules, reforms, powers, and internal politics
* Armies, navies, recruitment, manpower, reserves, equipment, logistics, morale, professionalism, and warfare
* Rebels, separatism, civil wars, occupations, resistance, peace agreements, and state collapse
* Espionage, spy networks, covert actions, counterintelligence, and foreign interference
* Research, advances, institutions, technological diffusion, societal development, and modernization
* Culture, religion, ideology, legitimacy, prestige, information, and soft power
* Events, situations, disasters, missions, journals, decisions, and historical developments
* AI decision-making, strategic objectives, diplomatic behavior, economic planning, and military priorities

Modern terminology must not produce a merely cosmetic conversion.

Renaming an EU5 concept is acceptable only when its underlying behavior also provides a convincing modern function.

Examples of possible reinterpretation include:

* Estates becoming political parties, business interests, trade unions, armed forces, bureaucracies, religious institutions, regional elites, civil society, media interests, or oligarchic networks
* Dynastic and court politics becoming leadership, cabinet, party, coalition, institutional, and elite politics
* Institutions becoming major phases of globalization, digitalization, financial integration, climate governance, biotechnology, automation, or artificial intelligence
* Colonization-related systems becoming development programs, foreign investment, strategic influence, settlement policy, peacekeeping, military basing, or territorial administration where appropriate
* Religious and cultural systems expanding to include ideology, national identity, citizenship, secularism, social values, and political legitimacy
* Early-modern markets becoming modern domestic, regional, and global production, trade, financial, energy, and supply-chain systems
* Subjects and dependencies becoming federal units, autonomous territories, protectorates, associated states, occupied administrations, client governments, and modern dependency relationships
* Traditional diplomatic blocs becoming modern alliances, economic unions, customs areas, security organizations, international institutions, and supranational structures

New mechanics should be designed when no converted EU5 system can adequately represent an essential modern feature.

Likely examples include:

* Nuclear deterrence and escalation
* Modern monetary and central-bank policy
* Detailed sanctions and financial isolation
* Cyber operations and digital infrastructure
* Modern media and information warfare
* Supranational legal integration
* Global supply-chain dependency
* Modern air and missile warfare where existing systems are insufficient

Even these additions should interact with EU5’s existing simulation rather than operating as isolated minigames.

The objective is not to build a separate strategy game inside EU5.

The objective is to transform the whole of EU5 into a modern-world grand-strategy simulation while preserving the depth, systemic interaction, and state-level gameplay that make EU5 its foundation.

## 3. Why 1993?

1993 is a strong starting point because it follows the collapse of the Soviet Union and sits at the beginning of the modern geopolitical era.

Important 1993 context:

- The United States is the sole global superpower.
- Russia is unstable and transitioning after the fall of the USSR.
- The former Soviet republics are newly independent.
- The European Union is entering the Maastricht era.
- Germany is recently reunified.
- Yugoslavia is collapsing into war.
- China is entering its high-growth reform era.
- Globalization is accelerating.
- NATO expansion, EU enlargement, the internet age, modern terrorism, climate politics, financial crises, and multipolar competition are still ahead.

---

## 4. Design Pillars

### 4.1 Plausible modern alternate history

The mod should allow alternate outcomes, but they should feel plausible within modern political, economic, demographic, and military constraints.

### 4.2 Statecraft over conquest

Conquest should exist, but modern statecraft should also revolve around diplomacy, influence, alliances, trade, investment, sanctions, domestic legitimacy, technological development, and crisis management.

### 4.3 Internal politics matter

Modern countries should not feel like simple map-painting machines. Regime stability, political legitimacy, corruption, separatism, ideology, institutions, public opinion, and economic pressures should shape gameplay.

### 4.4 Global systems matter

International organizations, global markets, trade blocs, energy dependencies, migration, technological change, and climate pressures should affect most countries.

### 4.5 Fun before perfect simulation

Historical and political accuracy matters, but gameplay must remain readable, stable, and fun.

---

## 5. Scope

### Included in the long-term vision

- Modern country borders from 1993 onwards
- All major recognized states
- Selected de facto states and breakaway regions
- Modern governments and regime types
- Modern ideologies and political systems
- International organizations and alliances
- Modern trade goods and industries
- Modern military structure
- Nuclear weapons and deterrence mechanics
- Post-Cold-War event chains
- Regional crisis systems
- Economic development and globalization
- Technological progression into the 21st century

### Not part of the initial version

- Perfect worldwide detail on day one
- Full simulation of every real-world political party
- Hyper-detailed military order of battle
- Every historical event scripted immediately
- Perfect balance between all countries in the first release

---

## 6. First Playable Target

### Version 0.1: 1993 Sandbox Foundation

The first playable version should prove that the modern setting works inside EU5. It does not need to be historically complete, perfectly balanced, or globally detailed. It only needs to establish that a 1993 modern-world setup can load, run, and produce believable gameplay.

Initial goals:

- Change the game start date to 1993.
- Define the basic modern country setup.
- Implement a limited set of modern governments.
- Create placeholder modern technologies.
- Create placeholder modern trade goods.
- Set up major alliances and blocs.
- Focus the first detailed region on Europe and the former Soviet Union.
- Ensure the game launches and runs without critical errors.

Recommended first focus region:

> Europe + former Soviet Union

Reason: This region contains many of the most important 1993 systems: the EU, NATO, post-Soviet transition, Yugoslavia, Russia, Ukraine, the Baltics, the Caucasus, and Eastern European reform.

### 6.1 Version 0.1 Design Philosophy

Version 0.1 should be treated as a vertical slice, not as a full release. The goal is to create a small but coherent version of the modern-world experience.

The first version should answer these questions:

- Can EU5 support a convincing 1993 start date?
- Can modern countries, borders, governments, and diplomacy be represented cleanly?
- Can modern politics be approximated using available EU5 systems?
- Can the game remain stable after replacing large amounts of historical setup?
- Which vanilla systems can be reused, which need heavy modification, and which need custom design?

### 6.2 Version 0.1 Work Packages

| Work package | Description | Priority |
|---|---|---|
| Start date conversion | Change the playable start date and supporting timeline values to 1993 onwards | Critical |
| Country framework | Define modern country tags, names, colors, flags, capitals, and basic existence | Critical |
| Europe and post-Soviet setup | Create initial political geography for Europe and the former Soviet Union | Critical |
| Government framework | Add placeholder modern regime categories | High |
| Diplomacy framework | Represent NATO, EU, CIS, and basic international alignments | High |
| Economy placeholder | Replace obviously medieval/early-modern economic assumptions with modern placeholders | High |
| Technology placeholder | Create a rough modern-era technology timeline | Medium |
| Localization cleanup | Ensure modern names and descriptions appear correctly in-game | Medium |
| Stability testing | Confirm the game launches, saves, reloads, and runs for several years | Critical |

### 6.3 Version 0.1 Geographic Scope

Version 0.1 should not attempt to perfectly model the entire world. It should include the world at a basic placeholder level, but detailed work should begin with Europe and the former Soviet sphere.

Primary focus:

- European Union member states in 1993
- NATO member states in 1993
- Former Soviet republics
- Yugoslav successor states and conflict zone
- Central and Eastern European transition states
- Turkey and the Caucasus as bridge regions

Secondary placeholder coverage:

- United States
- China
- Japan
- India
- Middle East regional powers
- Major African states
- Major Latin American states

### 6.3.1 Europe + Former Soviet Union 1993 Country List

This list is the first working country roster for the Version 0.1 focus region. It should be treated as a modding checklist rather than a final historical claim. The goal is to identify which playable or represented political entities need tags, names, capitals, colors, flags, starting governments, diplomatic alignments, and basic history setup for the 1993 start date.

#### Western, Northern, and Southern Europe

| Country / entity | 1993 status | Initial implementation priority | Notes |
|---|---|---|---|
| United Kingdom | Sovereign state; NATO member; EC/EU member | Critical | Major power and NATO anchor |
| Ireland | Sovereign state; EC/EU member | High | Neutral state within Western Europe |
| France | Sovereign state; NATO political member; EC/EU member; nuclear state | Critical | Major power and permanent UN Security Council member |
| Germany | Reunified sovereign state; NATO member; EC/EU member | Critical | Recently reunified and central to Europe |
| Netherlands | Sovereign state; NATO member; EC/EU member | High | Core Western European economy |
| Belgium | Sovereign state; NATO member; EC/EU member | High | Hosts major European institutions |
| Luxembourg | Sovereign state; NATO member; EC/EU member | Medium | Small but symbolically important EU state |
| Denmark | Sovereign state; NATO member; EC/EU member | High | Nordic NATO and EU member |
| Norway | Sovereign state; NATO member | High | Not an EU member in 1993 |
| Sweden | Sovereign state; neutral/non-aligned | High | Not yet an EU member in 1993 |
| Finland | Sovereign state; neutral/non-aligned | High | Not yet an EU member in 1993; post-Soviet adjustment |
| Iceland | Sovereign state; NATO member | Medium | Strategic North Atlantic location |
| Spain | Sovereign state; NATO member; EC/EU member | High | Major Southern European state |
| Portugal | Sovereign state; NATO member; EC/EU member | High | Atlantic and EU member |
| Italy | Sovereign state; NATO member; EC/EU member | Critical | Major European power |
| Austria | Sovereign state; neutral | High | Not yet an EU member in 1993 |
| Switzerland | Sovereign state; neutral | High | Wealthy neutral state |
| Malta | Sovereign state | Medium | Mediterranean microstate |
| Cyprus | Sovereign state; divided island | Medium | Controls the south and claims the whole island; Northern Cyprus is a separate de facto country actor guaranteed by Turkey |
| Northern Cyprus | Independent de facto country; recognized only by Turkey | Medium | Uses `TRNC` as an independent country actor. Turkey guarantees its independence or provides the closest available defensive-protection relationship; it is not a Turkish subject. |
| Greece | Sovereign state; NATO member; EC/EU member | High | Balkan and Eastern Mediterranean actor |
| Turkey | Sovereign state; NATO member | Critical | Bridge between Europe, Caucasus, Middle East, and Black Sea |

#### Central and Eastern Europe

| Country / entity | 1993 status | Initial implementation priority | Notes |
|---|---|---|---|
| Poland | Sovereign state; post-communist transition | Critical | Major future NATO/EU enlargement candidate |
| Czech Republic | Newly sovereign state after Czechoslovakia split | High | Created on 1 January 1993 |
| Slovakia | Newly sovereign state after Czechoslovakia split | High | Created on 1 January 1993 |
| Hungary | Sovereign state; post-communist transition | High | Future NATO/EU enlargement candidate |
| Romania | Sovereign state; post-communist transition | High | Important Balkan and Black Sea state |
| Bulgaria | Sovereign state; post-communist transition | High | Important Balkan and Black Sea state |
| Albania | Sovereign state; post-communist transition | Medium | Weak state capacity and economic crisis potential |

#### Yugoslav Successor Region

| Country / entity | 1993 status | Initial implementation priority | Notes |
|---|---|---|---|
| Slovenia | Independent state | High | Former Yugoslav republic; relatively stable |
| Croatia | Independent state; involved in Yugoslav Wars | Critical | Active conflict and territorial disputes |
| Bosnia and Herzegovina | Independent state; Bosnian War ongoing | Critical | Core early crisis region |
| Federal Republic of Yugoslavia | Serbia and Montenegro federation | Critical | Represents Serbia and Montenegro in 1993 |
| Macedonia | Independent state; international naming dispute | Medium | Use period-appropriate naming decision later |
| Republika Srpska | Rejected as a separate entity | None | All territory is assigned to Bosnia and Herzegovina; no country actor, tag, subject, releasable, or separate territorial ownership. Content follow-up is centralized in `country_content_design_backlog.md`. |
| Croatian Republic of Herzeg-Bosnia | Rejected as a separate entity | None | All territory is assigned to Bosnia and Herzegovina; no country actor, tag, subject, releasable, or separate territorial ownership. Content follow-up is centralized in `country_content_design_backlog.md`. |
| Republic of Serbian Krajina | Rejected as a separate entity | None | All territory is assigned to Croatia; no country actor, tag, subject, or releasable. Content follow-up is centralized in `country_content_design_backlog.md`. |
| Kosovo | Standard EU5 Vassal of Federal Republic of Yugoslavia | Medium | Uses `KOS` as a separate subject actor under `YUG`. This is a temporary starting setup. Detailed country-content follow-up is centralized in `country_content_design_backlog.md`. |

#### Former Soviet Union

| Country / entity | 1993 status | Initial implementation priority | Notes |
|---|---|---|---|
| Russia | Sovereign successor state of the USSR; Tatarstan consolidated at start; nuclear state | Critical | All Tatarstan territory is assigned to Russia. Detailed follow-up is centralized in `country_content_design_backlog.md`. |
| Ukraine | Sovereign state; Crimea consolidated at start; inherited Soviet nuclear weapons | Critical | All Crimean territory, including Sevastopol, is assigned directly to Ukraine. Detailed follow-up is centralized in `country_content_design_backlog.md`. |
| Belarus | Sovereign state; inherited Soviet nuclear weapons | High | Post-Soviet transition and CIS alignment |
| Moldova | Sovereign state; all recognized territory consolidated under one starting actor | High | Moldova is the only starting country actor. Transnistria and Gagauzia have no separate starting actors, subjects, or territorial ownership. Content follow-up is centralized in `country_content_design_backlog.md`. |
| Estonia | Sovereign state; Baltic state | High | Newly independent; future EU/NATO candidate |
| Latvia | Sovereign state; Baltic state | High | Newly independent; future EU/NATO candidate |
| Lithuania | Sovereign state; Baltic state | High | Newly independent; future EU/NATO candidate |
| Georgia | Sovereign state; Georgian regions consolidated at start | High | Abkhazia, South Ossetia, and Adjara are assigned to Georgia. None has a separate starting actor, subject, tag, or territorial ownership. Detailed follow-up is centralized in `country_content_design_backlog.md`. |
| Armenia | Sovereign state; Nagorno-Karabakh conflict context | High | Caucasus conflict participant |
| Azerbaijan | Sovereign state; Nagorno-Karabakh consolidated at start | High | All Nagorno-Karabakh territory is assigned to Azerbaijan. Detailed follow-up is centralized in `country_content_design_backlog.md`. |
| Nakhchivan | Standard EU5 Vassal of Azerbaijan using `NAK` | Medium | Separate subject actor controlling the Nakhchivan exclave under `AZE`; detailed follow-up is centralized in `country_content_design_backlog.md`. |
| Kazakhstan | Sovereign state; inherited Soviet nuclear weapons | High | Major Central Asian state and nuclear disarmament chain |
| Uzbekistan | Sovereign state | Medium | Major Central Asian population center |
| Turkmenistan | Sovereign state | Medium | Energy state and neutralist direction |
| Kyrgyzstan | Sovereign state | Medium | Central Asian post-Soviet transition state |
| Tajikistan | Sovereign state; civil war ongoing | High | Active internal conflict in 1993 |
| Transnistria | Internal Moldova content at campaign start | Medium | No separate starting actor, subject, or territorial ownership. Content follow-up is centralized in `country_content_design_backlog.md`. |
| Gagauzia | Internal Moldova content at campaign start | Medium | No separate starting actor, subject, or territorial ownership. Content follow-up is centralized in `country_content_design_backlog.md`. |
| Abkhazia | Internal Georgia content at campaign start | Medium | No separate starting actor, subject, or territorial ownership. Detailed follow-up is centralized in `country_content_design_backlog.md`. |
| South Ossetia | Internal Georgia content at campaign start | Low | No separate starting actor, subject, tag, or territorial ownership. Detailed follow-up is centralized in `country_content_design_backlog.md`. |
| Nagorno-Karabakh / Artsakh | Internal Azerbaijan content at campaign start | Medium | No separate starting actor, subject, technical tag, or territorial ownership. Detailed follow-up is centralized in `country_content_design_backlog.md`. |
| Chechnya | Standard EU5 Vassal of Russia using `CHE` | Medium | Temporary starting setup. Detailed country-content follow-up is centralized in `country_content_design_backlog.md`. |

#### Microstates and Special European Entities

| Country / entity | 1993 status | Initial implementation priority | Notes |
|---|---|---|---|
| Andorra | Sovereign microstate | Low | Can be included later if map scale supports it |
| Liechtenstein | Sovereign microstate | Low | Can be included later if map scale supports it |
| Monaco | Sovereign microstate | Low | Can be included later if map scale supports it |
| San Marino | Sovereign microstate | Low | Can be included later if map scale supports it |
| Vatican City | Sovereign microstate | Low | Special religious/diplomatic role if represented |

#### Initial Tagging Principles

- Every fully recognized sovereign state in Europe and the former Soviet Union should receive a proper tag in Version 0.1 if the map and setup allow it.
- Unresolved unrecognized separatist administrations within recognized states default to parent-state ownership and internal country content. Separate starting actors require explicit project-owner approval; existing locked exceptions remain unchanged.
- Disputed regions should be implemented only as deeply as needed for stable gameplay in Version 0.1.
- NATO, EU, CIS, neutrality, and post-Soviet transition status should be tracked from the beginning, even if only through placeholder modifiers.
- The first pass should prioritize loading, map recognizability, and major crisis regions over perfect political detail.

### 6.4 Version 0.1 Historical Snapshot

The first start-date snapshot should represent the world as it broadly exists in 1993, not as it exists today.

Key 1993 assumptions:

- Russia exists as the main successor state of the USSR but is politically unstable.
- Ukraine, Belarus, Kazakhstan, the Baltic states, the Caucasus states, and Central Asian republics are independent.
- Germany is reunified.
- Czechoslovakia has split into the Czech Republic and Slovakia.
- Yugoslavia has fragmented, with ongoing war in Bosnia and broader instability in the Balkans.
- The European Union is emerging from the Maastricht Treaty framework.
- NATO remains a Cold War-era alliance in transition, not yet enlarged into Eastern Europe.
- China is not yet a peer superpower but is a rapidly rising state.
- The United States begins as the strongest global power.

### 6.5 Version 0.1 Success Criteria

Version 0.1 is successful when:

- The mod loads without crashing.
- The 1993 start date appears and is playable.
- Major countries exist with correct modern names.
- Europe and the former Soviet Union are recognizable.
- Major alliances and blocs are represented at least in placeholder form.
- Basic modern governments exist.
- The game can run for at least 10 in-game years without major errors.
- The project has a clear path from placeholder systems to deeper mechanics.

### 6.6 Version 0.1 Known Acceptable Shortcuts

The first version may temporarily use simplified or placeholder content:

- Generic modern government types instead of country-specific constitutions.
- Simplified borders where province-level precision is not yet possible.
- Placeholder leaders where leader systems are not yet implemented.
- Simplified trade goods and industries.
- Simplified international organizations using whatever vanilla diplomatic systems are easiest to adapt.
- Temporary localization text.
- Basic country modifiers instead of full custom mechanics.

These shortcuts should be documented and replaced gradually.

## 7. Major System Translations

| Vanilla EU-style concept | Modern World equivalent |
|---|---|
| Dynasties | Governments, leaders, parties, institutions |
| Estates | Political factions, oligarchs, military, corporations, unions, civil society |
| Religion | Religion, ideology, identity, legitimacy, social values |
| Institutions | Globalization, internet, financialization, climate governance, AI |
| Colonization | Foreign investment, influence, development aid, peacekeeping, military basing |
| Trade goods | Energy, electronics, finance, services, agriculture, rare earths, arms, consumer goods |
| Manpower | Population, conscription, professional army, reserves, mobilization capacity |
| Technology groups | Development level, research base, education, industrial capacity |
| Imperial diplomacy | Alliances, blocs, treaties, sanctions, international organizations |

---

## 8. Government and Regime Types

Potential modern government categories:

- Parliamentary democracy
- Presidential democracy
- Semi-presidential republic
- Constitutional monarchy
- Federal republic
- One-party state
- Military junta
- Personalist dictatorship
- Theocracy
- Hybrid regime
- Transitional government
- Failed state / warlord state

Government systems should affect:

- Stability
- Legitimacy
- Reform speed
- Military loyalty
- Corruption
- Diplomatic options
- Economic policy
- Resistance to unrest
- Ability to join alliances or blocs

---

## 9. Ideology and Political Alignment

Potential ideological categories:

- Liberal democracy
- Conservatism
- Social democracy
- Socialism
- Communism
- Nationalism
- Religious conservatism
- Islamism
- Authoritarian capitalism
- Military authoritarianism
- Technocracy
- Populism

Political alignment should not be a simple one-axis system. Countries can be democratic but nationalist, authoritarian but capitalist, socialist but non-aligned, or religious but economically liberal.

---

## 10. International Organizations and Blocs

Important organizations to represent:

These institutional entities are outside the 349-entry political-territorial registry and require a separate owner-reviewed institutional registry.

- United Nations
- NATO
- European Union
- Commonwealth of Independent States
- Organization for Security and Co-operation in Europe
- African Union / Organization of African Unity
- ASEAN
- Mercosur
- NAFTA
- OPEC
- WTO / GATT transition
- Arab League
- Gulf Cooperation Council

Possible mechanics:

- Membership modifiers
- Shared markets
- Defensive guarantees
- Sanctions
- Peacekeeping
- Accession requirements
- Bloc-specific missions or reforms
- Diplomatic pressure

---

## 11. Economy

The modern economy should represent more than production value. Important concepts include:

- GDP-like economic capacity
- Development level
- Industrial base
- Service economy
- Energy dependency
- Debt
- Inflation
- Corruption
- Foreign investment
- Trade openness
- Sanctions
- Resource exports
- Strategic industries

Possible modern trade goods:

- Oil
- Natural gas
- Coal
- Uranium
- Rare earths
- Electronics
- Automobiles
- Arms
- Pharmaceuticals
- Financial services
- Consumer goods
- Grain
- Livestock
- Timber
- Steel
- Chemicals
- Textiles
- Tourism
- Software

---

## 12. Military and Security

Modern military gameplay should include:

- Professional armies
- Conscription systems
- Reserve forces
- Air power
- Naval power
- Missile systems
- Nuclear deterrence
- Special forces
- Insurgency and counterinsurgency
- Peacekeeping
- Military aid
- Arms imports and exports
- Defense spending

The goal is not to create a tactical wargame, but to make military power feel modern and politically constrained.

---

## 13. Nuclear Weapons

Nuclear weapons should be represented carefully as a strategic deterrence system rather than a normal battlefield weapon.

Possible nuclear states in 1993:

- United States
- Russia
- United Kingdom
- France
- China
- Ukraine
- Belarus
- Kazakhstan
- India
- Pakistan
- Israel

Important design questions:

- How should deterrence be represented?
- Can nuclear weapons be dismantled through events?
- How should proliferation work?
- What happens during nuclear escalation?
- Should nuclear war be a game-ending crisis?

---

## 14. Population and Society

Population should be one of the strongest modern-era systems.

Important population factors:

- Total population
- Urbanization
- Birth rate
- Migration
- Education
- Ethnic identity
- Religious identity
- Regional separatism
- Labor force
- Aging population
- Refugees
- Public unrest

---

## 15. Technology Eras

Possible modern technology periods:

1. Post-Cold-War Transition, 1993-2001
2. Globalization and Internet Expansion, 2001-2008
3. Financial Crisis and Multipolarity, 2008-2014
4. Hybrid Warfare and Digital Society, 2014-2020
5. Pandemic and Supply Chain Era, 2020-2025
6. AI, Climate, and Strategic Competition, 2025 onwards

Technology should affect military, economy, administration, diplomacy, internal politics, and information control.

---

## 16. Important 1993 Event Chains

Potential early event chains:

- Russian constitutional crisis
- Yugoslav Wars
- Bosnian War
- First Chechen War buildup
- Oslo Accords
- Rwandan crisis buildup
- Somali Civil War and UN intervention
- NAFTA implementation
- Maastricht Treaty and EU development
- NATO enlargement debate
- Post-Soviet nuclear disarmament
- Chinese market reforms
- German reunification costs
- South African transition to democracy
- North Korean nuclear crisis

---

## 17. Country Priority List

### Tier 1 countries

- United States
- Russia
- China
- Germany
- France
- United Kingdom
- Japan
- India
- Ukraine
- Turkey
- Iran
- Iraq
- Saudi Arabia
- Israel
- Egypt
- Brazil
- South Africa

### Tier 2 countries and regions

- Poland
- Czech Republic
- Slovakia
- Hungary
- Romania
- Bulgaria
- Serbia / Federal Republic of Yugoslavia
- Croatia
- Bosnia and Herzegovina
- Slovenia
- Belarus
- Kazakhstan
- Georgia
- Armenia
- Azerbaijan
- North Korea
- South Korea
- Indonesia
- Mexico
- Canada
- Argentina

---

## 18. Visual Design Ideas

This document should eventually include or link to visuals such as:

- 1993 world political map
- 1993 Europe political map
- Former Soviet Union map
- NATO and EU membership map
- Global alliance/bloc diagram
- Technology-era timeline
- Government type chart
- Ideology matrix
- Economy system diagram
- Mod folder structure diagram
- Development roadmap

Recommended approach:

- Keep this file as the Markdown/text source of truth.
- Store images in a `/docs/visuals/` folder.
- Reference visuals from this document.
- Export polished versions to PDF, DOCX, or slides when needed.

Example visual reference format:

```markdown
![1993 Europe Political Map](docs/visuals/1993_europe_political_map.png)
```

---

## 19. Documentation Structure

Recommended project documentation folders:

```text
/docs
  /visuals
  /research
  /design
  /country_design
  /implementation_logs
  /roadmaps

/mod
  /common
  /history
  /events
  /localization
  /map
  /gfx
```

Suggested future files:

```text
/docs/country_design/USA_1993.md
/docs/country_design/Russia_1993.md
/docs/country_design/China_1993.md
/docs/country_design/Germany_1993.md
/docs/country_design/Ukraine_1993.md
/docs/design/governments.md
/docs/design/economy.md
/docs/design/military.md
/docs/design/international_organizations.md
/docs/roadmaps/version_0_1.md
```

---

## 20. Open Design Questions

* How detailed should internal party politics be?
* How should nuclear war be handled?
* Should the EU be represented as an international organization, a special subject system, or a unique federalization mechanic?
* Should NATO be a defensive alliance, institution, or custom diplomatic system?
* How should modern warfare avoid becoming constant world conquest?
* How should international law and sanctions restrict aggression?
* How should individual historical events be assigned to the scheduled, historically expected, or fully conditional classes?
* How should the strength of historical direction change as the campaign increasingly diverges from real history?

---

## 21. Development Principles

- Complete the global design specification before beginning implementation.
- Do not create or modify game files until the project reaches Design Freeze.
- Define global systems before writing detailed country-specific mechanics.
- Separate government form, regime character, ideology, political alignment, and state capacity.
- Use one consistent classification system for sovereign states, dependencies, de facto states, disputed territories, and non-state movements.
- Document the inputs, outputs, interactions, player choices, AI behavior, and failure states of every major mechanic.
- Clearly distinguish confirmed decisions, provisional proposals, unresolved questions, and content deferred to later releases.
- Prioritize readable and interconnected systems over unnecessary simulation detail.
- Make peaceful statecraft, economic development, diplomacy, influence, and internal politics as meaningful as warfare.
- Preserve plausible alternate history without forcing historical outcomes regardless of changing conditions.
- Keep gameplay engaging and respectful when representing wars, ethnic conflict, terrorism, repression, and humanitarian crises.
- Begin implementation only after the core design has been reviewed for consistency and formally frozen.

---

## 22. Decision Log

| Date         | Decision                                          | Reason                                                                                                                     |
| ------------ | ------------------------------------------------- | -------------------------------------------------------------------------------------------------------------------------- |
| 16 July 2026 | Campaign start date set to 1 January 1993         | Establishes one exact historical snapshot and allows developments during 1993 to occur dynamically                         |
| 16 July 2026 | Campaign has no fixed historical end date         | Allows indefinite continuation through reusable and systemic gameplay                                                      |
| 16 July 2026 | No fixed content or technology horizon            | Design work will continue until the project owner decides that the planned content is sufficient                           |
| 16 July 2026 | Historically directed sandbox selected            | Major historical developments should remain prominent while still allowing meaningful alternate outcomes                   |
| 16 July 2026 | Plausible cancellation selected                   | Historical events should not occur when earlier developments have removed their causes or made them implausible            |
| 17 July 2026 | Player represents the state itself                | Preserves normal EU5 campaign continuity through elections, coups, revolutions, government changes, and regime transitions |
| 17 July 2026 | Full EU5 simulation conversion selected           | The complete EU5 simulation will be modernized and retained, with replacement or new mechanics used only where no adequate equivalent exists |
| TBD          | First focus region: Europe + former Soviet Union  | High relevance to 1993 and manageable first scope                                                                          |
| TBD          | Version 0.1 defined as a vertical slice           | Prevents the first release from becoming too large or unfocused                                                            |
| TBD          | Placeholder content is acceptable for Version 0.1 | Allows the mod to become playable before all historical detail is complete                                                 |
| TBD          | Document will serve as central design bible       | Keeps broad context and design choices in one place                                                                        |
| 20 July 2026 | Republic of Serbian Krajina rejected as a separate entity | All starting territory is assigned to Croatia; no RSK country actor, tag, subject, or releasable |
| 20 July 2026 | Croatian Republic of Herzeg-Bosnia rejected as a separate entity | All territory is assigned to Bosnia and Herzegovina; no HZB country actor, tag, subject, releasable, or separate territorial ownership |
| 20 July 2026 | Kosovo temporarily set as standard EU5 Vassal of Federal Republic of Yugoslavia | Preserves `KOS` as a separate subject actor under `YUG`; detailed follow-up is centralized in `country_content_design_backlog.md` |
| 20 July 2026 | Northern Cyprus retained as an independent de facto country actor | Uses `TRNC`; Turkey guarantees its independence or provides the closest available defensive-protection relationship, but Northern Cyprus is not a Turkish subject |
| 20 July 2026 | All Moldova-related sub-entities consolidated under Moldova | Moldova is the only starting country actor; Transnistria and Gagauzia have no separate starting actors, subjects, or territorial ownership. Content follow-up is centralized in `country_content_design_backlog.md` |
| 20 July 2026 | Chechnya temporarily set as standard EU5 Vassal of Russia | Retains `CHE` as a separate subject actor under `RUS`; detailed follow-up is centralized in `country_content_design_backlog.md` |
| 20 July 2026 | Eritrea starts as an independent country | Uses `ERI` as an independent starting actor with no Ethiopian subject relationship; detailed follow-up is centralized in `country_content_design_backlog.md` |
| 20 July 2026 | Country-content follow-up centralized and archived documents made read-only | Detailed country-content requirements belong only in `country_content_design_backlog.md`; only the current non-archived design bible is updated |
| 20 July 2026 | Somaliland consolidated into Somalia at campaign start | Somalia is the only starting country actor for all Somali territory; Somaliland has no separate actor, subject, technical tag, or separate ownership, and detailed follow-up is centralized in `country_content_design_backlog.md` |
| 20 July 2026 | China and Taiwan start as separate countries | `CHN` and `TWN` are independent starting actors with reciprocal claims and cores; Taiwan has United States defensive protection, with detailed follow-up centralized in `country_content_design_backlog.md` |
| 20 July 2026 | Georgian regional entities consolidated at campaign start | Abkhazia, South Ossetia, and Adjara are assigned to Georgia; none has separate starting representation, and detailed follow-up is centralized in `country_content_design_backlog.md` |
| 20 July 2026 | Nagorno-Karabakh / Artsakh consolidated into Azerbaijan at campaign start | All Nagorno-Karabakh territory is assigned to Azerbaijan; no separate starting actor, subject, technical tag, or territorial ownership, with detailed follow-up centralized in `country_content_design_backlog.md` |
| 20 July 2026 | Parent-state default adopted for comparable unresolved separatist administrations | Such regions remain part of their recognized parent state and are handled through country content unless the project owner explicitly approves a separate starting actor; existing locked exceptions remain unchanged |
| 20 July 2026 | Republika Srpska rejected as a separate entity | All starting territory is assigned to Bosnia and Herzegovina; no separate country actor, tag, subject, releasable, or territorial ownership |
| 20 July 2026 | Nakhchivan set as a standard EU5 Vassal of Azerbaijan | Uses `NAK` as a separate subject actor controlling the exclave under `AZE`; detailed follow-up is centralized in `country_content_design_backlog.md` |
| 20 July 2026 | Tatarstan consolidated into Russia at campaign start | All Tatarstan territory is assigned to Russia; no separate starting actor, subject, tag, or territorial ownership; detailed follow-up is centralized in `country_content_design_backlog.md` |
| 20 July 2026 | Crimea consolidated directly into Ukraine at campaign start | All Crimean territory, including Sevastopol, is assigned to Ukraine; no separate starting actor, subject, tag, or territorial ownership; detailed follow-up is centralized in `country_content_design_backlog.md` |
| 20 July 2026 | GIA classified as internal Algeria content | Algeria remains the sole starting country actor for its territory; GIA receives no separate country, subject, tag, or ownership, with detailed follow-up in `country_content_design_backlog.md` |
| 20 July 2026 | Kurdish regions retained within Iraq, Turkey, Iran, and Syria | No unified Kurdish starting country or subject; all relevant territory remains with the four recognized states, while regional organizations and possible future paths are handled through `country_content_design_backlog.md` |
| 20 July 2026 | Western Sahara set as a standard EU5 Vassal of Morocco | `WSA` controls all Western Sahara territory under `MOR`; Polisario is internal West Saharan content, and detailed follow-up is centralized in `country_content_design_backlog.md` |
| 20 July 2026 | Southern Lebanon retained entirely within Lebanon | `LEB` owns all Lebanese territory at campaign start; the southern security zone and its associated organizations are internal Lebanon content with detailed follow-up in `country_content_design_backlog.md` |
| 20 July 2026 | Five provisional entities consolidated into parent states | Southern Iraqi opposition is internal `IRQ` content; Mayotte belongs directly to `FRA`; NPFL is internal `LBR` content; RUF is internal `SLE` content; RPF is internal `RWA` content. None receives a separate starting actor, subject, tag, or territorial ownership; detailed follow-up is centralized in `country_content_design_backlog.md`. |
| 21 July 2026 | Five additional provisional entities consolidated into parent states | Réunion belongs directly to `FRA`; Saint Helena, Ascension and Tristan da Cunha belong directly to `GBR`; SPLA is internal `SUD` content; ULIMO is internal `LBR` content; UNITA is internal `ANG` content. None receives a separate starting actor, subject, tag, or territorial ownership; detailed follow-up is centralized in `country_content_design_backlog.md`. |
| 21 July 2026 | Five South Asian and Indian Ocean entries consolidated into parent states | Azad Jammu and Kashmir and Gilgit-Baltistan are internal `PAK` content; British Indian Ocean Territory / Diego Garcia belongs directly to `GBR`; Hezb-e Islami Gulbuddin and Hezb-e Wahdat are internal `AFG` content. None receives a separate starting actor, subject, tag, or territorial ownership; detailed follow-up is centralized in `country_content_design_backlog.md`. |
| 21 July 2026 | Five Central and South Asian entries consolidated into parent states | The later IMU precursor networks are internal `UZB` content; Ittihad-i Islami, Jamiat-e Islami / the Rabbani government, and Junbish-i Milli are internal `AFG` content; the Jammu and Kashmir government is internal `IND` administration content. None receives a separate starting actor, subject, tag, or territorial ownership; detailed follow-up is centralized in `country_content_design_backlog.md`. |
| 21 July 2026 | Five South, Central, and East Asian entries classified | LTTE is internal `LKA` content; Northeast Indian insurgents are internal `IND` content; Tajik Opposition is internal `TAJ` content; Guangxi is internal `CHN` content; Hong Kong is a separate `HKG` country actor and standard EU5 Vassal of `GBR`. Detailed follow-up is centralized in `country_content_design_backlog.md`. |
| 21 July 2026 | Tibet set as a Chinese Vassal; other Chinese regional decisions retained | Tibet is a separate `TIB` country actor and standard EU5 Vassal of `CHN`; Xinjiang, Inner Mongolia, and Ningxia remain internal `CHN` content with direct Chinese ownership; Macau remains a separate `MAC` country actor and standard EU5 Vassal of `POR`. The Tibetan Government-in-Exile remains separately classified; detailed follow-up is centralized in `country_content_design_backlog.md`. |
| 22 July 2026 | Five Southeast Asian armed organizations consolidated into parent-state content | KNU, KIO, and Arakan / Rakhine insurgent actors are internal `MYA` content; Khmer Rouge is internal `CAM` content; New People's Army is internal `PHI` content. None receives a separate starting actor, subject, tag, or territorial ownership; detailed follow-up is centralized in `country_content_design_backlog.md`. |
| 22 July 2026 | Myanmar groups internalized and Pacific dependency representation locked | Shan armed groups and Wa State / UWSA are internal `MYA` content; Bougainville is internal `PNG` content; American Samoa is a separate `ASM` country actor and standard EU5 Vassal of `USA`. Christmas Island, Cocos (Keeling), and Norfolk Island belong directly to `AST`; New Caledonia, French Polynesia, and Wallis and Futuna to `FRA`; Guam and Northern Mariana Islands to `USA`; Cook Islands, Niue, and Tokelau to `NZL`; and Pitcairn to `GBR`. Palau remains unchanged; detailed follow-up is centralized in `country_content_design_backlog.md`. |
| 22 July 2026 | Final two provisional entity classifications locked | Senkaku / Diaoyu is internal `JAP` territory with `CHN` and `TWN` claims; South Georgia and the South Sandwich Islands belong directly to `GBR` with an `ARG` claim. Neither receives a separate actor, subject, tag, or territorial ownership. The entity re-review now has 0 provisional cases. |
| 22 July 2026 | Full political-territorial registry migrated; Palestine, East Timor, and global island-dependency rules locked | The active registry now contains 349 entries: 202 starting country actors and 147 non-country political/territorial entries. State of Palestine begins as `PAL`; East Timor and Fretilin are internal `IDN` content; non-sovereign island dependencies belong directly to their administering states except the locked Vassal exceptions and transitional Palau. Institutional organizations remain outside this registry. |
| TBD          | Use the generic Vassal subject type for all subject relationships until the modern subject system is reviewed and decided | Temporary placeholder; the subject types, names, and mechanics must be reconsidered later |

---

## 23. Glossary

| Term | Meaning in this project |
|---|---|
| Design bible | Central document defining the mod vision, systems, scope, and decisions |
| Total conversion | A mod that changes the game setting, map data, countries, mechanics, and content extensively |
| Vertical slice | A limited but playable version proving the core concept |
| Bloc | A diplomatic, military, or economic grouping such as NATO, EU, CIS, or ASEAN |
| Regime type | The form and political character of a government |
| De facto state | A political entity with practical control over territory but limited recognition |

---

## 24. Next Steps

The project will complete its full design before any implementation work begins.

### Design Phase 1: Foundational Decisions

1. The campaign starts on 1 January 1993 and has no fixed historical end date.
2. Historical, technological, political, economic, social, and speculative content will continue to be expanded without a fixed content horizon until the project owner decides that the planned design is sufficient.
3. The campaign follows a historically directed sandbox model: major historical developments are strongly encouraged when their underlying conditions remain plausible.
4. Historical events use plausible cancellation and must be cancelled, delayed, replaced, or transformed when earlier developments remove their causes or make their historical form implausible.
5. The player represents the state itself and normally retains control through elections, government changes, coups, revolutions, regime transitions, and leadership succession.
6. The principal gameplay loop includes domestic politics, institutional reform, economic management, development, diplomacy, international organizations, trade, investment, sanctions, military modernization, warfare, intelligence, covert action, technology, research, demographics, migration, social policy, regional integration, bloc leadership, crisis management, historical events, territorial change, state formation, soft power, culture, information, and global influence.
7. The mod follows a simulation-heavy approach: major modern state systems should be modeled directly and in substantial detail, while abstraction is reserved for low-value bookkeeping, excessive micromanagement, unclear information, disproportionate performance costs, or confirmed technical limitations.

### Design Phase 2: World Entity Framework

1. Create a universal classification system for sovereign states, dependencies, autonomous territories, de facto states, occupied territories, disputed territories, insurgent administrations, separatist movements, rebel factions, and abstract movements.
2. Define the gameplay rights and restrictions associated with each category.
3. Define recognition, territorial control, claims, autonomy, independence, annexation, release, reunification, and state-collapse rules.
4. Apply the classification system consistently across every regional 1993 country list.
5. Resolve duplicated entries, inconsistent proposed identifiers, and conflicting entity classifications.
6. Maintain the migrated 349-entry global entity registry as the authoritative political-territorial world-roster document.

### Design Phase 3: Politics and Government

1. Separate government form, regime character, ideology, political alignment, state capacity, and economic policy into distinct design dimensions.
2. Define elections, leadership succession, term limits, coalition formation, coups, revolutions, democratization, authoritarian consolidation, and state failure.
3. Define political factions or interest groups and how they influence policy.
4. Define legitimacy, stability, corruption, repression, civil liberties, military loyalty, and reform pressure.
5. Specify how domestic politics creates player choices, risks, and alternate political paths.

### Design Phase 4: Diplomacy and International Organizations

1. Define recognition, diplomatic relations, alliances, guarantees, access agreements, foreign bases, sanctions, embargoes, aid, intervention, and peacekeeping.
2. Design a reusable international-organization framework.
3. Specify the United Nations, NATO, European Union, CIS, OSCE, OAU/African Union, ASEAN, Arab League, GCC, OPEC, NAFTA, Mercosur, and GATT/WTO.
4. Define membership requirements, institutional powers, internal voting, expansion, suspension, withdrawal, and dissolution.
5. Define international responses to aggressive war, occupation, atrocities, nuclear proliferation, and treaty violations.

### Design Phase 5: Economy and Society

1. Define national economic capacity, government revenue, expenditure, debt, inflation, unemployment, and financial crises.
2. Define production, services, trade, strategic resources, energy dependency, foreign investment, sanctions, and economic development.
3. Define population, urbanization, education, workforce, living standards, inequality, demographic change, migration, and refugees.
4. Define how economic and social conditions affect politics, unrest, military capacity, diplomacy, and technological development.
5. Establish the complete modern goods, industries, and economic-policy framework.

### Design Phase 6: Military, Security, and Nuclear Weapons

1. Define professional forces, conscription, reserves, mobilization, readiness, logistics, military spending, and equipment.
2. Define land, air, naval, missile, special-forces, insurgency, counterinsurgency, proxy-war, and peacekeeping systems.
3. Define occupation, war exhaustion, civilian costs, reconstruction, armistices, and peace settlements.
4. Design nuclear capability, deterrence, proliferation, sharing, disarmament, escalation, retaliation, and nuclear-war consequences.
5. Define political and international constraints that prevent modern warfare from becoming unrestricted map conquest.

### Design Phase 7: Technology and Global Change

1. Create the complete technology-era structure from 1993 to the final end date.
2. Define research capacity, technology diffusion, modernization, and technological dependency.
3. Design globalization, the internet, digital society, cyber capabilities, climate policy, biotechnology, automation, space activity, and artificial intelligence.
4. Define how global crises and technological shifts alter economics, politics, diplomacy, society, and warfare.

### Design Phase 8: Country and Regional Content

1. Create a standard country-design template.
2. Define starting political, economic, demographic, diplomatic, and military conditions for every country.
3. Design regional conflict frameworks and major country-specific mechanics.
4. Design conditional historical events and plausible alternate-history branches.
5. Establish country priorities for the first release without leaving the rest of the world mechanically undefined.

### Design Phase 9: Integration and Design Freeze

1. Document the inputs, outputs, player decisions, AI behavior, and interactions of every major system.
2. Check the complete design for contradictions, duplicated mechanics, missing feedback loops, and unnecessary complexity.
3. Separate Version 0.1 requirements from later-release content.
4. Complete the decision log and unresolved-question register.
5. Create a master design-document index.
6. Conduct a final design review.
7. Declare Design Freeze before beginning any implementation work.
