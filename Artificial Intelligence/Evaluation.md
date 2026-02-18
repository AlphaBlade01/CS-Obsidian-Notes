- Not to be confused with evaluating a predictor (model already chosen)
- **Training set:** annotated data used for training within a chosen model
- **Test set:** annotated data but used to evaluate trained predictor

## Holdout validation
1. Randomly choose 30% of data to form validation set, remaining forms training set
2. Train model on the training set
3. Estimate test performance on test set
4. Choose model with lowest validation error
5. Re-train chosen model on entire input set
6. Estimate future performance of the obtained predictor on a test set
#### Advantages & Disadvantages
	+ Computationally cheapest
	- Most unreliable if sample size not large enough
## k-Fold Cross-Validation
1. Split training set randomly into $k$ equal-sized disjoint sets
2. Use $k-1$ of the sets for training
3. Use the remaining one for validation
4. Permute the $k$ sets and repeat $k$ times
5. Average the performance on the validation sets
6. Choose the model with the smallest average error
7. Re-train chosen model on entire input set
8. Estimate future performance of obtained predictor on a test set
#### Advantages & Disadvantages
	+ Slightly more reliable than holdout
	- Wastes 1/k of annotated data
	- Computationally k times as expensive as holdout
## Leave-one-out
1. Leave out one example from annotated data to act as the validation set
2. Train model using all remaining data
3. For a dataset containing $N$ examples, repeat this $N$ times
4. Average results across all $N$ runs
#### Advantages & Disadvantages
	+ Doesn't waste data
	- Computationally most expensive