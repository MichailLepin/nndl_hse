### 🧠 “Seoul Bike Sharing EDA (Front-End JS Version)”

You are a front-end data-visualisation engineer.
Build a **single-page web app (`index.html`)** that performs **Exploratory Data Analysis (EDA)** of the dataset **SeoulBikeData.csv** — all computations must happen **entirely in the browser**, no backend or Python allowed.

#### 📂 Data

* The CSV file `SeoulBikeData.csv` will be hosted in the same repo (e.g. `./SeoulBikeData.csv`).
* Use **PapaParse** (CDN) to load and parse the CSV asynchronously.
* Parse the `Date` column as JavaScript Date objects and keep the `Hour` column as integer.

#### 🧮 Data Processing

* Compute and display in HTML tables:

  * first 5 rows of data
  * summary statistics (mean, median, std) for all numeric columns
  * missing-value counts per column
* All calculations must be done in JS using built-in functions (no backend, no pandas).

#### 📊 Visualisations (using Plotly.js)

1. **Distribution Plots**

   * Histograms or KDE-like density curves for
     `Rented Bike Count`, `Temperature`, `Humidity`, `Wind Speed`.
   * Add clear titles, axis labels and tooltips.

2. **Hourly and Monthly Trends**

   * Group by `Hour` and plot average rented bike count per hour (line chart).
   * Group by `Month` (or derived season) and plot average demand (bar chart).
   * Highlight or annotate peak hours and peak months.

3. **Categorical Analysis**

   * Create boxplots or pointplots showing how `Rented Bike Count` varies by
     `Seasons`, `Holiday`, and `Functioning Day`.

4. **Correlation Matrix**

   * Compute Pearson correlations for all numeric columns.
   * Render an interactive **heatmap** (Plotly heatmap) and highlight the features with highest positive/negative correlation with `Rented Bike Count`.

#### 🧭 Insights Section

At the bottom of the page, render a short textual summary automatically generated in JS:

* peak demand hours and months
* weather effects (temperature ↗ vs humidity ↘)
* whether missing data exists
* implications for predictive modelling

#### 🧰 Technical Requirements

* Pure front-end: HTML + JS only.
* Use CDNs for all libraries:

  ```html
  <script src="https://cdn.jsdelivr.net/npm/papaparse@5.4.1/papaparse.min.js"></script>
  <script src="https://cdn.plot.ly/plotly-latest.min.js"></script>
  ```
* The page should automatically load the CSV and render all charts on load — no file upload buttons or manual triggers.
* Code must be compatible with GitHub Pages (no Node.js, no bundler).

#### 📁 Folder structure

```
/ (root)
 ├── index.html        ← main EDA dashboard
 ├── SeoulBikeData.csv ← dataset
 └── /assets (optional for CSS)
```
