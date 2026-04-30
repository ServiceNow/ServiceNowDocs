---
title: Configure Look up inbox items report
description: Configure the report to retrieve workers' inbox items such as to-dos, action items, and approval.
locale: en-US
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

        ![Increment or decrement.](../image/CF-Last-functionally-updated-1.png)

    2.  Create a calculated field of type `Lookup Value – As of Date`, name it `CF_Assigned_to_Worker_Previous`, and use **CF\_Last\_functionally\_updated\_-1** as the reference field.

        ![Lookup value as of date.](../image/cf_assigned_to_worker_previous.png)

2.  Create calculated field 2.

    1.  Create a calculated field of type Text Constant and name it `CF_Text_0`.

        ![Calculated field of type Text Constant.](../image/Cf_text_0.png)

    2.  Create a calculated field of type Text Constant and name it `CF_Text_as_1`.

        ![Calculated field of type Text Constant.](../image/CF_Text_as_1.png)

    3.  Create a calculated field of type **True/False Condition** and name it `CF_Competed_by_Is_Not_Equal_Old_Assignee`.

        ![Calculated field of type True/False Condition.](../image/CF_Competed_by_Is_Not_Equal_Old_Assignee.png)

    4.  Create a calculated field of type **Evaluate Expression** and name it `CF_EE_Completed_by_Admin_Exist_as_Old_Assignee_or_Not`.

        ![Calculated field of type Evaluate Expression.](../image/CF_EE_Completed_by_Admin_Exist.png)

3.  Create calculated field 3.

    1.  Create a calculated field of type Text Constant and name it `CF_Text`.

        ![Calculated field of type Text Constant.](../image/CF_Text.png)

    2.  Create a calculated field of type Lookup Related Value and name it `CF_Action_Event`.

        ![Calculated field of type Lookup Related Value.](../image/CF_Action_Event8.png)

    3.  Create a calculated field of type Concatenate Text and name it `CF_Inbox_Subject`.

        ![Calculated field of type Concatenate Text.](../image/CF_Inbox_Subject9.png)

4.  Create calculated field 4.

    1.  Create a calculated field of type Text Constant and name it `CF_url`.

        ![Calculated field of type Text Constant.](../image/CF_URL10.png)

    2.  Create a calculated field of type Lookup Related Value and name it `CF_business_pro_transaction`.

        ![Calculated field of type Lookup Related Value.](../image/CF_business_pro_transaction11.png)

    3.  Create a calculated field of type Lookup Related Value and name it `CF_BP_Wid`.

        ![Calculated field of type Lookup Related Value.](../image/CF_BP_Wid12.png)

    4.  Create Concatenate text type calculated field named `CF_Inbox_url`.

        ![Concatenate text type calculated field.](../image/CF_Inbox_url13.png)

5.  Create calculated field 5.

    1.  Create a calculated field of type Lookup Related Value and name it `cf_step_id`.

        ![Calculated field of type Lookup Related Value.](../image/cf_step_id14.png)

    2.  Create a calculated field of type Lookup Related Value and name it `CF_subject_id`.

        ![Calculated field of type Lookup Related Value.](../image/CF_subject_id15.png)

    3.  Create a calculated field of type Lookup Related Value and name it `CF_subject_and_step_id`.

        ![Calculated field of type Lookup Related Value.](../image/CF_subject_and_step_id16.png)

6.  Create calculated field 6.

    1.  Create a calculated field of type Lookup Related Value and name it `CF_sent_back`.

        ![Calculated field of type Lookup Related Value.](../image/CF_sent_back17.png)

7.  Create calculated field 7.

    1.  Create a calculated field of type Lookup Related Value and name it `CF_Business Process Definition on Action Event`.

        ![Calculated field of type Lookup Related Value.](../image/CF_Business-Process-Definition-on-Action-Event18.png)

    2.  Create a calculated field of type Lookup Related Value, name it `Cf_parent_business_process_definition`, and use **CF\_Business Process Definition on Action Event** as the reference field.

        ![Calculated field of type Lookup Related Value.](../image/Cf_parent_business_process_definition19.png)

8.  Create calculated field 8.

    1.  Create a calculated field of type Increment/Decrement and name it `CF_Last_updated_on-1`.

        ![Calculated field of type Increment/Decrement.](../image/CF_Last_updated_on-1-20.png)

    2.  Create a calculated field of type Lookup Value – As of Date, name it `cf_status_as_of_moment`, and use **CF\_Last\_updated\_on-1** as the reference field.

        ![Calculated field of type Lookup Value – As of Date.](../image/cf_status_as_of_moment21.png)

9.  Create calculated field 9.

    1.  Create a calculated field of type Lookup Value – As of Date and name it `CF_Action_Event`.

        ![Calculated field of type Lookup Value – As of Date.](../image/CF_Action_Event22.png)

10. Create calculated field 10.

    1.  Create a calculated field of type Lookup Value – As of Date, name it `CF_worker`, and use **CF\_Action\_Event** as the lookup field.

        ![Calculated field of type Lookup Value – As of Date.](../image/CF_worker23.png)

11. Create calculated field 11.

    1.  Create a True/False condition type calculated field named `CF_Awaiting_person_is_ISU`.

        ![True/False condition type calculated field .](../image/CF_Awaiting_person_is_ISU24.png)

12. Create the report.

    1.  Access the **Create Custom Report** task.

    2.  Provide a report name.

        Example of report name: SNIH\_Inbox\_Items.

    3.  Select the report type as **Advanced**.

    4.  Deselect the **Optimized for performance** option.

    5.  Select the data source as **Business Process Event** steps.

    6.  Leave the **Temporary Report** box unchecked, then click **OK**.

        ![Custom Report.](../image/SNIH_Inbox_Items25.png)

    7.  Select the report business object and report fields as given below.

        ![Report Business Object.](../image/report-business-object26.png)

        ![Report Business Object.](../image/report-business-object27.png)

    8.  In the Group column heading section, select all business object as below.

        Group Column heading for each business object must be empty.

        ![Report Business Object.](../image/report-business-object28.png)

    9.  In the **Filter** section, select the value as shown below.

        Add parenthesis as given in the screenshots below.

        ![Report Business Object.](../image/report-business-object29.png)

        ![Report Business Object.](../image/report-business-object30.png)

        ![Report Business Object.](../image/report-business-object31.png)

        ![Report Business Object.](../image/report-business-object32.png)

    10. In the Prompt section, select **Populate Undefined Prompt Defaults**.

        ![Report Business Object.](../image/report-business-object33.png)

    11. Select the value of prompts as given below under the Prompt default section.

        Confirm that the Label For Prompt XML Alias of all prompt fields must be same as the image provided below.

        ![Report Business Object.](../image/report-business-object34.png)

    12. In the advanced section, select **Enable as Webservice**, and select **OK**.

    13. Select the three dots icon and then go to **Web Services&gt;View URLs**.

        ![Report Business Object.](../image/report-business-object35.png)

    14. Select a time range from the parameters and select **OK**.

        ![Report Business Object.](../image/report-business-object36.png)

    15. In the **View URLs Web Service** page, select the marked icon under CSV section.

        A new browser tab opens.

        ![Report Business Object.](../image/report-business-object37.png)

        The RaaS URL of the report opens in a new browser tab.

        ![RaaS URL report URL.](../image/report-business-object38.png)

        https://wd2-impl-services1.workday.com represents the Base URL of customer’s workday tenant.

        Tenant\_Name represents customer’s workday tenant.

        Report\_Owner\_user\_name represents user name of the report’s owner.

        Report\_Owner\_user\_name represents user name of the report’s owner.


