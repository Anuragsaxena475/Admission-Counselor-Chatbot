🎓 Admission Counselor Chatbot 🤖

This project is an AI-powered Admission Counselor Chatbot designed to assist students during the college admission process. It can answer common questions, provide relevant information, and reduce the workload on admission staff by handling repetitive queries.

🧠 Technologies Used
Python

TensorFlow / Keras (Deep Learning)

NLTK (Natural Language Processing)

Pickle (for saving preprocessed data)

JSON (for storing intent data)

📌 Key Features
Understands and classifies user questions using Deep Learning

Cleans and preprocesses text using NLP

Provides predefined responses based on intent classification

Can be extended with more intents and responses

Lightweight and easy to integrate with any frontend

🧪 How It Works
1. Natural Language Processing (NLP)
Used during data preparation:

Tokenization: Breaks sentences into words using nltk.word_tokenize()

Lemmatization: Converts words to their base form with WordNetLemmatizer

Bag of Words: Converts text to vectors representing word presence

These steps turn user input into a format understandable by the neural network.

2. Deep Learning Model
A Sequential model built with Keras

Input: Bag-of-words vector from NLP preprocessing

Output: Predicted intent (e.g., "admission_deadline", "course_info")

Trained using categorical_crossentropy loss and SGD optimizer

💡 Future Improvements
Integrate with a web-based UI or WhatsApp

Add more personalized conversation flow

Use transformer models for more complex understanding

