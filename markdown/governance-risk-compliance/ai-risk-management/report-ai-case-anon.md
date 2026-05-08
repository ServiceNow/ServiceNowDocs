---
title: Report an AI case anonymously
description: Report an AI case by describing the issue, affected users, and any relevant data.
locale: en-US
release: australia
product: AI Risk Management
classification: ai-risk-management
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 4
breadcrumb: [Use, AI Risk and Compliance, Governance, Risk, and Compliance]
---

# Report an AI case anonymously

Report an AI case by describing the issue, affected users, and any relevant data.

## Before you begin

Anonymous AI case reporting is available when the AI Case Management \(sn\_ai\_case\_mgmt\) application is installed. Installing AI Case Management automatically installs and configures the Anonymous Report Center plugin and required record producers.

Role required: sn\_ai\_case\_mgmt.ai\_case\_business\_user \(This role is required to access the Employee Center\). No role is required to submit a report directly through the Anonymous Report Center.

## About this task

You can report anytime, without sharing your name or contact details. Investigators only see the report details, not who submitted it. The AI case is managed as part of AI Risk and Compliance application and can be viewed in AI Control Tower to support risk and compliance oversight.

The Report an AI case record producer within the AI Case Management application \(sn\_ai\_case\_mgmt\) supports secure handling of anonymous AI case reports. Before an anonymous report is saved, all free‑text fields \(such as case type, summary, business unit, and jurisdiction\) are automatically sanitized. This process removes HTML, scripts, styles, symbols, and unsupported characters; restricts input to standard alphanumeric characters and basic punctuation; and trims extra whitespace. Only alphanumeric characters and `@ . _ -` are retained. These automated checks help reduce the risk of unsafe or malformed input in anonymously submitted AI cases.

**Note:** When submitting an anonymous report, don’t include personal data about yourself or other individuals that could directly or indirectly reveal your identity \(for example, names, email addresses, or phone numbers\).

## Procedure

1.  Access the Anonymous report center using one of these options.

<table id="choicetable_npy_jjm_23c"><thead><tr><th align="left" id="d140021e92">

Option

</th><th align="left" id="d140021e95">

Description

</th></tr></thead><tbody><tr><td id="d140021e101">

**Direct portal access**

</td><td>

1.  Launch the portal by using **\[your instance URL\]/arc**.
2.  Select **Submit a report anonymously**.


</td></tr><tr><td id="d140021e125">

**Employee center access**

</td><td>

1.  Navigate to **All** &gt; **Self-Service** &gt; **Employee Center**.
2.  On the Employee Center landing page, select **Help center** &gt; **Technology services** and then select **AI assets** from the Technology services topics section.
3.  Select the **Visit Anonymous Report Center** card.
4.  Select **Submit a report anonymously**.


</td></tr></tbody>
</table>    If you’re unable to access the Anonymous Report Center, confirm the following.

    -   Confirm with a team member that has the admin role that the AI Case Management is installed and active.
    -   Confirm that pop-up blockers or browser extensions aren’t preventing the portal from loading.
    After accessing the Anonymous report center, you’re signed out automatically to keep your identity anonymous.

2.  Select **Report an AI case** and on the form, fill in the fields.

    For full descriptions of the fields, see [Report an AI case form](../reference/report-anon-ai-case-form.md).

3.  Enter the CAPTCHA verification code on the screen.

4.  Select **Submit**.

    After you submit an anonymous AI case, the system generates a report number and a private report key. Save this information securely. You need the report key to check status updates or provide additional information later. If you lose the report key, it can’t be recovered and the case can’t be identified or retrieved on your behalf. You need this information to follow up on a case. For more information, see [Follow up on a report from the Anonymous Reporting Center](follow-up-anonymously.md).

5.  To save a PDF copy of your report, select **Download report copy**.


## Result

The AI case record is created and assigned to the AI case team for review. A report extract is generated so you can follow up on the progress of the submitted AI case.

**Note:** Maintain this report extract securely for future reference to preserve anonymity.

## What to do next

A user with the AI Risk and Compliance Analyst role \[sn\_grc\_ai\_gov.ai\_risk\_and\_compliance\_analyst\] who is part of the Assigned group according to the Assignment rules.

AI cases are managed through AI Case Management within AI Risk and Compliance to help ensure consistent tracking, investigation, and resolution of AI‑related issues.

After an AI case is created and enters the New state, the next step is Triage, where the AI Risk and Compliance team reviews the case to validate scope, assess severity, and determine the appropriate course of action. Depending on the outcome of triage, the team may initiate an assessment. For more information, see [Initiate AI assessment on an AI asset](initiate-assessment-on-an-ai-asset.md).

-   **[Report an AI case form](../reference/report-anon-ai-case-form.md)**  
Use the Report an AI case form in the Anonymous Report Center to report an AI case with the necessary details. After you submit the AI case report, mandatory fields and input format are validated before submission.
-   **[Follow up on a report from the Anonymous Reporting Center](follow-up-anonymously.md)**  
After you submit an anonymous report, save the **Report key** and **Report number**. Use these reference numbers to follow up or address comments on your case anonymously.

**Parent Topic:**[Using AI Risk and Compliance](../concept/using-ai-risk-and-compliance.md)

