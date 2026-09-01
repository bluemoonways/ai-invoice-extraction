# 🧾 AI Invoice Extraction

An AI-powered invoice extraction workflow built with **n8n** that extracts structured information from PDF invoices and stores invoice line items in Google Sheets.

## 🚀 Project Overview

The workflow allows a user to upload a PDF invoice through an n8n form. The PDF text is extracted, Google Gemini processes the invoice, and the information is returned in structured output.

Each invoice line item is then split into an individual record before being stored in Google Sheets.

## 🔄 Workflow

![AI Invoice Extraction Workflow](screenshots/Invoice%20Extraction%20Workflow.png)

## ✨ Key Features

- 📄 Upload invoices through an n8n form
- 🔍 Extract text from PDF invoices
- 🤖 Use Google Gemini for invoice data extraction
- 📦 Extract every invoice line item separately
- 🧩 Return structured JSON output
- 📊 Store invoice data in Google Sheets
- 🔄 Append or update records using Invoice Number
- ⚡ Reduce manual invoice data entry

## 📋 Data Extracted

- Invoice Number
- Invoice Date
- Due Date
- Customer Name & Email
- Vendor Name & Email
- Product Description
- Quantity
- Unit Price
- Line Item Amount
- Currency
- Total Invoice Amount

## 🧠 AI Processing

The AI agent extracts invoice information accurately, keeps every line item separate, returns numeric values as numbers, and uses `null` when a field is missing.

The structured output is then passed to the **Split Out** node for item-wise processing.

## 📊 Google Sheets Output

Extracted invoice details, customer/vendor information, line-item data, currency, and total amount are mapped into Google Sheets.

**Invoice Number** is used as the matching column for append/update behavior.

## 💡 Key Achievement

Instead of storing an entire invoice as one unstructured record, the workflow processes each invoice item separately.

### Sample Invoice Output

| Product | Qty | Amount |
|---|---:|---:|
| Dell Inspiron 15 3520 | 1 | PKR 115,000 |
| Logitech MX Master 3S Wireless Mouse | 1 | PKR 18,500 |
| Anker 543 USB-C Hub | 2 | PKR 15,000 |

Sample invoice total: **PKR 149,000**

## 🛠️ Technologies Used

- **n8n**
- **Google Gemini AI**
- **PDF Extraction**
- **Structured JSON Output**
- **Split Out Node**
- **Google Sheets**
- **Workflow Automation**

## 📁 Workflow File

You can view and download the complete n8n workflow here:

👉 [View n8n Workflow JSON](Invoice_Extraction_Workflow.json)

## 👨‍💻 Author

**Faheem Abbas**

AI Automation Specialist | n8n | AI Agents | Workflow Automation | API Integrations
---

### #n8n #AIAutomation #InvoiceAutomation #GoogleGemini #GoogleSheets #WorkflowAutomation #PDFExtraction
