# 📚 BookScraper INR

A high-throughput web scraper that crawls all 50 pages of [books.toscrape.com](https://books.toscrape.com), extracts pricing and rating data, converts GBP → INR on the fly, and ships it straight to CSV.

## What It Does
- Crawls 1,000 book listings across 50 paginated catalogue pages
- Extracts **title, price, star rating, and stock availability**
- Converts GBP pricing to INR at a configurable exchange rate
- Cleans encoding artifacts (currency symbols, stray bytes) for pristine output
- Outputs a ready-to-use `books_data_inr.csv`

## Tech Stack
`Python` · `Requests` · `BeautifulSoup4` · `CSV`

## Run It
```bash
pip install requests beautifulsoup4
python scraper.py
```

Output: `books_data_inr.csv` with columns `Title | Price (₹) | Rating | Availability`

## Why It's Solid
- Fails gracefully — skips broken pages instead of crashing the whole run
- Real-time terminal feedback for every scraped record
- Zero external config — runs end-to-end out of the box

## Roadmap
- [ ] Async requests for faster crawling
- [ ] Live exchange rate API integration
- [ ] Export to JSON / database sink

---
*One command. One thousand books. One clean CSV.*
