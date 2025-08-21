# Domain-Specific Web Scraper & NLP Analysis for Professional Wrestling

This project demonstrates a complete pipeline for domain-specific data collection and Natural Language Processing (NLP). It scrapes data for 320 professional wrestling documents from Wikipedia, processes the text, and performs analysis to identify key terms and themes within the professional wrestling domain.

## Project Overview

The primary goal of this project is to build a domain-specific corpus from a niche topic (professional wrestling) and then analyze it to extract meaningful insights. The notebook handles everything from data collection and cleaning to advanced NLP techniques like tokenization, lemmatization, stemming, and term frequency analysis.

### Key Features
*   **Web Scraping**: Collects content from hundreds of wrestler profiles on Wikipedia using `requests` and `BeautifulSoup`.
*   **Text Preprocessing**: Cleans and prepares the text data for analysis using `nltk`.
*   **NLP Analysis**: Applies tokenization, lemmatization, and stemming to create a structured dataset.
*   **Term Specificity**: Calculates a specificity score to identify terms that are highly relevant to the wrestling domain.
*   **Frequency Analysis**: Identifies the most frequently used terms in the corpus.

## Methodology

### 1. Data Collection
The scraper starts with the Wikipedia category for "American male professional wrestlers" and iteratively collects the individual pages of each wrestler listed. For this run, a total of 320 documents were successfully scraped.

### 2. Text Processing & NLP
Once the raw HTML content is collected, the following NLP pipeline is applied using the `nltk` library:
*   **Tokenization**: Text is broken down into individual words or tokens.
*   **Stopword Removal**: Common English words (e.g., "the," "is," "a") are removed to reduce noise.
*   **Lemmatization**: Words are reduced to their base or dictionary form (e.g., "wrestled" becomes "wrestle").
*   **Stemming**: Words are reduced to their root form (e.g., "champions" becomes "champion").

### 3. Analysis and Results
The processed data is analyzed to determine term specificity and frequency.

**Top Terms by Specificity Score:**
This table shows terms that are most unique and important to the wrestling domain.
| Term | Specificity Score |
| :--- | :--- |
| wrestling | 11631.98 |
| heavyweight | 9905.89 |
| nwa | 7054.62 |
| wwe | 6043.69 |
| wrestler | 5708.79 |

**Top Terms by Frequency:**
This table highlights the most commonly used words across all scraped documents.
| Term | Frequency |
| :--- | :--- |
| championship| 9520 |
| wrestling | 7433 |
| team | 5973 |
| match | 5619 |
| tag | 5115 |

## How to Use

### Installation
You can install the required Python libraries using pip:
```bash
pip install requests beautifulsoup4 pandas nltk seaborn tqdm lxml
```

### Running the Project
1.  Clone the repository to your local machine.
2.  Open and run the Jupyter Notebook `wrestle scrape.ipynb` to execute the entire scraping and analysis pipeline.

## Dependencies
This project relies on the following Python libraries:
*   `requests`: For making HTTP requests to Wikipedia.
*   `beautifulsoup4`: For parsing HTML and extracting content.
*   `pandas`: For data manipulation and creating dataframes.
*   `nltk`: The core library for NLP tasks.
*   `tqdm`: For displaying progress bars.
*   `lxml`: As an efficient XML and HTML parser.

