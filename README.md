# Deep Content-Driven Key Generation & Multi-Chaotic Image Encryption

This repository implements a **CNN + ViT + Attention-based key generator** for deterministic image encryption using **multi-chaotic maps**.  
It also computes the **entropy of encrypted images** and provides a **high-security, content-adaptive framework** for image and video encryption.

---

## 🔹 Features

- **Advanced key generation from images** using:
  - **ResNet18 (CNN)** → local features  
  - **ViT-B/16 (Vision Transformer)** → global features  
  - **Multihead Attention** → fuse CNN + ViT features  
- **Deterministic multi-chaotic key generator**:
  - Logistic Map, Tent Map, Sine Map  
  - Henon Map, Chebyshev Map  
  - Chaos map selection based on deep key
- **Image encryption using**:
  - Pixel **permutation**  
  - Pixel **XOR with chaotic key**
- **Security evaluation**:
  - Entropy calculation of encrypted images (ideal ≈ 8 for 8-bit images)

---

## 🏗️ Architecture

### 1️⃣ AdvancedLKM (Learning Key Model)
Hybrid deep learning model that extracts robust image features:

- ResNet18 → local features  
- ViT-B/16 → global features  
- Multi-Head Attention → fuse features  
- Fully connected layers → generate high-dimensional, content-dependent key

### 2️⃣ Multi-Chaotic Maps
Generates pseudo-random sequences using:

- Logistic Map  
- Tent Map  
- Sine Map  
- Henon Map  
- Chebyshev Map  

Chaos map is selected deterministically based on the deep key.

### 3️⃣ Key Generation Strategy
1. Deep key → scalar seed  
2. Select chaotic map  
3. Generate pseudo-random sequence  
4. Convert to byte-level encryption key  

### 4️⃣ Encryption & Decryption
**Encryption:**

- Shuffle pixels using chaotic permutation  
- XOR pixel values with chaotic key  

**Decryption:** reverse XOR → inverse permutation → restores original image


## ⚙️ Parameters & Configuration
- `chaos_map_type`: Choose from ['logistic', 'tent', 'sine', 'henon', 'chebyshev']
- `patch_size`: Patch size for ViT (default: 16)
- `cnn_model`: CNN backbone (default: ResNet18)

## 📝 Notes
- Recommended image size: 256x256 or 512x512
- Large images may increase processing time
- GPU usage is highly recommended for faster key generation and encryption


## 🔬 References
H. Alaeddine, "Deep Content-Driven Key Generation via CNN–Transformer Fusion with Multi-Chaotic Dynamics for High-Security Image and Video Encryption", *The Visual Computer*, 2026.

## 🔹 Dependencies

Install the required packages:

```bash
pip install torch torchvision pillow numpy matplotlib opencv-python
namics for High-Security Image and Video Encryption", *The Visual Computer*, 2026.


