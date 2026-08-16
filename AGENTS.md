# Federal Data Field Guide: LLM & Agent Operating Instructions

This repository contains the authoritative source code, raw data, and structural definitions for the **Federal Data Field Guide** (April 2026, V.1), produced by the Executive Fellowship in Applied Technology Policy (a joint program of UC Berkeley's School of Information and Goldman School of Public Policy)[cite: 2]. When an LLM or AI agent is invoked to assist with queries using this guide, it MUST strictly adhere to the guidelines, schemas, and operational constraints defined below[cite: 2].

---

## I. Core Mission & Scope Constraints

1. **Scope & Exclusions**: This guide focuses exclusively on publicly available datasets created, maintained, and published by executive branch agencies of the U.S. federal government[cite: 2]. It **excludes** sensitive or classified datasets, as well as derivative works such as reports or interactive web tools that use data[cite: 2].
2. **Verifiable Information Only**: Never invent, extrapolate, or hallucinate non-existent federal agencies, datasets, or classification codes[cite: 2]. All dataset identities, agency affiliations, and metadata mappings must be strictly verifiable against the guide or repository contents[cite: 2].
3. **Platypus Principle (Multi-Category Classification)**: Datasets do not always fit neatly into a single category (hence the duck-billed platypus mascot)[cite: 2]. When a dataset exhibits multi-category traits, assign a **Primary Category** and list relevant **Secondary Categories**[cite: 2].
4. **Direct & Objective Tone**: Communicate plainly and directly. Avoid hyperbole, marketing fluff, or conversational setup sentences. Begin responses immediately with structured tables or direct facts.

---

## II. Primary Data Categories & Functional Ontology

All federal datasets must be categorized using the **eight primary categories** defined in the Federal Data Field Guide[cite: 2]. Agents must not use external domain groupings (e.g., "Health", "Economy", "Environment"), as the guide's taxonomy is organized by **collection methods, policy frameworks, and functional use cases**[cite: 2].

| Category Identifier | Category Name | Primary Definition & Scope | Primary Collection Modes | Key Governing Laws & Policies |
| :--- | :--- | :--- | :--- | :--- |
| `CAT-STAT` | **Statistical Data** | Measures group- and population-level characteristics of people, businesses, and the economy to inform planning, policymaking, and resource allocation[cite: 2]. | Surveys, interviews (in-person, phone, mail, web), third-party reports (e.g., law enforcement), administrative supplements[cite: 2]. | CIPSEA, Title 13 (Census), Title 26 (IRS Sec. 6103), PRA, Privacy Act, FERPA, HIPAA[cite: 2]. |
| `CAT-ADMIN` | **Administrative Data** | Generated through routine government operations and transactions, such as program eligibility, benefit delivery, regulation, and tax administration[cite: 2]. | Program application forms, regulatory filings, electronic records, internal agency databases, third-party institutions (lenders, states)[cite: 2]. | Privacy Act (SORNs), FOIA, OPEN Government Data Act, HMDA, NEPA, HIPAA, FERPA[cite: 2]. |
| `CAT-GEO` | **Geospatial Data** | Contains specific location attributes (latitude/longitude, addresses, or spatial references) capturing spatial and environmental information[cite: 2]. | Satellite and aerial imagery, environmental sensors, GPS/address surveys, interagency or commercial data agreements[cite: 2]. | Geospatial Data Act (GDA), National Spatial Data Infrastructure (NSDI), Privacy Act, GeoPlatform[cite: 2]. |
| `CAT-SCI` | **Scientific Data** | Generates, validates, and replicates findings that advance knowledge across scientific disciplines, clinical trials, and theoretical models[cite: 2]. | Research sensors, biological sampling, time-limited field measurements, spaceflight experiments, continuous monitoring[cite: 2]. | FAIR Principles, Evidence Act, Information Quality Act (IQA), OSTP Public Access Policies, Common Rule[cite: 2]. |
| `CAT-ACCT` | **Accountability Data** | Measures government functions, spending, policy implementation, and service delivery to provide transparency into government activities[cite: 2]. | Administrative financial systems, operational software, performance metrics, compliance logs, FOIA request logs[cite: 2]. | DATA Act, FFATA, FOIA, Food and Nutrition Act, Information Quality Act (IQA), OPEN Government Data Act[cite: 2]. |
| `CAT-EVAL` | **Evaluation Data** | Analyzes the design, implementation, and impact of government initiatives to determine value, relevance, and areas for program improvement[cite: 2]. | Mixed methods (one-time or targeted studies), surveys, qualitative interviews, experiments, secondary administrative/statistical data[cite: 2]. | Foundations for Evidence-Based Policymaking Act (Evidence Act - Agency Learning Agendas), Privacy Act (SORNs), CIPSEA, IQA[cite: 2]. |
| `CAT-NAV` | **Navigation Data** | Characterizes federal and non-federal resources in a structured way to help citizens and software identify relevant benefits, services, or information[cite: 2]. | Centralized resource inventories, administrative/reference lists, interagency portals, API-driven web catalogs[cite: 2]. | OPEN Government Data Act (open by default/machine-readable), IQA, FDAAA, Uniform Guidance, FFATA[cite: 2]. |
| `CAT-REF` | **Reference Data** | Provides structure, standardization, and consistency (classification codes, boundaries, official names) across other data sources to enable interoperability[cite: 2]. | Administrative coding processes, statistical geography definitions, legislative/regulatory directives, geospatial surveying[cite: 2]. | Evidence Act Data Inventories, OPEN Government Data Act, Geospatial Data Act (FGDC standards), IQA[cite: 2]. |

---

## III. Legal & Governance Framework Ontology

When describing the legal context, privacy constraints, or access restrictions of any dataset, reference the appropriate statutory or policy frameworks below:

* **Privacy & Security**:
  * **Privacy Act of 1974**: Governs PII handling; requires Systems of Records Notices (SORNs) and limits disclosures to routine uses[cite: 2].
  * **FISMA / OMB Circular A-130**: Governs cybersecurity, risk management, and federal IT as strategic assets[cite: 2].
  * **CIPSEA (Title III of Evidence Act)**: Protects data collected under a pledge of confidentiality for statistical/evidence-building purposes only; shields data from enforcement, tax, or immigration uses[cite: 2].
  * **Title 13 (Census) & Title 26 (IRS Sec. 6103)**: Enforces strict confidentiality for census responses and tax return information[cite: 2].
  * **HIPAA & FERPA**: Sector-specific privacy laws protecting health records and student educational records[cite: 2].
* **Transparency & Evidence-Building**:
  * **OPEN Government Data Act (OGDA)**: Mandates that non-sensitive data be "open by default" in machine-readable formats and indexed on Data.gov[cite: 2].
  * **Evidence Act of 2018**: Requires agency Learning Agendas, Comprehensive Data Inventories, and establishes Chief Data Officers, Evaluation Officers, and Statistical Officials[cite: 2].
  * **FOIA**: Mechanism for public record requests, subject to statutory privacy exemptions[cite: 2].
* **Data Quality & Governance**:
  * **Paperwork Reduction Act (PRA)**: Requires OMB approval for public data collections from 10+ persons to minimize burden[cite: 2].
  * **Information Quality Act (IQA)**: Enforces objectivity, utility, and integrity of published data, including correction mechanisms for influential data[cite: 2].
  * **Geospatial Data Act (GDA)**: Governs location data standards through the FGDC and GeoPlatform[cite: 2].
  * **FAIR Principles**: Mandates scientific research data be Findable, Accessible, Interoperable, and Reusable[cite: 2].

---

## IV. Execution Workflow for Dataset Identification & Inquiries

**Sequential Logic**:
* **Step 1: Categorization Strategy**
  * Identify the primary function of the dataset based on the Field Guide's 8 categories[cite: 2].
  * If a dataset exhibits multi-category traits (Platypus principle), designate a **Primary Category** and **Secondary Category**[cite: 2].
* **Step 2: Verification**
  * Verify the official dataset title, managing department/agency, collection mode, and legal governing authorities[cite: 2].
  * If a dataset is not cataloged or is a derivative report/interactive tool, state clearly that it falls outside the guide's primary dataset scope[cite: 2].
* **Step 3: Response Formatting**
  * **No Introductory Fluff**: Do not include setup phrasing (e.g., "Here is the dataset information:"). Start directly with the structured response.
  * **No Labeled Closings**: End with a standard paragraph or table; do not include headers like `Summary:` or `Conclusion:`.

---

## V. Verified Dataset Inventory (Index from Guide)

When identifying datasets or answering inquiries, verify the query against this canonical list of datasets explicitly cited in the Federal Data Field Guide:

### Statistical Data (`CAT-STAT`)
* **American Community Survey (ACS)** (U.S. Census Bureau / Department of Commerce)[cite: 2]
* **Decennial Census** (U.S. Census Bureau)[cite: 2]
* **National Incident-Based Reporting System (NIBRS)** (Federal Bureau of Investigation)[cite: 2]
* **Survey of Consumer Finances (SCF)** (Federal Reserve Board)[cite: 2]
* **Survey of Household Economics and Decisionmaking (SHED)** (Federal Reserve Board)[cite: 2]
* **National Crime Victimization Survey (NCVS)** (Bureau of Justice Statistics)[cite: 2]
* **Law Enforcement Management & Administrative Statistics (LEMAS)** (Bureau of Justice Statistics)[cite: 2]
* **National Assessment of Educational Progress (NAEP)** (Department of Education)[cite: 2]
* **National Survey of College Graduates (NSCG)** (National Science Foundation)[cite: 2]
* **Consumer Price Index (CPI)** (Bureau of Labor Statistics)[cite: 2]
* **Behavioral Risk Factor Surveillance System (BRFSS)** (Centers for Disease Control and Prevention)[cite: 2]

### Administrative Data (`CAT-ADMIN`)
* **IRS Form 990 Data** (Internal Revenue Service)[cite: 2]
* **Characteristics of SNAP Households** (Food and Nutrition Service / USDA)[cite: 2]
* **RePORTER (Research Portfolio Online Reporting Tools)** (National Institutes of Health)[cite: 2]
* **H-1B Employer Data Hub** (U.S. Citizenship and Immigration Services / DHS)[cite: 2]
* **Home Mortgage Disclosure Act (HMDA) Data** (Consumer Financial Protection Bureau)[cite: 2]
* **Housing Assistance Program Data - Owners** (Federal Emergency Management Agency / DHS)[cite: 2]
* **Geographic Distribution of VA Expenditure (GDX)** (Department of Veterans Affairs)[cite: 2]
* **Defense Casualty Analysis System (DCAS)** (Department of Defense)[cite: 2]
* **Single Family Section 502 Direct Active Loans** (U.S. Department of Agriculture)[cite: 2]
* **FAFSA Completion by High School & Public School District** (Department of Education)[cite: 2]
* **National Vital Statistics System (NVSS) Birth Data** (Centers for Disease Control and Prevention / HHS)[cite: 2]

### Geospatial Data (`CAT-GEO`)
* **North American Bat Monitoring (NABat) Database** (U.S. Geological Survey)[cite: 2]
* **Cropland Data Layer** (National Agricultural Statistics Service / USDA)[cite: 2]
* **Next Generation Weather Radar (NEXRAD)** (National Oceanic and Atmospheric Administration)[cite: 2]
* **National Bridge Inventory (NBI)** (Department of Transportation)[cite: 2]
* **Power Plants in the U.S.** (Energy Information Administration / DOE)[cite: 2]
* **Military Training Routes (MTRs)** (Federal Aviation Administration)[cite: 2]
* **National Water Dashboard** (U.S. Geological Survey)[cite: 2]
* **Air Quality System (AQS)** (Environmental Protection Agency)[cite: 2]
* **Landsat** (NASA / USGS)[cite: 2]
* **Public Housing Developments** (Department of Housing and Urban Development)[cite: 2]
* **Geospatial Health Systems** (Department of Health and Human Services)[cite: 2]

### Scientific Data (`CAT-SCI`)
* **Framingham Heart Study (FHS)** (National Institutes of Health / HHS)[cite: 2]
* **Atmospheric Radiation Monitoring Dataset (ARM)** (Department of Energy / Oak Ridge National Laboratory)[cite: 2]
* **Dolphin Sound Production** (NOAA / U.S. Navy)[cite: 2]
* **database of Genotypes and Phenotypes (dbGaP)** (National Institutes of Health)[cite: 2]
* **All of Us** (National Institutes of Health)[cite: 2]
* **ScienceHub** (Environmental Protection Agency)[cite: 2]
* **Dr. Duke's Phytochemical & Ethnobotanical Databases** (U.S. Department of Agriculture)[cite: 2]
* **National Ecological Observatory Network (NEON)** (National Science Foundation)[cite: 2]
* **Local Climatological Data** (NOAA / NCEI)[cite: 2]
* **Biological Data Repository** (National Aeronautics and Space Administration)[cite: 2]
* **National Invasive Species Information Center Species Profiles** (U.S. Department of Agriculture)[cite: 2]

### Accountability Data (`CAT-ACCT`)
* **SNAP Application Processing Timeliness** (Food and Nutrition Service / USDA)[cite: 2]
* **Approved Apportionments Data** (Office of Management and Budget)[cite: 2]
* **Freedom of Information Act (FOIA) Requests** (Department of Justice)[cite: 2]
* **Information Collection Review Data** (Office of Management and Budget)[cite: 2]
* **USASpending** (Department of the Treasury)[cite: 2]
* **Historical National Median Processing Time** (USCIS / DHS)[cite: 2]
* **National 800 Number Network Average Speed to Answer** (Social Security Administration)[cite: 2]
* **State Medicaid and CHIP Applications, Eligibility Determinations, and Enrollment Data** (Centers for Medicare & Medicaid Services / HHS)[cite: 2]
* **Federal Government Energy and Water Use** (Department of Energy)[cite: 2]
* **Assault and Use of Force** (Customs and Border Protection / DHS)[cite: 2]

### Evaluation Data (`CAT-EVAL`)
* **Weatherization Assistance Program (WAP) Retrospective Evaluation** (Department of Energy / ORNL)[cite: 2]
* **WIC Tribal Organizations & U.S. Territories Study** (U.S. Department of Agriculture)[cite: 2]
* **Telehealth Resource Center Performance Measurement** (Health Resources and Services Administration / HHS)[cite: 2]
* **RETAIN (Retaining Employment & Talent After Injury/Illness Network) Evaluation** (Department of Labor / SSA)[cite: 2]
* **Pathways to Partnerships Program Evaluation** (Department of Education)[cite: 2]
* **Innovation Corps (I-Corps) Program Dataset** (National Science Foundation)[cite: 2]
* **Malaria Behavioral Survey (MBS) Data** (U.S. Agency for International Development)[cite: 2]
* **Evidence & Evaluation Clearinghouses**: Pathways to Work Evidence Clearinghouse, HomVEE, Title IV-E Prevention Services Clearinghouse, CrimeSolutions (NIJ), NREPP (SAMHSA), What Works Clearinghouse (IES)[cite: 2].

### Navigation Data (`CAT-NAV`)
* **Health Care Access & Quality Information** (Department of Veterans Affairs)[cite: 2]
* **PubMed** (National Institutes of Health)[cite: 2]
* **Permitting Innovation Center Categorical Exclusions** (Council on Environmental Quality)[cite: 2]
* **PatentsView** (U.S. Patent and Trademark Office)[cite: 2]
* **Data.gov** (General Services Administration)[cite: 2]
* **SNAP Retailer Locator** (U.S. Department of Agriculture)[cite: 2]
* **Medicare Provider Data Catalog** (Centers for Medicare & Medicaid Services)[cite: 2]
* **FAS AAS Opportunities Dashboard** (General Services Administration)[cite: 2]
* **ClinicalTrials.gov** (National Institutes of Health)[cite: 2]
* **Grants.gov** (Department of Health and Human Services)[cite: 2]
* **Harmonized Tariff Schedule** (U.S. International Trade Commission)[cite: 2]

### Reference Data (`CAT-REF`)
* **National Spatial Reference System (NSRS)** (NOAA / National Geodetic Survey)[cite: 2]
* **Administrative Boundaries of National Park System Units** (National Park Service / DOI)[cite: 2]
* **U.S. Maritime Limits & Boundaries** (National Oceanic and Atmospheric Administration)[cite: 2]
* **Metropolitan & Micropolitan Statistical Area Delineations** (Office of Management and Budget)[cite: 2]
* **North American Industry Classification System (NAICS)** (Office of Management and Budget)[cite: 2]
* **Census Designated Places** (U.S. Census Bureau)[cite: 2]
* **TIGER/Line Shapefiles** (U.S. Census Bureau)[cite: 2]
* **Orange Book (Approved Drug Products with Therapeutic Equivalence Evaluations)** (Food and Drug Administration)[cite: 2]
* **National Vulnerability Database** (National Institute of Standards and Technology)[cite: 2]
* **Federal School Code Lists** (Department of Education)[cite: 2]

---

## VI. Standardized Output Templates

### 1. Single Dataset Lookup Format

**Dataset Name**: [Official Dataset Title]  
**Managing Agency**: [Department / Bureau / Office]  
**Primary Category**: `[CAT-ID]` ([Category Name])[cite: 2]  
**Secondary Category**: `[CAT-ID]` ([Category Name] or *None*)[cite: 2]  

| Attribute | Metadata Detail |
| :--- | :--- |
| **Collection Mode** | [Surveys / Administrative Forms / Sensors / Mixed Methods / etc.][cite: 2] |
| **Governing Policy/Laws** | [CIPSEA / Privacy Act / OGDA / GDA / Evidence Act / etc.][cite: 2] |
| **Access & Portals** | [Open Access / Restricted Access / API / Data.gov / GeoPlatform][cite: 2] |
| **Data Use Case** | [Summary of practical/policy use case from guide][cite: 2] |

### 2. Multi-Dataset Comparison / Query Format

| Dataset Name | Agency | Primary Category | Collection Mode | Legal & Policy Framework |
| :--- | :--- | :--- | :--- | :--- |
| [Dataset 1] | [Agency 1] | `[CAT-ID]`[cite: 2] | [Mode 1][cite: 2] | [Policy/Law 1][cite: 2] |
| [Dataset 2] | [Agency 2] | `[CAT-ID]`[cite: 2] | [Mode 2][cite: 2] | [Policy/Law 2][cite: 2] |
