# Future_ML_02
Support Ticket Classification &amp; Prioritization Model
Project Overview

This repository contains a Natural Language Processing (NLP) and Machine Learning decision-support system.
The system automatically reads customer support tickets, classifies them into operational categories, and assigns an urgency priority level. By automating this triage process, IT teams can significantly reduce response times, efficiently manage their backlogs, and prevent Service Level Agreement (SLA) failures.

**Dataset Filename : all_tickets_processed_improved_v3.csv**


The Architecture

To ensure efficiency and reliability, this project avoids complex dual-model setups in favor of ajob-ready pipeline that uses both Machine Learning with Deterministic Business Logic:

Text Preprocessing (NLP): Raw ticket text is cleaned to reduce noise. This includes lowercasing, removing special characters/numbers, filtering out stopwords, and applying lemmatization using NLTK.

Feature Extraction: The cleaned text is converted into numerical vectors using TF-IDF (Term Frequency-Inverse Document Frequency), limited to the top 5,000 features.

Machine Learning Classification: A Logistic Regression model accurately predicts the ticket's core category (e.g., Hardware, Access, Purchase, HR Support).

Deterministic Priority Engine: A custom rules-engine instantly maps the predicted category to a Priority Level (High, Medium, Low) based on operational risk, preventing priority inflation.
