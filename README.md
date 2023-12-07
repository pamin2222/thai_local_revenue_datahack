## [DataHack] Thailand Local Administration: Special Grant and Local Revenue Data

### Data source
ข้อมูลเงินอุดหนุนเฉพาะกิจ / รายได้ท้องถิ่น
https://twitter.com/teng_mfp/status/1731115208557703516

### Dataset
Original datasets are available in `/data` folder. The datasets are in CSV format downloaded from the original Google Sheets.

- `data_processed` folder contains the processed datasets in CSV format.
- `data_processed/local_revenue_61to65_processed.csv` 
 is an aggregated dataset of local revenue from year 61 to 65. 
Plus, initial data cleaning as follows:
  - Normalize column names
  - Concatenate all datasets into one with 'data_year' column indicating the year of the data, 'row_id' column as an index.
  - Convert financial values to numeric
  - strip whitespace for string columns, and row values
  - Correct typo & normalize values for 'จังหวัด', 'อำเภอ', and 'ชื่อท้องถิ่น'

### Code
- `1_local_revenue_61to65_concat_clean.ipynb` is a Jupyter notebook for data cleaning and aggregation.

- [WIP] `2_local_revenue_61to65_eda.ipynb` is a Jupyter notebook for exploratory data analysis.