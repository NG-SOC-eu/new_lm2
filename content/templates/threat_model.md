# Threat model — Exercise ___ (banking / energy)

Trainee: ______________________   Date: ____________

## 1. Assets in scope

One row per asset. Use the same asset names you registered in RITA.

| # | Asset | Host / component | Owner | C | I | A | Why it is critical |
|---|-------|------------------|-------|---|---|---|--------------------|
| A1 |      |                  |       |   |   |   |                    |
| A2 |      |                  |       |   |   |   |                    |
| A3 |      |                  |       |   |   |   |                    |
| A4 |      |                  |       |   |   |   |                    |
| A5 |      |                  |       |   |   |   |                    |

`C`, `I`, `A` = confidentiality, integrity, availability. Rate each `High`,
`Medium` or `Low`.

## 2. Trust boundaries and data flows

Describe each flow that crosses a trust boundary (internet -> DMZ, DMZ ->
internal, corporate IT -> OT, ...).

| # | From | To | Protocol / port | Boundary crossed | Authenticated? | Encrypted? |
|---|------|----|-----------------|------------------|----------------|------------|
| F1 |     |    |                 |                  |                |            |
| F2 |     |    |                 |                  |                |            |
| F3 |     |    |                 |                  |                |            |
| F4 |     |    |                 |                  |                |            |

## 3. Threat scenarios (STRIDE + MITRE ATT&CK)

One row per threat scenario. The `risk_id` must match the one you use in
`risk_register.csv` and `risk_matrix.md`.

| risk_id | Asset (#) | Flow (#) | STRIDE category | ATT&CK technique (ID + name) | Attack path (entry -> target) | Vulnerability enabling it |
|---------|-----------|----------|-----------------|------------------------------|-------------------------------|---------------------------|
| R01 |  |  |  |  |  |  |
| R02 |  |  |  |  |  |  |
| R03 |  |  |  |  |  |  |
| R04 |  |  |  |  |  |  |
| R05 |  |  |  |  |  |  |

STRIDE categories: Spoofing, Tampering, Repudiation, Information disclosure,
Denial of service, Elevation of privilege.

## 4. Diagram (optional)

If you draw a data-flow diagram, save it in this folder as `threat_model.png`
and note the file name here: ____________________
