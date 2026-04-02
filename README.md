💹 Deep-Volatility: Neural Network Optimized Derivatives Pricing

![alt text](https://img.shields.io/badge/Python-3.9+-blue.svg)

![alt text](https://img.shields.io/badge/TensorFlow-2.15+-orange.svg)

![alt text](https://img.shields.io/badge/Quant-Derivatives-gold.svg)

A high-performance Deep Learning Engine designed to price financial derivatives Black-Scholes-Merton (1973) formula. By training on live market data, this model captures the "Volatility Smile"—a real-world market phenomenon that classic analytical models fail to address.

🔬 The Financial Problem

The classic Black-Scholes model assumes that Volatility (
σ
σ
) is constant across all strike prices. In reality, the market prices "fear" and "hype" differently for every option. This leads to the Volatility Smile, where deep "out-of-the-money" options are consistently mispriced by traditional math.

🛠️ The Hybrid Pipeline

This project utilizes a Physics-Informed Neural Network (PINN) concept:

Data Harvesting: Multi-asset options chain ingestion (SPY, AAPL, TSLA, NVDA) using yfinance.

Feature Engineering:

- Moneyness (
S
/
K
S/K
): Normalizing asset prices for cross-ticker scalability.

-Time-to-Maturity (
T
T
): Annualized temporal decay.

- Risk-Free Rate (
r
r
): Real-time interest rate modeling.

Neural Architecture (Multilayer Perceptron):

ELU Activation: Optimized for non-linear "curvy" financial distributions.

Softplus Output: Enforcing the "Non-Negative Price" law of finance.

Volatility Surface Modeling: Instead of direct price regression, the model learns the Implied Volatility (
σ
σ
) surface to ensure pricing integrity.

📊 The "Volatility Smile" Showdown

The primary metric of success is the Residual Analysis between the Analytical Baseline (Math) and the Deep Learning Model (AI).

Red Dots (Black-Scholes): Exhibit a "U-shaped" error curve (The Smile), proving the math is rigid.

Green Dots (Deep-Volatility AI): Exhibit a flat, low-variance error distribution, proving the AI has successfully learned the market's hidden pricing logic.

<img width="855" height="547" alt="download" src="https://github.com/user-attachments/assets/9b7c50a9-acde-41f6-a14a-3f83671e74b8" />
