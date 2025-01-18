# Task 1: Data Ingestion and Data Preprocessing

## Overview
This project focuses on building a data ingestion and preprocessing pipeline to fetch and prepare messages from Ethiopian-based Telegram e-commerce channels. The goal is to collect raw data (including text, images, and documents) from selected Telegram channels, process the text data (especially focusing on Amharic), and structure the data for further analysis and entity extraction.

### Objectives
- **Data Ingestion**: Set up a system to fetch messages from Telegram e-commerce channels.
- **Data Preprocessing**: Process and clean the raw data, handling text, images, and documents.
- **Preparation for Entity Extraction**: Convert the raw data into a structured format, preparing it for further analysis.

---

## Steps

### 1. Identify and Connect to Relevant Telegram Channels
- **Objective**: Identify at least five Ethiopian-based e-commerce channels.
- **Action**: Use a custom scraper to connect to Telegram and fetch data from the selected channels.
- You may use the **Telethon** or **python-telegram-bot** libraries for interacting with Telegram.
  
### 2. Implement Message Ingestion System
- **Objective**: Collect text, images, and documents posted in real-time.
- **Action**: Set up a system that listens for new messages from the selected channels and fetches the content (text, images, documents) as soon as they are posted.
  
### 3. Preprocess Text Data
- **Objective**: Tokenize, normalize, and handle Amharic-specific linguistic features.
- **Action**: 
  - **Tokenization**: Break the text into words or sentences.
  - **Normalization**: Convert text to lowercase, remove punctuation, stopwords, and perform stemming/lemmatization.
  - **Amharic-specific handling**: Ensure that tokenization and text normalization work for Amharic, which may require specialized handling for diacritics, characters, and script.

### 4. Clean and Structure the Data
- **Objective**: Prepare the data in a unified format.
- **Action**:
  - **Separate Metadata**: Extract and structure metadata such as the sender, timestamp, and message type (text, image, document).
  - **Message Content**: Clean and separate the actual message content (text or media) from the metadata.
  
### 5. Store Preprocessed Data
- **Objective**: Store the cleaned and structured data for future analysis.
- **Action**: 
  - Store the processed data in a structured format such as **CSV**, **JSON**, or a **database**.
  - Ensure that data is accessible and easy to query for further analysis, such as entity extraction.

---

## Requirements

- **Programming Language**: Python
- **Libraries**:
  - `telethon` or `python-telegram-bot` for Telegram API interaction.
  - `nltk` or `spacy` for text processing.
  - `pandas` or `json` for data storage and manipulation.
  
---

## Setup Instructions

### 1. Clone the Repository

```bash
git clone https://github.com/your-repository.git
cd your-repository

