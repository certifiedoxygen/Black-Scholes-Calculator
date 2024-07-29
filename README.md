
# Black Scholes Option Premium Calculater with Visualisation

## Project Description
This project is a Black-Scholes Option Pricing Calculator that allows users to calculate the theoretical prices of European call and put options. It is a web-hosted interactive application built with Streamlit, featuring an interface for inputting parameters such as spot price, strike price, time to maturity, volatility, and risk-free rate. The app also visualizes option Greeks and provides sensitivity analysis for informed decision-making in options trading

**Link to Project**: https://black-scholes-calculator.streamlit.app/

## Black-Scholes Model

The **Black-Scholes model**, often referred to as the **Black-Scholes-Merton (BSM) model**, is a fundamental concept in modern finance. It provides a mathematical framework for estimating the theoretical value of options by accounting for various risk factors and the passage of time.

The Black-Scholes equation relies on five key variables:

- **Volatility of the Underlying Asset**: Measures the degree of variation in the asset's price over time.
- **Price of the Underlying Asset**: The current market price of the asset for which the option is written.
- **Strike Price of the Option**: The predetermined price at which the option holder can buy (call) or sell (put) the underlying asset.
- **Time Until Expiration**: The remaining time until the option contract expires, typically expressed in years.
- **Risk-Free Interest Rate**: The theoretical rate of return on an investment with zero risk, often approximated by government bond yields.

This model is widely used in financial markets to price options and assess risk, making it an essential tool for traders and investors.

## Model Assumptions

The Black-Scholes model operates under several assumptions:

- No dividends are paid out during the life of the option.
- Markets exhibit randomness (market movements cannot be precisely predicted).
- There are no transaction costs associated with buying the option.
- The risk-free rate and volatility of the underlying asset remain known and constant throughout the life of the option.
- Returns on the underlying asset are log-normally distributed.
- The option is European, meaning it can only be exercised at expiration.

## Formulas
The prices of call and put options are calculated using the following formulas:

**Call Option**
```math
C = S_0 \cdot N(d_1) - K \cdot e^{-rT} \cdot N(d_2)
```
**Put Option**
```math
P = K \cdot e^{-rT} \cdot N(-d_2) - S_0 \cdot N(-d_1)

```
**d1 and d2**
```math
d_1 = \frac{\ln\left(\frac{S_0}{K}\right) + \left(r + \frac{\sigma^2}{2}\right)T}{\sigma \sqrt{T}}
```
```math
d_2 = d_1 - \sigma \sqrt{T}
```

## Option Greeks
The Greeks measure the sensitivity of the option's price to changes in underlying parameters while holding other parameters constant. They are the partial derivatives of the option price with respect to the parameters.

#### The Greeks Include:
- **Delta (Δ)**: Sensitivity to changes in the price of the underlying asset.
- **Gamma (Γ)**: Sensitivity to changes in Delta.
- **Theta (Θ)**: Sensitivity to the passage of time.
- **Vega (𝜈)**: Sensitivity to changes in volatility.
- **Rho (𝜌)**: Sensitivity to changes in the risk-free interest rate.

#### Greek Formulas:
```math
Δ_{call} = N(d_1) 
```
```math
Δ_{put} = N(d_1) - 1 
```
```math
Γ = \frac{N'(d_1)}{S_0 \cdot \sigma \sqrt{T}} 
```
```math
Θ_{call} = -\frac{S_0 \cdot N'(d_1) \cdot \sigma}{2\sqrt{T}} - rK e^{-rT} N(d_2) 
```
```math
Θ_{put} = -\frac{S_0 \cdot N'(d_1) \cdot \sigma}{2\sqrt{T}} + rK e^{-rT} N(-d_2) 
```
```math
ν = S_0 \cdot N'(d_1) \cdot \sqrt{T} 
```
```math
ρ_{call} = K \cdot T e^{-rT} N(d_2) 
```
```math
ρ_{put} = -K \cdot T e^{-rT} N(-d_2) 
```

### Connect with Me

[![LinkedIn](https://img.shields.io/badge/LinkedIn-Connect%20with%20Me-blue?style=for-the-badge&logo=linkedin)](https://www.linkedin.com/in/yashkhaitan/)
