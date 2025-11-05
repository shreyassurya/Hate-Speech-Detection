# 🧠 Hate Speech Detection

This project focuses on detecting **hate speech** and **offensive language** in user-generated text such as tweets or comments. It uses Natural Language Processing (NLP) and Machine Learning techniques to classify text into three categories — *Hate Speech*, *Offensive Language*, or *Neither (Clean)*.

---

## 📁 Project Structure

```
Hate-Speech-Detection/
│
├── HateSpeechData.csv          # Dataset file
├── Hate_Speech_Detection.ipynb  # Main Jupyter Notebook
└── README.md                    # Project documentation
```

---

## ⚙️ Installation & Setup

1. **Clone this repository**

   ```bash
   git clone https://github.com/shreyassurya/Hate-Speech-Detection.git
   cd Hate-Speech-Detection
   ```

2. **Install dependencies**

   ```bash
   pip install -r requirements.txt
   ```

3. **Run the notebook**
   Open `Hate_Speech_Detection.ipynb` in Jupyter Notebook or Google Colab and execute the cells in order.

---

## 🧩 Implementation Overview

### 1. **Data Upload and Preprocessing**

* The dataset is uploaded and loaded using **pandas**.
* Tweets are cleaned by:

  * Converting to lowercase
  * Removing punctuation and special characters
  * Removing stopwords

### 2. **Feature Extraction**

* **TF-IDF Vectorizer**: Converts cleaned text into numerical vectors.
* **Sentence-BERT (SBERT)**: Generates semantic embeddings for better context understanding.

### 3. **Model Training**

* **Linear SVM** trained on TF-IDF features.
* **Logistic Regression** trained on SBERT embeddings.

### 4. **Evaluation**

* Metrics such as **Accuracy**, **Precision**, **Recall**, and **F1-score** are calculated for both models.

### 5. **Prediction Interface**

* Built using **ipywidgets**, allowing users to type a comment and instantly get classification results.

---

## 🧠 Sample Predictions

| Input Text               | Predicted Class    |
| ------------------------ | ------------------ |
| "I hate people like you" | Hate Speech        |
| "You are so dumb"        | Offensive Language |
| "I like your post"       | Neither (Clean)    |

---

## 📊 Model Performance

| Model                       | Accuracy | Notes                                         |
| --------------------------- | -------- | --------------------------------------------- |
| TF-IDF + Linear SVM         | ~89%     | High precision and recall for offensive class |
| SBERT + Logistic Regression | ~87%     | Captures semantic meaning well                |

---

## 🖥️ Technologies Used

* Python
* Pandas, NumPy
* NLTK
* scikit-learn
* Sentence-Transformers
* ipywidgets
* Jupyter Notebook / Google Colab

---

## 📈 Workflow Diagram

1. Dataset Upload
2. Data Cleaning & Preprocessing
3. Feature Extraction (TF-IDF / SBERT)
4. Model Training
5. Evaluation
6. Real-time Prediction via UI

---

## 👨‍💻 Author

**Shreyas Suryawanshi**
[GitHub Profile](https://github.com/shreyassurya)

---

