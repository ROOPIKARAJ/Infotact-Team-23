# Hotel Booking Demand Analysis - Infotact Team 23

## Project Overview

This comprehensive data science project, developed by **Infotact Team 23**, focuses on analyzing hotel booking demand patterns to predict cancellations and optimize revenue management strategies. The project follows a systematic approach from data preprocessing to predictive modeling and visualization, spanning 4 weeks of intensive development.

## Project Structure

The project is organized as follows:

- `WEEK1/`: Data Acquisition, Cleaning & Feature Engineering
  - `data_preprocessing_and_engineering.ipynb`: Main Jupyter Notebook covering the complete data pipeline
  - `Data/hotel_bookings_resort.csv`: The primary dataset (40,060 initial records)
  - `cleaned_data.csv`: Output of the cleaning and preprocessing steps (33,968 records, 38 features)
- `WEEK2/`: Exploratory Data Analysis (EDA) and Statistical Testing
  - `eda_and_statistical_testing.ipynb`: Comprehensive analysis with correlations and variable relationships
- `WEEK3/`: Predictive Modeling
  - `predictive_modeling.ipynb`: Machine learning pipeline with Logistic Regression and Decision Tree models
- `WEEK4/`: Dashboard Development
  - `WEEK4 Hotel Booking Dashboard.pbix`: Interactive Power BI dashboard for business intelligence

## Week-by-Week Analysis

### Week 1: Data Acquisition, Cleaning & Feature Engineering

**Key Accomplishments:**

- **Dataset Loading**: Successfully loaded hotel bookings dataset with 40,060 initial records
- **Data Cleaning Pipeline**:
  - Handled NULL values by standardizing to `NaN` format
  - Removed duplicate records (reduced from 40,060 to 33,968 entries - 15.3% reduction)
  - Standardized column names to lowercase with underscores
  - Fixed data types and converted dates to proper datetime format
- **Feature Engineering**:
  - Created `totalstay` feature combining weekend and week nights
  - Extracted temporal features from reservation dates (year, month, day, weekday)
  - Calculated `pricepernight` for better rate analysis
  - Applied log transformation to ADR for variance stabilization

**Deliverables:**

- Cleaned dataset (`cleaned_data.csv`) with 33,968 records and 38 features
- Comprehensive data preprocessing pipeline
- Enhanced feature set for improved analysis

### Week 2: Exploratory Data Analysis & Statistical Testing

**Key Analyses Performed:**

- **Data Distribution Analysis**:
  - Visualized distributions of lead time, ADR, and total stay
  - Identified skewness patterns and outliers
- **Correlation Matrix Analysis**:
  - Generated comprehensive heatmap of feature correlations
  - Identified key drivers of booking cancellations
- **ADR vs Cancellation Analysis**:
  - Univariate analysis using boxplots
  - Bivariate analysis with quantile-based binning
  - Discovered price sensitivity patterns

**Key Findings:**

- **Lead Time**: Positive correlation with cancellations (bookings made far in advance more likely to cancel)
- **Special Requests**: Negative correlation (customers with more requests less likely to cancel)
- **ADR Impact**: Higher rates show increased cancellation probability
- **Car Parking**: Negative correlation with cancellations

### Week 3: Predictive Modeling

**Machine Learning Pipeline:**

- **Data Preprocessing**:
  - Label encoding for categorical variables
  - Feature scaling using StandardScaler
  - Train-test split (80-20) with stratification
- **Model Development**:
  - **Logistic Regression**: Baseline model with 94.74% accuracy
  - **Decision Tree**: Alternative model with 89.81% accuracy
- **Performance Evaluation**:
  - Comprehensive metrics: Accuracy, Precision, Recall, F1-Score, ROC-AUC
  - Confusion matrices for both models
  - ROC curve comparison

**Model Performance:**
| Model | Accuracy | Precision | Recall | F1-Score | ROC-AUC |
|-------|----------|-----------|--------|----------|---------|
| Logistic Regression | 94.74% | 99.05% | 78.37% | 87.50% | 97.98% |
| Decision Tree | 89.81% | 81.60% | 73.10% | 77.12% | 93.83% |

**Key Predictive Features:**

1. Country (12.64% importance)
2. Required Car Parking Spaces (11.75%)
3. Arrival Week Number (11.62%)
4. Lead Time (10.50%)
5. Reservation Month (10.14%)

### Week 4: Dashboard Development

**Power BI Dashboard:**

- **Interactive Visualization**: Created comprehensive dashboard (`WEEK4 Hotel Booking Dashboard.pbix`)
- **Key Metrics Display**:
  - Cancellation rates by various dimensions
  - Revenue trends and patterns
  - Booking patterns and seasonality
  - Customer segmentation insights
- **Business Intelligence Features**:
  - Interactive filters for date ranges and customer segments
  - Real-time KPI monitoring
  - Predictive model integration insights

## Technical Stack & Tools

### Core Technologies:

- **Python**: Primary programming language for data science
- **Pandas**: Data manipulation and analysis
- **NumPy**: Numerical operations and array handling
- **Scikit-learn**: Machine learning algorithms and preprocessing
- **Matplotlib & Seaborn**: Data visualization and statistical plotting
- **Jupyter Notebook**: Interactive development environment
- **Power BI**: Dashboard development and business intelligence

### Data Processing:

- **Data Size**: 33,968 records, 38 features (after preprocessing)
- **Processing Pipeline**: Automated cleaning and feature engineering
- **Model Training**: 80-20 train-test split with stratification

## Business Impact & Insights

### Revenue Management Benefits:

1. **Cancellation Prediction**: 94.74% accuracy enables proactive overbooking strategies
2. **Price Optimization**: ADR insights help optimize pricing strategies
3. **Customer Segmentation**: Identify high-value, low-cancellation-risk customers
4. **Resource Planning**: Better forecasting for staffing and inventory

### Key Business Insights:

- **Recall** is critical for revenue management (missed cancellations cost revenue)
- **Precision** important for avoiding false positives
- Logistic Regression offers more stable predictions
- Decision Tree provides better interpretability

### Implementation Recommendations:

1. **Model Deployment**: Integrate predictive models into booking system
2. **Real-time Alerts**: Set up automated alerts for high-risk bookings
3. **Dashboard Monitoring**: Regular review of Power BI metrics
4. **Model Maintenance**: Quarterly retraining with new data
5. **Business Rules**: Develop automated response strategies for predicted cancellations

## Project Success Metrics

### Data Quality Achievements:

- **Data Reduction**: 15.3% reduction through duplicate removal
- **Missing Value Resolution**: 100% completion through imputation
- **Feature Enhancement**: 7 new engineered features

### Model Performance:

- **Prediction Accuracy**: 94.74% (Logistic Regression)
- **Business Value**: High recall (78.37%) for revenue protection
- **Interpretability**: Clear feature importance for business decisions

### Operational Efficiency:

- **Automated Pipeline**: End-to-end data processing automation
- **Real-time Insights**: Dashboard for continuous monitoring
- **Scalable Framework**: Ready for production deployment

## Installation & Setup

### Prerequisites:

- Python 3.7 or higher
- Jupyter Notebook/JupyterLab
- Power BI Desktop (for dashboard)

### Dependencies:

```bash
pip install pandas numpy seaborn matplotlib scikit-learn
```

### How to Run:

1. **Clone the repository**:

   ```bash
   git clone <repository-url>
   cd Infotact-Team-23
   ```

2. **Install dependencies**:

   ```bash
   pip install pandas numpy seaborn matplotlib scikit-learn
   ```

3. **Run the analysis**:
   - Start with `WEEK1/data_preprocessing_and_engineering.ipynb`
   - Follow with `WEEK2/eda_and_statistical_testing.ipynb`
   - Proceed to `WEEK3/predictive_modeling.ipynb`
   - Open `WEEK4 Hotel Booking Dashboard.pbix` in Power BI

4. **Data Flow**:
   - Original dataset: `WEEK1/Data/hotel_bookings_resort.csv`
   - Cleaned data: `WEEK1/cleaned_data.csv`
   - Models and visualizations: Respective week folders

## Future Enhancements

### Technical Improvements:

1. **Advanced Models**: Random Forest, Gradient Boosting for better performance
2. **Deep Learning**: Neural networks for complex pattern recognition
3. **Time Series Analysis**: Seasonal trend forecasting
4. **A/B Testing**: Model performance validation

### Business Expansion:

1. **Multi-property Analysis**: Extend to multiple hotel properties
2. **Competitor Analysis**: Market positioning insights
3. **Customer Lifetime Value**: Long-term customer profitability analysis
4. **Dynamic Pricing**: Real-time price optimization algorithms
