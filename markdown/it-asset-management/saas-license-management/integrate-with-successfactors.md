---
title: Integrating with SAP SuccessFactors
description: Integrating your Software Asset Management application with the SAP SuccessFactors application enables you to track your software subscriptions and to reclaim unused licenses.Set up basic authentication to enable access to the SAP SuccessFactors API.Create a connection between your SAP SuccessFactors OData API and your ServiceNow instance.Enable client certificate authentication for the outbound communication from SAP Master Data service by generating the keystore.jks and keystore.cer files.Enable client certificate authentication for the outbound communication by uploading the JKS certificate in your ServiceNow instance.Use the API key generated during the client application configuration to register the application as an OAuth provider.Create a SAML2 assertion record to generate the SAML2 assertion and exchange the assertion for the access tokens with the provider.Create a connection record for the OData API in SuccessFactors. The SuccessFactors spoke connection and credential alias uses these connections to perform actions in SuccessFactors.Create a connection record for the OData API in SuccessFactors. The SuccessFactors spoke connection and credential alias uses these connections to perform actions in SuccessFactors.Create an SAP SuccessFactors integration profile to track software subscriptions and optimize licensing for your SAP SuccessFactors applications.
locale: en-US
release: australia
product: SaaS License Management
classification: saas-license-management
topic_type: concept
last_updated: "2026-03-12"
reading_time_minutes: 22
breadcrumb: [Integrate with SaaS applications, SaaS License Management, Software Asset Management, IT Asset Management]
---

# Integrating with SAP SuccessFactors

Integrating your Software Asset Management application with the SAP SuccessFactors application enables you to track your software subscriptions and to reclaim unused licenses.

**Important:**

You must request and install the following applications from [ServiceNow Store](https://store.servicenow.com/sn_appstore_store.do#!/store/home):

-   SaaS License Management
-   SuccessFactors Spoke
-   Software Asset Management integration with SuccessFactors

-   If your installed SAP SuccessFactors spoke version is 3.1.5 or lower, follow these steps:
    1.  [Set up basic authentication for SAP SuccessFactors](integrate-with-successfactors.md#)
    2.  [Create an SAP SuccessFactors connection](integrate-with-successfactors.md#)
    3.  [Create an SAP SuccessFactors integration profile](integrate-with-successfactors.md#)
-   If your installed SAP SuccessFactors spoke version is 4.0.0 or higher, follow these steps:
    1.  [Register OAuth application in SuccessFactors](integrate-with-successfactors.md#)
    2.  [Upload the JKS certificate in your ServiceNow instance](integrate-with-successfactors.md#)
    3.  [Register SuccessFactors as an OAuth provider](integrate-with-successfactors.md#)
    4.  [Create the SAML2 assertion producer record](integrate-with-successfactors.md#)
    5.  [Create credential record for the OData API](integrate-with-successfactors.md#)
    6.  [Create connection record for the OData API](integrate-with-successfactors.md#)
    7.  [Create an SAP SuccessFactors integration profile](integrate-with-successfactors.md#)

**Important:** Minimize security risks and protect information by granting access only to the necessary user or API permissions.

|Process|Required user role in the SAP SuccessFactors application|Authentication scopes|
|-------|--------------------------------------------------------|---------------------|
|Download subscriptions|admin|None|
|Pull user activity|admin|None|
|Reclaim subscription|admin|None|

## Set up basic authentication for SAP SuccessFactors

Set up basic authentication to enable access to the SAP SuccessFactors API.

### Before you begin

SAP SuccessFactors Role required: admin

### Procedure

1.  Log in to the SAP SuccessFactors instance using your admin credentials.

2.  On the page header of your instance, select **Home** &gt; **Admin Center**.

3.  Create a group to assign API access permissions to.

    **Tip:** Include only non-admin users in this group, as admin users automatically have access to the SuccessFactors API.

    1.  In the **Tool Search** field of the Admin Center, search for and select **Manage Permission Groups**.

    2.  On the Permission Group dialog box, enter a name for the permission group in the **Group Name** field.

    3.  In the Choose Group Members section, specify the users or user groups that you want to include in this permission group by adding them to a People Pool.

        People Pools allow you to specify the sets of users or user groups that you want to include or exclude for a permission group. You can either include all users and user groups in a single People Pool or group them into different People Pools. For example, you can create different People Pools for each department or office location within your organization.

        To add users or user groups to a People Pool, select an identification category, such as **Username**, and then enter each user or user group in the corresponding text box. Each entry must be separated by a comma.

        You can apply multiple identification categories to a single People Pool by clicking **Add another category**. You can also add additional People Pools by clicking **Add another People Pool**.

    4.  In the Exclude these people from the group section, specify the users or user groups that you want to exclude from this permission group by adding them to a People Pool.

        To add users or user groups to a People Pool, select an identification category, such as **Username**, and then enter each user or user group in the corresponding text box. Each entry must be separated by a comma.

        You can apply multiple identification categories to a single People Pool by clicking **Add another category**. You can also add additional People Pools by clicking **Add another People Pool**.

    5.  Select **Done**.

4.  Configure API access permissions for your group.

    1.  In the **Tool Search** field of the Admin Center, search for and select **Manage Permission Roles**.

    2.  Select **Create New**.

    3.  On the Permission Role Detail form, enter a name for the permission role in the **Role Name** field.

    4.  Enter a description for the permission role in the **Description** field.

    5.  Under Permission settings, select **Permission...**.

    6.  In the Permission settings dialog box, select **Manage Integration Tools** from the left navigation pane.

    7.  Select the **Allow Admin to Access OData API through Basic Authentication** check box.

    8.  Select **Employee Central API** from the left navigation pane.

    9.  Select the **Employee Central HRIS OData API \(editable\)** check box.

    10. Select **Done**.

        The dialog box closes and you return to the Permission Role Detail form.

    11. Under the **Grant this role to...** tab, select **Add...** to search for and select the permission groups that you created in step [4](integrate-with-successfactors.md#create-group).

        Adding this permission group allows the associated users and user groups to access the APIs that are enabled in this permission role.

    12. Select **Save Changes**.


## Create an SAP SuccessFactors connection

Create a connection between your SAP SuccessFactors OData API and your ServiceNow instance.

### Before you begin

ServiceNow Role required: sam\_integrator

### Procedure

1.  From your ServiceNow instance, navigate to **Process Automation** &gt; **Flow Designer**.

    The Flow Designer launches in a new tab.

2.  Select the **Connections** tab.

3.  Select **View Details** for your SuccessFactors\_OData connection.

4.  From the list of available connections, search for and select SuccessFactors\_OData.

5.  Select **Configure**.

6.  In the Configure Connection dialog box, fill in the fields.

    |Field|Description|
    |-----|-----------|
    |Connection Name|Name of the SuccessFactors\_OData connection.|
    |Connection URL|OData API URL of your SAP SuccessFactors instance.|
    |User name|Username for your SAP SuccessFactors admin account. Enter the same username that you used to log in to your SAP SuccessFactors instance in [Set up basic authentication for SAP SuccessFactors](integrate-with-successfactors.md#).|
    |Password|Password for your SAP SuccessFactors admin account. Enter the same password that you used to log in to your SAP SuccessFactors instance in [Set up basic authentication for SAP SuccessFactors](integrate-with-successfactors.md#).|

7.  Select **Configure Connection**.


## Register OAuth application in SuccessFactors

Enable client certificate authentication for the outbound communication from SAP Master Data service by generating the `keystore.jks` and `keystore.cer` files.

### Before you begin

Role required: admin

### Procedure

1.  Create a JKS certificate by using any one of the following methods:

    -   Follow the steps in the [Creating Java Keystore\(JKS\) with Private Key and Certificate Chain](https://help.sap.com/docs/SAP_Cloud_Platform_Master_Data_for_Business_Partners/246fb358c1c7413289c03b8c72734209/18f5bae37a664396b2ebbc1b3c384c53.html) topic [SAP Help Portal](https://help.sap.com/docs/).
    -   Install Java JDK 8 and Open SSL and execute the following commands in the Terminal:

        1.  `openssl genrsa -out private.key 2048`

            The `private.key` file is generated.

        2.  `openssl rsa -in private.key -pubout -out public.key`

            Extract the public key from key pair type.

        3.  `openssl req -new -x509 -key private.key -out publickey.cer -days 365`

            Enter details of the Distinguished Name \(DN\). The `publickey.cer` file is generated.

        4.  `openssl pkcs12 -export -in publickey.cer -inkey private.key -out successfactors.p12 -name "successfactors"`

            You’re prompted for a password. The `successfactors.p12` file is generated using the private and public key created in step a and step b.

        5.  `keytool -importkeystore -srckeystore successfactors.p12 -srcstoretype pkcs12 -destkeystore successfactors.jks`

            You’re prompted for the destination and source file password. The `successfactors.jks` file is created using the `successfactors.p12` file created in step c.

        **Note:** Confirm that you enter the same passwords in steps c and d. For example, if you enter the password as `123456` in step c, you must enter `123456` as password in step d too.

2.  Log in to the SuccessFactors account as an admin.

3.  Navigate to **Admin Centre** and select **Company Settings**.

4.  Select **Manage OAuth2 Client Applications**.

5.  Select **Register Client Application**.

    ![Managing OAuth2 client applications](../image/manage-oauth-client-sf.png)

6.  In the **X.509 Certificate** field, provide the contents of the `publickey.cer` file \(public key\) without the headers.

7.  Select **Submit**.


### Result

The API Key is generated and displayed.

### What to do next

Copy the API key generated and record the value for later use.

## Upload the JKS certificate in your ServiceNow instance

Enable client certificate authentication for the outbound communication by uploading the JKS certificate in your ServiceNow instance.

### Before you begin

Role required: admin

### Procedure

1.  Log in to your ServiceNow instance as an admin.

2.  Upload the JKS certificate to your ServiceNow instance.

    For instructions to upload the JKS certificate, see Upload a certificate to an instance.![Uploading certificate to an instance](../image/saml-oauth-sf.png)


## Register SuccessFactors as an OAuth provider

Use the API key generated during the client application configuration to register the application as an OAuth provider.

### Before you begin

Change the application scope to SuccessFactors spoke.

Role required: admin

### Procedure

1.  In your ServiceNow instance, navigate to **System OAuth** &gt; **Application Registry**.

2.  Select **New**.

3.  In the form, fill in these fields.

<table id="table_yb3_bwh_dwb"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Name

</td><td>

Unique name to identify the certificate. For example, `SuccessFactors SAML`.

</td></tr><tr><td>

Client ID

</td><td>

Value of the API key you had copied after registering the OAuth client application in SuccessFactors.

</td></tr><tr><td>

Client Secret

</td><td>

**Note:** Client secret isn’t needed to register the application as an OAuth provider. You can provide any value for this field.

</td></tr><tr><td>

Default Grant Type

</td><td>

Default grant type used to establish the token. Select **SAML2 Bearer**.

</td></tr><tr><td>

Token URL

</td><td>

SuccessFactors OAuth server endpoint URL that includes the Company ID in this format: `https://<SuccessFactors_Instance_Name>/oauth/token?company_id=<Company_ID>`. For example, `https://example.successfactors.eu/oauth/token?company_id=SFCPART123456`.

</td></tr></tbody>
</table>    ![Application Registries form](../image/app-registry-sf.png)

4.  Select **Submit**.


## Create the SAML2 assertion producer record

Create a SAML2 assertion record to generate the SAML2 assertion and exchange the assertion for the access tokens with the provider.

### Before you begin

Change the application scope to SuccessFactors spoke.

Role required: admin

### Procedure

1.  Create a SAML2 assertion producer record in your instance.

    1.  Navigate to **All** &gt; **System OAuth** &gt; **SAML2 Assertion Producers**.

    2.  Select **New**.

    3.  On the form, fill these values.

        |Field|Description|
        |-----|-----------|
        |Name|Unique name to identify the SAML2 assertion producer record. For example, `Successfactor SAML OAuth`.|
        |Issuer|Unique identifier for the assertion issuing entity. Provide the ServiceNow instance URL.|
        |Subject NameID|User name to log in to the SuccessFactors instance. For example, `sfadmin`.|
        |Audience|Intended audience for the assertion. Enter the value, `www.successfactors.com`.|
        |Recipient|Intended recipient for the assertion. Enter URL in this format, `https://<SuccessFactors-Instance-Name>/oauth/token`.|

        ![SAML2 Assertion Producer](../image/saml-assert-prov.png)

    4.  Select and hold \(or right-click\) the form header and select **Save**.

    5.  Under the **SAML2 Assertion Keystores** tab, select **New**.

    6.  On the form, fill these values.

        |Field|Description|
        |-----|-----------|
        |Name|Unique name to identify the SAML2 assertion keystore record. For example, `successfactors`.|
        |Signing Key Alias|Alias of key entry stored in the Keystore used to sign the assertion. For example, `successfactors`.|
        |Signing Key Password|Password of the key entry stored in the keystore used to sign the assertion.|
        |Signing Keystore|Required X.509 certificate record. Select the X.509 certificate record that you had earlier created. For more information, see[Upload the JKS certificate in your ServiceNow instance](integrate-with-successfactors.md#).|

        ![SAML2 Assertion Keystore.](../image/saml-assert-keystore.png)

    7.  Select **Submit**.

    8.  Navigate to **All** &gt; **System OAuth** &gt; **SAML2 Assertion Producers**.

    9.  Open the SAML2 assertion producer record that you had created.

        For example, **Successfactor SAML OAuth**.

    10. Under the **SAML2 Assertion Attributes** tab, select **New**.

    11. On the form, fill these values.

        |Field|Description|
        |-----|-----------|
        |Name|Name to identify the SAML2 assertion attribute record. Enter `api_key`.|
        |Type|Type of the **Value** field. Select **String**.|
        |Value|API key generated after the OAuth client application is created in SuccessFactors.|

        ![SAML2 Assertion Attribute.](../image/saml2-assertion-att.png)

    12. Select **Submit**.

2.  Associate the SAML2 assertion producer with the application registry record.

    1.  Navigate to **System OAuth** &gt; **Application Registry**.

    2.  Open the application registry record that you had created.

        For example, **SuccessFactors OAuth Reg**. For more information about creating the application registry, see [Register SuccessFactors as an OAuth provider](integrate-with-successfactors.md#).

    3.  Under the **OAuth Entity Profiles** tab, open the default OAuth entity profile record.

        For example, **Successfactor SAML default\_profile**.

    4.  For the **Assertion Producer** field, select the SAML2 assertion producer record you had created.

        For example, **Successfactor SAML OAuth**.![Defining OAuth scoped for this profile](../image/oauth-ent-profile-sf.png)

    5.  Select **Update**.


## Create credential record for the OData API

Create a connection record for the OData API in SuccessFactors. The SuccessFactors spoke connection and credential alias uses these connections to perform actions in SuccessFactors.

### Before you begin

Role required: admin

### Procedure

1.  Navigate to **All** &gt; **Connections &amp; Credentials** &gt; **Credentials**.

2.  Click **New**.

    The system displays the message **What type of Credentials would you like to create?**.

3.  Select **OAuth 2.0 Credentials**.

    An empty OAuth 2.0 Credentials form is displayed.

4.  On the form, fill these values.

<table id="table_twl_mk2_5kb"><thead><tr><th>

Field

</th><th>

Value required

</th></tr></thead><tbody><tr><td>

Name

</td><td>

Name to uniquely identify the record. For example, enter `SAML_SuccessFactors_OData_Cred`.

</td></tr><tr><td>

OAuth Entity Profile

</td><td>

OAuth entity profile record that is associated with the OAuth application registry you had created. For example, `Successfactor SAML default_profile`.For more information about creating the application registry, see [Register SuccessFactors as an OAuth provider](integrate-with-successfactors.md#).

</td></tr><tr><td>

Active

</td><td>

Option to actively use the credential record.

</td></tr><tr><td>

Order

</td><td>

Order to apply this credential. For example, enter `100`.

</td></tr></tbody>
</table>    ![OAuth 2.0 credentials](../image/saml-sf-odata-cred.png)

5.  Click **Submit**.


### Result

The credential record to authorize actions using the OData API is created.

## Create connection record for the OData API

Create a connection record for the OData API in SuccessFactors. The SuccessFactors spoke connection and credential alias uses these connections to perform actions in SuccessFactors.

### Before you begin

Role required: admin

### Procedure

1.  Navigate to **All** &gt; **Connections &amp; Credentials** &gt; **Connection &amp; Credential Aliases**.

2.  Open for the record for **SuccessFactors OData**.

    For example, **SuccessFactors\_OData**.

3.  From the **Connections** tab, click **New**.

    The system displays an empty HTTP\(s\) Connection form.

4.  On the form, fill these values.

    |Field|Description|
    |-----|-----------|
    |Name|Name to uniquely identify the record. For example, `SAML_SuccessFactors_OData_Conn`.|
    |Credential|Credential record you created for the OData API. For example, `SAML_SuccessFactors_OData_Cred`.|
    |Connection URL|SuccessFactors service root URL in this format: `https://<SuccessFactors_Instance_Name>/odata/v2`. For example, `https://apisalesdemo2.successfactors.eu/odata/v2`.|
    |Active|Option to actively use the connection record.|

5.  Click **Submit**.


### Result

The connection record for the OData API in SuccessFactors is created.

## Create an SAP SuccessFactors integration profile

Create an SAP SuccessFactors integration profile to track software subscriptions and optimize licensing for your SAP SuccessFactors applications.

### Before you begin

The Software Asset Management - SaaS License Management plugin \(sn\_sam\_saas\_int\) must be installed from the [ServiceNow Store](https://store.servicenow.com/).

Change the application scope to **Global**.

ServiceNow Role required: sam\_integrator

**Important:** You must select the **Software Asset Management integration with SuccessFactors** check box for this integration while installing optional features on the Application Manager page. For more information about choosing the required SaaS applications, see [Request SaaS License Management](../task/request-saas-license-management.md).

### About this task

If you’re using Software Asset Workspace, the option to create the SuccessFactors integration profile in Core UI is inactive.

### Procedure

1.  Navigate to the integration profile.

<table id="choicetable_o3p_z3k_qtb"><thead><tr><th align="left" id="d58108e2331">

Interface

</th><th align="left" id="d58108e2334">

Action

</th></tr></thead><tbody><tr><td id="d58108e2340">

**Core UI**

</td><td>

1.  Navigate to **All** &gt; **Software Asset** &gt; **SaaS License** &gt; **Direct Integration Profiles**.
2.  Select **New**.
3.  Select **SuccessFactors Integration Profile**.


</td></tr><tr><td id="d58108e2382">

**Software Asset Workspace**

</td><td>

1.  Navigate to **License operations** &gt; **User Subscriptions** &gt; **Direct integration profiles**.
2.  Select **New**.
3.  Select **SuccessFactors** from the drop-down list.
4.  Select **Continue**.


</td></tr></tbody>
</table>2.  On the form, fill in the fields.

<table id="table_bv2_1gv_1nb"><thead><tr><th>

Field

</th><th>

Value

</th></tr></thead><tbody><tr><td>

Display Name

</td><td>

Name of the integration profile. For example, `SuccessFactors Integration`.

</td></tr><tr><td>

Status

</td><td>

Status of the integration profile. -   If you have not published the integration profile, this field is automatically set to **Draft**.
-   If you have already published the integration profile, this field is automatically set to **Published**.


</td></tr><tr><td>

Profile Type

</td><td>

Type of integration profile. This field is automatically set to `SuccessFactors Subscription`.

</td></tr></tbody>
</table>3.  Review the required user roles or API permissions specified in the **Vendor configuration** field for each process to minimize security risks and optimize SaaS licenses.

    **Note:** For more information, see [Minimal user permissions](integrate-with-workfront.md#) table.

    1.  In the Download Subscription Subflow section, verify that the **Subflow** field is set to **SuccessFactors Download Subscriptions**.

        **Note:** The **Download subscriptions** check box is selected by default and you can't clear it.

    2.  In the Calculate Activity Subflow section, verify that the **Subflow** field is set to **SuccessFactors Update User Activity**.

        **Note:** The **Download Activity** check box is selected by default. If you clear it, the activity scheduled job **SAM - Refresh &lt;displayname&gt; Activity** isn't created.

    3.  In the Reclaim Subscription Subflow section, verify that the **Subflow** field is set to **SuccessFactors Reclaim Subscription**.

        **Note:** The **Reclaim subscriptions** check box is selected by default. If you don't want to reclaim subscriptions, you can clear this check box. If you clear it, the removal candidates are created but the reclaim subscription subflow isn't triggered or the reclamation process isn't initiated.

4.  Select **Save**.

    Your ServiceNow instance creates a draft integration profile.

    The **Connection &amp; Credential** field appears and is automatically set to **sn\_successfactors.SuccessFactors\_OData**.

5.  Generate and add the SAP SuccessFactors user login report to your integration profile.

    This report is required for retrieving the last activity date of your SAP SuccessFactors users. You must generate and add the latest version of this report every time you want to update the last activity date of your SAP SuccessFactors users in the Software Subscriptions \[samp\_sw\_subscription\] table.

    1.  Log in to your SAP SuccessFactors instance using the admin credentials.

    2.  On the page header of your instance, select **Home** &gt; **Admin Center**.

    3.  On the page header of the Admin Center, select **Reporting**.

    4.  Select **New** to create a report.

    5.  When prompted to select the type of report that you want to create, select **Report - Table** &gt; **Select**.

    6.  Under **How would you like your data to be structured?**, select **Single Domain**.

    7.  Under **What data would you like to start with?**, select **Login Data**.

    8.  Click **Select**.

        The Creating Login Data report page opens.

    9.  On the **General Info** tab, fill in the fields.

        |Field|Description|
        |-----|-----------|
        |Domain|Domain from which you’re retrieving data. This field is automatically set to **Login Data**.|
        |Report Name|Name of the report.|
        |Description|Description of the report.|
        |Report Priority|Priority of the report.|
        |Remove Styling|Deselect this check box.|

    10. On the **People** tab, select **Refine criteria**.

    11. In the Define Team dialog box, fill in the fields.

        |Field|Description|
        |-----|-----------|
        |Team Manager|Manager of the team for which you want to create this report. Select **Logged In User**.|
        |Team Reporting Type|Type of report that you want to create for the team. Select **Other Filters**. When you select this report type, you can define report scopes to filter the user groups that you want to include in the report. See [step 14](integrate-with-successfactors.md#filter-criteria) for more details.|
        |Include inactive users|Option to include all inactive team members in the report. Leave this option unselected.|

    12. Select **OK**.

        The dialog box closes and you return to the **People** tab.

    13. In the Define Report Scope section of the **People** tab, select the **Division**, **Department**, and **Location** report scopes to define filter criteria for the user groups that you want to include in the report.

        By default, all filter criteria for these report scopes are enabled.

    14. On the **Columns** tab, select **+ Select Columns** to specify the data columns that you want to include in the report.

        You can sort, group, or rearrange the columns as needed.

    15. Select the **Last Login** and **User Sys ID** check boxes so that the first column is Last Login and the second column is User Sys ID on the report.

    16. On the **Configuration** tab, specify whether you want your data columns to display data in either the date only or the date and time format.

        For each applicable data column, select either **Date** \(date only\) or **Timestamp** \(date and time\). After you select the format for each data column, select **OK**.

    17. On the **Filters** tab, select filters to refine the data that is displayed on the report.

    18. Select **Refine Criteria** &gt; **Employee Login Detail** &gt; **Last Login**.

        A pop-up displays with the Define last login filter.

    19. Select the **By Rule** &gt; **Add rule** tab.

    20. From the drop-down list, select the **Greater than** option.

    21. Enter the date from when you want to generate the report.

        You must select a date not older than a couple of weeks to keep the file size within allowed limits.

    22. Select **Done** after you select the filters.

    23. Select **Generate**.

    24. In the Download section of the generated report, select **Excel** to export the report as an Excel file.

        **Note:** The Excel file must not be greater than 5 MB.

    25. Return to your SAP SuccessFactors integration profile form.

    26. On the Integration Profile form header, select the Manage Attachments icon \(![Manage attachments icon.](../image/manage-attachments-icon.png)\).

    27. In the Attachments dialog box, select **Choose file** to locate and select your user login report.

    28. After the report uploads successfully, close the dialog box to return to the integration profile form.

6.  After the form reloads, select **Validate Connection** to verify the connection and credential details of this integration.

    Validating the connection verifies the Download Subscriptions and Calculate Activity APIs, but not the Reclaim Subscriptions APIs.

7.  After the connection is verified, select **Publish**.

8.  In the Publish Confirmation dialog box, select **OK**.

    **Note:** If you clear the **Download Activity** check box after the integration profile is published, you must revalidate the connections and then republish the integration profile because the following events occur:

    -   The **Status** field on the integration profile form changes to **Draft**.
    -   The **Validate connection** button shows up on the form.
    -   The current **SAM - Refresh &lt;displayname&gt; Activity** job gets deleted.
    By default, the activity job runs every one hour and deletes the file attached to the integration profile as part of the clean-up. If the file isn't found, the activity job fails to indicate no new attachment. The job failure has no impact on the already updated last activity.

    If you plan to attach the file once everyday or once a week, you can update the run time of the **SAM - Refresh Success Factors Activity** scheduled job accordingly. You can also run this job on demand whenever you attach a file.

    You must attach a file every time for the job to run because SAP SuccessFactors doesn’t have an API for activity data pull.


### What to do next

After the integration connects, your ServiceNow instance automatically creates software models, reclamation rules, and software subscriptions that are refreshed daily.

After creating an integration profile, view information about the profile in the Software Asset Workspace by navigating to **License operations** &gt; **User subscription** &gt; **Direct integration profiles**. You can select an integration profile to view the following related lists. If all of the following related lists aren't visible for an integration profile in the default view, you can select the custom integration view from the Details tab:

-   Software Models
-   Unrecognized Subscription Identifiers
-   Scheduled Jobs
-   Scheduled Job Results
-   Software Subscriptions
-   Subscription Identifier Exclusion Rule
-   Subscription User Exclusion Rule

After creating an integration profile, you can define subscription exclusion rules to keep certain subscriptions from license cost calculations. For more information, see [Subscription exclusions for SaaS and SSO applications](subscription-exclusions.md#).

If you want to set up multiple integration profiles with unique connections, create child aliases to manage different configurations and settings for each integration profile. For more information, see [Create a child alias to set up multiple integration profiles](../reuse/create-child-alias-saas.md).

**Important:** Child aliases and alias overrides aren't supported for the **SuccessFactors Update User Activity** subflow because this subflow doesn't use REST steps directly where aliases are required.

Review all automatically generated reclamation rules to reclaim user subscriptions. For more information, see [Review a software reclamation rule](../task/add-reclamation-rule-sub.md).

Create software entitlements for the automatically generated software models to track used software against owned software.

-   For more information on creating software entitlements in the Software Asset Management Core UI, see [Create entitlements in Software Asset Management classic](../task/track-software-rights.md).
-   For more information on creating software entitlements in the Software Asset Workspace, see [Create entitlements in workspace](../task/create-entitlements-workspace.md).
-   For more information on creating software entitlements using the Software Asset Management Playbook, see [Create entitlements using the guided walk-through](../task/guidedwalk-workspace.md).

Reconciliation also runs on your subscriptions as a scheduled job or on-demand. You can view your reconciliation results in the [License Workbench](sam-license-workbench.md) \(Software Asset Management classic application\) or the [License usage view](sam-workspace-workbench.md) \(Software Asset Workspace\). Use these results to determine your license compliance position and to remediate any non-compliance.

-   For more information on running reconciliation in the Software Asset Management classic application, see [Run software reconciliation in Software Asset Management classic](../task/t_RunReconciliation.md).
-   For more information on running reconciliation in the Software Asset Workspace, see [Run software reconciliation in the workspace](../task/run-recon-workspace.md).

