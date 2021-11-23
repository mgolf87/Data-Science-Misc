# Data-Science-Misc

<br />

## Quantile Regression
### QuantileRegression.ipynb
#### How can DoorDash give us an estimated delivery range?
Quantile Regression is used to generate bounds (i.e. DoorDash: "Your order will arive in 25 to 35 minutes")
Regression Loss Function: L = (y - Xθ)^2
Quantile Loss Function: L = τ(y - Xθ)        if y - Xθ >= 0 : predicted value low, used for low quantiles, penalizes high
                            (τ - 1)(y - Xθ)  if y - Xθ < 0  : predicted value high, used for high quantiles, penalizes low
Penalize the Loss when: 
    The percentile τ is low, but the prediction is Xθ is high
    The percentile τ is high, but the prediction is Xθ is low
For this example we will be using τ = [0.2, 0.5, 0.9] however we will only consider the 20th and 90th quantile as we want our time prediction to have a minimum at 20% and a maximum at 90% ensuring that we don't get the hopes up of the customers too much like a 10% minimum might. As well, we don't want our maximum to be higher than 90% as this may skew our range to appear greater than what is likely.
<br />

## Topic 2
### Files
Description

<br />

## Topic 3
### Files
Description

<br />

## Topic 4
### Files
Description

<br />

## Topic 5
### Files
Description

<br />

## Topic 6
### Files
Description

<br />
