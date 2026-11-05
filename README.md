# OpenCart-E-Commerce---Manual-Testing
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
