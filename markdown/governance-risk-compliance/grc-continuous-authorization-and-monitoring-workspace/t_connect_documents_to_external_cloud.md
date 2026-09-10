---
title: Connect documents to external cloud storage
description: Link documents to external cloud storage such as Google Drive, OneDrive, or SharePoint to keep your documents synchronized across platforms.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/governance-risk-compliance/grc-continuous-authorization-and-monitoring-workspace/t\_connect\_documents\_to\_external\_cloud.html
release: australia
product: GRC: Continuous Authorization and Monitoring Workspace
classification: grc-continuous-authorization-and-monitoring-workspace
topic_type: task
last_updated: "2026-09-10"
reading_time_minutes: 1
keywords: [external cloud, cloud storage, document sync, Google Drive, OneDrive, SharePoint, cloud integration]
breadcrumb: [Document reuse across records, Continuous authorization and monitoring tasks in the CAM Workspace, Use, Continuous Authorization and Monitoring, Governance, Risk, and Compliance]
---

# Connect documents to external cloud storage

Link documents to external cloud storage such as Google Drive, OneDrive, or SharePoint to keep your documents synchronized across platforms.

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

-   External cloud integration enabled and configured by your administrator
-   Multi-provider documents plugin installed on your instance
-   Credentials configured for at least one external cloud provider \(Google Drive, OneDrive, or SharePoint\)

## About this task

External cloud integration keeps documents synchronized between your ServiceNow instance and cloud storage. Use this when you need to:

-   Maintain a single source of truth across multiple platforms
-   Pull updates from cloud storage into authorization packages
-   Push approved versions to cloud storage

**Note:** The Connect external cloud option only appears if your administrator has installed the multi-provider documents plugin on your instance.

## Procedure

1.  In the authorization package or engagement, open the **Documents** side panel.

2.  Select the menu icon next to the document you want to connect to cloud storage.

3.  Select **Attach from cloud**.

    The **External Cloud** dialog opens.

4.  Select the cloud operation you need:

    1.  **Attach from cloud:** Select this option to link a document from your cloud storage and create a new version in ServiceNow instance with the cloud document's content.

    2.  **Upload to cloud:** Select this option to push the current ServiceNow version of the document to your cloud storage.

5.  Select **Continue** to confirm your selection and initiate the cloud operation.

    Wait for the operation to complete.


## Result

Success notifications confirm that the document is synced or added. Error notifications alert you to any issues that occurred during the sync.

**Parent Topic:**[Document reuse across records](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/governance-risk-compliance/grc-continuous-authorization-and-monitoring-workspace/c_cam_document_management_system.md)

