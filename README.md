# PRIMETRADE-AI-ASSESMENT
**Technical Project Summary: Behavioral Analysis of 211k+ Trades**
**Project Overview**
This project analyzes the relationship between market sentiment (Fear & Greed Index) and trader performance on the Hyperliquid platform. Using a dataset of 211,218 trade records, I identified behavioral patterns among different trader segments and developed actionable strategies to improve platform retention and liquidity.

**Methodology**

To ensure data integrity, I followed a rigorous "Full-Stack" Data Analytics workflow:

*Data Engineering: Resolved a critical Unix Epoch error (timestamps defaulting to 1970) and standardized IST date strings for perfect alignment between trade logs and sentiment indices.

*Sentiment Mapping: Merged the datasets on a daily level to classify trades into five categories: Extreme Fear, Fear, Neutral, Greed, and Extreme Greed.

*Behavioral Segmentation: Segmented users into 29 Winners and 3 Inconsistent traders based on cumulative PnL and trade frequency.

*Machine Learning Bonus: Implemented K-Means Clustering to scientifically identify three distinct "Trader Archetypes" based on risk appetite and execution volume.

**Key Insights**

*The "Fear" Alpha: My analysis shows that Fear days yield the highest total PnL ($3.35M) and the highest average position sizes ($7,816).

*Euphoria & FOMO: During Extreme Greed, trade frequency spikes to nearly 40,000, but average position sizes drop to their lowest point ($3,112), indicating inefficient retail "chasing" behavior.

*Directional Bias: Visualizing BUY vs. SELL ratios confirmed that traders tend to have a higher short-bias during extreme sentiment shifts compared to neutral phases.

**Actionable Strategy Recommendations**

*The "Fear" Fee Incentive: Reward high-conviction traders with a 15% fee rebate during Fear cycles (Index < 30) to incentivize liquidity when the market is distressed.

*Behavioral Safety Rails: Implement a dynamic trade frequency cap for "Inconsistent" segment accounts during Extreme Greed to prevent capital erosion from high-frequency FOMO trading.
