**Core Objective:** Evaluate classifier reliability and provide confidence guarantees on prediction ability beyond training data
**i.i.d. Assumption:** All samples $(x_{i},\ y_{i})$ are drawn independently and identically distributed

- **True error:** $c_{\mathcal{D}} \equiv Pr_{(x,y)~\mathcal{D}}(c(x)\neq y)$
- **Observed error:** $\hat{c}_{\mathcal{S}} = \frac{1}{n} \sum^n_{i=1} I[c(x_{i}) \neq y_{i}]$
	where $I(.)$ donates indicator function

