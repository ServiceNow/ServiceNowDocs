---
title: Using Document Management System in Audit Workspace
description: The Document Management System in Audit Workspace provides a centralized repository for storing and managing documents in engagements, control tests, and evidence records. The Documents panel is a native side pane that allows you to store, version, and control access to documents.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/governance-risk-compliance/audit-management/manage-documents-panel.html
release: brazil
product: Audit Management
classification: audit-management
topic_type: concept
last_updated: "2026-09-10"
reading_time_minutes: 3
breadcrumb: [Audit Workspace overview, Audit Management, Governance, Risk, and Compliance]
---

# Using Document Management System in Audit Workspace

The Document Management System in Audit Workspace provides a centralized repository for storing and managing documents in engagements, control tests, and evidence records. The Documents panel is a native side pane that allows you to store, version, and control access to documents.

The Documents panel is available alongside the existing Attachments panel on engagements, control tests, and evidence records in the Audit Workspace. Unlike attachments—which are linked only to the record where they were added—documents are stored at the instance level and can be linked to multiple GRC records. The document owner or any authorized user can link the same document to multiple records. When you rename a document, the change updates everywhere it is linked.

## Supported records

The Documents panel is available on the following records:

-   Engagement
-   Control test
-   Evidence

## Document availability by record state

You can add, remove, or edit documents only while the parent record is open. When an engagement or control test moves into a closed state, the Documents panel becomes read-only. You can still view the documents that are already linked to the record, but you can't add, remove, or edit them.

The following closed states make the Documents panel read-only:

-   Engagement: Closed Complete or Closed Incomplete
-   Control test: Closed Complete, Closed Incomplete, or Closed Skipped

## Folders

You can organize documents into folders and nested folders from the Documents panel. Use the breadcrumb at the top of the panel to navigate between folder levels. The Documents panel also lets you filter between documents that you own, documents shared with you, and all documents you have access to.

## Document actions

Select a document to perform the following actions:

-   Download, rename, or edit metadata. For more information, see [Documents panel actions](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/governance-risk-compliance/audit-management/documents-panel-actions.md).
-   Track versions and manage approval workflows. For more information, see [Document version and approval workflow](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/governance-risk-compliance/audit-management/document-version-approval-workflow.md).
-   Manage permissions. For more information, see [Manage document permissions](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/governance-risk-compliance/audit-management/manage-document-permissions.md).
-   Connect to an external cloud location. For more information, see [Connect an external cloud document](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/governance-risk-compliance/audit-management/connect-external-cloud-documents.md).
-   Remove the document from the record. For more information, see [Remove a document from a record](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/governance-risk-compliance/audit-management/remove-a-document-from-a-record.md).

Adding or removing a document adds a corresponding entry to the work notes of the record.

## Information on the documents

Use the ServiceNow Otto® panel to get more information on the documents using generative AI capabilities. Ask questions about document content or generate summaries to quickly understand key information.

Voice assist enables voice chat and audio summaries of documents. Use voice commands to navigate documents and receive spoken summaries, making document review more accessible and efficient.

## Documents panel vs. Cloud files

The Documents panel is separate from the Microsoft based cloud file integration. For more information, see [Manage your documents and work papers with Audit Management as cloud files](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/governance-risk-compliance/audit-management/manage-cloud-docs-using-onedrive-int.md).

-   Use the Documents panel to manage documents natively within ServiceNow with version control and approval workflows.
-   Use the **Cloud files** related list to keep documents on Microsoft OneDrive or Microsoft SharePoint as the source of truth.

## Smart docs and Voice agent configuration in Audit Workspace

For the configuration guide for Smart docs and Voice agent in Audit Workspace, see [KB3153395](https://support.servicenow.com/kb?id=kb_article_view&sysparm_article=KB3153395).

