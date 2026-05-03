# IT3040 - ITPM Assignment 1 - Option 1

**Student Name:** Thilakarathna T R P  
**Registration Number:** IT23384392  
**Module:** IT3040 – IT Project Management  
**Semester:** Semester 1  

---

## Assignment Title
Transliteration Accuracy Testing for Chat Sinhala

---

## Description

This project contains a Playwright automation script for testing the **Chat Sinhala transliteration** feature available at:

🔗 https://www.pixelssuite.com/chat-translator

The purpose of this assignment is to identify **50 negative test cases** where chat-style Singlish input is **not correctly converted** into Sinhala output, covering all 24 Singlish input types specified in Appendix 1 of the assignment.

---

## Test Scope

**In scope:**
- Chat Sinhala transliteration function only

**Out of scope:**
- Standard Sinhala transliteration
- Backend API testing
- Performance testing
- Security testing
- Scalability testing

---

## Files Included

| File | Description |
|------|-------------|
| `test_automation.py` | Playwright automation script |
| `IT23384392_Assignment 1 - Test cases.xlsx` | Excel file with 50 negative test cases and execution results |
| `IT23384392_README.md` | Project documentation |
| `IT23384392_github_link.txt` | GitHub repository link |

---

## Requirements

- Python 3.11 or above
- Google Chrome (recommended)
- Playwright
- openpyxl

---

## Installation Steps

**Step 1 — Create and activate a virtual environment:**

```bash
python3 -m venv venv
source venv/bin/activate
```

> On Windows use: `venv\Scripts\activate`

**Step 2 — Install dependencies:**

```bash
pip install --upgrade pip
pip install playwright openpyxl
```

**Step 3 — Install Playwright browsers:**

```bash
playwright install
```

---

## How to Run the Automation

Make sure the Excel file is **closed** before running. Then run:

```bash
python3 test_automation.py \
  --excel "IT23384392_Assignment 1 - Test cases.xlsx" \
  --sheet "Test Cases" \
  --input-col "Input" \
  --expected-col "Expected output" \
  --actual-col "Actual output" \
  --status-col "Status" \
  --url "https://www.pixelssuite.com/chat-translator" \
  --wait-ms 10000 \
  --type-delay-ms 120 \
  --slow-mo-ms 400 \
  --save-every 1 \
  --keep-open
```

---

## Test Case Summary

| Detail | Value |
|--------|-------|
| Total test cases | 50 |
| Test case type | Negative (FAIL) |
| Singlish input types covered | All 24 |
| Input length types used | S (≤30 chars), M (31–299 chars), L (300–450 chars) |

### Singlish Input Types Covered

1. Question forms
2. Command forms
3. Greetings
4. Requests
5. Responses
6. Repeated Words
7. Inputs with Punctuation Marks
8. Romanization / Spelling Variants
9. Isolated English Word Insertions in Singlish
10. Multi-Word English Phrases in Singlish
11. English Digital Terms in Singlish
12. Platform/App Names in Singlish
13. English Abbreviations/Acronyms in Singlish
14. English Clipped Forms in Singlish
15. Place Names Embedded in Singlish
16. Person Names Embedded in Singlish
17. Inputs with Numbers and Numeric Suffixes
18. Inputs with Currency
19. Inputs with Time Formats
20. Inputs with Dates
21. Inputs with Unit of Measurements
22. Inputs with Slang and Casual Phrasing
23. Online Identifiers in Singlish
24. Inputs Containing Emojis

---

## Notes

- The Excel file contains **50 negative test cases** — all resulting in **FAIL** status.
- The **Actual output** and **Status** columns are populated automatically by the Playwright script.
- The **Singlish input types covered** and **Evidence or rationale** columns are filled manually.
- Do **not** open the Excel file while the automation script is running.
