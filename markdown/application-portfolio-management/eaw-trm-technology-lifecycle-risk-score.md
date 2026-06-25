---
title: Technology lifecycle risk score in Enterprise Architecture Workspace
description: The Technology Portfolio Management \(TPM\) lifecycle risk score is a numeric value that quantifies how close a technology is to its end-of-support or end-of-life milestone. Risk scores roll up from individual technologies through application services to business applications, and serve as an indicator in scoring profiles to surface lifecycle exposure across the portfolio.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/application-portfolio-management/eaw-trm-technology-lifecycle-risk-score.html
release: australia
topic_type: reference
last_updated: "2026-05-20"
reading_time_minutes: 6
breadcrumb: [Rationalization of business applications, Exploring Enterprise Architecture Workspace, Enterprise Architecture Workspace, Enterprise Architecture]
---

# Technology lifecycle risk score in Enterprise Architecture Workspace

The Technology Portfolio Management \(TPM\) lifecycle risk score is a numeric value that quantifies how close a technology is to its end-of-support or end-of-life milestone. Risk scores roll up from individual technologies through application services to business applications, and serve as an indicator in scoring profiles to surface lifecycle exposure across the portfolio.

## Technology lifecycle risk scores

Technologies without lifecycle data, or that have passed all lifecycle milestones, receive the maximum risk score of 100. Technologies more than 18 months from their next milestone receive a risk score of 0. Between those extremes, the score scales by proximity to the next milestone and by which milestone type is approaching — with end of life weighted more heavily than end of support.

Two scheduled jobs must complete before lifecycle risk scores are available in Enterprise Architecture Workspace: one to discover technologies and link them to lifecycle records, and one to calculate the risk scores from those records.

## Key tables for technology lifecycle risk scores

|Table|Label|Description|
|-----|-----|-----------|
|sn\_apm\_tpm\_discovered\_technology|TPM Discovered Technologies|Links each discovered technology to a business application, application service, server CI, and lifecycle record. Populated by the data collection scheduled job.|
|sn\_apm\_tpm\_technology\_lifecycle|TPM Technology Lifecycle|Holds the lifecycle milestone dates for each software product or hardware model: end-of-support date, end-of-extended-support date, and end-of-life date.|
|sn\_apm\_tpm\_technology\_risk|TPM Technology Risk|Stores the calculated risk score per technology, per application service, and per business application. Distinguished by the Table name \[table\_name\] field.|

## Lifecycle milestone fields

The risk calculation uses the following date fields from the TPM Technology Lifecycle \[sn\_apm\_tpm\_technology\_lifecycle\] table.

|Field|Meaning|
|-----|-------|
|End of Support \[eos\_date\]|The date after which the vendor no longer provides standard support for the technology.|
|End of Extended Support \[eoes\_date\]|The date after which extended or paid support ends. Weighted more heavily than end of support in the risk formula.|
|End of Life \[eol\_date\]|The date after which the technology is fully retired. Carries the highest weight in the risk formula.|
|Earliest Lifecycle date \[earliest\_lifecycle\_date\]|The soonest upcoming milestone date across the three fields before. This is the value the risk formula uses to determine proximity.|

## Data collection

The **Populate TPM Discovered Technologies and Lifecycles** scheduled job traverses CMDB and Service Mapping relationships to create records in the TPM Discovered Technologies \[sn\_apm\_tpm\_discovered\_technology\] table. Each record links a discovered technology to:

-   A business application \(cmdb\_ci\_business\_app\)
-   An application service \(cmdb\_ci\_service\)
-   A server or host CI \(cmdb\_ci\)
-   A technology lifecycle record \(sn\_apm\_tpm\_technology\_lifecycle\)

Without this job, no lifecycle dates are available for risk calculation. For instructions on running the job, see [Run a scheduled job to generate TPM lifecycle data](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/application-portfolio-management/eaw-run-scheduled-job-update-tpm-data.md).

## Risk score calculation

The **Populate Technology Lifecycle Risks** scheduled job calculates a risk score for each discovered technology using a two-factor formula.

```
riskScore = baseScore × multiplier
```

Factor 1 — Multiplier \(which milestone is next?\)

The multiplier reflects the severity of the approaching milestone.

|Next milestone|Multiplier|
|--------------|----------|
|End of Support \(EOS\)|2|
|End of Extended Support \(EOES\)|3|
|End of Life \(EOL\)|4|
|All milestones already passed, or no lifecycle data available|Score is set to 100 immediately — the formula is not applied.|

Factor 2 — Base score \(how far away is the next milestone?\)

The base score reflects how much time remains before the next milestone.

|Days until next milestone|Base score|
|-------------------------|----------|
|0–30 days|20|
|31–90 days|10|
|91–180 days|6|
|181–360 days|4|
|361–540 days|2|
|More than 540 days \(18+ months\)|0|

The maximum possible score from the formula is 80 \(base score 20 × multiplier 4, when a technology is within 30 days of its end-of-life date\). The absolute maximum of 100 applies only when all lifecycle dates have passed or no lifecycle data exists.

Scores are stored per fiscal period in the TPM Technology Risk \[sn\_apm\_tpm\_technology\_risk\] table.

**Note:** **Populate Technology Lifecycle Risks** scheduled job runs monthly by default. You can also run it on demand. For instructions, see [Run a scheduled job to update TRM technical debt data in EA Workspace](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/application-portfolio-management/eaw-run-job-trm-tech-debts.md).

## Technology lifecycle risk score example

This example shows how the risk score is calculated for a single technology.

|Input|Value|Explanation|
|-----|-----|-----------|
|Days until next milestone|60 days|The Earliest lifecycle date \[earliest\_lifecycle\_date\] is 60 days from today.|
|Next milestone type|End of Life \(EOL\)|The approaching date is the End of life date \[eol\_date\].|
|Base score|10|60 days falls in the 31–90 day range.|
|Multiplier|4|EOL carries the highest multiplier.|
|Risk score|40|10 × 4 = 40. Stored in the TPM Technology Risk table \[sn\_apm\_tpm\_technology\_risk.risk\_score\].|

## Risk score aggregation

After individual technology risk scores are calculated, the scores aggregate up the hierarchy by summation. All three levels are stored in the TPM Technology Risk \[sn\_apm\_tpm\_technology\_risk\] table, distinguished by the table name \[table\_name\] field.

|Level|Table name \[table\_name\] value|How the score is computed|
|-----|--------------------------------|-------------------------|
|Technology|TPM Discovered Technologies \[sn\_apm\_tpm\_discovered\_technology\] table|Individual risk score from the two-factor formula mentioned earlier.|
|Application Service|Application Service \[cmdb\_ci\_service\] table|Sum of all technology risk scores associated with that application service.|
|Business Application|Business Application \[cmdb\_ci\_business\_app\] table|Sum of all technology risk scores across all application services linked to the business application.|

The business application–level risk score is the value that the Lifecycle Risk indicator uses when contributing to an application's overall score in a scoring profile.

## Where lifecycle risk scores appear in Enterprise Architecture Workspace

<table id="table_pjb_v2v_hjc"><thead><tr><th>

Location

</th><th>

How it is used

</th></tr></thead><tbody><tr><td>

Application Indicators \(Setup page\)

</td><td>

The Lifecycle Risk indicator appears in the Application Indicators list. You can add it to a scoring profile to include the risk score in application score calculation. You can also regenerate scores on demand from this page.

</td></tr><tr><td>

Application Rationalization — Bubble Chart

</td><td>

The Lifecycle Risk indicator score can be selected as an axis or bubble size value to visualize risk distribution across the portfolio.

</td></tr><tr><td>

Application Rationalization — List view

</td><td>

The Lifecycle Risk score is available as a sortable column, enabling you to rank applications from highest to lowest lifecycle exposure.

</td></tr><tr><td>

Application 360 Dashboard

</td><td>

The lifecycle risk score for the selected application appears alongside other indicator scores. **Note:** The Application 360 dashboard requires the Load Application Indicators and compute Application Scores scheduled job to have run for the current fiscal period. If the job has not run, lifecycle risk scores don't appear.

</td></tr></tbody>
</table>**Parent Topic:**[Rationalization of business applications](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/application-portfolio-management/eaw-rationalize-business-applications.md)

**Related topics**  


[Tech debt indicator score for application rationalization](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/application-portfolio-management/trm-tech-debt-indicator-for-app-rat.md)

[Application indicator score calculation in Enterprise Architecture Workspace](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/application-portfolio-management/eaw-application-indicator-score-calculation.md)

[Regenerate application indicator scores on-demand in Enterprise Architecture Workspace](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/application-portfolio-management/eaw-regenerate-indicator-score.md)

[Run a scheduled job to generate TPM lifecycle data](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/application-portfolio-management/eaw-run-scheduled-job-update-tpm-data.md)

[Manage scoring profiles](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/application-portfolio-management/eaw-configure-scoring-profiles.md)

