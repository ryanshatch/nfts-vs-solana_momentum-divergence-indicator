# NFTs vs SOL — Settings Guide

This file explains what each setting does in simple terms.

## Symbols

### Solana
This is the main SOL chart used for comparison.

### Proxy Symbols
These are the tokens used to build the proxy basket.

Examples:
- BLUR
- LOOKS
- TNSR
- MAGIC
- APE
- ME
- PENGU
- JUP
- SNS
- DBR
- S
- ADA
- ETH

If a token is not available on your exchange feed, change that symbol manually.

---

## Weights

Each proxy token has a weight.

- **Higher weight** = that token matters more in the proxy basket
- **Lower weight** = that token matters less
- **0 weight** = that token is ignored

### Normalize by active weight sum
This keeps the basket more balanced when you turn tokens on or off.

- **On:** better for comparing different token mixes
- **Off:** raw weighted total

---

## Calculation

### Momentum Length
How far back SOL momentum is measured.

- Lower = faster, more sensitive
- Higher = slower, smoother

### Z-Score Length
How far back the script measures what is normal or abnormal.

- Lower = more reactive
- Higher = smoother, steadier

### Smoothing
Softens the lines.

- Lower = more sharp movement
- Higher = cleaner, slower movement

### Normalize each symbol by running mean
Adjusts each proxy token against its own recent average activity.

- **On:** better when tokens have very different sizes
- **Off:** uses raw activity

### Per-symbol running mean length
How much history is used for that normalization.

- Lower = faster adjustment
- Higher = slower adjustment

### Use close × volume instead of raw volume
Uses approximate dollar activity instead of plain volume.

- **Off:** raw token volume
- **On:** price-adjusted activity

---

## Colors

These settings only change appearance.

You can change the colors for:
- BLUR
- LOOKS
- TNSR
- MAGIC
- APE
- ME
- PENGU
- JUP
- SNS
- DBR
- S
- ADA
- ETH

---

## Simple starting setup

A simple default setup:

- **Momentum Length:** 14
- **Z-Score Length:** 50
- **Smoothing:** 5
- **Normalize each symbol by running mean:** On
- **Per-symbol running mean length:** 100
- **Normalize by active weight sum:** On
- **Use close × volume:** Off

---

## Quick tips

- Want faster signals -> lower the lengths
- Want cleaner signals -> raise the lengths
- Want fairer comparison between big and small tokens -> keep normalization on
- Want to remove a token -> set its weight to 0
- Want one token to matter more -> raise its weight