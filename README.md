# Nautilus Data Insights: Maritime Sales Pipeline & Dimensional Modeling

🌐 *Read this in Portuguese (BR):* **English** | [Português](#-nautilus-data-insights-pipeline-de-vendas-marítimas-e-modelagem-dimensional)

---

This project develops an end-to-end Data Processing Pipeline (ETL) and Dimensional Modeling focused on sales history, CRM customer management, import costs, and currency exchange rates for a maritime and nautical equipment company.

The primary objective is to transform raw, multi-format data (CSV, JSON) into an analytical structure optimized for business insight extraction, profit margin calculation, and performance analysis.

## 🚀 Technologies Used

* **Python 3.x**
* **Pandas:** Data cleaning, manipulation, and transformation.
* **Regex (Regular Expressions):** Text standardization and complex string extraction.
* **Jupyter Notebook / Google Colab:** Development and prototyping environment.

## 🛠️ ETL Process & Data Quality

The project mitigates data inconsistencies from source systems through the following pipeline stages:
1. **Location Standardization:** Utilizing Regex to extract State acronyms (UF) and isolate municipality names from misaligned strings in the CRM dataset.
2. **Complex String Handling:** Correcting and unifying emails containing invalid characters (e.g., replacing `#` with `@`).
3. **Product Category Normalization:** Mapping via Regular Expressions to consolidate over 30 poorly written text variations into 3 official macro-categories (*electronics, propulsion, and anchoring*).
4. **Data Typing:** Converting monetary strings (e.g., `R$ 33122.52`) into appropriate numerical formats (`float64`) for mathematical calculations.
5. **Deduplication:** Identifying and removing duplicate records to ensure primary key uniqueness.

## 📐 Dimensional Modeling (Star Schema)

To guarantee high performance in analytical queries and facilitate seamless integration with Data Visualization tools (such as Power BI or Tableau), the data architecture follows a **Star Schema** pattern.

The structure consists of a central fact table surrounded by dimension tables, enabling granular analysis by customer, product, time, and geographic location.

### Model Architecture


---
## 📈 Next Steps
* Final joining of the fact table with import costs (`custos_importacao.json`) and exchange rates (`bcdata.sgs.csv`) to calculate net profit and currency conversion margins.
* Building business metrics (such as RFM Analysis - Recency, Frequency, Monetary).
