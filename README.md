# AI-CHATBOT-WITH-NLP

COMPANY:CODTECH IT SOLUTIONS
NAME:AKSHAY.M
INTERN ID:CT08NEP
DOMAIN:PYTHON
BATCH DURATION:January 15th/2025 to February 15th/2025

## Chatbot Using NLTK and SpaCy

This chatbot application demonstrates a simple rule-based chatbot built using Python, NLTK (Natural Language Toolkit), and SpaCy. It showcases fundamental natural language processing techniques such as tokenization, stopword removal, and text preprocessing to generate conversational responses. Below is a detailed explanation of the code and its functionality.

### Features of the Chatbot
- **Rule-Based Responses**: The chatbot responds based on predefined responses stored in a dictionary.
- **Text Preprocessing**: User input is processed by converting text to lowercase, tokenizing, removing punctuation, and filtering out stopwords.
- **Randomized Responses**: For each input category, the chatbot provides varied responses by selecting them randomly from a list, making conversations more engaging.
- **Customizable Responses**: You can easily expand the chatbot's vocabulary and add more categories and responses.
- **Interactive Chat Loop**: The chatbot runs in an interactive mode where users can converse with it until they type "exit."

### Code Walkthrough

#### 1. **Imports and Setup**
The code starts by importing the necessary libraries:
- `nltk`: For tokenization and stopword handling.
- `spacy`: To load SpaCy's English language model.
- `random`: To randomize responses.

Necessary data for `nltk` (e.g., tokenizer and stopwords) is downloaded to ensure proper functionality.

#### 2. **Predefined Responses**
The chatbot uses a dictionary named `responses` to map keywords to a list of potential responses. For example:
- Input like "hello" triggers responses such as "Hi there!" or "Hello!"
- The "default" category handles inputs that don't match predefined keywords.

#### 3. **Text Preprocessing**
The function `preprocess_text()` prepares user input for analysis:
- Converts text to lowercase.
- Tokenizes the input into words using NLTK's `word_tokenize()`.
- Removes punctuation and non-alphanumeric tokens.
- Filters out common stopwords (e.g., "the," "is," "and") to focus on meaningful words.

#### 4. **Generating a Response**
The `chatbot_response()` function matches the preprocessed user input with keywords in the `responses` dictionary:
- If a keyword is found in the user input, a random response is selected from the associated list.
- If no keyword matches, a random response from the "default" category is returned.

#### 5. **Interactive Chat**
The `chat()` function provides an interactive chat interface:
- Users can type their messages, and the chatbot responds accordingly.
- Typing "exit" ends the conversation.

### Usage
To use the chatbot, follow these steps:
1. Ensure you have Python installed.
2. Install the required libraries using:
   ```bash
   pip install nltk spacy
   ```
3. Download the SpaCy English model:
   ```bash
   python -m spacy download en_core_web_sm
   ```
4. Save the code in a Python file (e.g., `chatbot.py`).
5. Run the chatbot using:
   ```bash
   python chatbot.py
   ```
6. Start chatting! Type your messages and see the chatbot's responses. Type "exit" to end the chat.

### Customization
You can extend the chatbot's functionality by modifying the `responses` dictionary:
- Add new keywords and their respective responses.
- Include more advanced processing, such as using SpaCy for named entity recognition (NER) or dependency parsing.

### Limitations
- **Rule-Based**: The chatbot relies solely on predefined rules, limiting its ability to handle diverse or complex inputs.
- **Basic NLP Techniques**: The use of stopwords and keyword matching is simple and might miss nuanced user intents.

### Future Enhancements
To make the chatbot more sophisticated:
- Implement machine learning-based models for intent recognition.
- Integrate external APIs to fetch dynamic data for responses.
- Add a richer conversational context using NLP libraries like Dialogflow.

This code serves as a great starting point for beginners learning about chatbots and natural language processing.
