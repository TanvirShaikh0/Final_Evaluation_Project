# ZigWheels New Bikes & Used Cars Automation

Automates the extraction and validation of upcoming Honda bikes and popular used cars on ZigWheels using Selenium WebDriver, TestNG, and Cucumber. The suite supports multi-browser execution, dynamic form handling, screenshot capture, and data-driven testing for validating extracted results.

---

## Project Overview

This project simulates a user extracting upcoming Honda bikes (under 4 lakh INR), listing popular used car models in Chennai, and validating login error handling. It validates the correctness of extracted data, logs relevant test data, captures screenshots, and generates detailed HTML and Allure reports.

---

## Problem Statement

Automate the following on ZigWheels (or a similar site):

- Display upcoming Honda bikes (name, price, expected launch date) with price < 4 lakh INR
- List all popular used car models in Chennai
- Attempt Google login with invalid credentials and capture the error message

---

## Automation Scope

- Multi-browser support (Chrome, Firefox, Edge)
- Extraction of dynamic content (bikes, cars, error messages)
- Handling windows, frames, and popups
- Form filling and warning message capture
- Screenshot capture on success/failure
- Data-driven testing (Excel/CSV)
- Rich reporting with Allure and ExtentReports
- Page Object Model for modular code

---

## Tech Stack

- **Java** – Core programming language
- **Selenium WebDriver** – Browser automation
- **TestNG** – Testing framework
- **Cucumber** – BDD support
- **Apache POI** – For reading Excel files
- **ExtentReports** – HTML reports
- **Allure** – Advanced reporting
- **WebDriverManager** – Manages browser drivers
- **Log4j** – Logging
- **Page Object Model (POM)** – Clean, maintainable test structure

---

## Project Structure
```
ZigWheels/
├── src/
│   ├── main/
│   │   ├── java/
│   │   │   └── com/zigwheels/
│   │   │       ├── base/
│   │   │       ├── pages/
│   │   │       ├── utilities/
│   │   │       ├── models/
│   │   │       ├── listeners/
│   │   │       ├── hooks/
│   │   └── resources/
│   │       └── config.properties
│   └── test/
│       ├── java/
│       │   └── com/zigwheels/
│       │       ├── tests/
│       │       └── stepDefination/
│       │       └── testRunner/
│       └── resources/
│           └── features
│           └── testdata
├── test-output/
│   ├── ExtentReport.html
│   └── screenshots/
├── testng.xml
├── cucumber_testng.xml
├── pom.xml
└── README.md
```
---
## Test Case Scenarios

### Test Case 1: Upcoming Honda Bikes Extraction

**Objective**: Extract and display upcoming Honda bikes (name, price, expected launch date) with price < 4 lakh INR.

**Steps**:
1. Navigate to ZigWheels upcoming bikes section.
2. Filter by manufacturer 'Honda'.
3. Extract bike name, price, and expected launch date for each bike under 4 lakh INR.
4. Log and display the extracted data.

**Expected Result**:
- List of upcoming Honda bikes under 4 lakh INR with all required details.

**Validation**:
- Assert that all bikes are Honda and price < 4 lakh INR.
- Capture screenshot of the results.

---

### Test Case 2: Popular Used Cars in Chennai

**Objective**: Extract and display all popular used car models in Chennai.

**Steps**:
1. Navigate to ZigWheels used cars section.
2. Select city as Chennai.
3. Extract all popular used car models.
4. Log and display the extracted models.

**Expected Result**:
- List of popular used car models in Chennai.

**Validation**:
- Assert that all models are listed and city is Chennai.
- Capture screenshot of the results.

---

### Test Case 3: Google Login Error Handling

**Objective**: Attempt Google login with invalid credentials and capture the error message.

**Steps**:
1. Navigate to ZigWheels login page.
2. Choose Google login.
3. Enter invalid credentials.
4. Capture and log the error message.

**Expected Result**:
- Proper error message is displayed for invalid login.

**Validation**:
- Assert that the error message is captured and matches expected text.
- Capture screenshot of the error.

---

## Setup Instructions

1. Clone the repository
   git clone https://github.com/<your-username>/zigwheels-automation.git
2. Install dependencies
   mvn clean install
3. Configure environment (browser, URLs) in config.properties

---

## Running Tests

### From Command Line
mvn test

### Run with Specific Browser
Set browser in config.properties:
browser=chrome

### From IDE
- Right-click on testng.xml → Run as TestNG Suite
- Or run any test class directly

---

## Reports and Screenshots
- Allure Report: allure-report/index.html
- Extent Report: test-output/ExtentReport.html
- Screenshots: screenshots/ or test-output/screenshots/

---

## Best Practices Implemented
- Page Object Model with PageFactory
- Explicit waits for dynamic elements
- Excel-driven testing with Apache POI
- Screenshot capture on failure and success
- Integration with Allure and ExtentReports
- Cross-browser support
- Modular and reusable architecture
