# 🏆 RPA Challenge - Invoice Extraction Automation

## 📌 Project Overview
This project automates the extraction of invoice data using UiPath **Studio 2023.10** and the **Robotic Enterprise Framework (REFramework)**.  
It processes invoices from various formats **(PDF, scanned images)** and extracts key fields such as **invoice number, date, total amount, and company name**.  
The extracted data is validated and stored in a structured format for further processing.

## 🚀 Features
- **Document Processing** → Extracts invoice details from **PDF and scanned images**.
- **Data Cleaning** → Removes unwanted characters (e.g., `$`, `"` from total amounts).
- **Transaction-Based Processing** → Uses **Get Transaction Data** to manage invoices.
- **Structured Logging & Error Handling** → Follows REFramework standards.
- **Config-Driven Design** → Uses `Config.xlsx` for flexible settings.

---

## **📌 How It Works**
### **1️⃣ Initialization (`Init`)**
- **`InitAllSettings.xaml`** → Loads configuration data from `Config.xlsx`.
- **`InitAllApplications.xaml`** → Opens and prepares the browser or file system.
- **`I-1.RPAChallenge_OpenBrowser.xaml`** → Opens the invoice portal.
- **`I-2.RPAChallenge_DownloadExcel`** → Download the result example file.
- **`I-3.RPAChallenge_ClickStart.xaml`** → Starts the extraction process.
- **`I-4.RPAChallenge_ExtractData.xaml`** → Extracts invoice details.

### **2️⃣ Get Transaction Data (`GetTransactionData`)**
- **Fetches each invoice row** as a transaction for processing.
- **Handles structured data extraction** for invoice processing.
- **`G-1.RPAChallenge_UploadCsv.xaml`** → Upload Challenge File.
- **`G-2.RPAChallenge_GetFinalScore.xaml`** → Get Final Score.

### **3️⃣ Process Transaction (`Process`)**
- **`P-1.RPAChallenge_ReadInvoice.xaml`** → Read Invoice.

### **4️⃣ End Process (`End Process`)**
- **`E-1.RPAChallenge_CloseBrowser.xaml`** → Closes the browser session after processing.

---

## **🛠️ Setup Instructions**
1️⃣ **Clone this repository**  
```bash
git clone https://github.com/Make310/AUX-RPAChallenge_InvoiceExtraction.git
