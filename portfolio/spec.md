# Specification: Academic Portfolio Website

## 1. Goal
Build a clean, responsive, single-page academic portfolio for Borra Bhavitha (B.Tech Mathematics and Computing, IISc). Present me as a student with interests in Machine Learning, Deep Learning, Computer Vision, AI research, and problem solving.

## 2. Tech Stack & Constraints
* USE ONLY: HTML5, CSS3, Vanilla JS (only if absolutely necessary).
* DO NOT USE: React, Next.js, Vue, Angular, Bootstrap, Tailwind, or any external CSS frameworks.
* Keep the implementation simple, lightweight, and maintainable.

## 3. Page Structure & Content
* **Hero/Header:**
  * Name: Borra Bhavitha
  * Subtitle (Must be displayed on two separate lines): 
    * Line 1: B.Tech in Mathematics and Computing
    * Line 2: Indian Institute of Science, Bengaluru
* Include a professional profile picture (use the local file: bhavitha.jpg). Format the Hero section with a two-column, side-by-side layout on desktop: place the circular profile picture on the left, and vertically center the text (Name, Subtitle 1, Subtitle 2) on the right. Ensure this layout stacks cleanly (picture on top of text) on mobile screens.
* **About:** Short, natural first-person intro mentioning my B.Tech status at IISc and interests in ML, DL, CV, AI research, and problem-solving.
* **Academic Background:**
  * B.Tech in Mathematics and Computing | Indian Institute of Science, Bengaluru | 2024 – Present (Expected: 2028) | CGPA: 6.1
    * Core Coursework: Algorithms and Programming, Analysis and Linear Algebra, Computer Systems and Architecture, Discrete Mathematics, Linear Algebra and Multi Variable Calculus, Numerical Methods, Data Structures and Algorithms, Probability and Statistics, Introduction to Artificial Intelligence and Machine Learning, Introduction to Algebraic Structures, Introdution to Automata Theory and Computability, Introduction to Basic Analysis[cite: 3].

  * Class XII | Narayana Junior College, Kanuru | 2024 | 98.3%[cite: 3]
    * JEE Advanced Rank: 6611
    * JEE Mains Rank: 1616
  * Class X (CBSE) | Kennedy High School, Kanuru | 2022 | 95.2%[cite: 3]
* **Experience (Must be under Experience/Internship, NOT independent projects):**
  * Engineering Intern | TANUH AI Center for Excellence in Healthcare | May 2026 – July 2026.
  * Description: Contributing to AI-driven healthcare research under the TANUH AI Center of Excellence by designing, developing, and benchmarking machine learning and deep learning models for mammography-based breast tissue density classification. Research areas include Domain adaptation, self-supervised learning, semi-supervised learning, explainable AI, medical image classification, and model generalization.
* **Projects (STRICTLY ONLY THESE TWO):**
  1. **Self-Supervised Learning** (March 2026 – April 2026): Representation Analysis (PyTorch). Implemented SimCLR, MoCo, VICReg, and Barlow Twins. Analyzed robustness to label noise, representation quality, and training dynamics using linear probing and embeddings. Observed improved generalization over supervised learning and sensitivity to early training corruption.
  2. **Breast Tissue Density Classification** (May 2026 – July 2026): Carried out during engineering internship. Implemented and benchmarked ML/DL models for breast tissue density classification from mammograms. Designed domain adaptation, self-supervised, semi-supervised, and contrastive frameworks. Developed DANN-based pipelines (DenseNet121, RegNetY-8GF, NFNet-F3, MAE-ViT, DINOv2, Barlow Twins, Mean Teacher, SupCon). Evaluated SVM/ELM and end-to-end models. Implemented TransMIL. Used Grad-CAM++ and Attention Rollout. Built scalable PyTorch pipelines.
* **Skills (Format strictly as "Category: skill_1, skill_2, ..."):**
  * Programming: Python, C (basics), Bash
  * ML/DL: PyTorch, Scikit-learn, NumPy, Pandas, Deep Learning, CNNs, Vision Transformers, Self-Supervised Learning, Semi-Supervised Learning, Domain Adaptation, Contrastive Learning
  * Computer Vision: OpenCV, Feature Extraction, Image Classification, Data Augmentation, Explainable AI
  * Core CS: Data Structures & Algorithms, Operating Systems, Recursion, Problem Solving, Competitive Programming
  * Systems/Tools: Python-C Integration, Memory Management, Algorithm Optimization, Git, VS Code, pydicom
  * Certifications: Introductory course on Quantum Computing (CDAC & IIT Roorkee)[cite: 3].
* **Interests:** Machine Learning, Deep Learning, Problem Solving (integrate naturally).
* **Extra-curricular Activities:**
  * Event Coordinator: Telugu Samskrutika Samiti (TSS) (2025–Present) and Pravega Culturals-Dance (Lasya, 2025)[cite: 3].
  * Volunteer: IISc Open Day (2025: "Match the Emoji" facial recognition demo; 2026: Tower of Hanoi recursion visualization) and Pravega 2024[cite: 3].
  * Mentorship: Tutored Class 11 and 12 students preparing for JEE[cite: 3].
  * Creative: Design Team and Dancer (Classical Kuchipudi, Freestyle)[cite: 3].
* **Contact:**
  * Emails: bhavithab@iisc.ac.in, borrabhavitha@gmail.com
  * LinkedIn: https://www.linkedin.com/in/borra-bhavitha
  * GitHub: [https://github.com/bhavitha1917](https://github.com/bhavitha1917)
* **CV/Resume:** Link to the local file Borra_Bhavitha_CV.pdf. Make sure it opens in a new tab.

## 4. Design & UX
* **Vibe:** Modern academic/research portfolio. Clean, professional, and elegant.
* **Colors:** 
  * Background: Soft, very pale lavender (e.g., #F4F0FA or similar) to give it some life without being overwhelming.
  * Primary Text/Headings: Deep navy/dark blue.
  * Secondary Text: Subtle dark gray.
* **Typography:** Manrope for headings and Inter for body text, with strong system sans-serif fallbacks.
* **Responsiveness:** Must work perfectly on mobile, tablet, and desktop. No horizontal overflow.
* **Component Styling:** The content inside every single section (About, Academic Background, Experience, Projects, Skills, Extra-curricular Activities) must be enclosed within clean, white "card" containers (with rounded corners and a subtle drop shadow) so they pop off the lavender background uniformly.

## 5. Artifacts to Generate
Generate `index.html`, `style.css`, and `script.js` (only if needed).
Alongside the code, create:
* `issues.md`: Note any implementation issues discovered (like placeholder links).
* `insights.md`: Note important design/implementation decisions for future work.
