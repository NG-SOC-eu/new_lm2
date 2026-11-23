# RITA Quick Guide

This guide summarises the main steps for working with RITA (Risk Identification and Threat Assessment).

## Login
1. Navigate to `https://ng-soc.eurodyn.com/login`.
2. Enter the username and password provided in the exercise.
3. Click **Log In** to access the dashboard.

## Asset Creation
1. From the dashboard, choose **Assets → Add Asset**.
2. Provide name, description, and owner.
3. Save the asset; repeat for each system component.

## Threat and Vulnerability Mapping
1. Open an asset and use **Threats → Add Threat** to assign relevant threats.
2. Link vulnerabilities via **Vulnerabilities → Add Vulnerability**.
3. Capture references or evidence in the provided fields.

## Risk Evaluation
1. Within the asset, select **Risk Evaluation**.
2. Estimate likelihood and impact; RITA calculates the risk score.
3. Document existing controls and recommended treatments.

## Imports
1. Use **Data Import** in the main menu to upload CSV or JSON templates.
2. Map incoming fields to RITA’s schema and run the import.
3. Review imported records for accuracy.

The register template `content/templates/risk_register.csv` (also available on
the analyst machine at `~/deliverables/exercise<N>/risk_register.csv`) uses
column names that map directly onto RITA’s asset, threat and risk fields, so you
can build the register offline and import it in one go.

## Exporting your results (required evidence)
1. Open the risk evaluation view for the exercise.
2. Choose **Export** and select CSV (or JSON).
3. Save the file on the analyst machine as
   `~/deliverables/exercise1/rita_export.csv` (or `exercise2`). If the browser
   saves it to `~/Downloads`, move it:
   ```bash
   mv ~/Downloads/rita_export*.csv ~/deliverables/exercise1/rita_export.csv
   ```
4. If your build of RITA offers no export, take a screenshot of the risk
   evaluation table instead and save it in the same folder as
   `rita_evaluation.png`.
5. Note the file name and the number of assets, threats and risks you
   registered — the submission questionnaire asks for them.

## Where the answers are recorded
RITA holds the model. The platform questionnaire at the end of each exercise
(**Deliverables submission**) is where you type the answers that the instructor
grades. The files in `~/deliverables/` are your working documents and evidence.
