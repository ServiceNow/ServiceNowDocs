---
title: Configure the Track Approval report
description: Configure the Learning Assignment report in Workday to retrieve worker's inbox items like to-dos, action items, approval, and so on.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/integrate-applications/integration-hub/wd-learning-confrep3.html
release: australia
product: Integration Hub
classification: integration-hub
topic_type: task
last_updated: "2026-06-21"
reading_time_minutes: 3
breadcrumb: [Workday Learning Spoke, Integration Hub spokes, Build integrations, Integration Hub, Workflow Data Fabric]
---

# Configure the Track Approval report

Configure the Learning Assignment report in Workday to retrieve worker's inbox items like to-dos, action items, approval, and so on.

## Before you begin

User with access to report creation and the Business process event steps report data source.

## About this task

-   For identification purposes, all calculated field name starts with **CF**.
-   Create all calculated fields for this report before developing the report. Thus, all fields are available while creating the report.
-   Report name can be different while creating the report. But ensure that the report field name or column heading override for the respective field \(if it’s given in the report document\) is same as it is in the report document. Report field label should be same as it is in the report document. Else, the developed action fails.
-   **Group Column Heading** for each business object in the **Group Column Headings** section should be empty.
-   Ensure that you add parenthesis in filter while creating it.
-   All reports must be shared or owned by the ISU user that accesses these actions on the ServiceNow platform.
-   In the **Advanced** section, select the **Enable as webservice** check box.

## Procedure

1.  Create increment and decrement type calculated field with name, **CF\_Last\_functionally\_updated\_-1**.

    \[Omitted image "wd-track-approval-1.jpg"\] Alt text:

2.  Create the Lookup Value As Of Date type calculated field with name, **cf\_assigned\_to\_worker\_previous** and use **CF\_Last\_functionally\_updated\_-1** in this field.

    \[Omitted image "wd-track-approval-2.jpg"\] Alt text:

3.  Create the Text Constant type calculated field with name, **Cf\_text\_0**.

    \[Omitted image "wd-track-approval-3.jpg"\] Alt text:

4.  Create the Text Constant type calculated field with name, **CF\_Text\_as\_1**.

    \[Omitted image "wd-track-approval-4.jpg"\] Alt text:

5.  Create the True/False condition type calculated field with name, **cf\_competed\_by\_is\_not\_equal\_old\_assignee**.

    \[Omitted image "wd-track-approval-5.jpg"\] Alt text:

6.  Create Evaluate Expression calculated field with name, **CF\_EE\_Completed\_by\_admin\_exist\_as\_old\_Assignee\_or\_not**.

    \[Omitted image "wd-track-approval-6.jpg"\] Alt text:

7.  Create the Text Constant type calculated field with name, **CF\_Text**.

    \[Omitted image "wd-track-approval-7.jpg"\] Alt text:

8.  Create the Lookup Related Value type calculated field with name, **CF\_Action\_Event**.

    \[Omitted image "wd-track-approval-8.jpg"\] Alt text:

9.  Create the Concatenate Text type calculated field with name, **CF\_inbox\_SUbject**.

    \[Omitted image "wd-track-approval-9.jpg"\] Alt text:

10. Create the Text Constant type calculated field with name, **CF\_url**.

    \[Omitted image "wd-track-approval-10.jpg"\] Alt text:

11. Create the Lookup Related Value type calculated field with name, **CF\_business\_pro\_transaction**.

    \[Omitted image "wd-track-approval-11.jpg"\] Alt text:

12. Create the Lookup Related Value type calculated field with name, **CF\_BP\_Wid**.

    \[Omitted image "wd-track-approval-12.jpg"\] Alt text:

13. Create the Concatenate Text type calculated field with name, **CF\_Inbox\_url**.

    \[Omitted image "wd-track-approval-13.jpg"\] Alt text:

14. Create the Lookup Related Value type calculated field with name, **cf\_step\_id**.

    \[Omitted image "wd-track-approval-14.jpg"\] Alt text:

15. Create the Lookup Related Value type calculated field with name, **CF\_subject\_id**.

    \[Omitted image "wd-track-approval-15.jpg"\] Alt text:

16. Create the Concatenate Text type calculated field with name, **CF\_subject\_and\_step\_id**.

    \[Omitted image "wd-track-approval-16.jpg"\] Alt text:

17. Create the Lookup Related Value type calculated field with name, **CF\_sent\_back**.

    \[Omitted image "wd-track-approval-17.jpg"\] Alt text:

18. Create the Lookup Related Value type calculated field with name, **Cf\_parent\_business\_process\_definition**.

    \[Omitted image "wd-track-approval-18.jpg"\] Alt text:

19. Create the Increment or Decrement Date type calculated field with name, **CF\_Last\_updated\_on-1**.

    \[Omitted image "wd-track-approval-19.jpg"\] Alt text:

20. Create the Lookup Value As Of Date type calculated field with name, **cf\_status\_as\_of\_moment** and use **CF\_Last\_updated\_on-1** in this field.

    \[Omitted image "wd-track-approval-20.jpg"\] Alt text:

21. Create the Track Approval report.

    1.  Access **Create Custom Report** task.

    2.  Provide the report name such as, **SNIH\_Inbox\_Items**.

    3.  Select report type as **Advanced**.

    4.  Clear the **Optimized for performance** check box.

    5.  Select **Business Process Event steps** for **Data Source**.

    6.  Don't select **temporary report** check box.

    7.  Click **Ok**.

        \[Omitted image "wd-track-approval-21.jpg"\] Alt text:

    8.  Select the report business object and report fields as shown here.

        \[Omitted image "wd-track-approval-22.jpg"\] Alt text: \[Omitted image "wd-track-approval-23.jpg"\] Alt text:

    9.  In the **Group Column Headings** section, select the business object as shown here.

        The **Group Column Heading** for each business object is empty.

        \[Omitted image "wd-track-approval-24.jpg"\] Alt text:

    10. In the **Filter conditions for filtering on instances** section, select the values as shown.

        Be sure to add parentheses.

        \[Omitted image "wd-learning-filter-1.jpg"\] Alt text: \[Omitted image "wd-learning-filter-2.jpg"\] Alt text: \[Omitted image "wd-learning-filter-3.jpg"\] Alt text: \[Omitted image "wd-learning-filter-4.jpg"\] Alt text: \[Omitted image "wd-learning-filter-5.jpg"\] Alt text: \[Omitted image "wd-learning-filter-6.jpg"\] Alt text: \[Omitted image "wd-learning-filter-7.jpg"\] Alt text: \[Omitted image "wd-learning-filter-8.jpg"\] Alt text:

    11. In the **Prompts** section, select the **Populate undefined prompt defaults** check box.

        \[Omitted image "wd-track-approval-30.jpg"\] Alt text:

    12. Select the values under the **Prompt Default** section and ensure that the values of **Label For Prompt XML Alias** are as shown here.

        \[Omitted image "wd-track-approval-31.jpg"\] Alt text: \[Omitted image "wd-track-approval-32.jpg"\] Alt text:

    13. In the **Advanced** section, select the **Enable as webservice** check box and click **Ok**.

    14. After the report configuration is done, click the three dots icon and navigate to **Web Services** &gt; **View URLs**.

        \[Omitted image "wd-track-approval-33.jpg"\] Alt text:

    15. Specify values for the fields on the View URLs Web Service form and click **Ok**.

        \[Omitted image "wd-track-approval-34.jpg"\] Alt text:

    16. In the View URLs Web Service page, click the **CSV** icon.

        \[Omitted image "wd-track-approval-35.jpg"\] Alt text:

        The RaaS URL of the report is displayed in a new browser tab.

        \[Omitted image "wd-track-approval-36.jpg"\] Alt text:

        -   `https://wd2-impl-services1.workday.com` is the base URL of your Workday tenant.
        -   `Tenant_Name` is your Workday tenant.
        -   `Report_Owner_user_name` is the user name of the report’s owner.
        -   `SNIh_Inbox_Items` is the report name.

