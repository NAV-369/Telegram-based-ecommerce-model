

# Task 2: Label a Subset of Dataset in CoNLL Format

## Overview
In this task, you are tasked with labeling a portion of the provided dataset using the **CoNLL format**, which is commonly used for Named Entity Recognition (NER) tasks. The objective is to identify and label entities such as products, prices, and locations within Amharic text.

## Objective
- **Labeling Entities**: Label the dataset for specific entity types such as product names, price, and location.
- **CoNLL Format**: The labeled data should follow the **CoNLL format** for NER tasks.
- **Textual Data**: Use the "Message" column of the provided dataset, which contains text describing various products and entities.

---

## CoNLL Format

Each line in the CoNLL format should represent a token (word) from the text. Each token should be followed by its corresponding entity label. 

### Format:
1. **Each token (word)** is labeled on its own line.
2. **The token is followed by its entity label** (e.g., `B-Product`, `I-Product`).
3. **Blank lines** separate individual sentences/messages.

### Entity Types:
- **B-Product**: The beginning of a product entity (e.g., "Baby bottle").
- **I-Product**: Inside a product entity (e.g., the word "bottle" in "Baby bottle").
- **B-LOC**: The beginning of a location entity (e.g., "Addis Abeba", "Bole").
- **I-LOC**: Inside a location entity (e.g., the word "Abeba" in “Addis Abeba”).
- **B-PRICE**: The beginning of a price entity (e.g., "ዋጋ 1000 ብር", "በ 100 ብር").
- **I-PRICE**: Inside a price entity (e.g., the word "1000" in “ዋጋ 1000 ብር”).
- **O**: Tokens that are outside any entities.

### Example:
Here is an example of how you should label a sentence in CoNLL format:

የቤት እቃ      O
የግምት ቦታ  B-LOC
በአዲስ አበባ    I-LOC
እቃ በተለዋዋጭ  B-Product
ቤት አሞሌ      I-Product
በተለዋዋጭ 1000 ብር   B-PRICE

In this example:
- "የቤት እቃ" is labeled as a product entity (B-Product).
- "ቦታ" is labeled as a location entity (B-LOC).
- "1000 ብር" is labeled as a price entity (B-PRICE).

---

## Requirements

1. **Labeling Dataset**:
   - You need to label **at least 30-50 messages** from the provided dataset's "Message" column.
   
2. **Save the Labeled Data**:
   - Save your labeled data in a **plain text file** in the CoNLL format.

3. **Text Processing**:
   - Use the provided dataset and focus on identifying product names, locations, and prices within the Amharic text.
   
---

## Instructions

1. **Prepare Your Environment**:
   - Ensure you have the dataset available, particularly the "Message" column containing Amharic text.
   
2. **Labeling**:
   - Carefully read through each message in the dataset and identify the entities (products, prices, locations).
   - Label the entities as per the CoNLL format.

3. **Save Your Work**:
   - After labeling each message, save the results in a text file using the CoNLL format.
   
---

## Submission

- **File Format**: Ensure that the labeled data is saved in **plain text format** with a `.txt` extension.
- **Submit**: Submit the labeled file for review and further processing.

---

## Notes

- This task is critical for the preparation of data used in training a Named Entity Recognition (NER) model.
- The labeled data will be used for identifying and extracting specific entities in Amharic text related to e-commerce.

---

## Contribution Guidelines
- Please ensure that all data is labeled consistently according to the provided entity categories.
- If you encounter any unclear cases, please annotate them as `O` (outside any entity) or leave a note in the labeled file for clarification.

This markdown README will guide the user through the process of labeling the dataset in CoNLL format. You can copy and paste this into your project’s README file for clear instructions.