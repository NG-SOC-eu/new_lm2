# Solution for Exercise 1: Banking Sector

## Expected findings
- Complete inventory of critical assets (core banking, digital channels, SWIFT, customer databases).
- Map of dependencies between applications and third parties, including cloud service providers and payment processors.
- Identification of relevant threats based on MITRE ATT&CK for financial environments (e.g. targeted phishing, credential abuse, data exfiltration).
- Assessment of existing controls (multi-factor authentication, fraud monitoring, segregation of duties) and gaps.

## Identified risks
- Compromise of privileged credentials that enables fraudulent transfers or manipulation of accounting records.
- Ransomware attacks against payment servers with a direct impact on service availability and regulatory compliance.
- Exfiltration of sensitive customer data with regulatory (PSD2, GDPR) and reputational consequences.
- Critical dependency on an external supplier without robust continuity plans.

## Recommended mitigations
- Implement privileged access management (PAM) with continuous monitoring and automatic credential rotation.
- Strengthen phishing detection with awareness campaigns, advanced filtering, and reinforced authentication.
- Establish network segmentation and regularly tested immutable backups to mitigate ransomware.
- Formalise service level agreements (SLAs) and contingency plans with key third parties; conduct recovery tests.
- Integrate anomalous behaviour alerts into the SIEM and define incident response procedures coordinated with business areas.

## Reference answers for the submission questionnaire

The **Exercise 1 – Deliverables submission** level is a questionnaire
(`ASSESSMENT_LEVEL`, type `QUESTIONNAIRE`): nothing is auto-graded, so the
instructor reviews the answers against this key.

### Rating grids (questions 4 and 5)

Reference ratings for the fixed scenario list. Accept one band either way when
the trainee justifies it in the free-text answers; challenge anything further
out, and in particular any answer that rates S2 or S5 below `High` impact.

| Scenario | Likelihood | Impact | Comment |
|---|---|---|---|
| S1 Credential stuffing against the portal | Very High | High | Continuous, automated, and observed against every retail bank. |
| S2 SQL injection web → core banking DB | Medium | Critical | Needs a flaw to exist, but reaches the crown jewels directly. |
| S3 Session hijacking of a customer session | Medium | High | Per-customer fraud, contained blast radius. |
| S4 Insider privilege misuse on `bank-analyst` | Low | High | Low frequency, high trust, hard to detect. |
| S5 Exfiltration of customer data from the core DB | Low | Critical | GDPR/PSD2 exposure plus lasting reputational damage. |
| S6 Denial of service against the public portal | High | Medium | Frequent and visible, but recoverable and non-destructive. |

### What a good submission looks like

- **Asset inventory** – 5 assets with a named owner and differentiated C/I/A
  ratings; the core banking database and the authentication service should
  appear. Uniform "High everywhere" ratings indicate no real analysis.
- **Data flows** – at least one flow crossing internet → DMZ and one crossing
  DMZ → internal; the trainee should notice which are unauthenticated or
  unencrypted between `bank-web` and `bank-db`.
- **Threat model** – each scenario carries a plausible STRIDE category and a
  real ATT&CK technique ID (for example T1110.004, T1190, T1539, T1078, T1498).
  Wrong-but-defended IDs are acceptable; invented IDs are not.
- **Risk ranking** – ordering must be consistent with the two grids. A risk
  ranked first with Low likelihood and Low impact is a contradiction to raise.
- **RITA evidence** – a real path under `~/deliverables/exercise1/` plus counts
  that match the register (at least 5 assets, 5 threats, 5 risks).
- **Treatment plan** – MFA and rate limiting for S1, parameterised queries and
  least-privilege DB accounts for S2, segmentation and monitoring for S5. Each
  entry names an owner and a residual risk lower than the current level.
- **Accepted risks** – accepting a risk is valid if it has an owner and a review
  date; accepting S2 or S5 without compensating controls is not.
- **Executive summary** – business language, no technique IDs, and an explicit
  decision request. If it reads like the technical report, it fails its purpose.
