---
title: Workday configuration for workers performance review historical data report
description: Retrieve the workers historical performance review information by creating the workers performance review historical data report.
locale: en-US
release: zurich
product: Integration Hub
classification: integration-hub
topic_type: task
last_updated: "2026-01-29"
reading_time_minutes: 3
breadcrumb: [Workday HR Spoke, Integration Hub spokes, Build integrations, Integration Hub, Workflow Data Fabric]
---

# Workday configuration for workers performance review historical data report

Retrieve the workers historical performance review information by creating the workers performance review historical data report.

## Before you begin

Role required: User with access to report creation and the Workers by Organization data source.

-   Create all calculated fields for this report before developing the report, so that while creating report all fields are available.
-   While creating the report, ensure that the report name, report field names or column heading override for the respective field \(if given in report document\) is same as it is in report document.

    Report field label should be same as in report doc. Else, the developed action will fail.

-   While creating filter, ensure that you add parenthesis on filter.
-   All reports must be owned by the ISU user which will be used for accessing these actions on the ServiceNow platform.
-   In the **Advanced** section, **Enable as webservice** option should be selected.

Create all calculated fields so that these fields can be used while developing report.

-   Calculated field 1: Create Aggregate Related Instances type calculated field named **CF\_Competencies\_all**

    ![Workday HR spoke.](../image/wdhr-worker-perf-review-hist-rep-1.png)

    .

-   Calculated field 2: Create Aggregate Related Instances type calculated field named **CF Content Evaluation - Accomplishments all**

    ![Workday HR spoke.](../image/wdhr-worker-perf-review-hist-rep-2.png)

    .

-   Calculated field 3: Create Aggregate Related Instances type calculated field named **CF\_Content Evaluation - Areas for Development all**

    ![Workday HR spoke.](../image/wdhr-worker-perf-review-hist-rep-3.png)

    .

-   Calculated field 4: Create Aggregate Related Instances type calculated field named **CF\_Content Evaluation - Career Interests all**

    ![Workday HR spoke.](../image/wdhr-worker-perf-review-hist-rep-4.png)

    .

-   Calculated field 5: Create Aggregate Related Instances type calculated field named **CF\_Content Evaluation - Goals all**

    ![Workday HR spoke.](../image/wdhr-worker-perf-review-hist-rep-5.png)

    .

-   Calculated field 6: Create Aggregate Related Instances type calculated field named **CF\_Content Evaluation - Responsibilities all**

    ![Workday HR spoke.](../image/wdhr-worker-perf-review-hist-rep-6.png)

    .

-   Calculated field 7: Create True False condition type calculated field named **CF\_evaluated by manager**

    ![Workday HR spoke.](../image/wdhr-worker-perf-review-hist-rep-7.png)

    .


## Procedure

1.  Access the Create Custom Report task.

2.  Provide the report name such as, `CR Employee performance review historical data`.

3.  Select report type as **Advanced**.

4.  Clear the **Optimized for performance** option.

5.  Select **Data Source** as **Workers by Organization**.

6.  Do not select the **Temporary report** option and click **OK**.

    ![Workday HR spoke.](../image/wdhr-worker-perf-review-hist-rep-8.png)

7.  Select the report business object and report fields.

    ![Workday HR spoke.](../image/wdhr-worker-perf-review-hist-rep-9.png)

    ![Workday HR spoke.](../image/wdhr-worker-perf-review-hist-rep-10.png)Workday HR spoke.

    ![Workday HR spoke.](../image/wdhr-worker-perf-review-hist-rep-11.png)

    ![Workday HR spoke.](../image/wdhr-worker-perf-review-hist-rep-12.png)

8.  In **Group Column Heading** section, select all business object as below.

    ![Workday HR spoke.](../image/wdhr-worker-perf-review-hist-rep-13.png)**Group Column Heading** for each business object will be blank.

9.  In **Sort** section, select the value as shown below.

    ![Workday HR spoke.](../image/wdhr-worker-perf-review-hist-rep-14.png)

10. In **Sort** section, under **Sub level sort**, select the value as shown below.

    ![Workday HR spoke.](../image/wdhr-worker-perf-review-hist-rep-15.png)

    ![Workday HR spoke.](../image/wdhr-worker-perf-review-hist-rep-16.png)

    ![Workday HR spoke.](../image/wdhr-worker-perf-review-hist-rep-17.png)

    ![Workday HR spoke.](../image/wdhr-worker-perf-review-hist-rep-18.png)

11. In **Filter** section, select the value as given below.

    Ensure to add parenthesis. ![Workday HR spoke.](../image/wdhr-worker-perf-review-hist-rep-19.png)

12. In **Sub-Filter** section, select the value as given below.

    Ensure to add parenthesis.

    ![Workday HR spoke.](../image/wdhr-worker-perf-review-hist-rep-20.png)

    ![Workday HR spoke.](../image/wdhr-worker-perf-review-hist-rep-21.png)

    ![Workday HR spoke.](../image/wdhr-worker-perf-review-hist-rep-22.png)

13. In **Prompts** section, select the **Populate Undefined Prompt Defaults** option.

    ![Workday HR spoke.](../image/wdhr-worker-perf-review-hist-rep-23.png)

14. Select the value of prompts as given below under Prompt default section.

    Make sure the **Label For Prompt XML Alias** of all prompt fields must be same.

    ![Workday HR spoke.](../image/wdhr-worker-perf-review-hist-rep-24.png)

15. In **Advanced** section, select **Enable as webservice** option and click **OK**.

16. Click on three dots icon and navigate to **Web Services** &gt; **View URLs** option once report configuration is done.

    ![Workday HR spoke.](../image/wdhr-worker-perf-review-hist-rep-25.png)

17. Select the **Organization** for which you want to run this report and select the option if you want to include subordinate organization and managers.

    ![Workday HR spoke.](../image/wdhr-worker-perf-review-hist-rep-26.png)

18. In View URLs Web Service page, click the marked icon under the **CSV** section.

    ![Workday HR spoke.](../image/wdhr-worker-perf-review-hist-rep-27.png)

    A new browser tab is opened.

    The RaaS URL of the report is displayed in new browser tab and you can obtain these details from the link.

    -   `https://wd2-impl-services1.workday.com` is the base URL of customer's workday tenant.
    -   **Tenant\_Name** is the customer's workday tenant.
    -   **Report\_Owner\_user\_name** represents user name of the report's owner.
    -   **Report\_Name** is the report name.
    ![Workday HR spoke.](../image/wdhr-worker-perf-review-hist-rep-28.png)

    **Note:** Each section in the report \(such as competencies and goals\) is independent, but these sections will be grouped together to assess a specific worker's performance. For example, to retrieve Worker A's performance review information for the year 2023, it is necessary to examine all records from each section where the assessment date falls within the 2023 review period.


