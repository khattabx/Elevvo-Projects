# RFM Customer Segmentation

This project applies **RFM (Recency, Frequency, Monetary)** analysis to an online retail dataset in order to perform structured customer segmentation. The workflow demonstrates the use of Python, data cleaning, and visualization techniques for actionable business insights.

---

## Project Workflow

The end-to-end process included:

- Acquiring and exploring raw transactional data  
- Cleaning and preprocessing the dataset (Excel and Python)  
- Implementing RFM logic to calculate customer metrics  
- Visualizing customer segments and related business insights  
- Documenting the entire pipeline in a Jupyter Notebook  

---

## Dataset Information

- **Dataset**: Online Retail  
- **Source**: UCI Machine Learning Repository  
- **Format**: Excel (`Online Retail.xlsx`)  
- **Description**: Contains historical transactional data from a UK-based online store  
- **Key Columns**: InvoiceNo, StockCode, Description, Quantity, InvoiceDate, UnitPrice, CustomerID, Country  

---

## Data Preparation

- Converted `InvoiceDate` to datetime format  
- Filtered out rows with missing `CustomerID`  
- Excluded canceled transactions (`InvoiceNo` starting with "C")  
- Added computed column `TotalPrice = Quantity × UnitPrice`  
- Ensured dataset integrity for RFM calculations  

---

## Notebook: `Customer_Segmentation_RFM.ipynb`

The notebook contains:

1. Data loading and inspection  
2. Data preprocessing and filtering  
3. Calculation of RFM metrics:  
   - **Recency**: Days since last purchase  
   - **Frequency**: Number of transactions  
   - **Monetary**: Total spending  
4. Scoring of RFM values using quintiles (1–5)  
5. Creation of composite RFM scores (e.g., 543, 111)  
6. Customer segmentation mapping (Champions, Loyal, At Risk, etc.)  
7. Merging RFM results back into the dataset for advanced analysis  

---

## Visualizations

Implemented using **Matplotlib**:

- Customer distribution across segments (bar and pie charts)  
- Average monetary value by segment  
- Top countries ranked by segment volume  
- Overview of key business metrics (customers, revenue, order value, etc.)  

---

## Project Files

| File                              | Description                                                     |
|-----------------------------------|-----------------------------------------------------------------|
| `Customer_Segmentation_RFM.ipynb` | Jupyter Notebook with full workflow and visualizations          |
| `Online Retail.xlsx`              | Raw dataset from UCI                                            |
| `full_dataset_with_rfm.csv`       | Processed dataset including RFM scores and segment labels       |
| `README.md`                       | Project documentation                                           |

---

## How to Run

Clone or download the repository  

```bash
   git clone git@github.com:khattabx/Customer-Segmentation-RFM.git
   cd Customer-Segmentation-RFM
```

Install required libraries:  

   ```bash
   pip install pandas matplotlib openpyxl
   ```
