---
title: Integrate with Workday using Basic Authentication
description: Integrate your Software Asset Management application with the Workday application using Basic authentication method to track your software subscriptions.To set up the Workday integration successfully, perform this procedure in Workday.Create a Workday integration profile to track software subscriptions and optimize licensing for your Workday applications.
locale: en-US
release: yokohama
product: SaaS License Management
classification: saas-license-management
topic_type: concept
last_updated: "2026-02-26"
reading_time_minutes: 8
breadcrumb: [Integrating with Workday, Integrate with SaaS applications, SaaS License Management, Software Asset Management, IT Asset Management]
---

# Integrate with Workday using Basic Authentication

Integrate your Software Asset Management application with the Workday application using Basic authentication method to track your software subscriptions.

## Configure permissions in Workday

To set up the Workday integration successfully, perform this procedure in Workday.

### Before you begin

Role required: Users having roles such as Security Admin, Integration Admin, Integration Auditor, who can create Integration System Users and assign required security policies.

### Procedure

1.  Register an Integration System User.

    **Note:** While filling out account information details, you must select the **Do Not Allow UI Sessions** check box.

2.  Create a security group and assign it to the Integration System User.

    1.  In **Action**, navigate to **Security Group** &gt; **Maintain Domain Permissions for Security Group** and provide the following permission:

        |Operation|Domain Security Policy|Functional Areas|
        |---------|----------------------|----------------|
        |Get Only|Worker Data: Current Staffing Information|Staffing|
        |Get Only|Worker Data: Workers|Staffing|

        **Note:** Confirm that the domain security policies are activated for the security group using the active pending security policy changes.


### Result

The new credentials for this Integration System User would be used to configure the connection in the ServiceNow instance.

## Create a Workday integration profile

Create a Workday integration profile to track software subscriptions and optimize licensing for your Workday applications.

### Before you begin

Role required: admin, sam\_admin, sam\_integrator

Install the latest Workday HR spoke. For more information about the latest version, see the **Spoke version** section in [Workday HR Spoke](https://www.servicenow.com/docs/access?context=workday-hr-spoke&version=yokohama&pubname=yokohama-integrate-applications&ft:locale=en-US).

**Important:** You must select the **Software Asset Management integration with Workday** check box for this integration while installing optional features on the [Application Manager](https://www.servicenow.com/docs/access?context=application-manager&version=yokohama&pubname=yokohama-platform-administration&ft:locale=en-US) page. For more information about choosing the required SaaS applications, see [Request SaaS License Management](../task/request-saas-license-management.md).

### About this task

If you’re using Software Asset Workspace, the option to create the Workday integration profile in Core UI is inactive.

### Procedure

1.  Navigate to the integration profile.

<table id="choicetable_o3p_z3k_qtb"><thead><tr><th align="left" id="d218935e327">

Interface

</th><th align="left" id="d218935e330">

Action

</th></tr></thead><tbody><tr><td id="d218935e336">

**Core UI**

</td><td>

1.  Navigate to **All** &gt; **Software Asset** &gt; **SaaS License** &gt; **Direct Integration Profiles**.
2.  Select **New**.
3.  Select **Workday Integration Profile**.


</td></tr><tr><td id="d218935e378">

**Software Asset Workspace**

</td><td>

1.  Navigate to **License operations** &gt; **User Subscriptions** &gt; **Direct integration profiles**.
2.  Select **New**.
3.  Select **Workday** from the drop-down list.
4.  Select **Continue**.


</td></tr></tbody>
</table>2.  On the form, fill in the fields.

<table id="table_qnq_djt_ysb"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td colspan="2">

Integration Profile

</td></tr><tr><td>

Display name

</td><td>

Name of the integration profile. For example, `Workday integration`.

</td></tr><tr><td>

Authentication type

</td><td>

Type of authentication to access Workday APIs.-   Basic Auth
-   OAuth 2.0


</td></tr><tr><td>

Status

</td><td>

Status of the integration profile. -   If you haven’t published the integration profile, this field is automatically set to  **Draft**.
-   If you’ve already published the integration profile, this field is automatically set to  **Published**.


</td></tr><tr><td>

Profile type

</td><td>

Type of integration profile. This field is automatically set to **Workday Subscription**.

</td></tr></tbody>
</table>3.  Review the required user roles or API permissions specified in the **Vendor configuration** field for each process to minimize security risks and optimize SaaS licenses.

    **Note:** For more information, see [Minimal user permissions](integrate-with-workday.md) table.

    In the Download Subscription Subflow section, verify that the **Subflow** field is set to **Workday Download Subscriptions**. The **Download subscriptions** check box is selected by default and you can't clear it.

4.  Select **Save**.

    The Connection Setup section is displayed on the integration profile.

<table id="table_cyv_lyq_m3c"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Connection Details

</td><td>

-   If the connection details exist, this field is already populated.
-   If the connection details don't exist, you must create them.


</td></tr><tr><td>

SOAP Username

</td><td>

User name of the Integration system user created while [configuring permissions in Workday.](integrate-with-workday-basicauth.md#)**Important:** Include the tenant suffix in the username. For example, `username@<tenant>`.

</td></tr><tr><td>

SOAP Password

</td><td>

Password of the Integration system user created while [configuring permissions in Workday](integrate-with-workday-basicauth.md#).

</td></tr></tbody>
</table>5.  If connection details don't exist, create the connection details.

    |Interface|Action|
    |---------|------|
    |**Core UI**|In the **Connection Details** field, select the search icon \(![Search icon.](../image/search-icon.png)\).|
    |**Software Asset Workspace**|Select the **Connection details** link.|

    1.  Select **New**.

    2.  On the form, fill in the fields.

        |Field|Description|
        |-----|-----------|
        |Base URL|Workday SOAP API URL with the tenant name in the following format: `https://<workday_host_url>/ccx/service/<workday_tenant_name>`.|
        |Version|The SOAP API version, for example, `v33.2`.|
        |Webservice Type|Should be set to **SOAP**.|

    3.  Select **Submit**.

        A record is created and added in the **Connection Details** field.

    4.  Review the connection details by selecting the new integration profile and selecting the lookup icon ![Lookup icon](../image/search-icon.png) in the **Connection details** field.

6.  Create a SOAP user name and password when you don't have these credentials automatically populated.

    **Note:** Only an admin role can create or update the SOAP user name and password.

<table id="choicetable_rhj_5w1_stb"><thead><tr><th align="left" id="d218935e870">

Interface

</th><th align="left" id="d218935e873">

Action

</th></tr></thead><tbody><tr><td id="d218935e879">

**Core UI**

</td><td>

1.  Navigate to **All** &gt; **System Web Services** &gt; **SOAP Security Policies**.
2.  Select **All** in the top menu bar.
3.  Select **WorkdayHR**.


</td></tr><tr><td id="d218935e918">

**Software Asset Workspace**

</td><td>

Select the **SOAP username profile** link.

</td></tr></tbody>
</table>    1.  On the Soap Security Policy form, select the lookup icon ![Lookup icon](../image/search-icon.png) in the **WS-Security Username Profile** field.

    2.  Select **New**.

    3.  On the WS-Security Username Profiles \(Outbound\) form, fill in the name, user name, and password for the integration profile.

    4.  Select **Submit**.

7.  Select **Save**.

8.  Under the **FSE worker calculation** tab, activate the worker categories covered by your contract by setting the value of **Active** to **true** and entering the FSE percentage.

9.  If worker categories are listed in your contract but not available in the FSE worker calculation tab, add a new worker category.

    1.  In the **FSE worker calculation** tab, select **New**.

    2.  On the form, fill in the fields.

        |Field|Description|
        |-----|-----------|
        |Worker Category|The worker category listed in your contract.|
        |FSE Percentage|The FSE percentage for the worker category that you added. Full Service Equivalent \(FSE\) is the method by which the subscriptions are calculated.|
        |Integration profile|The Workday integration profile that you created.|
        |Active|Option to make the worker category active.|

    3.  Select **Submit**.

10. Define the mapping of the newly created worker category.

    1.  Select the **Worker category** tab and select **New**.

    2.  On the form, fill in the fields:

        |Field|Description|
        |-----|-----------|
        |Worker Type|The type of worker, either Employee or Contingent.|
        |Employee/Contingent worker type|The type of Employee or Contingent worker.|
        |Time Type|Indicates whether the worker is full-time or part-time.|
        |Worker Category|The worker category that you created.|
        |Integration profile|The Workday integration profile that you created.|
        |Active|Option to make the mapping active.|

    3.  Select **Submit**.

11. Activate the list of modules that are defined in your contract.

    1.  Select the **Modules** tab.

    2.  Open the module record.

    3.  Set the **Active** field to **True**.

    4.  Select **Save**.

12. Verify that there is at least one active record in all the tabs for your contract: FSE worker calculation, Worker category, and Modules, before publishing the connection.

13. On the integration profile form, select **Validate Connection** to verify the connection and credential details of this integration.

14. After the connection is verified, select **Publish**.

15. In the Publish Confirmation dialog box, select **OK**.


### What to do next

After the integration connects, your ServiceNow instance automatically creates software models, reclamation rules, and software subscriptions that are refreshed daily.

If you want to set up multiple integration profiles with unique connections, create child aliases to manage different configurations and settings for each integration profile. For more information, see [Create a child alias to set up multiple integration profiles](../reuse/create-child-alias-saas.md).

Review all automatically generated reclamation rules to reclaim user subscriptions. For more information, see [Review a software reclamation rule](../task/add-reclamation-rule-sub.md).

Create software entitlements for the automatically generated software models to track used software against owned software.

-   For more information on creating software entitlements in the Software Asset Management Core UI, see [Create entitlements in Software Asset Management classic](../task/track-software-rights.md).
-   For more information on creating software entitlements in the Software Asset Workspace, see [Create entitlements in workspace](../task/create-entitlements-workspace.md).
-   For more information on creating software entitlements using the Software Asset Management Playbook, see [Create entitlements using the guided walk-through](../task/guidedwalk-workspace.md).

Reconciliation also runs on your subscriptions as a scheduled job or on-demand. You can view your reconciliation results in the [License Workbench](sam-license-workbench.md) \(Software Asset Management classic application\) or the [License usage view](sam-workspace-workbench.md) \(Software Asset Workspace\). Use these results to determine your license compliance position and to remediate any non-compliance.

-   For more information on running reconciliation in the Software Asset Management classic application, see [Run software reconciliation in Software Asset Management classic](../task/t_RunReconciliation.md).
-   For more information on running reconciliation in the Software Asset Workspace, see [Run software reconciliation in the workspace](../task/run-recon-workspace.md).

