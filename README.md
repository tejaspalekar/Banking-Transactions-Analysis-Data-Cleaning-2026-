# Banking Transactions Analysis & Data Cleaning (2026)

This project analyzes a simulated bank transaction dataset containing 50,000 transactions from January 1 to October 10, 2026. The workflow focuses on cleaning the raw data, standardizing fields, identifying inconsistent records, and generating business KPIs for transaction quality and performance.

## Project Objective

The goal is to:

- load and inspect a large transaction dataset
- clean and standardize column names and values
- remove duplicate transaction IDs and invalid records
- convert date and amount fields into usable formats
- calculate KPI metrics such as success rate and transaction value
- prepare cleaned data for further reporting and analysis

## Dataset

The repository includes a simulated HDFC-style dataset:

- `Simulated_HDFC_Style_Bank_Transactions_50000_Jan01_Oct10_2026.xlsx`

The dataset contains transaction-level information such as:

- `transaction_id`
- `transaction_datetime`
- `transaction_date`
- `customer_id`
- `account_type`
- `transaction_type`
- `channel`
- `direction`
- `amount_inr`
- `merchant_category`
- `city`
- `status`
- `is_simulated_data`

## Data Cleaning Steps

The notebook performs the following cleaning operations:

- standardizes column names to lowercase and underscore format
- checks for missing values
- removes duplicate transaction IDs
- converts date columns to proper datetime format
- converts monetary values to numeric values
- removes invalid negative amounts
- standardizes text fields such as status, account type, and transaction type
- fills missing optional category values with a default label
- filters the records to the required date range

## Key KPIs

From the analysis workflow, the dataset produces the following summary metrics:

- Total transactions: 50,000
- Successful transactions: 44,050
- Failed transactions: 3,502
- Unique customers: 7,991
- Successful transaction value: ₹133,860,421.35
- Average successful transaction value: ₹3,038.83
- Success rate: 88.10%

## Output Files

- `cleaned_transactions.csv` — cleaned and standardized transaction dataset
- `monthly_analysis.csv` — monthly metrics summary for successful transactions

## Repository Structure

```text
.
├── README.md
├── Simulated_HDFC_Style_Bank_Transactions_50000_Jan01_Oct10_2026.xlsx
├── banking_py.ipynb
├── cleaned_transactions.csv
├── monthly_analysis.csv
```

## Tools and Libraries

This project uses:

- Python 3
- pandas
- NumPy
- matplotlib
- Jupyter Notebook

## How to Run

1. Open the notebook:
   ```bash
   jupyter notebook banking_py.ipynb
   ```
2. Run the cells in order to:
   - load the dataset
   - clean the records
   - compute KPIs
   - export the cleaned outputs

## Notes

- The data is simulated for analysis purposes.
- The project is designed to demonstrate data-cleaning and KPI reporting workflows typical in banking analytics.
- The notebook is useful as a reference for exploratory data analysis, data quality checks, and summary reporting.

## License

This project is intended for educational and demonstration purposes.

## Author

Tejas Palekar
