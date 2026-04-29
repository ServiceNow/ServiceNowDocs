---
title: Add User to Group Azure AD activity
description: The Add User to Group activity adds a user to an existing security group in Azure Active Directory.
locale: en-US
release: australia
product: Orchestration
classification: orchestration
topic_type: reference
last_updated: "2026-03-12"
reading_time_minutes: 1
breadcrumb: [Azure AD activity pack, Orchestration activity packs, Classic Orchestration, ServiceNow AI Platform Additional Capabilities, Extend ServiceNow AI Platform capabilities]
---

# Add User to Group Azure AD activity

The Add User to Group activity adds a user to an existing security group in Azure Active Directory.

To access this activity in the Workflow Editor, select the **Custom** tab, and then navigate to **Custom Activities** &gt; **Azure AD**. This activity was built with the [REST web service activity template](../../orchestration-activity-designer/task/t_CreateARESTWebServiceActivity.md#).

**Important:** The REST message used for this activity must be configured to use [OAuth 2.0](https://www.servicenow.com/docs/access?context=c_OAuthApplications&version=australia&pubname=australia-platform-security&ft:locale=en-US).

## Input variables

|Variable|Description|
|--------|-----------|
|user\_id|Object ID \(GUID\) of the member to be added.|
|group\_id|Object ID \(GUID\) of the target group.|

## Output variables

|Variable|Description|
|--------|-----------|
|error|Returns the error string from the REST message. If there are no errors, this variable returns a null value.|
|body|Contains a string value representing the output from the REST message.|
|status\_code|Contains the status code returned from the Web service.|

## Conditions

|Condition|Description|
|---------|-----------|
|Success|Activity successfully added the object ID to the security group.|
|Failure|Activity failed to update the group's membership, or the activity failed to connect to Azure AD.|

**Parent Topic:**[Azure AD activity pack](../concept/c_AzureADActivityPack.md)

