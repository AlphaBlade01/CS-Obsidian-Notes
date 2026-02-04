**Regression:** Learning a function which captures the trend between input & output
	output being continuous

### Univariate linear regression
	One input attribute to regression function

$$y = f(x; w_0, w_1) = w_1x + w_0$$
$w_0, w_1$ = free parameters that determine the "best" line
$x$ = input / independent variable
$y$ = output / dependent variable

## Loss function
	Cost function / Error function
Figures out how good/bad the line of best fit is.
	Loss is the mismatch (distance) between model's output $f(x)$ and actual target $y$
### Types
**Absolute value loss:** $L1 = |f(x) - y|$
**Mean squared error loss:** $L2 = (f(x) - y)^2$
**0/1 loss:** $L_{0/1} = 0$ if $f(x) = y$, else $1$ 
