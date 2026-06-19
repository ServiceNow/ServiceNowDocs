---
title: Workday configuration for spend authorization report
description: Retrieve the Spend Authorization event data based on time duration by creating the spend authorization report.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/zurich/integrate-applications/integration-hub/wdhr-spend-auth-rep.html
release: zurich
product: Integration Hub
classification: integration-hub
topic_type: task
last_updated: "2025-12-08"
reading_time_minutes: 3
breadcrumb: [Workday HR Spoke, Integration Hub spokes, Build integrations, Integration Hub, Workflow Data Fabric]
---

# Workday configuration for spend authorization report

Retrieve the Spend Authorization event data based on time duration by creating the spend authorization report.

## Before you begin

Role required: User with access to report creation and the Business Process Transactions and Spend Authorizations data sources.

-   Create all calculated fields for this report before developing the report, so that while creating report all fields are available.
-   While creating the report, ensure that the report name, report field names or column heading override for the respective field \(if given in report document\) is same as it is in report document.

    Report field label should be same as in report doc. Else, the developed action will fail.

-   While creating filter, ensure that you add parenthesis on filter.
-   All reports must be owned by the ISU user which will be used for accessing these actions on the ServiceNow platform.
-   In the **Advanced** section, **Enable as webservice** option should be selected.

Create all calculated fields so that these fields can be used while developing report.

-   Calculated field 1:
    -   Create Aggregate Related Instances type calculated field named **CF\_Comment\_By\_Employee\_ID**.

        \[Omitted image "wdhr-spend-auth-rep-1.png"\] Alt text: Configuring “CF\_Comment\_By\_Employee\_ID” calculated field for Action Event, showing Comment as source and Comment by Person as aggregate field.

    -   Create Aggregate Related Instances type calculated field named **CF\_Comment\_by\_worker** and use **CF\_Comment\_By\_Employee\_ID** in source field.

        \[Omitted image "wdhr-spend-auth-rep-2.png"\] Alt text: Setting up “CF\_Comment\_by\_worker” calculated field using “CF\_Comment\_By\_Employee\_ID” as source and Workers as aggregate field.

-   Calculated field 2: Create Lookup Related Value type calculated field named **CF\_Last\_Functionally\_updated**.

    \[Omitted image "wdhr-spend-auth-rep-3.png"\] Alt text: Configuring lookup calculated field “CF\_Last\_Functionally\_updated” for Spend Authorization, selecting Action Event and Last Functionally Updated as return value.


## Procedure

1.  Access the Create Custom Report task.

2.  Provide the report name such as, `RPT_Spend_Authorization_1`.

3.  Select report type as **Advanced**.

4.  Clear the **Optimized for performance** option.

5.  Select **Data Source** as **Spend Authorizations**.

6.  Select **Data Source Filter** as **Spend Authorizations for Company**.

7.  Leave the **Temporary report** option unchecked and click **OK**.

    \[Omitted image "wdhr-spend-auth-rep-4.png"\] Alt text: Create Custom Report screen with report name, type, data source, and business object fields for spend authorization report setup.

8.  Select the report business object and report fields.

    \[Omitted image "wdhr-spend-auth-rep-5.png"\] Alt text: Columns tab showing selected business objects, fields, column heading overrides, and formats for spend authorization event report.\[Omitted image "wdhr-spend-auth-rep-6.png"\] Alt text: Additional report columns for Spend Authorization Line, including justification, transaction memo, reimbursement type, expense item, quantity, and unit cost.\[Omitted image "wdhr-spend-auth-rep-7.png"\] Alt text: Report columns for Comments and Attachments, including comment fields, employee ID, Workday ID, content type, and uploaded by.\[Omitted image "wdhr-spend-auth-rep-8.png"\] Alt text: Report columns for Attachments for Business Document, showing attachment content field.

9.  In **Group Column Heading** section, select all business object as below.

    **Group Column Heading** for each business object will be blank. \[Omitted image "wdhr-spend-auth-rep-9.png"\] Alt text: Group Column Headings section with business objects and blank group column headings for the report.

10. In **Filter** section, select the value as given below.

    Ensure to add parenthesis. \[Omitted image "wdhr-spend-auth-rep-10.png"\] Alt text: Filter section for report instances, showing conditions for Last Functionally Updated field with starting and ending prompt values.

11. In **Prompts** section, select the **Populate Undefined Prompt Defaults** option.

    \[Omitted image "wdhr-spend-auth-rep-11.png"\] Alt text: Prompts section with instructions, “populate undefined prompt defaults” checkbox, and display prompt values in results option.

12. Select the value of prompts as given below under Prompt default section.

    Make sure the **Label For Prompt XML Alias** of all prompt fields must be same.

    **Note:** Select all companies if you want to see all events instead of any specific company related events.

    \[Omitted image "wdhr-spend-auth-rep-12.png"\] Alt text: Prompt Defaults section listing prompt qualifiers, XML aliases, default types, default values, and required status for each prompt field.

13. In **Advanced** section, select **Enable as webservice** option and click **OK**.

14. Click on three dots icon and navigate to **Web Services** &gt; **View URLs** option once report configuration is done.

    \[Omitted image "wdhr-spend-auth-rep-13.png"\] Alt text: Advanced section with “enable as webservice” checkbox selected and View URLs option highlighted for report web service URLs.

15. Select time range in **Start Date** and **End Date** parameter, and click **OK**.

    \[Omitted image "wdhr-spend-auth-rep-14.png"\] Alt text: View URLs Web Service page showing fields for start date and end date parameters for generating report URL.

16. In View URLs Web Service page, click the marked icon under the **CSV** section.

    A new browser tab is opened.\[Omitted image "wdhr-spend-auth-rep-15.png"\] Alt text: CSV section in View URLs Web Service page, highlighting CSV link for exporting report data.

    The RaaS URL of the report is displayed in new browser tab and you can obtain these details from the link.\[Omitted image "wdhr-spend-auth-rep-16.png"\] Alt text: Browser tab with generated RaaS URL for spend authorization report, showing Workday tenant base URL and report parameters.

    -   `https://wd2-impl-services1.workday.com` is the base URL of customer's workday tenant.
    -   **Tenant\_Name** is the customer's workday tenant.
    -   **Report\_Owner\_user\_name** represents user name of the report's owner.
    -   **Report\_Name** is the report name.

