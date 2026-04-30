---
title: Workday configuration for job requisition event report
description: Retrieve the Create Job Requisition event data based on time duration by creating the job requisition event report.
locale: en-US
release: zurich
product: Integration Hub
classification: integration-hub
topic_type: task
last_updated: "2025-12-06"
reading_time_minutes: 2
breadcrumb: [Workday HR Spoke, Integration Hub spokes, Build integrations, Integration Hub, Workflow Data Fabric]
---

# Workday configuration for job requisition event report

Retrieve the Create Job Requisition event data based on time duration by creating the job requisition event report.

## Before you begin

Role required: User with access to report creation and the Business Process Transactions data source.

-   Create all calculated fields for this report before developing the report, so that while creating report all fields are available.
-   While creating the report, ensure that the report name, report field names or column heading override for the respective field \(if given in report document\) is same as it is in report document.

    Report field label should be same as in report doc. Else, the developed action will fail.

-   While creating filter, ensure that you add parenthesis on filter.
-   All reports must be owned by the ISU user which will be used for accessing these actions on the ServiceNow platform.
-   In the **Advanced** section, **Enable as webservice** option should be selected.

Create all calculated fields so that these fields can be used while developing report.

-   Calculated field 1:
    -   Create Aggregate Related Instances type calculated field named **CF\_Comment\_By\_Employee\_ID**.

        ![](../image/wdhr-job-req-event-rep-1.jpg)

    -   Create Aggregate Related Instances type calculated field named **CF\_Comment\_by\_worker** and use **CF\_Comment\_By\_Employee\_ID** in source field.

        ![](../image/wdhr-job-req-event-rep-2.jpg)

-   Calculated field 2: Create LookUp Related Value type calculated field named CF\_Compensation\_grade.

    ![](../image/wdhr-job-req-event-rep-3.jpg)

-   Calculated field 3:
    -   Create LookUp Related Value type calculated field named **CF\_Number\_of\_opening\_created**.

        ![](../image/wdhr-job-req-event-rep-4.jpg)

    -   Create LookUp Related Value type calculated field named CF\_positions\_created and use **CF\_Number\_of\_opening\_created** in field section.

        ![](../image/wdhr-job-req-event-rep-5.jpg)

-   Calculated field 4: Create LookUp Related Value type calculated field named **CF\_Attachment\_Proposed**.

    ![](../image/wdhr-job-req-event-rep-6.jpg)


## Procedure

1.  Access the Create Custom Report task.

2.  Provide the report name such as, `RPT_job_Requisition`.

3.  Select report type as **Advanced**.

4.  Clear the **Optimized for performance** option.

5.  Select **Data Source** as **Business Process Transactions**.

6.  Do not select the **Temporary report** option and click **OK**.

    ![](../image/wdhr-job-req-event-rep-7.jpg)

7.  Select the report business object and report fields.

    ![](../image/wdhr-job-req-event-rep-8.jpg)![](../image/wdhr-job-req-event-rep-9.jpg)![](../image/wdhr-job-req-event-rep-10.jpg)

8.  In **Group Column Heading** section, select all business object as below.

    **Group Column Heading** for each business object will be blank.

    ![](../image/wdhr-job-req-event-rep-11.jpg)

9.  In **Filter** section, select the value as given below.

    Ensure to add parenthesis.

    ![](../image/wdhr-job-req-event-rep-12.jpg)

10. In **Prompts** section, select the **Populate Undefined Prompt Defaults** option.

    ![](../image/wdhr-job-req-event-rep-13.jpg)

11. Select the value of prompts as given below under Prompt default section.

    Make sure the **Label For Prompt XML Alias** of all prompt fields must be same.

    ![](../image/wdhr-job-req-event-rep-14.jpg)

12. In **Advanced** section, select **Enable as webservice** option and click **OK**.

13. Click on three dots icon and navigate to **Web Services** &gt; **View URLs** option once report configuration is done.

    ![](../image/wdhr-job-req-event-rep-15.jpg)

14. Select **Business process** as **Job Requisition**, **Transaction Status** as **In Progress**, time range in **Starting Last functionally Updated** and **Ending Last Functionally Updated**, and click **OK**.

    **Note:** This step is one-time process required to get the WID of business process and transaction status. After the initial full load, transaction status ID is not needed as details of all events will be retrieved; **In Progress** as well as **Completed**.

    ![](../image/wdhr-job-req-event-rep-16.jpg)

15. In View URLs Web Service page, click the marked icon under the **CSV** section.

    A new browser tab is opened.

    ![](../image/wdhr-job-req-event-rep-17.jpg)

    The RaaS URL of the report is displayed in new browser tab and you can obtain these details from the link.

    ![](../image/wdhr-job-req-event-rep-18.jpg)

    -   `https://wd2-impl-services1.workday.com` is the base URL of customer’s workday tenant.
    -   **Tenant\_Name** is the customer’s workday tenant.
    -   **Report\_Owner\_user\_name** represents user name of the report’s owner.
    -   **Report\_Name** is the report name.
    -   **Business\_Processes%21WID=\(32 character code\)** is the business process WID and **Transaction\_Status%21WID=\(32 character code\)** is the Transaction WID.
    **Note:** After the initial full load, Transaction Status WID is not used as parameter as all in progress and completed transactions will be retrieved.

    |Usecase|Business process|Workday ID|
    |-------|----------------|----------|
    |Job requisition|Job requisition|956972d0179342df82c26bb0781d9660|

    Workday ID of **In Progress** transaction status is e2d08afc53614c37b32b31270bb8bee3.


