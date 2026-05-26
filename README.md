# multimodal-emotion-recognition
A multimodal emotion recognition framework that combines ResNet-50 image features and CLIP text embeddings using a Late Fusion strategy. The project includes data preprocessing, feature extraction, model training, and evaluation for emotion classification tasks.

# Multimodal Late Fusion Framework using ResNet-50 and CLIP

## Overview

This project implements a multimodal emotion classification framework that combines visual and textual information using a Late Fusion strategy.

The visual modality is processed with a ResNet-50 convolutional neural network, while the textual modality is represented using CLIP text embeddings. The final prediction is produced through weighted late fusion of the visual and textual outputs.

The project was developed as part of the HAICAI 2026 coursework and demonstrates multimodal learning techniques for emotion recognition tasks.

---

## Features

- Image classification using ResNet-50
- Text representation using OpenAI CLIP (ViT-B/32)
- Cross-modal pairing of image and text data
- Multimodal Late Fusion architecture
- Evaluation using Accuracy and Macro F1 Score
- Visualization of training performance

---

## Project Structure

```
HAICAI_2026.ipynb      # Main notebook containing the complete pipeline
README.md             # Project documentation
requirements.txt      # Python dependencies
```

---

## Installation

Clone the repository:

```bash
git clone https://github.com/your-username/your-repository.git
cd your-repository
```

Install the required packages:

```bash
pip install -r requirements.txt
```

Alternatively, install the main dependencies manually:

```bash
pip install torch torchvision transformers scikit-learn pandas numpy matplotlib pillow
pip install git+https://github.com/openai/CLIP.git
```

---

## Usage

Open and run the notebook:

```bash
jupyter notebook HAICAI_2026.ipynb
```

or

```bash
jupyter lab
```

Execute the notebook cells sequentially to:

1. Load and preprocess the dataset.
2. Generate image features using ResNet-50.
3. Generate text embeddings using CLIP.
4. Perform cross-modal pairing.
5. Train and evaluate the multimodal model.
6. Compute performance metrics.

---

## Model Architecture

### Visual Branch
- Backbone: ResNet-50
- Input Size: 224 × 224
- Output: Emotion classification logits

### Text Branch
- Model: CLIP (ViT-B/32)
- Input: Text descriptions
- Output: Text embeddings

### Fusion Strategy
Late Fusion with weighted combination:

- Visual contribution: 0.6
- Text contribution: 0.4

Final prediction is obtained by combining the outputs of both modalities.

---

## Results

| Model | Accuracy | Macro F1 |
|---------|---------|---------|
| Visual Only (ResNet-50) | 0.570 | 0.574 |
| Text Only (CLIP) | 0.238 | 0.173 |
| Multimodal (Late Fusion) | 0.570 | 0.574 |

### Best Performing Model

**Multimodal Late Fusion**

- Accuracy: **57.0%**
- Macro F1 Score: **57.4%**

---

## Technologies Used

- Python
- PyTorch
- Torchvision
- OpenAI CLIP
- NumPy
- Pandas
- Scikit-learn
- Matplotlib

---

## Future Improvements

- Early Fusion architectures
- Attention-based multimodal fusion
- Hyperparameter optimization
- Larger multimodal datasets
- Transformer-based visual encoders

---

## Author

Developed for the HAICAI 2026 project on Multimodal Emotion Recognition.
