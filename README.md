<a href="https://colab.research.google.com/github/ProfByRnV/github-issue-triage-ml/blob/main/issue_triage_ml.ipynb" target="_parent"><img src="https://colab.research.google.com/assets/colab-badge.svg" alt="Open In Colab"/></a>
# 🚀 IssueTriage ML

An end-to-end Natural Language Processing (NLP) project that automates the triage of GitHub issues. 

Open-source maintainers and engineering teams spend countless hours manually reading and tagging incoming issues. **IssueTriage ML** solves this bottleneck by scraping live repository data, cleaning the raw text, and using machine learning to instantly predict whether an issue is a **Bug**, **Enhancement**, or **Documentation** request.

## 🧠 The Architecture

1. **Data Ingestion:** Uses the GitHub REST API to scrape and construct a perfectly balanced dataset of closed issues from major repositories (e.g., `scikit-learn`).
2. **Text Processing Pipeline:** Cleans messy developer text using Regular Expressions and `nltk`. Automatically strips out markdown formatting, python code blocks, URLs, and standard English stopwords.
3. **Feature Engineering:** Converts raw text into a mathematical matrix using Term Frequency-Inverse Document Frequency (TF-IDF).
4. **Classification Engine:** Uses a heavily optimized Logistic Regression model (`scikit-learn`) to predict labels and calculate confidence scores.

## 📊 Results

The model achieves an **88% overall accuracy** on unseen test data, demonstrating strong capability in handling subjective human language and ambiguous technical requests.

* **Precision on Documentation:** 96%
* **Precision on Bugs:** 91%
* **Recall on Enhancements:** 92%

## 🛠️ Tech Stack

* **Language:** Python
* **Data Manipulation:** Pandas
* **Natural Language Processing:** NLTK, Regular Expressions (re)
* **Machine Learning:** Scikit-Learn (TF-IDF Vectorizer, Logistic Regression)
* **Environment:** Google Colab / Jupyter Notebook

## 💻 How to Run (Quickstart)

1. Open the `IssueTriage_ML.ipynb` file in this repository.
2. Click the **"Open in Colab"** button at the top of the file (or upload the file directly to your Google Colab workspace).
3. Run the cells sequentially. The environment will automatically handle library installations, scrape fresh data via the GitHub API, train the model, and launch the inference tool.

## 🔮 Future Roadmap
* Expand the classifier to identify subjective tags like `good first issue` or `help wanted`.
* Deploy the inference function as a lightweight FastAPI endpoint.
* Integrate directly via GitHub Webhooks to auto-label issues the moment they are submitted.
