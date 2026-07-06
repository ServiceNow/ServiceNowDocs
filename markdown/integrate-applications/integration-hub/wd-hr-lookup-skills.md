---
title: Create report to extract skills
description: Create report to extract skill \(maintains skills and skill cloud skills\) details from Workday based on the time duration.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/integrate-applications/integration-hub/wd-hr-lookup-skills.html
release: australia
product: Integration Hub
classification: integration-hub
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 2
breadcrumb: [Workday HR Spoke, Integration Hub spokes, Build integrations, Integration Hub, Workflow Data Fabric]
---

# Create report to extract skills

Create report to extract skill \(maintains skills and skill cloud skills\) details from Workday based on the time duration.

## Before you begin

-   Role required: User with access to report creation and Maintained Skills and Skills Cloud Skills report data source.
-   Create all calculated fields for this report before developing the report. This ensure that all fields are available during report creation.

## About this task

This procedure must be performed in your Workday instance.

-   While creating the report, ensure that the report name, report field names, or column heading override for the respective field \(if given in report document\) should be same as in the report document.

    **Important:** Report field label should be same as in the report document.

-   While creating filter, ensure that you add parenthesis in filter.
-   All reports must be owned by ISU user which will be used for accessing these action on the ServiceNow platform.
-   In the **Advanced** section, ensure that the **Enable as webservice** check box is selected.

## Procedure

1.  Access the **Create Custom Report** task.

2.  Provide the report name.

    For example, `CR Skills details`.

3.  Select report type as **Advanced**.

4.  Clear the **Optimized for performance** check box.

5.  Select **Maintained Skills and Skills Cloud Skills** for **Data Source**.

6.  Do not select the **Temporary report** check box and click Ok.

    \[Omitted image "wdhr-lookup-skills-1.PNG"\] Alt text: Skills custom report.

7.  Select the report business object and report fields.

    \[Omitted image "wdhr-lookup-skills-2.PNG"\] Alt text: Select the report business object and report fields.\[Omitted image "wdhr-lookup-skills-3.PNG"\] Alt text: Select the report business object and report fields.

8.  In **Filter** section, select the required values.

    \[Omitted image "wdhr-lookup-skills-4.PNG"\] Alt text: Select the required filter values.

9.  In the **Prompts** section, select the **Populate Undefined Prompt Defaults** check box.

    \[Omitted image "wdhr-lookup-skills-5.PNG"\] Alt text: Select the Populate Undefined Prompt Defaults check box.

10. Select the value of prompts under the **Prompt Default** section.

    Ensure that the **Label For Prompt XML Alias** values for all prompt fields are as shown here.

    \[Omitted image "wdhr-lookup-skills-6.PNG"\] Alt text: Select the value of prompts under the Prompt Default section.

11. In the **Advanced** section, select the **Enable as webservice** check box and click **Ok**.

12. Click the three dots icon and navigate to **Web Service** &gt; **View URLs**.

    \[Omitted image "wdhr-lookup-skills-7.PNG"\] Alt text: Navigate to Web Service &gt; View URLs .

13. Select the time duration for which you want to extract the data.

    \[Omitted image "wdhr-lookup-skills-8.PNG"\] Alt text: Select the time duration.

14. In View URLs Web Service page, click the marked icon under **CSV** section.

    \[Omitted image "wdhr-lookup-skills-9.png"\] Alt text: Click the marked icon under CSV section.

    You will be navigated to a new browser and the RaaS URL of the report is displayed.

15. From the RaaS URL, copy and record these values.

    \[Omitted image "wdhr-lookup-skills-10.PNG"\] Alt text: RaaS URL.

    -   `https://wd2-impl-services1.workday.com` is the base URL of your Workday tenant.
    -   **Tenant\_Name** is your Workday tenant.
    -   **Report\_Owner\_user\_name** is user name of the report’s owner.
    -   **CR\_Skills\_details** is the report name.

