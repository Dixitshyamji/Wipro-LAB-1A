# Wipro LAB-1A — Swift Basics, Variables, Types & Operators
### Student Grade Calculator

## Objective
Demonstrate Swift's type system and operators by building a student grade calculator that:
- Stores student data with correct types
- Calculates total, average, percentage, and pass/fail status
- Demonstrates all required operator categories
- Assigns grades using `if/else` and `switch`
- Validates boundary values

---

## Files
| File | Description |
|------|-------------|
| `main.swift` | Complete Swift source covering all 5 tasks |
| `README.md` | This file — includes test table |

---

## How to Run

**Option A — Swift CLI (macOS/Linux)**
```bash
swift main.swift
```

**Option B — Xcode Playground**
Paste `main.swift` content into a new Playground and run.

**Option C — Online**  
Paste into [https://swiftfiddle.com](https://swiftfiddle.com) and click **Run**.

---

## Test Table (8+ Input/Output Cases)

| # | Input (Marks: M/S/E/H/C) | Attendance | Expected Total | Expected % | Expected Grade | Expected Status | Boundary / Notes |
|---|--------------------------|-----------|---------------|-----------|---------------|----------------|-----------------|
| 1 | 88, 76, 92, 65, 95 | 85.5% | 416 | 83.2% | A | PASS | Normal case (default input) |
| 2 | 100, 100, 100, 100, 100 | 100.0% | 500 | 100.0% | A+ | PASS | All perfect scores |
| 3 | 0, 0, 0, 0, 0 | 0.0% | 0 | 0.0% | F | FAIL | All zero — lower boundary |
| 4 | 40, 40, 40, 40, 40 | 75.0% | 200 | 40.0% | F | PASS | Exactly passing mark (40) each |
| 5 | 39, 40, 40, 40, 40 | 74.9% | 199 | 39.8% | F | FAIL | One subject fails; attendance below 75% |
| 6 | 90, 85, 88, 92, 95 | 95.0% | 450 | 90.0% | A+ | PASS | A+ boundary (≥90%) |
| 7 | 70, 72, 68, 75, 65 | 76.0% | 350 | 70.0% | B | PASS | B grade boundary (≥70%) |
| 8 | 50, 55, 60, 52, 58 | 50.0% | 275 | 55.0% | D | PASS (marks) ⚠️ | Passes marks but attendance < 75% |
| 9 | -5, 105, 40, 40, 40 | -1.0% | — | — | Invalid | Invalid | Out-of-range marks + attendance |
| 10 | 59, 60, 61, 62, 58 | 74.9% | 300 | 60.0% | C | PASS | C grade boundary; attendance just below 75% |

### Grade Scale
| Percentage | Grade | Remark |
|-----------|-------|--------|
| ≥ 90% | A+ | Outstanding |
| ≥ 80% | A | Excellent |
| ≥ 70% | B | Good |
| ≥ 60% | C | Average |
| ≥ 50% | D | Below Average |
| < 50% | F | Fail – Needs Improvement |

### Pass/Fail Rule
- **PASS**: All 5 subjects must have marks ≥ 40
- **FAIL**: Any subject below 40

---

## Operator Coverage Summary

| Category | Example in Code |
|----------|----------------|
| Arithmetic (`+`, `-`, `*`, `/`, `%`) | `total`, `average`, `percentage` calculation |
| Comparison (`>`, `<`, `==`, `<=`) | Grade thresholds, pass check |
| Logical (`&&`, `\|\|`, `!`) | `overallOK`, `needsSupport` |
| Compound-assignment (`+=`, `-=`, `*=`) | `tempScore` modification |
| Nil-coalescing (`??`) | `displayGrade` fallback |

---

*Submitted by: Shyam Dixit | Roll: 101 | Wipro LAB-1A*
