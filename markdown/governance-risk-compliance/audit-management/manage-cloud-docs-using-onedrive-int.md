---
title: Manage your documents and work papers with Audit Management as cloud files
description: You can manage your documents and work papers with Audit Management as cloud files using cloud providers like Microsoft instead of attaching them to the record.
locale: en-US
release: yokohama
product: Audit Management
classification: audit-management
topic_type: concept
last_updated: "2025-01-30"
reading_time_minutes: 1
breadcrumb: [Using Audit Management, Audit Management, Governance, Risk, and Compliance]
---

# Manage your documents and work papers with Audit Management as cloud files

You can manage your documents and work papers with Audit Management as cloud files using cloud providers like Microsoft instead of attaching them to the record.

Beginning with the Washington DC release, the document integration functionality is supported on the engagement and audit task records.

## Key benefits of workpapers and document management using Microsoft

The document integration provides the following benefits for the users:

-   Connect to the existing documents on Microsoft OneDrive such as Excel, Microsoft PowerPoint presentations, and Microsoft Word documents etc.
-   Mark a document as sharable or non-sharable​.
-   Share a non-sharable document with multiple GRC records​.
-   Control read and write access to the cloud files based on the configurable permissions.​
-   Collaborate on the documents present in the Microsoft SharePoint site​.

## Use cases for managing the cloud files

The document integration functionality addresses the following use cases for the customers:

-   Edit and read the documents and workpapers using Microsoft based on the configured access.
-   Link the documents and workpapers present in the Microsoft SharePoint site with GRC records in ServiceNow.
-   Connect to the existing documents and workpapers on Microsoft OneDrive.
-   Reference and link the cloud files that are already linked to other GRC records.
-   Mark a file that cannot be shared between the records as non-sharable so that the corresponding cloud file on Microsoft cannot be shared with other records in ServiceNow.
-   Configure the cloud file access to provide read and write access to the users based on the defined conditions.

## Roles required to manage the document integration tasks

The following roles are required to manage the document integration tasks.

<table id="table_t4n_yt2_d1c"><thead><tr><th>

Roles

</th><th>

Tasks

</th></tr></thead><tbody><tr><td>

Auditor \(sn\_audit\_ws.auditor\) and Audit Supervisor \(sn\_audit\_ws.supervisor\)

</td><td>

Can perform the following tasks:-   Link the existing documents and workpapers on Microsoft OneDrive.
-   Edit and read the documents and workpapers using Microsoft based on the configured access​.
-   Reference and link the cloud files that are already connected to other GRC records​.

</td></tr><tr><td>

Workspace Admin \(sn\_grc\_workspace.admin\)​

</td><td>

Can configure the cloud file access to provide read and write access to the users based on the defined conditions.

</td></tr></tbody>
</table>**Note:** For general guidelines on managing the documents using Microsoft Office 365, see [KB1587297](https://support.servicenow.com/nav_to.do?uri=%2Fkb%3Fid%3Dkb_article_view%26sysparm_article%3DKB1587297).

