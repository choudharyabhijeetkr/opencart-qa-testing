# 🛒 OpenCart — Manual Testing QA Documentation

![Status](https://img.shields.io/badge/Status-Execution%20Complete-brightgreen)
![Test Cases](https://img.shields.io/badge/Test%20Cases-178-blue)
![Pass Rate](https://img.shields.io/badge/Pass%20Rate-82.6%25-green)
![Modules](https://img.shields.io/badge/Modules-8-orange)
![Type](https://img.shields.io/badge/Type-Manual%20Testing-purple)

A complete **manual testing QA documentation suite** for the [OpenCart (Frontend)](https://demo.opencart.com) e-commerce application, covering test scenarios, test cases, execution results, and defect tracking — all in a structured Excel workbook.

---

## 📁 Repository Contents

```
📦 opencart-qa-testing/
 ┣ 📄 README.md                                  ← You are here
 ┗ 📊 OpenCart_QA_TestDocumentation_WithActuals.xlsx  ← Main test document
```

---

## 📊 About the Test Document

**File:** `OpenCart_QA_TestDocumentation_WithActuals.xlsx`

The workbook contains **6 structured sheets**:

| Sheet | Description |
|---|---|
| 📋 Cover Page | Project metadata, tester info, and module-wise execution summary |
| 📌 Test Scenarios | All 8 test scenarios with priority, reference, and live pass/fail counts |
| 🧪 Module Sheets (×8) | Test cases per module with actual results, status, and defect references |
| 📈 Execution Tracker | All 178 TCs consolidated in one view for end-to-end traceability |
| 🐛 Defect Log | Isolated view of all Fail and Blocked test cases |
| 📊 Summary Dashboard | Overall pass rate, per-module stats, and status legend |

---

## ✅ Execution Summary

> **Application Under Test:** [demo.opencart.com](https://demo.opencart.com)
> **Total Test Cases:** 178 | **Overall Pass Rate: 82.6%**

| Module | Scenario ID | Priority | Total | ✅ Pass | ❌ Fail | 🚧 Blocked | Pass % |
|---|---|---|---|---|---|---|---|
| Register | TS_001 | P0 | 27 | 21 | 6 | 0 | 77.8% |
| Login | TS_002 | P0 | 23 | 18 | 4 | 1 | 78.3% |
| Logout | TS_003 | P0 | 11 | 9 | 2 | 0 | 81.8% |
| Forgot Password | TS_004 | P2 | 25 | 9 | 1 | 15 | 36.0% |
| Search | TS_005 | P1 | 22 | 21 | 1 | 0 | 95.5% |
| Product Compare | TS_006 | P4 | 24 | 24 | 0 | 0 | 100% |
| Product Display Page | TS_007 | P1 | 37 | 36 | 1 | 0 | 97.3% |
| Add to Cart | TS_008 | P1 | 9 | 9 | 0 | 0 | 100% |
| **TOTAL** | — | — | **178** | **147** | **15** | **16** | **82.6%** |

---

## 🐛 Key Defects Found

| Defect ID | Module | Description | Severity |
|---|---|---|---|
| OPENCART-BUG-1 | Register / Login | Confirmation email not received on account registration | High |
| OPENCART-BUG-9 | Logout | User gets logged back in on clicking browser Back after logout | High |
| — | Forgot Password | Application email system not working — 15 TCs blocked | Critical |
| — | Login | Multiple login edge-case failures | Medium |

> 📝 Full defect details (Actual Result vs Expected Result per TC) are available in the **Defect Log** sheet.

---

## 🗂️ Test Case ID Convention

| Module | Prefix | Example |
|---|---|---|
| Register | `TC_RF_` | `TC_RF_001` |
| Login | `TC_LF_` | `TC_LF_001` |
| Logout | `TC_LG_` | `TC_LG_001` |
| Forgot Password | `TC_FP_` | `TC_FP_001` |
| Search | `TC_SF_` | `TC_SF_001` |
| Product Compare | `TC_PC_` | `TC_PC_001` |
| Product Display Page | `TC_PDP_` | `TC_PDP_001` |
| Add to Cart | `TC_ATC_` | `TC_ATC_001` |

---

## 🏷️ Status Legend

| Status | Meaning |
|---|---|
| ✅ Pass | Test executed and actual result matches expected result |
| ❌ Fail | Test executed but actual result does NOT match expected result |
| 🚧 Blocked | Test could not be executed due to a blocker (e.g., email system down) |
| 🔄 In Progress | Test execution is ongoing |
| ⬜ Not Executed | Test has not yet been run |

---

## 🔢 Priority Scale

| Priority | Label | Meaning |
|---|---|---|
| 🔴 P0 | Critical | Must pass — showstopper if failed |
| 🟠 P1 | High | Core functionality, high business impact |
| 🟡 P2 | Medium | Important but not blocking |
| 🔵 P3 | Low | Edge cases, UI validations |
| 🟢 P4 | Informational | Nice-to-have coverage |

---

## 🛠️ Tools & Tech

| Area | Details |
|---|---|
| **Application** | OpenCart Frontend — [demo.opencart.com](https://demo.opencart.com) |
| **Testing Type** | Manual Functional Testing |
| **Documentation Tool** | Microsoft Excel (.xlsx) with openpyxl |
| **Test Management** | Custom Excel-based framework |
| **Bug Tracking** | Inline defect log (Defect ID column) |
| **Browsers Tested** | Chrome, Firefox (any supported browser) |

---

## 📌 How to Use This Document

1. **Download** `OpenCart_QA_TestDocumentation_WithActuals.xlsx`
2. **Open** in Microsoft Excel or Google Sheets
3. Navigate to the relevant **module sheet** (e.g., `Register`, `Login`)
4. Each row = one test case with: Pre-requisites → Steps → Test Data → Expected → **Actual Result** → **Status**
5. Use the **Execution Tracker** sheet for a full consolidated view
6. Use the **Defect Log** sheet to extract all failures for bug reporting
7. Use the **Summary Dashboard** for a quick health check of the release

---

