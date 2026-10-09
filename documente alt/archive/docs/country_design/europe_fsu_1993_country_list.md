# Europe + Former Soviet Union 1993 Country List

## Purpose

This file defines the initial Version 0.1 country setup for Europe and the former Soviet Union in the 1993 start date. It is considered draft-complete for the main sovereign-state pass, with remaining work focused on implementation choices for microstates, autonomous regions, and de facto / rebel entities.

It should track:
- Country name
- Proposed EU5 tag
- Capital
- Government type
- Alignment / bloc
- 1993 status
- Notes for borders, conflicts, claims, and implementation

---

## Tag Rules

- Prefer recognizable three-letter tags.
- Avoid conflicts with existing EU-style tags where possible.
- Use placeholder tags until EU5 tag constraints are known.
- Use standard EU5 country and subject types wherever possible; do not invent custom entity or subject types unless the project owner explicitly approves them.
- De facto, breakaway, rebel, and autonomous entities may receive tags later if gameplay needs justify them.
- Avoid duplicate implementation entries; cross-region references should point back to the primary row.

---

## Categories

1. Western Europe
2. Nordic Europe
3. Central Europe
4. Eastern Europe
5. Balkans / Yugoslav Wars
6. Baltic States
7. Russia and Slavic former Soviet states
8. Caucasus
9. Central Asia
10. Turkey and bridge regions

---

## 1. Western Europe

| Country | Proposed tag | Capital | Government type | Alignment / bloc | 1993 status | Notes |
|---|---:|---|---|---|---|---|
| Germany | GER | Berlin | Federal parliamentary republic | EU / NATO | Reunified state | Recently reunified; former East Germany integrated. |
| France | FRA | Paris | Semi-presidential republic | EU / NATO | Stable major power | Nuclear state; permanent UN Security Council member. |
| United Kingdom | GBR | London | Constitutional monarchy / parliamentary democracy | EU / NATO | Stable major power | Nuclear state; permanent UN Security Council member. |
| Ireland | IRE | Dublin | Parliamentary republic | EU / neutral-leaning | Stable state | Not a NATO member; Northern Ireland issue affects regional politics. |
| Netherlands | HOL | Amsterdam | Constitutional monarchy / parliamentary democracy | EU / NATO | Stable state | Amsterdam as constitutional capital; government seated in The Hague. |
| Belgium | BEL | Brussels | Constitutional monarchy / federalizing parliamentary democracy | EU / NATO | Stable but internally divided | Federalization reforms ongoing in 1993. |
| Luxembourg | LUX | Luxembourg | Constitutional monarchy / parliamentary democracy | EU / NATO | Stable microstate | Important finance and EU institution role. |
| Switzerland | SWI | Bern | Federal republic / direct democracy | Neutral | Stable neutral state | Not EU or NATO; strong banking and alpine defense identity. |
| Austria | AUS | Vienna | Federal parliamentary republic | Neutral / EU applicant | Stable neutral state | Not yet EU member in 1993; joined in 1995. |
| Italy | ITA | Rome | Parliamentary republic | EU / NATO | Stable but politically turbulent | Early 1990s Tangentopoli crisis and party system collapse. |
| Spain | SPA | Madrid | Constitutional monarchy / parliamentary democracy | EU / NATO | Stable democratic state | Post-Franco democratic consolidation. |
| Portugal | POR | Lisbon | Semi-presidential republic | EU / NATO | Stable democratic state | Post-authoritarian democracy consolidated. |
| Andorra | AND | Andorra la Vella | Parliamentary co-principality | Neutral / European microstate | Microstate | 1993 constitution adopted; modern sovereignty status clarified. |
| Monaco | MCO | Monaco | Constitutional monarchy | Neutral / European microstate | Microstate | Closely tied to France. |
| San Marino | SMR | San Marino | Parliamentary republic | Neutral / European microstate | Microstate | Independent enclave within Italy. |
| Vatican City | VAT | Vatican City | Ecclesiastical elective monarchy | Neutral / Holy See | Microstate / special entity | May be represented as a special government, event-only state, or non-playable entity. |
| Malta | MLT | Valletta | Parliamentary republic | Neutral / European state | Stable state | Not EU or NATO in 1993; EU accession much later. |

---

## 2. Nordic Europe

| Country | Proposed tag | Capital | Government type | Alignment / bloc | 1993 status | Notes |
|---|---:|---|---|---|---|---|
| Denmark | DEN | Copenhagen | Constitutional monarchy / parliamentary democracy | EU / NATO | Stable state | EU and NATO member; starts as overlord of the Faroe Islands and Greenland through standard EU5 Vassal subject relationships. |
| Norway | NOR | Oslo | Constitutional monarchy / parliamentary democracy | NATO / non-EU | Stable state | NATO member; not an EU member. Strong North Sea oil economy. |
| Sweden | SWE | Stockholm | Constitutional monarchy / parliamentary democracy | Neutral / EU applicant | Stable neutral state | Not yet EU member in 1993; joined in 1995. Historically neutral but increasingly West-aligned. |
| Finland | FIN | Helsinki | Parliamentary republic | Neutral / EU applicant | Stable neutral state | Not yet EU member in 1993; joined in 1995. Balances Western integration with post-Cold War Russian relations. |
| Iceland | ICE | Reykjavik | Parliamentary republic | NATO / non-EU | Stable state | NATO member without a standing army; strategically important North Atlantic location. |
| Faroe Islands | FAR | Torshavn | Autonomous territorial government | Vassal of Denmark / non-EU | Danish vassal subject | Historical autonomy is retained, but gameplay uses the standard EU5 Vassal subject type under Denmark rather than a custom autonomy subject. |
| Greenland | GRL | Nuuk | Autonomous territorial government | Vassal of Denmark / non-EU | Danish vassal subject | Historical autonomy is retained, but gameplay uses the standard EU5 Vassal subject type under Denmark rather than a custom autonomy subject. |
| Åland | — | Mariehamn | Autonomous demilitarized region within Finland | Finland | Part of Finland | No separate country, subject, or tag. Use normal Finnish ownership; represent autonomy and demilitarization through modifiers or regional rules. |

---

## 3. Central Europe

| Country | Proposed tag | Capital | Government type | Alignment / bloc | 1993 status | Notes |
|---|---:|---|---|---|---|---|
| Poland | POL | Warsaw | Parliamentary republic | Post-Warsaw Pact / West-leaning | Stable transition state | Major post-communist state; pursuing NATO and EU integration. |
| Czech Republic | CZE | Prague | Parliamentary republic | Post-Warsaw Pact / West-leaning | Newly independent state | Created after the peaceful dissolution of Czechoslovakia on 1 January 1993. |
| Slovakia | SVK | Bratislava | Parliamentary republic | Post-Warsaw Pact / West-leaning | Newly independent state | Created after the peaceful dissolution of Czechoslovakia on 1 January 1993. |
| Hungary | HUN | Budapest | Parliamentary republic | Post-Warsaw Pact / West-leaning | Stable transition state | Post-communist democracy; pursuing Western integration. |
| Liechtenstein | LIE | Vaduz | Constitutional monarchy | Neutral / European microstate | Microstate | Closely tied to Switzerland; possible microstate tag or non-playable entity. |

---

## 4. Eastern Europe

| Country | Proposed tag | Capital | Government type | Alignment / bloc | 1993 status | Notes |
|---|---:|---|---|---|---|---|
| Romania | ROM | Bucharest | Semi-presidential republic | Post-communist / West-leaning | Transition state | Post-Ceaușescu state with difficult democratic and economic transition. |
| Bulgaria | BUL | Sofia | Parliamentary republic | Post-communist / West-leaning | Transition state | Former Warsaw Pact state; not yet NATO or EU member. |
| Moldova | MOL | Chișinău | Parliamentary republic | Post-Soviet / CIS-leaning | Fragile newly independent state with internal autonomy and separatist challenges | Moldova is the only starting country actor for all internationally recognized Moldovan territory, including Transnistria and Gagauzia. Neither region receives a separate starting country actor, subject, or separate territorial ownership. Content follow-up is centralized in `country_content_design_backlog.md`. Registry status: LOCKED. |
| Transnistria | — | Tiraspol | Internal separatist administration within Moldova | Moldovan territory / Russian-backed local authority | Internal Moldova content | No separate starting country actor, subject, or territorial ownership. Content follow-up is centralized in `country_content_design_backlog.md`. Registry status: LOCKED. |
| Gagauzia | — | Comrat | Internal autonomous / separatist region within Moldova | Moldovan territory / Gagauz regional politics | Internal Moldova content | No separate starting country actor, subject, or territorial ownership. Content follow-up is centralized in `country_content_design_backlog.md`. Registry status: LOCKED. |

---

## 5. Balkans / Yugoslav Wars

| Country | Proposed tag | Capital | Government type | Alignment / bloc | 1993 status | Notes |
|---|---:|---|---|---|---|---|
| Slovenia | SLV | Ljubljana | Parliamentary republic | Post-Yugoslav / West-leaning | Newly independent state | Internationally recognized; largely escaped prolonged war after 1991 Ten-Day War. |
| Croatia | CRO | Zagreb | Semi-presidential republic | Post-Yugoslav / West-leaning | At war / internal conflict | All Croatian territory is assigned to Croatia in the starting setup. The Republic of Serbian Krajina is rejected as a separate entity and receives no tag, subject, releasable, or starting actor. Content follow-up is centralized in `country_content_design_backlog.md`. Registry status: LOCKED. |
| Bosnia and Herzegovina | BOS | Sarajevo | Republic / wartime government | Internationally recognized / besieged | At war / internal conflict | All internationally recognized Bosnian territory is assigned to Bosnia and Herzegovina in the starting setup. Republika Srpska and the Croatian Republic of Herzeg-Bosnia are rejected as separate entities and receive no country actors, tags, subjects, releasables, or separate territorial ownership. Content follow-up is centralized in `country_content_design_backlog.md`. Registry status: LOCKED. |

| Croatian Republic of Herzeg-Bosnia | — | Mostar | Former Bosnian Croat wartime authority | Croatian-backed internal Bosnian content | No separate entity | All territory is assigned to Bosnia and Herzegovina. No country actor, technical tag, subject, releasable, or separate territorial ownership. Content follow-up is centralized in `country_content_design_backlog.md`. Registry status: LOCKED. |
| Federal Republic of Yugoslavia | YUG | Belgrade | Federal republic | Serbia-Montenegro / sanctioned | Sole starting Yugoslav country | Starts as one country containing Serbia and Montenegro; under sanctions and involved in the Yugoslav Wars. |
| Serbia | SER | Belgrade | Republic within FR Yugoslavia | FR Yugoslavia | Internal constituent / releasable | Not a separate starting actor. Its territory is part of `YUG`; `SER` is retained only as a releasable tag for dissolution or separation paths. Registry status: LOCKED. |
| Montenegro | MNT | Podgorica | Republic within FR Yugoslavia | FR Yugoslavia | Internal constituent / releasable | Not a separate starting actor. Its territory is part of `YUG`; `MNT` is retained only as a releasable tag for dissolution or separation paths. Registry status: LOCKED. |
| Kosovo | KOS | Pristina | Autonomous territorial government | Vassal of Federal Republic of Yugoslavia | Yugoslav vassal subject | Starts as a standard EU5 Vassal of `YUG`, while Yugoslav/Serbian sovereignty and the underlying Kosovo dispute remain part of its historical context. This is a temporary representation decision. Detailed country-content follow-up is centralized in `country_content_design_backlog.md`. Registry status: LOCKED. |
| Macedonia | MKD | Skopje | Parliamentary republic | Post-Yugoslav / non-aligned | Newly independent state | Internationally known at the time as the former Yugoslav Republic of Macedonia due to naming dispute with Greece. |
| Albania | ALB | Tirana | Parliamentary republic | Post-communist / non-aligned | Transition state | Recently ended communist isolation; economically and politically unstable. |
| Greece | GRE | Athens | Parliamentary republic | EU / NATO | Stable state | EU and NATO member; Macedonia naming dispute affects diplomacy. |
| Cyprus | CYP | Nicosia | Presidential republic | Non-aligned / Europe-facing | Divided island state | Controls the south and claims the entire island; Northern Cyprus is represented as a separate de facto country actor guaranteed by Turkey. |
| Northern Cyprus | TRNC | North Nicosia | De facto republic | Independent country guaranteed by Turkey | Independent de facto country | Starts as an independent country actor using `TRNC`, not as a Turkish subject. Turkey guarantees its independence or provides the closest available defensive-protection relationship. Recognition remains limited to Turkey, and the Republic of Cyprus continues to claim the territory. Registry status: LOCKED. |

---

## 6. Baltic States

| Country | Proposed tag | Capital | Government type | Alignment / bloc | 1993 status | Notes |
|---|---:|---|---|---|---|---|
| Estonia | EST | Tallinn | Parliamentary republic | Post-Soviet / West-leaning | Newly restored independent state | Russian troop withdrawal and minority questions are key early-1990s issues. |
| Latvia | LAT | Riga | Parliamentary republic | Post-Soviet / West-leaning | Newly restored independent state | Russian-speaking minority and citizenship issues are important domestic factors. |
| Lithuania | LIT | Vilnius | Semi-presidential republic | Post-Soviet / West-leaning | Newly restored independent state | First Soviet republic to declare restored independence; pursuing Western integration. |

---

## 7. Russia and Slavic Former Soviet States

| Country | Proposed tag | Capital | Government type | Alignment / bloc | 1993 status | Notes |
|---|---:|---|---|---|---|---|
| Russia | RUS | Moscow | Federal semi-presidential republic | CIS / post-Soviet great power | Unstable successor state with Tatarstan consolidated | All Tatarstan territory is assigned to Russia at campaign start. Detailed follow-up is centralized in `country_content_design_backlog.md`. |
| Ukraine | UKR | Kyiv | Semi-presidential republic | Post-Soviet / non-aligned | Sovereign state with Crimea consolidated | All Crimean territory, including Sevastopol, is assigned directly to Ukraine at campaign start. Detailed follow-up is centralized in `country_content_design_backlog.md`. |
| Belarus | BLR | Minsk | Parliamentary republic | Post-Soviet / CIS | Newly independent state | Still pre-Lukashenko at 1993 start; close economic and political ties with Russia. |
| Chechnya | CHE | Grozny | Separatist republic represented as subject | Standard EU5 Vassal of Russia | Temporary Russian subject | Starts as a separate `CHE` country actor and standard EU5 Vassal of Russia (`RUS`). This is a temporary representation. Detailed country-content follow-up is centralized in `country_content_design_backlog.md`. Registry status: LOCKED. |
| Tatarstan | — | Kazan | Internal autonomous republic within Russia | Russian Federation / regional autonomy | Internal Russia content | No separate starting country actor, subject, technical tag, or territorial ownership. Detailed follow-up is centralized in `country_content_design_backlog.md`. Registry status: LOCKED. |
| Crimea | — | Simferopol | Internal autonomous republic within Ukraine | Ukrainian sovereignty / Russian influence | Internal Ukraine content | No separate starting country actor, subject, technical tag, or territorial ownership. All Crimean territory, including Sevastopol, belongs directly to Ukraine. Detailed follow-up is centralized in `country_content_design_backlog.md`. Registry status: LOCKED. |

---

## 8. Caucasus

| Country | Proposed tag | Capital | Government type | Alignment / bloc | 1993 status | Notes |
|---|---:|---|---|---|---|---|
| Georgia | GEO | Tbilisi | Parliamentary / presidential transition republic | Post-Soviet / unstable | Sovereign state with all Georgian regional entities consolidated | Abkhazia, South Ossetia, and Adjara are assigned to Georgia at campaign start. None has a separate starting actor, subject, technical tag, or territorial ownership. Detailed follow-up is centralized in `country_content_design_backlog.md`. Registry status: LOCKED. |
| Abkhazia | — | Sukhumi | Internal separatist administration within Georgia | Georgian territory / Abkhaz separatist authorities | Internal Georgia content | No separate starting country actor, subject, or territorial ownership. Detailed follow-up is centralized in `country_content_design_backlog.md`. Registry status: LOCKED. |
| South Ossetia | — | Tskhinvali | Internal separatist region within Georgia | Georgian territory / local separatist administration | Internal Georgia content | No separate starting country actor, subject, technical tag, or territorial ownership. Detailed follow-up is centralized in `country_content_design_backlog.md`. Registry status: LOCKED. |
| Adjara | — | Batumi | Internal autonomous region within Georgia | Georgian sovereignty / local autonomy | Internal Georgia content | No separate starting country actor, subject, technical tag, or territorial ownership. Detailed follow-up is centralized in `country_content_design_backlog.md`. Registry status: LOCKED. |
| Armenia | ARM | Yerevan | Semi-presidential republic | Post-Soviet / Russia-leaning | Newly independent state at war | Nagorno-Karabakh remains external conflict and country-content context; Armenia receives no ownership through a separate Artsakh actor. |
| Azerbaijan | AZE | Baku | Presidential republic | Post-Soviet / Turkey-leaning | Sovereign state with Nagorno-Karabakh consolidated into Azerbaijan | All Nagorno-Karabakh territory is assigned to Azerbaijan at campaign start. Detailed follow-up is centralized in `country_content_design_backlog.md`. |
| Nagorno-Karabakh / Artsakh | — | Stepanakert | Internal separatist administration within Azerbaijan | Azerbaijani territory / Armenian-backed local administration | Internal Azerbaijan content | No separate starting country actor, subject, technical tag, or territorial ownership. Detailed follow-up is centralized in `country_content_design_backlog.md`. Registry status: LOCKED. |
| Nakhchivan | NAK | Nakhchivan | Autonomous republic represented as a subject state | Standard EU5 Vassal of Azerbaijan | Azerbaijani vassal exclave | Separate `NAK` country actor controlling Nakhchivan as a standard EU5 Vassal of Azerbaijan (`AZE`). Detailed follow-up is centralized in `country_content_design_backlog.md`. Registry status: LOCKED. |

---

## 9. Central Asia

| Country | Proposed tag | Capital | Government type | Alignment / bloc | 1993 status | Notes |
|---|---:|---|---|---|---|---|
| Kazakhstan | KAZ | Almaty | Presidential republic | CIS / post-Soviet | Newly independent state | Capital still Almaty in 1993; nuclear weapons inherited from USSR pending disarmament. |
| Uzbekistan | UZB | Tashkent | Presidential republic | CIS / post-Soviet | Newly independent authoritarian state | Uzbekistan remains the only starting country actor. The precursor networks of the later Islamic Movement of Uzbekistan are internal Uzbek and cross-border content, with no separate starting actor, subject, tag, or territorial ownership. Detailed follow-up is centralized in `country_content_design_backlog.md`. Registry status: LOCKED for the organization entry. |
| Turkmenistan | TKM | Ashgabat | Presidential republic | CIS / post-Soviet | Newly independent authoritarian state | Gas-rich state under Saparmurat Niyazov. |
| Kyrgyzstan | KYR | Bishkek | Presidential republic | CIS / post-Soviet | Newly independent state | Comparatively reformist early post-Soviet trajectory. |
| Tajikistan | TAJ | Dushanbe | Presidential / wartime government | CIS / post-Soviet | Civil war state | Tajikistan remains the only starting country actor and territorial owner. The Tajik Opposition is internal Tajik conflict content with no separate starting actor, subject, technical tag, or territorial ownership. Detailed follow-up is centralized in `country_content_design_backlog.md`. Registry status: LOCKED for the opposition entry. |
| Tajik Opposition | — | Various / field command | Internal Tajik political and armed coalition | Tajikistan | Internal Tajikistan content | No separate starting country actor, subject, technical tag, or territorial ownership. Represent through Tajikistan’s civil-war, regional-control, negotiation, and event content. Registry status: LOCKED. |

---

## 10. Turkey and Bridge Regions

| Country | Proposed tag | Capital | Government type | Alignment / bloc | 1993 status | Notes |
|---|---:|---|---|---|---|---|
| Turkey | TUR | Ankara | Parliamentary republic | NATO / Europe-Middle East bridge | Stable state with Kurdish regions consolidated | All Turkish Kurdish territory remains assigned directly to Turkey. Detailed follow-up is centralized in `country_content_design_backlog.md`. |
| Turkish Kurdistan / PKK Insurgency | — | Regional content | Internal political and security issue | Turkey | Internal Turkey content | No separate starting country actor, subject, technical tag, or territorial ownership. Detailed follow-up is centralized in `country_content_design_backlog.md`. |
| Cyprus issue | CYP-TRNC | Nicosia / North Nicosia | Cross-reference | Greece-Turkey / UN dispute | Diplomatic flashpoint | Use the Cyprus and Northern Cyprus rows in section 5 as the primary implementation entries; this row is only a Turkey-region diplomacy reminder. |
| Thrace / Turkish Straits | STR | Istanbul / Çanakkale | Strategic region | Turkish sovereignty / international importance | Strategic region | Not a country; should be represented through modifiers, naval access, or strait-control mechanics. |
