# IT3040 – ITPM Assignment 1
## Transliteration Accuracy Testing

Student ID: IT23809642  
Module: IT3040 – IT Project Management  
Year: 3 Semester 1  

---

## Project Overview

This project evaluates the accuracy of the Sinhala transliteration system available at:

https://www.pixelssuite.com/chat-translator

The objective is to assess how accurately the system converts chat-style Singlish input into Sinhala output. The testing focuses on identifying incorrect transliterations using commonly used informal Sinhala typing patterns.

This assignment is conducted as an individual assessment and contributes 18% to the final module grade.

---

## Assignment Objectives

- Evaluate the correctness of chat-style Sinhala transliteration
- Identify incorrect conversions (failures)
- Design and execute automated test cases using Playwright
- Analyze weaknesses in the system using structured testing

Note: Standard Sinhala mode, backend APIs, performance, and security testing are not included in scope.

---

## Test Case Design

- Total test cases: 50  
- All test cases are negative scenarios (system failures)  
- Each test case begins with `Neg_` as required  
- Test cases cover Singlish input types defined in Appendix 1  
- Input length categories used:
  - S (≤ 30 characters)
  - M (31–299 characters)
  - L (300–450 characters)

Test cases are stored in:

`IT23809642 - Test cases.xlsx`

---

## Automation Approach

All test cases are automated using Playwright.

The automation script:
- Reads test cases from Excel
- Sends Singlish inputs to the web application
- Captures Sinhala output
- Compares expected vs actual results
- Writes results back to Excel

---

## Technologies Used

- Python 3  
- Playwright  
- OpenPyXL  

---

## Project Structure

```
test_automation/
│── test_automation.py
│── IT23809642 - Test cases.xlsx
│── README.md
```

---

## Setup Instructions

### 1. Install Prerequisites

- Install Python 3.11 or above  
- Install Google Chrome (recommended)  

---

### 2. Install Dependencies

```bash
pip install -U pip
pip install playwright openpyxl
playwright install
```

---

### 3. Run the Automation Script

```bash
python test_automation.py --excel "IT23809642 - Test cases.xlsx" --url "https://www.pixelssuite.com/chat-translator" --wait-ms 5000 --type-delay-ms 80 --slow-mo-ms 200 --save-every 1 --keep-open
```

---

## Execution Process

1. Enter test cases in the Excel file:
   - TC ID
   - Input length type
   - Input
   - Expected output

2. Run the automation script.

3. The script automatically fills:
   - Actual output
   - Status (Pass / Fail)

4. Manually complete the remaining columns:
   - Singlish input types covered
   - Evidence or rationale

---

## Output

- Results are recorded automatically in the Excel file  
- Each test case includes:
  - Expected vs Actual output
  - Pass / Fail status
  - Input type classification
  - Supporting rationale

---

## Scope Limitations

- Only chat-style Sinhala transliteration is tested  
- Standard mode is excluded  
- Backend, performance, and security testing are not included  

---

## Repository

https://github.com/HASHINI-MARASINGHE/IT3040-ITPM-Assignment1-IT23809642

---

## Submission Notes

- All files are renamed using student ID  
- Repository is publicly accessible  
- Excel file is original and free from plagiarism  
- Automation follows provided guidelines  

---

## Author

IT23809642