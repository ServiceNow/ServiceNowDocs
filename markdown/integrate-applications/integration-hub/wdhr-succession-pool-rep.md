---
title: Workday configuration for succession pool report
description: Retrieve the succession pool data based on succession pool and employee by creating the succession pool report.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/zurich/integrate-applications/integration-hub/wdhr-succession-pool-rep.html
release: zurich
product: Integration Hub
classification: integration-hub
topic_type: task
last_updated: "2025-01-12"
reading_time_minutes: 2
breadcrumb: [Workday HR Spoke, Integration Hub spokes, Build integrations, Integration Hub, Workflow Data Fabric]
---

# Workday configuration for succession pool report

Retrieve the succession pool data based on succession pool and employee by creating the succession pool report.

## Before you begin

Role required: User with access to report creation and the All Succession Pools data source.

-   Create all calculated fields for this report before developing the report, so that while creating report all fields are available.
-   While creating the report, ensure that the report name, report field names or column heading override for the respective field \(if given in report document\) is same as it is in report document.

    Report field label should be same as in report doc. Else, the developed action will fail.

-   While creating filter, ensure that you add parenthesis on filter.
-   All reports must be owned by the ISU user which will be used for accessing these actions on the ServiceNow platform.
-   In the **Advanced** section, **Enable as webservice** option should be selected.

Create all calculated fields so that these fields can be used while developing report.

-   Calculated field 1: Create Aggregate Related Instances type calculated field named **CF\_worker succession pool**. \[Omitted image "wdhr-succession-pool-rep-1.png"\] Alt text: CF\_worker succession pool calculated field configuration

## Procedure

1.  Access the Create Custom Report task.

2.  Provide the report name such as, `CR succession pool details`.

3.  Select report type as **Advanced**.

4.  Clear the **Optimized for performance** option.

5.  Select **Data Source** as **All Succession Pools**.

6.  Do not select the **Temporary report** option and click **OK**.

    \[Omitted image "wdhr-succession-pool-rep-2.png"\] Alt text: Report setup with All Succession Pools data source

7.  Select the report business object and report fields.

    \[Omitted image "wdhr-succession-pool-rep-3.png"\] Alt text: Columns tab with business objects and fields\[Omitted image "wdhr-succession-pool-rep-4.png"\] Alt text: Columns tab continued with CF\_worker succession pool fields

8.  In **Group Column Heading** section, select all business object as below.

    **Group Column Heading** for each business object will be blank. \[Omitted image "wdhr-succession-pool-rep-5.png"\] Alt text: Group Column Headings configuration section of the report

9.  In **Filter** section, select the value as given below.

    Ensure to add parenthesis. \[Omitted image "wdhr-succession-pool-rep-6.png"\] Alt text: Filter on Instances configuration

10. In **Prompts** section, select the highlighted effective date as **prompt for effective as of date** and select the **Populate Undefined Prompt Defaults** option.

    \[Omitted image "wdhr-succession-pool-rep-7.png"\] Alt text: Prompts tab with runtime date prompts

11. Select the value of prompts as given below under Prompt default section.

    Make sure the **Label For Prompt XML Alias** of all prompt fields must be same.

    \[Omitted image "wdhr-succession-pool-rep-8.png"\] Alt text: Prompt Defaults section of the report

12. In **Advanced** section, select **Enable as webservice** option and click **OK**.

13. Click on three dots icon and navigate to **Web Services** &gt; **View URLs** option once report configuration is done.

    \[Omitted image "wdhr-succession-pool-rep-9.png"\] Alt text: Web Service menu with View URLs

14. Select the succession pool for which you want to run this report.

    If you want any specific worker from succession pool, select worker; otherwise leave it blank.\[Omitted image "wdhr-succession-pool-rep-10.png"\] Alt text: View URLs Web Services parameters

15. In View URLs Web Service page, click the marked icon under the **CSV** section.

    A new browser tab is opened.

    \[Omitted image "wdhr-succession-pool-rep-11.png"\] Alt text: View URLs page with CSV download

16. View the RaaS URL of the report in the new browser tab.

    The RaaS URL of the report is displayed in new browser tab and you can obtain these details from the link.

    \[Omitted image "wdhr-succession-pool-rep-12.png"\] Alt text: RaaS URL in browser

    -   `https://wd2-impl-services1.workday.com` is the base URL of customer's workday tenant.
    -   **Tenant\_Name** is the customer's workday tenant.
    -   **Report\_Owner\_user\_name** represents user name of the report's owner.
    -   **Report\_Name** is the report name.

