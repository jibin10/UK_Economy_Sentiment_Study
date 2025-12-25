# UK Economy Sentiment Study (News + Social Media)

This project explores how the UK economy is discussed in **news articles** and **social media posts**. It collects text, cleans it, and runs basic text analysis to compare themes and sentiment across sources.

The work is organised as a single Jupyter Notebook (`UK_Economy_Sentiment_Study.ipynb`) with a clear step-by-step flow.

---

## What this project does

- Collects UK economy–related text from:
  - News websites (web scraping)
  - Reddit and Twitter/X (API-based collection)
- Cleans and normalises text (remove noise, tokenize, stopwords, etc.)
- Builds simple word statistics (most frequent words and visual summaries)
- Runs sentiment analysis on:
  - News data
  - Social media data
  - A combined comparison view

> Note: The notebook focuses on the analysis process. It is designed for learning and academic use.

---

## Data sources

### News
News content is collected from multiple publishers (examples in the notebook include BBC, Sky News, and The Guardian). Links may be stored first and then article text is extracted.

**Scraping permission note:** Permission to scrape the news portals was obtained by directly contacting the news agencies by email. Because of this, the collected news dataset cannot be shared publicly in this repository.

### Social Media
- Reddit: posts/comments are fetched using Reddit’s API flow
- Twitter/X: recent-search endpoint is used with a bearer token

---

## Project structure (expected folders)

The notebook reads/writes datasets using paths like these:

- `data/links/`  
  Stores link lists used for scraping (example: source link CSV files)

- `data/news/` and `data/news/clean/`  
  Raw scraped news + cleaned combined news dataset

- `data/social_media/clean/`  
  Cleaned Reddit and Twitter/X datasets

- `data/stable_news/` and `data/stable_sm/`  
  “Stable” (saved) copies that can be used if scraping/API collection is not run

If these folders do not exist, create them before running the notebook cells that save outputs.

---

## How to run

1. Open the notebook:
   - `Mid-term-assignment.ipynb`

2. Run cells in order (top to bottom).

3. Choose one of these approaches:
   - **Option A (recommended for quick run):** Use the existing “stable” datasets and run cleaning + analysis sections.
   - **Option B:** Run data collection first (scraping + APIs), then run cleaning + analysis.

---

## API keys and credentials (important)

This project requires API access for Reddit and Twitter/X if data collection is enabled.

- Store keys/tokens securely (environment variables or a local config file).
- Do **not** hardcode credentials in the notebook.
- Do **not** commit credentials to GitHub.

Suggested environment variables:
- `BEARER_TOKEN` (Twitter/X)

For Reddit, use a secure method to provide:
- client id / client secret
- username / password (if using password-based OAuth flow)
- user agent

---

## Notes on web scraping and usage

- Always follow each website’s terms of service and robots rules.
- Scraping can break if website HTML changes.
- The notebook includes an ethics/copyright section; keep usage limited to non-commercial learning and research.

---

## Output files

Depending on which parts are run, the notebook produces:
- cleaned CSV files for news and social media
- combined cleaned datasets for comparison analysis

Exact file names and locations are clearly shown in the notebook cells that save outputs.

---

## Limitations

- Results depend heavily on what data is collected (time period, query wording, platform filters).
- Social media text can be noisy, biased, and not representative of the full population.
- Sentiment tools can misread sarcasm, slang, and context.

---

## Disclaimer

This project is for educational and research purposes only. It does not provide financial advice and should not be used to make investment or policy decisions.
