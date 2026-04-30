---
title: Anonymous Reporting Center
description: The Anonymous Reporting Center \(ARC\) enables employees to submit compliance, privacy, or AI‑related concerns without revealing their identity. Employees are automatically signed out of the Employee Center when ARC opens.
locale: en-US
release: zurich
product: GRC Common Functions
classification: grc-common-functions
topic_type: concept
last_updated: "2026-02-18"
reading_time_minutes: 2
breadcrumb: [Common GRC features, Governance, Risk, and Compliance]
---

# Anonymous Reporting Center

The Anonymous Reporting Center \(ARC\) enables employees to submit compliance, privacy, or AI‑related concerns without revealing their identity. Employees are automatically signed out of the **Employee Center** when ARC opens.

After you report an anonymous case in ARC, a designated case analyst reviews the information and initiates an investigation. If additional clarification is required, the analyst adds comments to the report.

**Important:** ARC generates a Report key and Report number when you submit a new case. These values are required to track progress or address comments on your case anonymously.

## Accessing Anonymous Reporting Center

ARC is included with the following GRC applications:

-   Compliance Case Management \(sn\_comp\_case\)
-   Privacy Management \(sn\_privacy\)
-   AI Case Management \(sn\_ai\_case\_mgmt\)

If any of these applications are already installed, no additional setup is required.

For privacy and compliance cases, ARC can be accessed from the **Risk and Compliance** tab of the **Employee Center**.

For AI cases, it’s available at **Help center** &gt; **Technology services** &gt; **AI assets**.

## ARC landing page

![Use the Anonymous Reporting Center (ARC) landing page to submit a report and track its progress anonymously.](../image/arc-landing-page.png "ARC landing page")

Use the ARC landing page to report a case anonymously or follow up on a report.

<table id="table_rs2_4yt_l3c"><thead><tr><th>

Actions

</th><th>

Description

</th></tr></thead><tbody><tr><td>

**Submit a report anonymously**

</td><td>

Raise suspected compliance, privacy, or AI-related issues confidentially. Depending on the case type, you can choose to:-   [Report a compliance case](../../grc-compliance-case-mgmt/task/report-compliance-case-anonymously.md)
-   [Report a privacy case](../../grc-privacy-management/task/report-privacy-case-anonymously.md)
-   Report an AI case

**Important:** After submission, download a copy of your report to record the Report key and Report number.

</td></tr><tr><td>

**Follow up on a report**

</td><td>

Provide the Report key and Report number to check the case status or address investigator comments anonymously. ARC doesn't send email notifications or alerts about updates to your case. If you can't find these numbers, you have to submit a new case.

</td></tr></tbody>
</table>## Built-in sanitization layer

Before an anonymous report is saved, all free‑text fields in the forms \(such as case type, summary, business unit, and jurisdiction\) are sanitized to:

-   Remove HTML and embedded script or style content
-   Restrict input to standard alphanumeric characters and basic punctuation
-   Trim extra whitespaces

Sanitization reduces the risk of unsafe or malformed input.

## Review process

All reports submitted through ARC are routed to the appropriate case management team depending on the case type. The reporters appear as guests in the application workspace where records are created. A case analyst validates the details, assesses the severity, and determines the next steps for investigation.

-   **[Submit a report anonymously from the Anonymous Reporting Center](../task/grc-submit-report-anonymously.md)**  
Use **Submit a report anonymously** on the Anonymous Reporting Center \(ARC\) landing page to raise suspected compliance, privacy, or AI-related issues confidentially.
-   **[Follow up on a report from the Anonymous Reporting Center](../task/grc-follow-up-anonymously.md)**  
Check the status of your case on the Anonymous Reporting Center using the Report key and Report number. You must download a copy of your anonymous report after submitting a case to record these values.

**Parent Topic:**[Common Governance, Risk, and Compliance features](common-grc-features.md)

