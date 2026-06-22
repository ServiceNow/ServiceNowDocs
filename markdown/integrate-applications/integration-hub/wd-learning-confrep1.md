---
title: Configure the Learning Enrollment report
description: Configure the Learning Enrollment report in Workday to retrieve user's learning enrollments.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/integrate-applications/integration-hub/wd-learning-confrep1.html
release: australia
product: Integration Hub
classification: integration-hub
topic_type: task
last_updated: "2026-06-22"
reading_time_minutes: 2
breadcrumb: [Workday Learning Spoke, Integration Hub spokes, Build integrations, Integration Hub, Workflow Data Fabric]
---

# Configure the Learning Enrollment report

Configure the Learning Enrollment report in Workday to retrieve user's learning enrollments.

## Before you begin

User with access to report creation and the Learning Enrollments data source.

## About this task

-   For identification purposes, all calculated field name starts with **CF**.
-   Create all calculated fields for this report before developing the report. Thus, all fields are available while creating the report.
-   Report name can be different while creating the report. But ensure that the report field name or column heading override for the respective field \(if it’s given in the report document\) is same as it is in the report document. Report field label should be same as it is in the report document. Else, the developed action fails.
-   **Group Column Heading** for each business object in the **Group Column Headings** section should be empty.
-   Ensure that you add parenthesis in filter while creating it.
-   All reports must be shared or owned by the ISU user that accesses these actions on the ServiceNow platform.
-   In the **Advanced** section, select the **Enable as webservice** check box.

## Procedure

1.  Create Lookup Related Value type calculated field with name, **CF\_assigned\_by\_empid**.

    \[Omitted image "wd-learning-prop-enrol1.png"\] Alt text:

2.  Create Lookup Related Value type calculated field with name, **cf\_initiator\_wid**.

    \[Omitted image "wd-learning-prop-enrol2.png"\] Alt text:

3.  Create the True/False condition type calculated field with name, **CF\_status\_successfully\_completed**.

    \[Omitted image "wd-learning-prop-enrol3.png"\] Alt text:

4.  Create Extract Multi-instance type calculated field with name, **CF\_enrollment\_successfully\_completed** and select **CF\_status\_successfully\_completed** as the return value.

    \[Omitted image "wd-learning-prop-enrol4.png"\] Alt text:

5.  Create the True/False condition type calculated field with name, **Initiator = Worker**.

    \[Omitted image "wd-learning-prop-enrol5.png"\] Alt text:

6.  Create the Lookup Related Value type calculated field with name, **cf\_initiator**.

    \[Omitted image "wd-learning-prop-enrol6.png"\] Alt text:

7.  Create the Learning Enrollment report.

    1.  Access the **Create Custom Report** task.

    2.  Provide the report name, for example, `Test -Learning Assignment`.

    3.  Select report type as **Advanced**.

    4.  Clear the **Optimized for performance** check box.

    5.  Select **Data Source** as **Learning Enrollments**.

    6.  Don’t select the temporary report check box.

    7.  Click **Ok**.

        \[Omitted image "wd-learning-prop-enrol7.png"\] Alt text:

    8.  Select the report business object and report fields.

        \[Omitted image "wd-learning-prop-enrol8.png"\] Alt text: \[Omitted image "wd-learning-prop-enrol9.png"\] Alt text:

    9.  In the **Group Column Headings** section, select all business objects as shown here.

        The **Group Column Heading** for each business object is empty.

        \[Omitted image "wd-learning-prop-enrol10.png"\] Alt text:

    10. In the **Filter** section, select the values as shown here.

        Be sure to add the parentheses.

        \[Omitted image "wd-learning-prop-enrol11.png"\] Alt text:

    11. In the **Prompts** section, select the **Populate undefined prompt defaults** check box.

        \[Omitted image "wd-learning-prop-enrol12.png"\] Alt text:

    12. Under the **Prompts** section, select values as shown here.

        Make sure that the values of **Label For Prompt XML Alias** for all prompt fields are as shown.

        \[Omitted image "wd-learning-prop-enrol13.png"\] Alt text:

    13. In the **Advanced** section, select the **Enable as webservice** check box and click **Ok**.

    14. After report configuration is done, click the three dots icon and navigate to **Web Services** &gt; **View URLs**.

        \[Omitted image "wd-learning-prop-enrol14.png"\] Alt text:

    15. Select time range and click **Ok**.

        \[Omitted image "wd-learning-prop-enrol15.png"\] Alt text:

    16. In the View URLs Web Service page, click the active link you want to generate.

        In a new browser tab, you can access the RaaS URL.


