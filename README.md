# A-Content-Adaptive-Framework-for-High-Security-Image-Encryption.
CNN-Transformer Fusion with Multi-Chaotic Dynamics: A Content-Adaptive Framework for High-Security Image and Video Encryption.
🔐 Deep Content-Driven Image Encryption using CNN–ViT Fusion and Multi-Chaotic Systems
📌 Overview

This project implements a high-security image encryption framework using a hybrid deep learning architecture combined with multi-chaotic dynamics.

The system generates content-dependent cryptographic keys using a fusion of:

Convolutional Neural Networks (CNN)
Vision Transformers (ViT)
Multi-head attention

These keys are then used to drive chaotic maps for secure image encryption and decryption.

🧠 Key Features
🔹 Content-driven key generation
🔹 CNN + Vision Transformer fusion
🔹 Attention mechanism for feature fusion
🔹 Adaptive chaotic map selection
🔹 Permutation + XOR-based diffusion encryption
🔹 Entropy-based security evaluation
🏗️ Architecture
1️⃣ AdvancedLKM (Learning Key Model)

A hybrid deep learning model that extracts robust image features:

ResNet18 (CNN) → local features
ViT-B/16 (Transformer) → global features
Multi-Head Attention → fuse CNN + ViT features
Fully connected layers → generate high-dimensional key

Output: content-dependent encryption key

2️⃣ Multi-Chaotic Maps

Chaotic generators included:

Logistic Map
Tent Map
Sine Map
Henon Map
Chebyshev Map

A deterministic chaos selector chooses the map based on the deep key.

3️⃣ Key Generation Strategy
Deep key → scalar seed
Select chaotic map
Generate pseudo-random sequence
Convert to byte-level encryption key
4️⃣ Encryption & Decryption

Encryption:

Shuffle pixels using chaotic permutation
XOR pixel values with chaotic key

Decryption: reverse XOR → inverse permutation → original image

5️⃣ Security Metric
Shannon Entropy measures randomness
Ideal value ≈ 8 for 8-bit images
Higher entropy → stronger encryption
📖 How to Use
1️⃣ Clone the Repository
2️⃣ Install Dependencies
pip install torch torchvision numpy opencv-python matplotlib pillow
3️⃣ Prepare Your Image
Place your image in the project folder (e.g., D4.png)
Supported formats: .png, .jpg, .jpeg
4️⃣ Run the Script

Update the input path in the script:

input_path = "D4.png"

Then execute:

python main.py
5️⃣ Output
Displays:
Original image
Encrypted image
Decrypted image
6️⃣ Optional: Use as Function
model = AdvancedLKM().to(device)
model.eval()
process_image("your_image.png", model)
7️⃣ GPU Acceleration
Automatically uses GPU if available:

device = torch.device("cuda" if torch.cuda.is_available() else "cpu")
📊 Example Result
Encrypted image is visually scrambled
Decryption restores original perfectly
Entropy of encrypted image ~ 7.9+
🔒 Security Advantages
Content-dependent keys → resistant to known-plaintext attacks
High sensitivity to input changes
Large key space
Multi-chaotic unpredictability
📌 Applications
Secure image transmission
Medical image protection
Military and surveillance systems
IoT security
📄 License : This project is for research and academic purposes.

Voici un guide complet pour ton code, incluant instructions d’usage, dépendances, et explications des principaux algorithmes utilisés. Je vais structurer ça de manière claire et scientifique.

1️⃣ Dépendances

Avant d’exécuter le script, assure-toi d’avoir installé :

pip install torch torchvision pillow matplotlib numpy
torch / torchvision : PyTorch pour réseaux de neurones et modèles pré-entraînés (ResNet18 et ViT).
Pillow (PIL) : Chargement et traitement des images.
numpy : Calculs numériques et génération des séquences chaotiques.
matplotlib : (optionnel ici) pour visualisation si nécessaire.

⚠️ Note : ce code est conçu pour GPU (CUDA) si disponible. Sinon, il utilise CPU automatiquement.

2️⃣ Usage Instructions
Placer l’image que tu veux chiffrer dans le même dossier que le script.
Modifier le chemin de l’image dans la variable :
input_path = "image(D4).png"
Lancer le script.

✍️ Author : Hmidi Alaeddine
