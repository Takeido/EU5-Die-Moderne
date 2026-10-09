# South Asia 1993 Country List

## Purpose

This file defines the initial Version 0.1 country setup for South Asia in the 1993 start date. It follows the Europe + Former Soviet Union country-list template and captures sovereign states, disputed regions, insurgencies, and civil-war factions.

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
- Insurgent, disputed, autonomous, and occupied regions may be represented as rebel factions, modifiers, or special tags.
- Nuclear status, border disputes, and proxy conflicts should be preserved for later mechanics.

---

## Categories

1. Indian Subcontinent
2. Himalayan states
3. Afghanistan and borderlands
4. Indian Ocean South Asia
5. Cross-border disputes, claims, and implementation notes

---

## 1. Indian Subcontinent

| Country | Proposed tag | Capital | Government type | Alignment / bloc | 1993 status | Notes |
|---|---:|---|---|---|---|---|
| India | IND | New Delhi | Federal parliamentary republic | Non-aligned / regional power | Stable but conflict-affected state | India remains the only starting country actor and territorial owner for all Indian territory. The Jammu and Kashmir government and Northeast Indian insurgent networks are internal India content with no separate starting actors, subjects, technical tags, or territorial ownership. Detailed follow-up is centralized in `country_content_design_backlog.md`. Registry status: LOCKED for both entries. |
| Pakistan | PAK | Islamabad | Federal parliamentary republic | US/China-linked / Islamic republic | Unstable democratic state | Single normal country actor. The consolidated internal entities receive no separate countries or technical tags. Content follow-up is centralized in `country_content_design_backlog.md`. Kashmir policy, military influence, and Afghan policy remain central. |
| Bangladesh | BGD | Dhaka | Parliamentary republic | Non-aligned / South Asian | Stable transition state | Democratic restoration after 1991. |
| Sri Lanka | LKA | Colombo | Presidential republic | Non-aligned / civil war | Civil war state | Sri Lanka remains the only starting country actor and territorial owner. The LTTE is represented as internal Sri Lankan conflict content with no separate starting actor, subject, technical tag, or territorial ownership. Detailed follow-up is centralized in `country_content_design_backlog.md`. Registry status: LOCKED for the LTTE entry. |
| Tamil Eelam / LTTE | — | Northern and eastern Sri Lanka / field command | Internal Sri Lankan armed and political organization | Sri Lanka | Internal Sri Lanka content | No separate starting country actor, subject, technical tag, or territorial ownership. Represent through Sri Lanka’s internal conflict, regional control, autonomy, diplomacy, and event content. Registry status: LOCKED. |
| Kashmir | KSH | Srinagar / Muzaffarabad | Disputed region | India-Pakistan dispute | Insurgency / disputed territory | Split between Indian-administered and Pakistani-administered areas; potential unrest/rebel/claim system. |
| Khalistan militants | KHL | Field command | Sikh separatist insurgency | Anti-Indian state | Rebel remnant | Insurgency greatly weakened by 1993 but still relevant as recent conflict. |
| Northeast Indian insurgents | — | Regional networks | Internal Indian political and security content | India | Internal India content | No separate starting country actor, subject, technical tag, or territorial ownership. Distinct movements remain later India content. Registry status: LOCKED. |

| Jammu and Kashmir government | — | Jammu / Srinagar | Internal state administration within India | India | Internal India content | No separate starting country actor, subject, technical tag, or territorial ownership. Represent through Indian regional administration and Kashmir content. Registry status: LOCKED. |

---

### Pakistan consolidation note

Pakistan (`PAK`) is the only starting country actor and territorial owner for Pakistan. Azad Jammu and Kashmir and Gilgit-Baltistan are internal Pakistani regional content and receive no separate starting country actors, subjects, technical tags, or territorial ownership. Content follow-up is centralized in `country_content_design_backlog.md`. Registry status: LOCKED for both entries.

## 2. Himalayan States

| Country | Proposed tag | Capital | Government type | Alignment / bloc | 1993 status | Notes |
|---|---:|---|---|---|---|---|
| Nepal | NEP | Kathmandu | Constitutional monarchy / parliamentary democracy | India-China buffer | Stable transition state | Multiparty democracy restored in 1990; Maoist insurgency begins later. |
| Bhutan | BHU | Thimphu | Monarchy | India-aligned / Himalayan | Stable monarchy | Refugee issue with ethnic Nepalis relevant. |
| Tibet | TIB | Lhasa | Autonomous subject administration | Standard EU5 Vassal of China | Chinese vassal subject | Separate `TIB` country actor controlling Tibetan territory as a standard EU5 Vassal of China (`CHN`). Detailed follow-up is centralized in `country_content_design_backlog.md`. Registry status: LOCKED. |
| Tibetan Government-in-Exile | TGE | Dharamshala | Exile administration | India-based / anti-PRC claim | Exile claim entity | Not a normal country; useful for events, claims, refugee politics, and China-India diplomatic tension. |
| Sikkim | SKM | Gangtok | Indian state / former monarchy | India-aligned | Integrated Indian state | Annexed by India in 1975; not independent in 1993, but useful as a historical claim or local identity modifier. |
| Chittagong Hill Tracts insurgents | CHT | Field command | Indigenous autonomy insurgency | Anti-Bangladeshi state | Insurgency / autonomy conflict | Ongoing conflict in Bangladesh until the 1997 peace accord; should appear as unrest, rebel faction, or autonomy pressure. |

---

## 3. Afghanistan and Borderlands

| Country | Proposed tag | Capital | Government type | Alignment / bloc | 1993 status | Notes |
|---|---:|---|---|---|---|---|
| Afghanistan | AFG | Kabul | Islamic State / fragmented government | Mujahideen factions | Civil war state | Afghanistan is the only starting country actor and territorial owner. Jamiat-e Islami / the Rabbani government, Ittihad-i Islami, Junbish-i Milli, Hezb-e Islami Gulbuddin, Hezb-e Wahdat, and the later Taliban movement are represented within Afghanistan rather than as separate countries or tags. Content follow-up is centralized in `country_content_design_backlog.md`. |

| Islamic Movement of Uzbekistan precursor networks | — | Regional networks | Internal future organization content within Uzbekistan | Uzbekistan / transregional links | Internal Uzbekistan content | No separate starting country actor, subject, technical tag, or territorial ownership. Its later emergence is handled through Uzbekistan’s internal and cross-border content. Registry status: LOCKED. |

| Pashtun borderlands | PST | Field command | Cross-border tribal region | Afghanistan-Pakistan frontier | Strategic region | Not a state; use for unrest, smuggling, refugee, and proxy-war mechanics. |
| Durand Line dispute | DLD | N/A | Territorial claim framework | Afghanistan-Pakistan dispute | Cross-border claim issue | Not a country; use as a persistent claim, diplomatic tension, refugee, and proxy-war mechanic. |
| Afghan refugee networks | REF | Camps / border regions | Refugee population system | Afghanistan-Pakistan-Iran issue | Humanitarian / demographic modifier | Should affect Pakistan, Iran, and Afghanistan through population displacement, unrest, recruitment, and aid events. |

---

### Afghanistan consolidation note

All Afghan civil-war factions and the later Taliban movement are retained inside Afghanistan (`AFG`) rather than as separate countries or technical tags. This explicitly includes Jamiat-e Islami / the Rabbani government, Ittihad-i Islami, Junbish-i Milli, Hezb-e Islami Gulbuddin, and Hezb-e Wahdat. They receive no separate starting country actors, subjects, technical tags, or territorial ownership. Content follow-up is centralized in `country_content_design_backlog.md`. Registry status: LOCKED for the named entries.

## 4. Indian Ocean South Asia

| Country | Proposed tag | Capital | Government type | Alignment / bloc | 1993 status | Notes |
|---|---:|---|---|---|---|---|
| Maldives | MDV | Malé | Presidential republic | Non-aligned / island state | Stable authoritarian state | Small island state; strategic Indian Ocean position. |
| British Indian Ocean Territory / Diego Garcia | — | Diego Garcia | British overseas territory represented within the United Kingdom | UK sovereignty / US military presence | Direct United Kingdom territory | Assigned directly to the United Kingdom (`GBR`) at campaign start, with no separate country actor, subject, technical tag, or territorial ownership. Basing and Chagossian claim content are handled later. Registry status: LOCKED. |
| Chagos exiles / sovereignty claim | CHG | Mauritius / exile community | Exile claim movement | Mauritius-linked / anti-UK claim | Claim issue | Not a normal South Asian state, but relevant to Indian Ocean basing, decolonization claims, and Diego Garcia events. |

---

## 5. Cross-border disputes, claims, and implementation notes

### Major 1993 regional conflict systems

| System | Primary countries / tags | Recommended implementation | Notes |
|---|---|---|---|
| Kashmir dispute | IND, PAK, KSH | Claims, unrest, border militarization, event chain | Core India-Pakistan flashpoint. Azad Jammu and Kashmir and Gilgit-Baltistan are handled inside Pakistan rather than as separate tags; the dispute should interact with nuclear status and great-power diplomacy. |
| Sri Lankan Civil War | LKA | Internal conflict, regional control, autonomy demands, and event chains | The LTTE remains a major internal Sri Lankan actor but has no separate country tag or territorial ownership. |
| Afghan Civil War | AFG | Internal Afghanistan conflict system | The factions are consolidated into Afghanistan rather than separate countries. Content follow-up is centralized in `country_content_design_backlog.md`. |
| Chittagong Hill Tracts conflict | BGD, CHT | Regional unrest / autonomy insurgency | Useful for making Bangladesh less static without overstating the conflict as a full state. |
| India internal insurgencies | IND, KHL, KSH | Regional unrest, internal factions, security-law modifiers, and event chains | Punjab is declining by 1993, while Kashmir and distinct Northeast insurgencies remain more active inside India. |
| Afghanistan-Pakistan frontier | AFG, PAK, PST, DLD, REF | Cross-border unrest, refugee flows, proxy-war events | Should connect Pakistan's Afghan policy to domestic instability and regional diplomacy. |

### Recommended normal starting countries

These should normally exist as playable sovereign states in the 1993 bookmark:

- India (`IND`)
- Pakistan (`PAK`)
- Bangladesh (`BGD`)
- Sri Lanka (`LKA`)
- Nepal (`NEP`)
- Bhutan (`BHU`)
- Maldives (`MDV`)
- Afghanistan (`AFG`)

### Recommended special or nonstandard tags

These should usually be rebels, subjects, event entities, claims, modifiers, or map overlays rather than ordinary sovereign countries:

- Kashmir (`KSH`)
- Khalistan militants (`KHL`)
- Chittagong Hill Tracts insurgents (`CHT`)

- Tibet (`TIB`) as a standard EU5 Vassal of China (`CHN`), with the Tibetan Government-in-Exile (`TGE`) retained as a separate non-country entry.
- Pashtun borderlands / Durand Line systems (`PST`, `DLD`)
- Chagossian exile and sovereignty-claim movement (`CHG`); British Indian Ocean Territory / Diego Garcia is direct United Kingdom territory without a separate tag.

### Design priorities for Version 0.1

- Represent Pakistan as one normal country (`PAK`); the consolidated internal entities receive no separate country tags. Content follow-up is centralized in `country_content_design_backlog.md`.
- Do not over-fragment India, Pakistan, or Bangladesh into normal countries unless EU5 mechanics strongly support substate governments.
- Represent Kashmir as the region's central claim-and-crisis system rather than a simple independent country.
- Represent Afghanistan as one normal country (`AFG`); the consolidated factions receive no separate country tags. Content follow-up is centralized in `country_content_design_backlog.md`.

- Preserve the Sri Lankan Civil War as a major internal Sri Lankan conflict using regional control, unrest, factions, events, and other suitable mechanics without creating a separate LTTE country tag.
- Use unrest, autonomy, population displacement, security-law, and foreign-support modifiers to avoid creating too many tiny playable states.
