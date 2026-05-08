---
title: Integrating with SAP S/4HANA Cloud Public Edition
description: Integrating your Software Asset Management application with the SAP S/4HANA Public Cloud application enables you to track your software subscriptions and optimize licenses.Create a communication system and an inbound user to enable access to the SAP S/4HANA Public Cloud API and receive a user name and password for basic authentication.Create a communication arrangement to enable access to the SAP S/4HANA Public Cloud API.Create an SAP S/4HANA integration profile to track software subscriptions and optimize licensing for your SAP S/4HANA applications.
locale: en-US
release: australia
product: SaaS License Management
classification: saas-license-management
topic_type: concept
last_updated: "2026-03-12"
reading_time_minutes: 7
breadcrumb: [Integrate with SaaS applications, SaaS License Management, Software Asset Management, IT Asset Management]
---

# Integrating with SAP S/4HANA Cloud Public Edition

Integrating your Software Asset Management application with the SAP S/4HANA Public Cloud application enables you to track your software subscriptions and optimize licenses.

**Important:**

You must request and install the following applications from [ServiceNow Store](https://store.servicenow.com/sn_appstore_store.do#!/store/home):

-   SaaS License Management plugin \(com.sn\_sam\_saas\_int\)
-   Software Asset Management Professional for SAP plugin \(com.sn\_samp\_sap\)
-   SAP S/4HANA Spoke plugin \(sn\_s4\_hana\_cld\_spk\)
-   Software Asset Management integration with SAP S/4HANA plugin \(sn\_sam\_s4hanacloud\)

Minimize security risks and protect information by granting access only to the necessary user or API permissions.

|Process|Required user role in the SAP S/4HANA application|Authentication scopes|
|-------|-------------------------------------------------|---------------------|
|Download subscriptions|Business user|users:read|

## Create a communication system and user for SAP S/4HANA Public Cloud

Create a communication system and an inbound user to enable access to the SAP S/4HANA Public Cloud API and receive a user name and password for basic authentication.

### Before you begin

The SAP S/4HANA Public Cloud Integration Hub spoke must be active. For more information, see [SAP S4 HANA Public Cloud Spoke](https://www.servicenow.com/docs/access?context=sap-s4-hana-cloud-spk&version=australia&pubname=australia-integrate-applications&ft:locale=en-US).

SAP S/4HANA Role required: Business user

### Procedure

1.  Log in to the SAP Fiori launchpad using your business user credentials.

2.  From the Communication Management catalog, select the **Communication Systems** application.

3.  Select **New**.

4.  In the **New Communication System** window, enter a unique system ID in the **System ID** field.

    For example, `SAP S/4HANA Cloud source system`.

5.  Enter a unique name for the communication system in the **System Name** field.

    For example, `Integration_System_SNOW`.

6.  Select **Create**.

    The system ID and system name that you created appear in the corresponding fields in the General tab.

7.  In the Technical Data section, enter the host name of the SAP S/4HANA Cloud source system in the **Host Name** field.

    For example, `localhost`.

8.  Select the **Users for Inbound Communication** tab.

9.  Create an inbound communication user, by selecting the **+** button.

10. In the New Inbound Communication User window, select **User Name and Password** in the **Authentication Method** field.

11. Select **New User**.

12. In the Create Communication User window, enter the appropriate values in the **User Name**, **Description**, and **Password** fields.

13. Select **Create**.

    You’re redirected to the New Inbound Communication User window.

14. Select **OK**.

    The new user appears in the list of Users for Inbound Communication.

    **Important:** There are a few communication arrangements that require a user for outbound communication even if you're using it for inbound communication only. You can create a dummy user for outbound communication from the Users for Outbound Communication tab.

15. Select **Save**.


## Create a communication arrangement for SAP S/4HANA Public Cloud

Create a communication arrangement to enable access to the SAP S/4HANA Public Cloud API.

### Before you begin

SAP S/4HANA Role required: Business user

### Procedure

1.  Log in to the SAP Fiori launchpad using your business user credentials.

2.  From the Communication Management catalog, select the **Communication Arrangements** application.

3.  Select **New**.

4.  In the New Communication Arrangement window, select **SAP\_COM\_0889** as the communication scenario.

    For information on communication scenarios for the specific APIs, see [SAP S/4HANA Public Cloud APIs](https://api.sap.com/products/SAPS4HANACloud/apis/packages).

5.  Enter a unique communication arrangement name in the **Arrangement Name** field.

6.  Select **Create**.

7.  In the **Communication System** field under the Common Data section, select the communication system you created earlier.

    For example, `Integration_System_SNOW`.

    The **User Name** field for the selected communication system and the **Authentication Method** field associated with the communication scenario get automatically populated.

8.  Select **Save**.


## Create an SAP S/4HANA integration profile

Create an SAP S/4HANA integration profile to track software subscriptions and optimize licensing for your SAP S/4HANA applications.

### Before you begin

The Software Asset Management - SaaS License Management plugin \(sn\_sam\_saas\_int\) must be installed from the [ServiceNow Store](https://store.servicenow.com/).

For publishing the integration profile, change the application scope to **Global**.

ServiceNow Role required: sam\_integrator

**Important:** You must select the **Software Asset Management integration with SAP S4Hana Cloud** check box for this integration while installing optional features on the [Application Manager](https://www.servicenow.com/docs/access?context=application-manager&version=australia&pubname=australia-platform-administration&ft:locale=en-US) page. For more information about choosing the required SaaS applications, see [Request SaaS License Management](../task/request-saas-license-management.md).

### About this task

If you’re using Software Asset Workspace, the option to create the SAP S/4HANA integration profile in Core UI is inactive.

### Procedure

1.  Navigate to the integration profile.

<table id="choicetable_o3p_z3k_qtb"><thead><tr><th align="left" id="d52775e658">

Interface

</th><th align="left" id="d52775e661">

Action

</th></tr></thead><tbody><tr><td id="d52775e667">

**Core UI**

</td><td>

1.  Navigate to **All** &gt; **Software Asset** &gt; **SaaS License** &gt; **Direct Integration Profiles**.
2.  Select **New**.
3.  Select **SAP S4Hana Cloud Integration Profile**.


</td></tr><tr><td id="d52775e709">

**Software Asset Workspace**

</td><td>

1.  Navigate to **License operations** &gt; **User Subscription** &gt; **Direct integration profiles**.
2.  Select **New**.
3.  Select **SAP S4Hana Cloud** from the drop-down list.
4.  Select **Continue**.


</td></tr></tbody>
</table>2.  On the form, fill in the fields.

<table id="table_yrz_yrr_gdc"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Display name

</td><td>

Name of the integration profile. For example, `SAP S/4HANA Cloud`.

</td></tr><tr><td>

Status

</td><td>

Status of the integration profile. -   If you have not published the integration profile, this field is automatically set to **Draft**.
-   If you have already published the integration profile, this field is automatically set to **Published**.


</td></tr><tr><td>

Profile type

</td><td>

Type of integration profile. This field is automatically set to **SAP S4Hana Cloud Subscription**.

</td></tr></tbody>
</table>3.  Review the required user roles or API permissions specified in the **Vendor configuration** field for each process to minimize security risks and optimize SaaS licenses.

    For more information about the required roles and scopes, see [Minimal user permissions table](integrate-with-hana.md#).

4.  In the Download Subscription Subflow section, verify that the **Subflow** field is set to **SAP S4Hana Public Cloud Download Subscriptions**.

    **Note:** The **Download subscriptions** check box is selected by default and you can't clear it.

5.  Select **Save**.

    A draft integration profile is created.

    The **Connection &amp; Credential** field appears and is automatically set to **sn\_s4\_hana\_cld\_spk.SAP\_S4\_HANA\_Cloud**.

6.  Open the connection &amp; credential aliases record by selecting the preview icon ![](../image/preview-icon.png) beside the **Connection &amp; Credential** field.

7.  Select **Open Record** in the record preview.

8.  Select the **Create New Connection &amp; Credential** related link.

9.  On the form, fill in the fields.

    |Field|Description|
    |-----|-----------|
    |Connection Name|A unique name for the connection. For example, `SAP S4 HANA Cloud`.|
    |Connection URL|The URL to connect to the SAP S/4HANA public cloud instance. For example, `https://demo.s4hana.cloud.sap`.|
    |User Name|User name for the credential record.|
    |Password|Password for the credential record.|

10. Select **Create**.

11. On the Integration Profile form, select **Validate Connection** to verify the connection and credential details of this integration.

12. Select **Publish**.

13. In the Publish Confirmation dialog box, select **OK**.

    After the integration profile is published, it appears in the Direct Integration Profiles list.


### What to do next

After the integration connects, your ServiceNow instance automatically creates software models and software subscriptions that are refreshed daily.

After creating an integration profile, view information about the profile in the Software Asset Workspace by navigating to **License operations** &gt; **User subscription** &gt; **Direct integration profiles**. You can select an integration profile to view the following related lists. If all of the following related lists aren't visible for an integration profile in the default view, you can select the custom integration view from the Details tab:

-   Software Models
-   Unrecognized Subscription Identifiers
-   Scheduled Jobs
-   Scheduled Job Results
-   Software Subscriptions
-   Subscription Identifier Exclusion Rule
-   Subscription User Exclusion Rule

If you want to set up multiple integration profiles with unique connections, create child aliases to manage different configurations and settings for each integration profile. For more information, see [Create a child alias to set up multiple integration profiles](../reuse/create-child-alias-saas.md).

Create software entitlements for the automatically generated software models to track used software against owned software.

-   For more information on creating software entitlements in the Software Asset Management Core UI, see [Create entitlements in Software Asset Management classic](../task/track-software-rights.md).
-   For more information on creating software entitlements in the Software Asset Workspace, see [Create entitlements in workspace](../task/create-entitlements-workspace.md).
-   For more information on creating software entitlements using the Software Asset Management Playbook, see [Create entitlements using the guided walk-through](../task/guidedwalk-workspace.md).

