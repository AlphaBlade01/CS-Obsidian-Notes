- Algorithm searches for the best rules to split samples that are dissimilar
- **Gini Index:** Used in Classification And Regression Trees
	$I_{G}(p)=1-\sum^J_{i=1}p_{i}^2$
	where $p_i$ is the fraction of items labelled with class $i$ in the dataset
- **Information Gain:** measures the reduction in entropy after splitting dataset based on feature
	$IG(Y,X) = H(Y) - H(Y|X)$
### Limitations
- **Unstable:** Small change in data can lead to a large change in structure of obtained tree
- **Greedy Search:** Tree construction has no backtracking as searching through all possible trees is infeasible
- **Relatively inaccurate:** Many other models often perform better
### Solutions
- **Random Forest:** Combines multiple decision trees to reduce overfitting
- **Gradient Boosting:** Builds ensemble of trees sequentially where each tree corrects errors made by previous trees
## Mutual Information Feature Selection
1. Initialize: $F \leftarrow \text{all features}$, $S \leftarrow \emptyset$
2. Select the feature $f_{\max}$ that maximizes mutual information:
   $$f_{\max} = \arg\max_{X_i \in F} I(Y; X_i)$$
3. Update: $F \leftarrow F \setminus \{f_{\max}\}$, $S \leftarrow S \cup \{f_{\max}\}$
4. **Repeat** until $|S| = K$ (desired number of features):
	1. Select feature $f_{\max}$ that maximizes:
	   $$f_{\max} = \arg\max_{X_i \in F} \left( I(Y; X_i) - \beta \sum_{X_s \in S} I(X_s; X_i) \right)$$
	2. Update: $F \leftarrow F \setminus \{f_{\max}\}$, $S \leftarrow S \cup \{f_{\max}\}$
5. **End Repeat**
