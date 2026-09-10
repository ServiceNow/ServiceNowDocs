---
title: Edit document metadata
description: Update document properties such as name, owner, classification, and access settings to organize documents and control permissions.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/governance-risk-compliance/grc-continuous-authorization-and-monitoring-workspace/t\_edit\_document\_metadata.html
release: australia
product: GRC: Continuous Authorization and Monitoring Workspace
classification: grc-continuous-authorization-and-monitoring-workspace
topic_type: task
last_updated: "2026-08-27"
reading_time_minutes: 1
keywords: [document metadata, document properties, access settings, classification]
breadcrumb: [Document reuse across records, Continuous authorization and monitoring tasks in the CAM Workspace, Use, Continuous Authorization and Monitoring, Governance, Risk, and Compliance]
---

# Edit document metadata

Update document properties such as name, owner, classification, and access settings to organize documents and control permissions.

## Before you begin

Role required:

-   sn\_irm\_cont\_auth.system\_owner
-   sn\_irm\_cont\_auth.info\_system\_sec\_officer
-   sn\_irm\_cont\_auth.authorization\_official
-   sn\_irm\_cont\_auth.info\_system\_sec\_manager
-   sn\_irm\_cont\_auth.admin
-   sn\_irm\_cont\_auth.information\_owner
-   sn\_irm\_cont\_auth.sec\_control\_assessor
-   sn\_irm\_cont\_auth.system\_user

In general, any role with write access to the record can add, edit, or modify the docs.

**Note:** You can add documents only when the record is in an active state. Inactive records don't allow changes to linked documents.

## About this task

Document metadata identifies and classifies documents to organize them in your authorization package and control access permissions.

## Procedure

1.  In the **Documents** panel, select the document menu and select **Edit Metadata**.

    The Edit metadata dialog opens.

2.  Update the appropriate document metadata fields.

    |Field|Required|Description|
    |-----|--------|-----------|
    |Owner|Yes|User who has full permissions to manage the document. Search for users by name.|
    |Type|No|Document classification type \(Policy, Guideline, Procedure, Contract, or None\)|
    |Classification|No|Sensitivity level \(Public, Internal, Confidential, or Restricted\)|
    |State|No|Read-only field showing document status \(reflects version state\)|
    |Description|No|Brief description of document content and purpose|
    |Default Version|No|Version number that is designated as the active version|

3.  In the **Access Settings** section, configure access control options:

    1.  Check **By referenced records** to make the document accessible through linked records.

    2.  Check **Sharing permissions** to enable permission sharing for this document.

    3.  Configure **Admin access** to control administrative permissions for the document.

4.  Select **Save** to save your metadata changes.

    The metadata is updated and the dialog closes.


## Result

The document now reflects all the metadata changes you made.

**Parent Topic:**[Document reuse across records](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/governance-risk-compliance/grc-continuous-authorization-and-monitoring-workspace/c_cam_document_management_system.md)

