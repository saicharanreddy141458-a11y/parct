# Branch Operations Data Generation Sprint Plan

## Overview
We are generating synthetic but realistic data for HDFC Bank branches (Siruseri, Navalur, T Nagar) without changing the existing schema defined in `AI_DATABASE_SCHEMA_DOCUMENTATION.md`.  
Each sprint will progressively increase the dataset size and realism while ensuring schema compliance.

---

## Sprint 1: Small Dataset (Initial Pilot)
- Generate ~150 rows of data (covering 1 week).
- Focus on branch-level daily footfall and service usage.
- Ensure `Footfall_Percentage` sums to 100% per branch per day.
- Validate with user for correctness and realism.

## Sprint 2: Data Cleaning & Validation
- If Sprint 1 data is clean and realistic → no major changes.
- If issues are found → clean and regenerate corrected data.
- Expand to ~500 rows (covering 2–3 weeks).
- Check branch-specific service usage (e.g., more loan queries in T Nagar).

## Sprint 3: Medium Dataset
- Generate ~2,000 rows (covering ~2 months).
- Add realistic temporal variations:
  - Mondays → high loan activity.
  - Fridays → more teller transactions.
  - Lunch hours → dip in transactions.
- Recheck that percentages and totals are consistent.

## Sprint 4: Large Dataset
- Generate ~10,000 rows (covering ~6 months).
- Add seasonal patterns:
  - Salary days (1st/last of month) → spike in transactions.
  - Festival seasons → higher branch activity.
- Ensure staff scheduling aligns with footfall.

## Sprint 5: Final Production-Scale Dataset
- Generate ~50,000 rows (covering ~1 year).
- Include anomaly cases:
  - Sudden footfall drop (e.g., branch closed for maintenance).
  - Unexpected peak due to government announcements.
- This dataset will be used to train/test LLM (e.g., Nova on Bedrock).
- Provide final validated dataset to user for integration.

---

## Verification After Each Sprint
- After each sprint, the generated dataset will be shared with the user.
- User confirms correctness, realism, and schema compliance.
- Only after user approval, the next sprint begins.
