# OpenCart E-Commerce End-to-End Test Suite (150+ Test Cases)

[![QA - Manual Testing](https://img.shields.io/badge/QA-Manual%20Testing-blue.svg)](https://github.com/)
[![Test Cases - 155 Total](https://img.shields.io/badge/Test%20Cases-155%20Total-brightgreen.svg)](https://github.com/)
[![Platform - OpenCart](https://img.shields.io/badge/Platform-OpenCart-orange.svg)](https://demo.opencart.com)
[![Status - Production Ready](https://img.shields.io/badge/Status-Production%20Ready-success.svg)](https://github.com/)

---

## 📌 Executive Summary

This repository contains an industry-standard, production-ready manual test suite comprising **155 comprehensive test cases** created for the OpenCart E-Commerce platform ([demo.opencart.com](https://demo.opencart.com)).

Designed using professional Software Testing Life Cycle (STLC) practices, the suite covers critical e-commerce functional areas, edge cases, negative scenarios, boundary value analyses, and security validations (XSS/SQL injection prevention).

The test cases are structured using the **14-column industry-standard schema** with dynamic Excel formulas, automated pass-rate KPIs, conditional formatting, and interactive execution dropdowns.

---

## 🛠️ Test Environment Architecture

As outlined in the test environment specifications, the test suite is configured for the following environment matrix:

| Category | Specification / Configuration Details |
| :--- | :--- |
| **Target Application** | OpenCart Web Application ([demo.opencart.com](https://demo.opencart.com)) |
| **Browsers** | Google Chrome (v120+), Mozilla Firefox (v121+), Apple Safari (v17+), Microsoft Edge |
| **Operating Systems** | Windows 11, macOS Sonoma, Ubuntu Linux 22.04 LTS, Android 14, iOS 17 |
| **Test Management & Tools** | Microsoft Excel, Jira / Bugzilla (Defect Tracking), Selenium WebDriver, JMeter |
| **Network & Security** | Minimum 10 Mbps Broadband, SSL/TLS Encryption (HTTPS Enabled), Port 443 |
| **Test Data Sandbox** | Pre-configured customer accounts, valid/invalid credit cards, sandbox coupons |

---

## 📊 Modules & Coverage Breakdown

The test suite covers **155 test cases** across **7 core e-commerce modules**:

```text
├── 01. User Registration (30 Cases)
├── 02. User Authentication & Login (25 Cases)
├── 03. Product Catalog, Search & Navigation (25 Cases)
├── 04. Shopping Cart Management (25 Cases)
├── 05. Multi-Step Checkout Process (25 Cases)
├── 06. Payment Gateway Integration (15 Cases)
└── 07. Order History & Management (10 Cases)
```

### Module Summary Table

| Module ID | Module Name | Requirement ID | Test Cases | Testing Scope & Types Covered |
| :---: | :--- | :---: | :---: | :--- |
| **MOD-01** | **User Registration** | REQ-01 | 30 | Mandatory/Optional field validation, duplicate email checks, password strength rules, XSS/SQLi injection, confirmation emails. |
| **MOD-02** | **Login & Authentication** | REQ-02 | 25 | Valid/invalid credentials, password reset flows, account lockout policy, multi-tab sessions, HTTPS security checks. |
| **MOD-03** | **Product Catalog & Search** | REQ-03 | 25 | Category menus, keyword search, partial matching, grid/list toggles, price sorting, currency selector, stock indicators. |
| **MOD-04** | **Shopping Cart** | REQ-04 | 25 | Add to cart from PDP/PLP, quantity adjustments, item removal, discount coupon/voucher redemption, session persistence. |
| **MOD-05** | **Checkout Process** | REQ-05 | 25 | Guest vs Registered checkout, billing/shipping address forms, shipping methods, order review, idempotency checks. |
| **MOD-06** | **Payment Gateway** | REQ-06 | 15 | Cash on Delivery (COD), test credit cards, declined card scenarios, 3D Secure OTP verification, SSL transaction payloads. |
| **MOD-07** | **Order History** | REQ-07 | 10 | Customer order history dashboard, detailed order view, invoice printing, product reordering, return requests (RMA). |

---

## 📁 Repository Structure

```text
├── README.md                                     # Comprehensive Project Documentation
├── OpenCart_Manual_Test_Cases_150_SBI_Style.xlsx # Primary Master Excel Test Suite File
└── docs/
    ├── Requirement_Specification.pdf             # Business Requirements & User Stories
    └── Test_Environment_Config.pdf              # Test Hardware/Software Specifications
```

---

## 📋 Test Case Schema & Layout Structure

The master workbook strictly adheres to standard enterprise QA formats, utilizing a **14-column layout**:

1. **`Test Case ID`**: Unique identifier (e.g., `TC_REG_001`, `TC_LOG_001`).
2. **`Module`**: Functional area under test.
3. **`Test Scenario / Title`**: Concise description of the test objective.
4. **`Preconditions`**: Required setup state before execution.
5. **`Test Steps`**: Clear, step-by-step instructions.
6. **`Test Data`**: Specific inputs used during testing.
7. **`Expected Result`**: Expected system behavior.
8. **`Priority`**: Severity level (`High`, `Medium`, `Low`).
9. **`Test Type`**: Classification (`Functional`, `Boundary`, `Security`, `UI/UX`, `Usability`).
10. **`Execution Status`**: Interactive dropdown (`Not Run`, `Pass`, `Fail`, `Blocked`, `Not Applicable`).
11. **`Actual Result`**: Observed behavior during execution.
12. **`Defect ID`**: Reference ID for tracked issues (e.g., `BUG-101`).
13. **`Tester`**: Designated QA Engineer.
14. **`Execution Date`**: Timestamp of test execution.

---

## 📈 Excel Workbook Features

- **Automated Summary Dashboard (`Execution Summary` Sheet):**
  - Live metric cards calculating Total Cases, Passed, Failed, Blocked, and Not Run counts dynamically using `COUNTA`, `COUNTIF`, and `IFERROR` formulas.
  - Automated Pass Percentage (`%`) completion bar calculations.
- **Interactive Data Validation:** Dropdown options configured for the `Execution Status` column.
- **Conditional Formatting:**
  - **Priorities:** Soft visual fills for `High` (Light Red), `Medium` (Light Yellow), and `Low` (Light Green).
  - **Statuses:** Muted fills for `Pass` (Green), `Fail` (Red), and `Not Run` (Gray).
- **Usability Formats:** Auto-filters enabled, frozen header panes, auto-fitted row wrapping, and professional typography.

---

## 🧪 Sample Test Cases Preview

### Module 1: Registration (`TC_REG_001` - Positive Case)
- **Title:** Verify registration with all valid mandatory fields.
- **Preconditions:** User is on the OpenCart home page; test email account accessible.
- **Steps:**
  1. Click on "My Account" drop-down and select "Register".
  2. Enter valid First Name, Last Name, Email, and Telephone.
  3. Enter valid Password and Confirm Password.
  4. Select "Privacy Policy" checkbox and click "Continue".
- **Expected Result:** Account created successfully; user redirected to "Your Account Has Been Created!" success page.
- **Priority:** High | **Test Type:** Functional

### Module 2: Login (`TC_LOG_009` - Security / Negative Case)
- **Title:** Verify system defense against SQL Injection payload in login form.
- **Preconditions:** User is on the Login page (`index.php?route=account/login`).
- **Steps:**
  1. Enter `' OR '1'='1` in the E-Mail Address input field.
  2. Enter `' OR '1'='1` in the Password input field.
  3. Click "Login" button.
- **Expected Result:** System rejects login attempt, displays error message: *"Warning: No match for E-Mail Address and/or Password."* No database exception thrown.
- **Priority:** High | **Test Type:** Security

---

## 🚀 How to Use This Suite

1. **Clone the Repository:**
   ```bash
   git clone https://github.com/your-username/opencart-manual-test-suite.git
   ```
2. **Open in Microsoft Excel or Google Sheets:**
   - Open `OpenCart_Manual_Test_Cases_150_SBI_Style.xlsx`.
3. **Execute Test Cases:**
   - Navigate to the `Test Cases` sheet.
   - Execute test steps on the live application ([demo.opencart.com](https://demo.opencart.com)).
   - Update the `Execution Status` column via the interactive dropdown.
   - Enter `Actual Result` and log `Defect ID` if a failure occurs.
4. **Monitor Progress:**
   - Switch to the `Execution Summary` tab to view real-time metrics and pass/fail distribution charts.

---

## 👤 Author & Contact

- **QA Engineer:** [Your Name]
- **LinkedIn:** [Your LinkedIn Profile URL]
- **Email:** [Your Email Address]
- **Portfolio:** [Your Portfolio Website URL]