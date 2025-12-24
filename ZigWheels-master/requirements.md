# Project Requirements: ZigWheels New Bikes & Used Cars Automation

## Overview
This document outlines the requirements for automating the extraction and validation of upcoming Honda bikes, popular used cars in Chennai, and login error handling on ZigWheels (or a similar site).

---

## Problem Statement
Automate the following:
- Display upcoming Honda bikes (name, price, expected launch date) with price < 4 lakh INR
- List all popular used car models in Chennai
- Attempt Google login with invalid credentials and capture the error message

---

## Functional Requirements
1. Extract and display details of upcoming bikes (name, price, expected launch date) for manufacturer 'Honda' with price < 4 lakh INR.
2. Extract and display all popular used car models in Chennai.
3. Attempt to login with Google using invalid credentials and capture the error message.
4. Handle windows, frames, and popups during navigation and data extraction.
5. Fill forms and capture warning messages.
6. Extract menu items from frames and store them in collections.
7. Navigate back to the home page after each operation.
8. Support multi-browser execution (Chrome, Firefox, Edge).
9. Capture screenshots on success and failure.
10. Generate detailed HTML and Allure reports.
11. Support data-driven testing using Excel/CSV files.
12. Use Page Object Model for modular and maintainable code.

---

## Non-Functional Requirements
1. The framework should be modular, maintainable, and follow best coding practices (e.g., Page Object Model).
2. The system should support cross-browser testing (Chrome, Firefox, Edge).
3. The framework should be compatible with Windows OS and ideally support Linux/Mac.
4. Test execution should be efficient and scalable, supporting parallel execution.
5. The framework should provide clear documentation for setup, usage, and troubleshooting.

---

## User Stories & Acceptance Criteria
- **As a user, I want to see a list of upcoming Honda bikes under 4 lakh INR, so I can plan my purchase.**
  - *Acceptance:* The system displays bike name, price, and expected launch date for all matching bikes.
- **As a user, I want to see all popular used car models in Chennai, so I can consider buying a used car.**
  - *Acceptance:* The system displays a list of popular used car models in Chennai.
- **As a tester, I want to verify login error handling, so I can ensure proper feedback is given for invalid credentials.**
  - *Acceptance:* The system attempts Google login with invalid details and captures the error message.

---

## Tech Stack & Tools
- **Java** (11)
- **Selenium WebDriver** (4.34.0)
- **TestNG** (7.11.0)
- **Cucumber** (7.14.0)
- **JUnit** (4.13.2)
- **Allure** (2.29.1)
- **ExtentReports** (5.1.2)
- **Apache POI** (5.4.1)
- **Log4j** (2.25.1)
- **SLF4J** (2.0.9)
- **WebDriverManager**
- **Maven** (build, dependency management)

---

## Directory Structure
- `src/` - Source code and test scripts (organized by modules/pages)
- `allure-results/` - Allure raw results
- `allure-report/` - Allure HTML reports
- `logs/` - Log files
- `screenshots/` - Captured screenshots
- `test-output/` - TestNG output
- `pom.xml` - Maven project file
- `run.bat` - Batch script for running tests on Windows

---

## Setup & Usage
1. Clone the repository.
2. Install Java and Maven.
3. Run `mvn clean install` to install dependencies.
4. Configure environment (browser, URLs) in config.properties.
5. Use `mvn test` or `run.bat` to execute tests.
6. View reports in the `allure-report/` and `test-output/` directories.

---

## Authors
- [Pravin, Archi, Shivprasad, Tanvir]

## Revision History
- 2025-09-01: Updated for ZigWheels new bikes & used cars automation case study
