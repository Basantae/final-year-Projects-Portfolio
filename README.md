# Final Year Computing Portfolio

BSc (Hons) Computing (BIT), London Metropolitan University — via Informatics College Pokhara
Bashanta Rokaha

This repository holds the projects I built in my final year: a full-stack healthcare booking platform (final year project), a machine learning model, a database-driven web app, and a desktop application. Each one was built from scratch — requirements, design, implementation, testing, documentation.

I'm sharing this as a working portfolio, not a coursework dump. If you're a recruiter or engineer skimming this, the table below gets you oriented in under a minute.

---

## Table of Contents

- [Projects at a Glance](#projects-at-a-glance)
- [SmartCare — Final Year Project](#smartcare--final-year-project)
- [Heart Disease Prediction — Machine Learning](#heart-disease-prediction--machine-learning)
- [Kumari Cinemas — Database & Web](#kumari-cinemas--database--web)
- [Journal App — Desktop Application](#journal-app--desktop-application)
- [Career Development Work](#career-development-work)
- [Skills](#skills)
- [How I Work](#how-i-work)
- [Lessons Learned](#lessons-learned)
- [What's Next](#whats-next)
- [Running These Projects](#running-these-projects)
- [Contact](#contact)

---

## Projects at a Glance

| Project | Type | Stack | One-liner |
|---|---|---|---|
| [SmartCare](#smartcare--final-year-project) | Final Year Project | MERN, JWT, Cloudinary, Khalti/eSewa | Doctor appointment booking platform for Nepal, with AI-assisted patient support |
| [Heart Disease Prediction](#heart-disease-prediction--machine-learning) | AI/ML Coursework | Python, scikit-learn, pandas | Predicts heart disease risk from clinical data, compares 5 ML models |
| [Kumari Cinemas](#kumari-cinemas--database--web) | CC6012 — Data & Web Development | ASP.NET, Oracle SQL | Cinema management system with normalized relational DB |
| [Journal App](#journal-app--desktop-application) | CS6004NP — Application Development | C#, .NET MAUI Blazor Hybrid | Cross-platform journaling app with mood tracking and PDF export |
| [Career Development Work](#career-development-work) | Industry Exposure | React, Tailwind, GSAP | Client portfolio sites and internship-style project work |

Each folder has its own README with setup instructions, screenshots, and architecture notes.

---

## SmartCare — Final Year Project

A full-stack appointment booking platform built to fix a real problem: booking a doctor's appointment in Nepal usually still means a phone call or a physical queue. SmartCare moves that online, with separate portals for patients, doctors, and admins.

**Architecture**

```
React (Vite) frontend
        │
Express REST API
        │
Node.js business logic
        │
MongoDB Atlas
        │
Cloudinary · JWT · Khalti/eSewa · Groq API
```

**What it does**

- Patients: search doctors, book/reschedule/cancel appointments, track queue position, pay online, view history
- Doctors: manage availability, leave, appointments, and private clinical notes; view earnings
- Admins: manage doctors and users, view revenue and appointment analytics
- An AI chatbot (Groq API) handles common patient questions and FAQs
- Auth is JWT-based with role-based route protection; passwords are hashed

**Stack**: React, Vite, Tailwind CSS, Node.js, Express, MongoDB Atlas, JWT, Cloudinary, Khalti, eSewa, Groq API

**Why it's the centerpiece**: it's the only project here that combines auth, payments, real-time-ish scheduling logic, role-based dashboards, and an AI feature in one system — closest to what a production SaaS actually looks like.

`/smartcare-fyp` — full README, screenshots, and setup instructions inside.

---

## Heart Disease Prediction — Machine Learning

A supervised learning project predicting heart disease risk from patient clinical data.

**Workflow**: data cleaning → feature engineering → visualization → training 5 models → comparison → evaluation → a simple prediction interface.

**Models compared**: Logistic Regression, Decision Tree, Random Forest, SVM, K-Nearest Neighbors — evaluated on accuracy and ROC curves, with feature importance analysis to see which clinical indicators mattered most.

**Stack**: Python, pandas, NumPy, scikit-learn, Matplotlib, Seaborn

`/ai-heart-disease` — notebook, dataset, and results inside.

---

## Kumari Cinemas — Database & Web

A cinema management system for the CC6012 (Data and Web Development) module, focused on relational database design as much as the web layer.

**Covers**: film, auditorium, and customer management, ticket booking, occupancy reports.

**Database work**: ER modelling, normalization to 3NF, constrained schema with foreign keys, and hand-written SQL for all CRUD operations rather than relying on an ORM — the point of the module was understanding the database layer directly.

**Stack**: ASP.NET, Oracle SQL

`/kumari-cinemas` — ER diagrams, SQL scripts, and screenshots inside.

---

## Journal App — Desktop Application

A cross-platform journaling app for the CS6004NP (Application Development) module, built with .NET MAUI Blazor Hybrid.

**Features**: PIN-protected login, daily entries, mood tracking, search and filtering, PDF export, a stats dashboard, and theme switching.

**Stack**: C#, .NET MAUI Blazor Hybrid

`/journal-app` — screenshots and setup instructions inside.

---

## Career Development Work

Alongside coursework, I built and shipped client-facing work: single-page portfolio sites using Three.js and GSAP, deployed on Netlify, plus early exploration into workflow automation with n8n. This folder documents that side of the work — client communication, Figma-to-code handoff, and shipping to a real deadline rather than a grading rubric.

`/career-development` — case studies and links inside.

---

## Skills

**Languages**: JavaScript, Python, C#, SQL, HTML/CSS

**Frontend**: React, Tailwind CSS, Bootstrap, Blazor

**Backend**: Node.js, Express, REST APIs

**Databases**: MongoDB, Oracle SQL, SQL Server

**Machine Learning**: scikit-learn, pandas, NumPy, model evaluation, feature engineering

**Engineering practices**: JWT auth, MVC, ER modelling, UML, requirement analysis, Agile workflow, unit/black-box/white-box testing

**Tools**: Git, GitHub, VS Code, Visual Studio, Postman, Figma, Cloudinary, Netlify

---

## How I Work

Every project in this repo went through the same loop: requirements and wireframes first, then an ER or system diagram before touching code, then build in small testable pieces, then document as I go rather than after the fact. Version control was used from day one on all projects, not bolted on at submission time.

---

## Lessons Learned

Writing the code turned out to be the smaller part of each project. Planning, database design, and testing consistently took as much time as implementation — and skipping any of them showed up later as rework.

Building SmartCare's role-based dashboards taught me more about authentication and authorization edge cases than any tutorial did — specifically, how much harder it is to get permissions right across three different user roles than to get a single login flow working.

The ML project changed how I think about "improving a model." Early on I assumed better results meant trying a fancier algorithm. In practice, cleaning the data and picking better features moved accuracy more than switching models did.

Kumari Cinemas made database normalization concrete rather than theoretical — I hit real anomalies from a badly designed schema before fixing it to 3NF, which made the "why" behind normalization actually stick.

---

## What's Next

- Add Docker support and a basic CI/CD pipeline (GitHub Actions) to SmartCare
- Write automated tests for the SmartCare API (currently manually tested via Postman)
- Document the SmartCare API with Swagger
- Deploy SmartCare to a live environment instead of local-only
- Expand the ML project with a couple more datasets to check the models generalize

---

## Running These Projects

Clone the repo:

```bash
git clone https://github.com/Basantae/REPOSITORY_NAME.git
```

Each project is self-contained with its own setup steps — go into the folder and follow its README:

```bash
cd smartcare-fyp
```

---

## Contact

**Bashanta Rokaha**

- Portfolio: https://bashantarokaha.com.np
- GitHub: https://github.com/Basantae
- LinkedIn: https://www.linkedin.com/in/bashanta-rokaha-4a266633b/
- Instagram (Innovate Upward): [@yorkerr.07](https://instagram.com/yorkerr.07)
- Email: rokhabasasnta0@gmail.com
