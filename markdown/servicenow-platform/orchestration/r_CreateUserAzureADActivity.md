---
title: Create User Azure AD activity
description: The Create User activity creates a user for the Azure Active Directory tenant.
locale: en-US
release: australia
product: Orchestration
classification: orchestration
topic_type: reference
last_updated: "2026-03-12"
reading_time_minutes: 2
breadcrumb: [Azure AD activity pack, Orchestration activity packs, Classic Orchestration, ServiceNow AI Platform Additional Capabilities, Extend ServiceNow AI Platform capabilities]
---

# Create User Azure AD activity

The Create User activity creates a user for the Azure Active Directory tenant.

To access this activity in the Workflow Editor, select the **Custom** tab, and then navigate to **Custom Activities** &gt; **Azure AD**. This activity was built with the [REST web service activity template](../../orchestration-activity-designer/task/t_CreateARESTWebServiceActivity.md#).

**Important:** The REST message used for this activity must be configured to use OAuth 2.0.

## Input variables

|Variable|Description|
|--------|-----------|
|display\_name|Name of the Azure AD user in the accepted display format, such as **jacinto.gawron**.|
|user\_principal\_name|User principal name \(UPN\) in an email format. For example, you might enter **jacinto.gawron@khitomer.com**.|
|mail\_nickname|User's email alias that redirects to the user's full address.|
|password|User's Azure AD password. This password must be passed as a workflow input with a type of **Password \(2 Way Encrypted\)** and must meet the password policy set in Azure AD.|
|change\_password|Control that requires the user to change their password at the next login, if set to true.|
|account\_enabled|Control that sets the user's account is enabled, if set to true.|
|given\_name|First name of the user.|
|surname|Last name of the user.|
|other\_mails|List of additional email addresses for the user. For example, you might enter `["jac@home.com", "jgawron@fabrikam.com"]`.|
|country|The country or region in which the user is located. For example, you might enter **US** or **UK**. The default value is set to**US**.|
|city|City in which the user is located.|
|department|Name of the department in which the user works.|
|mobile|User's primary cell phone number.|
|job\_title|User's job title.|
|physical\_delivery\_office\_name|Office location in the user place of business.|
|postal\_code|Postal code of the user's address.|
|preferred\_language|Language in which the user prefers to communicate. This value must follow the ISO 639-1 Code. For example, you might enter **en-US**. The default value is set to **en-US**.|
|state|State or province for the user's address.|
|street\_address|Street address of the user's place of business.|
|telephone\_number|Primary telephone number of the user's place of business.|
|usage\_location|Two letter country code that is required for users who are assigned Office 365 licenses. The default value is **US**.|

## Output variables

<table id="table_tqb_dqx_45"><thead><tr><th>

Variable

</th><th>

Description

</th></tr></thead><tbody><tr><td>

error

</td><td>

Returns the error string from the REST message. If there are no errors, this variable returns a null value.

</td></tr><tr><td>

status\_code

</td><td>

Contains the status code returned from the Web service.

</td></tr><tr><td>

user\_exists

</td><td>

Output variable mapped to the JSON message that contains the `User already exists` error.

</td></tr><tr><td>

user\_info

</td><td id="e_UserInfoArray">

The **user\_info** array contains attributes that can be leveraged by other activities as inputs. For example, the user **objectid** output \(GUID\) can be passed to the Add User to Group activity as the **user\_id** input.-   **objectid**: User's Azure AD identifier.
-   **accountEnabled**: Boolean variable indicating whether the user's account is active or inactive.
-   **displayName**: Users display name, such as **jacinto.gawron**.
-   **userPrincipalName**: User's name in email format, such as **jacinto.gawron@wammo.com**.
-   **mailNickname**: User's email alias.

</td></tr></tbody>
</table>## Conditions

|Conditions|Description|
|----------|-----------|
|Created user|Activity successfully created the user.|
|User already exists|User already exists in the tenant domain.|
|Failure|Activity failed to connect to Azure AD, or an input value was invalid.|

