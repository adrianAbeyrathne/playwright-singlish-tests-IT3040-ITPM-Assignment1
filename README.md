# Singlish to Sinhala Transliteration Testing - IT3040 ITPM Assignment 1

## Project Description

This project automates testing of the Singlish to Sinhala transliteration tool available at:

https://www.pixelssuite.com/chat-translator

The automation identifies 50 failing test cases where the system fails to correctly convert chat-style Singlish input into Sinhala output. All test cases are negative test cases designed to evaluate the system's weaknesses.

## Test Coverage

The 50 test cases cover the following 24 Singlish input types, with a minimum of 2 test cases per type:

- Question forms
- Command forms
- Greetings
- Requests
- Responses
- Repeated Words
- Inputs with Punctuation Marks
- Romanization / Spelling Variants
- Isolated English Word Insertions
- Multi-Word English Phrases
- English Digital Terms
- Platform/App Names
- English Abbreviations/Acronyms
- English Clipped Forms
- Place Names Embedded
- Person Names Embedded
- Inputs with Numbers and Numeric Suffixes
- Inputs with Currency
- Inputs with Time Formats
- Inputs with Dates
- Inputs with Unit of Measurements
- Inputs with Slang and Casual Phrasing
- Online Identifiers
- Inputs Containing Emojis

## Prerequisites

- Python 3.11 or 3.12
- Google Chrome browser recommended

## Installation

### 1. Clone or download this repository

```bash
git clone https://github.com/adrianAbeyrathne/playwright-singlish-tests-IT3040-ITPM-Assignment1.git
cd playwright-singlish-tests-IT3040-ITPM-Assignment1
```

### 2. Install Python dependencies

```bash
pip install -U pip
pip install playwright openpyxl
playwright install
```

## Running the Tests

Run the following command from the project directory:

```bash
python test_automation.py --excel "Assignment 1 - Test cases.xlsx" --url "https://www.pixelssuite.com/chat-translator" --wait-ms 5000 --type-delay-ms 80 --slow-mo-ms 200 --save-every 1 --keep-open
```

## Command Parameters Explained

| Parameter | Value | Description |
| --- | --- | --- |
| `--excel` | `"Assignment 1 - Test cases.xlsx"` | Excel file containing test cases |
| `--url` | `"https://www.pixelssuite.com/chat-translator"` | Target website URL |
| `--wait-ms` | `5000` | Wait time before starting in milliseconds |
| `--type-delay-ms` | `80` | Delay between keystrokes in milliseconds |
| `--slow-mo-ms` | `200` | Slow motion delay in milliseconds |
| `--save-every` | `1` | Save after each test case |
| `--keep-open` | `-` | Keep browser open after completion |

## Expected Results

- All 50 test cases should show FAIL status.
- The script automatically populates Actual Output and Status columns.
- Results are saved directly to the Excel file.

## Project Files

| File | Description |
| --- | --- |
| `test_automation.py` | Main Playwright automation script |
| `Assignment 1 - Test cases.xlsx` | Excel file with 50 test cases and results |
| `README.md` | Installation and usage guide |
| `git-repo-link.txt` | Public GitHub repository link |

## Submission Information

- Module: IT3040 - ITPM (IT Project Management)
- Year: 3
- Semester: 1
- Assignment: Option 1 - Transliteration Accuracy Testing
- Submitted to: CourseWeb

## Notes

- Do not open the Excel file while the script is running.
- The browser will remain open after completion due to the `--keep-open` flag.
- Git repository is publicly accessible as required by the assignment.
