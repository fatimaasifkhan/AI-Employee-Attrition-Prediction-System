# 👥 AI Employee Attrition Prediction System

An **AI-assisted Employee Attrition Prediction System** developed using **Oracle APEX, Oracle Database, SQL, PL/SQL, and Google Gemini API**.

The system helps HR personnel analyze employee information, calculate an attrition risk score using predefined business rules, identify contributing factors, and generate AI-assisted insights through the **Gemini API**.

> **Note:** This project does not train or deploy a traditional Machine Learning model. Attrition scoring is performed using predefined business rules implemented with PL/SQL, while Google Gemini is used for AI-assisted analysis and generated insights.

---

## 📌 Project Overview

Employee attrition can have a significant impact on organizations through recruitment costs, loss of experienced employees, and reduced productivity.

This project provides an HR decision-support application that combines **rule-based analysis with Generative AI**.

The system collects employee information and evaluates predefined attrition factors to calculate an employee's attrition score and risk level. The Google Gemini API can then be used to provide additional AI-generated analysis based on the available employee information.

The application is built using **Oracle APEX** and **Oracle Database**, providing an interactive interface for HR users.

---

## 🎯 Objectives

The main objectives of the project are:

* Develop an HR-focused employee management system.
* Calculate employee attrition risk using predefined business rules.
* Identify factors contributing to attrition risk.
* Integrate Generative AI using the Google Gemini API.
* Provide AI-assisted explanations and insights.
* Store and manage employee information using Oracle Database.
* Provide an interactive HR dashboard.
* Generate structured employee prediction reports.
* Support HR decision-making through data-driven and AI-assisted insights.

---

# ✨ Features

## 🔐 HR Login

The system provides an authentication interface for HR users.

After login, authorized users can access the employee management and prediction features.

---

## 👤 Employee Management

HR users can:

* Add employee records
* View employee information
* Search employees
* Select employees for prediction
* Review employee details

---

## 📂 Dataset Upload

The application provides functionality for uploading employee datasets into the system.

Employee information may include:

* Age
* Department
* Job Role
* Job Level
* Monthly Income
* Job Satisfaction
* Work-Life Balance
* Overtime
* Years at Company
* Years in Current Role
* Years Since Last Promotion
* Years With Current Manager
* Total Working Years
* Performance Rating
* Distance From Home

---

# 🔮 Attrition Prediction

The system calculates an employee's **attrition score** using predefined business rules.

The score is based on selected employee and workplace factors.

For example:

```text
Low Job Satisfaction
        ↓
Increase Attrition Score

Poor Work-Life Balance
        ↓
Increase Attrition Score

Large Salary Difference
        ↓
Increase Attrition Score

Overtime
        ↓
Increase Attrition Score
```

The resulting score is used to classify the employee into a corresponding risk category.

Example:

```text
LOW RISK
MEDIUM RISK
HIGH RISK
```

---

# 🧮 Rule-Based Scoring

The core attrition calculation is implemented using **PL/SQL business logic** rather than a trained machine-learning model.

A simplified example:

```text
Attrition Score = 0

IF Job Satisfaction <= 2
    Score += 15

IF Work-Life Balance <= 2
    Score += 15

IF Salary Difference is high
    Score += 20

IF Overtime = Yes
    Score += 10

Evaluate Total Score
        ↓
Determine Risk Level
```

The actual conditions, weights, and thresholds are defined in the application's PL/SQL logic.

---

# 🤖 Google Gemini AI Integration

The project integrates **Google Gemini API** to introduce a Generative AI component into the HR system.

Gemini can be used to analyze the employee information and provide AI-generated insights based on the prediction results.

For example, after calculating the rule-based attrition score:

```text
Employee Data
      ↓
PL/SQL Rule-Based Scoring
      ↓
Attrition Score
      ↓
Risk Level
      ↓
Gemini API
      ↓
AI-Generated Analysis
```

Gemini can assist with generating:

* Explanation of risk factors
* Employee attrition insights
* Natural-language analysis
* Potential areas of concern
* HR-oriented recommendations
* Summary of prediction results

### Example

```text
Attrition Risk: HIGH

Rule-Based Factors:
• Low Job Satisfaction
• Poor Work-Life Balance
• Overtime
• Salary Difference

Gemini AI Analysis:

The employee's elevated attrition risk is associated with
multiple workplace factors, particularly job satisfaction,
work-life balance, and compensation-related factors.
HR may consider reviewing these areas as part of a broader
employee retention strategy.
```

---

# 🏗️ System Architecture

```text
                     ┌───────────────────┐
                     │      HR User      │
                     └─────────┬─────────┘
                               │
                               ▼
                    ┌────────────────────┐
                    │    Oracle APEX     │
                    │    Application     │
                    └─────────┬──────────┘
                              │
              ┌───────────────┼────────────────┐
              │               │                │
              ▼               ▼                ▼
       Employee Data     Dataset Upload    Prediction
              │               │                │
              └───────────────┼────────────────┘
                              │
                              ▼
                    ┌────────────────────┐
                    │   Oracle Database  │
                    │                    │
                    │ SQL + PL/SQL       │
                    └─────────┬──────────┘
                              │
                              ▼
                    ┌────────────────────┐
                    │ Rule-Based Scoring │
                    │                    │
                    │ Attrition Score    │
                    │ Risk Level         │
                    └─────────┬──────────┘
                              │
                              ▼
                    ┌────────────────────┐
                    │    Gemini API      │
                    │                    │
                    │ AI Analysis        │
                    │ Insights           │
                    │ Recommendations    │
                    └─────────┬──────────┘
                              │
                              ▼
                    ┌────────────────────┐
                    │ Prediction Results │
                    │ & Reports          │
                    └────────────────────┘
```

---

# 🛠️ Technologies Used

| Technology            | Purpose                              |
| --------------------- | ------------------------------------ |
| **Oracle APEX**       | Web application and HR interface     |
| **Oracle Database**   | Employee data storage                |
| **SQL**               | Data management and queries          |
| **PL/SQL**            | Attrition scoring and business logic |
| **Google Gemini API** | Generative AI analysis and insights  |
| **HTML**              | Application structure                |
| **CSS**               | User interface styling               |
| **JavaScript**        | Interactive UI functionality         |
| **APEX Charts**       | Data visualization                   |

---

# 🗄️ Database

Employee information is stored in an **Oracle Database**.

The database can contain employee attributes such as:

```text
Employee ID
Employee Name
Age
Department
Job Role
Job Level
Monthly Income
Job Satisfaction
Work-Life Balance
Overtime
Years at Company
Years in Current Role
Years Since Last Promotion
Years With Current Manager
Total Working Years
Performance Rating
Distance From Home
```

The exact database structure depends on the application's implementation.

---

# 🔄 System Workflow

```text
             HR Login
                 │
                 ▼
             Dashboard
                 │
                 ▼
       Add / Upload Employee
                 │
                 ▼
         Employee Records
                 │
                 ▼
        Select an Employee
                 │
                 ▼
       Calculate Risk Score
                 │
                 ▼
        Determine Risk Level
                 │
                 ▼
          Gemini Analysis
                 │
                 ▼
       Display AI Insights
                 │
                 ▼
         Generate Report
```

---

# 🖥️ Application Modules

### 1. HR Login

Authentication interface for HR users.

### 2. Dashboard

Provides an overview of employee information and attrition-related statistics.

### 3. Add Employee

Allows HR users to manually enter employee information.

### 4. Upload Dataset

Allows employee data to be imported into the system.

### 5. Employee Records

Displays stored employee information and allows HR users to search and select employees.

### 6. Attrition Prediction

Calculates an attrition score based on predefined rules.

### 7. Risk Analysis

Displays the employee's calculated risk category and contributing factors.

### 8. Gemini AI Analysis

Uses the Gemini API to generate natural-language analysis and insights based on the employee's prediction results.

### 9. Reports

Provides structured prediction and analysis information for HR review.

---

# 📊 Example Prediction

```text
---------------------------------------
       EMPLOYEE PREDICTION
---------------------------------------

Employee: Employee Name

Attrition Score: 60

Risk Level: HIGH

Important Factors:
✓ Low Job Satisfaction
✓ Poor Work-Life Balance
✓ Overtime
✓ Salary Difference

AI Analysis:
The employee's current profile contains several
factors associated with elevated attrition risk.
The identified factors can be reviewed by HR as
part of a broader employee retention strategy.
---------------------------------------
```

---

# 🔐 API Key Security

The Gemini API key should **never be committed to GitHub**.

Do not write:

```text
GEMINI_API_KEY = "your-real-api-key"
```

directly inside source code.

Instead, use an environment variable or secure application configuration.

Example:

```text
GEMINI_API_KEY=your_api_key_here
```

And add sensitive configuration files to `.gitignore`.

Example:

```text
.env
*.key
secrets/
```

> **Important:** If an API key has already been pushed to a public GitHub repository, revoke/rotate that key through the relevant Google AI service and replace it with a new key.

---

# 📁 Suggested Repository Structure

```text
employee-attrition-prediction/
│
├── README.md
│
├── database/
│   ├── tables.sql
│   ├── procedures.sql
│   └── queries.sql
│
├── apex/
│   └── apex_application.sql
│
├── dataset/
│   └── employee_data.csv
│
├── gemini/
│   └── gemini_integration.sql
│
├── screenshots/
│   ├── login.png
│   ├── dashboard.png
│   ├── employees.png
│   ├── prediction.png
│   ├── ai-analysis.png
│   └── report.png
│
└── documentation/
    └── project_documentation.pdf
```

---

# 🔬 Prediction Method

This system uses two complementary approaches:

### 1. Rule-Based Attrition Scoring

The employee's data is evaluated using predefined business rules implemented in PL/SQL.

```text
Employee Factors
       ↓
Business Rules
       ↓
Attrition Score
       ↓
Risk Level
```

### 2. Generative AI Analysis

The prediction results and relevant employee information can then be passed to Gemini to generate a human-readable analysis.

```text
Prediction Results
       ↓
Gemini API
       ↓
Natural Language Insights
```

This means the project **uses Generative AI but does not train its own Machine Learning model**.

---

# ⚠️ Responsible Use

Employee attrition predictions should be treated as **decision-support information**, not as definitive judgments about an employee.

The system should not be used as the sole basis for employment decisions.

Employee information should also be handled securely, with access limited to authorized personnel.

---

# 🔮 Future Enhancements

Potential future improvements include:

* Integration of a trained Machine Learning model
* SHAP-based explainability
* Automated HR notifications
* Department-level attrition analysis
* Employee retention recommendations
* Advanced dashboards
* Historical attrition trend analysis
* REST API integration
* Improved Gemini prompt engineering
* Automated report generation
* Model comparison if ML is introduced in a future version

---

# 🎓 Academic Project

This project demonstrates the integration of:

```text
Oracle APEX
      +
Oracle Database
      +
SQL
      +
PL/SQL
      +
Generative AI
      +
Google Gemini API
```

The project focuses on developing an **AI-assisted HR decision-support system** that combines structured business rules with Generative AI to provide employee attrition insights.

---

# 👩‍💻 Author

**Fatima**

AI & Technology | Data Analysis | Application Development

---

## 📜 License

This project was developed for educational and academic purposes.
