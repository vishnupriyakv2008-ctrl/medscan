# MedScan AI — Intelligent Medical Report Analyzer
live link: https://medscan-omega.vercel.app/

A lightweight, responsive, single-page **front-end demo** for exploring medical laboratory reports. The interface uses a clean clinical-light theme with navy text, teal accents, and a dashboard-style layout.

## Features

- **Report ingestion:** Select PDF or image files (including scanned-report images) and review uploaded report entries.
- **Result entry and review:** Add or edit test names, values, units, and reference ranges in the demo.
- **Normalization concept:** Designed to group common aliases such as Hb, Hemoglobin, and HGB; standardize units and support LOINC-based mapping in a future clinical-grade implementation.
- **Reference-range comparison:** Compare values with available ranges and display normal, low, high, or critical-style flags using visual indicators.
- **Abnormality explanations:** Present findings in plain language and show how results relate to their reference ranges.
- **Pattern detection:** Demonstration rules highlight combinations that may merit review, such as iron-deficiency-like patterns, elevated glucose with HbA1c, lipid risk patterns, liver markers, kidney markers, inflammation markers, thyroid patterns, and multiple low blood counts.
- **Summary dashboard:** Overview cards for report/test counts, abnormal findings, priority items, and suggested follow-up categories.
- **Trend tracking:** Visualize sample test values over time and compare reports.
- **Urgency prioritization:** Routine / Soon / Urgent-style prioritization for demo findings; this is not a validated clinical risk score.
- **Multilingual interface:** Language selection for the demo interface and explanatory text where available, including Indian-language options.
- **General lifestyle guidance:** Broad, non-prescriptive wellness and diet information, kept separate from medical advice.
- **Report library and details:** Browse saved demo reports and inspect their results.
- **Patient profile:** Keep basic demo profile context for organizing reports.
- **Care summary and printing:** Review a concise summary and use browser printing where supported.
- **Data export:** Export supported report/result data to CSV or JSON.
- **Local persistence:** Demo data and settings can be retained in the browser using local storage.
- **Reference guide and safety information:** In-app explanations of result flags and the limits of automated interpretation.
- **Responsive interface:** Sidebar navigation and layouts adapt to smaller screens.

## Run locally

1. Download or clone this repository.
2. Open `index.html` in a modern browser.
3. No package installation, build step, database, or backend is required for the front-end demo.

If the website file in the repository has a different name, open that HTML file instead.

## Important implementation notes

This repository/demo is a **prototype, not a medical device or diagnostic system**.

- **OCR is not connected:** The upload flow accepts files for the demo, but it does not currently run Tesseract, PaddleOCR, or a vision model to extract report tables automatically. Enter or review values manually.
- **Not a validated clinical rules engine:** Sample reference ranges, pattern rules, severity indicators, and urgency labels are illustrative only. They may not be accurate for an individual or laboratory.
- **No diagnosis or treatment:** Findings are prompts for discussion with a qualified healthcare professional, not diagnoses, treatment recommendations, or emergency triage.
- **Normalization is a design direction:** Full LOINC mapping, reliable unit conversions, and age-/sex-aware range selection require validated datasets and careful clinical implementation.
- **Privacy:** Demo data may be stored in the browser's local storage. Avoid entering identifiable or sensitive real patient information into this prototype, especially on shared devices.
- **Clinical review required:** A production system should be clinically validated, security-reviewed, privacy-compliant, and tested with diverse reports before real-world use.

## Intended pattern examples

The demo may illustrate combinations such as:

- Low hemoglobin + low MCV + low ferritin — possible iron-deficiency pattern.
- High fasting glucose + high HbA1c — glucose regulation concern.
- High LDL + high triglycerides + low HDL — lipid profile concern.
- High ALT/AST + bilirubin — liver-marker pattern.
- High creatinine/urea + low eGFR — kidney-marker pattern.
- High WBC + high CRP/ESR — inflammation-related pattern.
- High TSH + low T4 — thyroid-marker pattern.
- Low platelets + low WBC + low hemoglobin — multiple low blood-count pattern.

These are educational examples only. They are not diagnostic criteria and must be interpreted in clinical context.

## Technology

- HTML, CSS, and vanilla JavaScript
- Browser local storage for demo persistence
- Client-side charts and report/result interactions
- No external backend required for the standalone prototype

## License

No license has been specified yet. Unless a license is added, the repository's contents are not automatically granted an open-source license.
