# Troubleshooting Guide

---

## ❌ Folder Not Found

Cause:
- Folder name mismatch
- Missing Year folder
- Trailing spaces in Excel

Fix:
- Use trim() in expressions
- Confirm exact folder spelling

---

## ❌ Double Slash in Path

Example:
T4 Slips//John Smith


Cause:
- Year value missing

Fix:
- Verify trigger input mapping

---

## ❌ BadRequest (ItemId)

Cause:
- File path used instead of numeric ItemId

Fix:
- Use ItemId from "Get file metadata using path"

---

## ❌ Duplicate Emails

Cause:
- Duplicate rows in Excel

Fix:
- Remove duplicate EmployeeEmail entries

---

## ❌ Email Sent Without Link

Cause:
- Incorrect dynamic content used

Fix:
- Use webUrl output from Create sharing link step

---

## ❌ Actions Skipped

Cause:
- Incorrect Run After configuration

Fix:
- Verify success/failure conditions in each step
