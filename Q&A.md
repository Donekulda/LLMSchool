# Question and Answers for LLM and people about learning

## HMM (Hidden Markov Model) - finance mathematical analysis
**What does customizable lookback period in HMM model, from feature engineering, mean?**

**What do Moving average crossover signals in HMM model mean?**

**What is Look ahead Bias**
When predicting future prices but wrongly

Common Look-ahead Bias Mistakes:
1.Using end-of-day prices to make intraday decisions
2.Training models on the entire dataset including future data
3.Not accounting for delayed market data
4.Using adjusted prices without considering when adjustments were known

To Prevent Look-ahead Bias:
1.Always use .shift() for indicators
2.Split data properly into training/testing
3.Only use information that was available at the time
4.Account for real-world delays in data