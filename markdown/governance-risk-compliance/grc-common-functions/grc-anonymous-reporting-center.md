---
title: Anonymous Reporting Center \(ARC\)
description: Anonymous Reporting Center \(ARC\) enables employees to submit compliance, privacy, or AI-related concerns without revealing their identity
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/governance-risk-compliance/grc-common-functions/grc-anonymous-reporting-center.html
release: australia
product: GRC Common Functions
classification: grc-common-functions
topic_type: concept
last_updated: "2026-03-12"
reading_time_minutes: 2
breadcrumb: [Common GRC features, Governance, Risk, and Compliance]
---

# Anonymous Reporting Center \(ARC\)

Anonymous Reporting Center \(ARC\) enables employees to submit compliance, privacy, or AI-related concerns without revealing their identity

After an anonymous case is reported in ARC, a designated case analyst reviews the information and initiates an investigation. If additional clarification is required, the analyst adds comments to the report.

ARC generates a report key and report number when a new case is submitted. These values are required to track progress or address comments on a case anonymously.

## Accessing Anonymous Reporting Center

ARC is included with the following GRC applications:

-   Compliance Case Management \(sn\_comp\_case\)
-   Privacy Management \(sn\_privacy\)
-   AI Case Management \(sn\_ai\_case\_mgmt\)

If any of these applications are already installed, no additional setup is required.

For privacy and compliance cases, access ARC from the **Risk and Compliance** tab of the Employee Center.

For AI cases, access ARC from the Employee Center by navigating to **Help center** &gt; **Technology services** &gt; **AI assets**.

**Note:** Employees are automatically signed out of the Employee Center when ARC opens.

## ARC landing page

From the ARC landing page, employees can report a case anonymously or follow up on a report.

\[Omitted image "arc-landing-page.png"\] Alt text: Anonymous Reporting Center \(ARC\) landing page.

For information about filing specific types of anonymous reports, see the following topics:

-   [Report a compliance case anonymously](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/governance-risk-compliance/compliance-case-management/report-compliance-case-anonymously.md)
-   [Report a privacy case anonymously](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/governance-risk-compliance/privacy-workspace/report-privacy-case-anonymously.md)
-   [Report an AI case anonymously](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/governance-risk-compliance/ai-risk-management/report-ai-case-anon.md)

## Built-in sanitization layer

Before an anonymous report is saved, all free‑text fields in the forms are sanitized to reduce the risk of unsafe or malformed input. These text fields include **Case type**, **Summary**, **Business unit**, and **Jurisdiction**. The sanitization process includes:

-   Removing HTML and embedded script or style content
-   Restricting input to standard alphanumeric characters and basic punctuation
-   Trimming extra whitespaces

## Review process

All reports submitted through ARC are routed to the appropriate case management team depending on the case type. The reporters appear as guests in the application workspace where records are created. A case analyst validates the details, assesses the severity, and determines the next steps for investigation.

-   **[Submit an anonymous case from the Anonymous Reporting Center](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/governance-risk-compliance/grc-common-functions/grc-submit-report-anonymously.md)**  
Raise suspected compliance, privacy, or AI-related issues confidentially from the Anonymous Reporting Center \(ARC\) landing page.
-   **[Track report status or follow up on a report from the Anonymous Reporting Center](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/governance-risk-compliance/grc-common-functions/grc-follow-up-anonymously.md)**  
Check the status of your case on the Anonymous Reporting Center and follow up on any required additional details.

**Parent Topic:**[Common Governance, Risk, and Compliance features](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/governance-risk-compliance/grc-common-functions/common-grc-features.md)

