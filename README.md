# Data Ingestion, Preprocessing, and Entity Labeling Tasks

## Overview
This project consists of two main tasks focused on processing a dataset for Named Entity Recognition (NER) in the context of Ethiopian-based Telegram e-commerce channels. The tasks are aimed at both data ingestion and labeling the data for entity extraction.

### Tasks:
1. **Task 1: Data Ingestion and Data Preprocessing**
2. **Task 2: Label a Subset of Dataset in CoNLL Format**

---

## Task 1: Data Ingestion and Data Preprocessing

### Overview
In this task, we set up a system to ingest and preprocess messages from selected Ethiopian-based Telegram e-commerce channels. The goal is to collect text, images, and documents from the channels, process the data for further analysis, and prepare it for entity extraction.

### Objectives
- **Data Ingestion**: Collect messages (text, images, documents) in real-time from multiple Telegram channels.
- **Data Preprocessing**: Process and clean the text data, especially focusing on Amharic text, to make it ready for entity extraction and analysis.

### Steps

1. **Identify and Connect to Relevant Telegram Channels**  
   - Select at least five Ethiopian-based Telegram e-commerce channels.
   - Use a custom scraper to connect to these channels.

2. **Implement Message Ingestion System**  
   - Set up a real-time system to fetch messages (text, images, documents) from the selected channels.

3. **Preprocess Text Data**  
   - Tokenize, normalize, and handle Amharic-specific linguistic features.
   - Ensure proper handling of diacritics, characters, and script.

4. **Clean and Structure the Data**  
   - Separate metadata (e.g., sender, timestamp) from message content (e.g., text or media).
   - Organize the data into a structured format.

5. **Store Preprocessed Data**  
   - Store the data in a structured format (e.g., CSV, JSON, or a database) for further analysis.

---

## Task 2: Label a Subset of Dataset in CoNLL Format

### Overview
In this task, you will label a portion of the dataset in the **CoNLL format**, which is commonly used for Named Entity Recognition (NER) tasks. The goal is to identify and label entities such as products, prices, and locations in Amharic text.

### Objectives
- **Labeling Entities**: Label a subset of the dataset with specific entity types: products, prices, and locations.
- **CoNLL Format**: Label each token (word) in the dataset according to its corresponding entity in CoNLL format.

### CoNLL Format
Each token is labeled on its own line, followed by its entity type. Blank lines separate individual sentences/messages.

#### Entity Types:
- **B-Product**: Beginning of a product entity (e.g., "Baby bottle").
- **I-Product**: Inside a product entity (e.g., "bottle" in "Baby bottle").
- **B-LOC**: Beginning of a location entity (e.g., "Addis Abeba").
- **I-LOC**: Inside a location entity (e.g., "Abeba" in "Addis Abeba").
- **B-PRICE**: Beginning of a price entity (e.g., "ዋጋ 1000 ብር").
- **I-PRICE**: Inside a price entity (e.g., "1000" in "ዋጋ 1000 ብር").
- **O**: Tokens that are outside any entities.

#### Example:

የቤት እቃ        O
የግምት ቦታ     B-LOC
በአዲስ አበባ    I-LOC
እቃ በተለዋዋጭ    B-Product
ቤት አሞሌ        I-Product
በተለዋዋጭ 1000 ብር   B-PRICE

### Steps

1. **Labeling Dataset**  
   - Label at least 30-50 messages from the provided dataset's "Message" column.

2. **Save the Labeled Data**  
   - Save your work in a plain text file in the CoNLL format.
   
---

## Requirements

### Task 1:
- **Programming Language**: Python
- **Libraries**: `telethon` or `python-telegram-bot`, `nltk`, `spacy`, `pandas`, `json`

### Task 2:
- **File Format**: Plain text file with CoNLL formatting

---

## Setup Instructions

### Task 1: Data Ingestion and Data Preprocessing

1. Clone the repository:
   ```bash
   git clone https://github.com/your-repository.git
   cd your-repository

	2.	Install dependencies:

pip install -r requirements.txt


	3.	Set up Telegram API credentials:
	•	Obtain your API key from Telegram.
	•	Store your credentials in a .env file:

TELEGRAM_API_ID=your_api_id
TELEGRAM_API_HASH=your_api_hash


	4.	Run the scraper:

python scraper.py



Task 2: Label a Subset of Dataset in CoNLL Format
	1.	Label messages from the provided dataset, ensuring each token is properly identified and labeled.
	2.	Save the labeled data in a .txt file using the CoNLL format.
	3.	Submit the labeled file for review.

Notes
	•	Task 1 focuses on setting up the pipeline to collect and preprocess data from Telegram channels. The resulting cleaned data will be used for further analysis.
	•	Task 2 involves labeling specific entities in the dataset, which will be crucial for training a Named Entity Recognition (NER) model.
	•	Ensure consistent labeling and follow the CoNLL format strictly when labeling for Task 2.

Contribution Guidelines
	•	Please ensure your code is well-documented and follows the project’s coding standards.
	•	If you make any significant changes to the pipeline or labeling format, update this README accordingly.
	•	Open a GitHub issue for any unclear cases or problems encountered during the tasks.
