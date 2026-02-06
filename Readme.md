# Simulating Balatro Strategy Archetypes

This repository contains a Monte Carlo simulation study of strategic archetypes in a **Balatro-inspired poker roguelike game**. The project explores how different high-level strategies perform under uncertainty, using repeated simulation to evaluate win rates, progression depth, and economic outcomes.

The simulation is implemented in a Jupyter Notebook, and the full written analysis and results are documented in an accompanying PDF report.

---

## Project Overview

Balatro is a deck-building poker roguelike where players advance through escalating blinds by constructing hands, acquiring Jokers, and managing an in-game economy. Because the game combines randomness, nonlinear synergies, and long-term progression, analytical evaluation of strategy is difficult.

This project builds a **simplified Balatro-like simulator** and applies **Monte Carlo methods** to compare five commonly discussed strategy archetypes under controlled conditions.

---


### `Balatro.ipynb`
- Implements the full simulation engine
- Models:
  - 52-card deck and poker hand evaluation
  - Chip and multiplier-based scoring
  - Jokers, Vouchers, and interest-based economy
  - Progression through Small, Big, and Boss blinds
- Runs 1,000 simulations per strategy archetype
- Collects performance metrics such as:
  - Win rate
  - Maximum ante reached
  - Blinds cleared
  - Final money

### `Balatro Simulation Conclusion.pdf`
- Formal write-up of the project
- Includes:
  - Background and motivation
  - Model design and assumptions
  - Strategy definitions
  - Experimental setup
  - Statistical results with confidence intervals
  - Visualizations (boxplots and ECDFs)
  - Limitations and future work

---

## Strategy Archetypes Evaluated

The simulator compares five rule-based strategies:

- **Pair / Trips** – Prioritizes frequent, consistent hands
- **Scaling Joker** – Focuses on economy-driven multiplier growth
- **Flush / Suit** – Pursues suit-based synergies
- **Straight / Shortcut** – Builds consecutive rank patterns
- **Pareidolia / Face** – Exploits face-card synergies after acquiring a key Joker

---

## Key Findings

- **Pair / Trips** and **Scaling Joker** were the strongest performers, achieving the highest win rates and deepest progression.
- Strategies dependent on rarer synergies (Flush, Straight, Pareidolia) underperformed in the simplified model.
- Consistent, low-variance approaches proved more effective than high-synergy builds under constrained resources.

---

## Methodology

- Monte Carlo simulation with 1,000 independent runs per strategy
- Maximum ante capped at eight
- Win defined as clearing all blinds through the final ante
- Statistical analysis using confidence intervals and distributional comparisons

---

## Limitations

This simulator is **not a full recreation of Balatro**. Simplifications include:
- Limited Joker pool
- No shop rerolls or rarity tiers
- Approximate blind scaling
- Fixed 5-card draw model

The goal is comparative insight, not perfect fidelity.

---

## Future Work

Potential extensions include:
- Deck manipulation mechanics
- Expanded shop inventory and rerolls
- More realistic Joker interactions
- Dynamic strategy adaptation
- Calibration against real Balatro difficulty curves

---

## Disclaimer

This project is an analytical exercise inspired by Balatro.  
Balatro is a copyrighted game, and this work is not affiliated with or endorsed by its creators.


