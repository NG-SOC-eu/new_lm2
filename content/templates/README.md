# Deliverable templates

These are the working files you fill in during the exercises. They are copied to
the analyst machine of each scenario during provisioning:

- Exercise 1 (banking): `bank-analyst:/home/debian/deliverables/exercise1/`
- Exercise 2 (energy/ICS): `corp-workstation:/home/debian/deliverables/exercise2/`

If they are missing, download them from the repository or recreate them by hand.

| File | Deliverable it supports |
|---|---|
| `risk_register.csv` | Asset / threat / risk register. Also the import-export format for RITA. |
| `threat_model.md` | Threat model table (assets, STRIDE, ATT&CK, attack path). |
| `risk_matrix.md` | 5x5 likelihood vs. impact matrix, filled with risk IDs. |
| `risk_treatment_plan.md` | Prioritised mitigations and residual risk. |
| `executive_summary.md` | One-page summary for leadership. |
| `submission_checklist.md` | What has to be done before you submit. |

## How to edit them

The tables are plain text, so they are writable — unlike the read-only tables in
the exercise description. Any of these works:

```bash
cd ~/deliverables/exercise1
nano risk_register.csv          # terminal editor
mousepad risk_matrix.md         # graphical editor (Kali desktop)
libreoffice --calc risk_register.csv   # spreadsheet view of the register
```

Keep the column separators (`,` in CSV, `|` in Markdown) so the files stay
machine-readable and can be imported back into RITA.

## Where the answers finally go

Filling these files is not the submission. After each exercise the platform
shows a **Deliverables submission** questionnaire level: copy the key lines from
these files into the answer fields there. That is what the instructor sees and
grades. The files and the RITA export are the supporting evidence.
