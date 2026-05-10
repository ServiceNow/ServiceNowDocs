---
title: Get User Info Azure AD activity
description: The Get User Info activity returns the named user's information from the Azure Active Directory.
locale: en-US
release: australia
product: Orchestration
classification: orchestration
topic_type: reference
last_updated: "2026-03-12"
reading_time_minutes: 1
breadcrumb: [Azure AD activity pack, Orchestration activity packs, Classic Orchestration, ServiceNow AI Platform Additional Capabilities, Extend ServiceNow AI Platform capabilities]
---

# Get User Info Azure AD activity

The Get User Info activity returns the named user's information from the Azure Active Directory.

To access this activity in the Workflow Editor, select the **Custom** tab, and then navigate to **Custom Activities** &gt; **Azure AD**. This activity was built with the [REST web service activity template](../../orchestration-activity-designer/task/t_CreateARESTWebServiceActivity.md#).

**Important:** The REST message used for this activity must be configured to use [OAuth 2.0](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/platform-security/authentication/c_OAuthApplications.md).

## Input variables

<table id="table_nh4_gmx_45"><thead><tr><th>

Variable

</th><th>

Description

</th></tr></thead><tbody><tr><td>

user\_id

</td><td id="e_ObjectIDDesc">

The object ID \(GUID\) or the user principal name of the target user. An example of a user principal name is **someuser@a830edad9050849NDA1.onmicrosoft.com** **Note:** Version 2 of this activity enforces input validation. If empty, the following message appears: "Mandatory input 'user\_id' is empty"

.

</td></tr></tbody>
</table>## Output variables

<table id="table_mr4_jmx_45"><thead><tr><th>

Variable

</th><th>

Description

</th></tr></thead><tbody><tr><td>

error

</td><td>

Returns the error string from the REST message. If there are no errors, this variable returns a null value.

</td></tr><tr><td>

body

</td><td>

Contains a string value representing the output from the REST message.

</td></tr><tr><td>

status\_code

</td><td>

Contains the status code returned from the Web service.

</td></tr><tr><td>

user\_info

</td><td>

The **user\_info** array contains attributes that can be leveraged by other activities as inputs. For example, the user **objectid** output \(GUID\) can be passed to the Add User to Group activity as the **user\_id** input.-   **objectid**: User's Azure AD identifier.
-   **accountEnabled**: Boolean variable indicating whether the user's account is active or inactive.
-   **displayName**: Users display name, such as **jacinto.gawron**.
-   **userPrincipalName**: User's name in email format, such as **jacinto.gawron@wammo.com**.
-   **mailNickname**: User's email alias.

</td></tr></tbody>
</table>## Conditions

|Condition|Description|
|---------|-----------|
|User exists|Activity found the named user.|
|User does not exist|Activity was unable to find the named user in the customer tenant domain.|
|Failure|Activity failed to connect to Azure AD.|

**Parent Topic:**[Azure AD activity pack](../concept/c_AzureADActivityPack.md)

