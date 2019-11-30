---
title: "Time Series Modeling"
katex: true
markup: "mmark"
weight: 2
---
![challenges](/images/introduction/autoregressive.png)

Autoregressive(AR) Process:
<br>
Let 𝑦(𝑡) be the temperature time series.
An AR process models the conditional mean of 𝑦(𝑡) as a function of past observations:

$$ 𝑦_𝑡  = 𝑓(𝑦_{(𝑡−1)},𝑦_{(𝑡−2)},…,𝑦_{(𝑡−𝑛)})$$

In other words, future value of a time series is some function of the past values of y.

The function $$f$$ can be a linear of non-linear function of past values.
