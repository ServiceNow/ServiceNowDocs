---
title: Tech debt indicator score for application rationalization
description: The Technology Reference Model \(TRM\) Technical Debt indicator is a customizable application metric that evaluates the technical debt score for each Business Application. This score reflects the number of associated technologies that don’t comply with established TRM standards. It offers a clear and measurable value that can be leveraged across the Enterprise Architecture workspace for scoring, analysis, and visualization.
locale: en-US
release: australia
topic_type: reference
last_updated: "2026-03-12"
reading_time_minutes: 3
breadcrumb: [Rationalization of business applications, Exploring Enterprise Architecture Workspace, Enterprise Architecture Workspace, Enterprise Architecture]
---

# Tech debt indicator score for application rationalization

The Technology Reference Model \(TRM\) Technical Debt indicator is a customizable application metric that evaluates the technical debt score for each Business Application. This score reflects the number of associated technologies that don’t comply with established TRM standards. It offers a clear and measurable value that can be leveraged across the Enterprise Architecture workspace for scoring, analysis, and visualization.

By highlighting technology non-compliance, the TRM Technical Debt score helps identify high-risk applications enabling teams to prioritize modernization and rationalization initiatives effectively.

## TRM Technical Debt Indicator Score Logic

The application weight is the number of technical debts for that business application. If a business application has high technical debts, then its normalized value is considered as low. If a business application has low technical debts, then its normalized value is considered as high.

Following is the logic to generate the TRM technical debt indicator score:

-   Compliant Applications

    If a Business Application \(BA\) is listed in the TPM Discovered Technologies \(sn\_apm\_tpm\_discovered\_technology\) but not in the TRM Technical Debts \(sn\_apm\_trm\_standards\_technical\_debt\), then the application is considered as compliant.

    -   Tech debt score: 0
    -   Normalized value: 10
-   Unassessed Applications \(Not Discovered\)

    If a business application isn’t found in the TPM Discovered Technologies table:

    -   The application isn’t assessed
    -   No score is assigned
-   Non-compliant applications

    If a business application is found in both the TPM Discovered Technologies and TRM Technical Debts:

    -   The application is considered non-compliant
    -   Tech Debt score: Based on the number of non-compliant technologies \(range: 1–10\)
    -   Normalized value: From 1 through 10
-   Hardware-Only Applications

    If a business application is found in the TPM Discovered Technologies but only has hardware associated and isn’t listed in the TRM Technical Debts table:

    -   The application isn’t assessed
    -   No score is assigned

## Run scheduled jobs

You must run the following scheduled jobs to populate the TPM and TRM data in EA Workspace:

-   Populate TPM Discovered Technologies and Lifecycles

    This job populates the technology life-cycle data in the TPM Technology Lifecycle \[sn\_apm\_tpm\_technology\_lifecycle\] table.

    **Note:** The data includes end of support date, end of extended support date, and end of life date for your software products and hardware models.

    For instructions, see [Run a scheduled job to generate TPM lifecycle data](../../task/eaw-task/eaw-run-scheduled-job-update-tpm-data.md). For updating the TPM data for a selected business application, see [Update TPM data for a business application or application service](../../task/eaw-task/update-tpm-data.md).

-   Populate TRM technical debts in the EA Workspace

    This job updates the Technical Debt \[sn\_apm\_trm\_standards\_technical\_debt\] table with the latest technical debt data for your software products that is available in the TPM Discovered Technology \[sn\_apm\_tpm\_discovered\_technology\] table.

    **Note:** The Populate TRM technical debts in the EA Workspace scheduled job are available only the Software Asset Management \(SAM\) Foundation or Software Asset Management \(SAM\) Professional plugin is installed.

    For instructions, see [Run a scheduled job to update TRM technical debt data in EA Workspace](../../task/eaw-task/eaw-run-job-trm-tech-debts.md).


## Regenerate indicator score

Update application indicator scores on-demand, to assess the application for a technical risk, and gather real-time insights, regenerate indicator score for the Technical Debt indicator from the **Setup** page.![Navigate to the Application indicators page from the Setup section](../../image/eaw-image/eaw-setup-app-ndicators.png)

Select the Technical Debt indicator from the list, then select the Regenerate indicator score.![Regenerate indicator score for Technical Debt indicator](../../image/eaw-image/eaw-regenerate-ind-score.png)

## Technical Debt indicator score on the Application Rationalization List view page

The Technical Debt indicator score is available as a column on the Application Rationalization List page. You can sort the applications by their score from highest to lowest debt.![Technical Debt column in the Application Rationalization page](../../image/eaw-image/eaw-tech-debt-on-app-rat-list.png)

## Technical Debt indicator as bubble size on the Application Rationalization Bubble Chart page

The Technical Debt indicator is listed in the Bubble Size list under the Settings of the Bubble Chart page. You can select the indicator to from the Bubble Size list to see its score for business applications in the X and Y axes and specify the bubble sizes.![Selecting Technical Debt score as a bubble size on the Bubble Chart page of the Application Rationalization](../../image/eaw-image/eaw-tech-debt-indicator-bubble-chart.png)

**Parent Topic:**[Rationalization of business applications](../../concept/eaw-concept/eaw-rationalize-business-applications.md)

