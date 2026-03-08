# 🖼️ Image Captioning

> Give a model an image, and it will tell you what's in it — in plain English. This project builds an end-to-end image captioning system that understands visual content and generates meaningful, human-readable descriptions automatically.

---

## 🧭 What Is This Project?

Image captioning sits right at the intersection of **computer vision and natural language processing**. The challenge is not just recognising what objects are in an image, but understanding the relationships between them and expressing that as a coherent sentence.

This project implements a classic **encoder-decoder architecture** where a CNN-based encoder extracts rich visual features from an image, and a Transformer-based decoder takes those features and generates a descriptive caption word by word. Trained on a vocabulary of **50,000 tokens** and run on a **GPU environment** for faster training, the model is built to handle real-world image complexity.

---

## 📁 Project Structure

```
Image-Captioning/
│
├── image_captioning.ipynb                      # Full pipeline: preprocessing, training, inference
├── encoder_model_50000_model.keras             # Saved encoder model
├── encoder_model_50000_model.h5                # Encoder model in HDF5 format
├── encoder_weights_50000_model.weights.h5      # Encoder weights
├── encoder_architecture_50000_model.json       # Encoder architecture in JSON
├── decoder_model_50000_model.keras             # Saved decoder model
├── decoder_model_50000_model.h5                # Decoder model in HDF5 format
└── decoder_weights_50000_model.weights.h5      # Decoder weights
```

---

## 🛠️ Models, Concepts and Tools

**Models and Concepts:**
- 🏛️ **InceptionV3 (CNN)** - Pretrained on ImageNet, used as the visual encoder to extract high-level spatial features from input images
- 🔁 **Transformer Decoder** - Attends to the encoded image features and generates captions token by token using self-attention and cross-attention mechanisms
- 🔤 **Tokenization** - Text captions are tokenized over a vocabulary of 50,000 tokens for sequence generation
- 🧩 **Encoder-Decoder Architecture** - Image features and language generation are handled as two separate but connected components
- ⚡ **Transfer Learning** - InceptionV3 weights are leveraged from pretraining so the model focuses on learning caption generation rather than visual features from scratch

**Tools and Libraries:**
- 🐍 **Python** - Core language
- 📓 **Jupyter Notebook** - Development and experimentation
- 🤖 **TensorFlow / Keras** - Model building, training, saving, and inference
- 🖼️ **InceptionV3 (keras.applications)** - Pretrained CNN for image feature extraction
- 🔢 **NumPy** - Array operations and data handling
- 📊 **Matplotlib** - Visualizing training results and sample captions

---

## 🗂️ Saved Model Files

The repository includes **pre-trained encoder and decoder model files** so you don't have to train from scratch. Both `.keras` and `.h5` formats are provided for compatibility across different TensorFlow versions.

- Load `encoder_model_50000_model.keras` to extract image features from new images
- Load `decoder_model_50000_model.keras` to generate captions from those features
- Weights are also saved separately in case you want to load just the architecture and reinitialise

---

## ⚙️ Training Environment

- **GPU-accelerated training** for handling the computational load of InceptionV3 feature extraction and Transformer training
- Vocabulary size: **50,000 tokens**
- Framework: **TensorFlow / Keras**

---

## 💡 Key Highlights

- **No training required to try it out** — pre-saved model files are ready to load and run inference directly
- **Separation of encoder and decoder** means either component can be swapped or fine-tuned independently
- **Transfer learning with InceptionV3** keeps the model efficient without needing massive image datasets
- **Bridges vision and language** in a clean, well-structured notebook pipeline

---

## 🌍 Real-World Applications

Image captioning might sound like a research concept, but it has genuinely practical uses across many fields:

- ♿ **Accessibility** - Automatically generating alt-text for images helps visually impaired users understand visual content on websites and apps
- 🛒 **E-commerce** - Auto-captioning product images saves time for sellers and improves searchability for buyers
- 🏥 **Medical Imaging** - Describing radiology scans or pathology slides in natural language can assist doctors in documentation and reporting
- 📰 **News and Media** - Automatically tagging and captioning large volumes of images speeds up editorial workflows
- 🔍 **Image Search** - Caption generation powers smarter image search engines that go beyond keywords
- 🤖 **Robotics and AI Assistants** - Helps robots and AI systems describe their visual environment in natural language for better human-machine interaction
- 🎓 **Education** - Generating descriptions for educational images and diagrams makes learning material more accessible

---

## 🙋‍♀️ About the Author

Built with 💙 by **[Pranitee Majukar](https://github.com/pranitee23)**

*Found this helpful? A ⭐ would be really appreciated!*
