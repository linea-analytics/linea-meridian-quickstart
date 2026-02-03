# Meridian Notebook

This repository contains a minimal, end to end example of running a Bayesian Marketing Mix Model using **Google Meridian** in Python.

The notebook walks through data loading, model specification, estimation, and basic diagnostics and outputs such as decompositions and ROI style views.

## Contents

* `quickstart.ipynb`
  Main Jupyter notebook covering the full Meridian workflow.

* `formatted_data.csv`
  Example input dataset containing:

  * media variables
  * control variables (price, economy, events, etc.)
  * target variable

* `requirements.txt`
  Python dependencies required to run the notebook.

## What the notebook does

The notebook is structured as follows:

1. **Overview**
   Brief introduction to Meridian and the modelling approach.

2. **Data loading**
   Loads a pre formatted CSV where all features are already aligned and cleaned.

3. **Model specification**

   * Defines media and control columns
   * Configures priors and transformations implicitly via Meridian
   * Sets Bayesian sampling parameters

4. **Model fitting**
   Runs a Bayesian MMM using `google-meridian`, with conservative defaults chosen for speed rather than final production quality.

5. **Diagnostics and outputs**

   * R-hat checks
   * Model fit plots
   * Channel decompositions
   * ROI style summaries

This notebook is intended as a practical reference or starting point rather than a fully tuned production model.

## Setup

### Requirements

* Python **3.12** (required by Meridian)
* Virtual environment recommended

### Install and run

```bash
python -m venv venv
venv\Scripts\activate

pip install -r requirements.txt
jupyter notebook
```

Then open `quickstart.ipynb` and run the notebook top to bottom.

## Notes

* Sampling parameters (number of chains, draws, etc.) are deliberately kept low for faster iteration. Increase these for real analyses.

If you want, next step could be:

* adding a “data contract” section describing the expected CSV schema, or
* splitting this into a `quickstart` vs `production` notebook so intent is crystal clear.
