---
title: Workday configuration for termination event report
description: Retrieve the Termination event data based on time duration by creating the termination event report.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/zurich/integrate-applications/integration-hub/wdhr-termination-event-rep.html
release: zurich
product: Integration Hub
classification: integration-hub
topic_type: task
last_updated: "2025-12-08"
reading_time_minutes: 4
breadcrumb: [Workday HR Spoke, Integration Hub spokes, Build integrations, Integration Hub, Workflow Data Fabric]
---

# Workday configuration for termination event report

Retrieve the Termination event data based on time duration by creating the termination event report.

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

        \[Omitted image "wdhr-termination-event-rep-1.png"\] Alt text: Configuring “CF\_Comment\_By\_Employee\_ID” calculated field for Action Event, showing Comment as source and Comment by Person as aggregate field.

    -   Create Aggregate Related Instances type calculated field named **CF\_Comment\_by\_worker** and use **CF\_Comment\_By\_Employee\_ID** in source field.

        \[Omitted image "wdhr-termination-event-rep-2.png"\] Alt text: Setting up “CF\_Comment\_by\_worker” calculated field using “CF\_Comment\_By\_Employee\_ID” as source and Workers as aggregate field.

-   Calculated field 2:
    -   Create LookUp Related Value type calculated field named **CF\_Termination reason**.

        \[Omitted image "wdhr-termination-event-rep-3.png"\] Alt text: Configuring lookup calculated field “CF\_Termination reason” for Action Event, selecting Termination Event and Primary Termination Reason.

    -   Create LookUp Related Value type calculated field named **CF\_primary term reason** and use above mentioned calculated field as Lookup field.

        \[Omitted image "wdhr-termination-event-rep-4.png"\] Alt text: Setting up “CF\_primary term reason” calculated field using “CF\_Termination reason” as lookup field and Termination Reason as return value.

-   Calculated field 3: Create LookUp Related Value type calculated field named **CF\_Position**.

    \[Omitted image "wdhr-termination-event-rep-5.png"\] Alt text: Configuring lookup calculated field “CF\_Position” for Termination Event, selecting Worker and Position as return value.

-   Calculated field 4: Create Aggregate Related Instances type calculated field named **CF\_Position**.

    \[Omitted image "wdhr-termination-event-rep-6.png"\] Alt text: Setting up aggregate calculated field “CF\_Position” for Action Event, using Worker as source and Position as aggregate field.

-   Calculated field 5: Create Substring text type calculated field named **CF\_resignation\_primary\_term\_reason**.

    \[Omitted image "wdhr-termination-event-rep-7.png"\] Alt text: Configuring substring text calculated field “CF\_resignation\_primary\_term\_reason” for Resignation Event, using Business Process Reason as text field.


## Procedure

1.  Access the Create Custom Report task.

2.  Provide the report name such as, `RPT_termination_report`.

3.  Select report type as **Advanced**.

4.  Clear the **Optimized for performance** option.

5.  Select **Data Source** as **Business Process Transactions**.

6.  Leave the **Temporary report** option unchecked and click **OK**.

    \[Omitted image "wdhr-termination-event-rep-8.png"\] Alt text: Create Custom Report screen with report name, type, data source, and business object fields for termination event report setup.

7.  Select the report business object and report fields.

    \[Omitted image "wdhr-termination-event-rep-9.png"\] Alt text: Columns tab showing selected business objects, fields, column heading overrides, and formats for termination event report.\[Omitted image "wdhr-termination-event-rep-10.png"\] Alt text: Additional report columns for Termination Event, including last day of work, resignation, position, and comments.\[Omitted image "wdhr-termination-event-rep-11.png"\] Alt text: Report columns for Resignation Event, including notification date, notice period, resignation date, and comments.\[Omitted image "wdhr-termination-event-rep-12.png"\] Alt text: Report columns for Comments and Attachments, including comment fields, employee ID, Workday ID, attachment name, and uploaded by.\[Omitted image "wdhr-termination-event-rep-13.png"\] Alt text: Report columns for Attachments, showing attachment content field.

8.  In **Group Column Heading** section, select all business object as below.

    **Group Column Heading** for each business object will be blank. \[Omitted image "wdhr-termination-event-rep-14.png"\] Alt text: Group Column Headings section with business objects and blank group column headings for the report.

9.  In **Filter** section, select the value as given below.

    Ensure to add parenthesis. \[Omitted image "wdhr-termination-event-rep-15.png"\] Alt text: Filter section for report instances, showing conditions for Last Functionally Updated field with starting and ending prompt values.

10. In **Prompts** section, select the highlighted effective date as **prompt for effective as of date** and select the **Populate Undefined Prompt Defaults** option.

    \[Omitted image "wdhr-termination-event-rep-16.png"\] Alt text: Prompts section with highlighted effective date, “populate undefined prompt defaults” checkbox, and display prompt values in subtitle option.

11. Select the value of prompts as given below under Prompt default section.

    Make sure the **Label For Prompt XML Alias** of all prompt fields must be same.

    \[Omitted image "wdhr-termination-event-rep-17.png"\] Alt text: Prompt Defaults section listing prompt qualifiers, XML aliases, default types, default values, and required status for each prompt field.

12. In **Advanced** section, select **Enable as webservice** option and click **OK**.

13. Click on three dots icon and navigate to **Web Services** &gt; **View URLs** option once report configuration is done.

    \[Omitted image "wdhr-termination-event-rep-18.png"\] Alt text: Advanced section with “enable as webservice” checkbox selected and View URLs option highlighted for report web service URLs.

14. Select **Business process** as **Termination** or **Submit Resignation**, **Transaction Status** as **In Progress**, time range in **Start Date** and **End Date**, and click **OK**.

    **Note:** This step is one-time process required to get the WID of business process and transaction status. After the initial full load, transaction status ID is not needed as details of all events will be retrieved; **In Progress** as well as **Completed**.

    \[Omitted image "wdhr-termination-event-rep-19.png"\] Alt text: View URLs Web Service page showing fields for business process, transaction status, and date parameters for generating report URL.\[Omitted image "wdhr-termination-event-rep-20.png"\] Alt text: View URLs Web Service page showing fields for start date and end date parameters for generating report URL.

15. In View URLs Web Service page, click the marked icon under the **CSV** section.

    A new browser tab is opened.

    \[Omitted image "wdhr-termination-event-rep-21.png"\] Alt text: CSV section in View URLs Web Service page, highlighting CSV link for exporting report data.

    The RaaS URL of the report is displayed in new browser tab and you can obtain these details from the link.

    \[Omitted image "wdhr-termination-event-rep-22.png"\] Alt text: Browser tab with generated RaaS URL for termination event report, showing Workday tenant base URL and report parameters.

    -   `https://wd2-impl-services1.workday.com` is the base URL of customer's workday tenant.
    -   **Tenant\_Name** is the customer's workday tenant.
    -   **Report\_Owner\_user\_name** represents user name of the report's owner.
    -   **Report\_Name** is the report name.
    -   **Business\_Processes%21WID=\(32 character code\)** is the business process WID and **Transaction\_Status%21WID=\(32 character code\)** is the Transaction WID.
    **Note:** After the initial full load, Transaction Status WID is not used as parameter as all in progress and completed transactions will be retrieved.

    |Usecase|Business process|Workday ID|
    |-------|----------------|----------|
    |Termination|Termination|cd09bb46446c11de98360015c5e6daf6|
    |Termination|Submit Resignation|939f15e2eb371000099ebe0876cd932b|

    Workday ID of **In Progress** transaction status is e2d08afc53614c37b32b31270bb8bee3.


