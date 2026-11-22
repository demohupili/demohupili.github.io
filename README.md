# The S$1,000,000 Public Flat & The 99-Year Clock: Anatomy of Singapore HDB Resale Dynamics

**Author:** demohupili (`@demohupili`)  
**Cohort:** NUS Master of Science in Business Analytics (MSBA)  
**Dataset:** Singapore Housing & Development Board (HDB) Resale Sample (`../../data/hdb_resale_sample.csv`)  
**Interactive Dashboard & Decision Engine:** [`index.html`](./index.html)

---

## 1. Executive Summary & Business Problem

Singapore’s public housing ecosystem represents an internationally renowned social compact, housing over 80% of resident citizens across 26 planned new towns. Yet, as the pioneer generation of 99-year state leaseholds enters its sixth decade, and seven-figure transactions proliferate across secondary market listings, public housing has split into two divergent economies:
1. **The Suburban Shelter Engine:** Outer non-mature new towns providing affordable, family-scale living spaces anchored tightly between S$3,450 and S$3,930 per square meter.
2. **The Prime Speculative Market:** Central and city-fringe mature estates where buyers trade up to **S$9,776 per square meter** for unexpired leaseholds, transit convergence, and premier school zoning.

This investigation delivers a quantitative decomposition of **5,000 validated resale transactions** across Singapore's secondary market to resolve three critical executive questions:
* **The Location vs. Depreciation Paradox:** How does a flat's geographic maturity interact with its ticking 99-year lease clock?
* **The Architectural Typology Premium:** What is the quantified financial uplift of premium models (Pinnacle Type S1/S2, DBSS, Maisonettes) over standard public housing stock?
* **Actionable Capital Allocation:** How can first-time homebuyers and upgraders navigate the 30% Mortgage Servicing Ratio (MSR) cap and avoid the structural "<60-year leasehold liquidity trap"?

---

## 2. Key Empirical Findings

### Finding 1: The +S$139,694 Location Hegemony & Simpson’s Paradox
* **Location Out-Bids Age:** Mature estate flats command an 18.8% absolute price premium (mean **S$480,952** vs. **S$404,805**) and a **22.6% price-per-square-meter premium** (median **S$4,877/sqm** vs. **S$3,977/sqm**), despite being an average of **9.0 years older** (mean remaining lease of 68.9 years vs. 77.9 years).
* **Unmasking Simpson's Paradox:** A naive regression of price-per-square-meter against remaining leasehold exhibits a counter-intuitive U-shape, where flats with <60 years of lease (median S$4,943/sqm) transact higher than flats with 70–80 years of lease (median S$3,842/sqm). This is a textbook spatial selection artifact: the oldest flats reside exclusively in prime historic pioneer nodes (Queenstown, Marine Parade, Central Area), whereas 70–80 year flats are situated in outer 1990s satellite towns (Woodlands, Jurong West).
* **Controlled Hedonic Premium:** Once location and physical attributes are controlled in our multivariate OLS specification (\(R^2 = 0.7238\)), mature estate status adds an isolated **+S$139,694.43** hedonic premium (which expands to **+S$172,626** when evaluating 4-Room flats exclusively).

### Finding 2: The S$1,000,000 Sieve & Architectural Super-Premiums
* **Prime Leasehold Convergence:** All **9 million-dollar transactions** in this dataset occurred in mature estates (**Bishan, Central Area, Clementi, Kallang/Whampoa**), with **88.9% (8 of 9) retaining >92 years of remaining lease**.
* **Model Arbitrage:** Beyond geographical location, architectural typology drives massive price premiums:
  * **Type S2 (Pinnacle@Duxton):** Median **S$1,046,000** (**S$9,776/sqm**) — a **+126% premium** over standard blocks.
  * **Type S1 (Pinnacle@Duxton):** Median **S$864,000** (**S$9,194/sqm**).
  * **HDB Terraces (Whampoa/Jalan Bahagia):** Median **S$870,000** (**S$8,056/sqm**).
  * **DBSS (e.g. Natura Loft, City View):** Median **S$788,888** (**S$7,644/sqm**).
  * **Standard / Model A / New Generation:** Bounded between **S$4,330 and S$5,116/sqm**.
* **Storey Elevation Dividend:** High-floor units command an empirical uplift of **+S$6,670.19 per storey level**, providing insulation against broader market cyclical corrections.

### Finding 3: Non-Mature Value Ceiling & Space Subsidization
* **Market Liquidity Anchor:** **4-Room flats** represent the primary liquidity center of gravity, capturing **41.3% of total transactions** (2,065 units; median S$410,000, median 95.8 sqm).
* **Space-for-Location Arbitrage:** Non-mature satellite towns operate as space subsidization centers. A buyer allocating S$380,000–S$410,000 in Woodlands (median S$3,626/sqm) or Choa Chu Kang (median S$3,455/sqm) acquires an expansive 118–144 sqm 5-Room or Executive unit, whereas the same capital outlay in Queenstown (median S$6,179/sqm) or Marine Parade (median S$5,977/sqm) secures only an aging 65–68 sqm 3-Room flat.

---

## 3. Strategic Recommendations

### Recommendation 1: First-Time Homebuyers — The "85+ Year Non-Mature Capital Moat"
* **Action:** First-time buyers with combined household incomes of S$7,500–S$11,000 should bypass the S$140,000 mature estate surcharge and acquire 4-Room or 5-Room flats in younger non-mature clusters (e.g., Punggol with mean lease of 91.2 years; Sengkang with 87.3 years).
* **Financial Rationale:** Acquiring at S$4,200–S$4,600/sqm maximizes functional living space (95–118 sqm) while ensuring that at the end of a typical 20-year holding period, the remaining leasehold will still exceed 65 years. This eliminates CPF housing withdrawal prorations for secondary buyers, safeguarding resale exit liquidity.

### Recommendation 2: Upgraders — Avoid the Mature "<60-Year Liquidity Trap"
* **Action:** Upgraders must avoid deploying significant retirement equity into mature flats with less than 60 years remaining lease (common in older precincts of Ang Mo Kio, Bedok, and Geylang) under the assumption of perpetual price appreciation.
* **Financial Rationale:** While absolute entry prices appear modest (S$330,000–S$380,000), these units face accelerating secondary market friction: prospective future buyers face restricted CPF housing usage and shortened bank loan tenures when remaining lease drops below 60 years. Upgraders holding such assets face compressed liquidity windows and should reallocate toward young mature resale stock (>80 years lease).

### Recommendation 3: Mortgage Lenders & AVMs — S$3,264/Year Hedonic Valuation Standard
* **Action:** Mortgage underwriters, property tax assessors, and Automated Valuation Models (AVMs) should calibrate public housing valuation engines with our empirical hedonic benchmarks: **+S$3,263.77 per remaining lease year**, **+S$3,798.70 per square meter**, and **+S$6,670.19 per storey level**.
* **Financial Rationale:** Incorporating explicit hedonic parameters prevents collateral mispricing, decouples intrinsic location value from leasehold expiration, and accurately flags listings trading outside their mathematical fair-value band.

---

## 4. Methodology & Data Lineage

### 4.1 Data Pipeline & Feature Engineering
* **Data Sourcing:** Curated transactional observations from `../../data/hdb_resale_sample.csv` (5,000 records).
* **Lease Metrication:** String values in `remaining_lease` (e.g. `"61 years 04 months"`) were parsed into continuous floating-point years:
  $$\text{LeaseYears} = \text{Years} + \frac{\text{Months}}{12}$$
* **Vertical Storey Metrication:** Categorical ranges in `storey_range` (e.g. `"10 TO 12"`) were transformed into continuous mid-point values (e.g. 11.0).
* **Statutory Classification:** Towns were categorized into statutory designations:
  * *Mature (15 Towns):* Ang Mo Kio, Bedok, Bishan, Bukit Merah, Bukit Timah, Central Area, Clementi, Geylang, Kallang/Whampoa, Marine Parade, Pasir Ris, Queenstown, Serangoon, Tampines, Toa Payoh.
  * *Non-Mature (11 Towns):* Bukit Batok, Bukit Panjang, Choa Chu Kang, Hougang, Jurong East, Jurong West, Punggol, Sembawang, Sengkang, Woodlands, Yishun.

### 4.2 Multivariate Hedonic OLS Model
$$\text{ResalePrice} = \beta_0 + \beta_1 (\text{LeaseYears}) + \beta_2 (\text{FloorArea}_{\text{sqm}}) + \beta_3 (\text{IsMature}) + \beta_4 (\text{StoreyLevel}) + \epsilon$$

* **Model Diagnostics:**
  * \(\beta_0\) (Constant): -S$287,588.72
  * \(\beta_1\) (Remaining Lease / Year): **+S$3,263.77** (\(p < 0.001\))
  * \(\beta_2\) (Floor Area / Sqm): **+S$3,798.70** (\(p < 0.001\))
  * \(\beta_3\) (Mature Estate Premium): **+S$139,694.43** (\(p < 0.001\))
  * \(\beta_4\) (Elevation / Storey): **+S$6,670.19** (\(p < 0.001\))
  * \(R^2 = 0.7238\) (72.4% of total price variation explained)
  * Sample Size: \(N = 5,000\)

---

## 5. Interactive Decision Engine (`index.html`)

The accompanying dashboard at [`index.html`](./index.html) features an integrated **Housing Affordability & Lease Decay Engine**:
* Calculates maximum purchase budgets under the statutory **30% Mortgage Servicing Ratio (MSR)** and 25-year loan tenures.
* Projects remaining leasehold upon eventual exit given user-selected holding horizons (10, 20, or 30 years).
* Delivers real-time risk flags indicating whether the secondary buyer pool will encounter CPF housing usage restrictions.
