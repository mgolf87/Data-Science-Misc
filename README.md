# Data-Science-Misc
Collection of various Data Science topics and techniques.
<br />

## Quantile Regression
### QuantileRegression.ipynb
#### How can DoorDash give us an estimated delivery range?
Quantile Regression is used to generate bounds (i.e. DoorDash: "Your order will arive in 25 to 35 minutes")
<br />
<br />
Regression Loss Function: <br />
L = (y - Xθ)^2
<br />
<br />
Quantile Loss Function: <br />
L = τ(y - Xθ) if y - Xθ >= 0 : predicted value low, used for low quantiles, penalizes high
<br />
L = (τ - 1)(y - Xθ) if y - Xθ < 0  : predicted value high, used for high quantiles, penalizes low
<br />
<br />
Penalize the Loss when: 
<br />
The percentile τ is low, but the prediction is Xθ is high  
The percentile τ is high, but the prediction is Xθ is low
<br />
<br />
For this example we will be using τ = [0.2, 0.5, 0.9] however we will only consider the 20th and 90th quantile as we want our time prediction to have a minimum at 20% and a maximum at 90%. Thus, ensuring that we don't get the hopes up of the customers too much like a 10% minimum time might. As well, we don't want our maximum to be higher than 90% as this may skew our range to appear greater than what is likely.
<br />
<br />

## Topic 2
### Files
Description

<br />
<br />

## Topic 3
### Files
Description

<br />
<br />

## Topic 4
### Files
Description

<br />
<br />

## Topic 5
### Files
Description

<br />
<br />

## Topic 6
### Files
Description
