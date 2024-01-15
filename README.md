# Crypto asset Trading Dataset

This repository contains a dataset (`train.csv`) related to cryptoasset trading. The dataset consists of the following columns:

- **timestamp**: A timestamp for the minute covered by the row.
- **Asset_ID**: An ID code for the cryptoasset.
- **Count**: The number of trades that took place in that minute.
- **Open**: The USD price at the beginning of the minute.
- **High**: The highest USD price during the minute.
- **Low**: The lowest USD price during the minute.
- **Close**: The USD price at the end of the minute.
- **Volume**: The number of cryptoasset units traded during the minute.
- **VWAP**: The volume-weighted average price for the minute.
- **Target**: 15-minute residualized returns.

## Target Explanation

The **Target** column represents the 15-minute residualized returns for each row. Residualized returns are a measure used in financial analysis to account for market trends and variations. More details about how the target is calculated can be found in the 'Prediction and Evaluation' section of the notebook associated with this dataset.

## Data Dictionary

- **timestamp**: YYYY-MM-DD HH:MM format.
- **Asset_ID**: Unique identifier for each cryptoasset.
- **Count**: Integer representing the number of trades.
- **Open/High/Low/Close**: USD prices for the beginning, highest, lowest, and end of the minute.
- **Volume**: Number of cryptoasset units traded.
- **VWAP**: Volume-weighted average price for the minute.
- **Target**: 15-minute residualized returns.

## Prediction and Evaluation

Refer to the associated notebook in this repository for details on how the target variable is calculated and for any specific instructions on prediction and evaluation processes.

Feel free to explore and analyze the data for insights into cryptoasset trading patterns and behaviors.

Happy coding!
