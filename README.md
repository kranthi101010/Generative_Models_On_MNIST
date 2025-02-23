# Generative_Models_On_MNIST
Generative Deep Learning: Exploring RNNs, Variational Autoencoders (VAEs), and Conditional GANs on MNIST


## 🚀 Overview  
This project explores **generative deep learning models** to **generate, reconstruct, and manipulate images** using **RNNs, VAEs, and Conditional GANs** on the **MNIST dataset**.

---

## 🎯 Project Goals  
- **Train an RNN-based generative model** to reconstruct MNIST digits from sequential patches.  
- **Use a Variational Autoencoder (VAE)** to learn meaningful latent representations.  
- **Train a Conditional GAN** to generate MNIST images conditioned on labels.  

---

## 📂 Dataset  
- **MNIST Dataset:** Standard handwritten digit dataset, consisting of **60,000 training** and **10,000 testing images** (28×28 grayscale).  
- **Preprocessing:**  
  - Images are **normalized** and resized.  
  - **Patch extraction (7×7)** for RNN-based image reconstruction.  
  - **Latent space analysis (VAE)** using **dimension reduction techniques**.  
  - **Label conditioning for GANs** to generate class-specific images.  

---

## 🧠 Implemented Models and Methodology  

### **1️⃣ RNNs as Generative Models for Image Reconstruction**  
- Images are broken down into **7×7 patches**, and an **LSTM-based RNN** learns to reconstruct missing parts.  
- **The model predicts future patches**, generating complete images step-by-step.  
- The trained model successfully reconstructs digits with **realistic features**.  

---

### **2️⃣ Variational Autoencoders (VAEs) on MNIST**  
- The VAE consists of an **encoder-decoder architecture** that learns **latent space representations**.  
- The **encoder compresses images** into a smaller latent space, capturing essential features.  
- **Latent variable analysis** allows controlled image manipulation by varying learned dimensions.  
- Results show that **dimension 3 captures unique transformations** unseen in standard MNIST.  

---

### **3️⃣ Conditional GAN for Image Generation**  
- Unlike standard GANs, **Conditional GANs (cGANs) use label information** to guide image generation.  
- The **generator takes both noise and digit labels** to create class-specific handwritten digits.  
- The **discriminator learns to distinguish between real and fake images** while also verifying labels.  
- Results indicate that **GAN-generated images improve significantly when conditioned on labels**.  

---

## 📊 Results & Observations  

| **Model** | **Key Findings** |
|-----------|----------------|
| **RNN (LSTM) Generative Model** | Successfully reconstructs missing patches in MNIST images. |
| **VAE** | Allows controlled modifications in the latent space; Feature disentanglement is observed. |
| **Conditional GAN** | Generates **sharper, high-quality** digits compared to traditional GANs. |

### **Key Takeaways:**  
✅ **RNN-based models can be used for sequential image reconstruction**, improving **patch-based generation tasks**.  
✅ **VAEs provide meaningful latent space embeddings**, enabling feature-controlled modifications.  
✅ **Conditional GANs improve image realism** and provide **better training stability compared to standard GANs**.  
✅ **GAN training convergence can be visualized using discriminator and generator accuracy trends**.  

---

## 🔬 Model Performance and Evaluation  

### **RNN-based Image Reconstruction Performance:**  
- **Reconstructed images closely resemble original digits** with minor distortions in finer details.  
- **Sequential generation from patches captures underlying structures well**.  

### **VAE Latent Space Manipulation Results:**  
- **Varying specific latent dimensions** alters shape and thickness of digits.  
- **Dimension 3** in latent space **captures transformations not common in MNIST**.  

### **Conditional GAN Performance:**  
- **Initial epochs generate blurry images** with unstable training.  
- After convergence, **the model learns to generate digits with clear class-specific structures**.  
- Discriminator **converges faster**, and **generator improves image sharpness over epochs**.  

📈 **Graph: GAN Training Convergence**  
(Example plot showing how discriminator and generator losses stabilize over time.)  

---

## ⚙️ Dependencies  
Ensure you have the following installed before running the project:  

```bash
pip install tensorflow torch torchvision numpy matplotlib
