# Risk matrix — Exercise ___ (banking / energy)

Trainee: ______________________   Date: ____________

## How to fill it in

1. Rate every threat scenario from `threat_model.md` for **likelihood** and
   **impact** using the scales below.
2. Write its `risk_id` (R01, R02, ...) into the matching cell. A cell can hold
   several IDs, separated by spaces.
3. The colour band of the cell gives the risk level. Copy it back into the
   `risk_level` column of `risk_register.csv`.

### Likelihood scale

| Level | Meaning |
|-------|---------|
| Very Low | Not expected in the lifetime of the system; requires rare conditions. |
| Low | Possible but not expected in the next 12 months. |
| Medium | Plausible once in the next 12 months. |
| High | Expected at least once in the next 12 months. |
| Very High | Ongoing or expected repeatedly; attempts already observed. |

### Impact scale

| Level | Business / operational meaning | ICS safety meaning |
|-------|-------------------------------|--------------------|
| Very Low | Negligible, absorbed by normal operations. | No effect on the physical process. |
| Low | Minor service degradation, no regulatory duty. | Process deviation corrected automatically. |
| Medium | Service interruption, internal escalation, limited data loss. | Manual intervention required, no danger. |
| High | Major outage, regulatory notification, significant financial or data loss. | Equipment damage or unplanned shutdown. |
| Critical | Existential: licence, solvency or public trust at stake. | Risk to human life or to grid stability. |

## Matrix (write the risk IDs in the cells)

| Impact \ Likelihood | Very Low | Low | Medium | High | Very High |
|---------------------|----------|-----|--------|------|-----------|
| **Critical**        |          |     |        |      |           |
| **High**            |          |     |        |      |           |
| **Medium**          |          |     |        |      |           |
| **Low**             |          |     |        |      |           |
| **Very Low**        |          |     |        |      |           |

## Risk level bands

| Band | Cells | Action expected |
|------|-------|-----------------|
| Critical | Impact Critical with likelihood Medium or above; Impact High with likelihood Very High | Immediate treatment, escalate to leadership. |
| High | Impact High with likelihood Medium/High; Impact Critical with likelihood Very Low/Low | Treat within the current planning cycle. |
| Medium | Impact Medium with likelihood Medium or above; Impact High with likelihood Very Low/Low | Treat or formally accept with an owner and a review date. |
| Low | Everything else | Accept and monitor. |

## Ranked risks

Copy the outcome here, highest residual risk first. The RITA score is the one
calculated on the asset's **Risk Evaluation** screen.

| Rank | risk_id | Likelihood | Impact | Risk level | RITA score |
|------|---------|------------|--------|------------|------------|
| 1 |  |  |  |  |  |
| 2 |  |  |  |  |  |
| 3 |  |  |  |  |  |
| 4 |  |  |  |  |  |
| 5 |  |  |  |  |  |
