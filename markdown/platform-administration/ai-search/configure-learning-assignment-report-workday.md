---
title: Configure a Learning assignment custom report in Workday
description: Configure a custom report for Learning assignments in Workday. The Workday external content connector uses this custom report to make content and metadata from your Learning assignment data searchable.
locale: en-US
release: zurich
product: AI Search
classification: ai-search
topic_type: task
last_updated: "2025-10-27"
reading_time_minutes: 13
keywords: [Now Assist, AI Agents, generative AI, agentic AI]
breadcrumb: [Workday external content connector, Configure, External Content Connectors, ServiceNow Store applications and integrations, AI Search, Search administration, Configure core features, Administer]
---

# Configure a Learning assignment custom report in Workday

Configure a custom report for Learning assignments in Workday. The Workday external content connector uses this custom report to make content and metadata from your Learning assignment data searchable.

## Before you begin

A Workday admin must have already an integration system user and an unconstrained integration system security group in your Workday tenant. For details on this preliminary task, see [Configure Workday security settings](configure-workday-security-settings.md).

You need an account with the following privileges in your organization's Workday tenant:

-   Administrator privileges
-   **Custom Report Creation** domain access
-   Access to the **Learning Assignments by Learning Organization** report data source

Role required: none

## About this task

This task is optional. The Workday external content connector can retrieve Learning assignment data from your Workday source system using a custom report that you configure. If you don't want to retrieve Learning assignment data from Workday, you can skip this task.

## Procedure

1.  Log in to your Workday tenant with your administrator credentials.

2.  For each of the calculated fields shown in the following Calculated fields table, perform these steps.

    1.  In the Workday search bar, search for the **Create Calculated Field** task and select it.

    2.  On the Create Calculated Field page, enter the Field Name shown in the entry for the calculated field in the following Calculated fields table.

    3.  Select the Business Object and Function values shown in the entry for the calculated field in the following Calculated fields table.

    4.  Select **OK**.

        Workday takes you to the Calculation tab for the new calculated field.

    5.  On the Calculation tab, enter the calculation setting field values shown in the entry for the calculated field in the following Calculated fields table.

    6.  Select **OK**.

        Workday saves your calculation settings for the new calculated field.

    7.  Select **Done**.

<table id="table_zvq_fx1_zgc"><thead><tr><th>

Field Name

</th><th>

Business Object

</th><th>

Function

</th><th>

Calculation setting field values

</th></tr></thead><tbody><tr><td>

cf\_learning content\_type

</td><td>

Learning Assignments by Learning Organization

</td><td>

Lookup Related Value

</td><td>

-   Lookup Field: Learning Content
-   Related Business Object: Learning Content
-   Return Value: Learning Content Type


</td></tr><tr><td>

CF\_enrollment\_event\_status

</td><td>

Learning Enrollment Event

</td><td>

True/False Condition

</td><td>

-   And/Or: And
-   Field: Status
-   Operator: equal to
-   Comparison Type: Value specified in this filter
-   Comparison Value: Successfully Completed


</td></tr><tr><td>

CF\_enrollment

</td><td>

Learning Enrollment

</td><td>

Lookup Related Value

</td><td>

-   Lookup Field: Learning Enrollment Event
-   Related Business Object: Learning Enrollment Event
-   Return Value: CF\_enrollment\_event\_status


</td></tr><tr><td>

CF\_learning\_enrollment

</td><td>

Learning Assignment

</td><td>

Extract Multi-Instance

</td><td>

-   Source Field: Learning Enrollment
-   Related Business Object: Learning Enrollment
-   Condition: CF\_enrollment


</td></tr><tr><td>

cf\_course\_type\_is\_blended

</td><td>

Learning Assignments by Learning Organization

</td><td>

True/False Condition

</td><td>

-   And/Or: And
-   Field: CF\_Learning\_content\_type
-   Operator: in the selection list
-   Comparison Type: Value specified in this filter
-   Comparison Value: Blended Course


</td></tr><tr><td>

Cf\_learning\_content\_type\_is\_digital\_course

</td><td>

Learning Assignments by Learning Organization

</td><td>

True/False Condition

</td><td>

-   And/Or: And
-   Field: CF\_Learning\_content\_type
-   Operator: in the selection list
-   Comparison Type: Value specified in this filter
-   Comparison Value: Digital Course


</td></tr><tr><td>

Cf\_learning\_content\_type\_is\_course\_offering

</td><td>

Learning Assignments by Learning Organization

</td><td>

True/False Condition

</td><td>

-   And/Or: And
-   Field: CF\_Learning\_content\_type
-   Operator: in the selection list
-   Comparison Type: Value specified in this filter
-   Comparison Value: Course Offering


</td></tr><tr><td>

Cf\_learning\_content\_type\_is\_program

</td><td>

Learning Assignments by Learning Organization

</td><td>

True/False Condition

</td><td>

-   And/Or: And
-   Field: CF\_Learning\_content\_type
-   Operator: in the selection list
-   Comparison Type: Value specified in this filter
-   Comparison Value: Program


</td></tr><tr><td>

Cf\_learning\_content\_type\_is\_lesson

</td><td>

Learning Assignments by Learning Organization

</td><td>

True/False Condition

</td><td>

-   And/Or: And
-   Field: CF\_Learning\_content\_type
-   Operator: in the selection list
-   Comparison Type: Value specified in this filter
-   Comparison Value: Lesson


</td></tr><tr><td>

CF\_blended course

</td><td>

Learning Assignments by Learning Organization

</td><td>

Lookup Related Value

</td><td>

-   Lookup Field: Learning Content
-   Related Business Object: Learning Content
-   Return Value: Blended Course


</td></tr><tr><td>

CF\_blended course

</td><td>

Learning Assignments by Learning Organization

</td><td>

Lookup Related Value

</td><td>

-   Lookup Field: Learning Content
-   Related Business Object: Learning Content
-   Return Value: Blended Course


</td></tr><tr><td>

CF\_blended course id

</td><td>

Learning Assignments by Learning Organization

</td><td>

Lookup Related Value

</td><td>

-   Lookup Field: CF\_blended source
-   Related Business Object: Blended Course
-   Return Value: Reference ID


</td></tr><tr><td>

cf\_digital course

</td><td>

Learning Assignments by Learning Organization

</td><td>

Lookup Related Value

</td><td>

-   Lookup Field: Learning Content
-   Related Business Object: Learning Content
-   Return Value: Digital Course


</td></tr><tr><td>

cf\_digital\_course

</td><td>

Learning Assignments by Learning Organization

</td><td>

Lookup Related Value

</td><td>

-   Lookup Field: cf\_digital course
-   Related Business Object: Enrollable Course Behaviour
-   Return Value: Reference ID


</td></tr><tr><td>

cf\_course\_offering

</td><td>

Learning Assignments by Learning Organization

</td><td>

Lookup Related Value

</td><td>

-   Lookup Field: Learning Content
-   Related Business Object: Learning Content
-   Return Value: Course Offering


</td></tr><tr><td>

cf\_course\_offering\_id

</td><td>

Learning Assignments by Learning Organization

</td><td>

Lookup Related Value

</td><td>

-   Lookup Field: cf\_course\_offering
-   Related Business Object: Course
-   Return Value: Reference ID


</td></tr><tr><td>

CF\_Program

</td><td>

Learning Assignments by Learning Organization

</td><td>

Lookup Related Value

</td><td>

-   Lookup Field: Learning Content
-   Related Business Object: Learning Content
-   Return Value: Learning Program


</td></tr><tr><td>

Cf\_program\_id

</td><td>

Learning Assignments by Learning Organization

</td><td>

Lookup Related Value

</td><td>

-   Lookup Field: CF\_Program
-   Related Business Object: Learning Program
-   Return Value: Reference ID


</td></tr><tr><td>

CF\_lesson

</td><td>

Learning Assignments by Learning Organization

</td><td>

Lookup Related Value

</td><td>

-   Lookup Field: Learning Content
-   Related Business Object: Learning Content
-   Return Value: Learning Lesson


</td></tr><tr><td>

cf\_lesson\_id

</td><td>

Learning Assignments by Learning Organization

</td><td>

Lookup Related Value

</td><td>

-   Lookup Field: CF\_lesson
-   Related Business Object: Learning Lesson
-   Return Value: Reference ID


</td></tr></tbody>
</table>3.  Create a cf\_learning\_content\_id calculated field.

    1.  In the Workday search bar, search for the **Create Calculated Field** task and select it.

    2.  On the Create Calculated Field page, enter `cf_learning_content_id` as the Field Name for the new calculated field.

    3.  Select **Learning Assignments by Learning Organization** as the Business Object for the new calculated field.

    4.  Select **Evaluate Expression** as the Function for the new calculated field.

    5.  Select **OK**.

        Workday takes you to the Calculation tab for the new calculated field.

    6.  On the Calculation tab, enter these calculation field values.

        -   Field Type: Text
        -   Business Object: \(empty\)
        -   Default Value: Empty String
    7.  On the Calculation tab, in the table, add a new row with the specified field values for each entry in the following cf\_learning\_content\_id calculated field conditions table.

        |Condition|Return Value If Condition is True|
        |---------|---------------------------------|
        |cf\_course\_type\_is\_blended|cf\_blended course id|
        |Cf\_learning\_content\_type\_is\_digital\_course|cf\_digital\_course\_id|
        |Cf\_learning\_content\_type\_is\_course\_offering|cf\_course\_offering\_id|
        |Cf\_learning\_content\_type\_is\_program|Cf\_program\_id|
        |Cf\_learning\_content\_type\_is\_lesson|cf\_lesson\_id|

    8.  Select **OK**.

    9.  Select **Done**.

4.  Create a learning assignment report in Workday.

    1.  In the Workday search bar, search for the **Create Custom Report** task and select it.

    2.  On the Create Custom Report page, enter a name for your new custom report.

        As an example, you might enter `Workday connector LA report`.

    3.  In the Report Type field, select **Advanced**.

    4.  Clear the **Optimized for performance** option.

    5.  In the Data Source field, select **Learning Assignments by Learning Organization**.

    6.  Select the **Enable As Web Service** option.

    7.  Select **OK**.

    Workday takes you to the Edit Custom Report page for your new custom report.

5.  On the Edit Custom Report page, on the Columns tab, perform the following steps for each entry in the following Custom report columns table.

    1.  Select **+** to add a new column row.

    2.  In the new row, select or enter the field values shown in the column entry in the table.

        |Business Object|Field|Column Heading Override|Column Heading Override XML Alias|
        |---------------|-----|-----------------------|---------------------------------|
        |Learning Assignments by Learning Organization|Worker| |Worker|
        |Worker|Employee ID| |Employee\_ID|
        |Learning Assignments by Learning Organization|Assigned By| |Assigned\_By|
        |Assigned By|Workday ID|Assigned\_by\_WID|Assigned\_by\_WID|
        |Learning Assignments by Learning Organization|Assigned Date| |Assigned\_Date|
        |Learning Assignments by Learning Organization|Assignment Cancellation Date| |Assignment\_Cancellation\_Date|
        |Learning Assignments by Learning Organization|Assignment Mechanism| |assignmentMechanism|
        |Learning Assignments by Learning Organization|Assignment Record Completion Moment| |Assignment\_Record\_Completion\_Moment|
        |Learning Assignments by Learning Organization|Assignment Status| |Assignment\_Status|
        |Learning Assignments by Learning Organization|Created Moment| |Created\_Moment|
        |Learning Assignments by Learning Organization|Due Date| |Due\_Date|
        |Learning Assignments by Learning Organization|Last Functionally Updated| |Last\_Functionally\_Updated|
        |Learning Assignments by Learning Organization|Latest Assigned| |Latest\_Assigned|
        |Learning Assignments by Learning Organization|Learning Assignment| |Learning\_Assignment|
        |Learning Assignments by Learning Organization|Learning Content| |Learning\_Content|
        |Learning Assignments by Learning Organization|cf\_learning\_content\_id|Learning Content ID|Learning\_Content\_ID|
        |Learning Assignments by Learning Organization|Learning Enrollment| |Learning\_Enrollment|
        |Learning Assignments by Learning Organization|Learning Record| |Learning\_Record|
        |Learning Assignments by Learning Organization|Overdue| |Overdue|
        |Learning Assignments by Learning Organization|Required| |Required|
        |Learning Assignments by Learning Organization|Waived| |Waived|
        |Learning Assignments by Learning Organization|Waived by Worker| |Waived\_by\_Worker|
        |Learning Assignments by Learning Organization|Waive Reason| |Waive\_Reason|
        |Learning Assignments by Learning Organization|Worker's Manager\(s\)| |Worker\_s\_Manager\_s\_|
        |Worker's Manager\(s\)|Employee ID|Manager emp id|Manager\_Employee\_ID|
        |Worker's Manager\(s\)|Workday ID|Manager\_wid|managerworkdayID|

6.  On the Columns tab, in the Group Column Headings section for your new custom report, perform the following steps for each entry in the following Custom report group column headings table.

    1.  Select **+** to add a new column row.

    2.  In the new row, select or enter the field values shown in the group column heading entry in the table.

        |Business Object|Group Column Heading|Group Column Heading XML Alias|
        |---------------|--------------------|------------------------------|
        |Assigned By| |Assigned\_By\_group|
        |Worker| |Worker\_group|
        |Worker's Manager\(s\)| |Worker\_s\_Manager\_s\_\_group|

7.  On the Edit Custom Report page, navigate to the Sort tab, then perform these steps.

    1.  In the table, select **+** to add a new result sort order row for your custom report.

    2.  In the new row, select or enter the field values shown in the following Sort order table.

        |Field|Sort Direction|
        |-----|--------------|
        |Last Functionally Updated|Alphabetical - Ascending|

8.  On the Edit Custom Report page, navigate to the Filter tab, then perform the following steps for each filter condition entry in the following Filter conditions table.

    1.  In the Filter conditions for filtering on instances table, select **+** to add a new sort order row for your custom report.

    2.  In the new row, select or enter the field values shown for the filter condition entry in the table.

<table id="table_bkn_hs1_zgc"><thead><tr><th>

And/Or

</th><th>

\(

</th><th>

Field

</th><th>

Operator

</th><th>

Comparison Type

</th><th>

Comparison Value

</th><th>

\)

</th><th>

Required?

</th></tr></thead><tbody><tr><td>

And

</td><td>

 

</td><td>

Worker

</td><td>

in the selection list

</td><td>

Prompt the user for the value and ignore the filter condition if the value is blank

</td><td>

Default Prompt

</td><td>

 

</td><td>

Yes

</td></tr><tr><td>

And

</td><td>

\(\(

</td><td>

CF\_learning\_enrollment

</td><td>

is not empty

</td><td>

 

</td><td>

 

</td><td>

 

</td><td>

 

</td></tr><tr><td>

And

</td><td>

 

</td><td>

Assignment Mechanism

</td><td>

in the selection list

</td><td>

Value specified in this filter

</td><td>

-   Enroll in Course WS
-   Learning Facilitated Enroll
-   Learning Mass Enroll
-   Manager Enroll
-   Retraining


</td><td>

\)

</td><td>

Yes

</td></tr><tr><td>

Or

</td><td>

 

</td><td>

Assignment Mechanism

</td><td>

in the selection list

</td><td>

Value specified in this filter

</td><td>

Campaign

</td><td>

\)

</td><td>

Yes

</td></tr><tr><td>

And

</td><td>

 

</td><td>

Last Functionally Updated

</td><td>

greater than or equal to

</td><td>

Prompt the user for the value and ignore the filter condition if the value is blank

</td><td>

Starting Prompt

</td><td>

 

</td><td>

 

</td></tr><tr><td>

And

</td><td>

 

</td><td>

Last Functionally Updated

</td><td>

less than or equal to

</td><td>

Prompt the user for the value and ignore the filter condition if the value is blank

</td><td>

Ending Prompt

</td><td>

 

</td><td>

 

</td></tr><tr><td>

And

</td><td>

\(\(

</td><td>

cf\_learning content\_type

</td><td>

in the selection list

</td><td>

Value specified in this filter

</td><td>

-   Blended Course
-   Course Offering
-   Digital Course
-   External Content
-   Imported Content
-   Program


</td><td>

 

</td><td>

 

</td></tr><tr><td>

And

</td><td>

 

</td><td>

Learning Record

</td><td>

is not empty

</td><td>

 

</td><td>

 

</td><td>

\)

</td><td>

Yes

</td></tr><tr><td>

Or

</td><td>

 

</td><td>

cf\_learning content\_type

</td><td>

in the selection list

</td><td>

Value specified in this filter

</td><td>

Lesson

</td><td>

\)

</td><td>

 

</td></tr></tbody>
</table>9.  On the Edit Custom Report page, navigate to the Prompt tab, then select the **Populate Undefined Prompt Defaults** option

10. On the Prompt tab, perform the following steps for each prompt entry in the following Prompts table.

    1.  In the Prompt Defaults table, select **+** to add a new prompt row for your custom report.

    2.  In the new row, select or enter the field values shown for the prompt entry in the table.

        |Field|Prompt Qualifier|Label for Prompt XML Alias|Default Type|Default Value|Required|
        |-----|----------------|--------------------------|------------|-------------|--------|
        |Worker|Default Prompt|Worker|No default value| | |
        |Learning Organizations for Learning Assignment| |Learning\_Organizations\_for\_Learning\_Assignment|No default value| |Yes|
        |Include Subordinate Organizations| |Include\_Subordinate\_Organizations|Specify default value|Yes| |
        |Last Functionally Updated|Starting Prompt|Start\_Assigned\_Date|No default value| | |
        |Last Functionally Updated|Ending Prompt|End\_Assigned\_Date|No default value| | |

11. On the Advanced tab for your new custom report, select the **Enable As Web Service** option if it's not already selected, then select **OK**.

    Workday saves your configuration changes for your new custom report.

12. Transfer ownership of your new custom report to the integration system user created for the Workday external content connector.

    1.  From the View Custom Report page, navigate to **…** &gt; **Custom Report** &gt; **Transfer Ownership**.

    2.  On the Transfer Ownership of Custom Reports page, in the New Owner field, enter or select the **ISU SNOW ACL** integration system user account.

        **Important:** If you don't see this integration system user account in the system, check that a Workday admin has completed the [Configure Workday security settings](configure-workday-security-settings.md) preliminary task.

    3.  Select **OK**.

13. Generate a sample report using your new custom report and copy its CSV URL.

    1.  On the View Custom Report page for your new custom report, navigate to **...** &gt; **Web Service** &gt; **View URLs**.

    2.  On the View URLs Web Service page, configure a sample report by filling in the fields.

        |Field|Value|
        |-----|-----|
        |Worker|Select any member of your Workday organization.|
        |Learning Organizations for Learning Assignment|Select the supervisory organization for the chosen worker.|
        |Starting Last Functionally Updated|Select an arbitrary start date and time for the report.|
        |Ending Last Functionally Updated|Select an arbitrary end date and time for the report. The end date and time must occur after your specified start date and time.|

    3.  Select **OK**.

        Workday displays parameters and URLs for your sample report.

    4.  Long-press \(or right-click\) the **CSV** link and copy the CSV URL.

    5.  Paste the copied URL into a web browser or a text editor.

    The CSV URL has the format `https://<hostname>.workday.com/ccx/service/customreport2/<tenant-name>/<report-owner-user-name>/<report-name-alias>`. This URL may optionally be followed by a question mark and one or more URL parameters separated by ampersands. As an example, your CSV URL might be `https://wd2-impl-services1.workday.com/ccx/service/customreport2/Example/ISU_SNOW_ACL/Workday_connector_LA_report`.

14. Copy the base URL for your Workday tenant, your Workday tenant name, the custom report owner's user name, and the custom report name alias.

    1.  Copy the base URL for your Workday tenant from the pasted CSV URL and store it in a secure location.

        The base URL for your Workday tenant is the `https://<hostname>.workday.com` portion of the CSV URL \(everything before the third slash character\). As an example, if your CSV URL is `https://wd2-impl-services1.workday.com/ccx/service/customreport2/Example/ISU_SNOW_ACL/Workday_connector_LA_report`, the base URL for your Workday tenant is `https://wd2-impl-services1.workday.com`.

        **Important:** Your external content connector admin needs this base URL when configuring the Workday external content connector.

    2.  Copy the tenant name for your Workday tenant from the pasted CSV URL and store it in a secure location.

        The tenant name for your Workday tenant is the `<tenant-name>` portion of the CSV URL \(everything between the sixth and seventh slash characters\). As an example, if your CSV URL is `https://wd2-impl-services1.workday.com/ccx/service/customreport2/Example/ISU_SNOW_ACL/Workday_connector_LA_report`, your Workday tenant name is `Example`.

        **Important:** Your external content connector admin needs this tenant name when configuring the Workday external content connector.

    3.  Copy the report owner's user name for your custom Learning assignment report from the pasted CSV URL and store it in a secure location.

        The report owner's user name for your custom Learning assignment report is the `<report-owner-user-name>` portion of the CSV URL \(everything between the seventh and eighth slash characters\). As an example, if your CSV URL is `https://wd2-impl-services1.workday.com/ccx/service/customreport2/Example/ISU_SNOW_ACL/Workday_connector_LA_report`, your custom Learning assignment report owner's user name is `ISU_SNOW_ACL`.

        **Important:** Your external content connector admin needs this Learning assignment report owner's user name when configuring the Workday external content connector.

    4.  Copy the Learning assignment report name alias for your custom report from the pasted CSV URL and store it in a secure location.

        The report name alias for your custom Learning assignment report is the `<report-name-alias>` portion of the CSV URL \(everything between the eighth slash character and the question mark or the end of the URL\). As an example, if your CSV URL is `https://wd2-impl-services1.workday.com/ccx/service/customreport2/Example/ISU_SNOW_ACL/Workday_connector_LA_report`, your custom Learning assignment report name alias is `Workday_connector_LA_report`.

        **Important:** Your external content connector admin needs this Learning assignment report name alias when configuring the Workday external content connector.


## What to do next

Provide the following items to the connector admin who creates your Workday external content connectors:

-   The base URL for your Workday tenant that you copied in step [14.a](configure-learning-assignment-report-workday.md#copy-base-url-step).
-   The Workday tenant name that you copied in step [14.b](configure-learning-assignment-report-workday.md#copy-tenant-name-step).
-   The custom Learning assignment report owner's user name that you copied in step [14.c](configure-learning-assignment-report-workday.md#copy-report-owner-user-name-step).
-   The custom Learning assignment report's name alias that you copied in step [14.d](configure-learning-assignment-report-workday.md#copy-report-name-alias-step).

Your connector admin needs these items to configure a Workday external content connector to retrieve searchable content and metadata from learning assignments in your Workday source system.

**Parent Topic:**[Workday external content connector](../concept/workday-external-content-connector.md)

