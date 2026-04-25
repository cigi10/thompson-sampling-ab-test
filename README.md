# thompson-sampling-ab-test

A 2-armed bandit solution to A/B testing on the Cookie Cats dataset. Beta-Bernoulli posterior updates over 10,000 simulated users with cumulative regret tracking.

## Overview
Cookie Cats is a mobile puzzle game where players encounter gates that force them to wait before continuing. This project frames the two gate placements (gate_30 vs gate_40) as a Multi-Armed Bandit (MAB) problem and uses Thompson Sampling to dynamically allocate traffic to the better-performing variant, rather than running a static A/B test.

## Results

| Metric | Value |
|---|---|
| True mean A (gate_30) | 0.4482 |
| True mean B (gate_40) | 0.4423 |
| Oracle (mu*) | 0.4482 |
| Final cumulative regret | 17.02 |
| Model A chosen | 7118 / 10000 (71.2%) |
| Model B chosen | 2882 / 10000 (28.8%) |

The agent correctly identified gate_30 as the better variant, converging to it with 71.2% selection rate and a low cumulative regret of 17.02 over 10,000 iterations.

## Plots

![Cumulative Regret](https://github.com/user-attachments/assets/59251e9c-e2a8-4996-8140-21840d7ffb92)

## Dataset
[Cookie Cats - Kaggle](https://www.kaggle.com/datasets/mursideyarkin/mobile-games-ab-testing-cookie-cats)

## Stack
Python, NumPy, pandas, matplotlib
