---
title: Authentication and document access in policy authoring
description: Policy authoring now supports a hybrid authentication model that combines a shared system account with personal user credentials to enable document operations in Microsoft SharePoint and Google Drive.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/governance-risk-compliance/policy-and-compliance-management/personal-auth-and-document-access-policy-authoring.html
release: australia
product: Policy and Compliance Management
classification: policy-and-compliance-management
topic_type: concept
last_updated: "2026-06-05"
reading_time_minutes: 4
keywords: [personal authentication, policy authoring, document access permissions, system account, SharePoint, Google Drive, hybrid authentication, policy redlining]
breadcrumb: [Creating and associating policy texts from Cloud documents, Policy authoring and redlining in Compliance Workspace, Policy and Compliance Management, Governance, Risk, and Compliance]
---

# Authentication and document access in policy authoring

Policy authoring now supports a hybrid authentication model that combines a shared system account with personal user credentials to enable document operations in Microsoft SharePoint and Google Drive.

Policy authoring enables users to link policy documents hosted in Microsoft SharePoint or Google Drive to policy records in ServiceNow. Users can create, connect, or upload documents from a policy record and collaborate on the document in the cloud location. After the review and approval process is complete, the finalized document content is published as a Knowledge Base article in ServiceNow.

To make API calls to Microsoft or Google, ServiceNow requires an authenticated connection to the respective cloud service. Policy authoring supports two modes of authentication for this connection:

-   System account authentication
-   Personal authentication

## System account authentication

In system account authentication, document operations, such as creating, connecting, uploading, synchronizing content, and managing access permissions, run under a shared non-personal service account.

When a user creates or uploads a document from a policy record, the document is registered in the cloud storage location under the service account identity. It is not registered using the individual user's identity. As a result, the audit trail in SharePoint or Google Drive reflects the service account as the author or modifier, regardless of which user performed the action in ServiceNow.

## Personal authentication

Personal authentication was introduced to address the loss of individual user identity in the audit trail. When personal authentication is enabled, the create, connect, and upload operations run under the logged-in user's personal Microsoft O365 or Google account credentials. Documents created or modified from ServiceNow are registered in the cloud location under the individual user's identity, enabling accurate audit traceability of who initiated each document operation.

Personal authentication is supported for the following cloud locations:

-   -   Google Drive \(My Drive and Shared Drives\)

**Important:** Personal authentication is not supported for Microsoft OneDrive.

## Hybrid authentication model

Enabling personal authentication does not replace the system account entirely. Policy authoring uses a hybrid model in which personal credentials and system account credentials each handle a specific set of operations.

|Operation|Personal authentication enabled|Personal authentication inactive \(default\)|
|---------|-------------------------------|--------------------------------------------|
|Create document|Personal credentials|System account|
|Connect existing document|Personal credentials|System account|
|Upload document|Personal credentials|System account|
|Grant and update document access permissions|System account|System account|
|Sync document content \(Update link\)|System account|System account|

Document access permissions and content sync always run under the system account. Therefore, the service account must have sharing access to all documents in or Google Drive, even when personal authentication is enabled. Without this access, document access updates and content sync operations will fail.

**Note:** When a user performs a create, connect, or upload operation for the first time in a session with personal authentication enabled, a one-time authentication prompt appears. For , the prompt uses the logged-in Microsoft Office 365 session automatically. For Google Drive, the prompt requires the user to explicitly select an account from the account picker, followed by two separate authentication steps — one for Google Drive access and one for Google Docs access. After the token is generated, the prompt does not appear again for subsequent operations in the same session.

## Document access permissions

When a document is linked to a policy record, ServiceNow automatically grants access to the document for the users associated with the policy. Access is managed from ServiceNow to the cloud location only. Changes made directly to document permissions in or Google Drive aren't reflected back in ServiceNow.

The four roles involved in policy authoring are:

-   **Owner**: The policy owner who manages the policy record and drives the authoring workflow.
-   **Contributor**: Users who contribute to drafting the policy document.
-   **Reviewer**: Users who review the policy document before approval.
-   **Approver**: Users who approve the policy before it is published.

The access level granted to each role in the cloud document changes as the policy moves through its workflow states.

|Policy state|Owner|Contributor|Reviewer|Approver|
|------------|-----|-----------|--------|--------|
|Draft|Edit|Edit|—|—|
|Review|Edit|View|Edit|View|
|Awaiting Approval|View|View|View|View|
|Approved|View|View|View|View|

**Note:** Access levels are granted based on the email address configured for each user in ServiceNow. Verify that each user's email address in ServiceNow matches their Microsoft or Google account to confirm access is granted correctly.

## Behavior when a document is swapped

If a policy owner changes the document linked to a policy record by connecting a different document, the access permissions on the previous document are revoked and new access permissions are granted on the replacement document. This applies to both SharePoint and Google Drive.

Document access updates run asynchronously. There may be a short delay before the updated access is reflected in the cloud location after a document is swapped.

## One-way permission sync

Document access permissions are managed in one direction only, from ServiceNow to the cloud location. If a user manually modifies document permissions directly in SharePoint or Google Drive, those changes aren't captured in ServiceNow. The next time the policy changes state, ServiceNow will overwrite the manually applied permissions with the access levels defined for that state.

To avoid permission conflicts, manage document access through the Document access tab in the policy record rather than directly in SharePoint or Google Drive.

For personal authentication setup, see Knowledge Base article, [KB3075954](https://support.servicenow.com/kb?sys_kb_id=ace969cb47158f9811eaf24c736d435a&id=kb_article_view).

**Note:** You must log in to Support portal to view the KB articles.

