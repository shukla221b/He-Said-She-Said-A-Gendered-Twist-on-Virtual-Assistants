# 🎙️ He Said, She Said: A Gendered Twist on Virtual Assistants

This project explores how voice-based virtual assistants can be enhanced using machine learning models that adapt responses based on a speaker’s gender. It aims to promote more **empathetic**, **personalized**, and **ethically aware** AI interactions.

---

## 🧠 Problem Statement

Current virtual assistants operate on a one-size-fits-all paradigm, often missing personalization cues that could improve engagement and user satisfaction. Our project leverages audio-based features to classify gender and proposes using this signal to create more relatable virtual assistant interactions.

---

## 💡 Project Highlights

- **Goal**: Build a gender-sensitive voice classifier to tailor virtual assistant interactions
- **Impact**: Unlocks potential for AI systems that consider user context like gender, emotion, culture
- **Dataset**: Vocal Gender Features Dataset (10,380 audio samples, ~5768 valid instances)

---

## 🔍 Feature Engineering

- **Feature Types**: Spectral, Pitch, Energy, Frequency, Complexity
- **Feature Selection**: 
  - Removed highly correlated features (threshold > 0.9)
  - Top 20 features chosen via Random Forest and Decision Tree importance scores
  - Final 12 features selected using Recursive Feature Elimination + domain expertise

---

## ⚙️ Model Pipeline

- **Preprocessing**: 
  - Train-Test split (70-30)
  - Standardization using `StandardScaler`
  - Class balancing via **SMOTE**
  
- **Models Evaluated**:
  - Logistic Regression
  - Support Vector Machine (SVM)
  - Random Forest
  - LSTM
  - CNN

- **Best Performer**: **SVM** (98% accuracy, highest macro precision/recall)

---

## 📊 Model Evaluation

| Model             | Accuracy | Precision | Recall | F1-Score |
|------------------|----------|-----------|--------|----------|
| Logistic Reg.     | 95%      | 91%       | 94%    | 93%      |
| **SVM**           | **98%**  | **98%**   | **98%**| **98%**  |
| Random Forest     | 97%      | 97%       | 95%    | 96%      |
| LSTM              | 98%      | 97%       | 96%    | 97%      |
| CNN               | 96%      | 94%       | 95%    | 95%      |

---

## 🎧 Real World Testing

- Successfully tested on real voice clips
- Achieved **66.6% success rate** on real audio samples—highlighting the need for broader training data

---

## 🚧 Limitations & Next Steps

| Limitation                        | Mitigation Strategy                                      |
|----------------------------------|-----------------------------------------------------------|
| Binary gender classification     | Explore non-binary or spectrum-based models              |
| Accent/noise sensitivity         | Augment dataset with diverse accents and conditions      |
| Male-heavy dataset               | Improve class balance through more inclusive sampling    |

---

## 🔮 Future Scope

- Real-time deployment in virtual assistants
- Emotional tone detection and adaptation
- Multi-language voice recognition

---

## 👥 Team

- **Rishabh Shukla**
- Angel Mary Oviya  
- Shubhi Phartiyal