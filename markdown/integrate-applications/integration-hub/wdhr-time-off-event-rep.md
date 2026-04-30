---
title: Workday configuration for time off event report
description: Retrieve the Request Time Off event data based on time duration by creating the time off event report.
locale: en-US
release: zurich
product: Integration Hub
classification: integration-hub
topic_type: task
last_updated: "2025-12-08"
reading_time_minutes: 4
breadcrumb: [Workday HR Spoke, Integration Hub spokes, Build integrations, Integration Hub, Workflow Data Fabric]
---

# Workday configuration for time off event report

Retrieve the Request Time Off event data based on time duration by creating the time off event report.

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

        ![Calculated field configuration for CF_Comment_By_Employee_ID showing aggregate related instances with Comments source field and Comment by Person aggregation.](../image/wdhr-time-off-event-rep-1.png)

    -   Create Aggregate Related Instances type calculated field named **CF\_Comment\_by\_worker** and use **CF\_Comment\_By\_Employee\_ID** in source field.

        ![Calculated field configuration for CF_Comment_by_worker showing aggregate related instances with Person business object and Workers aggregation field.](../image/wdhr-time-off-event-rep-2.png)

-   Calculated field 2: Create Aggregate Related Instances type calculated field named **CF\_Time\_off\_entry**.

    ![Calculated field configuration for CF_Time_off_entry showing aggregate related instances with Time Off Event source and Time Off Entry aggregation.](../image/wdhr-time-off-event-rep-3.png)

-   Calculated field 3: Create Aggregate Related Instances type calculated field named **CF\_Time Off Plan for Absence Component**.

    ![Calculated field configuration for CF_Time Off Plan for Absence Component with Time Off business object and aggregation settings.](../image/wdhr-time-off-event-rep-4.png)

-   Calculated field 4: Create Aggregate Related Instances type calculated field named **CF\_time\_off\_plan**.

    ![Calculated field configuration for CF_time_off_plan showing Time Off Event source field with CF_Time Off Plan for Absence Component aggregation.](../image/wdhr-time-off-event-rep-5.png)


## Procedure

1.  Access the Create Custom Report task.

2.  Provide the report name such as, `RPT_time_off_event_report`.

3.  Select report type as **Advanced**.

4.  Clear the **Optimized for performance** option.

5.  Select **Data Source** as **Business Process Transactions**.

6.  Leave the **Temporary report** option unchecked and click **OK**.

    ![View Custom Report page displaying RPT_time_off_event_report configuration with Advanced report type and Business Process Transactions data source.](../image/wdhr-time-off-event-rep-6.png)

7.  Select the report business object and report fields.

    ![Report Columns tab showing 25 fields including Time Off Event, Action Event, Workday ID, Effective Date, and Comment fields with XML aliases.](../image/wdhr-time-off-event-rep-7.png)![Report Columns tab continuation displaying Comments, CF_Time_off_entry, and Attachments business objects with corresponding fields and XML aliases.](../image/wdhr-time-off-event-rep-8.png)

8.  In **Group Column Heading** section, select all business object as below.

    **Group Column Heading** for each business object will be blank.

    ![Group Column Headings configuration showing 6 items mapping business objects to XML aliases for Attachments, Comments, and Time Off data.](../image/wdhr-time-off-event-rep-9.png)

9.  In **Filter** section, select the value as given below.

    Ensure to add parenthesis.

    ![Filter tab showing Filter on Instances with Last Functionally Updated field conditions for Starting Prompt and Ending Prompt date filtering.](../image/wdhr-time-off-event-rep-10.png)

10. In **Prompts** section, select the **Populate Undefined Prompt Defaults** option.

    ![Prompts tab displaying Runtime Date Prompts configuration with Effective Date and Entry Date set to use date and time at runtime.](../image/wdhr-time-off-event-rep-11.png)

11. Select the value of prompts as given below under Prompt default section.

    Make sure the **Label For Prompt XML Alias** of all prompt fields must be same.

    ![Prompt Defaults table showing 10 fields including Business Processes, Transaction Status, and date filters with XML aliases and default values.](../image/wdhr-time-off-event-rep-12.png)

12. In **Advanced** section, select **Enable as webservice** option and click **OK**.

13. Click on three dots icon and navigate to **Web Services** &gt; **View URLs** option once report configuration is done.

    ![View Custom Report page with Web Service menu expanded showing View URLs option and report configuration details.](../image/wdhr-time-off-event-rep-13.png)

14. Select **Business process** as **Request Time Off**, **Transaction Status** as **In Progress**, time range in **Start Date** and **End Date**, and click **OK**.

    **Note:** This step is one-time process required to get the WID of business process and transaction status. After the initial full load, transaction status ID is not needed as details of all events will be retrieved; **In Progress** as well as **Completed**.

    ![View URLs Web Service dialog displaying filter parameters including Business Processes, date fields, and transaction status with date picker inputs.](../image/wdhr-time-off-event-rep-14.png)

15. In View URLs Web Service page, click the marked icon under the **CSV** section.

    A new browser tab is opened.

    ![Web service output format options showing Workday XML, Simple XML, and CSV download links with REST, XSD, and WSDL references.](../image/wdhr-time-off-event-rep-15.png)

    The RaaS URL of the report is displayed in new browser tab and you can obtain these details from the link.

    ![Browser address bar showing Workday custom report web service URL for RPT_time_off_event_report with Business_Processes parameter.](../image/wdhr-time-off-event-rep-16.png)

    -   `https://wd2-impl-services1.workday.com` is the base URL of customer's workday tenant.
    -   **Tenant\_Name** is the customer's workday tenant.
    -   **Report\_Owner\_user\_name** represents user name of the report's owner.
    -   **Report\_Name** is the report name.
    -   **Business\_Processes%21WID=\(32 character code\)** is the business process WID and **Transaction\_Status%21WID=\(32 character code\)** is the Transaction WID.
    **Note:** After the initial full load, Transaction Status WID is not used as parameter as all in progress and completed transactions will be retrieved.

    |Usecase|Business process|Workday ID|
    |-------|----------------|----------|
    |Time off|Request Time Off|cd0c4190446c11de98360015c5e6daf6|

    Workday ID of **In Progress** transaction status is e2d08afc53614c37b32b31270bb8bee3.


