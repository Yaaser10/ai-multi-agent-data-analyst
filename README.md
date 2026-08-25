# AI Multi-Agent Data Analyst System

A multi-agent AI system that transforms raw sales data into verified business analysis, insights, and practical recommendations using AI agents and deterministic Python tools.

## Key Features

- CSV data processing
- Automatic dataset inspection
- Missing value detection
- Invalid data detection
- Duplicate detection
- Python-based data cleaning
- AI-generated analysis planning
- Deterministic numerical calculations
- Product and category performance analysis
- Monthly revenue analysis
- Business insight generation
- Actionable business recommendations
- Final structured analysis report

## System Architecture

```text
Raw CSV Data
      |
      v
+----------------------+
| Data Inspector Agent |
+----------------------+
      |
      v
Data Quality Report
      |
      v
+----------------------+
| Python Cleaning Tool |
+----------------------+
      |
      v
Cleaned Dataset
      |
      v
+----------------------+
|    Analyst Agent     |
+----------------------+
      |
      v
Analysis Plan
      |
      v
+------------------------+
| Python Analysis Engine |
+------------------------+
      |
      v
Verified Numeric Results
      |
      v
+----------------------+
|    Insight Agent     |
+----------------------+
      |
      v
Business Insights
      |
      v
+----------------------+
| Recommendation Agent |
+----------------------+
      |
      v
Final Data Analysis Report
```

## How It Works

1. The **Data Inspector Agent** examines the dataset structure and identifies possible data quality problems.
2. The **Python Cleaning Tool** performs deterministic cleaning operations.
3. The **Analyst Agent** decides which business analyses are useful.
4. The **Python Analysis Engine** performs the actual numerical calculations.
5. The **Insight Agent** interprets the verified results.
6. The **Recommendation Agent** converts the insights into practical business actions.
7. The workflow combines everything into one final analysis report.

## Agents

### Data Inspector Agent

Analyzes:

- Dataset columns
- Data types
- Missing values
- Duplicate rows
- Suspicious values
- Possible cleaning requirements

### Analyst Agent

Selects useful business analyses without performing the calculations itself.

Available analyses include:

```text
TOTAL_REVENUE
TOTAL_QUANTITY_SOLD
TOP_PRODUCT_BY_REVENUE
TOP_PRODUCT_BY_QUANTITY
REVENUE_BY_PRODUCT
REVENUE_BY_CATEGORY
REVENUE_BY_MONTH
AVERAGE_SALE_VALUE
```

### Insight Agent

Transforms verified numerical results into understandable business insights.

### Recommendation Agent

Creates practical recommendations based only on the verified analysis and generated insights.

## Python Components

### Data Cleaning Tool

Python handles deterministic cleaning tasks such as:

- Removing duplicates
- Detecting invalid dates
- Filling missing categories
- Calculating missing revenue when enough data exists
- Preserving unresolved missing values instead of inventing information

### Analysis Engine

Python performs all important calculations to keep the analysis accurate and reproducible.

## AI + Python Design Principle

This project separates reasoning from calculation.

```text
AI
↓
Understand
Plan
Interpret
Recommend

Python
↓
Inspect
Clean
Calculate
Verify
```

This architecture reduces the risk of relying on an AI model for calculations that can be handled more reliably by deterministic code.

## Data Quality Principles

The system follows two important rules:

```text
Missing Value != Zero
```

A missing value means the information is unknown.

A zero means the value is known to be zero.

The workflow also follows:

```text
Fix what you can prove.
Flag what you cannot.
```

The system avoids inventing missing business data simply to complete the dataset.

## Example Input

```text
Date        Product    Category       Quantity    Price    Revenue

2026-01-05  Laptop     Electronics    2           1000     2000
2026-01-10  Mouse      Accessories    5           20       100
2026-02-03  Laptop     Electronics    1           1000     1000
2026-02-15  Keyboard   Accessories    3           50       150
2026-03-01  Mouse      Accessories    4           20       Missing
2026-03-12  Laptop     Electronics    Missing     1000     Missing
wrong-date  Keyboard   Missing        2           50       100
```

## Final Report

The final output contains:

```text
1. Data Inspection
2. Data Cleaning
3. Analysis Plan
4. Verified Analysis Results
5. Business Insights
6. Business Recommendations
```

## Tech Stack

- Python
- Pandas
- Groq API
- Qwen
- Google Colab
- Multi-Agent Architecture
- Structured Data Analysis
- Data Cleaning
- Business Intelligence
- Deterministic Analysis
- Secure API Key Management

## How to Run

1. Open `AI_Multi_Agent_Data_Analyst_System.ipynb` in Google Colab.
2. Add your Groq API key to Colab Secrets using:

   `GROQ_API_KEY`

3. Enable notebook access to the secret.
4. Run the cells from top to bottom.
5. Replace the example dataset with your own data if needed.
6. Run the complete multi-agent workflow.
7. Review the final data analysis report.

> Never hard-code or commit API keys to GitHub.

## What I Learned

This project demonstrates:

- Multi-agent workflow design
- Structured data inspection
- Data cleaning with Python
- Separation of AI reasoning and deterministic calculations
- Business analysis planning
- AI-generated insights
- AI-generated recommendations
- Agent-to-tool collaboration

## Project Purpose

This project was built as a hands-on exploration of how AI agents and traditional Python data tools can work together to transform raw structured data into reliable, actionable business intelligence.
