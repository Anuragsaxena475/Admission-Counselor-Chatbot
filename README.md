
# 🎓 Admission Counselor Chatbot 🤖

An AI-powered chatbot built to assist students during the **college admission process** by providing quick, relevant responses to frequently asked questions. This bot reduces the workload on admission staff by intelligently handling repetitive queries using **Natural Language Processing (NLP)** and **Deep Learning**.

---

## 🧠 Technologies Used

| Technology         | Purpose                                                              |
| ------------------ | -------------------------------------------------------------------- |
| Python             | Core programming language                                            |
| TensorFlow / Keras | Deep learning framework for building and training the neural network |
| NLTK               | Text preprocessing, tokenization, and lemmatization                  |
| JSON               | Storage of training data (intents and responses)                     |
| Pickle             | Saving trained models and preprocessed data                          |

---

## 📌 Key Features

* 🎯 **Intent Classification** using Deep Learning (Keras)
* 🧹 **Text Preprocessing** with NLP: Tokenization, Lemmatization, and Bag-of-Words
* 💬 **Contextual Responses**: Answers based on identified intent
* 🔁 **Easily Extendable**: Add more intents/responses via the `intents.json` file
* 💡 **Lightweight**: Simple to run locally or host on a server
* 🌐 **Frontend Ready**: Can be easily integrated into a website or messaging platform

---

## 🧪 How It Works

### 1️⃣ Data Preparation (NLP Pipeline)

* **Intent Structure**: Defined in `intents.json`

  ```json
  {
    "intents": [
      {
        "tag": "admission_deadline",
        "patterns": ["What is the last date to apply?", "When is the deadline?"],
        "responses": ["The application deadline is July 31st."]
      },
      ...
    ]
  }
  ```

* **Text Processing**:

  * **Tokenization**: `nltk.word_tokenize()` splits sentences into words
  * **Lemmatization**: `WordNetLemmatizer()` reduces words to root form
  * **Bag-of-Words**: Transforms words into numerical vectors representing presence/absence of known vocabulary terms

* **Saving Artifacts**: Vocabulary, classes, and training data are saved using `pickle`

---

### 2️⃣ Model Training (Deep Learning)

* **Model Type**: `Sequential` model (Keras)
* **Input**: Bag-of-Words vector
* **Hidden Layers**: Dense + Dropout layers for learning patterns and avoiding overfitting
* **Output Layer**: Softmax for multi-class classification (predict intent tag)
* **Loss Function**: `categorical_crossentropy`
* **Optimizer**: `SGD` with momentum for stable convergence

---

### 3️⃣ Response Generation

* **User input** is processed into a BoW vector
* **Model** predicts the best matching intent
* **Response** is randomly selected from the responses tied to that intent
* **Chat Interface** (CLI or connected UI) returns the response

## 📁 Project Structure

```
admission-counselor-chatbot/
│
├── intents.json              # All user intents, patterns, and responses
├── train_chatbot.py          # Script for preprocessing and training
├── chatbot.py                # Script to run the chatbot interaction
├── chatbot_model.h5          # Trained Keras model (saved)
├── words.pkl                 # Pickled vocabulary list
├── classes.pkl               # Pickled class labels
└── README.md                 # Project documentation
```

---

## 🚀 Future Improvements

* 💬 Integrate with **WhatsApp**, **Telegram**, or **Web Chat UI**
* 🧠 Replace basic model with **transformer-based models** (e.g., BERT) for better contextual understanding
* 🗂 Add **user context memory** for more interactive conversations
* 🔐 Integrate secure backend to fetch real-time admission data from a database
* 🌍 Support **multi-language conversations**

---

## 🤝 Contribution

If you'd like to contribute:

* Fork the repository
* Add your intents or improvements
* Submit a pull request

