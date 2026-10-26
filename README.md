# STA-SLR: E-Commerce Sales Trend Analysis using Simple Linear Regression

[![GitHub Pages](https://img.shields.io/badge/Live-Demo-brightgreen?logo=github)](https://teena0620.github.io/STA-SLR/)
[![Built with HTML5](https://img.shields.io/badge/HTML5-E34F26?logo=html5&logoColor=white)](https://developer.mozilla.org/en-US/docs/Web/HTML)
[![Styled with CSS3](https://img.shields.io/badge/CSS3-1572B6?logo=css3&logoColor=white)](https://developer.mozilla.org/en-US/docs/Web/CSS)
[![Powered by JavaScript](https://img.shields.io/badge/JavaScript-ES6+-F7DF1E?logo=javascript&logoColor=black)](https://developer.mozilla.org/en-US/docs/Web/JavaScript)
[![Chart.js](https://img.shields.io/badge/Chart.js-v4.4-FF6384?logo=chartdotjs&logoColor=white)](https://www.chartjs.org/)
[![PapaParse](https://img.shields.io/badge/PapaParse-v5.4-blue)](https://www.papaparse.com/)
[![License: MIT](https://img.shields.io/badge/License-MIT-yellow.svg)](LICENSE)

An interactive, client-side web application for analyzing e-commerce sales trends and predicting revenue using data mining, exploratory data analysis (EDA), and **Simple Linear Regression (SLR)**.

The project helps business owners, managers, and data analysts explore sales performance, discover seasonal and categorical patterns, measure the exact relationship between advertising spend and sales revenue, and test predictive "what-if" budget scenarios through an engaging, neo-brutalist dashboard.

---

## 🚀 Live Demo

You can try the live version hosted on GitHub Pages:  
👉 **[https://teena0620.github.io/STA-SLR/](https://teena0620.github.io/STA-SLR/)**

*(Or download this repository and double-click `index.html` to run locally in any web browser—no build tools or servers required!)*

---

## ✨ Key Features

### 1. 📊 Interactive Sales Trend Dashboard
- **Monthly Revenue Trend (`c1`)**: Track revenue over time with area highlights and monthly peaks.
- **Revenue by Category (`c2`)**: Compare performance across various product categories.
- **Top-Selling Products (`c3`)**: Ranked horizontal bar chart showcasing top revenue generators.
- **Orders by Category (`c4`)**: Donut chart detailing order volume distribution.
- **Order Value Histogram (`c5`)**: Statistical distribution of customer basket values.
- **Advertising Spend vs. Revenue (`c6`)**: Scatter plot exploring correlation between marketing budget and sales.

### 2. 🧪 Simple Linear Regression Lab
- **Ordinary Least Squares (OLS) Fit**:
  $$\hat{y} = b_0 + b_1 x$$
  Computes optimal slope ($b_1$) and intercept ($b_0$) in real time.
- **Fitted Regression Line (`r1`)**: Plots actual data points alongside the calculated line of best fit.
- **Residual Analysis Plot (`r2`)**: Displays errors ($y - \hat{y}$) against the baseline to verify model assumptions.
- **Model Goodness-of-Fit & Error Metrics**:
  - **Coefficient of Determination ($R^2$)**: Measures the proportion of variance explained by the model.
  - **Mean Absolute Error (MAE)**: Quantifies the average prediction error in dollar terms.
  - **Root Mean Squared Error (RMSE)**: Penalizes larger outliers to assess prediction reliability.
  - **Sample Size ($n$) & Excluded Count**: Explicit reporting of valid vs. skipped missing data points.

### 3. 🎯 Interactive Sales Prediction & Extrapolation Warning
- **Dual Controls**: Synchronized numeric input field (`#pin`) and range slider (`#psl`).
- **Real-Time Prediction**: Instant evaluation of predicted revenue $\hat{y}$ for any hypothetical $X$ budget.
- **Extrapolation Safety Guard**: Alerts users when an entered budget lies outside the observed domain ($[X_{\min}, X_{\max}]$), warning that out-of-sample extrapolation may be unreliable.

### 4. 📂 Client-Side CSV Upload & Auto Column Mapping
- **100% Private & In-Browser**: Uploaded files are parsed locally via PapaParse without sending data to any external server.
- **Automatic Header Detection**: Smart regex identification of date, category, product, order ID, quantity, price, advertising spend, and sales columns.
- **Manual Re-Mapping Interface**: Easily adjust column assignments via UI dropdowns to match any custom dataset schema.
- **Derived Revenue**: Automatically calculates `Revenue = Quantity × Unit Price` if an explicit revenue column is missing.
- **Data Quality Safeguard**: Preserves missing cells without silently coercing them to zero.

### 5. 🔍 Data Explorer & Statistical Summary
- **Live Search & Filter**: Search rows across any attribute or filter by date range and category.
- **Sortable Data Table**: Multi-direction column sorting (ascending/descending) with clean pagination.
- **Descriptive Statistics Table**: Auto-computes count, missing cells, mean, median, min, max, and sample standard deviation ($s$) for all numeric fields.

### 6. 💡 Business Insights Engine
- Dynamically generates business recommendations based on the active dataset:
  - Highest-earning product category and percentage contribution.
  - Peak monthly revenue period.
  - Month-over-month recent sales growth rate.
  - Top 3 revenue-driving products.
  - Correlation coefficient ($r$) strength and direction.
  - Actionable expected return per incremental unit of advertising spend.

---

## 📐 Mathematical Formulation

### 1. Slope ($b_1$) and Intercept ($b_0$)
$$b_1 = \frac{S_{xy}}{S_{xx}} = \frac{\sum_{i=1}^n (x_i - \bar{x})(y_i - \bar{y})}{\sum_{i=1}^n (x_i - \bar{x})^2}$$

$$b_0 = \bar{y} - b_1 \bar{x}$$

### 2. Goodness of Fit ($R^2$)
$$R^2 = 1 - \frac{SSE}{SST} = 1 - \frac{\sum (y_i - \hat{y}_i)^2}{\sum (y_i - \bar{y})^2}$$

### 3. Model Accuracy Metrics
$$\text{MAE} = \frac{1}{n} \sum_{i=1}^n |y_i - \hat{y}_i|$$

$$\text{RMSE} = \sqrt{\frac{1}{n} \sum_{i=1}^n (y_i - \hat{y}_i)^2}$$

---

## 📁 Repository Structure

```text
STA-SLR/
├── index.html           # Main application (HTML, CSS, JavaScript)
├── sample_data.csv      # Sample 200-row e-commerce dataset for testing
├── README.md            # Project documentation & instructions
├── LICENSE              # MIT License
└── .gitignore           # Git ignore file
```

---

## 🛠️ Getting Started

### Method 1: Run Locally
1. Clone the repository:
   ```bash
   git clone https://github.com/teena0620/STA-SLR.git
   ```
2. Navigate into the folder:
   ```bash
   cd STA-SLR
   ```
3. Open `index.html` in any modern web browser (Google Chrome, Microsoft Edge, Firefox, Safari).

### Method 2: Test with Sample Data
1. Download [sample_data.csv](sample_data.csv).
2. Scroll to the **Data Explorer** section in the web application.
3. Click **Upload CSV** and select `sample_data.csv`.
4. Observe all 6 charts, summary metrics, regression fit, and insights update instantly!

---

## 🌐 Enabling GitHub Pages (Hosting for Free)

To publish this website live on GitHub:
1. Go to your repository on GitHub: `https://github.com/teena0620/STA-SLR`.
2. Click **Settings** (tab at the top).
3. In the left sidebar, click **Pages**.
4. Under **Build and deployment > Source**, select **Deploy from a branch**.
5. Under **Branch**, select `main` and folder `/ (root)`.
6. Click **Save**.
7. In ~1 minute, your site will be live at:  
   **`https://teena0620.github.io/STA-SLR/`**

---

## 👤 Author

- **Teena Vishwakarma**  
  GitHub: [@teena0620](https://github.com/teena0620)

---

## 📄 License

This project is open-source and licensed under the [MIT License](LICENSE).
