# 🏦 Bank Loan Analysis

A comprehensive Python-based analysis of bank loan data focusing on loan performance, risk assessment, and key financial metrics. This project provides insights into loan portfolio health, monthly trends, and various demographic breakdowns.

## 📊 Overview

This analysis examines a dataset of 38,576 loan applications with 24 features, providing detailed insights into:
- Loan performance metrics (Good vs Bad loans)
- Monthly funding and repayment trends
- Geographic and demographic analysis
- Risk assessment indicators
- Key Performance Indicators (KPIs)

## 🎯 Key Findings

### Primary KPIs
- **Total Loan Applications**: 38,576
- **Total Funded Amount**: ₹435.76M
- **Total Amount Received**: ₹473.07M
- **Average Interest Rate**: 12.05%
- **Average DTI Ratio**: 13.33%

### Loan Quality Metrics
- **Good Loans**: 86.18% (33,243 applications)
- **Bad Loans**: 13.82% (5,333 applications)
- **Portfolio Health**: Excellent with positive cash flow

## 🛠️ Technologies Used

- **Python 3.x**
- **pandas** - Data manipulation and analysis
- **numpy** - Numerical computing
- **matplotlib** - Data visualization
- **seaborn** - Statistical data visualization
- **plotly** - Interactive visualizations


## 📈 Analysis Components

### 1. Data Exploration
- Dataset overview and structure
- Data types and missing values analysis
- Descriptive statistics

### 2. Primary KPIs
- Total loan applications (overall and MTD)
- Total funded amount (overall and MTD)
- Total amount received (overall and MTD)
- Average interest rate and DTI ratio

### 3. Loan Quality Assessment
- Good loans analysis (Fully Paid + Current)
- Bad loans analysis (Charged Off)
- Performance metrics and percentages

### 4. Trend Analysis
- Monthly loan applications
- Monthly funded amounts
- Monthly received amounts
- Seasonal patterns identification

### 5. Demographic Analysis
- State-wise loan distribution
- Employment length impact
- Loan purpose breakdown
- Home ownership patterns
- Term-based analysis (36 vs 60 months)

## 📊 Visualizations

The project includes various visualization types:

- **Line Charts**: Monthly trends for applications, funding, and collections
- **Bar Charts**: State-wise and purpose-wise analysis
- **Pie Charts**: Loan term distribution
- **Tree Maps**: Home ownership breakdown
- **Area Charts**: Time series analysis

## 🔍 Key Insights

1. **Portfolio Health**: 86.18% good loan rate indicates excellent risk management
2. **Profitability**: Positive cash flow with ₹473.07M received vs ₹435.76M funded
3. **Risk Balance**: Competitive 12.05% average interest rate
4. **Geographic Concentration**: California, Texas, and New York are top markets
5. **Purpose Distribution**: Debt consolidation is the primary loan purpose
6. **Term Preference**: 60% of loans are 36-month terms

## 🚀 Usage

### Prerequisites

Ensure you have Python 3.7+ installed on your system.

### Installation

1. **Clone the repository**
   ```bash
   git clone https://github.com/yourusername/bank-loan-analysis.git
   cd bank-loan-analysis
   ```

2. **Create a virtual environment**
   ```bash
   python -m venv venv
   source venv/bin/activate  # On Windows: venv\Scripts\activate
   ```

3. **Install dependencies**
   ```bash
   pip install -r requirements.txt
   ```

4. **Run the analysis**
   ```bash
   jupyter notebook notebooks/Bank_Loan_Analysis.ipynb
   ```

## 📋 Requirements

```txt
pandas>=1.3.0
numpy>=1.21.0
matplotlib>=3.4.0
seaborn>=0.11.0
plotly>=5.0.0
jupyter>=1.0.0
```

## 📝 Usage Examples

### Calculate Primary KPIs
```python
import pandas as pd
from src.kpi_calculator import calculate_primary_kpis

df = pd.read_csv('data/financial_loan.csv')
kpis = calculate_primary_kpis(df)
print(f"Total Applications: {kpis['total_applications']}")
```

### Generate Monthly Trend Analysis
```python
from src.visualizations import plot_monthly_trends

plot_monthly_trends(df, metric='loan_amount')
```

### Analyze Loan Quality
```python
from src.data_preprocessing import analyze_loan_quality

good_loans, bad_loans = analyze_loan_quality(df)
print(f"Good Loan Percentage: {good_loans['percentage']:.2f}%")
```

