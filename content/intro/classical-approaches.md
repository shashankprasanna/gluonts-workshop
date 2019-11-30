---
title: "Classical Time Series Modeling Approaches"
weight: 4
katex: true
markup: "mmark"
---

In classical Approaches the function $$f(\cdot)$$ is usually a linear model. i.e. $$𝑦_{𝑡+1}$$ is a linear combination of past values $$𝑦_{𝑡}, y_{t-1}, y_{t-2}, y_{t-3} ... $$ and so on.

One of the most common and widely used model is called ARIMA. Let's break it down and see how ARIMA works.

#### An AR (Autoregressive) process

$$ 𝑦_𝑡=𝑐 +𝜙_1 𝑦_{(𝑡−1)}+𝜙_2 𝑦_{(𝑡−2)}  +𝜀_𝑡 $$

$$ ⇒ 𝑦_𝑡−𝜙_1 𝑦_(𝑡−1)−𝜙_2 𝑦_(𝑡−2)=𝑐+𝜀_𝑡 $$

$$⇒ 𝑦_𝑡−𝜙_1𝐿𝑦_𝑡−…−𝜙_𝑝 𝐿^𝑝 𝑦_𝑡=𝑐+𝜀_𝑡 $$

$$ ⇒(1−𝜙_1 𝐿−…−𝜙_𝑝 𝐿^𝑝 )   𝑦_𝑡=𝑐+𝜀_𝑡 $$

$$ ⇒𝜙(𝐿)𝑦_𝑡=𝑐+𝜀_𝑡$$

Where $$L$$ is the lag operator and $$\phi(L)$$ is a polynomial in $$L$$

$$𝐿^𝑖 𝑦_𝑡=𝑦_{(𝑡−𝑖)}$$

#### Autoregressive (AR) and Integrated (I)

Let us revisit our AR equation:
$$𝜙(𝐿) 𝑦_𝑡=𝑐+𝜀_𝑡$$

If $$𝜙(𝐿)$$ could be factored as follows:
$$(1−𝐿) 𝜙^′(𝐿) 𝑦_𝑡=𝑐+𝜀_𝑡$$

Recall that: $$𝐿𝑦_𝑡=𝑦_(𝑡−1) $$

$$ ⇒ (1−𝐿)$$

$$ ⇒ 𝑦_𝑡=𝑦_𝑡−𝑦_(𝑡−1)$$

$$ ⇒ Δ𝑦_𝑡$$

$$⇒ 𝜙^′ (𝐿)Δ𝑦_𝑡=𝑐+𝜀_𝑡$$

The series can be made stationary by differencing the series show by $$Δ𝑦_𝑡$$

#### Autoregressive (AR) and Integrated (I) and Moving average (MA) - **ARIMA**

$$𝜙^′(𝐿)Δ𝑦_𝑡=𝑐+𝜀_𝑡$$

Moving Average is used to model the error term: $$𝜺_𝒕$$

$$𝜙^′ (𝐿)Δ𝑦_𝑡=𝑐+𝜀_𝑡+𝜃_1 𝜀_(𝑡−1)+…+𝜃_𝑞 𝜀_(𝑡−𝑞)$$

Moving Average model captures serial autocorrelation in a time series $$𝑦_𝑡$$ by expressing it as a function of past errors.

$$𝜙(𝐿) Δ^𝐷 𝑦_𝑡=𝑐+𝜃(𝐿)𝜀_𝑡$$
