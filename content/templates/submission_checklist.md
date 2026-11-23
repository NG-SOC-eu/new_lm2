# Submission checklist — Exercise ___ (banking / energy)

Work through this before you open the **Deliverables submission** level in the
platform.

## In RITA (https://ng-soc.eurodyn.com/)

- [ ] At least 5 assets registered, with owner and description.
- [ ] At least 5 threats mapped to those assets (STRIDE + ATT&CK reference).
- [ ] Vulnerabilities linked to the threats.
- [ ] Risk evaluation completed for every threat (likelihood + impact).
- [ ] Existing controls and recommended treatments documented.
- [ ] Results exported and the file saved in this folder as
      `rita_export.csv` (or `.json`).

## In this folder (`~/deliverables/exercise<N>/`)

- [ ] `threat_model.md` — assets, flows and threat scenarios filled in.
- [ ] `risk_register.csv` — one row per risk, all columns completed.
- [ ] `risk_matrix.md` — every risk ID placed in a cell, ranking table filled.
- [ ] `risk_treatment_plan.md` — treatments prioritised, accepted risks recorded.
- [ ] `executive_summary.md` — one page, no jargon.
- [ ] Any screenshot or diagram saved here with a descriptive name.

## In the platform

- [ ] Answer every question of the **Deliverables submission** level, copying the
      key lines from the files above.
- [ ] The risk IDs you use in the answers match the ones in your files.

## Verify your files are readable

```bash
cd ~/deliverables/exercise1     # or exercise2
ls -l
column -s, -t < risk_register.csv | less -S
```
