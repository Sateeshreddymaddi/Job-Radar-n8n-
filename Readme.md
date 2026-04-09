# 📡 Job Radar — Live Job Opportunity Tracker

A modern, real-time job tracking dashboard that fetches and visualizes job opportunities directly from Google Sheets. Built with pure HTML, CSS, and JavaScript — no frameworks required.

---

## 🚀 Features

* 🔄 **Live Job Feed** (auto-refresh every 6 hours)
* ⚙️ **Automated Data Pipeline via n8n**
* 📊 **Real-time Stats Dashboard**
* 🔍 **Search & Filter Jobs**
* 📈 **Score-based Ranking System (1–10)**
* 🧠 **Smart Match Reason Display**
* ⚡ **Fast & Lightweight (No Backend Required)**
* 🌐 **Google Sheets Integration (CSV)**

---

## 🖼️ Preview

> Add screenshots or GIFs here (recommended for GitHub)

---

## 🏗️ Tech Stack

* HTML5
* CSS3 (Modern UI + Animations)
* Vanilla JavaScript
* Google Sheets (as Database)

---

## 📂 Project Structure

```
job-radar/
│── index.html   # Main application file
│── README.md    # Documentation
```

---

## ⚙️ Data Pipeline (n8n Integration)

This project uses **n8n workflow automation** to continuously fetch and update job data.

### 🔁 Workflow Overview

1. n8n scrapes job listings (LinkedIn, job portals, etc.)
2. Filters jobs (e.g., last 72 hours, relevant roles)
3. Processes & scores jobs
4. Automatically updates Google Sheets
5. Frontend fetches updated data from the sheet (CSV)

### ⚡ Benefits

* Fully automated job updates
* No manual data entry required
* Real-time sync between backend automation and UI

---

## ⚙️ Setup Instructions

### 1. Clone the Repository

```bash
git clone https://github.com/your-username/job-radar.git
cd job-radar
```

---

### 2. Setup Google Sheets

1. Create a Google Sheet
2. Add the following columns:

```
job_title, company, location, posted_date, application_count, score, reason, job_url
```

3. Go to:

```
File → Share → Publish to Web
```

4. Select:

* Format: CSV
* Sheet: Your sheet

5. Copy the generated CSV URL

---

### 3. Update CSV URL

In `index.html`, replace:

```js
const CSV_URL = 'YOUR_GOOGLE_SHEET_CSV_URL';
```

---

### 4. Run the Project

Just open the file in your browser:

```bash
open index.html
```

---

## 📊 Data Format Example

| job_title          | company | location  | posted_date | application_count | score | reason             | job_url     |
| ------------------ | ------- | --------- | ----------- | ----------------- | ----- | ------------------ | ----------- |
| Frontend Developer | Google  | Hyderabad | 2026-04-01  | 120               | 9     | Strong React match | https://... |

---

## 🧠 Scoring System

| Score Range | Meaning      |
| ----------- | ------------ |
| 8 – 10      | 🔥 Top Match |
| 5 – 7       | ⚡ Mid Match  |
| 1 – 4       | ⚠️ Low Match |

---

## 🔍 Features Breakdown

### 🔎 Search

* Search by job title, company, or location

### 🎯 Filters

* High Match (8–10)
* Mid Match (5–7)
* Low Match (1–4)

### 🔃 Sorting

* Sort by Score
* Sort by Date

---

## 📡 Auto Refresh

The app automatically refreshes data every:

```
6 hours
```

Manual refresh button also available.

---

## ❗ Troubleshooting

### Data not loading?

* Ensure Google Sheet is **Published to Web**
* Ensure sharing is set to:

```
Anyone with the link can view
```

---

## 🌟 Future Improvements

* 🔐 Authentication (Admin Dashboard)
* 🤖 AI-based job scoring
* 📩 Email notifications
* 📱 Mobile optimization improvements
* 🧾 Export to CSV/JSON

---

## 🤝 Contributing

Contributions are welcome!

1. Fork the repo
2. Create a new branch
3. Commit changes
4. Submit a PR

---

## 📜 License

MIT License — Free to use and modify.

---

## 👨‍💻 Author

**Sateesh Reddy**

---

## ⭐ Support

If you like this project, give it a ⭐ on GitHub!
