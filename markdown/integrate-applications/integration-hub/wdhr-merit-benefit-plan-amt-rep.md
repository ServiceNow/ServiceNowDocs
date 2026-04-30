---
title: Workday configuration for merit and benefit plan amount report
description: Retrieve the worker's target merit plan amount and benefit plan's employer contribution amount based on Employee ID by creating the merit and benefit plan amount report.
locale: en-US
release: zurich
product: Integration Hub
classification: integration-hub
topic_type: task
last_updated: "2025-01-12"
reading_time_minutes: 2
breadcrumb: [Workday HR Spoke, Integration Hub spokes, Build integrations, Integration Hub, Workflow Data Fabric]
---

# Workday configuration for merit and benefit plan amount report

Retrieve the worker's target merit plan amount and benefit plan's employer contribution amount based on Employee ID by creating the merit and benefit plan amount report.

## Before you begin

Role required: User with access to report creation and the All Workers data source.

-   While creating the report, ensure that the report name, report field names or column heading override for the respective field \(if given in report document\) is same as it is in report document.

    Report field label should be same as in report doc. Else, the developed action will fail.

-   **Group Column Heading** for each business object in **Group Column Heading** section should be blank.
-   All reports must be shared or owned by the ISU user which will be used for accessing these actions on the ServiceNow platform.
-   In the **Advanced** section, **Enable as webservice** option should be selected.

## Procedure

1.  Access the Create Custom Report task.

2.  Provide the report name such as, `Get merit and benefit plan amount`.

3.  Select report type as **Advanced**.

4.  Clear the **Optimized for performance** option.

5.  Select **Data Source** as **All Workers**.

6.  Do not select the **Temporary report** option and click **OK**.

    ![Report setup with All Workers data source](../image/wdhr-merit-benefit-plan-amt-rep-1.png)

7.  Select the report business object and report fields.

    ![Columns tab with Worker, Merit Plan, and Benefit Elections fields](../image/wdhr-merit-benefit-plan-amt-rep-2.png)

8.  In **Group Column Heading** section, select all business object as below.

    **Group Column Heading** for each business object will be blank. ![Group Column Headings configuration](../image/wdhr-merit-benefit-plan-amt-rep-3.png)

9.  In **Filter** section, select the value as given below.

    ![Filter on Instances with Employee ID prompt](../image/wdhr-merit-benefit-plan-amt-rep-4.png)

10. In **Prompts** section, select the **Populate Undefined Prompt Defaults** option.

    ![Prompts tab with runtime date prompts](../image/wdhr-merit-benefit-plan-amt-rep-5.png)

11. Select the value of prompts as given below under Prompt default section.

    Make sure the **Label For Prompt XML Alias** of all prompt fields must be same.

    ![Prompt Defaults with Employee ID field](../image/wdhr-merit-benefit-plan-amt-rep-6.png)

12. In **Advanced** section, select **Enable as webservice** option and click **OK**.

13. Click on three dots icon and navigate to **Web Services** &gt; **View URLs** option once report configuration is done.

    ![Web Service menu with View URLs](../image/wdhr-merit-benefit-plan-amt-rep-7.png)

14. Provide an employee ID in the **Employee ID** field and click **OK**.

    ![View URLs dialog with Employee ID parameter](../image/wdhr-merit-benefit-plan-amt-rep-8.png)

15. In View URLs Web Service page, click the marked icon under the **CSV** section.

    A new browser tab is opened.

    ![View URLs page with CSV download](../image/wdhr-merit-benefit-plan-amt-rep-9.png)

16. View the RaaS URL of the report in the new browser tab.

    The RaaS URL of the report is displayed in new browser tab and you can obtain these details from the link.

    ![RaaS URL in browser](../image/wdhr-merit-benefit-plan-amt-rep-10.png)

    -   `https://wd2-impl-services1.workday.com` is the base URL of customer's workday tenant.
    -   **Tenant\_Name** is the customer's workday tenant.
    -   **Report\_Owner\_user\_name** represents user name of the report's owner.
    -   **Get\_merit\_and\_benefit\_plan\_amount** is the report name alias.

