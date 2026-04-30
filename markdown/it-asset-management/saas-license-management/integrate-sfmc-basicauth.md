---
title: Integrate Salesforce Marketing Cloud using basic authentication
description: Integrate your ServiceNow instance with Salesforce Marketing Cloud by using basic authentication.Create a user with which you can access the Salesforce Marketing Cloud SOAP API. The SOAP API enables you to retrieve records from your Salesforce Marketing Cloud data extensions and get information about your Salesforce Marketing Cloud users.Create a Contacts Counts report to retrieve and display the total number of billable contacts in your Salesforce Marketing Cloud account.Create a data extension to store your Contacts Counts report data on your Salesforce Marketing Cloud instance.Create an automation to automatically import Contacts Counts report data into your data extension after the report is generated.After you create the Contacts Counts report, data extension, and automation, you can retrieve report data between your scheduled report and automation jobs by running these jobs manually.Create an integration profile by using basic authentication to track software subscriptions and optimize stale licenses for the Salesforce Marketing Cloud service.
locale: en-US
release: xanadu
product: SaaS License Management
classification: saas-license-management
topic_type: concept
last_updated: "2024-08-01"
reading_time_minutes: 26
breadcrumb: [Integrating with Salesforce Marketing Cloud, Integrate with SaaS applications, SaaS License Management, Software Asset Management, IT Asset Management]
---

# Integrate Salesforce Marketing Cloud using basic authentication

Integrate your ServiceNow instance with Salesforce Marketing Cloud by using basic authentication.

**Important:** Minimize security risks and protect information by granting access only to the necessary user or API permissions.

<table id="table_box"><thead><tr><th>

Process

</th><th>

Required user role in the Salesforce Marketing Cloud application

</th><th>

Authentication scopes

</th></tr></thead><tbody><tr><td>

Download subscriptions

</td><td>

-   Email &gt; Admin &gt; API Access &gt; WebService API
-   Administration &gt; Users &gt; View

</td><td>

None

</td></tr><tr><td>

Pull user activity

</td><td>

-   Email &gt; Admin &gt; API Access &gt; WebService API
-   Administration &gt; Users &gt; View

</td><td>

None

</td></tr><tr><td>

Reclaim subscription

</td><td>

-   Email &gt; Admin &gt; API Access &gt; WebService API
-   Administration &gt; Users &gt; View
-   Administration &gt; Users &gt; Update

</td><td>

None

</td></tr><tr><td>

Download consumptions

</td><td>

-   Email &gt; Admin &gt; API Access &gt; WebService API
-   Email &gt; Subscribers &gt; Data Extension &gt; View
-   Email &gt; Subscribers &gt; Data Extension &gt; Manage Data

</td><td>

None

</td></tr></tbody>
</table>## Create a user for accessing the Salesforce Marketing Cloud SOAP API

Create a user with which you can access the Salesforce Marketing Cloud SOAP API. The SOAP API enables you to retrieve records from your Salesforce Marketing Cloud data extensions and get information about your Salesforce Marketing Cloud users.

### Before you begin

Salesforce Marketing Cloud Role required: admin user with privileges to create users and roles

### About this task

**Note:**

To use the web services, navigate to **Setup Home** &gt; **Settings** &gt; **Security** &gt; **Security Settings**. In the Username and Logins section, select the **Enable Username and Password for Web Services** check box.

For accessing user licenses and data extension, the API user must be created within the parent business unit. If the API user is created in a child business unit, it might not have access to the parent business unit's data.

### Procedure

1.  From a web browser, go to your Salesforce Marketing Cloud instance.

2.  Log in using your admin credentials.

3.  On the page header of your instance, select your profile icon and then select **Setup**.

4.  Create a Salesforce Marketing Cloud user.

    1.  Navigate to **Administration** &gt; **Users** &gt; **Users**.

    2.  Select **Create**.

    3.  On the form, fill in the fields.

<table id="table_vdp_vky_s4b"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Name

</td><td>

Name of the user.

</td></tr><tr><td>

Reply Email Address

</td><td>

Email address that you want to send and reply to email messages from. Salesforce Marketing Cloud also sends forgotten password requests to this email address. After you enter an email address, select **Verify** to verify the email address.

</td></tr><tr><td>

Add to From Name Dropdown

</td><td>

Option to send the reply email address through a domain verification process before the email address populates in an email.

</td></tr><tr><td>

Notification Email Address

</td><td>

The email address that you want to send Salesforce Marketing Cloud notifications to.

</td></tr><tr><td>

Username

</td><td>

User name for the user.

</td></tr><tr><td>

External Key

</td><td>

Key that uniquely identifies the user during API calls.

</td></tr><tr><td>

Time Zone

</td><td>

Time zone in which the user is located.

</td></tr><tr><td>

Culture Code

</td><td>

Language that is used on the Salesforce Marketing Cloud user interface for this user.

</td></tr><tr><td>

API User

</td><td>

The option indicating whether the user can access the Salesforce Marketing Cloud SOAP API. Select the check box to enable this option.

</td></tr><tr><td>

Temporary Password

</td><td>

A temporary password with which you can log in for the first time. You’re prompted to change this password on the first login.

</td></tr><tr><td>

Verify Password

</td><td>

Field to verify the temporary password.

</td></tr></tbody>
</table>    4.  Select **Save**.

5.  Create a user role that enables assigned users to access the Salesforce Marketing Cloud SOAP API and also manage users and data extensions.

    1.  Navigate to **Administration** &gt; **Users** &gt; **Roles**.

    2.  Select **Create**.

    3.  On the form, fill in the fields.

        |Field|Description|
        |-----|-----------|
        |Name|Name of the user role.|
        |External Key|Key that uniquely identifies the user role.|
        |Description|Description of the user role.|

    4.  In the Permissions form section, expand the **Email** &gt; **Subscribers** &gt; **Data Extension** permission category and then select the **Allow** check box for the View and Manage Data access permissions.

    5.  Expand the **Email** &gt; **Admin** &gt; **API Access** permission category and then select the **Allow** check box for the WebService API access permission.

    6.  Expand the **Administration** &gt; **Users** permission category and then select the **Allow** check box for the following access permissions:

        -   View
        -   Update
        -   Disable
    7.  Select **Save**.

6.  Assign the user role to your Salesforce Marketing Cloud user.

    1.  Navigate to **Administration** &gt; **Users** &gt; **Users**.

    2.  From the list of available users, select the check box for the user that you created in [step 4](integrate-sfmc-basicauth.md#create-user).

    3.  Select **Manage Roles**.

        The Roles form for the selected user opens.

    4.  In the Roles form section, select **Edit Roles**.

    5.  When the list of available roles appears, select the check box for the user role that you created in [step 5](integrate-sfmc-basicauth.md#create-user-role).

    6.  Select **Save**.


## Create a Contacts Counts report in Salesforce Marketing Cloud

Create a Contacts Counts report to retrieve and display the total number of billable contacts in your Salesforce Marketing Cloud account.

### Before you begin

Salesforce Marketing Cloud Role required: admin

### Procedure

1.  From a web browser, go to your Salesforce Marketing Cloud instance.

2.  Log in using your admin credentials.

3.  On the page header of your instance, select the business unit profile icon and then select the top-level parent business unit so that your Contacts Counts report includes data for both the parent business unit and all corresponding child business units.

4.  From the list of available Salesforce Marketing Cloud applications, select the **Analytics Builder** app icon and then select **Reports**.

    The Reports app overview opens.

5.  In the Report Catalog section, select **View Catalog**.

6.  From the Reports Catalog, search for **Contacts Counts** and then select **Create**.

    The Create Report dialog box opens.

7.  In the dialog box, select the time period that you want to retrieve and display data for from the **Date Range** list.

    The default value is **Last 30 Days**.

    **Tip:** To avoid performance issues during report generation, you should set this value to **Last 7 Days**.

8.  Select **Submit**.

    Your Salesforce Marketing Cloud instance generates the report and displays the results on the Results: Contacts Counts page.

9.  On the Results: Contacts Counts page, select **Save**.

    The Save Report dialog box opens.

10. In the dialog box, fill in the fields.

    |Field|Description|
    |-----|-----------|
    |Report Name|Name of the report.|
    |Report Source|Source of the report. This field is automatically set to **Contacts Counts**.|
    |Description|Description of the report.|

11. Select **Save**.

12. Create a schedule to run the Contacts Counts report automatically.

    1.  On the page header of the Reports app, select the **Overview** tab to return to the Reports app overview.

    2.  From your list of reports, open your newly created Contacts Counts report.

    3.  In the Schedule Options section, select **Edit**.

    4.  In the dialog box, fill in the fields.

<table id="table_jlw_f11_t4b"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td colspan="2">

Schedule Options

</td></tr><tr><td>

Start

</td><td>

The date and time from which you want to start running the report.

</td></tr><tr><td>

Time Zone

</td><td>

Time zone in which the report is being scheduled.

</td></tr><tr><td>

Repeat

</td><td>

Frequency at which you want to run the report. Configure the report to run once every week on Sundays.

</td></tr><tr><td>

End

</td><td>

Date on which you want to stop running the report.

</td></tr><tr><td colspan="2">

Delivery Options

</td></tr><tr><td>

Format

</td><td>

File type and file extension in which you want to receive the report results. Select **Data File \(.csv\)**.

</td></tr><tr><td>

Location

</td><td>

Location in which you want to save or share the report. Set this field to **Save report for FTP** and then fill in the corresponding fields:-   **Report Name**: The file name of the report, excluding the file extension.

If you want to include date and time in the report name, add it in the `Reportname_YYYYMMDD_HHMMSS` format.

**Note:** Take note of this file name for later use.

-   **Unique Option**: Option to create a report record instead of replacing the existing report record in SFTP. Leave this check box unselected.
-   **FTP Location**: Location of your Salesforce Marketing Cloud FTP files. Select **ExactTarget Enhanced FTP** so that the report is saved to your SFTP \(SSH File Transfer Protocol\) Reports folder.

**Note:** You can set up an SFTP user account in Salesforce Marketing Cloud to view the saved files at a specific FTP location. For more information, see [Setting up an SFTP user account in Salesforce Marketing Cloud](setup-user-accnt-sfmc.md#).

</td></tr></tbody>
</table>    5.  Select **Save**.


## Create a data extension for your Contacts Counts report

Create a data extension to store your Contacts Counts report data on your Salesforce Marketing Cloud instance.

### Before you begin

Salesforce Marketing Cloud Role required: admin

### About this task

Data extensions are tables that contain attributes representing your report data. When your ServiceNow instance connects with the Salesforce Marketing Cloud service, it retrieves data from this data extension.

### Procedure

1.  On the page header of your Salesforce Marketing Cloud instance, hover the Salesforce icon to display the list of available Salesforce Marketing Cloud applications.

2.  Select the **Audience Builder** app icon and then select **Contact Builder**.

    The Contact Builder app opens.

3.  Select the **Data Extensions** tab.

4.  In the pop-up dialog box, select **Get started** and then select **Create**.

    The Create New Data Extension dialog box opens.

5.  In the Properties step, fill in the fields.

<table id="table_e24_xb1_t4b"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Creation Method

</td><td>

Method in which you want to create the data extension. Select **Create from New**.

</td></tr><tr><td>

Name

</td><td>

Name of the data extension.

</td></tr><tr><td>

External Key

</td><td>

Optional key that uniquely identifies the data extension. You can enter a key of your choice.

</td></tr><tr><td>

Description

</td><td>

Description of the data extension.

</td></tr><tr><td>

Type

</td><td>

Type of data extension. This field is automatically set to **Standard**.

</td></tr><tr><td>

Location

</td><td>

Location in which you want to store the data extension. This field is automatically set to **Data Extensions**. Select **Change Location** to select a different location.

</td></tr><tr><td>

Is Sendable?

</td><td>

Option to indicate whether the data extension can be sent to your subscribers.

</td></tr></tbody>
</table>6.  Select **Next**.

7.  In the Data Retention Policy step, set the **Retention Setting** field to **Off**.

8.  Select **Next**.

9.  In the Attributes step, add the attributes that you want to include in the data extension.

    Attributes are used to map and import data from a report to a data extension. You must create an attribute for each report column that you want to import data from. Each attribute name must exactly match the corresponding report column name.

    For the Salesforce Marketing Cloud integration, attributes for the following Contacts Counts report columns are required:

<table id="table_dfq_wms_ncc"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Primary Key

</td><td>

Option for the attribute to include a unique identifier for all records in the data extension.This option must be enabled for the **Count\_Date** attribute.

</td></tr><tr><td>

Name

</td><td>

Name of the attribute. This name must exactly match the corresponding report column name.

</td></tr><tr><td>

Data Type

</td><td>

Data type of the attribute.

</td></tr><tr><td>

Required

</td><td>

Option that indicates whether the attribute requires a value for each record in the data extension.

</td></tr><tr><td>

Length

</td><td>

Maximum number of characters allowed in the attribute value.

</td></tr><tr><td>

Default Value

</td><td>

Optional default value for the attribute.For the **Flag** attribute, set the default value to `1`.

 **Note:** Don’t enter a default value for any attributes that are assigned as a primary key.

</td></tr></tbody>
</table>    |Name|Data Type|
    |----|---------|
    |Count\_Date|Text|
    |Total\_Distinct\_Contacts\_Count|Text|
    |Total\_Distinct\_Email\_Addresses1|Text|
    |Total\_Distinct\_Mobile\_Addresses\_Count|Text|
    |Flag|Text|

    **Note:** You can add additional attributes and the name must be the same as the Integration Attributes. For more information, see [Create a Salesforce Marketing Cloud integration profile using basic authentication](integrate-sfmc-basicauth.md#) or [Create a Salesforce Marketing Cloud integration profile using OAuth 2.0](integrate-sfmc-oauth.md#).

    Attributes for all other Contacts Counts report columns are optional. Fill in the fields for each attribute that you want to add.

10. Select **Complete**.

11. In the Data Extension Created dialog box, select **OK**.


## Build an automation to import Contacts Counts report data in your data extension

Create an automation to automatically import Contacts Counts report data into your data extension after the report is generated.

### Before you begin

Salesforce Marketing Cloud Role required: admin

### Procedure

1.  On the page header of your Salesforce Marketing Cloud instance, hover the Salesforce icon to display the list of available Salesforce Marketing Cloud applications.

2.  Select the **Journey Builder** app icon and then select **Automation Studio**.

    The Automation Studio app overview opens.

3.  Select **New Automation**.

    The workflow for the new automation opens.

4.  Create an automation schedule by dragging the **Schedule** icon from the Starting Sources section of the left menu pane to the Starting Source section of the workflow canvas.

5.  Define a schedule for the automation.

    1.  In the Starting Source section of the workflow canvas, select **Configure**.

    2.  In the dialog box, fill in the fields.

<table id="table_px4_mg1_t4b"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Start Date

</td><td>

The date from which you want to start running the automation.

</td></tr><tr><td>

Start Time

</td><td>

The time from which you want to start running the automation.

</td></tr><tr><td>

Time Zone

</td><td>

Time zone in which the automation is being scheduled.

</td></tr><tr><td>

Repeat

</td><td>

The frequency at which you want to run the automation. Configure the automation to run after the Contacts Counts report is generated. Select the same frequency that you had selected while [creating a Contacts Counts report in Salesforce Marketing Cloud.](integrate-sfmc-oauth.md#)

**Tip:** If you configure the automation to run on the same day that the report is generated, select a start time that gives enough time for the report to finish generating. ServiceNow recommends a start time of at least two hours after the report start time.

</td></tr><tr><td>

End

</td><td>

Number of times that the automation can run until the automation schedule ends.If you don’t want the automation schedule to end, set this field to **Never**.

This field doesn't appear only when **None \(run once\)** is selected from **Repeat**.

</td></tr></tbody>
</table>    3.  Select **Done**.

6.  Add a script activity to execute the Server-Side JavaScript for all activities that require it.

    1.  In the Activities section of the left menu pane, drag the **Script** icon into the workflow canvas.

        The script activity becomes the first step of the automation workflow.

    2.  Select **Choose** on the script activity step.

        The Choose Script Activity dialog box opens.

    3.  Select **Create New Script Activity**.

        The Create New Script Activity dialog box opens.

    4.  In the Properties step, fill in the fields.

<table id="table_j2s_3h1_t4b"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Name

</td><td>

Name of the script activity.

</td></tr><tr><td>

External Key

</td><td>

Optional key that uniquely identifies the script activity. You can enter a key of your choice.

</td></tr><tr><td>

Folder Location

</td><td>

The location in which you want to store your scripts. Select **Choose...** to select a different location.This field is automatically set to **Scripts**.

</td></tr><tr><td>

Description

</td><td>

Description of the script activity.

</td></tr></tbody>
</table>    5.  Copy and paste the following Server-Side JavaScript into the Server-Side JavaScript text box:

        ```
        <script runat="server"> 
        var rows = Platform.Function.DeleteData('*<data-extension-name>*',['Flag'],['1']);
        </script>
        
        ```

        The **\*&lt;data-extension-name&gt;\*** must exactly match the file name of the Data Extension that you created in [Create a data extension for your Contacts Counts report](integrate-sfmc-oauth.md#).

    6.  Select **Validate Syntax** to verify that the Server-Side JavaScript syntax is valid.

    7.  Select **Next**.

    8.  In the Summary step, verify that the script activity configuration is correct and then select **Finish**.

7.  Add a data extract activity to copy the Contacts Counts report from the SFTP Reports folder to the SFTP Import folder.

    The Salesforce Marketing Cloud instance uses the SFTP Import folder to locate and import report data into your data extensions. To enable your instance to import data from the Contacts Counts report into the corresponding data extension, you must copy the report to the SFTP Import folder.

    1.  In the Activities section of the left menu pane, drag the **Data Extract** icon into the workflow canvas.

        The data extract activity becomes the second step of the automation workflow.

    2.  Select **Choose** on the data extract activity step.

        The Choose Data Extract Activity dialog box opens.

    3.  Select **Create New Data Extract Activity**.

        The Create New Data Extract Activity dialog box opens.

    4.  In the Properties step, fill in the fields.

<table id="table_ezg_2j1_t4b"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Name

</td><td>

Name of the data extract activity.

</td></tr><tr><td>

External Key

</td><td>

Optional key that uniquely identifies the data extract activity. You can enter a key of your choice.

</td></tr><tr><td>

File Naming Pattern

</td><td>

The file name of the Contacts Counts report that you want to extract data from.This name must exactly match the file name of the Contacts Counts report that you created in [Create a Contacts Counts report in Salesforce Marketing Cloud](integrate-sfmc-basicauth.md#), including the file extension.

</td></tr><tr><td>

Extract Type

</td><td>

Data extract method. Set this field to **Enhanced FTP File Move and Copy**.

</td></tr><tr><td>

Description

</td><td>

Description of the data extract activity.

</td></tr></tbody>
</table>    5.  Select **Next**.

    6.  In the Configuration step, fill in the fields.

        |Field|Description|
        |-----|-----------|
        |Input Folder|Location in which you’ve saved the Contacts Counts report. Enter `\reports\`.|
        |Output Folder|Location that you want to copy the report to. Enter `\Import\`.|
        |Copy To Folder|Option to copy instead of move the report from the input folder to the output folder. This option enables you to keep the report in both locations. Select the check box to enable this option.|

    7.  Select **Next**.

    8.  In the Summary step, verify that the data extract activity configuration is correct and then select **Finish**.

8.  Add an import file activity to import the Contacts Counts report data into the data extension.

    1.  In the Activities section of the left menu pane, drag the **Data Copy or Import** icon into the workflow canvas.

        The Data Copy or Import activity becomes the third step of the automation workflow.

    2.  Select **Choose** on the Data Copy or Import activity step.

        The Choose Data Copy or Import dialog box opens.

    3.  Select **Create New Copy or Import Definition**.

        The Create New Copy or Import Definition dialog box opens.

    4.  In the Activity Info step, fill in the fields.

<table id="table_lqz_tk1_t4b"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Name

</td><td>

Name of the import file activity.

</td></tr><tr><td>

Description

</td><td>

Description of the import file activity.

</td></tr><tr><td>

External Key

</td><td>

Optional key that uniquely identifies the import file activity. You can enter a key of your choice.

</td></tr><tr><td>

Send notification email to

</td><td>

The email address to which you want to send notifications when an import completes.If you specify an email address, a notification email that contains the number of inserted and updated rows is sent to that address on successful import.

**Important:** The notification email contains an `Invalid Field Count` validation error due to the presence of empty lines in the imported CSV file. These empty lines appear automatically when you save the report to FTP. However, they have no impact on the integration.

</td></tr></tbody>
</table>    5.  Select **Next**.

    6.  In the Source step, select **File Location** in the Data Source header and fill in the fields.

<table id="table_r12_zk1_t4b"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

File Location

</td><td>

Location of the Contacts Counts report that you want to import data from. Select **ExactTarget Enhanced FTP**.

</td></tr><tr><td>

File Naming Pattern

</td><td>

The file name of the Contacts Counts report that you want to import data from. If you want to include date and time in the report name, add it in the `Reportname_YYYYMMDD_HHMMSS` format by selecting the **Date variable** and **Time variable** fields.

This name must exactly match the file name of the Contacts Counts report that you created in [Create a Contacts Counts report in Salesforce Marketing Cloud](integrate-sfmc-basicauth.md#), including the file extension.

</td></tr><tr><td>

Date Format

</td><td>

Format in which you want to display the date and time of the report data.

</td></tr><tr><td>

Delimiter

</td><td>

Format in which you want to separate each report record. Select **comma** to separate each record with a comma.If you want to enable the use of double quotes to separate each record, enable the **Respect double quotes \("\) as a text delimiter** option.

</td></tr><tr><td>

Bad Data Behavior

</td><td>

Option to skip rows with bad data. Select the check box to enable this option.

</td></tr></tbody>
</table>    7.  Select **Next**.

    8.  In the Destination step, search for and select the data extension that you created in [Create a data extension for your Contacts Counts report](integrate-sfmc-basicauth.md#).

    9.  Select **Next**.

    10. In the Mapping step, select the options **Add and Update** and **Map by Ordinal** in the Data Action header.

    11. When prompted, enable the **Import file has column headers** option and then map each data extension attribute to the corresponding column number in the Contacts Counts report.

        **Note:** Leave the **Flag** attribute unmapped.

    12. Select **Next**.

    13. In the Review step, verify that the import file activity configuration is correct and then select **Finish**.

9.  Select **Save**.

10. In the dialog box, fill in the fields.

    |Field|Description|
    |-----|-----------|
    |Name|Name of the automation.|
    |Description|Description of the automation.|
    |External Key|Optional key that uniquely identifies the automation.|
    |Location|Location in which you want to save the automation.|

11. Select **Save**.

12. In the Starting Source section of the workflow canvas, select **Active**.

13. In the Activate Schedule Confirmation dialog box, select **Activate** to activate the automation schedule.


## Retrieve Contacts Counts report data manually

After you create the Contacts Counts report, data extension, and automation, you can retrieve report data between your scheduled report and automation jobs by running these jobs manually.

### Before you begin

Salesforce Marketing Cloud Role required: admin

### About this task

Your Salesforce Marketing Cloud instance runs the report and automation jobs automatically based on the schedules that you define. If you want to retrieve Contacts Counts report data before the next scheduled report and automation jobs, you can run these jobs manually.

### Procedure

1.  Run your Contacts Counts report.

    1.  On the page header of your Salesforce Marketing Cloud instance, hover the Salesforce icon to display the list of available Salesforce Marketing Cloud applications.

    2.  Select the **Analytics Builder** app icon and then select **Reports**.

        The Reports app overview opens.

    3.  From your list of reports, select the Contacts Counts report that you created in [Create a Contacts Counts report in Salesforce Marketing Cloud](integrate-sfmc-basicauth.md#).

    4.  Select **Run**.

        Your Salesforce Marketing Cloud instance generates the report and displays the results on the Results: &lt;*report-name*&gt; page.

    5.  On the Results: &lt;*report-name*&gt; page, select the Download Results icon \(![Download icon](../image/download-results-sfmc.png)\).

    6.  In the dialog box, fill in the fields.

        |Field|Description|
        |-----|-----------|
        |Filename|The file name of the report, excluding the file extension.|
        |Report Source|Source of the report. This field is automatically set to **Contacts Counts**.|
        |Format|File type and file extension in which you want to receive the report results. Select **Data File \(.csv\)**.|

    7.  Select **Save**.

    8.  Save the file in your system.

2.  Import the file in your Data Extension.

    1.  On the page header of your Salesforce Marketing Cloud instance, hover the Salesforce icon to display the list of available Salesforce Marketing Cloud applications.

    2.  Select the **Audience Builder** app icon and then select **Contact Builder**.

    3.  Open the recently created Data Extension that you created while [creating a data extension for your Contacts Counts report](integrate-sfmc-oauth.md#).

    4.  Select **Import**.

    5.  In the Import Data Confirmation dialog box, select **Import into Data Extension** and then select **Ok**.

    6.  In the Import into Data Extension step, choose the file that you downloaded in the previous Step 1.

    7.  Select **Delimiter** as **comma**.

    8.  Select **Import Type** as **Add and Update**.

    9.  Select **Import options** as **Skip rows in the import file with bad data**.

    10. Select **Next**.

    11. In the Configure mapping dialog box, select **Map Manually**.

    12. Match the available data extension columns with the imported report columns and leave the Flag column empty.

    13. Select **Next**.

    14. In the Review and create dialog box, enter the email id on which you want notification when import completes and select **Finish**.

    15. In the Run Confirmation dialog box, select **Done**.


### Result

The latest Contacts Counts report data is imported into the data extension.

## Create a Salesforce Marketing Cloud integration profile using basic authentication

Create an integration profile by using basic authentication to track software subscriptions and optimize stale licenses for the Salesforce Marketing Cloud service.

### Before you begin

To create a Salesforce Marketing Cloud integration profile, request the Software Asset Management - SaaS License Management plugin \(sn\_sam\_saas\_int\) from the [ServiceNow Store](https://store.servicenow.com/).

**Tip:** To avoid incurring additional subscription costs, install the plugin and build the integration on a non-production instance.

ServiceNow Role required: sam\_integrator or admin

### About this task

If you’re using Software Asset Workspace, the option to create the Salesforce Marketing Cloud integration profile in Core UI is inactive.

### Procedure

1.  Navigate to the integration profile.

<table id="choicetable_o3p_z3k_qtb"><thead><tr><th align="left" id="d289671e3308">

Interface

</th><th align="left" id="d289671e3311">

Action

</th></tr></thead><tbody><tr><td id="d289671e3317">

**Core UI**

</td><td>

1.  Navigate to **All** &gt; **Software Asset** &gt; **SaaS License** &gt; **Direct Integration Profiles**.
2.  Select **New**.
3.  Select **Salesforce Marketing Cloud Integration Profile**.


</td></tr><tr><td id="d289671e3359">

**Software Asset Workspace**

</td><td>

1.  Navigate to **License operations** &gt; **User Subscriptions** &gt; **Direct integration profiles**.
2.  Select **New**.
3.  Select **Salesforce Marketing Cloud** from the drop-down list.
4.  Select **Continue**.


</td></tr></tbody>
</table>2.  On the form, fill in the fields.

<table id="table_gnm_whv_5fb"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr id="row_ksq_rt5_bgb"><td id="display-name">

Display name

</td><td id="display-name-def">

Name of the integration profile. For example, `Salesforce Marketing Cloud integration profile`.

</td></tr><tr><td>

Authentication type

</td><td>

Type of authentication to access Salesforce Marketing Cloud APIs.-   Basic Auth: Select this value.
-   OAuth 2.0
**Note:** For a new Salesforce Marketing Cloud profile, the authentication type is set to **Basic Auth** by default.

</td></tr><tr><td>

Connection &amp; Credential

</td><td>

Connection and credential alias for Salesforce Marketing Cloud. This field is automatically set to **sn\_sforce\_mc\_spoke.SalesforceMarketingCloud**.

</td></tr><tr><td>

Status

</td><td>

Status of the integration profile. If you have not published the integration profile, this field is automatically set to **Draft**. If you have already published the integration profile, this field is automatically set to **Published**.

</td></tr><tr id="row_nn5_st5_bgb"><td id="profile-type">

Profile type

</td><td id="profile-type-def">

Type of integration profile. This value is automatically set to **Salesforce Marketing Cloud Subscription**.

</td></tr><tr class="sub-head"><td>

Download Subscription Subflow

</td><td>

 

</td></tr><tr><td>

Subflow

</td><td>

This field is automatically set to **Salesforce Marketing Cloud Download Subscriptions**.You can view events performed by individual users up to one year prior to the current date. For more information, see [Review a software reclamation rule](../task/add-reclamation-rule-sub.md).

**Note:** Software Asset Management pulls the events from the time that you start downloading user subscriptions irrespective of the profile creation date.

</td></tr><tr class="sub-head"><td>

Reclaim Subscription Subflow

</td><td>

 

</td></tr><tr><td>

Subflow

</td><td>

This field is automatically set to **Salesforce Marketing Cloud Reclaim Subscription**.

</td></tr><tr class="sub-head"><td>

Download Consumption Subflow

</td><td>

 

</td></tr><tr><td>

Subflow

</td><td>

This field is automatically set to **Salesforce Marketing Cloud Download Contacts Consumption**.

</td></tr><tr class="sub-head"><td>

Integration Attributes

</td><td>

 

</td></tr><tr><td>

Attributes

</td><td>

The name-value attributes such as Count Date, Contacts, Email Contacts, and Mobile Contacts are automatically populated for the integration profile.You can add or remove the attributes based on your requirements.

**Note:** The attribute name must match the report column header in Salesforce Marketing Cloud instance. For more information, see [Create a data extension for your Contacts Counts report](integrate-sfmc-basicauth.md#).

</td></tr></tbody>
</table>3.  Select **Save**.

    Your ServiceNow instance creates a draft integration profile. The integration profile uses the Salesforce Marketing Cloud Download Subscriptions, Salesforce Marketing Cloud Reclaim Subscription, and Salesforce Marketing Cloud Download Contacts Consumption subflows to retrieve user data from your Salesforce Marketing Cloud services.

4.  Open the connection &amp; credential aliases record by selecting the preview icon \(![Preview icon.](../image/preview-icon.png)\) next to the **Connection &amp; Credential** field and then selecting **Open Record** in the record preview.

5.  On the Connection &amp; Credential Aliases form, select the **Create New Connection &amp; Credential** related link.

6.  In the dialog box, fill in the fields.

    |Field|Description|
    |-----|-----------|
    |Please Enter the Connection Information|
    |Connection Name|Name of the connection.|
    |SOAP Connection URL|URL of your SOAP Connection endpoint. Enter `https://<*subdomain*>.soap.marketingcloudapis.com/Service.asmx`, where &lt;*subdomain*&gt; is your Salesforce Marketing Cloud subdomain.|
    |Please Enter the Credential Information|
    |Username Profile Name|Name of your credentials.|
    |Username|Username of the user that you can access the Salesforce Marketing Cloud SOAP API with. Enter the user name of the user that you created in [Create a user for accessing the Salesforce Marketing Cloud SOAP API](integrate-sfmc-basicauth.md#).|
    |Password|Password of the user that you can access the Salesforce Marketing Cloud SOAP API with. Enter the password of the user that you created in [Create a user for accessing the Salesforce Marketing Cloud SOAP API](integrate-sfmc-basicauth.md#).|
    |Please enter additional information used for post processing|
    |Contacts Counts Data Extension|Name of the data extension that you want to retrieve Contacts Counts report data from. This name must exactly match the name of the data extension that you created in [Create a data extension for your Contacts Counts report](integrate-sfmc-basicauth.md#).|

7.  Select **Create**.

    The dialog box closes.

8.  On the Connection &amp; Credential Aliases form header, select the Back button to return to the Integration Profile form.

9.  Select **Publish**.

10. In the Publish Confirmation dialog box, select **OK**.


### What to do next

After the integration connects, your ServiceNow instance automatically creates software models, reclamation rules, and software subscriptions that are refreshed daily.

If you want to set up multiple integration profiles with unique connections, create child aliases to manage different configurations and settings for each integration profile. For more information, see [Create a child alias to set up multiple integration profiles](../task/create-child-alias-saas.md).

Review all automatically generated reclamation rules to reclaim user subscriptions. For more information, see [Review a software reclamation rule](../task/add-reclamation-rule-sub.md).

Create software entitlements for the automatically generated software models to track used software against owned software.

-   For more information on creating software entitlements in the Software Asset Management Core UI, see [Create entitlements in Software Asset Management classic](../task/track-software-rights.md).
-   For more information on creating software entitlements in the Software Asset Workspace, see [Create entitlements in workspace](../task/create-entitlements-workspace.md).
-   For more information on creating software entitlements using the Software Asset Management Playbook, see [Create entitlements using the guided walk-through](../task/guidedwalk-workspace.md).

Reconciliation also runs on your subscriptions as a scheduled job or on-demand. You can view your reconciliation results in the [License Workbench](sam-license-workbench.md) \(Software Asset Management classic application\) or the [License usage view](sam-workspace-workbench.md) \(Software Asset Workspace\). Use these results to determine your license compliance position and to remediate any non-compliance.

-   For more information on running reconciliation in the Software Asset Management classic application, see [Run software reconciliation](../task/t_RunReconciliation.md).
-   For more information on running reconciliation in the Software Asset Workspace, see [Run software reconciliation in the workspace](../task/run-recon-workspace.md).

