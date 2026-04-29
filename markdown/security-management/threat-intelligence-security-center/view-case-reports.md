---
title: View Case Reports
description: Use the case reports feature to generate reports related to the cases. These reports include post investigation report or an executive summary report.
locale: en-US
release: australia
product: Threat Intelligence Security Center
classification: threat-intelligence-security-center
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 3
breadcrumb: [Threat Analyst Workbench, Use, Threat Intelligence Security Center, Security Operations]
---

# View Case Reports

Use the case reports feature to generate reports related to the cases. These reports include post investigation report or an executive summary report.

## Before you begin

Role required: sn\_sec\_tisc.analyst

## Procedure

1.  Navigate to **Workspaces** &gt; **Threat Intelligence Security Center**.

2.  Click **Threat Analyst Workbench** icon.

3.  Go to **Case Management** &gt; **All Cases**.

    All the cases are displayed.

4.  Select any case.

5.  Go to **Case Reports**.

    ![Case Reports](../image/tisc-case-reports.png)

    **Note:** You can delete the reports from the list, create a duplicate copy of the existing reports and customize your own report.

6.  Click **New**.

    The report templates that are published and enabled in the base system are displayed.![New report template](../image/tisc-new-report.png)

7.  Select the desired Report Template.

    The selected report template for the report type is generated. Also, here once the report is published, that means that larger group of users can view it but if the report is in a draft state then that report is hidden from the users. As an analyst you can only view the published reports but not the reports in the draft state.

    **Note:**

    -   In case if you want to add more fields then select the fields and add it directly within your case report.
    -   If you want to add related list, for example a list of observables then select Observables. All the observables associated for that particular case will be listed, select one or more observables ans click **Add**. You can also filter out the required observable and add it to your case.
8.  Click **Save Content** to save the contents of your report.

9.  Click **Preview** to preview the report.

    **Note:** You can do the following:

    -   **Maximize** the report window.
    -   **Download** the report using **Download** icon.
    -   Pop out the report in a new tab in case if the height or size of the report to have better viewing experience.
    -   **Edit** the Report Name and Report description.
    -   **Publish** the report.
10. Click **Edit Content** button to republish the report.

    **Note:** A warning message is displayed for you to share the report:

    You must republish the report after you make changes, for you to download or share the report. Do you want to still continue editing?

11. Click **Edit**.

    If you want to edit the report, then you can continue editing the report as explained or you can publish the report. Once it is published, the report will be read-only.

12. Click on **Share Report in Email** to share the report.

    While sharing the report, the PDF report that was generated is attached as an attachment to the Email.![Share report in email](../image/tisc-share-email.png)

13. Add the required email fields such as To \(whom you want to share the report\), CC, and BCC

14. Mark the email as important, if required.

15. Click **Send**.

    The report will be shared with the larger group of users.


**Parent Topic:**[Threat Analyst Workbench](../concept/threat-analyst-workbench.md)

**Related topics**  


[Workbench Overview](../concept/workbench-overview.md)

[Creating cases using Threat Analyst Workbench](../concept/create-cases-using-threat-analyst-workbench.md)

[Creating case task using Threat Analyst Workbench](tisc-create-case-task.md)

[Working with Investigation Canvas](../concept/tisc-investigation-canvases.md)

[Add artifacts to case\(s\) or case task\(s\)](add-artifacts-to-a-case-s.md)

[Run Enrichment Actions within a case](run-enrichment-results.md)

[Create a security incident from a TISC case](tisc-create-si-case.md)

[Upload Secure File Attachments](secure-file-attachments.md)

