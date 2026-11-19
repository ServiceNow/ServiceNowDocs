---
title: Extract workers skill \(with the skill cloud\)
description: Extract worker's skill details based on employee ID and time duration.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/zurich/integrate-applications/integration-hub/wd-worker-skill-with-cloud.html
release: zurich
product: Integration Hub
classification: integration-hub
topic_type: task
last_updated: "2025-07-31"
reading_time_minutes: 2
breadcrumb: [Workday HR Spoke, Integration Hub spokes, Build integrations, Integration Hub, Workflow Data Fabric]
---

# Extract workers skill \(with the skill cloud\)

Extract worker's skill details based on employee ID and time duration.

## Before you begin

-   Role required: User with access to report creation and All Active and Terminated Workers report data source.
-   Create all calculated fields for this report before developing the report. This ensure that all fields are available during report creation.
    -   Create a True/False condition type calculated field with name **CF\_Last\_updated?**.

        \[Omitted image "wirker-skill-report-withcloud-1.PNG"\] Alt text: Create calculated field with name CF\_Last\_updated?.

    -   Create a Extract Multi-instance calculated field with name **CF last functionally updated**.

        \[Omitted image "wirker-skill-report-withcloud-2.PNG"\] Alt text: Create calculated field with name CF last functionally updated.


## About this task

This procedure must be performed in your Workday instance.

-   While creating the report, ensure that the report name, report field names, or column heading override for the respective field \(if given in report document\) should be same as in the report document.

    **Important:** Report field label should be same as in the report document.

-   While creating filter, ensure that you add parenthesis in filter.
-   All reports must be owned by ISU user which will be used for accessing these action on the ServiceNow platform.
-   In the **Advanced** section, ensure that the **Enable as webservice** check box is selected.

## Procedure

1.  Access the **Create Custom Report** task.

2.  Provide the report name to identify the report.

    For example, `CR Worker's skill details`.

3.  Select report type as **Advanced**.

4.  Clear the **Optimized for performance** check box.

5.  Select **All Active and Terminated Workers** for **Data Source**.

6.  Do not select the **Temporary report** check box and click **Ok**.

    \[Omitted image "wirker-skill-report-withcloud-3.PNG"\] Alt text: Create a custom report.

7.  Select the report business object and report fields.

    \[Omitted image "wirker-skill-report-withcloud-4.PNG"\] Alt text: Select the required report business object and report fields.

    \[Omitted image "wirker-skill-report-withcloud-5.PNG"\] Alt text: Select the required report business object and report fields.

8.  In the **Group Column Headings** section, select all business objects.

    Group Column heading for each business object will be blank.

    \[Omitted image "wirker-skill-report-withcloud-6.PNG"\] Alt text: Select the business objects under Group Column Headings.

9.  In the **Filter** section, select the value as shown here.

    Ensure that you add parenthesis as shown here.

    \[Omitted image "wirker-skill-report-withcloud-7.PNG"\] Alt text: Select values in the Filter section.

10. In the **Subfilter** section, select the value as shown.

    \[Omitted image "wirker-skill-report-withcloud-8.PNG"\] Alt text: Select values in the Subfilter section.

11. In the **Prompts** section, select the **Populate Undefined Prompt Defaults** check box.

    \[Omitted image "wirker-skill-report-withcloud-9.PNG"\] Alt text: Select the Populate Undefined Prompt Defaults check box.

12. Select the value of prompts in the **Prompt Default** section as shown.

    Ensure that the **Label For Prompt XML Alias** values of all prompt fields are as shown here.

    \[Omitted image "wirker-skill-report-withcloud-10.PNG"\] Alt text: Select the value of prompts in the Prompt Default section.

13. In the **Advanced** section, select the **Enable as Webservice** check box and click **Ok**.

14. After configuring the report, click the three dots icon and navigate to **Web Service** &gt; **View URLs**.

    \[Omitted image "wirker-skill-report-withcloud-11.png"\] Alt text: Navigate to Web Service &gt; View URLs .

15. Select the worker whose details you want to see or select the time duration for which you want to see the data.

    \[Omitted image "wirker-skill-report-withcloud-12.PNG"\] Alt text: Select worker details of time duration.

16. In the View URLs Web Service page, click the marked icon under the **CSV** section.

    \[Omitted image "wirker-skill-report-withcloud-13.png"\] Alt text: Click the marked icon under the CSV section.

    You will be navigated to a new browser and the RaaS URL of the report is displayed.

17. From the RaaS URL, copy and record these values.

    \[Omitted image "wirker-skill-report-withcloud-14.PNG"\] Alt text: RaaS URL.

    -   `https://wd2-impl-services1.workday.com` is the base URL of your Workday tenant.
    -   **Tenant\_Name** is your Workday tenant.
    -   **Report\_Owner\_user\_name** is user name of the report’s owner.
    -   **CR\_Worker\_s\_skill\_details** is the report name.

