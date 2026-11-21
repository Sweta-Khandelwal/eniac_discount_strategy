# Eniac Discount Strategy Optimization
### Exploratory data analysis of discounting prevalence, revenue concentration, category performance, and seasonality for Eniac.

---

### Contributors: Team Index

- [**Sweta Khandelwal**](https://github.com/Sweta-Khandelwal)

---

## 📦 Deliverables

- 📊 **[Final Presentation Deck (PDF)](documents/eniac_discount_strategy_deck.pdf)**
- 📄 **[Exploratory Analysis Log (PDF)](documents/eniac_exploratory_analysis_log.pdf)**
- 💻 **[Python Analysis Notebook](script/eniac_discount_strategy_script.ipynb)**
- 🗂️ **[Cleaned & Raw Datasets](data/)**

---

## 🎯 Project Overview

Created as a group project at **WBS Coding School**, this case study evaluates how Eniac's discounting behavior relates to revenue performance across time, discount brackets, product categories, and item conditions. By cleaning Eniac's transactional tables and running exploratory analysis in Python, we examined whether deep or frequent discounts drive stronger revenue—and outlined a more disciplined promotional strategy.

---

### Business Context

* **Eniac:** An online retailer specializing in Apple products and compatible technology accessories across product categories ranging from storage and flagship devices to cables, cases, and networking gear.
* **Pricing & Promotion Challenge:** Discounting is widespread across the catalog, making it critical to distinguish genuine promotional lift from baseline markdowns and seasonal shopping peaks.

---

### 🚀 Key Findings

* **Discounting is the baseline:** Roughly 93% of items sell below shelf price, with revenue heavily concentrated in the **10–25%** (~€3.47M / ~44.4%) and **1–10%** (~€2.65M / ~33.9%) discount buckets.
* **Steeper discounts do not guarantee higher revenue:** Discount tiers of **50%+** contribute a minimal share of revenue (~1.9%), while flagship hardware such as iPads performs strongly with lighter **1–10%** markdowns.
* **Seasonality drives major revenue waves:** Revenue surges around peak promotional periods—led by Black Friday/Cyber Week and December holiday sales—before tapering off into spring.
* **Pre-owned items carry heavy discounts for a small revenue share:** Pre-owned products experience higher median discounts (~27.9% vs. ~17.4% for new items) while accounting for only ~6.2% of revenue.

---
## Insights & Recommended Strategy

| Area | Analytical Takeaway | Recommended Action |
| :--- | :--- | :--- |
| **Discount Frequency** | ~93% of items sell below list price, mostly in the **10–25%** (~44.4%) and **1–10%** (~33.9%) tiers | Reduce reliance on constant discounting and protect full-price sales where demand holds |
| **Discount Depth & Revenue** | Higher discounts don't guarantee higher revenue; **50%+** brings minimal revenue (~1.9%) while flagships thrive at **1–10%** | Keep **10–25%** as the sweet spot and cap most discounts at **25%**, with rare exceptions |
| **Pre-Owned Inventory** | Pre-owned items carry steeper median discounts (~27.9% vs. ~17.4%) for a small revenue share (~6.2%) | Move pre-owned markdowns into a controlled, safer discount tier rather than heavy cuts |
| **Seasonality** | Revenue spikes around Black Friday/Cyber Week and December before cooling into spring | Run a targeted **Post-Holiday Sale in February** to clear excess stock ahead of March |

---

## 📊 Dataset & Sources

* **Source:** Eniac sales database provided by [WBS Coding School](https://github.com/WBSCodingSchool), organized across relational tables (`orders`, `orderlines`, `products`, and `brands`).
* **Observation Window:** Data runs from **1 January 2017** through **14 March 2018**, capturing ~€7.82M in analyzed revenue (~€4.93M during peak sale season vs. ~€2.88M off-season).
* **Key Variables Used:**
  * `orders` & `orders_cleaned`: Order identifiers, timestamps, order statuses, and totals.
  * `orderlines` & `orderlines_cleaned`: Line-item quantities, prices actually paid, and item-level discount calculations.
  * `products` & `products_cleaned`: Product identifiers, shelf prices, categories, and new vs. pre-owned attributes.
  * `brands`: Brand reference records.
* **Data Limitations & Preprocessing Notes:** 
  * **March 2017 Dip:** Low recorded revenue in March 2017 reflects an order-status recording issue in the source data rather than an actual sales drop.
  * **Observation Cutoff:** Data runs through **14 March 2018**.
  * **Revenue vs. Profit:** Unavailability of cost lead to no analysis of actual profits.

 ## 📁 Repository Structure

```text
├── README.md                                   # Project overview, key findings & strategy
├── script/
│   └── eniac_discount_strategy_script.ipynb    # Data cleaning, EDA & visualization notebook
├── data/
│   ├── cleaned/                                # Processed datasets (orderlines, orders, products)
│   └── raw/                                    # Original source CSV files
├── documents/
│   ├── eniac_discount_strategy_deck.pdf        # Final presentation deck
│   └── eniac_exploratory_analysis_log.pdf      # Exploratory analysis log & recommendations
└── images/
    ├── 01_daily_revenue_seasonality.svg
    ├── 02_discounted_vs_full_price_scatter.svg
    ├── 03_revenue_and_median_discount_by_category.svg
    ├── 04_total_revenue_distribution_by_discount_bucket.svg
    ├── 05_new_vs_preowned_performance.svg
    ├── 06_strategic_discount_tiers_by_category.svg
    └── 07_monthly_revenue_vs_median_discount.svg
```

## 🔗 How to Use This Project

1. **Quick executive summary:** Open the [Final Presentation (PDF)](documents/eniac_discount_strategy_deck.pdf) for the slide-by-slide findings and strategic recommendations.
2. **Detailed analysis & takeaways:** Review the [Exploratory Analysis Log (PDF)](documents/eniac_exploratory_analysis_log.pdf) for step-by-step observations and the closing summary matrix.
3. **Reproduce the analysis:** Open [`eniac_discount_strategy_script.ipynb`](script/eniac_discount_strategy_script.ipynb) in Jupyter Notebook or Google Colab and run the cells sequentially using the files in [`data/`](data/).

## 📬 Contact

- **GitHub:** [Sweta-Khandelwal](https://github.com/Sweta-Khandelwal)
- **LinkedIn:** [Sweta Khandelwal](https://www.linkedin.com/in/khandelwal-sweta/)
