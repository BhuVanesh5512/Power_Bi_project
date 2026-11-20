# Power BI Data Analysis Projects

A collection of Power BI reports and datasets built around product-category analysis and global bank interest-rate trends. The repository includes CSV datasets, report files, and image assets used in the dashboards.

## Project Overview

### 1. Product and Category Analysis

The main report, `project_dashboards.pbix`, is supported by five product datasets:

| Dataset | Records | Example fields |
|---|---:|---|
| Groceries | 5,258 | Item, price, rating, category, packed date, expiry date, quantity, brand |
| Stationery | 3,857 | Category, sub-category, brand, product name, type, colour, variant, price, rating, stock |
| Beauty products | 10,000 | Product, price, rating, brand, category, product type, size, skin type |
| Electronics | 5,999 | Product, brand, category, price, rating, release year, currency, rating count |
| Medicines | 8,392 | Medicine, manufacturer, price, rating, category, salt composition, dosage form, pack size, prescription requirement, uses |

**Total product records: 33,506** across the five CSV files in the current repository version.

### 2. Global Bank Interest Rate Analysis

The separate report, `opt2/Bank Interest Rate Analysis.pbix`, uses `opt2/global_bank_interest_rates.csv`.

The dataset contains **2,323 observations** and includes fields such as:

- Country and country codes
- Bank name and institution type
- Observation date, year, and month
- Interest rate and rate name
- Reference period and rate definition

The dataset includes observations for the Reserve Bank of India as well as central-bank and monetary-authority records from other countries. The rate definition and reference-period fields help distinguish what each published rate represents.

## Data Collection and Preparation

The datasets were compiled through **web research with ChatGPT used as an AI-assisted research and data-preparation tool**.

The collection workflow involved:

1. Identifying relevant product, medicine, grocery, stationery, electronics, and financial-rate information from publicly available web pages.
2. Using ChatGPT to assist with finding relevant information, organizing fields, structuring records, and reviewing consistency.
3. Compiling the collected information into category-wise CSV files with consistent column formats where appropriate.
4. Preparing the CSV files for import and analysis in Power BI.

**Data-source note:** ChatGPT was used to assist the research and preparation process; it should not be treated as the original publisher of the data. Values should be checked against the relevant website or official institution before being used for decisions. The current CSV files do not contain a source URL for every individual record, so complete record-level source tracing is not available from the files alone. Product prices, ratings, availability, and published interest rates can change over time.

## Repository Structure

```text
Power_Bi_project/
│
├── Datasets/
│   ├── GROCERIES.csv
│   ├── Stationary.csv
│   ├── beauty products.csv
│   ├── electronics.csv
│   └── medicines.csv
│
├── Images/
│   ├── Dashboard background and category images
│   └── Home Page Images/
│
├── opt2/
│   ├── Bank Interest Rate Analysis.pbix
│   └── global_bank_interest_rates.csv
│
├── project_dashboards.pbix
└── readme.md
```

## Tools and Technologies

- **Microsoft Power BI Desktop** — report creation, data modeling, and visualization.
- **CSV** — dataset storage and exchange.
- **ChatGPT** — assistance with web research, data organization, and preparation.
- **Git and GitHub** — version control, repository management, and project backup.

## How to Open the Reports

1. Download or clone this repository.
2. Install Microsoft Power BI Desktop.
3. Open `project_dashboards.pbix` for the product/category reports, or open `opt2/Bank Interest Rate Analysis.pbix` for the interest-rate report.
4. If Power BI asks for a data location, update the source path to the matching CSV file in the downloaded repository.
5. Refresh the data in Power BI after confirming the source paths.

## Git and GitHub Workflow

Git was used to track project changes and GitHub to store and manage the repository.

A typical workflow for updating this project is:

```bash
# Clone the repository
git clone https://github.com/BhuVanesh5512/Power_Bi_project.git
cd Power_Bi_project

# Get the latest changes
git pull origin main

# Create a separate working branch
git checkout -b update-dashboard

# Review changed files
git status

# Stage the files you want to save
git add .

# Commit with a descriptive message
git commit -m "Update Power BI dashboard and datasets"

# Push the branch to GitHub
git push -u origin update-dashboard
```

After pushing, create a pull request on GitHub to review and merge the changes into `main`. For a small change made directly on the main branch, the usual sequence is `git pull`, edit files, `git add`, `git commit`, and `git push`.

## Notes

- Keep the CSV files in their expected relative folders, or update the data-source paths in Power BI.
- Refresh reports when the underlying CSV data changes.
- Keep source URLs and collection dates alongside future dataset updates to make data provenance easier to verify.
- Medicine information is included for data-analysis purposes only; this project is not a medical reference or a source of treatment advice.
