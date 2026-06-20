---
title: Configure Look up inbox items report
description: Configure the report to retrieve workers' inbox items such as to-dos, action items, and approval.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/zurich/integrate-applications/integration-hub/configure-look-up-inbox-item-report.html
release: zurich
product: Integration Hub
classification: integration-hub
topic_type: task
last_updated: "2025-12-04"
reading_time_minutes: 5
breadcrumb: [Workday HR Spoke, Integration Hub spokes, Build integrations, Integration Hub, Workflow Data Fabric]
---

# Configure Look up inbox items report

Configure the report to retrieve workers' inbox items such as to-dos, action items, and approval.

## Before you begin

Role required: You must fulfill the following prerequisites:

-   Access to report creation access
-   Permission to access the "Business process event steps" data source
-   All calculated fields for this report must be created

    **Note:** Calculated field types are increment/decrement, look-up value, text constant, true/false condition, evaluate expression, and concatenate text fields.

-   All calculated field name starts with CF
-   Confirm that all report field names and column headings match exactly with the labels specified in the report document; otherwise, the developed actions will fail.
-   Leave the Group Column Heading field blank for every business object in the Group Column Heading section.
-   When creating filters, ensure you add parentheses exactly as shown in the provided screenshots.
-   To access actions on the ServiceNow platform, all reports must be either shared with or owned by an ISU user.
-   Confirm that in the advanced section, the **Enable as webservice** field is selected.

## Procedure

1.  Create calculated field 1.

    1.  Create a calculated field of type Increment/Decrement and name it `CF_Last_functionally_updated_-1`.

        \[Omitted image "CF-Last-functionally-updated-1.png"\] Alt text: Increment or decrement.

    2.  Create a calculated field of type `Lookup Value – As of Date`, name it `CF_Assigned_to_Worker_Previous`, and use **CF\_Last\_functionally\_updated\_-1** as the reference field.

        \[Omitted image "cf\_assigned\_to\_worker\_previous.png"\] Alt text: Lookup value as of date.

2.  Create calculated field 2.

    1.  Create a calculated field of type Text Constant and name it `CF_Text_0`.

        \[Omitted image "Cf\_text\_0.png"\] Alt text: Calculated field of type Text Constant.

    2.  Create a calculated field of type Text Constant and name it `CF_Text_as_1`.

        \[Omitted image "CF\_Text\_as\_1.png"\] Alt text: Calculated field of type Text Constant.

    3.  Create a calculated field of type **True/False Condition** and name it `CF_Competed_by_Is_Not_Equal_Old_Assignee`.

        \[Omitted image "CF\_Competed\_by\_Is\_Not\_Equal\_Old\_Assignee.png"\] Alt text: Calculated field of type True/False Condition.

    4.  Create a calculated field of type **Evaluate Expression** and name it `CF_EE_Completed_by_Admin_Exist_as_Old_Assignee_or_Not`.

        \[Omitted image "CF\_EE\_Completed\_by\_Admin\_Exist.png"\] Alt text: Calculated field of type Evaluate Expression.

3.  Create calculated field 3.

    1.  Create a calculated field of type Text Constant and name it `CF_Text`.

        \[Omitted image "CF\_Text.png"\] Alt text: Calculated field of type Text Constant.

    2.  Create a calculated field of type Lookup Related Value and name it `CF_Action_Event`.

        \[Omitted image "CF\_Action\_Event8.png"\] Alt text: Calculated field of type Lookup Related Value.

    3.  Create a calculated field of type Concatenate Text and name it `CF_Inbox_Subject`.

        \[Omitted image "CF\_Inbox\_Subject9.png"\] Alt text: Calculated field of type Concatenate Text.

4.  Create calculated field 4.

    1.  Create a calculated field of type Text Constant and name it `CF_url`.

        \[Omitted image "CF\_URL10.png"\] Alt text: Calculated field of type Text Constant.

    2.  Create a calculated field of type Lookup Related Value and name it `CF_business_pro_transaction`.

        \[Omitted image "CF\_business\_pro\_transaction11.png"\] Alt text: Calculated field of type Lookup Related Value.

    3.  Create a calculated field of type Lookup Related Value and name it `CF_BP_Wid`.

        \[Omitted image "CF\_BP\_Wid12.png"\] Alt text: Calculated field of type Lookup Related Value.

    4.  Create Concatenate text type calculated field named `CF_Inbox_url`.

        \[Omitted image "CF\_Inbox\_url13.png"\] Alt text: Concatenate text type calculated field.

5.  Create calculated field 5.

    1.  Create a calculated field of type Lookup Related Value and name it `cf_step_id`.

        \[Omitted image "cf\_step\_id14.png"\] Alt text: Calculated field of type Lookup Related Value.

    2.  Create a calculated field of type Lookup Related Value and name it `CF_subject_id`.

        \[Omitted image "CF\_subject\_id15.png"\] Alt text: Calculated field of type Lookup Related Value.

    3.  Create a calculated field of type Lookup Related Value and name it `CF_subject_and_step_id`.

        \[Omitted image "CF\_subject\_and\_step\_id16.png"\] Alt text: Calculated field of type Lookup Related Value.

6.  Create calculated field 6.

    1.  Create a calculated field of type Lookup Related Value and name it `CF_sent_back`.

        \[Omitted image "CF\_sent\_back17.png"\] Alt text: Calculated field of type Lookup Related Value.

7.  Create calculated field 7.

    1.  Create a calculated field of type Lookup Related Value and name it `CF_Business Process Definition on Action Event`.

        \[Omitted image "CF\_Business-Process-Definition-on-Action-Event18.png"\] Alt text: Calculated field of type Lookup Related Value.

    2.  Create a calculated field of type Lookup Related Value, name it `Cf_parent_business_process_definition`, and use **CF\_Business Process Definition on Action Event** as the reference field.

        \[Omitted image "Cf\_parent\_business\_process\_definition19.png"\] Alt text: Calculated field of type Lookup Related Value.

8.  Create calculated field 8.

    1.  Create a calculated field of type Increment/Decrement and name it `CF_Last_updated_on-1`.

        \[Omitted image "CF\_Last\_updated\_on-1-20.png"\] Alt text: Calculated field of type Increment/Decrement.

    2.  Create a calculated field of type Lookup Value – As of Date, name it `cf_status_as_of_moment`, and use **CF\_Last\_updated\_on-1** as the reference field.

        \[Omitted image "cf\_status\_as\_of\_moment21.png"\] Alt text: Calculated field of type Lookup Value – As of Date.

9.  Create calculated field 9.

    1.  Create a calculated field of type Lookup Value – As of Date and name it `CF_Action_Event`.

        \[Omitted image "CF\_Action\_Event22.png"\] Alt text: Calculated field of type Lookup Value – As of Date.

10. Create calculated field 10.

    1.  Create a calculated field of type Lookup Value – As of Date, name it `CF_worker`, and use **CF\_Action\_Event** as the lookup field.

        \[Omitted image "CF\_worker23.png"\] Alt text: Calculated field of type Lookup Value – As of Date.

11. Create calculated field 11.

    1.  Create a True/False condition type calculated field named `CF_Awaiting_person_is_ISU`.

        \[Omitted image "CF\_Awaiting\_person\_is\_ISU24.png"\] Alt text: True/False condition type calculated field .

12. Create the report.

    1.  Access the **Create Custom Report** task.

    2.  Provide a report name.

        Example of report name: SNIH\_Inbox\_Items.

    3.  Select the report type as **Advanced**.

    4.  Deselect the **Optimized for performance** option.

    5.  Select the data source as **Business Process Event** steps.

    6.  Leave the **Temporary Report** box unchecked, then click **OK**.

        \[Omitted image "SNIH\_Inbox\_Items25.png"\] Alt text: Custom Report.

    7.  Select the report business object and report fields as given below.

        \[Omitted image "report-business-object26.png"\] Alt text: Report Business Object.

        \[Omitted image "report-business-object27.png"\] Alt text: Report Business Object.

    8.  In the Group column heading section, select all business object as below.

        Group Column heading for each business object must be empty.

        \[Omitted image "report-business-object28.png"\] Alt text: Report Business Object.

    9.  In the **Filter** section, select the value as shown below.

        Add parenthesis as given in the screenshots below.

        \[Omitted image "report-business-object29.png"\] Alt text: Report Business Object.

        \[Omitted image "report-business-object30.png"\] Alt text: Report Business Object.

        \[Omitted image "report-business-object31.png"\] Alt text: Report Business Object.

        \[Omitted image "report-business-object32.png"\] Alt text: Report Business Object.

    10. In the Prompt section, select **Populate Undefined Prompt Defaults**.

        \[Omitted image "report-business-object33.png"\] Alt text: Report Business Object.

    11. Select the value of prompts as given below under the Prompt default section.

        Confirm that the Label For Prompt XML Alias of all prompt fields must be same as the image provided below.

        \[Omitted image "report-business-object34.png"\] Alt text: Report Business Object.

    12. In the advanced section, select **Enable as Webservice**, and select **OK**.

    13. Select the three dots icon and then go to **Web Services&gt;View URLs**.

        \[Omitted image "report-business-object35.png"\] Alt text: Report Business Object.

    14. Select a time range from the parameters and select **OK**.

        \[Omitted image "report-business-object36.png"\] Alt text: Report Business Object.

    15. In the **View URLs Web Service** page, select the marked icon under CSV section.

        A new browser tab opens.

        \[Omitted image "report-business-object37.png"\] Alt text: Report Business Object.

        The RaaS URL of the report opens in a new browser tab.

        \[Omitted image "report-business-object38.png"\] Alt text: RaaS URL report URL.

        https://wd2-impl-services1.workday.com represents the Base URL of customer’s workday tenant.

        Tenant\_Name represents customer’s workday tenant.

        Report\_Owner\_user\_name represents user name of the report’s owner.

        Report\_Owner\_user\_name represents user name of the report’s owner.


