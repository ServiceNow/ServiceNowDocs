---
title: Workday configuration for performance goals report
description: Retrieve the Goals details based on Organization by creating the performance goals report.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/zurich/integrate-applications/integration-hub/wdhr-performance-goals-rep.html
release: zurich
product: Integration Hub
classification: integration-hub
topic_type: task
last_updated: "2026-01-28"
reading_time_minutes: 1
breadcrumb: [Workday HR Spoke, Integration Hub spokes, Build integrations, Integration Hub, Workflow Data Fabric]
---

# Workday configuration for performance goals report

Retrieve the Goals details based on Organization by creating the performance goals report.

## Before you begin

Role required: User with access to report creation and the Goals by Organization data source.

-   While creating the report, ensure that the report name, report field names or column heading override for the respective field \(if given in report document\) is same as it is in report document.

    Report field label should be same as in report doc. Else, the developed action will fail.

-   All reports must be owned by the ISU user which will be used for accessing these actions on the ServiceNow platform.
-   In the **Advanced** section, **Enable as webservice** option should be selected.

## Procedure

1.  Access the Create Custom Report task.

2.  Provide the report name such as, `RPT_Employee_Goals`.

3.  Select report type as **Advanced**.

4.  Clear the **Optimized for performance** option.

5.  Select **Data Source** as **Goals by Organization**.

6.  Do not select the **Temporary report** option and click **OK**.

    \[Omitted image "wd-config-perf-goal1.png"\] Alt text: RPT Employee Goals.

7.  Select the report business object and report fields.

    \[Omitted image "wdhr-performance-goals-rep-2.png"\] Alt text: Workday performance goals.

    \[Omitted image "wdhr-performance-goals-rep-3.png"\] Alt text: Workday performance goals.

    \[Omitted image "wdhr-performance-goals-rep-4.png"\] Alt text: Workday performance goals.

    \[Omitted image "wdhr-performance-goals-rep-5.png"\] Alt text: Workday performance goals.

    \[Omitted image "wdhr-performance-goals-rep-6.png"\] Alt text: Workday performance goals.

    \[Omitted image "wdhr-performance-goals-rep-7.png"\] Alt text: Workday performance goals.

    \[Omitted image "wdhr-performance-goals-rep-8.png"\] Alt text: Workday performance goals.

8.  In **Prompts** section, select the highlighted effective date as **prompt for effective as of date** and select the **Populate Undefined Prompt Defaults** option.

    \[Omitted image "wdhr-performance-goals-rep-9.png"\] Alt text: Workday performance goals.

9.  Select the value of prompts under Prompt default section.

    Make sure the **Label For Prompt XML Alias** of all prompt fields must be same.

    \[Omitted image "wdhr-performance-goals-rep-10.png"\] Alt text: Workday performance goals.

10. In **Advanced** section, select **Enable as webservice** option and click **OK**.

11. Click on three dots icon and navigate to **Web Services** &gt; **View URLs** option once report configuration is done.

    \[Omitted image "wdhr-performance-goals-rep-11.png"\] Alt text: Workday performance goals.

12. Select any organization in **Organizations** parameter and optionally select the **Include manager** and **Include subordinate organizations** options, then click **OK**.

    \[Omitted image "wdhr-performance-goals-rep-12.png"\] Alt text: Workday performance goals.

13. In View URLs Web Service page, click the marked icon under the **CSV** section.

    A new browser tab is opened.

    \[Omitted image "wdhr-performance-goals-rep-13.png"\] Alt text: Workday performance goals.

    The RaaS URL of the report is displayed in new browser tab and you can obtain these details from the link.

    \[Omitted image "wdhr-performance-goals-rep-14.png"\] Alt text: Workday performance goals.

    -   `https://wd2-impl-services1.workday.com` is the base URL of customer's workday tenant.
    -   **Tenant\_Name** is the customer's workday tenant.
    -   **Report\_Owner\_user\_name** represents user name of the report's owner.
    -   **RPT\_Employee\_Goals** is the report name.

