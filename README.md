# Assignment 1 - Singlish to Sinhala Transliteration Testing

## Overview
This project tests the Chat Sinhala transliteration feature at
https://www.pixelssuite.com/chat-translator using Playwright automation.
The goal is to identify cases where the application incorrectly converts
chat-style Singlish input into Sinhala output.

This is Assignment 1 for IT3040 - ITPM, BSc (Hons) in Information Technology,
Year 3, Semester 1 at SLIIT.

## Prerequisites
- Python 3.11 or above
- Google Chrome browser installed

## Installation

### Step 1 - Clone or download this repository
Download the ZIP and extract it, or clone using:
git clone https://github.com/Aathi-141/it3040-assignment1_test_automation

### Step 2 - Open Command Prompt and navigate to the folder
cd C:\Users\user\Desktop\test_automation\test_automation

### Step 3 - Install required dependencies
pip install playwright openpyxl

python -m playwright install

## Running the Tests

Make sure the Excel file is closed before running.
Then run this command from inside the project folder:

python test_automation.py --excel "Assignment 1 - Test cases.xlsx" --url "https://www.pixelssuite.com/chat-translator" --wait-ms 15000 --type-delay-ms 100 --slow-mo-ms 500 --save-every 1 --keep-open

## What Happens When You Run It
- A browser window opens automatically
- The script visits https://www.pixelssuite.com/chat-translator
- It types each Singlish test case into the input box
- It clicks the Transliterate button and waits for the output
- The Actual output and Status columns are filled automatically
- The Excel file is saved after every single test case

## Checking Results
1. Wait for the script to finish all 50 rows
2. Press CTRL+C to stop
3. Open Assignment 1 - Test cases.xlsx
4. Check column E - Actual output (filled automatically)
5. Check column F - Status (shows FAIL for incorrect translations)
6. Since all 50 are negative test cases, FAIL means the app
   failed to correctly transliterate the Singlish input

## Project Structure
test_automation/
├── test_automation.py               Main Playwright automation script
├── Assignment 1 - Test cases.xlsx   Test cases with results
└── README.md                        This file

## Test Case Summary
- Total test cases: 50 negative test cases (Neg_0001 to Neg_0050)
- All 50 test cases result in FAIL status
- Coverage: At least 2 test cases for each of the 24 Singlish input types
- Input length categories:
    S = 30 characters or less
    M = 31 to 299 characters
    L = 300 to 450 characters

## Singlish Input Types Covered
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
