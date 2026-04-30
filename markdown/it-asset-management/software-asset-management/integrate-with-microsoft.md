---
title: Integrating with Microsoft 365
description: Integrating your ServiceNow instance with the Microsoft 365 service enables you to track your software subscriptions and software usage to determine license compliance and act on optimization opportunities.Register an application through the Microsoft Azure portal.Grant your application access to Power BI service content and APIs by enabling service principal authentication for Power BI read-only APIs. Power BI service content and APIs help optimize your Microsoft 365 subscriptions, such as by downgrading subscriptions from Office 365 E5 to Office 365 E3.Prevent anonymous user information in Microsoft 365 reports on activity to be imported to ServiceNow.Create an integration profile to track software subscriptions and optimize stale licenses for the Microsoft 365 service.Determine the exact software subscription information to be pulled from the Microsoft 365 admin center and verify if complete subscription information is pulled accurately to ServiceNow.Monitor the usage activity data for Microsoft 365 Copilot, Visio Online, and Project Online to identify reclamation candidates based on low usage.Evaluate software usage activity to discover active, inactive, and unassigned subscriptions among all subscriptions found on the Microsoft 365 portal.Evaluate Microsoft 365 compliance and optimization results to find actual and potential cost savings and recommended licensing optimizations.Change the endpoints of the REST message and OAuth application on your ServiceNow subscription profile so that you can use your subscriptions.If the User field in the Software Subscription \[samp\_sw\_subscription\] table is empty, map the field with an associated user.
locale: en-US
release: xanadu
product: Software Asset Management
classification: software-asset-management
topic_type: concept
last_updated: "2024-08-01"
reading_time_minutes: 27
breadcrumb: [Microsoft 365 integration, Software Asset Management publisher pack for Microsoft, Supported software publisher licenses, Software Asset Management, IT Asset Management]
---

# Integrating with Microsoft 365

Integrating your ServiceNow instance with the Microsoft 365 service enables you to track your software subscriptions and software usage to determine license compliance and act on optimization opportunities.

For more information about the Microsoft 365 services, see [Microsoft 365 plans](https://www.microsoft.com/en-us/microsoft-365/enterprise/compare-office-365-plans).

**Important:** Minimize security risks and protect information by granting access only to the necessary user or API permissions.

<table id="table_box"><thead><tr><th>

Process

</th><th>

Required user role in the Microsoft 365 application

</th><th>

Authentication scopes

</th></tr></thead><tbody><tr><td>

Download subscriptions

</td><td>

Application developer

</td><td>

-   User.Read.All
-   Organization.Read.All

</td></tr><tr><td>

Pull user activity

</td><td>

-   Power platform administrator
-   Application developer

</td><td>

Reports.Read.All

</td></tr></tbody>
</table>**Parent Topic:**[Microsoft 365 integration](microsoft-o365.md)

## Register a Microsoft Azure AD application

Register an application through the Microsoft Azure portal.

### Before you begin

Microsoft Azure AD Role required: Refer to the [Minimal user permissions](integrate-with-microsoft.md#) table.

### Procedure

1.  From a web browser, open the [App registrations page](https://portal.azure.com/?Microsoft_AAD_RegisteredApps=true#blade/Microsoft_AAD_RegisteredApps/ApplicationsListBlade) of the Microsoft Azure portal.

2.  Log in using your global administrator credentials.

3.  On the App registrations page, select **New registration**.

4.  In the Name section of the Register an application form, enter a name for the application.

5.  In the Supported account types section, select **Accounts in any organizational directory \(Any Microsoft Entra ID - Multitenant\)**.

6.  Select **Register**.

    The application is registered and you’re automatically redirected to the Overview page for the new application.

7.  On the Overview page, copy the values in the **Application \(client\) ID** and **Directory \(tenant\) ID** fields.

    Save them in a secure location for later use.

8.  Generate a Client secret for your application.

    1.  From the side navigation menu, navigate to **Manage** &gt; **Certificates &amp; secrets**.

        The Certificates &amp; secrets page opens.

    2.  In the Client secrets section, generate a client secret for the application by selecting **New client secret**.

    3.  In the dialog box, fill in the fields.

<table id="table_mks_npw_rqb"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Description

</td><td>

Description of the client secret.

</td></tr><tr><td>

Expires

</td><td>

Time period after which you want the client secret to expire. The options are:-   In 1 year
-   In 2 years
-   Never


</td></tr></tbody>
</table>    4.  Select **Add**.

        The dialog box closes and you return to the Certificates &amp; secrets page.

    5.  In the Client secrets section, copy the value in the **VALUE** field for the newly generated client secret.

        Save this in a secure location for later use.

9.  Specify the level of access that the application has to your protected resources.

    1.  From the side navigation menu, navigate to **Manage** &gt; **API permissions**.

    2.  On the API permissions page, select **Add a permission**.

    3.  In the Request API permissions dialog box, select the **Microsoft APIs** tab.

    4.  From the list of available Microsoft APIs, select **Microsoft Graph**.

    5.  When prompted to select the types of permissions that the application requires, select **Application permissions**.

    6.  Under Select permissions, select the check boxes for the following permissions:

        -   Reports.Read.All
        -   User.Read.All
        -   Organization.Read.All
    7.  Select **Add permissions**.

        The dialog box closes and you return to the API permissions page.

10. Grant admin consent for your application.


### What to do next

After you successfully register and set up your application, remain in the Microsoft Azure portal if you must enable your application to access Power BI service content and APIs.

## Enable service principal authentication for Power BI read-only APIs

Grant your application access to Power BI service content and APIs by enabling service principal authentication for Power BI read-only APIs. Power BI service content and APIs help optimize your Microsoft 365 subscriptions, such as by downgrading subscriptions from Office 365 E5 to Office 365 E3.

### Before you begin

Microsoft Azure AD Role required: global administrator

Power BI Role required: Power platform administrator

**Note:** This configuration enables the ServiceNow Software Asset Management application to get the usage information \(Last usage time\) for all Power BI Pro deployments across the Web and Desktop. The Software Asset Management application pulls the last activity date for Power BI deployments that are part of Microsoft 365 subscriptions.

### About this task

Service principal is an authentication method that enables your application to access secure Microsoft Azure AD resources, such as Power BI service content and APIs.

### Procedure

1.  Create a security group for service principal authentication.

    Security groups enable you to manage which users, devices, groups, and service principals can access shared resources. If you want to use an existing security group for service principal authentication, skip to [step 2](integrate-with-microsoft.md#add-app-security-group).

    1.  On the page header of the Microsoft Azure portal, use the search bar to search for and select the **Microsoft Entra ID** service.

        The Overview page for the Microsoft Azure AD service opens.

    2.  From the side navigation menu of the Microsoft Azure AD service, navigate to **Manage** &gt; **Groups**.

        The **Groups** &gt; **All groups** page opens.

    3.  On the All groups page, select **New group**.

    4.  On the form, fill in the fields.

<table id="table_rj1_j5y_pqb"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Group type

</td><td>

Group type.Set this field to **Security**.

</td></tr><tr><td>

Group name

</td><td>

Name of the group.

</td></tr><tr><td>

Group email address

</td><td>

Email address that is shared between all group members.

</td></tr><tr><td>

Group description

</td><td>

Description of the group.

</td></tr><tr><td>

Membership type

</td><td>

Method in which members can be added to or removed from the group.Set this field to **Assigned**.

</td></tr></tbody>
</table>    5.  Select **Create**.

    The security group is created and then you’re redirected to the Overview page for the new group.

2.  Add the application that you created in [Register a Microsoft Azure AD application](integrate-with-microsoft.md#) as a member of your security group.

    1.  If you didn’t create a security group in [step 1](integrate-with-microsoft.md#create-security-group) and are using an existing security group instead, open your existing security group.

        If you created a security group in [step 1](integrate-with-microsoft.md#create-security-group), skip to [step b](integrate-with-microsoft.md#step-b).

        1.  On the page header of the Microsoft Azure portal, use the search bar to search for and select the **Microsoft Entra ID** service.

            The Overview page for the Microsoft Azure AD service opens.

        2.  From the side navigation menu of the Microsoft Azure AD service, navigate to **Manage** &gt; **Groups**.

            The **Groups** &gt; **All groups** page opens.

        3.  From the list of available groups, locate and select your existing security group.

            The Overview page for the security group opens.

    2.  From the side navigation menu of your security group, navigate to **Manage** &gt; **Members**.

        The Members page opens.

    3.  On the Members page, select **Add members**.

        The Add members dialog box opens.

    4.  In the dialog box, search for and select the application that you created in [Register a Microsoft Azure AD application](integrate-with-microsoft.md#).

        **Important:** The application must not have any Power BI admin permissions set from the Microsoft Azure portal. You can verify your application permissions using the following steps:

        1.  Log in to the Microsoft Azure portal using either your global administrator, application administrator, or cloud application administrator credentials.
        2.  On the page header of the Microsoft Azure portal, use the search bar to search for and select the **Microsoft Entra ID** service.

            The Overview page for the Microsoft Azure AD service opens.

        3.  From the side navigation menu of the Microsoft Azure AD service, navigate to **Manage** &gt; **Enterprise applications**.

            The Enterprise applications page opens.

        4.  From the list of available enterprise applications, locate and select your application.
        5.  Select **Permissions**.
        6.  Verify that no Power BI admin-consent-required permissions are set on the application.
    5.  Select **Select**.

        The application is added as a member of your security group.

3.  Enable your security group to access read-only Power BI admin APIs.

    1.  In a new tab or web browser, open [Power BI](https://app.powerbi.com/).

    2.  Log in using either your global administrator or Power BI administrator credentials.

        The Power BI portal opens.

    3.  On the page header of the Power BI portal, select the Settings icon \(![Settings icon.](../image/gear-icon.png)\) and then select **Admin portal**.

        The Power BI Admin portal opens.

    4.  From the side navigation menu of the Admin portal, select **Tenant settings**.

    5.  In the Admin API settings section, expand the **Allow service principals to use read-only Power BI admin APIs** setting.

    6.  Select the toggle button to enable the setting.

    7.  When prompted, select the option to apply the setting to **Specific security groups**.

    8.  In the corresponding text box, enter the name of your security group.

    9.  Select **Apply**.

    After you enable this setting through the Power BI Admin portal, any application permissions that you set from the Microsoft Azure portal are no longer effective. All application permissions must subsequently be set and managed through the Power BI Admin portal.


## Configure updates on Microsoft 365 Admin Center

Prevent anonymous user information in Microsoft 365 reports on activity to be imported to ServiceNow.

### Before you begin

Role required: admin

### Procedure

1.  Log in to [Microsoft 365 admin center](https://admin.microsoft.com/Adminportal/Home) by using your admin credentials.

2.  Navigate to **Settings** &gt; **Services** &gt; **Org settings** &gt; **Reports**.

3.  Deselect the **Display concealed user, group, and site names in all reports** check box.

    For more information about the Microsoft 365 reports showing anonymous user information, see [Microsoft 365 reports show anonymous user names instead of actual user names](https://docs.microsoft.com/en-US/office365/troubleshoot/miscellaneous/reports-show-anonymous-user-name).


## Create a Microsoft 365 integration profile

Create an integration profile to track software subscriptions and optimize stale licenses for the Microsoft 365 service.

### Before you begin

ServiceNow Role required: sam\_integrator or admin

To integrate with Microsoft 365, activate the following plugins:

-   Software Asset Management Professional for Microsoft plugin \(com.snc.samp.microsoft\)
-   Software Asset Management - SaaS License Management \(sn\_sam\_saas\_int\) plugin from the [ServiceNow Store](https://store.servicenow.com/)

    For more information, see [Request SaaS License Management](../task/request-saas-license-management.md).


### About this task

If you’re using Software Asset Workspace, the option to create the direct integration profile in Core UI is inactive.

### Procedure

1.  From a web browser, open your ServiceNow instance.

<table id="choicetable_w41_4c4_2cc"><thead><tr><th align="left" id="d110174e1298">

Interface

</th><th align="left" id="d110174e1301">

Action

</th></tr></thead><tbody><tr><td id="d110174e1307">

**Core UI**

</td><td>

Navigate to **All** &gt; **Software Asset** &gt; **SaaS License** &gt; **Direct Integration Profiles**

</td></tr><tr><td id="d110174e1330">

**Software Asset Workspace**

</td><td>

1.  Navigate to **Workspaces** &gt; **Software Asset Workspace** &gt; **License operations**.
2.  Under **User subscription**, select **Direct integration profiles**.


</td></tr></tbody>
</table>2.  Select **New**.

3.  Select **Microsoft 365 Integration Profile**.

4.  On the form, fill in the fields.

<table id="table_e5p_q3w_rqb"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Display name

</td><td>

Name of the integration profile. For example, `Microsoft 365 integration for <*your-company*>`.

</td></tr><tr><td>

Client Id

</td><td>

Client ID of the application that you registered in the Microsoft Azure portal. Enter the application \(client\) ID that you copied in [Register a Microsoft Azure AD application](integrate-with-microsoft.md#).

</td></tr><tr><td>

Client secret

</td><td>

Client secret of the application that you registered in the Microsoft Azure portal. Enter the client secret that you copied in [Register a Microsoft Azure AD application](integrate-with-microsoft.md#).

</td></tr><tr><td>

Tenant name or Id

</td><td>

Globally unique identifier \(GUID\) of the application that you registered in the Microsoft Azure portal. Enter the directory \(tenant\) ID that you copied in [Register a Microsoft Azure AD application](integrate-with-microsoft.md#).**Warning:** When entering the directory \(tenant\) ID, do not add any additional extensions to the ID. Enter the ID exactly as it was copied in [Register a Microsoft Azure AD application](integrate-with-microsoft.md#).

</td></tr><tr><td>

REST message

</td><td>

Message that enables you to send requests to a REST web service endpoint.

</td></tr><tr><td>

Profile type

</td><td>

Type of integration profile. This field is automatically set to **Microsoft 365**.

</td></tr></tbody>
</table>5.  Select **Submit**.

6.  Check the status of the user subscription job by navigating to **Software Asset** &gt; **Administration** &gt; **Job Results**.


### What to do next

When you create an integration profile, a reclamation rule is automatically created for the software. It's important that you review the reclamation rule to ensure that it meets your specifications. You can view all automatically generated reclamation rules for Office 365 by navigating to **Software Asset** &gt; **Administration** &gt; **Reclamation Rules**. Reclamation rules are applied based on the Microsoft System Center Configuration Management \(SCCM\) usage data that is pulled through the Microsoft SCCM usage integration. For more information on these reclamation rules, see [Create a reclamation rule to import Microsoft SCCM usage data](../task/create-reclamation-rule-sccm.md).

**Note:** ServiceNow automatically creates one default reclamation rule for Office 365. You can also update the Last activity threshold field under the Subscription Usage Condition tab.

**Related topics**  


[Reclamation rules for Microsoft 365 integration](../reference/m365-reclamation-rules.md)

## Determine and verify Microsoft 365 subscription information in your ServiceNow instance

Determine the exact software subscription information to be pulled from the Microsoft 365 admin center and verify if complete subscription information is pulled accurately to ServiceNow.

### Before you begin

Role required: sam\_admin

### Procedure

1.  Filter with the Microsoft 365 integration profile you created to determine the exact software subscription information to be pulled from Microsoft 365 admin center to ServiceNow.

    This subscription includes all subscriptions available on the Microsoft 365 admin center.

2.  Verify with the Microsoft 365 admin if complete subscription information is pulled accurately to ServiceNow.

    **Note:**

    Software Asset Management pulls the last activity date for Microsoft 365 products using a combination of Microsoft System Center Configuration Manager \(SCCM\) integration and Microsoft 365 integration.

3.  If your Microsoft 365 subscription data isn’t getting pulled into Software Asset Management, verify your integration setup:

    1.  On the Integration Profile form, open the REST message record by selecting the Preview icon \(![Preview icon.](../image/preview-icon.png)\) next to the **REST message** field and then selecting **Open Record** in the record preview.

    2.  On the Rest Message form, select the **Get OAuth Token** related link.

        **Note:** For the role required to perform this step, refer to the [Minimal user permissions](integrate-with-microsoft.md#) table.

    3.  On the OAuth flow verification dialog box, view the status of the OAuth flow to determine whether your integration is set up correctly.

        -   If the `OAuth token flow completed successfully` message appears, your integration is set up correctly.
        -   If the `OAuth flow failed` message appears, your integration isn’t set up correctly. Use the information in this message to identify the errors in your integration setup.
4.  If your Power BI usage isn’t getting pulled into Software Asset Management, verify the status of your Power BI API connection.

    1.  On the Integration Profile form, select and hold \(or right-click\) the form header.

    2.  Select **Show XML**.

        **Note:** If the **Show XML** option isn't visible in the default view, you can customize the view. Select and hold \(or right-click\) the form header and then select **View** &gt; **custom integration**.

    3.  Under **&lt;xml&gt;** &gt; **&lt;samp\_sw\_subscription\_profile&gt;** &gt; **&lt;custom\_properties&gt;**, view the **powerBIAPIStatus** property to determine the status of your Power BI API connection.

        -   If the **powerBIAPIStatus** property is set to **success**, the Power BI API connection was successful.
        -   If the **powerBIAPIStatus** property is set to **failed**, the Power BI API connection wasn’t successful. Verify that you’ve followed all the integration setup steps correctly. You can also check your logs for more information about any errors in your integration setup.
5.  If the **User** field in the Software Subscription \[samp\_sw\_subscription\] table is empty, you can map the field with an associated user.

    For more information, see [Associate a user with subscription records](integrate-with-microsoft.md#).


## Upload the Microsoft 365 Copilot, Visio Online, and Project Online usage reports to your ServiceNow instance

Monitor the usage activity data for Microsoft 365 Copilot, Visio Online, and Project Online to identify reclamation candidates based on low usage.

### Before you begin

Role required:

-   Access the Microsoft 365 admin center: admin
-   Add reports to the ServiceNow instance: sam\_admin

### About this task

You can export the usage reports for Microsoft Copilot, Visio Online, and Project Online from the [Microsoft 365 admin center](https://admin.microsoft.com/#/homepage) and add the reports to your ServiceNow instance. These usage activity reports help in license optimization by identifying potential reclamation candidates based on low usage.

### Procedure

1.  Log in to [Microsoft 365 admin center](https://admin.microsoft.com/#/homepage) using your global administrator credentials.

2.  Navigate to **Reports** &gt; **Usage**.

3.  Download the usage reports.

    1.  Select **Copilot for Microsoft 365** and download the CSV file by selecting **Export**.

    2.  Select **Project** and download the CSV file by selecting **Export**.

    3.  Select **Visio** and download the CSV file by selecting **Export**.

    **Important:** You must not change the names of the downloaded files. You must upload the files as is to your ServiceNow instance.

4.  From the navigation menu, select **Identity**.

    The Azure portal for the current tenant opens.

5.  On the Overview page, copy the value in the **Tenant ID** field.

    Save the Tenant ID in a secure location for later use.

6.  From a web browser, open your ServiceNow instance.

<table id="choicetable_yzk_rml_bcc"><thead><tr><th align="left" id="d110174e2133">

Interface

</th><th align="left" id="d110174e2136">

Action

</th></tr></thead><tbody><tr><td id="d110174e2142">

**Core UI**

</td><td>

Open the Integration Profiles \[samp\_sw\_subscription\_profile\] table.Integration profiles open in the list view.

</td></tr><tr><td id="d110174e2153">

**Software Asset Workspace**

</td><td>

1.  Navigate to **Workspaces** &gt; **Software Asset Workspace** &gt; **License operations**.
2.  Under **User subscription**, select **Direct integration profiles**.
 Integration profiles open in the list view.

</td></tr></tbody>
</table>7.  Apply filters to open integration profiles for a specific Tenant id for which you want to upload the usage reports.

<table id="choicetable_np5_wnl_bcc"><thead><tr><th align="left" id="d110174e2202">

Interface

</th><th align="left" id="d110174e2205">

Action

</th></tr></thead><tbody><tr><td id="d110174e2211">

**Core UI**

</td><td>

1.  Select the Show/hide filter icon on the table header.
2.  Set the condition **\[Tenant name or id\] \[is\] \[Tenant ID copied in step 5\] AND \[Profile type\] \[is\] \[Microsoft 365\]**.
3.  Select **Run**.


</td></tr><tr><td id="d110174e2238">

**Software Asset Workspace**

</td><td>

1.  Select the filter icon and then select **Advanced view**.
2.  Set the condition **\[Tenant name or id\] \[is\] \[Tenant ID copied in step 5\]**.
3.  Add a filter condition by selecting **+ New condition set**.
4.  Set the condition **\[Profile type\] \[is\] \[Microsoft 365\]**.
5.  Select **Update**.


</td></tr></tbody>
</table>8.  Add the usage reports to an integration profile.

<table id="choicetable_my4_mcm_bcc"><thead><tr><th align="left" id="d110174e2290">

Interface

</th><th align="left" id="d110174e2293">

Action

</th></tr></thead><tbody><tr><td id="d110174e2299">

**Core UI**

</td><td>

1.  Select an integration profile.
2.  Select the Manage Attachments \(![](../../contract-management/image/attachments-icon.png)\) icon on the form header.
3.  In the Attachments dialog box, select **Choose file**.
4.  Select all the CSV files that you downloaded in step 3 to add them to the integration profile.
5.  Close the dialog box to return to the Integration Profile form.
6.  The uploaded CSV files appear next to the Manage Attachments icon.


</td></tr><tr><td id="d110174e2338">

**Software Asset Workspace**

</td><td>

1.  Select an integration profile.
2.  Select the Attachment \(![](../../contract-management/image/attachments-icon.png)\) icon from the sidebar of the integration profile.
3.  In the Attachments window, select **Select file**.
4.  Select all the CSV files that you downloaded in step 3 to add them to the integration profile.
5.  The uploaded CSV files appear in the Attachment window.


</td></tr></tbody>
</table>
### What to do next

The usage activity reports that you upload can be monitored for license optimization and generation of reclamation candidates. For details, see [Evaluating software usage activity for Microsoft 365 subscriptions](integrate-with-microsoft.md#).

## Evaluating software usage activity for Microsoft 365 subscriptions

Evaluate software usage activity to discover active, inactive, and unassigned subscriptions among all subscriptions found on the Microsoft 365 portal.

Software usage activity is the usage of software products and you can monitor license usage by tracking the software usage activity. Monitoring the software usage activity also helps you optimize your existing software subscriptions.

The following table lists the sources for collecting the software usage activity, the associated platform support, and the supported Microsoft 365 products.

|Sources of software usage activity collection|Platform support|Supported Microsoft Office 365 products|
|---------------------------------------------|----------------|---------------------------------------|
|Microsoft Graph APIs|Desktop, Web, Mobile|Outlook, Word, PowerPoint, Excel, OneNote, Teams, Exchange Online, SharePoint Online, Power BI|
|Microsoft SCCM or ACC-V|Desktop|Microsoft Office 365 apps for Enterprise|
|Jamf for macOS devices|Desktop|Microsoft Office 365 apps for Enterprise|
|Manual upload of the usage reports on the ServiceNow instance from the Microsoft Office 365 admin center|Desktop, Web, Mobile|Microsoft 365 Copilot, Visio Online, and Project Online|

**Note:** You can download the usage for Microsoft 365 Copilot, Visio Online, and Project Online from the Microsoft Office 365 admin center. For details, see [Upload the Microsoft 365 Copilot, Visio Online, and Project Online usage reports to your ServiceNow instance](integrate-with-microsoft.md#).

### Monitoring software usage activity for license optimization

Based on the software usage activity, Software Asset Management generates optimization recommendations for your software subscriptions that include the following:

-   Downgrades from Microsoft 365 E5 to E3 and E3 to E1
-   Consolidated Microsoft 365 subscriptions for multiple licenses. For example, if you have both Office 365 Enterprise E5 and Microsoft 365 Enterprise E3 subscriptions, a single license can be a recommended to cover multiple products.
-   Double licensed users with both Microsoft 365 and its applications \(Office 365, Enterprise Mobility+Security \(EMS\), Windows\) subscriptions
-   Individual subscriptions for Microsoft Teams, Microsoft Exchange Online, Microsoft SharePoint Online, Microsoft OneDrive, and Power BI
-   Unassigned user subscriptions

You can view the optimization recommendations on the [Optimization and savings dashboard in workspace](../reference/optimization-dashboard-workspace.md).

After completing the Microsoft 365 integration, you can view the usage activity information using any of the following tables:

-   Software Usages \[samp\_sw\_usage\]

    View the usage data for individual software products within the subscription in the Software Usages table. This table stores total usage and last activity retrieved from Microsoft APIs and other discovery solutions such as SCCM, Jamf, and ACC-V. The  **SAM - Collect Microsoft 365 Usage ** scheduled job collects the usage data daily and the  **SAM - Create New Reclamation Candidates for Office 365 Integration ** generates the removal candidates weekly. For more details on software usage fields and their descriptions, see [View or create software usage in workspace](../task/view-sw-usage-workspace.md).

    The Software Usages table includes the date when the software was last used and the type of the activities performed on the Desktop, Web, Mobile, or cumulative across platforms. The last activity data helps you select an optimized plan for individual products within your Microsoft 365 subscriptions. Software Asset Management generates a removal candidate for the current subscription by showing an optimized recommendation on the License workbench.

-   Microsoft 365 Apps Usage Reports \[samp\_m365\_apps\_usage\_report\]

    View the last activity date for the Microsoft 365 products in the Microsoft 365 Apps Usage Reports table for each user. This table stores usage data for Microsoft 365 products in True or False retrieved from Microsoft APIs only. The last activity date helps you determine reclamation candidates more accurately for Microsoft 365 products, including Microsoft Outlook, Microsoft Word, Excel Microsoft PowerPoint, and OneNote. For more details on Microsoft 365 apps usage fields and their descriptions, see [Microsoft 365 Apps Usage Reports](../reference/m365-apps-usage-report.md).


### License optimization for Microsoft subscriptions

Software usage activity helps you with license optimization by discovering reclamation candidates from both the individual Microsoft products and the Microsoft 365 suite subscriptions. You can determine the reclamation candidates using both APIs and discovery solutions.

-   Downgrades from Microsoft 365 E5 to E3 and E3 to E1: Determine the number of licenses per month that can be downgraded or reclaimed based on generated downgrade candidates.

    **Note:** You can also determine usage for Microsoft Access and Publisher from additional discovery solutions, such as Microsoft SCCM or ACC-V for E3 to E1 optimization.

-   Consolidated Microsoft 365 subscriptions: Find Microsoft 365 consolidate subscriptions reclamation candidates.
-   Double licensed users: Determine the number of licenses per month that can be downgraded or reclaimed based on recommended candidates with both Microsoft 365 and its applications \(Office 365, Enterprise Mobility+Security \(EMS\), Windows\) subscriptions.
-   Individual subscriptions: Reclamation rules are automatically created for individual subscriptions when the **SAM - Import user subscription** scheduled job runs. These individual subscriptions include Microsoft Teams, Microsoft Exchange Online, Microsoft SharePoint Online, Microsoft OneDrive, and Power BI. You can review the reclamation rules for individual subscriptions to fit your requirements. For more details, see [Review a software reclamation rule](../task/add-reclamation-rule-sub.md).

Additionally, the subscription assignment date that is automatically populated from the Microsoft 365 portal helps in generating the reclamation candidates for individual subscriptions. Using the subscription assignment date instead of the record creation date on the ServiceNow AI Platform helps to create correct reclamation candidates based on the actual use from the Microsoft 365 portal.

**Related topics**  


[Reclamation rules for Microsoft 365 integration](../reference/m365-reclamation-rules.md)

## Evaluate Microsoft 365 compliance and optimization results

Evaluate Microsoft 365 compliance and optimization results to find actual and potential cost savings and recommended licensing optimizations.

### Before you begin

Role required: sam\_admin or sam\_user

The discovery of Microsoft 365 must be complete to evaluate the software compliance. For more information about using Discovery and Microsoft SCCM together, see [Discovery and SCCM together](https://www.servicenow.com/docs/access?context=c_DiscoveryAndSCCMTogether&version=xanadu&pubname=xanadu-it-operations-management&ft:locale=en-US).

The usage of Microsoft 365 plans must be available from both Microsoft certified APIs and Microsoft SCCM to evaluate the software optimization.

### Procedure

1.  Navigate to **Software Asset Workspace** &gt; **License operations**.

2.  In the left pane, select **Licensing** &gt; **Software entitlements**.

3.  Select **New**.

4.  Create entitlements for Microsoft 365 by selecting the correct Publisher Part Number \(PPN\) to verify compliance.

    For more information about creating entitlements, see [Create entitlements in workspace](../task/create-entitlements-workspace.md).

    **Note:** Ensure that the License metric value is User Subscription.

5.  Navigate to **License usage** in the left pane.

6.  Select the **Reconciliation** tab.

7.  Select **Run reconciliation**.

8.  View compliance analysis results in [Office 365 &amp; Adobe Cloud dashboard in Software Asset Management classic](sam-saas-subscription-dash.md) and [SaaS overview dashboard in workspace](../reference/saas-dashboard-workspace.md).

    For more information about running software reconciliation, see [Run software reconciliation](../task/t_RunReconciliation.md) and [Run Software Asset Management Foundation plugin software reconciliation in classic](https://www.servicenow.com/docs/access?context=t_RunReconciliationSAMF&version=xanadu&pubname=xanadu-it-service-management&ft:locale=en-US).

9.  View all optimized plans for Microsoft 365 subscription on the [Optimization and savings dashboard in workspace](../reference/optimization-dashboard-workspace.md).


## Update REST and OAuth endpoints for Microsoft Office 365 Government plans

Change the endpoints of the REST message and OAuth application on your ServiceNow subscription profile so that you can use your subscriptions.

### Before you begin

Role required: sam\_admin

### About this task

The ServiceNow AI Platform® supports Microsoft Office 365 Government plans, which provide all the features and capabilities of Microsoft 365 services in a segmented government cloud community that enables organizations to meet U.S. compliance and security standards.

For more information on Microsoft Office 365 Government plans, see [Office 365 Government](https://docs.microsoft.com/en-us/office365/servicedescriptions/office-365-platform-service-description/office-365-us-government/office-365-us-government).

**Important:** The Software Asset Management application supports tracking last activity for license compliance, subscription management, and optimization recommendations for Microsoft products such as Exchange Online, Teams, Power BI, OneDrive, and so on. For more details, see [Evaluating software usage activity for Microsoft 365 subscriptions](integrate-with-microsoft.md#).

The detailed usage metrics for these Microsoft products \(except Power BI\) are only available through specific report APIs that aren't supported in government-regulated environments. For further details, refer to the [Microsoft national cloud deployments documentation](https://learn.microsoft.com/en-us/graph/api/reportroot-getm365appuserdetail?view=graph-rest-1.0&tabs=http).

### Procedure

1.  From your ServiceNow instance, navigate to **All** &gt; **Software Asset** &gt; **SaaS License** &gt; **Direct Integration Profiles**.

2.  Select the Microsoft 365 integration profile that you want to update.

3.  On the Integration Profile record, select the Preview this record icon \(![Preview this record icon.](../image/preview-icon.png)\) next to the **REST message** field.

4.  On the record preview, select **Open Record**.

    The REST Message record opens.

5.  Update the REST message endpoints on your Microsoft 365 integration profile.

    REST message endpoints enable you to retrieve usage data from your Microsoft 365 applications and services.

    1.  In the **HTTP Methods** related list, update the REST message endpoints based on your needs.

        Microsoft provides various endpoints for Microsoft Office 365 Government plans. For more information on the available endpoints, see [Office 365 U.S. Government GCC High endpoints](https://docs.microsoft.com/en-us/microsoft-365/enterprise/microsoft-365-u-s-government-gcc-high-endpoints?view=o365-worldwide).

        **Important:** You must change the `.com` to `.us` in the URL of each endpoint. For example, you must change `https://graph.microsoft.com/v1.0/reports` to `https://graph.microsoft.us/v1.0/reports`.

    2.  Select **Save**.

    3.  Update the OAuth entity scope for the **GET PowerBI Usage** endpoint.

        The OAuth entity scope specifies the level of access that users have to your protected resources.

        1.  Select the **GET PowerBI Usage** endpoint.

            The HTTP Method record opens.

        2.  In the Authentication section of the HTTP Method record, select the Preview this record icon \(![Preview this record icon.](../image/preview-icon.png)\) next to the **OAuth profile** field.
        3.  On the record preview, select **Open Record**.

            The OAuth Entity Profile record opens.

        4.  In the OAuth Entity Profile Scopes list, update the **OAuth scope** field of the **PowerBIPermissions** OAuth entity scope with the backend API URL that you are using for Microsoft Power BI.

            **Note:** Microsoft supports various backend API URLs for Power BI. For more information on the available URLs, see [Power BI for US Government](https://learn.microsoft.com/en-us/power-bi/enterprise/service-govus-overview).

        5.  Select **Update**.

            The OAuth Entity Profile record closes and you automatically return to the REST Message record.

6.  Update the OAuth application endpoint on your Microsoft 365 integration profile.

    The OAuth application endpoint enables your ServiceNow instance to access your Microsoft 365 subscription data.

    1.  In the Authentication section of the REST Message record, select the Preview this record icon \(![Preview this record icon.](../image/preview-icon.png)\) next to the **OAuth profile** field.

    2.  On the record preview, select **Open Record**.

        The OAuth Entity Profile record opens.

    3.  In the OAuth Entity Profile Scopes list, change the `.com` to `.us` in the URL that is listed in the **OAuth scope** field of the **Permissions** OAuth entity scope.

    4.  Select the Preview this record icon \(![Preview this record icon.](../image/preview-icon.png)\) next to the **OAuth provider** field.

    5.  On the record preview, select **Open Record**.

        The Application Registries record opens.

    6.  Select the Edit URL icon \(![Edit URL icon.](../../../common/image/icon-lock.png)\) next to the **Token URL** field.

    7.  In the URL, change the `.com` to `.us`.

        For example, change `https://login.microsoftonline.com` to `https://login.microsoftonline.us`.

    8.  Select the Lock URL icon \(![Lock URL icon.](../image/unlock-icon.png)\).

    9.  Select **Update**.


## Associate a user with subscription records

If the User field in the Software Subscription \[samp\_sw\_subscription\] table is empty, map the field with an associated user.

### Before you begin

ServiceNow Role required: admin

### About this task

SaaS integrations create subscription records in the Subscriptions \[samp\_sw\_subscription\] table. The fields on this table are populated by automated jobs and integrations. The User field is resolved based on the User principal name column value and verified against the **email** and **user\_name** fields of the User \[sys\_user\] table by default.

### Procedure

1.  To map the user data effectively, perform one of the following steps:

    -   Update the User field on subscriptions manually.

        By default, the integration overwrites the **User** field even if you set a value.

        1.  Update the **User** field of the subscription record manually to overwrite the User column value that is automatically set by the integration.

            After you update the value, the integration doesn't reset the value.

        2.  If you want to switch back to the user logic of the integration, clear the **User** field value.

            After you clear the value, the next integration execution repopulates the **User** field automatically.

    -   Modify the user lookup logic for SaaS subscriptions.

        If you have a different column for the user lookup, you might want to use it for lookup instead of the base system lookup.

        1.  Open the Script include `SAMSaasIntegrationUtils`.
        2.  Replace the getSysUser method call with the following script and your field name in the sys\_user table to replace the &lt;replace\_field\_name&gt;.

            ```
            getSysUser: function (upn) { 
            if (upn) { 
                        var userGr = new GlideRecord('sys_user');
                        userGr.addActiveQuery(); 
                        userGr.addNotNullQuery('<replace_field_name>');
                        userGr.addQuery('<replace_field_name>', upn);
                        userGr.setLimit(1); 
                        userGr.query(); 
                        if (userGr.next()) { 
                                    return userGr;
                         } 
                           }
                             }
            ```


