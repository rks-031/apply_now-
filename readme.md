## ApplyNow - You application SideKick

This tool will automatically scan job postings from various platforms (like LinkedIn, Naukri, Indeed) and apply for relevant jobs based on your preferences.

## Tech Stack

1. Frontend: React (Vite setup)
2. Backend: Node.js with Express
3. Database: MongoDB (to store job preferences, logs, and applied jobs)
4. Browser Automation: Puppeteer / Selenium (to interact with job sites)
5. Scheduler: Node.js cron jobs (to run scripts periodically)
6. Scraping Jobs: Cheerio / Axios (to fetch job listings from websites)

## Features

1. Job Preferences Input:

User provides keywords, locations, roles, experience levels, etc., through a React-based form.
Preferences are saved to MongoDB.

2. Job Scraping:

Use Puppeteer or Cheerio to scrape job listings from supported sites.
Filter jobs based on user preferences.

3. Automated Application Process:

Use Puppeteer to fill forms and submit resumes/CVs.
Store applied job details to avoid duplicate applications.

4. Dashboard (React):

View all jobs scraped, applications sent, and pending ones.
Option to manually intervene in case of issues (e.g., CAPTCHA).


5. Logs and Notifications:

Notify via email (Nodemailer) when an application is successful.
Keep logs of failed applications (for debugging).

6. Scheduler:

Use cron jobs to run scripts at regular intervals (daily/hourly).

7. Security Considerations:

Store passwords safely using environment variables and encryption.
Handle anti-bot measures (like CAPTCHA) gracefully.


## Folder Structure

```bash
project/
│
├── client/                # React (Vite setup) for the frontend
│   ├── src/
│   │   ├── components/
│   │   │   └── JobPreferencesForm.jsx
│   │   │   └── Dashboard.jsx
│   │   └── App.jsx
│   └── package.json
│
├── server/                # Node.js backend
│   ├── config/
│   │   └── db.js          # MongoDB connection logic
│   ├── routes/
│   │   └── jobs.js        # Routes to handle job scraping and application
│   ├── scripts/
│   │   └── scraper.js     # Puppeteer / Cheerio scraping logic
│   │   └── apply.js       # Automates job applications
│   ├── app.js             # Express server setup
│   └── package.json
│
├── .env                   # API keys, login credentials
└── README.md
```


