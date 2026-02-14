# Secure T4 Distribution Automation  
### SharePoint + Power Automate Implementation

## 📌 Overview

This project automates the secure internal distribution of T4 slips using:

- SharePoint Online (Document Library)
- Power Automate
- Excel Online (Employee Source List)
- Outlook / Gmail Connector

The system ensures each employee receives access **only to their own T4 document**, eliminating manual errors and reducing HR workload.

---

## 🎯 Problem Statement

Manual T4 distribution creates several risks:

- Sending documents to the wrong employee
- Email attachment security exposure
- No structured audit trail
- High manual effort during tax season
- Difficult to scale for growing organizations

---

## ✅ Solution Summary

This automation:

1. Reads employee list from Excel
2. Validates employee folder structure
3. Creates missing folders automatically
4. Validates PDF existence
5. Generates secure internal sharing link
6. Sends automated email to each employee

The process is repeatable yearly with minimal effort.

## 🏗 Folder Structure

T4 Slips/
└── 2025/
└── John Smith/
└── John Smith.pdf


PDF Naming Convention:
<FolderName>.pdf


---

## 🔁 Flow Overview

Manual Trigger (Enter Year)  
→ List rows from Excel  
→ Apply to each employee  
→ Check folder exists  
→ Create folder if missing  
→ Validate PDF exists  
→ Generate secure link  
→ Send email  

---

## 💼 Business Benefits

- Eliminates manual T4 email distribution errors
- Ensures employee-level access isolation
- Reduces HR workload significantly
- Fully repeatable annual process
- Audit-friendly and compliant
- Scalable foundation for future payroll automation

---

## 🛠 Technology Stack

- SharePoint Online
- Power Automate
- Excel Online (Business)
- Outlook / Gmail Connector

---

## 🔐 Security Design

- Private SharePoint site
- Library-level restricted access
- View-only link generation
- Organization-scoped sharing
- No public anonymous links

---

## 🚀 Future Enhancements

- Specific-person-only sharing links
- Automatic permission breaking per folder
- Logging & audit reporting
- Power BI dashboard for tracking
- Extension for T4A / ROE / Paystub distribution

---

## ⚠ Important

This repository contains **no real payroll data**.  
All sample files use dummy data for demonstration purposes only.
---

