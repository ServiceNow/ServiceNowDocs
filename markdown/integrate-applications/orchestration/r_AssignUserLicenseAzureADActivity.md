---
title: Assign User License Azure AD activity
description: The Assign User License activity assigns an additional Office 365 software license to the named user.
locale: en-US
release: australia
product: Orchestration
classification: orchestration
topic_type: reference
last_updated: "2026-03-12"
reading_time_minutes: 1
breadcrumb: [Azure AD activity pack, Orchestration activity packs, Classic Orchestration, Workflow Data Fabric]
---

# Assign User License Azure AD activity

The Assign User License activity assigns an additional Office 365 software license to the named user.

To access this activity in the Workflow Editor, select the **Custom** tab, and then navigate to **Custom Activities** &gt; **Azure AD**. This activity was built with the [REST web service activity template](../../orchestration-activity-designer/task/t_CreateARESTWebServiceActivity.md#).

**Important:** The REST message used for this activity must be configured to use [OAuth 2.0](https://www.servicenow.com/docs/access?context=c_OAuthApplications&version=australia&pubname=australia-platform-security&ft:locale=en-US).

## Input variables

|Variable|Description|
|--------|-----------|
|user\_id|The object ID \(GUID\) or the user principal name of the target user. An example of a user principal name is **someuser@a830edad9050849NDA1.onmicrosoft.com**.|
|sku\_id|Subscription SKU ID associated with the tenant's enterprise agreement.|

## Output variables

|Variable|Description|
|--------|-----------|
|error|Returns the error string from the REST message. If there are no errors, this variable returns a null value.|
|body|Contains a string value representing the output from the REST message.|
|status\_code|Contains the status code returned from the Web service.|

## Conditions

|Condition|Description|
|---------|-----------|
|Success|Activity successfully assigned an Office 365 license to a user.|
|Failure|Activity failed to assigned an Office 365 license to a user, or the activity failed to connect to Azure AD.|

