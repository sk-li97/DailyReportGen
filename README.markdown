# Daily Report Generator

## Overview
This script generates a daily report by processing advertising data from Huawei's advertising platform (Jinghong Kinetic). It aggregates data by date, region, and product, calculates CPI and ROAS, and outputs a formatted Excel file.

## Features
- Merges country/region and conversion data.
- Filters specific regions (e.g., Russia, Southeast Asia).
- Aggregates data by date, region, and product.
- Calculates CPI (based on conversion data) and ROAS.
- Outputs raw and formatted data to Excel with styled formatting.

## Requirements
- Python 3.10+
- pandas
- openpyxl

Install dependencies:
```bash
pip install pandas openpyxl
```

## Usage
Usage





Place input Excel files in C:\Users\lili.li\Downloads\:





区域-国家.xlsx (country/region mapping)



国家_地区报表_YYYY-MM-DD-YYYY-MM-DD_分日 (5).xlsx (request data)



国家_地区报表_YYYY-MM-DD-YYYY-MM-DD_分日 (6).xlsx (conversion data)



Update file paths in the Notebook's code cell (lines ~8-10) to match your data files and date range.



Update the output file path (line ~124) to C:\Users\lili.li\Desktop\日报\output-多比特-STARTDATE-ENDDATE.xlsx.



Open 日报多个时间-单一代码块.ipynb in Jupyter Notebook.



Run all cells to generate the report.


## Output
- Excel file with two sheets:
  - `原始数据`: Raw merged data.
  - `数据展示`: Formatted report with region totals, CPI, and ROAS.

## Notes
- Ensure input files are not open when running the script to avoid permission errors.
- The script assumes specific column names in input files (e.g., '时间', '国家/地区', '产品名称').

## License
MIT License
