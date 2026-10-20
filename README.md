# GenAI_with_LLM
Hands-on projects for Generative AI &amp; LLMs: EBMs, Autoencoder, Long short-term memory, Real NVP Model, diffusion mechanics, Convolutional Filters, MCMC sampling, and modern LLM techniques.
# Generative AI & LLM Coursework

Repository containing projects, assignments, and implementations for the Generative AI with LLMs course.

---

## 📁 Repository Structure

* `Energy_Based_Model.ipynb` — Training EBMs on MNIST with Contrastive Divergence & Langevin Dynamics

---

## 🚀 Projects & Assignments

### 1. Energy-Based Model (EBM) on MNIST
* **Objective:** Train an Energy-Based Model using a CNN energy function, Contrastive Divergence, and Langevin MCMC sampling to generate realistic handwritten digits.
* **Key Mechanics:**
  * **Score Separation:** Established a consistent logit score gap between real images ($f(x_{\text{real}}) \approx +5.0$) and synthetic MCMC noise ($f(x_{\text{fake}}) \approx -5.0$).
  * **Optimization:** Used a warm replay buffer to lower Langevin MCMC steps from 60 down to 20 in later epochs, accelerating training throughput by ~3x while maintaining generation quality.
* **Comparison with Fashion-MNIST Baseline:**
  * **Topology:** MNIST's sparse, high-contrast stroke geometry forms steeper, better-separated energy basins than the continuous garment textures in Fashion-MNIST.
  * **Stability:** Demonstrated higher convergence stability and lower variance across 120 epochs compared to the baseline.

#### Loss & Score Curves
![EBM Loss Curves](mnist_ebm_loss_curves.png)

#### Generated Digits Sample
![Generated MNIST Digits](generated_mnist_digits.png)
<img width="1189" height="490" alt="image" src="https://github.com/user-attachments/assets/b2377b68-6412-4bf1-8028-599e88410ccc" />
