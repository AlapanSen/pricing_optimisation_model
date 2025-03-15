

# E-Commerce Product Price Analyzer and Predictor

## Overview

This tool helps e-commerce sellers determine optimal pricing strategies for their products by analyzing market data and predicting ideal price points. The system scrapes competitor pricing information, analyzes market positioning, and recommends strategic pricing based on manufacturing costs and product quality.

## Features

- **Market-based Price Analysis**: Scrapes real product data from Amazon to analyze market pricing
- **Machine Learning Prediction**: Uses XGBoost models to predict optimal pricing based on market data
- **Category-specific Models**: Develops pricing models tailored to specific product categories
- **Multi-metric Pricing**: Predicts discounted price, MRP, and optimal discount percentage
- **Margin Optimization**: Ensures recommended prices maintain healthy profit margins
- **Visual Analytics**: Generates comprehensive visualizations of pricing recommendations
- **Price Positioning**: Shows where your product sits relative to market competitors
- **Data Enrichment**: Continuously improves with each analysis by expanding training dataset

## Requirements

- Python 3.6+
- Required packages:
  - requests
  - pandas
  - numpy
  - beautifulsoup4
  - matplotlib
  - seaborn
  - xgboost
  - scikit-learn
  - joblib

## Installation

1. Clone this repository or download the script
2. Install the required packages:
   ```
   pip install -r requirements.txt
   ```

## Usage

Run the script using Python:
```
python ecommerce_price_analyzer.py
```

Follow the interactive prompts:
1. Enter your product name
2. Select a product category from the list
3. Enter your manufacturing cost
4. Choose your product's quality tier (Premium/Mid-range/Budget)

The system will:
1. Search for similar products online
2. Extract pricing data from competitors
3. Train machine learning models (or use existing ones)
4. Generate pricing recommendations
5. Create visual reports of the recommendations
6. Save results to CSV files and image files

## How It Works

1. **Data Collection**: The tool scrapes Amazon search results for similar products in your category.
2. **Feature Engineering**: Creates advanced features including price-to-cost ratios, brand tier analysis, and market positioning.
3. **Model Training**: Trains XGBoost regression models for predicting discounted price, discount percentage, and MRP.
4. **Price Prediction**: Uses trained models to predict optimal pricing for your specific product.
5. **Visualization**: Generates comprehensive charts showing price breakdowns, market positioning, and comparative analysis.

## Output Files

The tool generates several output files:
- `pricing_recommendation_[product_name].csv`: CSV file with the pricing recommendation details
- `result_visualizations/`: Directory containing the following visualization files:
  - `price_breakdown_[product_name].png`: Visualization of cost vs. profit components
  - `price_positioning_[product_name].png`: Market positioning chart
  - `price_to_cost_comparison_[product_name].png`: Comparison of price-to-cost ratios
  - `pricing_dashboard_[product_name].png`: Comprehensive pricing dashboard with all metrics

## Advanced Features

### Category-specific Adjustments
The system includes predefined adjustments for different product categories, accounting for varying profit margins and manufacturing complexities across industries.

### Brand Tier Analysis
Products are classified into premium, mid-range, and budget tiers, with pricing recommendations adjusted accordingly.

### Seasonality Effects
The tool considers seasonal relevance when making pricing recommendations for certain categories.

### Fallback Mechanisms
If web scraping fails or data is insufficient, the system automatically falls back to simplified pricing algorithms based on industry standards.

## Limitations

- Requires internet access for data collection
- Performance depends on the quantity and quality of scraped data
- May be blocked by websites if used too frequently (uses rotating user agents and proxies to mitigate this)
- Some categories may have limited data, resulting in less accurate predictions

## Future Improvements

- Add support for more e-commerce platforms beyond Amazon
- Implement time-series analysis for seasonal pricing optimization
- Add competitor pricing alerts
- Develop a web interface for easier usage
- Implement product bundling recommendations
- Add inventory turnover optimization

