# Outreach CLI Tool

A Selenium + BeautifulSoup powered crawler for discovering and scraping contact information (emails, names, and industry buzzwords / seo keywords ) from organizational websites.  

DISCLAIMER: Please don't use this to be a spammer... Find organic connections!

---

🚀 What It Does  

- Starts from one or more seed websites.  

- Crawls outward to discover new pages.  

- Collects links that look like contact directories or team listings (for example, pages with “contact”, “team”, “people”, “staff”, “directory”, or “about-us” in the URL).  

- Extracts details such as:  

  - Email addresses  

  - Names (where available)  

  - Industry buzzwords / seo keywords 

  - Saves results into a clean Excel file for easy use.  

- Includes resume functionality, so you can safely stop and restart the process without losing progress.  

---

🛠️ Setup  

- It is strongly recommended to use a Python virtual environment when running this project.  

- This keeps dependencies isolated and avoids version conflicts across projects.  

- Once the environment is created and activated, install the dependencies:  

---

📋 Requirements  

Before running the scraper, make sure you have the following set up:  

- Python 3.9+ (tested up to Python 3.13)  

- Google Chrome installed on your system  

- Virtual environment (recommended to keep dependencies isolated)  

Python libraries needed:  

- selenium – for automated browsing  

- webdriver-manager – to automatically download the correct ChromeDriver version  

- beautifulsoup4 – for parsing page content  

- openpyxl – for saving results to Excel  

- requests – for handling web requests  

- pandas (optional, but useful if you want to do post-processing)  

---

⚙️ How to Run  

- Define the seed websites you want to start crawling from inside the script. (SEED_URLS =)

- Adjust the URL_KEYWORDS = ["contact", "team", "people", "staff", "directory", "about-us"] as per your needs.

- Install the required packages.  

- Start the program with Python.  

---

⏸️ Resume Functionality (Highly Recommended)  

This scraper saves its progress to a file. If you stop the program with Ctrl+C, it will store the list of pages already visited and any contacts found so far. When you restart, the crawler will resume from the saved state, instead of starting over.  

--- This feature is not just convenient but it is recommended for safety. Sending too many requests to a site in one go can trigger rate-limiting or even temporary IP blocking.  ---- 

By using the resume functionality, you can:  

- Break long crawls into smaller sessions.  

- Spread requests out over time. You can even get the program to sleep or wait between requests for this purpose.  

- It protects your IP address from getting blocked by the server.  

- Avoid overwhelming websites with too many requests and attracting suspicion.  

In practice:  

- Run the scraper for a while.  

- Stop it safely with Ctrl+C.  

- Resume later, picking up where you left off.  

---

📂 Output  

All scraped contacts are stored in an Excel spreadsheet.  

Each row includes:  

- The page URL where contact info was found.  

- Emails detected.  

- Names found (where identifiable).  

- Industry buzzwords / seo keywords 

---

⚠️ Notes  

- Always run inside a virtual environment.  

- Chrome runs in headless mode by default, so you won’t see a browser window.  

  Comment out the headless mode if you want to see your screen.  

  Sometimes, this helps Selenium work better(??).  

- The crawler includes random short delays between requests, but you should still use the resume functionality to avoid flooding websites.  

- If Chrome updates on your machine, the correct driver is automatically downloaded.  
