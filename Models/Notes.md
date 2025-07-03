#  Performance  GaussianHHMM

## n_components
**This tells how many different "states" or "regimes" the model should look for**
### Less States (2-3)
hmm = GaussianHMM(n_components=2)
#### Pros:
- Faster training and prediction
- More stable, less likely to overfit
- Clearer signals (just bull/bear)
#### Cons:
- Might miss subtle market patterns
- Too simplistic for complex markets

### More States (4-6)
hmm = GaussianHMM(n_components=5)
#### Pros:
- Can capture more complex market behaviors
- Better for sophisticated trading strategies
#### Cons:
- Needs more data to train effectively
- Risk of overfitting
- Harder to interpret

## covariance_type
**Determines how the model measures relationships between features**
### "full" covariance
hmm = GaussianHMM(covariance_type="full")
#### Pros:
- Captures all relationships between features
- Best for complex market interactions
#### Cons:
- Computationally expensive
- Needs more data
- Can overfit with too many features

### "diag" covariance
hmm = GaussianHMM(covariance_type="diag")
#### Pros:
- Faster computation
- More stable with less data
#### Cons:
- Misses cross-feature relationships
- Might be too simple for some markets

## n_iter
** Maximum number of times the model will try to improve its understanding **
### Lower iterations (500)
hmm = GaussianHMM(n_iter=500)
#### Pros:
- Faster training
- Good for quick testing
#### Cons:
- Might not find optimal solution
- Less accurate predictions

### Higher iterations (2000+)
hmm = GaussianHMM(n_iter=2000)
#### Pros:
- More likely to find optimal solution
- Better accuracy
#### Cons:
- Much slower training
- Diminishing returns after certain point