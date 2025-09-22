Submitted by: Sairaj Pattnaik
 Task: Web Scraping + NLP Text Analysis
 Tools: Python 3, BeautifulSoup, spaCy, pandas

--------------------------------------------------------
 OBJECTIVE:
--------------------------------------------------------
1. Extract article title and main text from URLs listed in Input.xlsx
2. Save each article as a separate .txt file (using URL_ID)
3. Perform NLP analysis on each file:
   - Positive/Negative word counts
   - Polarity & Subjectivity Score
   - Sentence length, FOG Index, Word Count, etc.
4. Export results to an Excel file in the format given in Output Data Structure.xlsx

--------------------------------------------------------
 FOLDER STRUCTURE:
--------------------------------------------------------

- Input.xlsx
- StopWords/
    └── (all stopword .txt files)
- MasterDictionary/
    └── positive-words.txt
    └── negative-words.txt
- extracted_articles/
    └── (Generated .txt files for each article)
- Blackcoffer_Final_Output.xlsx
- script.py
- README.txt

--------------------------------------------------------
 HOW TO RUN THE SCRIPT:
--------------------------------------------------------

1. Make sure Python 3 is installed.
2. Install required libraries:

   pip install pandas requests beautifulsoup4 spacy openpyxl

3. Download spaCy model (only once):

   python -m spacy download en_core_web_sm

4. Run the script:

   python blackcoffer_analysis.py

Output will be saved as: **Blackcoffer_Final_Output.xlsx**

--------------------------------------------------------
 REPORT: MY APPROACH & EXPERIENCE
--------------------------------------------------------

 1. Article Extraction:
- I used BeautifulSoup to scrape article titles and body paragraphs.
- Each article is saved as a `.txt` file using its URL_ID.

 2. NLP Analysis:
- For each file, I calculated various text metrics like:
  - Sentiment scores
  - Readability (FOG Index)
  - Word complexity and structure
- I used `spaCy` for tokenizing sentences and words (instead of NLTK).

--------------------------------------------------------
 CHALLENGES I FACED:
--------------------------------------------------------

 1. NLTK Error (`punkt_tab` not found):
- Tried to manually fix it but it kept showing errors.
-  Solution: Replaced NLTK with spaCy — it worked smoothly.

 2. Stopwords & Word Lists:
- I learned how to manually read `.txt` files into Python for stopwords and sentiment words.

 3. File I/O (Excel & Text):
- As I had only done file handling in C++ earlier, I used the **internet** to learn how to read/write `.xlsx` files using `pandas`.

--------------------------------------------------------
 HOW I LEARNED NLP:
--------------------------------------------------------

Since I was new to NLP, I referred to:
- [spaCy documentation](https://spacy.io/usage/spacy-101)
- YouTube tutorials on "Text Analysis in Python"
- Stack Overflow for Python logic like regex, syllables, and loops

This project really helped me understand how to apply NLP techniques to real-world articles.

--------------------------------------------------------
 CONCLUSION:
--------------------------------------------------------

Through this assignment, I got hands-on experience with:
- Web scraping in Python
- Working with real text data
- Calculating text sentiment & readability
- Using dictionaries and custom stopwords
- Exporting data to Excel

This project was a great learning experience and I’m excited to apply these skills to more projects ahead.

--------------------------------------------------------
THANK YOU! 
--------------------------------------------------------
