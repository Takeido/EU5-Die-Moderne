# Middle East + North Africa 1993 Country List

## Purpose

This file defines the initial Version 0.1 country setup for the Middle East and North Africa in the 1993 start date. It follows the Europe + Former Soviet Union country-list template and is intended as a first-pass regional baseline before province mapping.

It should track:
- Country name
- Proposed EU5 tag
- Capital
- Government type
- Alignment / bloc
- 1993 status
- Notes for borders, conflicts, claims, and implementation
- Recommended implementation role
- Start-date priority for Version 0.1

---

## Tag Rules

- Prefer recognizable three-letter tags.
- Avoid conflicts with existing EU-style tags where possible.
- Use placeholder tags until EU5 tag constraints are known.
- De facto, breakaway, rebel, occupied, and autonomous entities may receive tags later if gameplay needs justify them.
- Dependencies, occupied territories, and disputed regions may be represented as subjects, special provinces, modifiers, or event-only entities rather than normal playable tags.
- Use normal playable tags for internationally recognized sovereign states.
- Use non-playable, event, subject, autonomy, or rebel tags for entities that did not function as normal sovereign states in 1993.
- Avoid giving normal country status to occupied territories unless the engine needs them as special diplomatic or unrest containers.

---

## Categories

1. Levant and Israel-Palestine
2. Arabian Peninsula and Gulf
3. Iraq-Iran region
4. North Africa
5. Western Sahara and regional disputes
6. Implementation priorities

---

## 1. Levant and Israel-Palestine

| Country | Proposed tag | Capital | Government type | Alignment / bloc | 1993 status | Notes |
|---|---:|---|---|---|---|---|
| Israel | ISR | Jerusalem | Parliamentary republic | US-aligned / regional military power | Stable state / peace process | Oslo process begins in 1993; capital status disputed internationally. |
| State of Palestine | PAL | Tunis / Gaza-Ramallah later | Partially recognized republic represented as a state actor | Arab-backed / peace process | Separate starting country actor under occupation constraints | Begins as a separate starting country actor. The West Bank and Gaza Strip remain occupied-territory records under Israeli military and security constraints. The PLO is internal Palestinian political content. Registry status: LOCKED. |
| Palestine Liberation Organization | — | Tunis / field offices | Internal Palestinian political organization | State of Palestine / peace process | Internal Palestine content | No separate country actor or technical tag. Political leadership, diplomacy, and the Oslo transition are represented inside Palestine content. Registry status: LOCKED. |
| West Bank | — | East Jerusalem / Ramallah | Occupied Palestinian territory | State of Palestine / Israeli military and security control | Occupied territorial record | Part of the Palestinian starting-state design but not a separate actor or tag. Represent occupation, settlements, autonomy, unrest, and claims through territorial and country mechanics. Registry status: LOCKED. |
| Gaza Strip | — | Gaza City | Occupied Palestinian territory | State of Palestine / Israeli military and security control | Occupied territorial record | Part of the Palestinian starting-state design but not a separate actor or tag. Represent occupation, local administration, unrest, and the Oslo transition through territorial and country mechanics. Registry status: LOCKED. |
| Jordan | JOR | Amman | Constitutional monarchy | US-aligned / Arab state | Stable state | Peace treaty with Israel follows in 1994; Palestinian population and Iraq ties relevant. |
| Lebanon | LEB | Beirut | Confessional parliamentary republic | Syrian-influenced | Sovereign state with southern security zone consolidated | All Lebanese territory, including the southern security zone, is assigned directly to Lebanon at campaign start. The SLA and Israeli military presence are represented through internal Lebanon content. Detailed follow-up is centralized in `country_content_design_backlog.md`. |
| Syria | SYR | Damascus | Ba'athist presidential republic | Russia/Soviet legacy / anti-Israel | Stable authoritarian state with Kurdish regions consolidated | All Syrian Kurdish territory remains assigned directly to Syria. Detailed follow-up is centralized in `country_content_design_backlog.md`. |
| Golan Heights | GOL | Quneitra / Katzrin | Occupied territory | Israeli control / Syrian claim | Occupied disputed territory | Captured by Israel in 1967 and annexed under Israeli law; internationally disputed. Prefer province modifier, Syrian claim, and Israeli control rather than a normal playable tag. |
| South Lebanon Army / Israeli security zone | — | Marjayoun / southern Lebanon | Internal militia and security-zone content within Lebanon | Israeli-backed local militia / Israeli military presence | Internal Lebanon content | No separate starting country actor, subject, technical tag, or territorial ownership. All territory remains assigned directly to Lebanon. Detailed follow-up is centralized in `country_content_design_backlog.md`. Registry status: LOCKED. |

---

## 2. Arabian Peninsula and Gulf

| Country | Proposed tag | Capital | Government type | Alignment / bloc | 1993 status | Notes |
|---|---:|---|---|---|---|---|
| Saudi Arabia | SAU | Riyadh | Absolute monarchy | US-aligned / Gulf monarchy | Stable regional power | Oil giant; Gulf War coalition legacy and internal Islamist dissent matter. |
| Yemen | YEM | Sana'a | Republic | Non-aligned / fragile | Recently unified state | North and South Yemen unified in 1990; southern elite tensions and civil war risk culminate in 1994. |
| South Yemen separatists | SYE | Aden | Former socialist republic / separatist faction | Southern separatist | Potential rebel faction | Not independent in 1993 but useful for 1994 civil war setup. |
| Oman | OMA | Muscat | Absolute monarchy | Western-aligned | Stable state | Controls Musandam exclave near Strait of Hormuz. |
| United Arab Emirates | UAE | Abu Dhabi | Federal monarchy | Western-aligned / Gulf monarchy | Stable state | Federation of emirates; Dubai and Abu Dhabi both important. |
| Qatar | QAT | Doha | Absolute monarchy | Western-aligned / Gulf monarchy | Stable state | Gas-rich monarchy; still pre-1995 leadership change. |
| Bahrain | BHR | Manama | Monarchy | Western-aligned / Gulf monarchy | Stable but internally tense | Sectarian and reform tensions important. |
| Kuwait | KUW | Kuwait City | Constitutional monarchy | US-protected / Gulf monarchy | Restored state after Iraqi occupation | Recovered from 1990-1991 Iraqi invasion; security dependence central. |
| Neutral Zone / divided Saudi-Kuwaiti area | NZK | None | Divided former neutral zone | Saudi-Kuwaiti administration | Boundary implementation issue | Saudi-Kuwaiti Neutral Zone had been partitioned before 1993 but remains relevant for oil fields and map accuracy; represent through province ownership and resource modifiers, not a tag. |

---

## 3. Iraq-Iran Region

| Country | Proposed tag | Capital | Government type | Alignment / bloc | 1993 status | Notes |
|---|---:|---|---|---|---|---|
| Iraq | IRQ | Baghdad | Ba'athist presidential republic | Sanctioned / anti-US | Sovereign state with Kurdish regions and southern opposition consolidated | All Iraqi territory remains assigned directly to Iraq at campaign start. Iraqi Kurdistan and the southern opposition are internal Iraq content. Detailed follow-up is centralized in `country_content_design_backlog.md`. |
| Iraqi Kurdistan | — | Erbil | Internal autonomous administration within Iraq | Iraqi territory / Kurdish regional administration | Internal Iraq content | No separate starting country actor, subject, technical tag, or territorial ownership. Detailed follow-up is centralized in `country_content_design_backlog.md`. Registry status: LOCKED. |
| Kurdistan Democratic Party | — | Erbil / field command | Internal Kurdish political and armed organization | Iraqi Kurdish politics | Internal Iraq content | No separate country actor or territorial ownership. Detailed follow-up is centralized in `country_content_design_backlog.md`. |
| Patriotic Union of Kurdistan | — | Sulaymaniyah / field command | Internal Kurdish political and armed organization | Iraqi Kurdish politics | Internal Iraq content | No separate country actor or territorial ownership. Detailed follow-up is centralized in `country_content_design_backlog.md`. |
| Southern Iraqi opposition | — | Najaf / field command | Internal political and armed opposition within Iraq | Iraqi opposition | Internal Iraq content | No separate starting country actor, subject, technical tag, or territorial ownership. Represented through Iraqi country content; detailed follow-up is centralized in `country_content_design_backlog.md`. Registry status: LOCKED. |
| Iran | IRN | Tehran | Islamic republic | Anti-US / regional power | Stable revolutionary state with Kurdish regions consolidated | All Iranian Kurdish territory remains assigned directly to Iran. Detailed follow-up is centralized in `country_content_design_backlog.md`. |

---

## 4. North Africa

| Country | Proposed tag | Capital | Government type | Alignment / bloc | 1993 status | Notes |
|---|---:|---|---|---|---|---|
| Egypt | EGY | Cairo | Presidential republic | US-aligned / Arab state | Stable authoritarian state | Major Arab power; controls Suez Canal. |
| Libya | LBA | Tripoli | Jamahiriya / authoritarian republic | Sanctioned / anti-Western | Isolated state | Under sanctions after Lockerbie dispute; Qaddafi regime. |
| Tunisia | TUN | Tunis | Presidential republic | Western-leaning / Arab state | Stable authoritarian state | Ben Ali government; controlled liberalization. |
| Algeria | ALG | Algiers | Military-backed republic | Non-aligned / civil conflict | Civil-war state with GIA treated internally | Algeria owns and controls all starting territory. The Armed Islamic Group is represented only through internal insurgency and civil-war content. Detailed follow-up is centralized in `country_content_design_backlog.md`. |
| Islamic Salvation Front / Algerian Islamists | FIS | Field command | Islamist opposition / insurgency | Anti-regime | Rebel faction | Use as rebel faction or disaster mechanic rather than normal country. |
| Armed Islamic Group | — | Field command | Internal armed organization within Algeria | Anti-regime / Islamist insurgency | Internal Algeria content | No separate starting country actor, subject, technical tag, or territorial ownership. Represent through Algeria’s insurgency and civil-war systems. Detailed follow-up is centralized in `country_content_design_backlog.md`. Registry status: LOCKED. |
| Morocco | MOR | Rabat | Constitutional monarchy | Western-aligned / Arab monarchy | Stable state and overlord of Western Sahara | Begins as overlord of the standard EU5 Vassal `WSA`. Detailed follow-up is centralized in `country_content_design_backlog.md`. |

---

## 5. Western Sahara and Regional Disputes

| Country | Proposed tag | Capital | Government type | Alignment / bloc | 1993 status | Notes |
|---|---:|---|---|---|---|---|
| Western Sahara / Sahrawi Arab Democratic Republic | WSA | Laayoune / Tifariti | Sahrawi republic represented as subject state | Standard EU5 Vassal of Morocco | Moroccan vassal state | Controls all Western Sahara territory as a separate `WSA` country actor and standard EU5 Vassal of Morocco (`MOR`). The Polisario Front is internal West Saharan content. Detailed follow-up is centralized in `country_content_design_backlog.md`. Registry status: LOCKED. |
| Polisario Front | — | Tindouf / field command | Internal West Saharan political and armed organization | West Saharan politics / Algerian support | Internal West Sahara content | No separate starting country actor, subject, technical tag, or territorial ownership. Represented within `WSA`; detailed follow-up is centralized in `country_content_design_backlog.md`. Registry status: LOCKED. |
| Spanish North African plazas | CEU | Ceuta / Melilla | Spanish overseas territories | Spanish sovereignty / Moroccan claim | Disputed enclaves | Could be handled in Spain file or MENA cross-reference; important for Morocco-Spain diplomacy. |

---

## 6. Implementation Priorities

### Version 0.1 playable country baseline

Use these as normal playable or AI-controlled country tags unless later map constraints require consolidation:

| Priority | Country | Tag | Reason |
|---:|---|---:|---|
| 1 | Israel | ISR | Major regional military and diplomatic actor. |
| 1 | State of Palestine | PAL | Separate partially recognized starting country actor under occupation constraints. |
| 1 | Jordan | JOR | Key Levant state and peace-process actor. |
| 1 | Lebanon | LEB | Post-civil-war state under Syrian influence. |
| 1 | Syria | SYR | Major Levant state with Lebanon and Golan disputes. |
| 1 | Saudi Arabia | SAU | Major oil, religious, and Gulf security power. |
| 1 | Yemen | YEM | Fragile unified state with near-term civil-war risk. |
| 1 | Oman | OMA | Stable Gulf monarchy and Strait of Hormuz actor. |
| 1 | United Arab Emirates | UAE | Federal Gulf monarchy and oil/trade hub. |
| 1 | Qatar | QAT | Small but strategically important Gulf monarchy. |
| 1 | Bahrain | BHR | Small Gulf monarchy with internal tension. |
| 1 | Kuwait | KUW | Recently restored post-occupation state. |
| 1 | Iraq | IRQ | Sanctioned defeated regional power. |
| 1 | Iran | IRN | Major revolutionary regional power. |
| 1 | Egypt | EGY | Major Arab state and Suez Canal controller. |
| 1 | Libya | LBA | Sanctioned anti-Western state. |
| 1 | Tunisia | TUN | Stable authoritarian North African state. |
| 1 | Algeria | ALG | Civil-war state with major internal conflict. |
| 1 | Morocco | MOR | Monarchy and overlord of Western Sahara. |
| 1 | Western Sahara | WSA | Standard EU5 Vassal of Morocco controlling all Western Sahara territory. |

### Version 0.1 special entities and mechanics

Use these as non-standard tags, subject-like systems, province modifiers, claims, rebel factions, or event-only entities:

| Entity | Suggested implementation | Notes |
|---|---|---|
| Palestine Liberation Organization | Internal Palestine political content | No separate country actor or tag; political leadership, diplomacy, and Oslo-transition content belong inside `PAL`. |
| West Bank | Occupied provinces / autonomy unrest | Israeli-controlled, Palestinian-claimed, not sovereign in 1993. |
| Gaza Strip | Occupied provinces / autonomy unrest | Israeli-controlled, Palestinian-claimed, Oslo transition target. |
| Golan Heights | Occupied province modifier / Syrian claim | Israeli-controlled, Syrian-claimed. |
| South Lebanon Army / Israeli security zone | Internal Lebanon content | No separate country actor, subject, tag, or territorial ownership; Israeli presence, the security zone, militia activity, UNIFIL, resistance, and withdrawal paths belong in `country_content_design_backlog.md`. |
| South Yemen separatists | Rebel faction / disaster actor | Needed for 1994 Yemen civil-war path. |
| Iraqi Kurdistan | Internal Iraq content | No separate country actor, subject, tag, or territorial ownership; detailed follow-up belongs in `country_content_design_backlog.md`. |
| KDP and PUK | Internal Iraq factions | Represent through Iraqi country content rather than separate countries. |
| Southern Iraqi opposition | Internal Iraq content | No separate country actor, subject, tag, or territorial ownership; detailed follow-up belongs in `country_content_design_backlog.md`. |
| FIS / Algerian Islamists | Rebel faction / disaster actor | Core Algerian Civil War opposition. |
| Armed Islamic Group | Internal Algerian insurgency content | No country actor, subject, tag, or territorial ownership; detailed mechanics belong in `country_content_design_backlog.md`. |
| Polisario Front | Internal West Sahara faction | Represented inside `WSA`, not as a separate country actor or tag. |
| Ceuta and Melilla | Spanish-owned provinces / Moroccan claim | Cross-reference Spain file. |
| Saudi-Kuwaiti divided zone | Province/resource implementation detail | Oil and boundary accuracy, not a country. |

### Open design questions

- Palestine begins as a separate `PAL` state actor; its final occupation, diplomacy, and player-interface mechanics require later detailed design.
- Should Lebanon include explicit Syrian military-presence modifiers at start?
