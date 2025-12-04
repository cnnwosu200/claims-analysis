# Claims-Analysis

## Project Description

The goal of this assignment is to practice supporting practical decision-making and revenue cycle management by analyzing healthcare claims data from Stony Brook University Hospital. This assignment examines billing patterns, prevalent diagnoses and procedures, payer relationships, and service use.

## Data Source Information

Data Provider: Stony Brook University Hospital

Data Format: Three interconnected CSV files

Dataset Files:

1. HEADER File (`STONYBRK_20240531_HEADER.csv`)
* Contains claim-level information (one row per claim)
* Includes provider NPIs, service dates, payer information, and place of service
2. LINE File (`STONYBRK_20240531_LINE.csv`)
* Contains service line details (multiple rows per claim)
* Includes CPT/HCPCS codes, charges, units, and modifiers
3. CODE File (`STONYBRK_20240531_CODE.csv`)
* Contains diagnosis codes (multiple rows per claim)
* Includes ICD-10 codes and code qualifiers

## How to Run the Notebook

**Prerequisites**
* Google account (for Google Colab access)
* The three CSV data files

**Installation Steps**
1. Access Google Colab
2. Upload Data Files
   - Download the three CSV files provided
   - In Colab, click the folder icon in the left sidebar
   - Click the upload icon and select all three CSV files
   - Wait for the upload to complete
3. Install required Libraries
4. Update file paths
     ```
     DATA_DIR = Path('/content')
     HEADER_CSV = DATA_DIR / 'STONYBRK_20240531_HEADER.csv'
     LINE_CSV = DATA_DIR / 'STONYBRK_20240531_LINE.csv'
     CODE_CSV = DATA_DIR / 'STONYBRK_20240531_CODE.csv'
     ```
5. Run the analysis for each question

**Note on Data Storage**

- Files uploaded to Colab session storage are temporary and will be deleted when the session ends.

## Summary of Key Findings

* **Question 4: Common Procedures**
  - Critical care billing (CPT 99291, 68 cases) and detailed hospital care codes (99233, 45 cases) show that the intensive care unit and step-down unit are very busy, which means that the correct number of staff and resources needs to be allocated.

* **Question 5: Service Location Analysis**
  - About two-thirds (63.64%) of claims come from inpatient settings, while only one-third (36.36%) come from office visits. This shows that the hospital needs to invest in inpatient beds, ICU space, and 24/7 medical coverage, which are well worth it.

* **Question 9: Creative Analysis**
  - Surgical specialists usually use seven to nine diagnosis codes per claim for very complicated cases. On the other hand, high-volume general medicine providers (SB Internists, 152 claims) have a lower average complexity of three diagnoses, which clearly shows the difference between secondary specialist care and primary medical management.
  

## Required Libraries 
```

pandas>=1.3.0
matplotlib>=3.4.0
seaborn>=0.11.0

```

All required libraries are listed in **requirements.txt**
