---
title: Workday configuration for payslip report
description: Retrieve worker's payslip data based on time range and employee ID by creating the payslip report.
locale: en-US
release: zurich
product: Integration Hub
classification: integration-hub
topic_type: task
last_updated: "2026-01-07"
reading_time_minutes: 2
keywords: [payslip, payroll results, worker payslip]
breadcrumb: [Workday HR Spoke, Integration Hub spokes, Build integrations, Integration Hub, Workflow Data Fabric]
---

# Workday configuration for payslip report

Retrieve worker's payslip data based on time range and employee ID by creating the payslip report.

## Before you begin

Role required: User with access to report creation, the Payroll Results data source, and Copy Standard Report to Custom Report task.

-   User who is going to create this report should have Custom Report Creation domain access.
-   User should have report data source Payroll Results access.
-   User should have Copy Standard Report to Custom Report task access.
-   While creating the report, ensure that the report name, report field names or column heading override for the respective field \(if given in report document\) is same as it is in report document.

    Report field label should be same as in report doc. Else, the developed action will fail.

-   **Group Column Heading** for each business object should be blank.
-   All reports must be owned by the ISU user which will be used for accessing these actions on the ServiceNow platform.
-   In the **Advanced** section, **Enable as webservice** option should be selected.

## Procedure

1.  Access the **Copy Standard Report to Custom Report** task.

2.  Search for `Payslip to Print - Report Design` in Standard Report name box, select it, and click **OK**.

    ![](../image/wdhr-pk-payslip-1.png)

3.  Provide the desired name of the report such as, `Payslip to Print - Report Design - Copy` and click **OK**.

    ![](../image/wdhr-pk-payslip-2.png)

4.  In **Data Source** box, search for **Payroll Results** and select it.

    ![](../image/wdhr-pk-payslip-3.png)

5.  Once you select **Payroll Results** as data source, the report will automatically populate the Data source filter.

    ![](../image/wdhr-pk-payslip-4.png)

6.  Add **Sub Period \(if different from Pay Period\)** report field in column section in report.

    ![](../image/wdhr-pk-payslip-5.png)

7.  In **Columns** section, remove fields which are not in screenshots given below.

    Ensure all fields are in the same order as shown in the screenshots.

    ![](../image/wdhr-pk-payslip-6.png)

    ![](../image/wdhr-pk-payslip-7.png)

    ![](../image/wdhr-pk-payslip-8.png)

    ![](../image/wdhr-pk-payslip-9.png)

8.  In **Group Column Headings** section, remove business objects which are not in below screenshots.

    **Group Column Heading** for all business objects should be blank.

    ![](../image/wdhr-pk-payslip-10.png)

    ![](../image/wdhr-pk-payslip-11.png)

9.  In **Prompt** section, remove the pre-existing prompt.

    ![](../image/wdhr-pk-payslip-12.png)

10. Once pre-existing prompt is removed, select the **Populate Undefined Prompt defaults** option.

    This will populate all built-in prompts.

    **Note:** Ensure the prompts are configured as shown below.

    ![](../image/wdhr-pk-payslip-13.png)

11. In **Advanced** section, verify that **Enable as webservice** option is selected.

    Most likely it would be already selected.

    ![](../image/wdhr-pk-payslip-14.png)

12. Click **OK**, then **Done**.

13. Click on three dots icon and navigate to **Web Services** &gt; **View URLs** option once report configuration is done.

    ![](../image/wdhr-pk-payslip-15.png)

14. Select any time range in parameters, select any user in **Worker** box, and click **OK**.

    ![](../image/wdhr-pk-payslip-16.png)

15. In View URLs Web Service page, click the marked icon under the **CSV** section.

    A new browser tab is opened.

    ![](../image/wdhr-pk-payslip-17.png)

16. Review the RaaS URL of the report displayed in the new browser tab.

    You can obtain these details from the link.

    ![](../image/wdhr-pk-payslip-18.png)

    -   `https://wd2-impl-services1.workday.com` is the base URL of customer's workday tenant.
    -   **Tenant\_Name** is the customer's workday tenant.
    -   **Report\_Owner\_user\_name** represents user name of the report's owner.
    -   **Payslip\_to\_Print\_-\_Report\_Design\_-\_Copy** represents the report name alias.

