# AI-Powered-Data-Extraction-Structuring

## Project Overview
This project utilizes Natural Language Processing (NLP) and deep learning models to process unstructured renovation meeting transcripts and extract structured data. The system identifies renovation tasks, budget details, and project categories from real-world discussions and generates a structured Excel report that serves as a Scope of Work document.

## File Structure
```
📂 Project Folder
│-- 📄 Transcript 1.docx
│-- 📄 transcript 2.docx
│-- 📄 Transcript 3.docx
│-- 📊 Transcript1.xlsx
│-- 📊 Transcript2.xlsx
│-- 📊 Transcript3.xlsx
│-- 🐍 test.py
│-- 📄 README.md
```

## Requirements
To run this project, install the necessary dependencies:
```bash
pip install transformers pandas openpyxl
```

## How It Works
1. **Transcript Processing**
   - Loads unstructured meeting transcripts from `.docx` files.
   - Cleans the text by removing unnecessary white spaces and filler words.
   
2. **Data Extraction & Categorization**
   - Identifies key renovation tasks, budgets, and project elements.
   - Categorizes information under relevant sections like Kitchen, Bathroom, Flooring, Electrical, etc.
   
3. **Summarization & Title Generation**
   - Uses `Flan-T5` for title generation.
   - Uses `DistilBART-CNN` for summarization.
   
4. **Budget Identification & Allocation**
   - Extracts and maps budget information from informal mentions (e.g., "15 grand" → `$15,000`).

5. **Report Generation**
   - Outputs structured renovation details into an `.xlsx` report.

## Usage
Run the script to process all transcripts and generate structured reports:
```bash
python process_transcripts.py
```

## Output
Each transcript is processed, and a corresponding Excel file is created with:
- Renovation categories
- Task descriptions
- Estimated budgets
- Additional relevant details

## Technologies Used
- **Python** (Data Processing & AI Inference)
- **Transformers (Hugging Face)**
  - `Flan-T5` for task title generation
  - `DistilBART-CNN` for summarization
- **Regex & NLP techniques** for keyword-based extraction
- **Pandas & OpenPyXL** for Excel processing

## Applications & Impact
- Automates the tedious process of reviewing meeting transcripts.
- Ensures critical renovation details are accurately structured and documented.
- Generates professional reports for contractors, project managers, and stakeholders.
- Can be extended to other industries requiring unstructured-to-structured data transformatio
