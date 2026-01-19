# AI Prompt Usage Disclosure
## Purpose
This document outlines how AI tool (ChatGPT) was used during the data screening exercise. AI was used as a supporting assistant, not as a replacement for analytical judgment or decision-making.

## Tools Used
ChatGPT (Large Language Model)
Used for syntax clarification, debugging assistance, and documentation support.

## How AI Was Used
## 1. Understanding Errors and Debugging

**Prompt Used:**
> I am getting a UnicodeDecodeError while loading a CSV file in pandas. What does this error mean and how can I fix it?

**AI Response (Summary):**
- Explained encoding-related issues
- Suggested specifying encoding or inspecting file format

**My Action:**
- Investigated file structure
- Adjusted data loading approach based on dataset characteristics

## 2. Cleaning Special Characters in Text Columns

**Prompt Used:**
> How can I remove unnecessary special characters from a column in pandas while keeping letters and spaces intact?

**AI Response (Summary):**
- Suggested using regex-based string replacement

**My Action:**
- Applied regex-based cleaning
- Improved readability by chaining .str.strip()
- Ensured blank values remained untouched

## 3. Handling Missing Facility Names

**Prompt Used:**
> How should I handle blank values in a key identifier column like facility name?

**AI Response (Summary):**
- Discussed options such as dropping, imputing, or manual reconciliation

**My Action:**
- Cross-checked missing names using the official reference webpage
- Manually filled two missing facility names with documented justification

## 4. Converting Excel Serial Numbers to Dates

**Prompt Used:**
> I have Excel serial numbers mixed with string dates in a pandas column. How do I convert them to datetime?

**AI Response (Summary):**
- Explained Excel date origin (1899-12-30)
- Suggested using pd.to_datetime() with origin and unit

**My Action:**
- Converted column to numeric first
- Applied conditional datetime conversion
- Removed unnecessary time component
- Preserved missing or invalid values as NaT

## 5. Visualization Guidance

**Prompt Used:**

> What is a good way to visualize the top 10 categories by value in Python?

**AI Response (Summary):**
- Suggested bar charts and horizontal orientation for long labels

**My Action:**
- Chose a horizontal bar chart for clarity
- Customized layout and color palette
- Saved output as PNG for reporting

## What AI Was NOT Used For
- Selecting which data to drop or keep
- Interpreting results or drawing conclusions
- Making analytical or policy judgments

All final decisions regarding data cleaning, assumptions, and analysis were made independently.

**Summary**
AI tools were used responsibly as a coding and documentation assistant.
All analytical reasoning, validation, and final outputs reflect my own understanding and judgment.