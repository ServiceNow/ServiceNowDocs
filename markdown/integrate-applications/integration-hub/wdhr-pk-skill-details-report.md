---
title: Workday configuration for skill details report
description: Extract skills \(maintained skills and skill cloud skills\) details from Workday based on time duration by creating the skill details report.
locale: en-US
release: zurich
product: Integration Hub
classification: integration-hub
topic_type: task
last_updated: "2026-01-07"
reading_time_minutes: 1
keywords: [skills, maintained skills, skill cloud skills]
breadcrumb: [Workday HR Spoke, Integration Hub spokes, Build integrations, Integration Hub, Workflow Data Fabric]
---

# Workday configuration for skill details report

Extract skills \(maintained skills and skill cloud skills\) details from Workday based on time duration by creating the skill details report.

## Before you begin

Role required: User with access to report creation and the Maintained Skills and Skills Cloud Skills data source.

-   Create all calculated fields for this report before developing the report, so that all fields are available when you create the report.
-   While creating the report, ensure that the report name, report field names or column heading override for the respective field \(if given in report document\) is same as it is in report document.

    Report field label should be same as in report doc. Else, the developed action will fail.

-   While creating filter, ensure that you add parenthesis on filter.
-   All reports must be owned by the ISU user which will be used for accessing these actions on the ServiceNow platform.
-   In the **Advanced** section, **Enable as webservice** option should be selected.

## Procedure

1.  Access the Create Custom Report task.

2.  Provide the report name such as, `CR_Skills_details`.

3.  Select report type as **Advanced**.

4.  Clear the **Optimized for performance** option.

5.  Select **Data Source** as **Maintained Skills and Skills Cloud Skills**.

6.  Do not select the **Temporary report** option and click **OK**.

    ![](../image/wdhr-pk-skill-details-report-1.png)

7.  Select the report business object and report fields.

    ![](../image/wdhr-pk-skill-details-report-2.png)

    ![](../image/wdhr-pk-skill-details-report-3.png)

8.  In **Filter** section, select the value.

    Ensure to add parenthesis.

    ![](../image/wdhr-pk-skill-details-report-4.png)

9.  In **Prompts** section, select the **Populate Undefined Prompt Defaults** option.

    ![](../image/wdhr-pk-skill-details-report-5.png)

10. Select the value of prompts under Prompt default section.

    Make sure the **Label For Prompt XML Alias** of all prompt fields must be same as shown below.

    ![](../image/wdhr-pk-skill-details-report-6.png)

11. In **Advanced** section, select **Enable as webservice** option and click **OK**.

12. Click on three dots icon and navigate to **Web Services** &gt; **View URLs** option once report configuration is done.

    ![](../image/wdhr-pk-skill-details-report-7.png)

13. Select the time duration for which you want to extract the data and click **OK**.

    ![](../image/wdhr-pk-skill-details-report-8.png)

14. In View URLs Web Service page, click the marked icon under the **CSV** section.

    A new browser tab is opened.

    ![](../image/wdhr-pk-skill-details-report-9.png)

15. Review the RaaS URL of the report displayed in the new browser tab.

    You can obtain these details from the link.

    ![](../image/wdhr-pk-skill-details-report-10.png)

    -   `https://wd2-impl-services1.workday.com` is the base URL of customer's workday tenant.
    -   **Tenant\_Name** is the customer's workday tenant.
    -   **Report\_Owner\_user\_name** represents user name of the report's owner.
    -   **CR\_Skills\_details** represents the report name.

