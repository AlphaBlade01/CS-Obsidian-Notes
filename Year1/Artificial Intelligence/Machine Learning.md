## Supervised Learning
	Learning with a teacher
Focuses on two types of problems:
- **Classification:** Predicting a discrete label or class
	Eg. whether email is spam or not spam
- **Regression:** Predicting continuous values
	Eg. stock prices
#### Terminology
- **Input:** Also called **attribute**, **feature** or **independent variable** 
- **Output:** Also called **target**, **response**, or **dependent variable**.
- **Function ($f$):**  Also called a **hypothesis** or **predictor**
#### Process
- **Model:** form of function we want to learn, characterised by free parameters
- **Cost function:** Measures misfit of any function from the model given a training set
- **Training algorithm:** Function that minimises the cost function

## Unsupervised Learning
	Learning on unlabelled data
- **Clustering:** Finding sub-groups/clusters among feature vectors with similar traits
- **Dimensionality reduction:** Find patterns within feature vectors to be able to represent it in a lower dimension
### Uses
- Compressed representation saves on storage & computation
- Can reduce noise / irrelevant attributes in high dimensional data
- Often used in exploratory data analysis
## Types of models
- **Parametric models:** Summarise data using a finite set of parameters, making assumption about data distribution
- **Non-parametric models:** Can have a free number of parameters and doesn't make assumptions on data distribution
