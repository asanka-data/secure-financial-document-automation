# System Architecture

## 🔷 High-Level Architecture

HR Uploads PDFs → SharePoint Library
↓
Excel Employee List
↓
Power Automate Flow
↓
Folder + File Validation
↓
Secure Link Generation
↓
Automated Email


---

## 📁 SharePoint Layer

- Private site collection
- Library: `T4 Slips`
- Year-based folder organization
- Employee-level folder structure

Purpose:
- Centralized secure document storage
- Access control enforcement
- Audit logging

---

## 📊 Excel Data Layer

Employees.xlsx (Table Format)

Required Columns:
- FolderName
- EmployeeEmail

Purpose:
- Acts as source of truth for distribution
- Allows bulk automation
- Enables scalability

---

## ⚙ Power Automate Layer

Core Components:

1. Manual Trigger (Year input)
2. List rows from Excel
3. Apply to each employee
4. Get folder metadata
5. Create folder if missing
6. Get file metadata
7. Create sharing link
8. Send email

Purpose:
- Orchestrates validation and distribution
- Prevents missing file errors
- Ensures structured execution

---

## ✉ Email Delivery Layer

- Outlook (V2) or Gmail connector
- Secure internal link included
- No file attachments
- Controlled access via SharePoint permissions

---

## 🔐 Security Architecture

- No public anonymous links
- Organization-scoped link control
- HR-only SharePoint access
- SharePoint audit logging
