# Solution for Exercise 2: ICS Energy Infrastructure

## Expected findings
- Inventory of critical OT components (SCADA, PLC, RTU, field networks) and their interdependencies with IT systems.
- Updated zones and conduits diagram in line with ISA/IEC 62443 with identified remote access points.
- Register of pertinent threats and tactics (MITRE ATT&CK for ICS), including remote engineering compromise and process manipulation.
- Assessment of current controls such as industrial firewalls, application whitelisting, and OT change policies.

## Identified risks
- Intrusion into the corporate network that pivots towards the industrial DMZ and affects SCADA operations.
- Malicious manipulation of PLC parameters causing interruptions to power generation or distribution.
- Denial-of-service attacks against communication links with insufficient redundancy across control centres.
- Use of shared credentials for remote maintenance access without supervision or logging.

## Recommended mitigations
- Implement continuous monitoring of OT networks with anomaly detection and visibility of industrial protocols.
- Apply role-based access control and multi-factor authentication for remote engineering access.
- Segment the network with next-generation firewalls between IT/OT and critical zones, using minimally necessary control lists.
- Establish patch and change management procedures validated in test environments before production.
- Design and test OT incident response plans, with exercises coordinated with operations teams and suppliers.

## Reference answers for the submission questionnaire

The **Exercise 2 – Deliverables submission** level is a questionnaire
(`ASSESSMENT_LEVEL`, type `QUESTIONNAIRE`): nothing is auto-graded, so the
instructor reviews the answers against this key.

### Rating grids (questions 4, 5 and 6)

Reference ratings for the fixed scenario list. Accept one band either way when
justified. The point of the exercise is that operational and safety impact
diverge: a trainee who gives both grids identical answers has not understood
the ICS-specific part.

| Scenario | Likelihood | Operational impact | Safety impact |
|---|---|---|---|
| S1 Malware IT → control network | High | High | Equipment damage or unplanned shutdown |
| S2 Unauthorised remote access to `scada-server` | Medium | High | Equipment damage or unplanned shutdown |
| S3 Unauthorised Modbus/S7comm commands to the RTU | Medium | Critical | Risk to human life or to grid stability |
| S4 Malicious or faulty logic/firmware update | Low | High | Risk to human life or to grid stability |
| S5 Loss of visibility (HMI/historian down) | Medium | High | Manual intervention required, no danger |
| S6 Denial of service on control centre ↔ substation link | Medium | High | Manual intervention required, no danger |

S3 and S4 are the safety-defining scenarios: both write directly to the
physical process. S5 and S6 remove visibility and control but do not by
themselves command the plant, which is why their safety rating is lower while
their operational rating stays high.

### What a good submission looks like

- **Asset inventory** – assets assigned to a zone (corporate IT / DMZ /
  control), with the safety-critical flag set for the RTU and the SCADA server.
- **Zones and conduits** – the IT→OT crossing is identified explicitly, with the
  protocol and the access control (or the absence of one). Trainees should note
  that ports 502 and 102 on `substation-rtu` are reachable and unauthenticated.
- **Threat model** – ATT&CK for ICS references, not enterprise ones (for example
  T0886 Remote Services, T0836 Modify Parameter, T0857 System Firmware,
  T0815 Denial of View, T0814 Denial of Service).
- **Risk ranking** – must be driven by safety impact where it is highest, not
  purely by financial loss. A ranking that puts S5 above S3 needs a strong
  argument.
- **Mitigation plan** – controls suited to OT: unidirectional gateways or
  firewalled conduits, jump host with MFA for remote engineering access,
  protocol-aware monitoring, signed firmware and change control with a
  maintenance window. IEC 62443 references (SR 1.1, SR 5.1, SR 7.6) or ISO 27001
  equivalents.
- **Operational constraints** – the expected insight is that patching, agent
  installation and rebooting are not freely available in OT, so compensating
  controls (segmentation, monitoring, procedural controls) carry the load.
- **Cyber risk report** – states the safety consequence in plain language and
  asks leadership for a specific decision, such as funding the IT/OT
  segmentation or approving a maintenance window.
