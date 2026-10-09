EU5 Modern World Mod – Economic System Foundations
Status: Foundational economy design document
Scope: General economic circulation, monetary scaling, and large-reserve representation

1. Purpose
This document establishes the common foundation for the economy of the EU5 Modern World Mod. It defines the general circulation of money and goods, the authoritative conversion between real-world US-dollar values and EU5 Gold, and the design concept used to represent reserves above the practical EU5 treasury limit.

This document intentionally does not yet define detailed prices, wages, taxation formulas, production functions, interest rates, inflation mechanics, individual goods, bank balance-sheet rules, or the final implementation of every economic actor. Those matters require later design decisions.

2. Design Status and Authority
The following decisions are locked:
* 1 EU5 Gold represents 500 real US dollars under the selected 2026-dollar valuation basis.
* Whenever a real-world dollar value is translated into the mod, it must be converted into EU5 Gold.
* One Gold Cap modifier stack represents exactly 90,000,000 Gold.
* The Gold Cap modifier is a newly created accounting device and is not identical to the engine's actual maximum-gold value.
* Large reserves are represented by a combination of liquid Gold and one or more Gold Cap modifier stacks.

All other mechanisms described as requirements, working models, or open questions remain subject to later approval.

3. General Economic Circulation
The economy should be understood as several connected circulation loops rather than a single national treasury.

3.1 Real-Economy Loop
* Economic entities obtain labor, resources, intermediate goods, capital goods, services, and infrastructure access.
* Production transforms these inputs into goods and services.
* Goods and services are sold through markets or transferred through public and institutional systems.
* Sales create revenue for producers and income for workers, owners, governments, and financial institutions.
* Income returns to the economy through consumption, investment, taxation, saving, debt service, and transfers.
* Demand influences future production, employment, imports, investment, and prices.

3.2 Household and Population Loop
* Population groups provide labor and other economically relevant participation.
* They receive wages, benefits, transfers, dividends, or other income.
* They use income to satisfy needs and to purchase goods and services.
* Unspent income may become savings, deposits, investment, or debt repayment.
* Insufficient income or unavailable goods should create economic and social consequences that will be designed later.

3.3 Business and Production Loop
* Businesses and other productive entities receive sales revenue.
* They pay wages, suppliers, taxes, interest, maintenance, and investment costs.
* Profits may be retained, distributed, deposited, invested, or used to repay debt.
* Losses reduce reserves, increase borrowing needs, reduce production, or ultimately cause restructuring or failure.
* The exact legal and gameplay form of businesses remains open.

3.4 Government Fiscal Loop
* Governments collect taxes, fees, resource income, dividends, borrowing proceeds, and other public revenue.
* Governments spend on administration, welfare, public wages, procurement, infrastructure, subsidies, debt service, security, and other policies.
* Government deficits require financing through reserves, borrowing, monetary mechanisms, asset sales, or external support.
* Government surpluses increase reserves, repay debt, or finance investment.
* The economy must distinguish public income, public expenditure, liquid reserves, debt, and non-liquid financial claims.

3.5 Banking and Credit Loop
* Banks and other financial entities collect deposits or other funding.
* They provide loans and financing to governments, businesses, households, and other entities.
* Borrowers use financing for investment, liquidity, consumption, refinancing, or crisis stabilization.
* Principal repayments and interest return funds to lenders.
* Defaults, bank runs, liquidity shortages, and insolvency must be distinguishable in later detailed design.
* A bank's total financial position must not be assumed to equal its immediately spendable liquid Gold.

3.6 Investment Loop
* Savings and retained earnings can be transformed into investment.
* Investment creates or improves productive capacity, infrastructure, technology, institutions, housing, or other assets.
* Investment spending becomes income for the entities providing labor, goods, finance, and services.
* Successful investment can raise future output or reduce future costs.
* Failed or unproductive investment can destroy value or create debt without sufficient return.

3.7 International Trade and Finance Loop
* Entities import and export goods and services.
* Trade payments transfer money between domestic and foreign actors.
* Cross-border lending, investment, aid, sanctions, remittances, and debt service create additional international flows.
* Trade balances and financial flows affect reserves, debt, production, employment, and political choices.
* Currency, exchange-rate, and balance-of-payments mechanics require separate later decisions.

4. Economic Actors
The foundational model may involve the following categories:
* States and other public authorities
* Population groups or households
* Businesses and productive institutions
* Private banks
* State-owned banks and central banks
* Markets and trade systems
* International organizations
* Foreign governments and foreign investors
* Other entities capable of holding, receiving, spending, lending, or owing value

The existence of a category in this document does not decide its final EU5 implementation form.

5. Authoritative Monetary Conversion
5.1 Locked Conversion Rate
1 Gold = 500 real US dollars.

5.2 Conversion Formulas
EU5 Gold = real US dollars divided by 500.
Real-dollar equivalent = EU5 Gold multiplied by 500.

5.3 Conversion Examples
* 1 US dollar = 0.002 Gold.
* 100 US dollars = 0.2 Gold.
* 500 US dollars = 1 Gold.
* 1,000,000 US dollars = 2,000 Gold.
* 1,000,000,000 US dollars = 2,000,000 Gold.
* 45,000,000,000 US dollars = 90,000,000 Gold.
* 50,000,000,000 US dollars = 100,000,000 Gold.

5.4 Mandatory Use
All real-world dollar figures used for starting data, events, loans, investments, budgets, wages, prices, costs, revenues, aid, damages, assets, or other monetary design must be converted through this rule before becoming an EU5 Gold value.
The documentation should preserve the real-world source value when useful, but the implemented value must use Gold.
Historical nominal dollar figures may require conversion into the selected real-dollar valuation basis before division by 500. The precise inflation and historical-price methodology remains an open design decision.

6. Gold Cap Reserve Extension
6.1 Definition
A Gold Cap modifier is a stackable accounting representation of stored monetary value.
One Gold Cap modifier stack is worth exactly 90,000,000 Gold.
This value is deliberately lower than the practical treasury limit and is not the actual engine maximum.

6.2 Effective Reserve Formula
Effective total Gold = liquid Gold + (number of Gold Cap stacks multiplied by 90,000,000).

6.3 Packing Rule
When an entity's liquid Gold approaches the practical maximum, 90,000,000 Gold is removed from its liquid reserve and one Gold Cap modifier stack is added.
The conversion must conserve value exactly.
The operation may repeat whenever additional reserve value must be stored.
The exact trigger threshold and timing remain open.

6.4 Representation Examples
* 90,000,000 Gold can be represented as 1 Gold Cap stack and 0 liquid Gold.
* 100,000,000 Gold can be represented as 1 Gold Cap stack and 10,000,000 liquid Gold.
* 180,000,000 Gold can be represented as 2 Gold Cap stacks and 0 liquid Gold.
* 500,000,000 Gold can be represented as 5 Gold Cap stacks and 50,000,000 liquid Gold.
* 500,000,000 Gold has a real-dollar equivalent of 250,000,000,000 US dollars.

6.5 Redemption Requirement
A Gold Cap stack must be redeemable so that its stored 90,000,000 Gold can become liquid Gold again when required.
Redemption must remove one modifier stack and restore the corresponding value without creating or destroying money.
The final system must prevent redemption from pushing liquid Gold beyond the practical engine limit.
Whether redemption is automatic, manual, transaction-triggered, or handled through another accounting operation remains open.
Whether partial redemption is possible remains open.

6.6 Accounting Requirements
* Liquid Gold and Gold Cap stacks must never be double-counted.
* Transfers, loans, repayments, purchases, investment, and other payments must preserve total effective value.
* The system must support multiple modifier stacks.
* The system must remain stable through saving, loading, ownership changes, annexation, bankruptcy, entity removal, and scripted transfers.
* The modifier represents stored value, not income, production, interest, or a percentage bonus.
* Any entity using the system must have a reliable way to read its effective total reserve.

7. Liquidity Versus Total Wealth
Liquid Gold is immediately available for ordinary transactions.
Gold stored in Gold Cap stacks is part of the entity's effective monetary reserve but is not automatically assumed to be immediately spendable.
Assets, loans receivable, securities, buildings, infrastructure, and productive capacity are not automatically Gold and should not be counted as liquid reserves.
Debt is an obligation and must not be confused with a positive reserve.
Detailed balance-sheet categories will be designed separately.

8. Required Implementation Tests
* Confirm the practical maximum liquid Gold value in the target EU5 build.
* Confirm that the Gold Cap modifier can stack to the required number.
* Confirm that scripted conversion conserves value exactly.
* Confirm that AI-controlled entities can pack and redeem reserves correctly.
* Confirm that transactions crossing the liquid-reserve limit do not fail or duplicate money.
* Confirm correct behavior during annexation, mergers, splits, releases, bankruptcy, and entity destruction.
* Confirm correct save-and-load behavior.
* Confirm that the user interface can communicate liquid Gold, Gold Cap stacks, and effective total reserves clearly.
* Confirm performance when many entities hold multiple stacks.

9. Open Design Decisions
* Exact Gold Cap packing threshold
* Exact redemption trigger and player control
* Automatic versus manual redemption
* Partial versus full-stack redemption
* How a single transaction larger than the available liquid reserve is processed
* How Gold Cap stacks transfer between entities
* How reserves are handled during annexation, merger, division, release, or liquidation
* Which entity types can use the system
* How AI evaluates liquid reserves versus stored reserves
* How Gold Cap reserves interact with interest, investment, collateral, and bankruptcy
* How historical nominal money is converted into the project's real-dollar basis
* How inflation, currency exchange, and purchasing-power differences are modeled
* How Gold and real-dollar equivalents are displayed in the interface

10. Worked Example: Large Bank Reserve
A bank has an effective monetary reserve of 500,000,000 Gold.
Its real-dollar equivalent is 250,000,000,000 US dollars.
The reserve can be represented as 5 Gold Cap modifier stacks plus 50,000,000 liquid Gold.
The effective-reserve calculation is:
50,000,000 + (5 × 90,000,000) = 500,000,000 Gold.

This representation changes only how the value is stored. It must not change the bank's economic wealth, create income, erase obligations, or alter the value of transactions.

11. Design Principle
The economy should use one consistent monetary scale for ordinary wages, needs, prices, investments, bank loans, government budgets, and very large reserves. The Gold Cap system exists only to extend the storage range of that common scale. It must not create a second currency or a separate economic value system.

12. Goods, Production, and Building Design Process
12.1 Agreed Design Sequence

The detailed goods and production framework will be designed in the following order:

1. Define the raw goods and natural resources represented in the mod.
2. Define processed, intermediate, and final goods.
3. Define the production chains connecting those goods.
4. Define the buildings and EU5 production structures that represent those chains.
5. Review agriculture, energy, services, infrastructure, construction, trade, and modernization within the resulting framework.

This order is intended to prevent buildings from being designed before their economic inputs, outputs, and gameplay purpose are known.

12.2 EU5 Compatibility Principle

The design should preserve existing EU5 economic structures wherever possible. New goods, buildings, production relationships, modifiers, and scripted systems should be preferred over replacing core EU5 mechanics. A deeper mechanical change should be proposed only when the existing framework cannot represent an essential modern economic function adequately.

12.3 Decision Procedure

Each proposed good will be reviewed individually or in a coherent group. For every proposal, the design must determine:

• whether it deserves representation as a distinct EU5 good;
• whether it should be merged into a broader category;
• whether it is a raw, intermediate, final, strategic, military, subsistence, or luxury good;
• which locations can produce it;
• which buildings or production methods consume and produce it;
• whether its separate representation creates meaningful gameplay rather than unnecessary complexity.

No undecided proposal is considered locked. Approved decisions will be recorded in this document as the discussion proceeds.

12.4 Current Work Stage

The current work stage is the definition of raw goods and natural resources. The first decision concerns the desired overall level of detail for the raw-goods list.

12. Raw Materials Review and Candidate Modern Expansion

12.1 Working Principle
The vanilla EU5 system currently contains 52 raw materials. The mod should retain this level of granularity as its minimum reference point, but it should not split resources merely for realism. A new raw material is justified only when it creates a distinct geographic dependency, strategic bottleneck, production chain, or policy problem that cannot be represented adequately by an existing good. Lumber remains one general raw material rather than being divided into wood species.

The list below is a working comparison, not yet a locked final selection. Existing goods are marked VANILLA. Proposed additions are marked CANDIDATE and require individual approval.

12.2 Existing EU5 Raw Materials and Modern Production Chains
1. Horses [VANILLA] — breeding and transport animals; equestrian services; limited military, police, agricultural, sporting, and cultural use.
2. Clay [VANILLA] — bricks, tiles, ceramics, sanitary ware, cement additives, refractory products.
3. Sand [VANILLA] — glass, concrete, foundry materials, silicon feedstock, construction aggregates.
4. Coal [VANILLA] — electricity, coke, steel, chemicals, industrial heat, synthetic fuels.
5. Iron [VANILLA] — pig iron, steel, tools, machinery, vehicles, construction materials, weapons.
6. Copper [VANILLA] — wiring, electrical equipment, electronics, motors, plumbing, alloys, ammunition.
7. Gold [VANILLA] — jewelry, electronics, financial reserves, precision components.
8. Silver [VANILLA] — jewelry, electronics, photovoltaics, medical products, chemicals.
9. Stone [VANILLA] — aggregates, concrete inputs, road construction, general building materials.
10. Tin [VANILLA] — solder, tinplate, bronze, chemicals, electronics.
11. Lead [VANILLA] — batteries, radiation shielding, ammunition, alloys, industrial chemicals.
12. Silk [VANILLA] — textiles, luxury clothing, technical fabrics, medical sutures.
13. Dyes [VANILLA] — textile dyes, pigments, paints, printing inks, chemical colorants.
14. Incense [VANILLA] — fragrances, religious goods, cosmetics, traditional medicines.
15. Tea [VANILLA] — beverages, extracts, packaged consumer goods.
16. Cocoa [VANILLA] — chocolate, confectionery, beverages, cosmetics.
17. Coffee [VANILLA] — roasted coffee, beverages, extracts, packaged consumer goods.
18. Fiber Crops [VANILLA] — flax, hemp, jute and similar fibers into textiles, rope, composites, paper, insulation.
19. Ivory [VANILLA] — legacy luxury and craft uses; modern trade should be highly restricted or prohibited.
20. Lumber [VANILLA] — sawn wood, panels, pulp, paper, furniture, housing, packaging, construction.
21. Salt [VANILLA] — food processing, chemicals, chlorine, soda ash, road treatment, water treatment.
22. Medicaments [VANILLA] — medicinal plants and basic natural inputs into pharmaceuticals, extracts, cosmetics and traditional remedies.
23. Gems [VANILLA] — jewelry, cutting tools, abrasives, optical and precision applications.
24. Pearls [VANILLA] — jewelry and luxury goods.
25. Amber [VANILLA] — jewelry, decorative goods, niche chemicals and cultural products.
26. Saltpeter [VANILLA] — fertilizers, explosives, propellants, specialty chemicals.
27. Alum [VANILLA] — water treatment, paper, textiles, leather processing, chemicals.
28. Wine [VANILLA] — bottled wine, spirits inputs, food processing, hospitality and export consumption.
29. Elephants [VANILLA] — tourism, cultural use and protected wildlife; no major modern industrial chain.
30. Marble [VANILLA] — decorative stone, monuments, premium construction, interior finishes.
31. Mercury [VANILLA] — specialty instruments, chemicals, mining processes and legacy industrial uses; strongly regulated.
32. Saffron [VANILLA] — food, fragrances, cosmetics, specialty extracts.
33. Pepper [VANILLA] — processed spices, food manufacturing, extracts.
34. Cloves [VANILLA] — processed spices, food, fragrances, traditional medicines.
35. Chili [VANILLA] — food processing, spices, sauces, extracts.
36. Cotton [VANILLA] — yarn, cloth, clothing, medical textiles, household textiles.
37. Sugar [VANILLA] — food, beverages, ethanol, industrial fermentation, chemicals.
38. Tobacco [VANILLA] — cigarettes, cigars, nicotine products and regulated consumer goods.
39. Wool [VANILLA] — yarn, cloth, clothing, carpets, insulation.
40. Wild Game [VANILLA] — food, hides, tourism and regulated hunting products.
41. Fur [VANILLA] — clothing and luxury goods; modern demand and legality vary greatly.
42. Fish [VANILLA] — fresh and processed food, fishmeal, fish oil, aquaculture inputs.
43. Wheat [VANILLA] — flour, bread, pasta, animal feed, starch, ethanol.
44. Maize [VANILLA] — food, animal feed, starch, sweeteners, ethanol, bioplastics.
45. Rice [VANILLA] — food, flour, starch, beverages, animal feed.
46. Sturdy Grains [VANILLA] — barley, rye, oats, millet and similar grains into food, feed, malt, beer and spirits.
47. Legumes [VANILLA] — food, protein products, animal feed, oils where applicable.
48. Potatoes [VANILLA] — food, starch, alcohol, processed foods, animal feed.
49. Livestock [VANILLA] — meat, milk, leather, wool where relevant, fats, fertilizer, processed foods.
50. Olives [VANILLA] — edible olives, olive oil, food processing, soaps, cosmetics.
51. Fruit [VANILLA] — fresh and processed food, juices, preserves, fermentation, flavorings.
52. Beeswax [VANILLA] — honey-related goods, wax products, cosmetics, pharmaceuticals, polishes.

12.3 Candidate Additional Raw Materials for a Modern Economy
53. Crude Oil [CANDIDATE — core] — refinery products, gasoline, diesel, jet fuel, marine fuel, lubricants, petrochemicals, plastics, synthetic fibers, asphalt.
54. Natural Gas [CANDIDATE — core] — electricity, heating, industrial heat, hydrogen, ammonia, fertilizers, methanol, chemicals.
55. Uranium [CANDIDATE — core] — nuclear fuel, electricity generation, military nuclear programs and strategic stockpiles.
56. Bauxite [CANDIDATE — core] — alumina, aluminium, transport equipment, aircraft, packaging, construction, electrical products.
57. Nickel [CANDIDATE — core] — stainless steel, superalloys, batteries, plating, machinery.
58. Zinc [CANDIDATE — core] — galvanised steel, brass, batteries, chemicals, construction products.
59. Manganese [CANDIDATE — core] — steel alloys, batteries, chemicals.
60. Chromium [CANDIDATE — core] — stainless steel, superalloys, plating, pigments, refractory products.
61. Cobalt [CANDIDATE — core] — batteries, superalloys, catalysts, magnets, military and aerospace equipment.
62. Lithium [CANDIDATE — core] — batteries, glass, ceramics, lubricants, specialty chemicals.
63. Rare Earth Elements [CANDIDATE — core] — permanent magnets, electronics, wind turbines, electric vehicles, optics, catalysts, defense systems.
64. Phosphate Rock [CANDIDATE — core] — phosphate fertilizers, animal feed additives, industrial phosphates and chemicals.
65. Potash [CANDIDATE — core] — potassium fertilizers and industrial potassium chemicals.
66. Sulfur [APPROVED] — sulfuric acid, fertilizers, chemicals, explosives, petroleum refining, rubber vulcanisation.
67. Natural Rubber [CANDIDATE — core] — tires, seals, hoses, medical goods, industrial components.
68. Oil Crops [CANDIDATE — core] — soybean, rapeseed, sunflower, palm and similar oils into food oils, animal feed, biodiesel, soaps and chemicals. This category avoids splitting every oil crop.
69. Platinum-Group Metals [APPROVED] — catalytic converters, chemical catalysts, electronics, jewelry, hydrogen technologies, medical equipment.
70. Titanium Minerals [APPROVED] — titanium metal, aircraft, military equipment, medical implants, pigments.
71. Tungsten [APPROVED] — cutting tools, hard metals, high-temperature alloys, electronics, ammunition.
72. Molybdenum [APPROVED] — alloy steel, catalysts, lubricants, chemicals.
73. Graphite [APPROVED] — batteries, electrodes, refractories, lubricants, advanced materials.
74. Fluorspar [APPROVED] — fluorochemicals, aluminium processing, steelmaking, refrigerants and nuclear-fuel processing.
75. Specialty Ores [APPROVED] — grouped raw ore category representing antimony, niobium and tantalum ores. These ores feed later production of specialty metals used in electronics, semiconductors, advanced alloys, defense systems and other high-technology industries. Gallium, germanium and indium are not separate RGOs and are represented later through processing chains.

12.4 Preliminary Finding
A credible modern raw-material system does not require 90 separate raw materials. The current working list contains 75 entries: all 52 vanilla raw materials plus 23 proposed modern additions. Eight modern additions are currently approved: Sulfur, Platinum-Group Metals, Titanium Minerals, Tungsten, Molybdenum, Graphite, Fluorspar, and Specialty Ores. The remaining proposed additions require explicit approval before the raw-material list is locked. Unnecessary splitting of categories such as lumber, livestock, fruit, oil crops, rare earths or specialty metals remains contrary to the intended EU5-compatible level of abstraction.

Source note: the vanilla list and count are based on the EU5 goods reference for version 1.2.1, which records 52 raw materials and 22 produced goods.

12.5 Production-Chain Depth Principle
There is no fixed number of production stages for every good. Each production chain must be only as deep as required for meaningful gameplay. A distinct intermediate good should be introduced when it has independent strategic or economic importance, is traded or stockpiled meaningfully, or serves as an input for several different industries. Where an additional stage would add complexity without meaningful gameplay, production should proceed directly from the raw material to the produced good. The final design process must nevertheless result in one complete authoritative list of all processed, intermediate, and final goods
12.6 Production Methods Before Goods Proliferation
The mod introduces a new produced good only when it represents a distinct economic, strategic, or gameplay-relevant category that cannot be represented adequately through production methods.
Differences in quality, technology, efficiency, production process, material composition, recycling, automation, or comparable industrial improvements should, wherever possible, be represented through production methods rather than through additional goods.
Production methods may require additional raw materials or intermediate goods, use different energy sources, increase or decrease output, change production costs, alter labor requirements, and create other gameplay effects defined elsewhere.
Goods such as Steel, Aluminium, Paper, Glass, Cement, and comparable industrial products therefore remain single goods unless a later explicit decision establishes a separate category. Modern production technologies and specialised material inputs change their production methods rather than creating separate quality variants.
Example — Steel Production
Steel remains one produced good. Different production methods may use different combinations of Iron, Coal, Electricity, Manganese, Nickel, Chromium, Molybdenum, Tungsten, or other approved inputs. Basic methods produce Steel from Iron with Coal and/or Electricity. More advanced methods may consume additional alloying or technological inputs and produce a higher quantity of Steel. Separate goods such as Stainless Steel, Tool Steel, or Armour Steel are not created.
This rule is locked and applies across the goods and production design unless explicitly revised later.

12.7 Approved Produced Goods and Initial Production Chains
Steel [APPROVED] — one produced good. Basic production uses Iron with Coal and/or Electricity. More advanced production methods may consume additional approved inputs and increase Steel output without creating separate steel-quality goods.
Aluminium [APPROVED] — a distinct produced good. Its basic production chain is Bauxite + Electricity → Aluminium. Aluminium is used by construction, transport equipment, aircraft, packaging, electrical products, machinery, and other industries. Different technologies or additives should be represented through production methods rather than separate aluminium goods.
