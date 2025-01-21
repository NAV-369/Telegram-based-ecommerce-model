# Amharic NER Pipeline Project

## Instructions

This project involves building a Named Entity Recognition (NER) pipeline for Amharic data to identify entities such as products, prices, and locations from Ethiopian-based Telegram e-commerce channels.

The project is divided into the following tasks:
	1.	Amharic Data Collection and Preprocessing
	2.	Labeling Amharic Data for NER
	3.	Fine-Tuning Existing Models for NER
	4.	Model Comparison with Different NER Models
	5.	Model Interpretability

## Task 1: Data Ingestion and Data Preprocessing

## Objective

Set up a data ingestion system to fetch messages from multiple Ethiopian-based Telegram e-commerce channels. Prepare the raw data (text, images) for entity extraction.

## Steps:
	•	Identify and connect to relevant Telegram channels using a custom scraper.
	•	Implement a message ingestion system to collect text, images, and documents as they are posted in real-time.
	•	Preprocess text data by tokenizing, normalizing, and handling Amharic-specific linguistic features.
	•	Clean and structure the data into a unified format, separating metadata (e.g., sender, timestamp) from message content.
	•	Store preprocessed data in a structured format for further analysis.

## Task 2: Label a Subset of Dataset in CoNLL Format

## Objective

Label a portion of the provided dataset in the CoNLL format to identify entities such as products, prices, and locations in Amharic text.

## Steps:
	•	Use the “Message” column from the provided dataset, which contains text describing various products and entities.
	•	Format the text according to the CoNLL format:
	•	Each token (word) is labeled on its own line.
	•	The token is followed by its entity label.
	•	Blank lines separate individual sentences/messages.
	•	Label entities as follows:
	•	B-Product: Beginning of a product entity (e.g., “Baby bottle”).
	•	I-Product: Inside a product entity (e.g., the word “bottle” in “Baby bottle”).
	•	B-LOC: Beginning of a location entity (e.g., “Addis Abeba”, “Bole”).
	•	I-LOC: Inside a location entity (e.g., the word “Abeba” in “Addis Abeba”).
	•	B-PRICE: Beginning of a price entity (e.g., “ዋጋ 1000 ብር”, “በ 100 ብር”).
	•	I-PRICE: Inside a price entity (e.g., the word “1000” in “ዋጋ 1000 ብር”).
	•	O: Tokens outside any entities.
	•	Label at least 30-50 messages from the dataset and save your work in the CoNLL format.

## Task 3: Fine-Tune NER Model

## Objective

Fine-tune a Named Entity Recognition (NER) model to extract key entities (e.g., products, prices, and location) from Amharic Telegram messages.

## Steps:
	•	Use Google Colab or any other environment with GPU support for faster training.
	•	Install necessary libraries:

pip install transformers datasets torch  


	•	Select a pre-trained model for NER:
	•	XLM-Roberta
	•	bert-tiny-amharic
	•	afroxmlr
	•	Load the labeled dataset in CoNLL format from Task 2.
	•	Tokenize the data and align the labels with tokens produced by the tokenizer.
	•	Set up training arguments (learning rate, number of epochs, batch size, etc.).
	•	Use Hugging Face’s Trainer API to fine-tune the model.
	•	Evaluate the fine-tuned model on the validation set.
	•	After fine-tuning, save the model for future use.

## Task 4: Model Comparison & Selection

## Objective

Compare different models and select the best-performing one for the entity extraction task.

## Steps:
	•	Fine-tune multiple models for NER tasks, such as:
	•	XLM-Roberta
	•	DistilBERT
	•	mBERT (Multilingual BERT)
	•	Others (e.g., afroxmlr, bert-tiny-amharic).
	•	Evaluate the fine-tuned models on the validation set.
	•	Compare models based on key metrics:
	•	Accuracy
	•	Speed
	•	Robustness in handling multi-modal data.
	•	Select the best-performing model for production based on evaluation results.

## Task 5: Model Interpretability

## Objective

Use model interpretability tools to explain how the NER model identifies entities, ensuring transparency and trust in the system.

## Steps:
	•	Implement SHAP (SHapley Additive exPlanations) and LIME (Local Interpretable Model-agnostic Explanations) for interpreting the model’s predictions.
	•	Analyze difficult cases where the model might struggle to identify entities correctly (e.g., ambiguous text, overlapping entities).
	•	Generate reports on how the model makes decisions and identify areas for improvement.
