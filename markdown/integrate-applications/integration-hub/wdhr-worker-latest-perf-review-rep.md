---
title: Workday configuration for workers latest performance review report
description: Retrieve the workers latest performance review information by creating the workers latest performance review report.
locale: en-US
release: zurich
product: Integration Hub
classification: integration-hub
topic_type: task
last_updated: "2025-01-12"
reading_time_minutes: 4
breadcrumb: [Workday HR Spoke, Integration Hub spokes, Build integrations, Integration Hub, Workflow Data Fabric]
---

# Workday configuration for workers latest performance review report

Retrieve the workers latest performance review information by creating the workers latest performance review report.

## Before you begin

Role required: User with access to report creation and the Workers by Organization data source.

-   Create all calculated fields for this report before developing the report, so that while creating report all fields are available.
-   While creating the report, ensure that the report name, report field names or column heading override for the respective field \(if given in report document\) is same as it is in report document.

    Report field label should be same as in report doc. Else, the developed action will fail.

-   While creating filter, ensure that you add parenthesis on filter.
-   All reports must be owned by the ISU user which will be used for accessing these actions on the ServiceNow platform.
-   In the **Advanced** section, **Enable as webservice** option should be selected.

Create all calculated fields so that these fields can be used while developing report.

-   Calculated field 1:
    -   Create True False condition type calculated field named **CF\_review\_period**. ![Calculated field of true or false condition type](../image/wdhr-worker-latest-perf-review-rep-1.png)
    -   Create Extract Multi-instance type calculated field named **CF\_latest\_review**. ![Calculated field of extract multi-instance type](../image/wdhr-worker-latest-perf-review-rep-2.png)
-   Calculated field 2: Create Aggregate Related Instances type calculated field named **CF\_Competencies**. ![Calculated field of Aggregate Related Instances type example 1](../image/wdhr-worker-latest-perf-review-rep-3.png)
-   Calculated field 3: Create Aggregate Related Instances type calculated field named **CF Content Evaluation - Accomplishments**. ![Calculated field of Aggregate Related Instances type example 2](../image/wdhr-worker-latest-perf-review-rep-4.png)
-   Calculated field 4: Create Aggregate Related Instances type calculated field named **CF\_Content Evaluation - Areas for Development**. ![Calculated field of Aggregate Related Instances type example 3](../image/wdhr-worker-latest-perf-review-rep-5.png)
-   Calculated field 5: Create Aggregate Related Instances type calculated field named **CF\_Content Evaluation - Career Interests**. ![Calculated field of Aggregate Related Instances type example 4](../image/wdhr-worker-latest-perf-review-rep-6.png)
-   Calculated field 6: Create Aggregate Related Instances type calculated field named **CF\_Content Evaluation - Goals**. ![Calculated field of Aggregate Related Instances type example 5](../image/wdhr-worker-latest-perf-review-rep-7.png)
-   Calculated field 7: Create Aggregate Related Instances type calculated field named **CF\_Content Evaluation - Responsibilities**. ![Calculated field of Aggregate Related Instances type example 6](../image/wdhr-worker-latest-perf-review-rep-8.png)
-   Calculated field 8: Create Extract Multi-instance type calculated field named **CF\_latest\_review**. ![Calculated field of extract multi-instance type](../image/wdhr-worker-latest-perf-review-rep-9.png)
-   Calculated field 9: Create True False condition type calculated field named **CF\_evaluated by manager**. ![True or false condition in a calculated field](../image/wdhr-worker-latest-perf-review-rep-10.png)

## Procedure

1.  Access the Create Custom Report task.

2.  Provide the report name such as, `CR Employee latest performance review and feedback details`.

3.  Select report type as **Advanced**.

4.  Clear the **Optimized for performance** option.

5.  Select **Data Source** as **Workers by Organization**.

6.  Do not select the **Temporary report** option and click **OK**.

    ![View Custom Report example](../image/wdhr-worker-latest-perf-review-rep-11.png)

7.  Select the report business object and report fields.

    ![Example 1 business objects and report fields](../image/wdhr-worker-latest-perf-review-rep-12.png)![Example 2 business objects and report fields](../image/wdhr-worker-latest-perf-review-rep-13.png)![Example 3 business objects and report fields](../image/wdhr-worker-latest-perf-review-rep-14.png)![Example 4 business objects and report fields](../image/wdhr-worker-latest-perf-review-rep-15.png)

8.  In **Group Column Heading** section, select all business object as below.

    **Group Column Heading** for each business object will be blank. ![Group Column Heading section of the report](../image/wdhr-worker-latest-perf-review-rep-16.png)

9.  In **Sort** section, under **Sub level sort**, select the value as shown below.

    ![Example 1 of sub level sort](../image/wdhr-worker-latest-perf-review-rep-17.png)![Example 2 of sub level sort](../image/wdhr-worker-latest-perf-review-rep-18.png)![Example 3 of sub level sort](../image/wdhr-worker-latest-perf-review-rep-19.png)![Example 4 of sub level sort](../image/wdhr-worker-latest-perf-review-rep-20.png)

10. In **Filter** section, select the value as given below.

    Ensure to add parenthesis. ![Filter section of the report](../image/wdhr-worker-latest-perf-review-rep-21.png)

11. In **Sub-Filter** section, select the value as given below.

    Ensure to add parenthesis. ![Example1 sub-filter](../image/wdhr-worker-latest-perf-review-rep-22.png)![Example2 sub-filter](../image/wdhr-worker-latest-perf-review-rep-23.png)![Example3 sub-filter](../image/wdhr-worker-latest-perf-review-rep-24.png)![Example4 sub-filter](../image/wdhr-worker-latest-perf-review-rep-25.png)

12. In **Prompts** section, select the **Populate Undefined Prompt Defaults** option.

    ![Populate Undefined Prompt Defaults option in the Prompts section](../image/wdhr-worker-latest-perf-review-rep-26.png)

13. Select the value of prompts as given below under Prompt default section.

    Make sure the **Label For Prompt XML Alias** of all prompt fields must be same.

    ![Prompt Defaults section of the report](../image/wdhr-worker-latest-perf-review-rep-27.png)

14. In **Advanced** section, select **Enable as webservice** option and click **OK**.

15. Click on three dots icon and navigate to **Web Services** &gt; **View URLs** option once report configuration is done.

    ![View URLs option in the View Custom Report](../image/wdhr-worker-latest-perf-review-rep-28.png)

16. Select the organization for which you want to run this report, select the option if you want to include subordinate organization and manager, and select the date range for which you want to see the data.

    ![Organization, managers, subordinate organizations, and date range of in the View URLs Web Service page](../image/wdhr-worker-latest-perf-review-rep-29.png)

17. In View URLs Web Service page, click the marked icon under the **CSV** section.

    A new browser tab is opened.

    ![CSV option in View URLs Web Service page](../image/wdhr-worker-latest-perf-review-rep-30.png)

18. View the RaaS URL of the report in the new browser tab.

    The RaaS URL of the report is displayed in new browser tab and you can obtain these details from the link.

    ![RaaS URL of the report](../image/wdhr-worker-latest-perf-review-rep-31.png)

    -   `https://wd2-impl-services1.workday.com` is the base URL of customer's workday tenant.
    -   **Tenant\_Name** is the customer's workday tenant.
    -   **Report\_Owner\_user\_name** represents user name of the report's owner.
    -   **Report\_Name** is the report name.

