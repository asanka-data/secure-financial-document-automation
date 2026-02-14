# Flow Logic Explanation

## 1️⃣ Manual Trigger

Input:
- Year (Text)

Purpose:
- Makes process reusable each year
- Avoids hardcoding year value

---

## 2️⃣ List Rows Present in a Table

Source:
- Employees.xlsx

Returns:
- Value array of employee records

---

## 3️⃣ Apply to Each

Loops through each employee row.

Each iteration handles:
- Folder validation
- File validation
- Link creation
- Email sending

---

## 4️⃣ Get Folder Metadata Using Path

Checks:
/T4 Slips/<Year>/<FolderName>


If folder exists → continue  
If folder not found → handled by next step

---

## 5️⃣ Create New Folder (Conditional)

Run After Configuration:
- Runs only if folder check failed

Purpose:
- Automatically creates missing employee folders
- Prevents runtime failures

---

## 6️⃣ Get File Metadata Using Path

Checks:
/T4 Slips/<Year>/<FolderName>/<FolderName>.pdf


Ensures:
- T4 file exists before sending email

---

## 7️⃣ Create Sharing Link

Uses:
- Numeric ItemId from metadata step

Configuration:
- View only
- People in organization

Purpose:
- Secure controlled access link

---

## 8️⃣ Send Email

To:
- EmployeeEmail (from Excel)

Body includes:
- Secure sharing link

---

## 🔄 Run After Logic Strategy

- Folder creation runs only if folder missing
- File validation runs if folder existed OR created
- Sharing link runs only if file exists
- Email runs only if link created

This prevents broken emails or empty links.
