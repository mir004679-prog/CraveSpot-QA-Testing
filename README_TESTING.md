# CraveSpot — QA & Testing Engineer Package

Welcome to the **Quality Assurance & Testing** workspace for CraveSpot!

## 📦 What's Included in This Package
- `tests/`
  - `test_backend.py` — Python `unittest` test suite covering core routes, auth, rate-limiting, and error handling
  - `manual_test.py` — Comprehensive 262-assertion integration test runner with live API outputs
  - `manual_test.ps1` — PowerShell test runner script
  - `simulate_user.py` — End-to-end user journey simulation script
  - `capture_website_screenshots.py` — Automated Selenium script to capture live UI screenshots
  - `generate_test_images.py` — Visual test artifact generator
  - `API_TEST_RESULTS.md` & `.json` — Documented test outputs for all 22 live API endpoints
  - `test_images/` — 5 actual high-resolution live website verification screenshots
- `requirements.txt` — Dependencies needed for running tests (unittest, requests, selenium)

## 🚀 How to Run the Test Suites
### 1. Run Unit Tests (In-Process)
```bash
python -m unittest tests/test_backend.py
```
**Expected**: `Ran 15 tests ... OK` (100% pass)

### 2. Run Comprehensive Integration & API Tests
Ensure MySQL database `CraveSpot` is running, then execute:
```bash
python tests/manual_test.py
```
**Expected**: `PASSED: 262 | FAILED: 0 | SCORE: 100%`

### 3. Capture Fresh Website Screenshots
Ensure backend (port 5000) and frontend (port 5500) are running:
```bash
python tests/capture_website_screenshots.py
```

## 🎯 QA & Testing Team Responsibilities
1. Run regression tests before every deployment.
2. Validate HTTP response codes, JSON schemas, and security headers.
3. Test edge cases (missing params, invalid coordinates, expired tokens).
4. Verify cross-browser visual fidelity using automated screenshots.
