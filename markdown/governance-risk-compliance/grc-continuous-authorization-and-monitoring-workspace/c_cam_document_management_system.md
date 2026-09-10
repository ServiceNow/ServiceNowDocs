---
title: Document reuse across records
description: Link documents to authorization packages, boundaries, and engagements from your workspace, cloud storage, or local systems. Linked documents become shared resources across records.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/governance-risk-compliance/grc-continuous-authorization-and-monitoring-workspace/c\_cam\_document\_management\_system.html
release: australia
product: GRC: Continuous Authorization and Monitoring Workspace
classification: grc-continuous-authorization-and-monitoring-workspace
topic_type: concept
last_updated: "2026-08-17"
reading_time_minutes: 3
keywords: [document management, authorization package, documents, versioning, DMS]
breadcrumb: [Continuous authorization and monitoring tasks in the CAM Workspace, Use, Continuous Authorization and Monitoring, Governance, Risk, and Compliance]
---

# Document reuse across records

Link documents to authorization packages, boundaries, and engagements from your workspace, cloud storage, or local systems. Linked documents become shared resources across records.

When you link a document to a record, that document becomes a shared resource for your instance. Any authorized user can reference it across multiple packages. If the document changes, whether it's content revisions or updated versions, those changes appear everywhere the document is linked. You get a single source of truth instead of scattered copies.

**Note:** You can link documents to an authorization package, boundary, or an engagement at any step in the workflow. The package just needs to be active.

## Attachments and linked documents work differently

Attachments are tied to one record only. If you attach a file, another record that needs the same file must attach it again. You end up managing multiple copies.

Linked documents are available at the instance level. Link once, reference many times. When you update the document, every package that links to it sees the update immediately.

## Where you can pull documents from

You can link documents from:

-   Documents in your workspace
-   Documents shared with you by colleagues
-   Documents in cloud repositories \(Google Drive, Microsoft OneDrive, SharePoint\)
-   Documents on local drives \(when your admin has configured access\)

## Track document versions through approval workflows

Documents progress through a clear approval journey:

-   Draft: Document is in preparation and has not been submitted for review.
-   Awaiting Review: Document has been submitted and is under reviewer assessment.
-   Awaiting Approval: Review is complete. Document is pending approval for publication.
-   Published: All required approvals have been obtained. This is the active version in use.
-   Retired: Superseded version. Replaced by a newer published version.

**Important:** Versions move forward through the approval process. You can't go back to an earlier version after a new one is published.

## When to link documents

Link documents when you want to:

-   Use the same document across multiple authorization packages without creating copies
-   Watch a document evolve as it moves through reviews and approvals
-   Control who can view, edit, or approve based on their role
-   Organize documents in folders to keep your workspace clean
-   Keep documents in cloud storage while linking them here for easy access

-   **[Add documents to records](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/governance-risk-compliance/grc-continuous-authorization-and-monitoring-workspace/t_add_documents_to_auth_package.md)**  
Link documents from your workspace, cloud storage, or local drives to authorization packages, boundaries, and engagements. You can organize documents into folders and grant access to other users.
-   **[Set document permissions](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/governance-risk-compliance/grc-continuous-authorization-and-monitoring-workspace/t_set_document_permissions.md)**  
Grant users and roles access to documents by assigning permissions at the role, user, group, or criteria level. Permissions control whether users can view, edit, or own documents.
-   **[Configure document approval workflows](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/governance-risk-compliance/grc-continuous-authorization-and-monitoring-workspace/t_configure_document_approval_workflow.md)**  
Set up reviewers and approvers for linked documents to establish a formal approval workflow before a document version becomes active.
-   **[Create, manage, and submit document versions for approval](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/governance-risk-compliance/grc-continuous-authorization-and-monitoring-workspace/t_track_document_versions.md)**  
Create and manage document versions to maintain a complete history of changes as a document evolves.
-   **[Review and approve document versions](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/governance-risk-compliance/grc-continuous-authorization-and-monitoring-workspace/t_review_and_approve_documents.md)**  
Examine document versions submitted for review and authorize them to move forward in the approval workflow as a reviewer or approver.
-   **[Use ServiceNow Otto to analyze linked documents](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/governance-risk-compliance/grc-continuous-authorization-and-monitoring-workspace/t_use_smart_docs_with_documents.md)**  
Use ServiceNow Otto to summarize documents, ask questions, and generate audio summaries without manually reviewing every page.
-   **[Connect documents to external cloud storage](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/governance-risk-compliance/grc-continuous-authorization-and-monitoring-workspace/t_connect_documents_to_external_cloud.md)**  
Link documents to external cloud storage such as Google Drive, OneDrive, or SharePoint to keep your documents synchronized across platforms.
-   **[Edit document metadata](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/governance-risk-compliance/grc-continuous-authorization-and-monitoring-workspace/t_edit_document_metadata.md)**  
Update document properties such as name, owner, classification, and access settings to organize documents and control permissions.

**Parent Topic:**[Continuous authorization and monitoring tasks in the CAM Workspace](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/governance-risk-compliance/grc-continuous-authorization-and-monitoring-workspace/cam-ws-continuous-auth-monitor.md)

