# Python Data Analysis Notebooks

**Python · pandas · NumPy · Seaborn · Matplotlib · Jupyter / Google Colab**

Two exploratory projects covering data inspection, grouped analysis, feature creation, and visualization. The original notebook filenames and saved outputs are retained.

| Project | Focus | Status |
| --- | --- | --- |
| [Automobile fuel efficiency](#automobile-fuel-efficiency) | MPG, vehicle features, missing values, correlations | Analysis with saved outputs; original input file not bundled |
| [911 calls exploration](#911-calls-exploration) | Call categories, locations, timestamps, heatmaps | Guided capstone with saved outputs; input CSV not bundled |

For a self-contained business case study with an included dataset, see [E-commerce Sales & Customer Behavior](https://github.com/govhersalmanova/ecommerce-sales-customer-behavior-analysis).

## Automobile fuel efficiency

[View notebook](Govhar_Salmanova_Automobile_Analysis.ipynb) · [Open in Colab](https://colab.research.google.com/github/govhersalmanova/data-analysis-notebook/blob/main/Govhar_Salmanova_Automobile_Analysis.ipynb)

**Question:** How does fuel efficiency vary with vehicle weight, horsepower, cylinders, origin, and model year?

The saved analysis covers **398 vehicles and nine fields**, including six missing horsepower values. It standardizes column names, converts numeric fields, checks missing values and duplicates, and uses distributions, grouped comparisons, scatterplots, and correlations.

Findings from the saved notebook outputs:

- Average fuel efficiency is **23.51 MPG**.
- Weight has a strong negative correlation with MPG (**r = −0.832**).
- Average MPG is **30.45** for Japan, **27.89** for Europe, and **20.08** for the USA within this sample.
- Four-cylinder cars average **29.29 MPG**, compared with **14.96 MPG** for eight-cylinder cars.

These are descriptive associations in the available sample. They do not isolate causal effects or constitute a prediction model. Horsepower calculations omit missing observations; group comparisons do not control for model year or vehicle mix.

**Rerun:** Open in Colab and upload the original CSV or Excel file when prompted. Required columns: `name`, `mpg`, `cylinders`, `displacement`, `horsepower`, `weight`, `acceleration`, `model_year`, `origin`. The original data file and its provenance are not included, so the saved results have not been independently regenerated from that input.

## 911 calls exploration

[View notebook](G%C3%B6vh%C9%99r_Salmanova_02_911_Calls_Data_Capstone_Project_Solutions.ipynb) · [Open in Colab](https://colab.research.google.com/github/govhersalmanova/data-analysis-notebook/blob/main/G%C3%B6vh%C9%99r_Salmanova_02_911_Calls_Data_Capstone_Project_Solutions.ipynb)

**Question:** How do recorded emergency calls vary by reason, township, day, and hour?

This notebook retains the prompts and solutions format of a guided capstone. Its cited data source is [Montgomery County 911 calls on Kaggle](https://www.kaggle.com/mchirico/montcoalert). The original course/template attribution should be confirmed before presenting it as independently designed work.

The saved snapshot contains **99,492 calls**:

- EMS: **48,877** calls.
- Traffic: **35,695** calls.
- Fire: **14,920** calls.
- Lower Merion has the highest recorded township count: **8,443** calls.

Techniques include extracting call reasons from text, parsing timestamps, creating hour/month/weekday features, grouping data, and producing heatmaps and cluster maps.

**Rerun:** Obtain the appropriate `911.csv` snapshot from the cited source and place it beside the notebook. In Colab, upload it to the session before running the load cell. Later source versions may contain different row counts and results.

**Interpretation limits:** Missing ZIP codes, townships, and addresses are present. Several original trend plots count non-null `twp` values, so they omit calls with missing township. Month-only grouping also combines years if a multi-year dataset is supplied. Absolute counts are not population-adjusted risk measures and should not be used directly for staffing or safety decisions.

## Environment

```sh
python -m pip install -r requirements.txt
python -m jupyter lab
```

The automobile notebook uses a Colab upload widget; use its Colab link for that workflow. Local execution requires adapting that input cell. Dependencies are declared, not locked to a verified full-run environment.

## Repository contents

- `Govhar_Salmanova_Automobile_Analysis.ipynb` — fuel-efficiency exploration.
- `Gövhər_Salmanova_02_911_Calls_Data_Capstone_Project_Solutions.ipynb` — guided emergency-call exploration.
- `requirements.txt` — local Python dependencies.
- `docs/portfolio-roadmap.md` — next steps to develop these studies into reproducible case studies.

Visuals are embedded in the notebooks; no standalone screenshots or datasets are currently bundled. No explicit repository license is present.
