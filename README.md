# Pentest Finding Generator — Excel VBA Tool

## Purpose

This tool was created to help penetration testers and security professionals **document, organize, and report web application vulnerabilities** in a structured and professional format — all within Microsoft Excel without needing any external software.

During a web application penetration test, testers often discover multiple vulnerabilities across different severity levels. Manually writing up findings in a report is time-consuming and error-prone. This generator solves that by providing:

- A **standardized input form** to log each finding consistently with title, evidence, severity, CVSS score, CWE reference, status, and remediation advice
- An **automated summary dashboard** that calculates risk scores, counts findings by severity, and visualizes data with charts — generated at the click of a button via VBA macro
- A **detailed report sheet** that auto-populates from the input form using Excel formulas, keeping everything in sync
- A **one-click PDF export** to produce a client-ready deliverable without reformatting

The tool is designed to be used during or immediately after an engagement, reducing report writing time and ensuring no findings are missed or inconsistently documented.

**Intended users:** Penetration testers, red teamers, bug bounty hunters, security consultants, and students learning web application security.

---

## Files
- `PentestFindingGenerator.xlsm` — Main workbook (macro-enabled Excel)
- `PentestMacros.bas` — VBA module to import into the workbook

## Setup (one-time)
1. Open `PentestFindingGenerator.xlsm` in Excel
2. Press **Alt+F11** to open VBA Editor
3. Right-click on your workbook in the Project pane → **Import File...**
4. Select `PentestMacros.bas`
5. Close VBA Editor and **Enable Macros** when prompted

## How to Use
| Sheet | Purpose |
|---|---|
| 📋 Input Form | Enter engagement details and findings |
| 📊 Summary | Auto-calculated dashboard + charts |
| 📄 Detailed Report | Formula-linked detailed view |
| ℹ️ Instructions | Full usage guide |

## Macros (Alt+F8 to run)
| Macro | What it does |
|---|---|
| `GeneratePentestReport` | Refresh all sheets, apply color coding, update charts |
| `ExportToPDF` | Export Summary + Detailed Report as PDF |
| `ClearAllFindings` | Reset findings table |
| `AddFindingRow` | Add a new pre-formatted finding row |

## Severity Color Codes
- 🟥 **Critical** (CVSS 9–10)
- 🔴 **High** (CVSS 7–8.9)
- 🟠 **Medium** (CVSS 4–6.9)
- 🟡 **Low** (CVSS 0.1–3.9)
- 🔵 **Info** (CVSS 0)
