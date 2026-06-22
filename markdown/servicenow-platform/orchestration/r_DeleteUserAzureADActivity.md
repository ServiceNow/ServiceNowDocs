---
title: Delete User Azure AD activity
description: The Delete User activity deletes the named user's account from the Azure Active Directory tenant.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/zurich/servicenow-platform/orchestration/r\_DeleteUserAzureADActivity.html
release: zurich
product: Orchestration
classification: orchestration
topic_type: reference
last_updated: "2025-07-31"
reading_time_minutes: 1
breadcrumb: [Azure AD activity pack, Orchestration activity packs, Classic Orchestration, ServiceNow AI Platform Additional Capabilities, Extend ServiceNow AI Platform capabilities]
---

# Delete User Azure AD activity

The Delete User activity deletes the named user's account from the Azure Active Directory tenant.

To access this activity in the Workflow Editor, select the **Custom** tab, and then navigate to **Custom Activities** &gt; **Azure AD**. This activity was built with the [REST web service activity template](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/servicenow-platform/orchestration/t_CreateARESTWebServiceActivity.md).

**Important:** The REST message used for this activity must be configured to use [OAuth 2.0](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/platform-security/authentication/c_OAuthApplications.md).

## Input variables

|Variable|Description|
|--------|-----------|
|user\_id|The object ID \(GUID\) or the user principal name of the target user. An example of a user principal name is **someuser@a830edad9050849NDA1.onmicrosoft.com**.|

## Output variables

|Variables|Description|
|---------|-----------|
|error|Returns the error string from the REST message. If there are no errors, this variable returns a null value.|
|body|Contains a string value representing the output from the REST message.|
|status\_code|Contains the status code returned from the Web service.|

## Conditions

|Condition|Description|
|---------|-----------|
|Deleted user|Activity deleted the specified user.|
|User does not exist|Specified user does not have an account in the tenant domain.|
|Failure|Activity failed to connect to Azure AD.|

**Parent Topic:**[Azure AD activity pack](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/servicenow-platform/orchestration/c_AzureADActivityPack.md)

