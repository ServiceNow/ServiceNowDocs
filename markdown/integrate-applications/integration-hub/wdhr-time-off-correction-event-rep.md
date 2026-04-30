---
title: Workday configuration for time off correction event report
description: Retrieve the Correct Time Off event data based on time duration by creating the time off correction event report.
locale: en-US
release: zurich
product: Integration Hub
classification: integration-hub
topic_type: task
last_updated: "2025-12-08"
reading_time_minutes: 4
breadcrumb: [Workday HR Spoke, Integration Hub spokes, Build integrations, Integration Hub, Workflow Data Fabric]
---

# Workday configuration for time off correction event report

Retrieve the Correct Time Off event data based on time duration by creating the time off correction event report.

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

        ![Aggregate Related Instances calculated field CF_Comment_By_Employee_ID configuration, showing source field, related business object, and fields to aggregate.](../image/wdhr-time-off-correction-event-rep-1.png)

    -   Create Aggregate Related Instances type calculated field named **CF\_Comment\_by\_worker** and use **CF\_Comment\_By\_Employee\_ID** in source field.

        ![Aggregate Related Instances calculated field CF_Comment_by_worker configuration, using CF_Comment_By_Employee_ID as source field.](../image/wdhr-time-off-correction-event-rep-2.png)

-   Calculated field 2: Create Aggregate Related Instances type calculated field named **CF\_Time\_off\_entry**.

    ![Aggregate Related Instances calculated field CF_Time_off_entry configuration, showing source field, related business object, and fields to aggregate.](../image/wdhr-time-off-correction-event-rep-3.png)


## Procedure

1.  Access the Create Custom Report task.

2.  Provide the report name such as, `RPT_time_off_correction_event`.

3.  Select report type as **Advanced**.

4.  Clear the **Optimized for performance** option.

5.  Select **Data Source** as **Business Process Transactions**.

6.  Leave the **Temporary report** option unchecked and click **OK**.

    ![Create Custom Report dialog showing report name RPT_time_off_correction_event, report type Advanced, data source Business Process Transactions, and temporary report option.](../image/wdhr-time-off-correction-event-rep-4.png)

7.  Select the report business object and report fields.

    ![Columns tab showing report business object and report fields selection for time off correction event report.](../image/wdhr-spend-auth-rep-6.png)![Columns tab continued, showing additional report fields for time off correction event report.](../image/wdhr-spend-auth-rep-7.png)

8.  In **Group Column Heading** section, select all business object as below.

    **Group Column Heading** for each business object will be blank. ![Group Column Headings section listing business objects with blank group column headings and XML aliases.](../image/wdhr-time-off-correction-event-rep-8.png)

9.  In **Filter** section, select the value as given below.

    Ensure to add parenthesis. ![Filter tab showing conditions for Last Functionally Updated field, using starting and ending prompts for comparison values.](../image/wdhr-time-off-correction-event-rep-9.png)

10. In **Prompts** section, select the **Populate Undefined Prompt Defaults** option.

    ![Prompts section showing Populate Undefined Prompt Defaults checkbox selected.](../image/wdhr-time-off-correction-event-rep-10.png)

11. Select the value of prompts as given below under Prompt default section.

    Make sure the **Label For Prompt XML Alias** of all prompt fields must be same.

    ![Prompt Defaults section showing Business Processes, Transaction Status, and date prompt fields with Label For Prompt XML Alias values.](../image/wdhr-time-off-correction-event-rep-11.png)![Prompt Defaults section continued, showing Last Functionally Updated prompt fields configuration.](../image/wdhr-time-off-correction-event-rep-12.png)

12. In **Advanced** section, select **Enable as webservice** option and click **OK**.

13. Click on three dots icon and navigate to **Web Services** &gt; **View URLs** option once report configuration is done.

    ![View Custom Report screen for “RPT_time_off_correction_event” showing Actions menu open and “View URLs” option highlighted for accessing report web service URLs.](../image/wdhr-time-off-correction-event-rep-13.png)

14. Select **Business process** as **Correct Time Off**, **Transaction Status** as **In Progress**, time range in **Start Date** and **End Date**, and click **OK**.

    **Note:** This step is one-time process required to get the WID of business process and transaction status. After the initial full load, transaction status ID is not needed as details of all events will be retrieved; **In Progress** as well as **Completed**.

    ![Report prompt dialog showing Business process set to Correct Time Off, Transaction Status set to In Progress, and date range parameters.](../image/wdhr-time-off-correction-event-rep-14.png)![Report prompt dialog continued, showing Start Date and End Date parameters with OK and Cancel buttons.](../image/wdhr-time-off-correction-event-rep-15.png)

15. In View URLs Web Service page, click the marked icon under the **CSV** section.

    A new browser tab is opened.

    ![View URLs Web Service page showing JSON, CSV, GData, and simplexml output format options with CSV section highlighted.](../image/wdhr-time-off-correction-event-rep-16.png)

    The RaaS URL of the report is displayed in new browser tab and you can obtain these details from the link.

    ![RaaS URL displayed in browser tab showing the report web service URL with tenant name, report owner, report name, and WID parameters.](../image/wdhr-time-off-correction-event-rep-17.png)

    -   `https://wd2-impl-services1.workday.com` is the base URL of customer's workday tenant.
    -   **Tenant\_Name** is the customer's workday tenant.
    -   **Report\_Owner\_user\_name** represents user name of the report's owner.
    -   **Report\_Name** is the report name.
    -   **Business\_Processes%21WID=\(32 character code\)** is the business process WID and **Transaction\_Status%21WID=\(32 character code\)** is the Transaction WID.
    **Note:** After the initial full load, Transaction Status WID is not used as parameter as all in progress and completed transactions will be retrieved.

    |Usecase|Business process|Workday ID|
    |-------|----------------|----------|
    |Correct time off|Correct Time Off|cd0c42da446c11de98360015c5e6daf6|

    Workday ID of **In Progress** transaction status is e2d08afc53614c37b32b31270bb8bee3.


