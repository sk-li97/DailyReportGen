# DailyReportGen

## Overview
This Jupyter Notebook (`日报多个时间-单一代码块.ipynb`) generates daily advertising reports from Huawei's Jinghong Kinetic platform. It processes data by merging regio/country and conversion data, filters specific regions (Russia, Southeast Asia, Asia-Pacific, Latin America), aggregates by date, region, and product, calculates CPI (based on conversion data) and ROAS, and outputs a formatted Excel file with raw and styled sheets.由于华为的鲸鸿动能平台非常容易闪退，所以没有采取爬虫的方式，每天更新的文件路径也差距不大，直接用jupyter是我的个人习惯。

## Features
- Merges country/region and conversion data.
- Filters data for specified regions.
- Aggregates data by date, region, and product.
- Calculates CPI (conversion-based) and ROAS.
- Outputs to Excel with two sheets: `原始数据` (raw data) and `数据展示` (formatted report with styling).

## Requirements
- Python 3.10+
- pandas
- openpyxl

Install dependencies:
```bash
pip install pandas openpyxl
```

## Usage
1. Place input Excel files in `C:\Users\lili.li\Downloads\`:
   - `区域-国家.xlsx` (country/region mapping)
   - `国家_地区报表_YYYY-MM-DD-YYYY-MM-DD_分日 (5).xlsx` (request data)
   - `国家_地区报表_YYYY-MM-DD-YYYY-MM-DD_分日 (6).xlsx` (conversion data)
2. Update file paths in the Notebook's code cell (lines ~8-10) to match your data files and date range.
3. Update the output file path (line ~124) to `C:\Users\lili.li\Desktop\日报\output-多比特-STARTDATE-ENDDATE.xlsx`.
4. Open `日报多个时间-单一代码块.ipynb` in Jupyter Notebook.
5. Run all cells to generate the report.

## Output
- Excel file with two sheets:
  - `原始数据`: Raw merged data.
  - `数据展示`: Formatted report with region totals, CPI, ROAS, and styled formatting (headers, region rows, and totals).

## Notes
- Ensure input and output files are not open during execution to avoid permission errors.
- The script assumes specific column names (e.g., `时间`, `国家/地区`, `产品名称`) in input files.
- Update file paths daily to match downloaded data files from Huawei's platform.
- Clear Notebook outputs before committing to GitHub to reduce file size.

## License
MIT License
