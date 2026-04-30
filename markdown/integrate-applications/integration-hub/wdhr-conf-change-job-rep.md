---
title: Workday configuration for change job event report
description: Create report to retrieve change job event data based on the provided time duration.
locale: en-US
release: zurich
product: Integration Hub
classification: integration-hub
topic_type: task
last_updated: "2025-12-04"
reading_time_minutes: 3
breadcrumb: [Workday HR Spoke, Integration Hub spokes, Build integrations, Integration Hub, Workflow Data Fabric]
---

# Workday configuration for change job event report

Create report to retrieve change job event data based on the provided time duration.

## Before you begin

Role required: User with access to report creation and the Business Process Transactions data source.

-   Create all calculated fields for this report before developing the report, so that while creating report all fields are available.
-   While creating the report, ensure that the report name, report field names or column heading override for the respective field \(if given in report document\) is same as it is in report document.

    Report field label should be same as in report doc. Else, the developed action will fail.

-   While creating filter ensure to add parenthesis on filter.
-   All reports must be owned by the ISU user which will be used for accessing these actions on the ServiceNow platform.
-   In the **Advanced** section, **Enable as webservice** option should be selected.

Create all calculated fields so that these fields can be used while developing report.

1.  Cal field 1: Create Aggregate Related Instances type calculated field named **CF\_Comment\_By\_Employee\_ID**.

    ![Aggregate Related Instances type calculated field.](../image/wdhr-conf-change-job-rep-1.jpg)

2.  Create Aggregate Related Instances type calculated field named **CF\_Comment\_by\_worker** and use **CF\_Comment\_By\_Employee\_ID** in source field.

    ![Aggregate Related Instances type calculated field](../image/wdhr-conf-change-job-rep-2.jpg)


## Procedure

1.  Access the Create Custom Report task.

2.  Provide the report name such as, `RPT_Change_job_event_report`.

3.  Select report type as **Advanced**.

4.  Clear the **Optimized for performance** option.

5.  Select **Data Source** as **Business Process Transactions**.

6.  Do not select the **Temporary report** option and click **OK**.

    ![RPT_Change_job_event_report report.](../image/wdhr-conf-change-job-rep-3.jpg)

7.  Select the report business object and report fields.

    ![Report business object and report fields.](../image/wdhr-conf-change-job-rep-4.jpg)![Report business object and report fields.](../image/wdhr-conf-change-job-rep-5.jpg)

8.  In **Group Column Heading** section, select all business object as below.

    **Group Column Heading** for each business object will be blank.

    ![Business objects in Group Column Heading.](../image/wdhr-conf-change-job-rep-6.jpg)

9.  In **Filter** section, select the value as given below.

    Ensure to add parenthesis.![Select values in the Filter section.](../image/wdhr-conf-change-job-rep-7.jpg)

10. In **Prompts** section, select the **Populate Undefined Prompt Defaults** option.

    ![Select the Populate Undefined Prompt Defaults option.](../image/wdhr-conf-change-job-rep-8.jpg)

11. Select the value of prompts as given below under Prompt default section.

    Make sure the **Label For Prompt XML Alias** of all prompt fields must be same.

    ![Same Label For Prompt XML Alias for all prompt fields.](../image/wdhr-conf-change-job-rep-9.jpg)

12. In **Advanced** section, select **Enable as webservice** option and click **OK**.

13. Click on three dots icon and navigate to **Web Services** &gt; **View URLs** option once report configuration is done.

    ![View URLs.](../image/wdhr-conf-change-job-rep-10.jpg)

14. Select **Business Processes** as **Change Job**, **Transaction Status** as **In Progress**, time range in **Start Date** and **End Date** parameter and click **OK**.

    **Note:** This step is one-time process required to get the WID of business process and transaction status. After the initial full load, transaction status ID is not needed as details of all events will be retrieved; **In Progress** as well as **Completed**.

    ![Details for generating report.](../image/wdhr-conf-change-job-rep-11.jpg)

15. In View URLs Web Service page, click the marked icon under the **CSV** section.

    A new browser tab is opened.

    ![](../image/wdhr-conf-change-job-rep-12.jpg)

    The RaaS URL of the report is displayed in new browser tab and you can obtain these details from the link.

    ![](../image/wdhr-conf-change-job-rep-13.jpg)

    -   `https://wd2-impl-services1.workday.com` is the base URL of customer’s workday tenant.
    -   **Tenant\_Name** is the customer’s workday tenant.
    -   **Report\_Owner\_user\_name** represents user name of the report’s owner.
    -   **RPT\_Change\_Job\_event\_report** is the report name.
    -   **Business\_Processes%21WID=\(32 character code\)** is the business process WID and **Transaction\_Status%21WID=\(32 character code\)** is the Transaction WID.
    **Note:** After the initial full load, Transaction Status WID is not used as parameter as all in progress and completed transactions will be retrieved.

    |Usecase|Business process|Workday ID|
    |-------|----------------|----------|
    |Change job|Change job|c24592468ed147b2ac6d0de4d699a7da|

    Workday ID of **In Progress** transaction status is e2d08afc53614c37b32b31270bb8bee3.


