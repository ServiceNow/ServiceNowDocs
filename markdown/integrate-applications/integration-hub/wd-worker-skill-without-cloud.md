---
title: Extract workers skill \(without the skill cloud\)
description: Extract worker’s skill details without skill cloud, based on employee ID or time duration.
locale: en-US
release: xanadu
product: Integration Hub
classification: integration-hub
topic_type: task
last_updated: "2024-10-25"
reading_time_minutes: 2
breadcrumb: [Workday HR Spoke, Integration Hub available spokes, Building integrations in Integration Hub, Integration Hub, Creating integrations with applications]
---

# Extract workers skill \(without the skill cloud\)

Extract worker’s skill details without skill cloud, based on employee ID or time duration.

## Before you begin

-   Role required: User with access to report creation and All Active and Terminated Workers report data source.
-   Create all calculated fields for this report before developing the report. This ensure that all fields are available during report creation.
    -   Create a True/False condition type calculated field with name **CF\_updated**.

        ![Create calculated field with name CF_updated.](../image/worker-skill-report-withoutcloud-1.PNG)

    -   Create a Extract Multi-instance calculated field with name **CF\_last functionally updated skill for worker**.

        ![Create calculated field with name CF_last functionally updated skill for worker.](../image/worker-skill-report-withoutcloud-2.PNG)


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

    ![Create a custom report.](../image/worker-skill-report-withoutcloud-3.PNG)

7.  Select the report business object and report fields as shown.

    ![Select the required report business object and report fields.](../image/worker-skill-report-withoutcloud-4.PNG)

8.  In the **Group Column Headings** section, select all business objects.

    Group Column heading for each business object will be blank.

    ![Select the business objects under Group Column Headings.](../image/worker-skill-report-withoutcloud-5.PNG)

9.  In the **Filter** section, select the value as shown.

    Ensure to add parenthesis as shown.

    ![Select the values in Filter section.](../image/worker-skill-report-withoutcloud-6.PNG)

10. In the **Subfilter** section, select the value as shown.

    ![Select the values in Subfilter section.](../image/worker-skill-report-withoutcloud-7.PNG)

11. In **Prompts** section, select the **Populate Undefined Prompt Defaults** check box.

    ![Select the Populate Undefined Prompt Defaults check box.](../image/wirker-skill-report-withcloud-8.PNG)

12. Select the value of prompts in the **Prompt Default** section as shown.

    Ensure that the **Label For Prompt XML Alias** values of all prompt fields are as shown here.

    ![Select the value of prompts in the Prompt Default section.](../image/worker-skill-report-withoutcloud-9.PNG)

13. In the **Advanced** section, select the **Enable as Webservice** check box and click **Ok**.

14. After configuring the report, click the three dots icon and navigate to **Web Service** &gt; **View URLs**.

    ![Navigate to Web Service > View URLs .](../image/worker-skill-report-withoutcloud-10.png)

15. Select the worker whose details you want to see or select the time duration for which you want to see the data.

    ![Select worker details of time duration.](../image/worker-skill-report-withoutcloud-11.PNG)

16. In the View URLs Web Service page, click the marked icon under the **CSV** section.

    ![Click the marked icon under the CSV section.](../image/worker-skill-report-withoutcloud-12.png)

    You will be navigated to a new browser and the RaaS URL of the report is displayed.

17. From the RaaS URL, copy and record these values.

    ![RaaS URL.](../image/worker-skill-report-withoutcloud-13.PNG)

    -   `https://wd2-impl-services1.workday.com` is the base URL of your Workday tenant.
    -   **Tenant\_Name** is your Workday tenant.
    -   **Report\_Owner\_user\_name** is user name of the report’s owner.
    -   **CR\_Worker\_s\_skill\_details** is the report name.

