# Cryptoasset Trading Dataset

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

The **Target** column represents the 15-minute residualized returns for each row. Residualized returns are calculated from log returns (𝑅𝑎) over 15 minutes using the formula:

$\{R}^a(t) = \log\left(\frac{P^a(t+16)}{P^a(t+1)}\right)$

Additionally, a linear residualization is applied to remove the market signal from individual asset returns when creating the target. The formula for the target is:

$M(t) = \frac{\sum_{a} w_a R_a(t)}{\sum_{a} w_a}$  

$\beta_a = \frac{\langle M \cdot R_a \rangle}{\langle M^2 \rangle}$

$\Target^𝑎(𝑡)=𝑅^𝑎(𝑡)−𝛽^𝑎𝑀(𝑡)\$

Where $\(𝑀(𝑡)\)$ is the weighted average market returns, and $\(\beta_a\)$ is the asset-specific weight.

## Evaluation Metrics

This dataset is part of a forecasting competition that aims to predict returns for individual assets. The predictions will be evaluated on a weighted version of the Pearson correlation coefficient. The weights for the evaluation are given by the `Weight` column in the Asset Details file.

In this simplified tutorial, we will use correlation (without weights) for evaluation and consider only two assets, BTC and ETH.

Make sure to refer to the competition guidelines for the complete evaluation details.

## Getting Started

1. Clone this repository.
2. Explore the dataset (`train.csv`) and understand the features and target.
3. Refer to the associated notebook for details on the target calculation and any specific instructions on prediction and evaluation processes.

Feel free to analyze the data, build models, and participate in the competition!

Happy coding!
