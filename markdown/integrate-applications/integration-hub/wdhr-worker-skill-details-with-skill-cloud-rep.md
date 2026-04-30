---
title: Workday configuration for worker's skill details report with Skill Cloud
description: Extract worker's skill details including skill level details based on employee ID or time duration by creating the worker's skill details report.
locale: en-US
release: zurich
product: Integration Hub
classification: integration-hub
topic_type: task
last_updated: "2025-01-12"
reading_time_minutes: 2
breadcrumb: [Workday HR Spoke, Integration Hub spokes, Build integrations, Integration Hub, Workflow Data Fabric]
---

# Workday configuration for worker's skill details report with Skill Cloud

Extract worker's skill details including skill level details based on employee ID or time duration by creating the worker's skill details report.

## Before you begin

Role required: User with access to report creation and the All Active and Terminated Workers data source.

-   Create all calculated fields for this report before developing the report, so that while creating report all fields are available.
-   While creating the report, ensure that the report name, report field names or column heading override for the respective field \(if given in report document\) is same as it is in report document.

    Report field label should be same as in report doc. Else, the developed action will fail.

-   While creating filter, ensure that you add parenthesis on filter.
-   All reports must be owned by the ISU user which will be used for accessing these actions on the ServiceNow platform.
-   In the **Advanced** section, **Enable as webservice** option should be selected.

Create all calculated fields so that these fields can be used while developing report.

-   Calculated field 1:
    -   Create True/False condition type calculated field named **CF\_Last\_updated?**. ![CF_Last_updated calculated field of true or false condition type](../image/wdhr-worker-skill-details-with-skill-cloud-rep-1.png)
    -   Create Extract Multi-instance type calculated field named **CF last functionally updated**. ![CF last functionally updated Extract Multi-Instance field](../image/wdhr-worker-skill-details-with-skill-cloud-rep-2.png)

## Procedure

1.  Access the Create Custom Report task.

2.  Provide the report name such as, `CR Worker's skill details`.

3.  Select report type as **Advanced**.

4.  Clear the **Optimized for performance** option.

5.  Select **Data Source** as **All Active and Terminated Workers**.

6.  Do not select the **Temporary report** option and click **OK**.

    ![Report setup with All Active and Terminated Workers](../image/wdhr-worker-skill-details-with-skill-cloud-rep-3.png)

7.  Select the report business object and report fields.

    ![Columns tab with Worker and Skill for Worker fields](../image/wdhr-worker-skill-details-with-skill-cloud-rep-4.png)

8.  In **Group Column Heading** section, select all business object as below.

    **Group Column Heading** for each business object will be blank. ![Group Column Headings configuration](../image/wdhr-worker-skill-details-with-skill-cloud-rep-5.png)

9.  In **Filter** section, select the value as given below.

    Ensure to add parenthesis. ![Filter on Instances with multiple conditions](../image/wdhr-worker-skill-details-with-skill-cloud-rep-6.png)

10. In **Subfilter** section, select the value as given below.

    ![Sub Level Filter for Skill for Worker](../image/wdhr-worker-skill-details-with-skill-cloud-rep-7.png)

11. In **Prompts** section, select the **Populate Undefined Prompt Defaults** option.

    ![Prompts tab with runtime date prompts](../image/wdhr-worker-skill-details-with-skill-cloud-rep-8.png)

12. Select the value of prompts as given below under Prompt default section.

    Make sure the **Label For Prompt XML Alias** of all prompt fields must be same.

    ![Prompt Defaults with Worker and date fields](../image/wdhr-worker-skill-details-with-skill-cloud-rep-9.png)

13. In **Advanced** section, select **Enable as webservice** option and click **OK**.

14. Click on three dots icon and navigate to **Web Services** &gt; **View URLs** option once report configuration is done.

    ![Web Service menu with View URLs](../image/wdhr-worker-skill-details-with-skill-cloud-rep-10.png)

15. Select the worker whose details you want to see or select the time duration for which you want to see the data.

    ![View URLs dialog with Worker and date parameters](../image/wdhr-worker-skill-details-with-skill-cloud-rep-11.png)

16. In View URLs Web Service page, click the marked icon under the **CSV** section.

    A new browser tab is opened.

    ![View URLs page with CSV download](../image/wdhr-worker-skill-details-with-skill-cloud-rep-12.png)

17. View the RaaS URL of the report in the new browser tab.

    The RaaS URL of the report is displayed in new browser tab and you can obtain these details from the link.

    ![RaaS URL in browser](../image/wdhr-worker-skill-details-with-skill-cloud-rep-13.png)

    -   `https://wd2-impl-services1.workday.com` is the base URL of customer's workday tenant.
    -   **Tenant\_Name** is the customer's workday tenant.
    -   **Report\_Owner\_user\_name** represents user name of the report's owner.
    -   **CR\_Worker\_s\_skill\_details** is the report name.

