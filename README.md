# EcoShift – Carbon Footprint Tracker

**EcoShift** is a full-stack web application that helps individuals track sustainable daily habits, measure their environmental impact, and understand how everyday choices contribute to reducing CO₂ emissions.

The platform transforms sustainability activities into measurable insights through **CO₂ savings calculations, interactive analytics, habit tracking, user profiles, date-based filtering, and exportable reports**.

---

## Challenge Details

### Chosen Vertical

**Environmental Sustainability & Habit Tracking**

---

### Problem

Many people want to adopt sustainable habits but struggle to understand the measurable environmental impact of their everyday actions. EcoShift addresses this gap by converting common sustainable activities into understandable **CO₂ savings metrics**.

---

### Approach & Logic

EcoShift allows users to:

1. Create and manage personal profiles.
2. Select and record sustainable activities.
3. Specify the quantity and date of each activity.
4. Calculate estimated CO₂ savings using predefined emission factors.
5. View individual and community-level environmental impact.
6. Analyze progress through interactive charts.
7. Export collected data and reports for further analysis or presentation.

The backend processes each activity using predefined CO₂ factors and stores the resulting records in a lightweight **SQLite database**.

---

### How the Solution Works

```text
User
  ↓
Create Profile
  ↓
Select Sustainable Habit
  ↓
Log Activity
  ↓
CO₂ Savings Calculation
  ↓
SQLite Database
  ↓
Analytics & Dashboard
  ↓
Reports / CSV / Presentation Data
```

---

### Assumptions

* CO₂ emission factors are based on predefined standard estimates for supported activities.
* Example: avoiding approximately **0.21 kg CO₂ per kilometer** of car travel by choosing cycling instead.
* Users are expected to accurately report their sustainable activities.
* The prototype is designed for a single-server deployment.
* CO₂ savings represent estimated environmental impact rather than laboratory-level measurements.

---

## Key Features

### Sustainable Habit Tracking

Track everyday environmentally friendly activities such as:

* Cycling
* Plant-based meals
* Recycling
* Walking
* Public transportation
* And other configurable sustainability actions

---

### Interactive Impact Dashboard

Monitor important sustainability metrics including:

* Total CO₂ saved
* Total sustainable actions
* Active users
* Average CO₂ savings per person
* Category-wise impact
* Top-performing users
* Impact within a selected date range

---

### Profile Management

Users can:

* Create profiles
* Store basic profile information
* Switch between profiles
* Manage individual sustainability activity records

---

### Activity Logging

Each sustainability activity can include:

* Habit type
* Quantity
* Date
* Optional notes
* Automatically calculated CO₂ savings

---

### Date-Based Analytics

Analyze environmental impact using:

* Custom date ranges
* Quick date selections
* Historical activity records
* Filtered dashboard statistics

---

### Data Visualization

Interactive visualizations powered by **Chart.js** provide a clearer understanding of:

* CO₂ savings trends
* Activity categories
* User performance
* Overall community impact

---

### Export & Reporting

EcoShift provides multiple ways to use the collected data:

* CSV export
* Summary reports
* Individual user reports
* Presentation-ready data
* Stakeholder-oriented insights

---

### Local Storage

Browser local storage is used for:

* Auto-saving form information
* Maintaining user preferences
* Improving the overall user experience

---

## Architecture

EcoShift follows a modular **MVC-inspired architecture** to keep application logic organized and maintainable.

```text
EcoShift
│
├── Frontend
│   ├── HTML
│   ├── CSS / Bootstrap
│   ├── JavaScript
│   └── Chart.js
│
├── Backend
│   ├── Node.js
│   ├── Express.js
│   ├── REST API
│   └── Middleware
│
├── Database
│   └── SQLite
│
└── Configuration
    └── config.json
```

---

### Architectural Principles

* Separation of concerns
* Modular backend organization
* RESTful API design
* Centralized configuration
* Lightweight database architecture
* Maintainable application structure

---

## Security & Reliability

The application incorporates several security-focused practices:

* **Helmet** for HTTP security headers
* **Strict Content Security Policy (CSP)**
* **Express Rate Limit** for request throttling
* **Express Validator** for input validation
* **HPP** for HTTP Parameter Pollution protection
* Request payload limits
* Server-side validation
* Controlled API endpoints

These measures help reduce common web application security risks while keeping the prototype lightweight.

---

## Accessibility

EcoShift is designed with accessibility in mind and follows WCAG-oriented practices including:

* Semantic HTML
* ARIA attributes where required
* Keyboard-friendly interactions
* Accessible form controls
* Readable typography
* Sufficient color contrast
* Approximately **4.5:1 or greater contrast** for standard text where applicable

---

## Tech Stack

| Layer         | Technologies                                       |
| ------------- | -------------------------------------------------- |
| Frontend      | HTML5, CSS3, Bootstrap, JavaScript                 |
| Visualization | Chart.js                                           |
| Backend       | Node.js, Express.js                                |
| Database      | SQLite                                             |
| Utilities     | date-fns, body-parser, CORS                        |
| Security      | Helmet, Express Rate Limit, Express Validator, HPP |
| Configuration | JSON                                               |

---

## 📁 Project Structure

```text
ecoshift-carbon-footprint-tracker/
│
├── .gitignore
├── LICENSE
├── README.md
├── co2_challenge.db
├── config.json
├── package.json
├── package-lock.json
└── server.js
```

The application is structured to support further modularization as the project grows.

---

## Getting Started

### Prerequisites

Make sure the following are installed:

* **Node.js v14 or later**
* **npm**

You can verify your installation with:

```bash
node --version
npm --version
```

### 1. Clone the Repository

```bash
git clone https://github.com/rishav8877/ecoshift-carbon-footprint-tracker.git
```

### 2. Navigate to the Project

```bash
cd ecoshift-carbon-footprint-tracker
```

### 3. Install Dependencies

```bash
npm install
```

### 4. Start the Application

```bash
npm start
```

For development:

```bash
npm run dev
```

### 5. Open the Application

Visit:

```text
http://localhost:3000
```

---

## Application Screenshots

### Landing Page

<img width="984" height="614" alt="Landing Page" src="https://github.com/user-attachments/assets/2c20af64-7cbe-4a8d-a2dd-fc6f98642cd9" />
  
*The landing page introduces EcoShift with key features and a clear call-to-action for users to get started.*

---

### Impact Dashboard

<img width="996" height="501" alt="Impact Dashboard" src="https://github.com/user-attachments/assets/09e04943-9619-4702-ad48-7eadf507de44" />
  
*A summary dashboard displaying total CO₂ saved, active users, total actions, and average savings per person within a selected date range.*

---

### Log Action

<img width="776" height="612" alt="Log Action" src="https://github.com/user-attachments/assets/53334334-166a-450c-a3f7-9d9e1f585e34" />
 
*A form to log sustainable actions with fields for habit selection, date, quantity, and optional notes.*

---

### My Recent Actions

<img width="753" height="416" alt="Log Action (2)" src="https://github.com/user-attachments/assets/b73b73b9-7bc5-4f3d-b27c-10ac54090f30" />
  
*A list of recently logged sustainable actions with details like date, quantity, and CO₂ savings.*

---

### Create Profile

<img width="760" height="527" alt="Create Profile" src="https://github.com/user-attachments/assets/f8f7db40-af7f-4ccc-9ec9-bc6dfedb9f8c" />
  
*A profile creation form for entering user details such as name, email, and internship start date.*

---

### Export & Reporting

<img width="580" height="590" alt="Export   Reporting" src="https://github.com/user-attachments/assets/92903caf-8769-432f-9276-535b3af24537" />
  
*An export and reporting interface offering options to download CSV data, generate summary reports, and prepare presentation-ready insights.*

---

### CSV Export

Provides raw activity data suitable for:

* Microsoft Excel
* Google Sheets
* Data analysis
* Further processing

---

### Summary Report

Provides an executive-level overview containing important sustainability metrics.

---

### Individual Reports

Provides user-specific sustainability progress and activity summaries.

---

### Presentation Data

Generates stakeholder-ready insights that can be used for:

* Demonstrations
* Sustainability presentations
* Project evaluations
* Community reporting

---

## Configuration

Application settings can be managed through:

```text
config.json
```

The configuration system supports settings related to:

* Application themes
* Language preferences
* Date formats
* CO₂ emission factors
* Data retention
* Export formats

---

### Data Retention

Default retention period:

```text
365 days
```

---

### Supported Export Formats

* CSV
* HTML
* PDF

---

## REST API

EcoShift exposes RESTful API endpoints for managing users, habits, activity logs, and dashboard information.

---

### Habits

```http
GET /api/habits
```

---

Retrieve available sustainability habits.

### Users

```http
POST /api/users
GET /api/users
```

Create and retrieve user profiles.

---

### User Habits

```http
POST /api/users/:userId/habits
GET /api/users/:userId/habits
```

Manage habits associated with a specific user.

---

### Activity Logs

```http
POST /api/logs
GET /api/users/:userId/logs
```

Create and retrieve sustainability activity records.

---

### Dashboard

```http
GET /api/dashboard
```

Retrieve aggregated sustainability and CO₂ impact metrics.

---

## CO₂ Impact Calculation

EcoShift uses predefined emission factors to estimate the environmental impact of logged activities.

A simplified calculation can be represented as:

```text
CO₂ Savings = Activity Quantity × CO₂ Saving Factor
```

For example:

```text
Cycling Distance = 10 km
Estimated CO₂ Saving Factor = 0.21 kg/km

Estimated CO₂ Saved = 10 × 0.21
                    = 2.10 kg CO₂
```

These values are estimates intended to make sustainability impact easier to understand and compare.

---

## Community Impact

EcoShift is not limited to individual progress.

By aggregating activity data, the platform can demonstrate collective environmental impact through:

* Total community CO₂ savings
* Combined sustainable actions
* User participation
* Category-level contribution
* Top-performing participants

This helps turn individual sustainable choices into a measurable community-level outcome.

---

## Example User Journey

```text
1. User opens EcoShift
        ↓
2. Creates a profile
        ↓
3. Selects sustainable habits
        ↓
4. Logs daily activities
        ↓
5. Backend calculates CO₂ savings
        ↓
6. Data is stored in SQLite
        ↓
7. Dashboard updates automatically
        ↓
8. User analyzes progress
        ↓
9. Data can be exported as reports
```
---

## Project Goals

EcoShift was developed with the following goals:

* Make environmental impact easier to understand
* Encourage consistent sustainable habits
* Quantify everyday sustainability decisions
* Provide accessible sustainability analytics
* Enable community-level impact tracking
* Make environmental data easy to export and present

---

## Future Enhancements

Potential future improvements include:

* Cloud database integration
* Progressive Web App support
* Sustainability reminders and notifications
* AI-powered sustainability recommendations
* Location-aware activity tracking
* Gamification and achievement badges
* Weekly and monthly sustainability goals
* Advanced carbon-footprint categories
* Community challenges and leaderboards
* Authentication and role-based access
* Advanced analytics and predictive insights
* Multi-language support

---

## 📏 Challenge Compliance

| Requirement           | Implementation                               |
| --------------------- | -------------------------------------------- |
| Repository Visibility | Public GitHub Repository                     |
| Repository Size       | Designed to remain under 10 MB               |
| Git Strategy          | Main branch                                  |
| Backend               | Node.js + Express.js                         |
| Database              | SQLite                                       |
| API                   | RESTful API endpoints                        |
| Security              | Helmet, Rate Limiting, Validation, HPP       |
| Accessibility         | Semantic HTML, ARIA, contrast-focused design |
| Analytics             | Chart.js                                     |
| Export                | CSV, HTML, PDF                               |
| Configuration         | `config.json`                                |

---

## 📄 License

This project is licensed under the **MIT License**.

See the [LICENSE](LICENSE) file for more information.

---

## Acknowledgements

Special thanks to:

* Challenge stakeholders and mentors for their feedback
* The open-source community
* **Chart.js** for data visualization
* **Bootstrap** for responsive UI components
* **date-fns** for date manipulation utilities
* **Express.js** and the Node.js ecosystem for backend development

---

## 🌱 EcoShift

> **Track your habits. Measure your impact. Shift towards a greener future.**

EcoShift turns everyday sustainable actions into measurable environmental impact — helping individuals and communities understand how small changes can create meaningful results.
