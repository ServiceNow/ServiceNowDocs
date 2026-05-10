---
title: Configure the Learning Assignment report
description: Configure the Learning Assignment report in Workday to retrieve user's learning assignments.
locale: en-US
release: australia
product: Integration Hub
classification: integration-hub
topic_type: task
last_updated: "2026-05-09"
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

    ![](../image/wd-learning-enroll-1.jpg)

2.  Create the True/False condition type calculated field with name, **CF\_enrollment\_event\_status**.

    ![](../image/wd-learning-enroll-2.jpg)

3.  Create the Lookup Related Value type calculated field with name, **CF\_enrollment** and select **CF\_enrollment\_event\_status** as the return value.

    ![](../image/wd-learning-enroll-3.jpg)

4.  Create Extract Multi-Instance type calculated field with name, **CF\_learning\_enrollment** and select **CF\_enrollment** as the return value.

    ![](../image/wd-learning-enroll-4.jpg)

5.  Create the True/False condition type calculated field with name, **cf\_course\_type\_is\_blended**.

    ![](../image/wd-learning-enroll-5.jpg)

6.  Create the True/False condition type calculated field with name, **Cf\_learning\_content\_type\_is\_digital\_course**.

    ![](../image/wd-learning-enroll-6.jpg)

7.  Create the True/False condition type calculated field with name, **Cf\_learning\_content\_type\_is\_course\_offering**.

    ![](../image/wd-learning-enroll-7.jpg)

8.  Create the True/False condition type calculated field with name, **Cf\_learning\_content\_type\_is\_program**.

    ![](../image/wd-learning-enroll-8.png)

9.  Create the True/False condition type calculated field with name, **Cf\_learning\_content\_type\_is\_lesson**.

    ![](../image/wd-learning-enroll-9.jpg)

10. Create the Lookup Related Value type calculated field with name, **CF\_blended course**.

    ![](../image/wd-learning-enroll-10.jpg)

11. Create the Lookup Related Value type calculated field with name, **cf\_blended course id**.

    ![](../image/wd-learning-enroll-11.jpg)

12. Create the Lookup Related Value type calculated field with name, **cf\_digital course**.

    ![](../image/wd-learning-enroll-12.jpg)

13. Create the Lookup Related Value type calculated field with name, **cf\_digital\_course\_id**.

    ![](../image/wd-learning-enroll-13.jpg)

14. Create the Lookup Related Value type calculated field with name, **cf\_course\_offering**.

    ![](../image/wd-learning-enroll-14.jpg)

15. Create the Lookup Related Value type calculated field with name, **cf\_course\_offering\_id**.

    ![](../image/wd-learning-enroll-15.jpg)

16. Create the Lookup Related Value type calculated field with name, **CF\_Program**.

    ![](../image/wd-learning-enroll-16.jpg)

17. Create the Lookup Related Value type calculated field with name, **Cf\_program\_id**.

    ![](../image/wd-learning-enroll-17.jpg)

18. Create the Lookup Related Value type calculated field with name, **CF\_lesson**.

    ![](../image/wd-learning-enroll-18.jpg)

19. Create the Lookup Related Value type calculated field with name, **cf\_lesson\_id**.

    ![](../image/wd-learning-enroll-19.jpg)

20. Create the Evaluate Expression type calculated field with name, **cf\_learning\_content\_id** and use all the calculated field created under **Calculated field 3**.

    ![](../image/wd-learning-enroll-20.jpg)

21. Create the Learning Assignment report.

    1.  Access the **Create Custom Report** task.

    2.  Provide the report name, for example, `Test -Learning Assignment`.

    3.  Select report type as **Advanced**.

    4.  Clear the **Optimized for performance** check box.

    5.  Select data source as **Learning Assignments by Learning Organization**.

    6.  Don’t select the temporary report check box.

    7.  Click **Ok**.

        ![](../image/wd-learning-enroll-21.jpg)

    8.  Select the report business object and report fields.

        ![](../image/wd-learning-enroll-22.jpg) ![](../image/wd-learning-enroll-23.jpg) ![](../image/wd-learning-enroll-24.jpg)

    9.  In the **Group Column Headings** section, select all business objects.

        The **Group Column Heading** for each business object is empty.

        ![](../image/wd-learning-enroll-25.jpg)

    10. In the **Sort** tab, select the values as shown here.

        ![](../image/wd-learning-enroll-26.jpg)

    11. In the **Filter** tab, select the values as show here.

        Be sure to add parentheses.

        ![](../image/wd-learning-enroll-27.jpg) ![](../image/wd-learning-enroll-28.jpg)

    12. In the **Prompts** tab, select the **Populate Undefined prompt defaults** check box.

        ![](../image/wd-learning-enroll-29.jpg)

    13. Select the values of prompts under the **Prompt Default** section and ensure that the values of the **Label For Prompt XML Alias** field are as shown here.

        ![](../image/wd-learning-enroll-30.jpg)

    14. In the **Advanced** section, select the **Enable as webservice** check box and click **Ok**.

    15. After the report configuration is done, click the three dots icon and navigate to **Web Services** &gt; **View URLs**.

        ![](../image/wd-learning-enroll-31.png)

    16. Specify values for the fields as per your requirement and click **Ok**.

        ![](../image/wd-learning-enroll-32.jpg)

    17. In the View URLs Web Service page, click the active link you want to generate.

        The RaaS URL is displayed in a new browser tab.


