# Text-Analyzer-Pipeline 🚀

A web-based Text Analyzer built with **Python** and **Flask** that processes text to find the most frequently used words. This project was developed to demonstrate the **Pipe and Filter Architectural Style** for a Software Design and Architecture (SDA) lab project.

It works completely offline and does not rely on any external APIs.

## 📖 What does this project do?
The Text Analyzer allows users to paste any length of text and instantly see a bar chart of the top 10 most used words. 
It is highly useful for:
- **Students:** Finding the main topic of a long document.
- **Teachers:** Checking the vocabulary used in assignments.
- **SEO/Writers:** Analyzing keyword density in articles.

## 🏗️ Architecture: Pipe and Filter
This system is designed using the **Pipe and Filter** architecture pattern. 
- **Filter:** A standalone component that performs a single specific task on the data.
- **Pipe:** The connector that passes data from one filter to the next.

Because each filter is independent, the data moves in a unidirectional flow, changing state at every step. This makes the system highly modular—you can easily add, remove, or bypass a filter without breaking the application.

## ⚙️ The Four Filters
The text processing pipeline consists of the following sequential steps:

1. **Get Input Filter:** 
   - *Input:* Raw text from the user.
   - *Action:* Strips leading and trailing white spaces.
   - *Output:* Clean raw text.

2. **Clean + Tokenize Filter:** 
   - *Input:* Clean raw text.
   - *Action:* Converts text to lowercase, removes punctuation (dots, commas), and splits sentences into an array of individual words.
   - *Output:* List of words.

3. **Remove Stopwords Filter (Toggleable):** 
   - *Input:* List of words.
   - *Action:* Removes common, unhelpful words (e.g., 'the', 'is', 'a', 'on').
   - *Output:* List of meaningful words.

4. **Count Words Filter (Toggleable):** 
   - *Input:* List of meaningful words.
   - *Action:* Calculates the frequency of each word and sorts them to find the top 10.
   - *Output:* Dictionary/JSON of top words and their counts.

## ✨ Key Features
- **Filter Toggling:** Users can dynamically turn the Stopwords and Counting filters on or off from the UI to see how the data flow changes.
- **Visual Output:** Results are displayed in a clean Bar Chart.
- **Independent Modules:** Shows true decoupling in software design.

## 💻 Technologies Used
- **Backend:** Python 3, Flask
- **Frontend:** HTML, CSS, JavaScript

## 🚀 How to Run Locally

1. **Install requirements:**
   ```bash
   pip install -r requirements.txt
Run the Flask application:

Bash
python app.py
Open in Browser:
Navigate to http://127.0.0.1:5000

👨‍💻 Author
Umair Saleem
Software Engineering Student at UET Lahore (New Campus)
