# Bitcoin-Sentiment-Trader-Performance-Analysis
AI Intern Assignment

## What is this project about?
 
I was given two datasets as part of my internship assignment:
 
1. **Bitcoin Fear & Greed Index** — daily sentiment score (0–100) with labels like *Extreme Fear*, *Fear*, *Neutral*, *Greed*, and *Extreme Greed*
2. **Historical Trader Data from Hyperliquid** — real trade records with PnL, leverage, side (long/short), account info, and more
 
The goal was simple but interesting: *does market sentiment actually affect how well traders perform?* I merged both datasets on date and dug into the numbers to find out.
 
---
 
## Project Structure
 
```
📁 bitcoin-sentiment-analysis/
│
├──  bitcoin_sentiment_analysis.ipynb   
├──  fear_greed_index.csv               ← Fear & Greed dataset
├──  historical_trader_data.csv         ← Hyperliquid trader dataset
├──  merged_trader_sentiment.csv        ← output: both datasets merged
└──  README.md                          ← you're reading this
```
 
---
 
## How to Run It
 
**Option 1 — Google Colab (easiest)**
 
1. Click the badge below or go to [colab.research.google.com](https://colab.research.google.com)
2. Upload the `.ipynb` file → File → Upload Notebook
3. Upload both CSVs to your Google Drive
4. Update the file paths in Step 2 and run all cells top to bottom
 
[![Open In Colab](https://colab.research.google.com/assets/colab-badge.svg)](https://colab.research.google.com/)
 
**Option 2 — Run locally**
 
```bash
git clone https://github.com/AAdi-112/Bitcoin-Sentiment-Trader-Performance-Analysis.git
cd bitcoin-sentiment-analysis
 
pip install pandas numpy matplotlib seaborn scipy
 
jupyter notebook bitcoin_sentiment_analysis.ipynb
```
 
---
 
## What I Did — Step by Step
 
| Step | Description |
|------|-------------|
| 1 | Imported all required libraries |
| 2 | Loaded both datasets |
| 3 | Cleaned the data — fixed date formats, standardized column names, removed nulls & duplicates |
| 4 | EDA on both datasets separately — distributions, win rates, top traders |
| 5 | Merged the two datasets on the `date` column |
| 6 | Analyzed mean PnL and win rate for each sentiment bucket |
| 7 | Deeper patterns — long vs short splits, correlation, top trader behavior, monthly heatmap |
| 8 | ANOVA test to check if PnL differences across sentiments are statistically real |
| 9 | Summarized key insights and strategy recommendations |
 
---
 
## Key Findings
 
> These are based on the actual data — numbers will reflect what the dataset shows.
 
- Traders performed differently depending on the market sentiment of that day
- There's a measurable correlation between the Fear & Greed index value and average daily PnL
- Long vs Short performance wasn't consistent across all sentiment categories — some sentiments clearly favored one side
- Top traders showed distinct behaviour patterns depending on whether the market was fearful or greedy
- The ANOVA test confirmed whether or not these differences are statistically significant (not just noise)
 
---
 
## Visualizations Generated
 
The notebook produces **10+ charts** saved as PNG files:
 
- Sentiment distribution (pie + bar)
- Fear & Greed index over time
- PnL distribution histogram
- Top traders by total PnL
- Mean PnL and Win Rate by sentiment
- Box plot of PnL per sentiment
- Long vs Short mean PnL by sentiment
- Correlation scatter plot (FG value vs daily PnL)
- Top 5 traders' PnL breakdown by sentiment
- Monthly heatmap (sentiment × month)
- Average leverage by sentiment
 
---
 
## Libraries Used
 
- `pandas` — data loading, cleaning, merging
- `numpy` — numerical operations
- `matplotlib` — plotting
- `seaborn` — styled visualizations, heatmaps
- `scipy` — Pearson correlation, ANOVA test
 
---
 
## Dataset Sources
 
| Dataset | Source |
|--------|--------|
| Fear & Greed Index | [Google Drive Link](https://drive.google.com/file/d/1PgQC0tO8XN-wqkNyghWc_-mnrYv_nhSf/view?usp=sharing) |
| Hyperliquid Trader Data | [Google Drive Link](https://drive.google.com/file/d/1IAfLZwu6rJzyWKgBToqwSmmVYU6VbjVs/view?usp=sharing) |
