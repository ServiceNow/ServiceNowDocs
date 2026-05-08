---
title: Remove User from Group Azure AD activity
description: The Remove User from Group activity removes an existing user from a security group in Azure Active Directory.
locale: en-US
release: australia
product: Orchestration
classification: orchestration
topic_type: reference
last_updated: "2026-03-12"
reading_time_minutes: 1
breadcrumb: [Azure AD activity pack, Orchestration activity packs, Classic Orchestration, Workflow Data Fabric]
---

# Remove User from Group Azure AD activity

The Remove User from Group activity removes an existing user from a security group in Azure Active Directory.

To access this activity in the Workflow Editor, select the **Custom** tab, and then navigate to **Custom Activities** &gt; **Azure AD**. This activity was built with the [REST web service activity template](../../orchestration-activity-designer/task/t_CreateARESTWebServiceActivity.md#).

**Important:** The REST message used for this activity must be configured to use OAuth 2.0.

## Input variables

|Variable|Description|
|--------|-----------|
|user\_id|Object ID \(GUID\) of the user to be removed.|
|group\_id|Object ID \(GUID\) of the target group.|

## Output variables

|Variable|Description|
|--------|-----------|
|error|Returns the error string from the REST message. If there are no errors, this variable returns a null value.|
|body|Contains a string value representing the output from the REST message.|
|status\_code|Contains the status code returned from the Web service.|

## Conditions

|Variable|Description|
|--------|-----------|
|Success|Activity removed the object ID from the security group.|
|Failure|Activity failed to update the group's membership, or the activity failed to connect to Azure AD.|

**Parent Topic:**[Azure AD activity pack](../concept/c_AzureADActivityPack.md)

