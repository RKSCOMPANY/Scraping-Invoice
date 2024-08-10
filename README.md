# Scraping-Invoice

<h2>## LLM Project: Invoice Data Extraction</h2>

<h2>### Project Overview</h2>
This project aims to develop an AI-powered system capable of extracting essential information from invoice PDFs stored in Google Drive. The extracted data includes customer details, product information, and total amount due.

<h2>### Core Components</h2>
<h3>1. **PDF Extraction:**</h3>
   * **Google Drive Integration:** The system integrates with Google Drive API to access and retrieve invoice PDFs.
   * **PDF Parsing:** Extracted PDFs are converted into text format using a suitable PDF parsing library (e.g., PyPDF2, pdfplumber).

<h3>2. **Data Preprocessing:**</h3>
   * **Text Cleaning:** The extracted text is cleaned to remove noise, formatting inconsistencies, and irrelevant information.
   * **Data Structuring:** The cleaned text is formatted into a structured format suitable for LLM processing.

<h3>3. **LLM Processing:**</h3>
   * **GPT-4 Integration:** The project utilizes the GPT-4 language model to extract required information.
   * **Prompt Engineering:** A carefully crafted prompt template is used to guide the LLM in extracting customer details, product information, and total amount due.
   * **Information Extraction:** The LLM processes the invoice text and extracts the specified data points.

<h3>4. **Data Masking:**</h3>
   * **Sensitive Information:** The extracted customer address, GST number, and PAN number are masked to protect sensitive information.

<h2>### Prompt Template</h2>
The core prompt template used for LLM processing is:

```
You are a helpful AI assistant that can extract information from invoices. 

Given the following invoice text, extract the customer details (name, address, etc.) hide the address , GST No. & PAN No. , 
a list of products purchased with their quantity and price, and the total amount due. 

If the information is not available, simply state 'Not available'.

Invoice Text: {texts}
```

<h2>### Conclusion</h2>
<h3>By combining PDF extraction, LLM capabilities, and effective prompt engineering, this project aims to provide a robust and efficient solution for extracting valuable information from invoices.
