# IFood-Case

This repository contains my solution for the iFood technical case.

## Context: 
Having an efficient offer distribution strategy is a specific challenge due to the multiple aspects involved. A suitable coupon distribution strategy not only attracts customers to a service but can also establish a long-term relationship.

## Objectives: 
1. Analyze historical transaction, offer, and customer data.
2. Develop a technique/model to help decide which offer to send to each customer.
3. Demonstrate the potential impact of your solution on the business.
   
## REquirements:
- Python 3.11+
- Java 11+ (for PySpark)
- Dependencies in requirements.txt

## Repo Structure
```
ifood-case/
├── data/                             # Datasets
│ ├── raw/                            # Dados originais
│ └── processed/                      # Dados processados
├── notebooks/                        # Jupyter notebooks
│ ├── 1_data_processing.ipynb
│ └── 2_modeling.ipynb
├── presentation/                     # Slides para stakeholders
├── src/                              # Código fonte (opcional)
├── README.md
└── requirements.txt
```
## Setup:
```
python -m venv .venv
source .venv/bin/activate        # or .\.venv\Scripts\activate on Windows
pip install -r requirements.txt
```

## Running order: 
1. Install 'requirements.txt'
2. Run '1_data_processing.ipynb'
3. Run '2_modeling.ipynb'

## Notes: 
The project was implemented on "Databricks Community Edition". 
In Community or Free edition you only have access to serverless compute. 
In this serverless compute, access to legacy directory such as Filestore is not allowed. 
Access to the legacy DBFS root is restricted or disabled to move to secure storage pattern UC Volumes.
To access the ifood json files, we need to create a managed volume in Unity Catalog (configuration included in '1_data_processing.ipynb')

** If you are not gonna use databricks, you will need to change the paths to access and save files in the notebooks.
