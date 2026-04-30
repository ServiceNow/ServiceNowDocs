---
title: Workday configuration for worker job history report
description: Retrieve worker's job history based on employee ID or contingent worker ID by creating the worker job history report.
locale: en-US
release: zurich
product: Integration Hub
classification: integration-hub
topic_type: task
last_updated: "2026-01-07"
reading_time_minutes: 1
keywords: [worker job history, job history, employee history]
breadcrumb: [Workday HR Spoke, Integration Hub spokes, Build integrations, Integration Hub, Workflow Data Fabric]
---

# Workday configuration for worker job history report

Retrieve worker's job history based on employee ID or contingent worker ID by creating the worker job history report.

## Before you begin

Role required: User with access to report creation and the Worker from Prompt data source.

-   While creating the report, ensure that the report name, report field names or column heading override for the respective field \(if given in report document\) is same as it is in report document.

    Report field label should be same as in report doc. Else, the developed action will fail.

-   While creating filter, ensure that you add parenthesis on filter.
-   All reports must be owned by the ISU user which will be used for accessing these actions on the ServiceNow platform.
-   In the **Advanced** section, **Enable as webservice** option should be selected.

## Procedure

1.  Access the Create Custom Report task.

2.  Provide the report name such as, `RPT_Worker_s_Job_History`.

3.  Select report type as **Advanced**.

4.  Clear the **Optimized for performance** option.

5.  Select **Data Source** as **Worker from Prompt**.

6.  Do not select the **Temporary report** option and click **OK**.

    ![](../image/wdhr-pk-worker-job-history-1.png)

7.  Select the report business object and report fields.

    ![](../image/wdhr-pk-worker-job-history-2.png)

8.  In **Group Column Heading** section, select all business object as below.

    **Group Column Heading** for each business object will be blank. ![](../image/wdhr-pk-worker-job-history-3.png)

9.  In **Filter** section, select the value.

    Ensure to add parenthesis.

    ![](../image/wdhr-pk-worker-job-history-4.png)

10. In **Prompts** section, select the highlighted effective date as **Prompt for effective as of date** and select the **Populate Undefined Prompt Defaults** option.

    ![](../image/wdhr-pk-worker-job-history-5.png)

11. Select the value of prompts under Prompt default section.

    Make sure the **Label For Prompt XML Alias** of all prompt fields must be same as shown below.

    ![](../image/wdhr-pk-worker-job-history-6.png)

12. In **Advanced** section, select **Enable as webservice** option and click **OK**.

13. Click on three dots icon and navigate to **Web Services** &gt; **View URLs** option once report configuration is done.

    ![](../image/wdhr-pk-worker-job-history-7.png)

14. Select any worker in **Worker** parameter and click **OK**.

    ![](../image/wdhr-pk-worker-job-history-8.png)

15. In View URLs Web Service page, click the marked icon under the **CSV** section.

    A new browser tab is opened.

    ![](../image/wdhr-pk-worker-job-history-9.png)

16. Review the RaaS URL of the report displayed in the new browser tab.

    You can obtain these details from the link.

    ![](../image/wdhr-pk-worker-job-history-10.png)

    -   `https://wd2-impl-services1.workday.com` is the base URL of customer's workday tenant.
    -   **Tenant\_Name** is the customer's workday tenant.
    -   **Report\_Owner\_user\_name** represents user name of the report's owner.
    -   **RPT\_Worker\_s\_Job\_History** represents the report name.

