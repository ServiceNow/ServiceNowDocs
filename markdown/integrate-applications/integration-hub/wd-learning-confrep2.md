---
title: Configure the Learning Assignment report
description: Configure the Learning Assignment report in Workday to retrieve user's learning assignments.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/integrate-applications/integration-hub/wd-learning-confrep2.html
release: australia
product: Integration Hub
classification: integration-hub
topic_type: task
last_updated: "2026-06-19"
reading_time_minutes: 3
breadcrumb: [Workday Learning Spoke, Integration Hub spokes, Build integrations, Integration Hub, Workflow Data Fabric]
---

# Configure the Learning Assignment report

Configure the Learning Assignment report in Workday to retrieve user's learning assignments.

## Before you begin

User with access to report creation and the Learning Assignments by Learning Organization data source.

## About this task

-   For identification purposes, all calculated field name starts with **CF**.
-   Create all calculated fields for this report before developing the report. Thus, all fields are available while creating the report.
-   Report name can be different while creating the report. But ensure that the report field name or column heading override for the respective field \(if it’s given in the report document\) is same as it is in the report document. Report field label should be same as it is in the report document. Else, the developed action fails.
-   **Group Column Heading** for each business object in the **Group Column Headings** section should be empty.
-   Ensure that you add parenthesis in filter while creating it.
-   All reports must be shared or owned by the ISU user that accesses these actions on the ServiceNow platform.
-   In the **Advanced** section, select the **Enable as webservice** check box.

## Procedure

1.  Create Lookup Related Value type calculated field with name, **cf\_learning content\_type**.

    \[Omitted image "wd-learning-enroll-1.jpg"\] Alt text:

2.  Create the True/False condition type calculated field with name, **CF\_enrollment\_event\_status**.

    \[Omitted image "wd-learning-enroll-2.jpg"\] Alt text:

3.  Create the Lookup Related Value type calculated field with name, **CF\_enrollment** and select **CF\_enrollment\_event\_status** as the return value.

    \[Omitted image "wd-learning-enroll-3.jpg"\] Alt text:

4.  Create Extract Multi-Instance type calculated field with name, **CF\_learning\_enrollment** and select **CF\_enrollment** as the return value.

    \[Omitted image "wd-learning-enroll-4.jpg"\] Alt text:

5.  Create the True/False condition type calculated field with name, **cf\_course\_type\_is\_blended**.

    \[Omitted image "wd-learning-enroll-5.jpg"\] Alt text:

6.  Create the True/False condition type calculated field with name, **Cf\_learning\_content\_type\_is\_digital\_course**.

    \[Omitted image "wd-learning-enroll-6.jpg"\] Alt text:

7.  Create the True/False condition type calculated field with name, **Cf\_learning\_content\_type\_is\_course\_offering**.

    \[Omitted image "wd-learning-enroll-7.jpg"\] Alt text:

8.  Create the True/False condition type calculated field with name, **Cf\_learning\_content\_type\_is\_program**.

    \[Omitted image "wd-learning-enroll-8.png"\] Alt text:

9.  Create the True/False condition type calculated field with name, **Cf\_learning\_content\_type\_is\_lesson**.

    \[Omitted image "wd-learning-enroll-9.jpg"\] Alt text:

10. Create the Lookup Related Value type calculated field with name, **CF\_blended course**.

    \[Omitted image "wd-learning-enroll-10.jpg"\] Alt text:

11. Create the Lookup Related Value type calculated field with name, **cf\_blended course id**.

    \[Omitted image "wd-learning-enroll-11.jpg"\] Alt text:

12. Create the Lookup Related Value type calculated field with name, **cf\_digital course**.

    \[Omitted image "wd-learning-enroll-12.jpg"\] Alt text:

13. Create the Lookup Related Value type calculated field with name, **cf\_digital\_course\_id**.

    \[Omitted image "wd-learning-enroll-13.jpg"\] Alt text:

14. Create the Lookup Related Value type calculated field with name, **cf\_course\_offering**.

    \[Omitted image "wd-learning-enroll-14.jpg"\] Alt text:

15. Create the Lookup Related Value type calculated field with name, **cf\_course\_offering\_id**.

    \[Omitted image "wd-learning-enroll-15.jpg"\] Alt text:

16. Create the Lookup Related Value type calculated field with name, **CF\_Program**.

    \[Omitted image "wd-learning-enroll-16.jpg"\] Alt text:

17. Create the Lookup Related Value type calculated field with name, **Cf\_program\_id**.

    \[Omitted image "wd-learning-enroll-17.jpg"\] Alt text:

18. Create the Lookup Related Value type calculated field with name, **CF\_lesson**.

    \[Omitted image "wd-learning-enroll-18.jpg"\] Alt text:

19. Create the Lookup Related Value type calculated field with name, **cf\_lesson\_id**.

    \[Omitted image "wd-learning-enroll-19.jpg"\] Alt text:

20. Create the Evaluate Expression type calculated field with name, **cf\_learning\_content\_id** and use all the calculated field created under **Calculated field 3**.

    \[Omitted image "wd-learning-enroll-20.jpg"\] Alt text:

21. Create the Learning Assignment report.

    1.  Access the **Create Custom Report** task.

    2.  Provide the report name, for example, `Test -Learning Assignment`.

    3.  Select report type as **Advanced**.

    4.  Clear the **Optimized for performance** check box.

    5.  Select data source as **Learning Assignments by Learning Organization**.

    6.  Don’t select the temporary report check box.

    7.  Click **Ok**.

        \[Omitted image "wd-learning-enroll-21.jpg"\] Alt text:

    8.  Select the report business object and report fields.

        \[Omitted image "wd-learning-enroll-22.jpg"\] Alt text: \[Omitted image "wd-learning-enroll-23.jpg"\] Alt text: \[Omitted image "wd-learning-enroll-24.jpg"\] Alt text:

    9.  In the **Group Column Headings** section, select all business objects.

        The **Group Column Heading** for each business object is empty.

        \[Omitted image "wd-learning-enroll-25.jpg"\] Alt text:

    10. In the **Sort** tab, select the values as shown here.

        \[Omitted image "wd-learning-enroll-26.jpg"\] Alt text:

    11. In the **Filter** tab, select the values as show here.

        Be sure to add parentheses.

        \[Omitted image "wd-learning-enroll-27.jpg"\] Alt text: \[Omitted image "wd-learning-enroll-28.jpg"\] Alt text:

    12. In the **Prompts** tab, select the **Populate Undefined prompt defaults** check box.

        \[Omitted image "wd-learning-enroll-29.jpg"\] Alt text:

    13. Select the values of prompts under the **Prompt Default** section and ensure that the values of the **Label For Prompt XML Alias** field are as shown here.

        \[Omitted image "wd-learning-enroll-30.jpg"\] Alt text:

    14. In the **Advanced** section, select the **Enable as webservice** check box and click **Ok**.

    15. After the report configuration is done, click the three dots icon and navigate to **Web Services** &gt; **View URLs**.

        \[Omitted image "wd-learning-enroll-31.png"\] Alt text:

    16. Specify values for the fields as per your requirement and click **Ok**.

        \[Omitted image "wd-learning-enroll-32.jpg"\] Alt text:

    17. In the View URLs Web Service page, click the active link you want to generate.

        The RaaS URL is displayed in a new browser tab.


