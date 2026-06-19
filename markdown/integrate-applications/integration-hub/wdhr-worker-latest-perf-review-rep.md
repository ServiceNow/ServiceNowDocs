---
title: Workday configuration for workers latest performance review report
description: Retrieve the workers latest performance review information by creating the workers latest performance review report.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/zurich/integrate-applications/integration-hub/wdhr-worker-latest-perf-review-rep.html
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
    -   Create True False condition type calculated field named **CF\_review\_period**. \[Omitted image "wdhr-worker-latest-perf-review-rep-1.png"\] Alt text: Calculated field of true or false condition type
    -   Create Extract Multi-instance type calculated field named **CF\_latest\_review**. \[Omitted image "wdhr-worker-latest-perf-review-rep-2.png"\] Alt text: Calculated field of extract multi-instance type
-   Calculated field 2: Create Aggregate Related Instances type calculated field named **CF\_Competencies**. \[Omitted image "wdhr-worker-latest-perf-review-rep-3.png"\] Alt text: Calculated field of Aggregate Related Instances type example 1
-   Calculated field 3: Create Aggregate Related Instances type calculated field named **CF Content Evaluation - Accomplishments**. \[Omitted image "wdhr-worker-latest-perf-review-rep-4.png"\] Alt text: Calculated field of Aggregate Related Instances type example 2
-   Calculated field 4: Create Aggregate Related Instances type calculated field named **CF\_Content Evaluation - Areas for Development**. \[Omitted image "wdhr-worker-latest-perf-review-rep-5.png"\] Alt text: Calculated field of Aggregate Related Instances type example 3
-   Calculated field 5: Create Aggregate Related Instances type calculated field named **CF\_Content Evaluation - Career Interests**. \[Omitted image "wdhr-worker-latest-perf-review-rep-6.png"\] Alt text: Calculated field of Aggregate Related Instances type example 4
-   Calculated field 6: Create Aggregate Related Instances type calculated field named **CF\_Content Evaluation - Goals**. \[Omitted image "wdhr-worker-latest-perf-review-rep-7.png"\] Alt text: Calculated field of Aggregate Related Instances type example 5
-   Calculated field 7: Create Aggregate Related Instances type calculated field named **CF\_Content Evaluation - Responsibilities**. \[Omitted image "wdhr-worker-latest-perf-review-rep-8.png"\] Alt text: Calculated field of Aggregate Related Instances type example 6
-   Calculated field 8: Create Extract Multi-instance type calculated field named **CF\_latest\_review**. \[Omitted image "wdhr-worker-latest-perf-review-rep-9.png"\] Alt text: Calculated field of extract multi-instance type
-   Calculated field 9: Create True False condition type calculated field named **CF\_evaluated by manager**. \[Omitted image "wdhr-worker-latest-perf-review-rep-10.png"\] Alt text: True or false condition in a calculated field

## Procedure

1.  Access the Create Custom Report task.

2.  Provide the report name such as, `CR Employee latest performance review and feedback details`.

3.  Select report type as **Advanced**.

4.  Clear the **Optimized for performance** option.

5.  Select **Data Source** as **Workers by Organization**.

6.  Do not select the **Temporary report** option and click **OK**.

    \[Omitted image "wdhr-worker-latest-perf-review-rep-11.png"\] Alt text: View Custom Report example

7.  Select the report business object and report fields.

    \[Omitted image "wdhr-worker-latest-perf-review-rep-12.png"\] Alt text: Example 1 business objects and report fields\[Omitted image "wdhr-worker-latest-perf-review-rep-13.png"\] Alt text: Example 2 business objects and report fields\[Omitted image "wdhr-worker-latest-perf-review-rep-14.png"\] Alt text: Example 3 business objects and report fields\[Omitted image "wdhr-worker-latest-perf-review-rep-15.png"\] Alt text: Example 4 business objects and report fields

8.  In **Group Column Heading** section, select all business object as below.

    **Group Column Heading** for each business object will be blank. \[Omitted image "wdhr-worker-latest-perf-review-rep-16.png"\] Alt text: Group Column Heading section of the report

9.  In **Sort** section, under **Sub level sort**, select the value as shown below.

    \[Omitted image "wdhr-worker-latest-perf-review-rep-17.png"\] Alt text: Example 1 of sub level sort\[Omitted image "wdhr-worker-latest-perf-review-rep-18.png"\] Alt text: Example 2 of sub level sort\[Omitted image "wdhr-worker-latest-perf-review-rep-19.png"\] Alt text: Example 3 of sub level sort\[Omitted image "wdhr-worker-latest-perf-review-rep-20.png"\] Alt text: Example 4 of sub level sort

10. In **Filter** section, select the value as given below.

    Ensure to add parenthesis. \[Omitted image "wdhr-worker-latest-perf-review-rep-21.png"\] Alt text: Filter section of the report

11. In **Sub-Filter** section, select the value as given below.

    Ensure to add parenthesis. \[Omitted image "wdhr-worker-latest-perf-review-rep-22.png"\] Alt text: Example1 sub-filter\[Omitted image "wdhr-worker-latest-perf-review-rep-23.png"\] Alt text: Example2 sub-filter\[Omitted image "wdhr-worker-latest-perf-review-rep-24.png"\] Alt text: Example3 sub-filter\[Omitted image "wdhr-worker-latest-perf-review-rep-25.png"\] Alt text: Example4 sub-filter

12. In **Prompts** section, select the **Populate Undefined Prompt Defaults** option.

    \[Omitted image "wdhr-worker-latest-perf-review-rep-26.png"\] Alt text: Populate Undefined Prompt Defaults option in the Prompts section

13. Select the value of prompts as given below under Prompt default section.

    Make sure the **Label For Prompt XML Alias** of all prompt fields must be same.

    \[Omitted image "wdhr-worker-latest-perf-review-rep-27.png"\] Alt text: Prompt Defaults section of the report

14. In **Advanced** section, select **Enable as webservice** option and click **OK**.

15. Click on three dots icon and navigate to **Web Services** &gt; **View URLs** option once report configuration is done.

    \[Omitted image "wdhr-worker-latest-perf-review-rep-28.png"\] Alt text: View URLs option in the View Custom Report

16. Select the organization for which you want to run this report, select the option if you want to include subordinate organization and manager, and select the date range for which you want to see the data.

    \[Omitted image "wdhr-worker-latest-perf-review-rep-29.png"\] Alt text: Organization, managers, subordinate organizations, and date range of in the View URLs Web Service page

17. In View URLs Web Service page, click the marked icon under the **CSV** section.

    A new browser tab is opened.

    \[Omitted image "wdhr-worker-latest-perf-review-rep-30.png"\] Alt text: CSV option in View URLs Web Service page

18. View the RaaS URL of the report in the new browser tab.

    The RaaS URL of the report is displayed in new browser tab and you can obtain these details from the link.

    \[Omitted image "wdhr-worker-latest-perf-review-rep-31.png"\] Alt text: RaaS URL of the report

    -   `https://wd2-impl-services1.workday.com` is the base URL of customer's workday tenant.
    -   **Tenant\_Name** is the customer's workday tenant.
    -   **Report\_Owner\_user\_name** represents user name of the report's owner.
    -   **Report\_Name** is the report name.

