# BI System for Sales Department 

This project is a technical test in Data Engineering aimed at the design and implementation of a Business Intelligence (BI) system for decision-making in a company’s purchasing department. The system should provide both financial and operational analyses related to suppliers, using purchasing data and exchange rates.

## Project Requirements

The system must meet the following requirements:

1. **Financial Part:**
   - Determine the total amount of daily purchases, converted to euros, and distributed by company sections.
   - Consider different suppliers, currencies, and daily exchange rates to ensure proper conversion.

2. **Supplier Analysis Part:**
   - Generate a ranking of suppliers based on the total amount purchased and the number of distinct products acquired.
   - Measure the quality of the supplier by comparing the actual lead time of purchases with the theoretical lead time for each supplier and product.

3. **Data Sources:**
   - **Invoice_header**: General purchase data, including supplier information, order dates, receipt dates, and invoice details.
   - **Invoice_products**: Product details per invoice, including quantity, price, and section.
   - **Products**: Product master data.
   - **Suppliers**: Supplier master data.
   - **Daily_currencies**: Historical daily exchange rates.

4. **System Design:**
   - **Datamart**: Create a dimensional datamart to meet the system requirements.
   - **ETL (Extract, Transform, Load)**: Use Python and the `pandas` library to load, transform, and write the tables to the datamart.
   - **Granularity and Modeling**: Justify the design decisions, such as the granularity of the data, relevant dimensions and facts, and their relationships.

## Implementation

The system is implemented in the following documents:

1. **Jupyter Notebook**: Contains Python code to load and transform data from the provided files, perform data modeling, and create the datamart. This file also contains explanatory comments about each step and justification for the decisions made.

2. **User Manual (PDF)**: Provides a detailed explanation of how to use the BI system to obtain the necessary reports and analyses. It relies on a Tableau dashboard that visualizes the data and enables dynamic analysis.

3. **Tableau Document**: Presents the main charts and analyses that answer the questions in the statement, including supplier analysis, purchase amounts, and the comparison between actual and theoretical lead times.

## Optional Functionalities

- **Monthly Purchase Analysis**: Incorporation of an analysis of monthly purchases compared to the purchase budget for each company section. The budget is located in an Excel file named `purchase_budget.xls`.

**Note**: Implementing the optional part does not affect the mandatory functionalities but adds value by enriching the analysis and providing greater insights into the BI system.

## Estructura del Proyecto
/project-directory
├── notebook/
│   └── SistemaBI.ipynb  
├── reports/
│   ├── SistemaBI_ManualUsuario.docx  
│   └── SistemaBI.twb  
├── data/
│   ├── invoice_header.csv  
│   ├── invoice_products.csv  
│   ├── products.csv  
│   ├── suppliers.csv  
│   ├── daily_currencies.csv  
│   └── purchase_budget.xls  
└── README.md  

## Installation

To run the project, make sure you have the following packages installed:

- Python 3.x
- `pandas`
- `numpy`
- `matplotlib` (optional for Python visualizations)

You can install the dependencies using `pip`:

```bash
pip install pandas numpy matplotlib
```

## Usage

### 1. Running the Script in Jupyter Notebook
The script performs the following tasks:

- Load the data from the provided CSV files.
- Clean and transform the data to the required format for the datamart.
- Create the necessary datamart tables and export them as CSV files.

### 2. Visualization in Tableau
The `SistemaBI.twb` file contains all the charts and interactive visualizations that allow the purchasing manager to analyze suppliers, purchase amounts, and supplier performance in terms of lead time.

### 3. User Manual
The manual provides details on how to use the system to query and analyze data, including the visualization and analysis of suppliers, purchases, and delivery times.

## Design Justification
The datamart design and ETL process are based on the specific requirements of the task. The granularity of purchases is determined at the invoice and product level, and the analysis dimensions include suppliers, products, sections, and dates. Transformations such as currency conversion and lead time calculation are applied to meet business needs.

## Conclusions
This project provides an integrated solution for purchase analysis in a company’s purchasing department, with both financial and operational focus. The Python implementation allows for efficient data processing, while Tableau facilitates dynamic visualization of the results.
