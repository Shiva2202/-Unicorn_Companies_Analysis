# 🦄 Unicorn Companies Analysis

An exploratory data analysis (EDA) of the world's **unicorn companies** — privately held startups valued at **$1 billion or more** — using Python, Pandas, Matplotlib, and Seaborn.

The project cleans a real-world dataset of 1,074 companies and explores which industries, countries, and continents dominate the unicorn landscape, and how funding relates to valuation.

---

## 📌 Table of Contents

- [Project Overview](#-project-overview)
- [Dataset](#-dataset)
- [Tech Stack](#-tech-stack)
- [Project Structure](#-project-structure)
- [Analysis Workflow](#-analysis-workflow)
- [Key Insights](#-key-insights)
- [How to Run](#-how-to-run)
- [Future Improvements](#-future-improvements)
- [Author](#-author)

---

## 🎯 Project Overview

The goal of this project is to answer questions such as:

- Which industries produce the most unicorns?
- Which industries have the highest average valuation?
- Where in the world are unicorns concentrated?
- Is there a relationship between the funding a company raises and its valuation?

---

## 📂 Dataset

**File:** `Unicorn_Companies.xlsx` — 1,074 rows × 10 columns

| Column | Description |
|---|---|
| `Company` | Name of the company |
| `Valuation` | Company valuation (e.g. `$180B`, `$850M`) |
| `Date Joined` | Date the company reached unicorn status |
| `Industry` | Industry / sector |
| `City` | Headquarters city |
| `Country` | Headquarters country |
| `Continent` | Headquarters continent |
| `Year Founded` | Year the company was founded |
| `Funding` | Total funding raised (e.g. `$8B`, `$500M`) |
| `Select Investors` | Notable investors |

---

## 🛠 Tech Stack

- **Python 3**
- **Pandas** & **NumPy** – data manipulation
- **Matplotlib** & **Seaborn** – data visualization
- **OpenPyXL** – reading Excel files
- **Jupyter Notebook / Google Colab**

---

## 📁 Project Structure

```
Unicorn-Companies-Analysis/
│
├── Unicorn_Companies.xlsx             # Raw dataset
├── Unicorn_Companies_Analysis.ipynb   # Analysis notebook
└── README.md                          # Project documentation
```

---

## 🔄 Analysis Workflow

1. **Data Loading** – Import the Excel dataset into a Pandas DataFrame.
2. **Data Overview** – Inspect shape, columns, data types, and summary statistics.
3. **Data Cleaning**
   - Checked missing values (count and percentage per column).
   - Filled missing `City` values with `"Unknown"`.
   - Converted `Valuation` and `Funding` from text (`$180B`, `$850M`) into numeric columns `Valuation_B` and `Funding_B` (in billions of dollars).
4. **Univariate Analysis** – Unicorn count by industry; distribution of valuations.
5. **Bivariate Analysis** – Valuation vs. funding; average valuation by industry.
6. **Multivariate Analysis** – Valuation vs. funding, colored by continent and sized by valuation.
7. **Correlation Analysis** – Pearson correlation between valuation and funding.

---

## 📊 Key Insights

- **Fintech** leads with the most unicorns (224), followed by **Internet software & services** (205) and **E-commerce & direct-to-consumer** (111).
- **North America** (589) and **Asia** (310) account for the large majority of unicorns; the **United States** (562), **China** (173), and **India** (65) are the top three countries.
- Valuations are **heavily right-skewed**: the median is about $2B, while a few giants (e.g. Bytedance at $180B) pull the average up to roughly $3.5B.
- **Artificial intelligence** has the highest average valuation among the top industries.
- Valuation and funding show a **moderate positive correlation (~0.60)** — more funding tends to go with higher valuation, but it is far from the whole story.

> Numbers above are computed from the dataset in this repo; re-run the notebook to reproduce the charts.

---

## 🚀 How to Run

1. **Clone the repository**
   ```bash
   git clone https://github.com/Shiva2202/Unicorn-Companies-Analysis.git
   cd Unicorn-Companies-Analysis
   ```

2. **Install dependencies**
   ```bash
   pip install pandas numpy matplotlib seaborn openpyxl jupyter
   ```

3. **Launch the notebook**
   ```bash
   jupyter notebook Unicorn_Companies_Analysis.ipynb
   ```

4. **Update the file path** in the data-loading cell if needed (the notebook was written on Google Colab):
   ```python
   file_path = 'Unicorn_Companies.xlsx'
   ```

You can also open the notebook directly in **Google Colab** and upload the dataset.

---

## 🔮 Future Improvements

- Analyze unicorn growth over time using `Date Joined` and `Year Founded`.
- Time-to-unicorn analysis (years from founding to $1B valuation).
- Investor-level analysis (most active investors).
- Country- and city-level breakdowns and an interactive dashboard (Plotly / Streamlit / Power BI).

---

## 👤 Author

**Borath Shiva Kumar**

- GitHub: [@Shiva2202](https://github.com/Shiva2202)

---

⭐ If you found this project useful, consider giving it a star!
