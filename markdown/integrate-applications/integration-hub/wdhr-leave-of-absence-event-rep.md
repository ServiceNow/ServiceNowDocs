---
title: Workday configuration for leave of absence event report
description: Retrieve the Leave of Absence event data based on time duration by creating the leave of absence event report.
locale: en-US
release: zurich
product: Integration Hub
classification: integration-hub
topic_type: task
last_updated: "2025-12-08"
reading_time_minutes: 4
breadcrumb: [Workday HR Spoke, Integration Hub spokes, Build integrations, Integration Hub, Workflow Data Fabric]
---

# Workday configuration for leave of absence event report

Retrieve the Leave of Absence event data based on time duration by creating the leave of absence event report.

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

        ![Configuring calculated field “CF_Comment_By_Employee_ID” for Action Event, showing selection of Comment as source and Comment by Person as aggregate field.](../image/wdhr-leave-of-absence-event-rep-1.png.png)

    -   Create Aggregate Related Instances type calculated field named **CF\_Comment\_by\_worker** and use **CF\_Comment\_By\_Employee\_ID** in source field.

        ![Setting up “CF_Comment_by_worker” calculated field using “CF_Comment_By_Employee_ID” as source and Workers as aggregate field.](../image/wdhr-leave-of-absence-event-rep-2.png.png)

-   Calculated field 2: Create Lookup Related Value type calculated field named **CF\_last\_day\_of\_leave**.

    ![Configuring lookup calculated field “CF_last_day_of_leave” for Leave of Absence Event, selecting Leave Request Event and Last Day of Leave – Estimated.](../image/wdhr-leave-of-absence-event-rep-3.png.png)


## Procedure

1.  Access the Create Custom Report task.

2.  Provide the report name such as, `RPT_leave_of_absence`.

3.  Select report type as **Advanced**.

4.  Clear the **Optimized for performance** option.

5.  Select **Data Source** as **Business Process Transactions**.

6.  Leave the **Temporary report** option unchecked and click **OK**.

    ![Create Custom Report screen with report name, type, data source, and business object fields for leave of absence report setup.](../image/wdhr-leave-of-absence-event-rep-4.png.png)

7.  Select the report business object and report fields.

    ![Columns tab showing selected business objects, fields, column heading overrides, and formats for leave of absence event report.](../image/wdhr-leave-of-absence-event-rep-5.png.png)![Report columns for Attachments, including Attachment Name, Created Moment, Created By, Content Type, and Uploaded By.](../image/wdhr-leave-of-absence-event-rep-6.png.png)

8.  In **Group Column Heading** section, select all business object as below.

    **Group Column Heading** for each business object will be blank. ![Group Column Headings section with business objects and blank group column headings for the report.](../image/wdhr-leave-of-absence-event-rep-7.png.png)

9.  In **Filter** section, select the value as given below.

    Ensure to add parenthesis. ![Filter section for report instances, showing parenthesis and filter conditions for Leave Functionality Updated On.](../image/wdhr-leave-of-absence-event-rep-8.png.png)

10. In **Prompts** section, select the **Populate Undefined Prompt Defaults** option.

    ![Prompts section with “populate undefined prompt defaults” checkbox and runtime date prompts for effective date and time zone.](../image/wdhr-leave-of-absence-event-rep-9.png.png)

11. Select the value of prompts as given below under Prompt default section.

    Make sure the **Label For Prompt XML Alias** of all prompt fields must be same.

    ![Prompt Defaults section listing prompt qualifiers, XML aliases, default types, default values, and required status for each prompt field.](../image/wdhr-leave-of-absence-event-rep-10.png.png)

12. In **Advanced** section, select **Enable as webservice** option and click **OK**.

13. Click on three dots icon and navigate to **Web Services** &gt; **View URLs** option once report configuration is done.

    ![Advanced section with “enable as webservice” checkbox selected and View URLs option highlighted for report web service URLs.](../image/wdhr-leave-of-absence-event-rep-11.png.png)

14. Select **Business process** as **Request leave of absence**, **Transaction Status** as **In Progress**, time range in **Start Date** and **End Date**, and click **OK**.

    **Note:** This step is one-time process required to get the WID of business process and transaction status. After the initial full load, transaction status ID is not needed as details of all events will be retrieved; **In Progress** as well as **Completed**.

    ![View URLs Web Service page showing fields for business process, transaction status, and date parameters for generating report URL.](../image/wdhr-leave-of-absence-event-rep-12.png.png)

15. In View URLs Web Service page, click the marked icon under the **CSV** section.

    A new browser tab is opened.

    ![CSV section in View URLs Web Service page, highlighting CSV link for exporting report data.](../image/wdhr-leave-of-absence-event-rep-13.png.png)

    The RaaS URL of the report is displayed in new browser tab and you can obtain these details from the link.

    ![Browser tab with generated RaaS URL for leave of absence event report, showing Workday tenant base URL and report parameters.](../image/wdhr-leave-of-absence-event-rep-14.png.png)

    -   `https://wd2-impl-services1.workday.com` is the base URL of customer's workday tenant.
    -   **Tenant\_Name** is the customer's workday tenant.
    -   **Report\_Owner\_user\_name** represents user name of the report's owner.
    -   **Report\_Name** is the report name.
    -   **Business\_Processes%21WID=\(32 character code\)** is the business process WID and **Transaction\_Status%21WID=\(32 character code\)** is the Transaction WID.
    **Note:** After the initial full load, Transaction Status WID is not used as parameter as all in progress and completed transactions will be retrieved.

    |Usecase|Business process|Workday ID|
    |-------|----------------|----------|
    |Leave of absence|Request leave of absence|cd0c14d6446c11de98360015c5e6daf6|

    Workday ID of **In Progress** transaction status is e2d08afc53614c37b32b31270bb8bee3.


