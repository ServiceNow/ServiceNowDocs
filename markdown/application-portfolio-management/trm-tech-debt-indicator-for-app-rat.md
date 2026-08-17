---
title: Tech debt indicator score for application rationalization
description: The Technology Reference Model \(TRM\) Technical Debt indicator is a customizable application metric that evaluates the technical debt score for each Business Application. This score reflects the number of associated technologies that don’t comply with established TRM standards. It offers a clear and measurable value that can be leveraged across the Enterprise Architecture workspace for scoring, analysis, and visualization.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/application-portfolio-management/trm-tech-debt-indicator-for-app-rat.html
release: australia
topic_type: reference
last_updated: "2026-03-12"
reading_time_minutes: 4
breadcrumb: [Rationalization of business applications, Exploring Enterprise Architecture Workspace, Enterprise Architecture Workspace, Enterprise Architecture]
---

# Tech debt indicator score for application rationalization

The Technology Reference Model \(TRM\) Technical Debt indicator is a customizable application metric that evaluates the technical debt score for each Business Application. This score reflects the number of associated technologies that don’t comply with established TRM standards. It offers a clear and measurable value that can be leveraged across the Enterprise Architecture workspace for scoring, analysis, and visualization.

**Important:**

Technology Lifecycle Management \(TLM\) was previously known as Technology Portfolio Management \(TPM\). TPM and TLM refer to the same feature. Table names and scheduled job names continue to use TPM and haven't been renamed.

Whether your instance displays TPM or TLM also depends on your application versions. TLM labels appear only when both the Enterprise Architecture Workspace application \(version 9.2.1 or later\) and the Technology Lifecycle Management plugin, sn\_apm\_tpm \(version 1.11.0 or later\), are installed. If either application is on an earlier version, the interface continues to show TPM.

By highlighting technology non-compliance, the TRM Technical Debt score helps identify high-risk applications enabling teams to prioritize modernization and rationalization initiatives effectively.

## TRM Technical Debt Indicator Score Logic

The application weight is the number of technical debts for that business application. If a business application has high technical debts, then its normalized value is considered as low. If a business application has low technical debts, then its normalized value is considered as high.

Following is the logic to generate the TRM technical debt indicator score:

-   Compliant Applications

    If a Business Application \(BA\) is listed in the TLM Discovered Technologies \(sn\_apm\_tpm\_discovered\_technology\) but not in the TRM Technical Debts \(sn\_apm\_trm\_standards\_technical\_debt\), then the application is considered as compliant.

    -   Tech debt score: 0
    -   Normalized value: 10
-   Unassessed Applications \(Not Discovered\)

    If a business application isn’t found in the TLM Discovered Technologies table:

    -   The application isn’t assessed
    -   No score is assigned
-   Non-compliant applications

    If a business application is found in both the TLM Discovered Technologies and TRM Technical Debts:

    -   The application is considered non-compliant
    -   Tech Debt score: Based on the number of non-compliant technologies \(range: 1–10\)
    -   Normalized value: From 1 through 10
-   Hardware-Only Applications

    If a business application is found in the TLM Discovered Technologies but only has hardware associated and isn’t listed in the TRM Technical Debts table:

    -   The application isn’t assessed
    -   No score is assigned

## Run scheduled jobs

You must run the following scheduled jobs to populate the TLM and TRM data in EA Workspace:

-   Populate TLM Discovered Technologies and Lifecycles

    This job populates the technology life-cycle data in the TLM Technology Lifecycle \[sn\_apm\_tpm\_technology\_lifecycle\] table.

    **Note:** The data includes end of support date, end of extended support date, and end of life date for your software products and hardware models.

    For instructions, see [Run a scheduled job to generate TLM lifecycle data](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/application-portfolio-management/eaw-run-scheduled-job-update-tpm-data.md). For updating the TLM data for a selected business application, see [Update TLM data for a business application or application service](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/application-portfolio-management/update-tpm-data.md).

-   Populate TRM technical debts in the EA Workspace

    This job updates the Technical Debt \[sn\_apm\_trm\_standards\_technical\_debt\] table with the latest technical debt data for your software products. The data is available in the TLM Discovered Technology \[sn\_apm\_tpm\_discovered\_technology\] table.

    **Note:** The Populate TRM technical debts in the EA Workspace scheduled job are available only the Software Asset Management \(SAM\) Foundation or Software Asset Management \(SAM\) Professional plugin is installed.

    For instructions, see [Run a scheduled job to update TRM technical debt data in EA Workspace](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/application-portfolio-management/eaw-run-job-trm-tech-debts.md).


## Regenerate indicator score

Update application indicator scores on-demand, to assess the application for a technical risk, and gather real-time insights, regenerate indicator score for the Technical Debt indicator from the **Setup** page.\[Omitted image "eaw-setup-app-ndicators.png"\] Alt text: Navigate to the Application indicators page from the Setup section

Select the Technical Debt indicator from the list, then select the Regenerate indicator score.\[Omitted image "eaw-regenerate-ind-score.png"\] Alt text: Regenerate indicator score for Technical Debt indicator

## Technical Debt indicator score on the Application Rationalization List view page

The Technical Debt indicator score is available as a column on the Application Rationalization List page. You can sort the applications by their score from highest to lowest debt.\[Omitted image "eaw-tech-debt-on-app-rat-list.png"\] Alt text: Technical Debt column in the Application Rationalization page

## Technical Debt indicator as bubble size on the Application Rationalization Bubble Chart page

The Technical Debt indicator is listed in the Bubble Size list under the Settings of the Bubble Chart page. You can select the indicator from the Bubble Size list to see its score for business applications in the X and Y axes.\[Omitted image "eaw-tech-debt-indicator-bubble-chart.png"\] Alt text: Selecting Technical Debt score as a bubble size on the Bubble Chart page of the Application Rationalization

**Parent Topic:**[Rationalization of business applications](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/application-portfolio-management/eaw-rationalize-business-applications.md)

