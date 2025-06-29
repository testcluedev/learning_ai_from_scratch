# 🤖 Learning AI From Scratch

Welcome! This repository documents my personal hands-on journey to understand how and what a **modern AI Engineer** does — starting completely from scratch with **NLP**, **machine learning**, and practical experiments. The goal is to take tiny steps all the way to using the models, agents, automated networking and security tools.

I built this to:
- Learn the basics step by step (math, code, pipeline)
- Practice building real sentiment analysis models
- Explore classic NLP before jumping to large language models (LLMs)
- Keep track of my questions, answers, and progress

---

## ✅ What's inside?

- 📓 **Jupyter notebooks** — working examples, notes, experiments  
- 🧩 Classic NLP pipelines — sigmoid, logistic regression, Naive Bayes  
- 📊 TF-IDF vectorizer with bigrams — modern text baseline  
- 🔍 **[Results.md](Results.md)** — detailed accuracy comparisons & final plots  
- 📂 Everything built in Python in a virtual environment

---

## 🗺️ Learning Plan & Roadmap

Here’s the **phased plan** I’m following:
1️⃣ **Understand core math:**  
   - Sigmoid function, theta (weights), bias term  
   - Cost function and gradient descent  

2️⃣ **First NLP classifier:**  
   - Raw word frequency counts  
   - Manual logistic regression to see the math directly

3️⃣ **Classic bag-of-words model:**  
   - Naive Bayes classifier  
   - Understand word likelihoods & independent word assumption

4️⃣ **TF-IDF upgrade:**  
   - Switch to weighted word importance  
   - Add bigrams for context (e.g., “not good”)

5️⃣ **Stronger classifier:**  
   - Logistic Regression on sparse TF-IDF  
   - Regularization, interpret learned weights

6️⃣ **Modern LLM step:**  
   - Next: move to BERT or DistilBERT  
   - Try fine-tuning on small text sets

7️⃣ **Deploy & automate:**  
   - Wrap in an API  
   - Create LLM-based chatbot or RAG system  
   - Integrate with my MCP server

---

## 🔢 Common Questions I Explored

Here are some **real questions I asked myself while building this**:

- **What is the bias term?**  
  → It’s a constant value added to the input so the model can shift the decision boundary left or right. It’s typically set to `1` so its weight (theta₀) can be learned freely.  

- **Why do we set bias to 1?**  
  → If you didn’t fix it to 1, the model couldn’t adjust the baseline prediction. The bias weight lets the prediction be non-zero even if all features are zero.

- **Where does `theta` come from?**  
  → Theta is the vector of learnable weights, updated with gradient descent to minimize the cost function.

- **What is TF-IDF really doing?**  
  → It balances each word’s frequency with how unique it is across all documents — highlighting words that are common in *one* doc but rare overall.

- **How does Naive Bayes differ from Logistic Regression?**  
  → Naive Bayes models `P(word | class)` for each word & multiplies them. Logistic Regression learns weight coefficients for each feature — more flexible when features correlate.

- **What libraries help hide the math?**  
  → Libraries like `scikit-learn` (vectorizers, `MultinomialNB`, `LogisticRegression`), `PyTorch` (tensors, loss functions), and `TensorFlow` do the math under the hood with simple function calls. You focus on the pipeline, not low-level derivatives.

---

## 📊 Full Experiment Results

👉 See **[Results.md](Results.md)** for:
- Comparison table of all techniques
- How accuracy improved from 67% → 86%
- Final plots of the sentiment model pipeline

---

## 🚀 Recommended Courses I’m Using

- ✅ [Coursera NLP Specialization](https://www.coursera.org/specializations/natural-language-processing)
- ✅ [FastAI Practical Deep Learning](https://course.fast.ai/)
- ✅ [deeplearning.ai Prompt Engineering](https://learn.deeplearning.ai/)
- for more learning 👉 See **[learning_plan.md](learning_plan.md)** for:

---

## 🔗 How to run this

```bash
# Clone the repo
git clone https://github.com/YOURUSERNAME/learning_ai_from_scratch.git

# Set up virtual environment & activate
python -m venv venv
source venv/bin/activate  # or venv\\Scripts\\activate on Windows

# Install dependencies
pip install -r requirements.txt

# Launch Jupyter
jupyter notebook
