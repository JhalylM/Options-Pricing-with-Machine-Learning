## Overview
This project explores the use of machine learning techniques, specifically Random Forest regressors, to predict options prices. The aim was to provide a data-driven alternative to the Black-Scholes model and assess their relative performance. Both call and put options were analyzed.

## Key Features
- Compared **Random Forest Regressors** for calls and puts against the traditional **Black-Scholes formula**.
- Evaluated models on multiple metrics: **MSE**, **RMSE**, **MAPE**, and **PEX%**.
- Analyzed feature importance for the Random Forest models.

## Results
The Random Forest models significantly outperformed the Black-Scholes formula on all metrics:

| Metric          | Calls (RF)  | Calls (BS)  | Puts (RF)   | Puts (BS)   |
|-----------------|-------------|-------------|-------------|-------------|
| **MSE**        | 7.52        | 1145.28     | 2.42        | 33545.37    |
| **RMSE**       | 2.74        | 33.84       | 1.56        | 183.15      |
| **MAPE**       | 16.53%      | 545.10%     | 7.86%       | 14651.23%   |
| **PEX 10%**    | 11.11%      | 0.00%       | 88.89%      | 0.00%       |

### Feature Importance (Random Forest Models)
- **Calls**: logMoneyness = 55%, impliedVolatility = 45%, daysToExpiration = 0%
- **Puts**: logMoneyness = 85%, impliedVolatility = 15%, daysToExpiration = 0%

## Conclusion
Random Forest regressors provide a superior alternative to the Black-Scholes model for options pricing. Their ability to account for nonlinear relationships in the data led to significantly improved performance metrics.

### Future Work
- Include additional features like interest rates or dividend yields.
- Test performance under different market conditions or for exotic options.
- Explore advanced models like Gradient Boosting or Neural Networks.

---
