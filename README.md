# PRIMETRADE-AI-ASSESMENT
**Technical Project Summary: Behavioral Analysis of 211k+ Trades**

**The Objective**
The goal of this project was to analyze how market sentiment (Fear & Greed) influences trader behavior on the Hyperliquid platform. By merging a high-volume trade dataset with sentiment indices, I aimed to identify profitable segments and propose actionable platform features.

**1. Data Engineering & Integrity**
Working with 211,218 trade records, the first hurdle was data alignment.

Epoch Correction: I identified and resolved a common Unix Epoch error where timestamps were rendering as 1970.

Timezone Standardizing: I parsed complex IST date strings to ensure that every trade was perfectly mapped to the correct daily sentiment classification.

Feature Engineering: I calculated cumulative PnL per account and standardized position sizes to enable fair comparison across different trader types.

**2. Key Insights & Behavioral Trends**
My analysis revealed that sentiment is a massive driver of risk appetite:

The "Fear" Advantage: Contrary to expectations, the most profitable environment for our top traders was during Fear cycles, generating a total PnL of $3.35M.

The FOMO Effect: During Extreme Greed, trade frequency spiked to nearly 40,000 trades, but average position sizes dropped to their lowest point ($3,112), suggesting retail "chasing" behavior.

Directional Bias: Sellers tended to be more active during extreme sentiment shifts, while buyers remained relatively consistent across neutral phases.

**3. Machine Learning: Behavioral Archetypes**
I moved beyond simple grouping by implementing a K-Means Clustering model to define three distinct trader "Archetypes":

The Power Winners (Cluster 1): High-frequency, high-PnL accounts that drive platform volume.

The Tactical Scalpers (Cluster 2): Moderate frequency with consistent profitability.

The Explorers (Cluster 0): Low-frequency accounts with smaller, cautious positions.

**4. Actionable Strategy**
Incentivize Conviction: Implement a 15% fee rebate for "Winner" accounts during Fear days to reward liquidity providers when the market is distressed.

Behavioral Safety Rails: Introduce a dynamic trade frequency cap for inconsistent traders during Extreme Greed to protect them from high-frequency FOMO-driven losses
