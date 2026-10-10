EU5 Modern World Mod – Economic System Foundations
Status: Foundational economy design document
Scope: General economic circulation, monetary scaling, and large-reserve representation

1. Purpose
This document establishes the common foundation for the economy of the EU5 Modern World Mod. It defines the general circulation of money and goods, the authoritative conversion between real-world US-dollar values and EU5 Gold, and the design concept used to represent reserves above the practical EU5 treasury limit. Goods, resources, and production-chain design are maintained in [Goods and Ressources](<Goods and Ressources.md>).

This document intentionally does not yet define detailed prices, wages, taxation formulas, production functions, interest rates, inflation mechanics, the complete final goods catalogue, bank balance-sheet rules, or the final implementation of every economic actor. Those matters require later design decisions.

2. Design Status and Authority
The following monetary decisions are LOCKED:
* 1 EU5 Gold represents 500 real US dollars under the selected 2026-dollar valuation basis.
* Whenever a real-world dollar value is translated into the mod, it must be converted into EU5 Gold.
* One Gold Cap modifier stack represents exactly 900,000,000 Gold.
* The Gold Cap modifier is a newly created accounting device and is not identical to the engine's actual maximum-gold value.
* Large reserves are represented by a combination of liquid Gold and one or more Gold Cap modifier stacks.

Goods-design decisions and their APPROVED, LOCKED, or PENDING status are maintained in [Goods and Ressources](<Goods and Ressources.md>). Open questions and mechanisms described only as requirements or working models remain PENDING unless explicitly approved or locked.

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
5.1 Conversion Rate [LOCKED]
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
* 450,000,000,000 US dollars = 900,000,000 Gold (one Gold Cap stack).

5.4 Mandatory Use
All real-world dollar figures used for starting data, events, loans, investments, budgets, wages, prices, costs, revenues, aid, damages, assets, or other monetary design must be converted through this rule before becoming an EU5 Gold value.
The documentation should preserve the real-world source value when useful, but the implemented value must use Gold.
Historical nominal dollar figures may require conversion into the selected real-dollar valuation basis before division by 500. The precise inflation and historical-price methodology remains an open design decision.

6. Gold Cap Reserve Extension
6.1 Definition [LOCKED]
A Gold Cap modifier is a stackable accounting representation of stored monetary value.
One Gold Cap modifier stack is worth exactly 900,000,000 Gold.
This value is deliberately lower than the practical treasury limit and is not the actual engine maximum.
Owner-confirmed revision: the stack value was raised from 90 million to 900 million Gold following EU5 patch 1.1, which the owner identified as enabling the increase. The current LOCKED value supersedes the previous stack value. The exact engine maximum, packing threshold, and scripted behavior still require the implementation checks below.

6.2 Effective Reserve Formula
Effective total Gold = liquid Gold + (number of Gold Cap stacks multiplied by 900,000,000).

6.3 Packing Rule
When an entity's liquid Gold approaches the practical maximum, 900,000,000 Gold is removed from its liquid reserve and one Gold Cap modifier stack is added.
The conversion must conserve value exactly.
The operation may repeat whenever additional reserve value must be stored.
The exact trigger threshold and timing remain open.

6.4 Representation Examples
* 900,000,000 Gold can be represented as 1 Gold Cap stack and 0 liquid Gold.
* 1,000,000,000 Gold can be represented as 1 Gold Cap stack and 100,000,000 liquid Gold.
* 1,800,000,000 Gold can be represented as 2 Gold Cap stacks and 0 liquid Gold.
* 5,000,000,000 Gold can be represented as 5 Gold Cap stacks and 500,000,000 liquid Gold.
* 5,000,000,000 Gold has a real-dollar equivalent of 2,500,000,000,000 US dollars.

6.5 Redemption Requirement
A Gold Cap stack must be redeemable so that its stored 900,000,000 Gold can become liquid Gold again when required.
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

9. Open Design Decisions [PENDING]
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
A bank has an effective monetary reserve of 5,000,000,000 Gold.
Its real-dollar equivalent is 2,500,000,000,000 US dollars.
The reserve can be represented as 5 Gold Cap modifier stacks plus 500,000,000 liquid Gold.
The effective-reserve calculation is:
500,000,000 + (5 × 900,000,000) = 5,000,000,000 Gold.

This representation changes only how the value is stored. It must not change the bank's economic wealth, create income, erase obligations, or alter the value of transactions.

11. Design Principle
The economy should use one consistent monetary scale for ordinary wages, needs, prices, investments, bank loans, government budgets, and very large reserves. The Gold Cap system exists only to extend the storage range of that common scale. It must not create a second currency or a separate economic value system.

12. Goods, Resources, and Production-Chain Design Reference

[Goods and Ressources](<Goods and Ressources.md>) is the authoritative design document for all RGOs, raw materials, processed and intermediate goods, production and consumer goods, and their chains from the RGO to the final consumer. It contains the goods-design principles, approved decisions, reference lists, individual goods reviews, production-method rules, and outstanding questions formerly maintained here.

All future goods and production-chain decisions must be recorded there. This document continues to define general economic circulation, economic actors, monetary conversion, and Gold Cap reserve accounting.
