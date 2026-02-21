# 🎧 Deep Learning for Audio Reconstruction and Style Transfer

## 📌 Overview

This project explores multiple deep learning approaches for **audio reconstruction** and **style transfer**, progressively adapting objectives to computational constraints.

Initially designed to generate music using a Variational Autoencoder (VAE), the project evolved toward:

- 🎼 Music reconstruction  
- 🎹 Music style transfer  
- 🎤 Voice style transformation  

The work is structured chronologically into four main parts:

- **P1 — Music Reconstruction with RNNs**
- **P2 — Music Style Transfer**
- **P3 — Voice Style Transfer (Digits Dataset)**
- **P4 — Improved Voice Modeling with Embeddings**

---

# 🧠 Part 1 — Music Reconstruction with RNNs

## Dataset

- Scraped from *Free Music Archive* (licenses verified)
- 198 to 1840 "chill" tracks
- Additional datasets:
  - Piano (154 tracks)
  - Aggressive / Phonk / Hard (120 tracks)

All tracks were converted into spectrograms of size:

```
1025 × 2000  (~46 seconds)
```

Data was globally normalized.

## Models Tested

- Linear VAE  
- Convolutional VAE  
- Hybrid architectures  
- RNN / LSTM / GRU encoder-decoder  
- RNN-based VAE  
- Transformer  

## Loss Function

```python
MSE(log(1 + x), log(1 + x_hat))
```

This reflects human auditory perception (logarithmic sensitivity to amplitude).

## Key Findings

- RNNs and GRUs performed best for reconstruction.
- LSTMs were less effective (music patterns were mostly short-term).
- Reconstruction quality was strong.
- Generation ability was very limited.
- GPU RAM constraints prevented scaling to larger architectures.

---

# 🎼 Part 2 — Music Style Transfer

## Objective

Transform **piano ↔ chill** music styles.

## Approach

- Removed chunking strategy.
- Added one-hot encoding for style conditioning.
- Introduced:
  - Bottleneck layer
  - FiLM (Feature-wise Linear Modulation)

## Style Difference (Average Pixel Difference)

| Method | Difference |
|--------|------------|
| Basic RNN | 0.33 |
| New aggressive dataset | +44% improvement |
| Bottleneck | 0.58 |
| Bottleneck + FiLM | 2.3 |

Although perceptible differences appeared, true stylistic transformation remained limited.

### Observed Trade-off

Reconstruction quality vs. style strength.

---

# 🔢 Part 3 — Voice Style Transfer (Digits Dataset)

To simplify the task:

- Kaggle dataset
- 6 speakers
- Digits 0–9
- 50 variations per digit
- 3000 total samples

Spectrogram size:

```
1025 × 80
```

## Experiments

- Linear VAE
- Fully Convolutional VAE
- Latent dimension tuning
- Masked loss (ignoring padding)
- Transformer (caused linearization effect)

## Observations

- Smaller latent dimensions improved stability.
- Latent dimension = 2 performed surprisingly well.
- MSE overly smoothed outputs.
- L1 loss preserved sharper details.
- Style transfer remained shallow.

---

# 🚀 Part 4 — Improved Architecture

## Improvements

- Reduced hop length → spectrogram size:

```
512 × 50
```

- Replaced one-hot encoding with learnable embeddings.
- Embedding dimension: 32.
- Used masked loss functions (ignore padding).

## Architectures Tested

- Linear model (latent = 32)
- Convolutional model (latent = 20)
- Convolutional model (latent = 50)
- Hybrid + FiLM

## Results

- Voice timbre preserved.
- Style transfer perceptible.
- Digit recognition still weak.
- FiLM improved low-amplitude modeling but slightly degraded global quality.

---

# 📊 Key Insights

- Models were highly effective at reconstruction.
- Style transfer remains limited.
- Dataset diversity strongly impacts performance.
- Spectrogram representation complexity is challenging.
- Smaller latent spaces sometimes generalize better.
- Hardware constraints significantly shaped architectural decisions.

# 📁 Project Structure

```
P1/       → Music Reconstruction
P2/       → Music Style Transfer
P3/       → Voice VAE Experiments
P4/       → Embedding + Improved Models
Autres/   → Local working version
```

Each part contains:

- Dedicated README
- Jupyter notebooks
- Visualizations
- Audio samples (when possible)

⚠️ Dataset (~12GB) is not included in this repository.

---

# 🔮 Future Improvements

- Use pretrained audio models and fine-tune them
- Improve FiLM integration across layers
- Implement GAN-based style transfer
- Add perceptual loss (e.g., MFCC-based)
- Use larger and more structured datasets
- Increase computational power

---

# 🎯 Conclusion

This project demonstrates iterative experimentation under computational constraints.

It successfully achieved:

- Strong spectrogram reconstruction
- Perceptible voice style modification
- Conditional modeling using embeddings
- Exploration of FiLM for audio tasks

With more compute and a better structured dataset, these methods could be significantly extended.
