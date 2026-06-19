---
title: Enable personal authentication for policy authoring
description: Configure the integration type on the Microsoft OneDrive Spoke connection credential to enable policy authoring operations to run under the logged-in user's personal credentials instead of the system account.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/governance-risk-compliance/policy-and-compliance-management/enable-personal-auth-connection-credential-alias.html
release: australia
product: Policy and Compliance Management
classification: policy-and-compliance-management
topic_type: task
last_updated: "2026-06-05"
reading_time_minutes: 3
keywords: [personal authentication, policy authoring, connection credential alias, integration type, OneDrive Spoke, SharePoint, Google Drive]
breadcrumb: [Authentication and document access in policy authoring, Creating and associating policy texts from Cloud documents, Policy authoring and redlining in Compliance Workspace, Policy and Compliance Management, Governance, Risk, and Compliance]
---

# Enable personal authentication for policy authoring

Configure the integration type on the Microsoft OneDrive Spoke connection credential to enable policy authoring operations to run under the logged-in user's personal credentials instead of the system account.

## Before you begin

-   Verify that the Microsoft OneDrive Spoke or Google Drive Spoke application is installed on your instance.
-   Verify that personal authentication setup is complete.

    **Note:** For more information, see Knowledge Base article, [KB3075954](https://support.servicenow.com/kb?sys_kb_id=ace969cb47158f9811eaf24c736d435a&id=kb_article_view). You must log in to Support portal to view the KB article.


Role required: sn\_compliance\_ws.corporate\_compliance\_analyst, mp\_document.user

## About this task

By default, all policy authoring operations — creating, connecting, and uploading documents to SharePoint or Google Drive — run under a shared service account \(system account\). As a result, documents created or modified from ServiceNow are registered in the cloud location under the service account identity, and the individual user who performed the action is not captured.

Enabling personal authentication introduces a hybrid model where the create, connect, and upload operations run under the logged-in user's personal credentials, while document access permissions and content sync \(Update link\) continue to run under the system account. This preserves an audit trail of which user initiated each document operation in the cloud location.

**Important:** Personal authentication is supported for SharePoint and Google Drive only. OneDrive is not supported.

## Procedure

1.  Navigate to **All** &gt; **Policy and Compliance** &gt; **Administration** &gt; **GRC Properties**.

2.  Set the file sharing service property.

    Locate the **Select a file sharing service to host documents and attachments** property and select either **SharePoint** or **Google Drive** depending on the cloud location where your documents are hosted.

    Personal authentication is not supported for Microsoft OneDrive.

3.  Open the Connection &amp; Credential Aliases list.

    Go to **All** &gt; **IntegrationHub** &gt; **Connections &amp; Credentials** &gt; **Connection &amp; Credential Aliases**.

4.  Open the default **OneDrive** connection credential alias.

    This is the default alias shipped with the Microsoft OneDrive Spoke. All policy authoring flows that interact with OneDrive or SharePoint use this alias by default.

5.  Set up the connection for this default alias.

    1.  In the Connections related list, verify whether a connection record already exists.

    2.  If no connection record exists, select **New**.

    3.  In Microsoft OneDrive Spoke Connection screen, enter the following values:

    |Field|Values|
    |-----|------|
    |Name|Microsoft OneDrive Spoke Connection|
    |Credential|Microsoft OneDrive Spoke Credential|
    |Connection alias|sn\_onedrive\_spoke.OneDrive|
    |Connection URL|https://graph.microsoft.com|
    |API Version|v1.0|
    |Active|Selected|

6.  Open the connection credential associated with the alias.

    In the **Microsoft OneDrive Spoke Connection** record in the **Connections** tab, select the credential listed in the **Credential** column: **Microsoft OneDrive Spoke Credential**. This is an OAuth 2.0 Credentials record.

7.  Change the integration type to Personal.

    On the OAuth 2.0 Credentials record, locate the **Integration Type** field. The default value is **System**. Select **Personal** from the drop-down list.

    When the integration type is set to **Personal**, all create, connect, and upload calls made to Microsoft or Google APIs will look for the logged-in user's personal credential token and use it for the operation.

8.  Select **Update** to save the record.


## Result

Personal authentication is now enabled for policy authoring. Documents created or uploaded from ServiceNow will now be registered in the cloud location under the logged-in user's identity, enabling audit traceability at the individual user level.

**Note:** When a user performs a create, connect, or upload operation for the first time in a session with personal authentication enabled, a one-time authentication prompt appears. For SharePoint, the prompt uses the logged-in Microsoft O365 session automatically. For Google Drive, the prompt requires the user to explicitly select an account from the account picker, followed by two separate authentication steps, one for Google Drive access and one for Google Docs access. After the token is generated, the prompt does not appear again for subsequent operations in the same session.

## What to do next

After enabling personal authentication, verify that:

-   Verify that the system credential user \(service account\) has sharing access to the documents in SharePoint or Google Drive. Document access permission grants and content sync operations always run under the system account credentials, even when personal authentication is enabled. If the system credential user does not have access, document access and update operations will fail.
-   Users who will perform policy authoring operations have active Microsoft O365 or Google accounts associated with their ServiceNow login.

