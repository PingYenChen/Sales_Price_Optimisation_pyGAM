# Sales_Price_Optimisation_pyGAM
# Price Optimization for Phone Cases using GAMs 💰

A Jupyter notebook for **price optimization** using Generalized Additive Models (GAMs) on mock sales data for Phone cases.  
It models price-quantity relationships, estimates revenue curves with uncertainty (expectiles), and identifies optimal prices by product and promotional events — blending statistics, machine learning, and visualization for revenue maximization.

Created to demonstrate non-linear demand modeling, applicable to e-commerce pricing strategies.

## Technologies Used

- **Pandas & NumPy**: Data manipulation and numerical operations.
- **Statsmodels**: OLS regression for baseline modeling.
- **pyGAM**: Generalized Additive Models with expectiles for quantile regression.
- **Scikit-learn**: Label encoding for categoricals.
- **Plotly Express**: Interactive scatter plots and visualizations.
- **Plotnine & Pytimetk**: ggplot-style plots for revenue optimization curves.
- Datasets: Mock CSV with product, price, quantity_sold, event.

## Key Features

- **Demand Modeling**: GAMs to capture non-linear price elasticity by product tier (Standard vs Premium).
- **Quantile Regression**: Expectiles (0.025, 0.5, 0.975) for median revenue and confidence intervals.
- **Event Segmentation**: Separate analysis for "No Promo" and special events (Black Friday, Christmas, etc.).
- **Revenue Optimization**: Identify max revenue prices with markers on curves.
- **Faceted Visualizations**: Interactive and static plots by product and event.
- **Data Prep**: Filtering, encoding, and revenue calculation (price × quantity).

## Process & Workflow

The notebook follows a structured analytics pipeline:

1. **Import & Setup**: Load libraries and mock sales data (CSV with 800 rows).
2. **Exploratory Analysis**: Visualize price vs quantity scatters with trendlines (Plotly).
3. **Baseline Modeling**: OLS regression with dummies for products/events to estimate lifts.
4. **GAM Fitting**: Loop over products/events, fit ExpectileGAMs for revenue quantiles.
5. **Predictions & Optimization**: Generate revenue curves, find max median revenue points.
6. **Visualization**: Faceted ggplot-style plots with ribbons (CI), lines (median), and points (optimal/max CI).
7. **Insights**: Optimal prices by scenario, e.g., lower during promos for volume boost.

Results show steeper elasticity for standard cases and event-driven pricing shifts.

## Potential Applications & Further Utilization

This GAM-based optimization extends to various pricing domains:

- **E-commerce & Retail**: Dynamic pricing for products, A/B test analysis, promo impact modeling.
- **Marketing & Demand Forecasting**: Elasticity estimation, revenue simulation under scenarios.
- **Finance/Operations**: Inventory pricing, yield management (e.g., airlines/hotels), cost-plus adjustments.
- **Extensions**: Integrate real-time data (e.g., via APIs), add multi-product interactions, use Bayesian GAMs for priors, or deploy as dashboard (Streamlit).

Fork and customize with your sales data – great for pricing analytics portfolios! 🌟
