# 🧠 Economic Complexity Analysis — Iran (ECI Project)

This repository hosts the complete workflow, datasets, and tools for analyzing the **Economic Complexity Index (ECI)**, **Product Complexity Index (PCI)**, and **Product Space** of **Iran**.  
It follows the methodology of Hausmann & Hidalgo and aims to model and visualize the evolution of Iran’s economic complexity between **2000 and 2025**.

<br>

##  Project Team

- **Yasin Shamsedini** — Data Science & Machine Learning Lead  
- **Ehsan Masoumi** — Economic Research & Policy Analysis  

<br>

## Goals

1. Build the trade data matrix (`M_{c,p}`) for Iran and global partners using HS4 classification.  
2. Compute **RCA**, **ECI**, and **PCI** metrics for all countries and years.  
3. Construct the **Product Space** network and identify **potential export opportunities** for Iran.  
4. Develop **forecasting models** to predict future ECI trends.  
5. Build an interactive **Streamlit dashboard** and produce the final analytical **PDF report**.

<br>

## Repository Structure

```plaintext
economic-complexity-ir/
├─ data/
│   ├─ raw/                # Unprocessed trade data (from UN Comtrade or other sources)
│   └─ processed/          # Clean, standardized data used in analysis
├─ notebooks/
│   ├─ 01_data_fetching.ipynb       # Download and merge trade data
│   ├─ 01b_data_cleaning.ipynb      # Cleaning and standardization
│   ├─ 02_rca_mcp.ipynb             # RCA and binary M_cp matrix
│   ├─ 03_eci_pci.ipynb             # ECI / PCI computation
│   ├─ 04_product_space.ipynb       # Product Space and density
│   └─ 05_ml_forecasting.ipynb      # Predictive modeling and validation
├─ report/
│   ├─ QA_data_summary.md
│   └─ Final_Report.pdf
├─ streamlit_app.py
├─ requirements.txt
└─ README.md
````

<br>

## Data Sources

* **UN Comtrade API** — Annual trade data

  * Reporter: *Iran (364)*
  * Partner: *World (0)*
  * Classification: HS4
  * Period: 2000 – 2025

Additional references:

* [World Bank — WDI](https://databank.worldbank.org/source/world-development-indicators)
* [OEC / Harvard Growth Lab](https://oec.world/)
* National export statistics

<br>

## ⚙️ Installation

Clone the repo and install dependencies:

```bash
git clone https://github.com/<yourusername>/economic-complexity-ir.git
cd economic-complexity-ir
pip install -r requirements.txt
```

Or using Conda:

```bash
conda create -n eci python=3.10
conda activate eci
pip install -r requirements.txt
```

---

## How to Use

1. **Data Collection** — Run `notebooks/01_data_fetching.ipynb` to fetch trade data.
2. **Cleaning** — Run `notebooks/01b_data_cleaning.ipynb` to prepare the dataset.
3. **RCA & M_cp** — Compute RCA and the binary export matrix.
4. **ECI & PCI** — Calculate complexity metrics using `03_eci_pci.ipynb`.
5. **Visualization & Modeling** — Explore product space and forecasting in later notebooks.

QA results are stored in `report/QA_data_summary.md`.

---

## Roadmap

| Phase | Title                         | Deliverables                       |
| ----- | ----------------------------- | ---------------------------------- |
| 1     | Data Acquisition & Cleaning   | Master trade table, QA report      |
| 2     | RCA & M_cp Matrix             | RCA tables, binary M_cp files      |
| 3     | ECI/PCI Calculation           | ECI_PCI_timeseries.csv             |
| 4     | Product Space & Opportunities | proximity_phi.csv, density_IRN.csv |
| 5     | Modeling & Forecasting        | ML models and performance reports  |
| 6     | Dashboard & Visualization     | Streamlit app                      |
| 7     | Final Reporting               | PDF report and presentation        |

<br>



## 📄 License

MIT License © 2025 Yasin Shamsedini & Ehsan Masoumi

<br>


<!--
---

## Dashboard

Once analysis is complete, you can launch the interactive dashboard:

```bash
streamlit run streamlit_app.py
```


## 📬 Contact

* 📧 Yasin Shamsedini — [[your_email@example.com](mailto:your_email@example.com)]
* 📧 Ehsan Masoumi — [[your_email@example.com](mailto:your_email@example.com)]

---

> *“Economic complexity is not just about exports — it’s about the knowledge embedded in what a country can make.”*

-->

