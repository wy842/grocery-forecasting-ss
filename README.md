Grocery Sales Forecasting – Corporación Favorita
Overview

Forecasting daily grocery sales for Guayaquil stores (Ecuador) for Q1 2014 using time series analysis and machine learning.

    Forecast horizon: Jan 1 – Mar 31, 2014 (90 days)

    Scope: 8 stores, 33 product families

    Best model: LightGBM

Dataset

    Total records: 17,039,400

    Date range: Jan 2013 – Aug 2017

    Stores: 8 (24, 26, 28, 29, 30, 32, 34, 51)

    Product families: 33

    Unique items: 4,005

Feature Engineering

29 features were created across key categories:

    Time features: day of week, month, quarter, week of year

    Holidays: national, regional indicators

    Payday effects: payday flags, distance to payday

    External factors: oil prices, transactions

    Promotions: onpromotion flag

    Store & product metadata

Models

Three models were developed and evaluated:

    Naive Seasonal Baseline

        MAE: 978.61

        MAPE: 16.41%

    Prophet

        MAE: 4,690.36

        MAPE: 99.08%

    LightGBM (Best)

        MAE: 658.62

        MAPE: 10.98%

LightGBM outperformed the baseline by ~32.7%.
Forecast Results

Forecasts generated for 3 store-family combinations:

    Store 51 – GROCERY I

        Avg daily: 9,081 units

        Q1 total: 817,311 units

    Store 24 – GROCERY I

        Avg daily: 5,592 units

        Q1 total: 503,290 units

    Store 34 – GROCERY I

        Avg daily: 6,296 units

        Q1 total: 566,619 units

Key Insights

    Promotions increase sales by ~73%

    Strong payday effect (15th & end of month spikes)

    National holidays significantly impact demand

    GROCERY I is the top-performing category

Deployment Recommendations

    Use LightGBM for production forecasting

    Retrain models monthly with new data

    Monitor performance (MAE, MAPE)

    Expand coverage to more stores and families

    Integrate forecasts into inventory systems

Next Steps

    Expand to additional store-family combinations

    Incorporate external signals (weather, events)

    Automate pipeline (ETL + training + inference)

Status

Project completed and ready for deployment 🚀
