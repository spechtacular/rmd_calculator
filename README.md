# 📘 RMD Calculator & Multi-Year Projection

A lightweight Python tool for calculating **Required Minimum Distributions (RMDs)** from traditional IRAs and projecting future account balances over multiple years.

This script uses the **IRS Uniform Lifetime Table (Table III)** and supports:

* RMD calculation starting at age 73
* Multi-year projection of account balances
* Growth rate modeling
* Tax withholding adjustments
* CSV export
* XLSX export with proper currency formatting
* Clean, readable Terminal output

Ideal for retirees, planners, and anyone wanting a simple, transparent RMD projection tool.

---

## 📦 Features

### ✔ RMD Calculation

Uses the IRS **Uniform Lifetime Table** divisor for your age.

### ✔ Multi-Year Projection

For each projected year, the script computes:

* Beginning balance
* RMD amount
* Taxes withheld
* Net distribution received
* Ending balance after growth

### ✔ Growth Rate

Assumes a fixed annual portfolio return (e.g., 3%, 4%, 5%).

### ✔ Tax Withholding

Automatically subtracts the percentage before calculating your ending balance.

### ✔ CSV Export

Saves results to a `.csv` file readable by Excel, Google Sheets, Numbers, etc.

### ✔ XLSX Export

Creates a fully formatted Excel workbook with:

* Bold headers
* Auto-sized columns
* Proper U.S. currency formatting ($#,##0.00)

---

## 🛠 Requirements

Your environment needs:

* **Python 3.8+**
* **openpyxl** (for XLSX export)

Install with:

```bash
pip install openpyxl
```

---

## 🚀 How to Run

From inside the project folder:

```bash
python rmd_projection.py
```

You will be prompted for:

1. Your age
2. Prior year’s IRA balance
3. Years to project
4. Annual growth percentage
5. Tax withholding percentage

After the projection prints, you may choose to export the output to XLSX.

---

## 📤 Exporting to Excel

If you choose `y` at the export prompt:

```
Export results to XLSX? (y/n): y
Enter XLSX filename (e.g., rmd_projection.xlsx):
```

The file saves in the project directory and includes full currency formatting.

---

## 📁 Project Structure

```
rmd_calculator/
│
├── rmd_projection.py      # Main script
├── README.md              # Project documentation
└── requirements.txt       # (optional) Dependency list
```

Create a `requirements.txt` like this if you want one:

```
openpyxl
```

---

## 📊 Example Output (Terminal)

```
Yr  Age     Start Balance          RMD         Tax    Net Rcvd    End Balance
1   73      $500,000.00        $18,867.92   $3,773.58  $15,094.34  $505,566.04
2   74      $505,566.04        $19,825.73   $3,965.15  $15,860.58  $509,700.24
...
```

---

## ⚠ Disclaimer

This tool is **not tax, legal, or financial advice**.
Always double-check RMD values with your IRA custodian or financial professional.

---

## 🤝 Contributing

Pull requests welcome.
If you want support for:

* Roth conversions
* Joint Life Table (spouse >10 years younger)
* Side-by-side multi-scenario projections

…open an issue or request an enhancement.

---


