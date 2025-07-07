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
1. Place input Excel files in the specified paths (see `config.json`).
2. Update `config.json` with correct file paths and target regions.
3. Run the script:
```bash
python daily_report.py
```

## Configuration
Edit `config.json` to set:
- Input file paths (`country_file`, `data_file`, `conversion_file`).
- Output file path (`output_file`).
- Target regions (`target_regions`).

## Output
- Excel file with two sheets:
  - `原始数据`: Raw merged data.
  - `数据展示`: Formatted report with region totals, CPI, and ROAS.

## Notes
- Ensure input files are not open when running the script to avoid permission errors.
- The script assumes specific column names in input files (e.g., '时间', '国家/地区', '产品名称').

## License
MIT License