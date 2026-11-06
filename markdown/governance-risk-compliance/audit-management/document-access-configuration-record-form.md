---
title: Cloud file configuration record form
description: Update the access permissions for a record in the Cloud file configuration record form.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/australia/governance-risk-compliance/audit-management/document-access-configuration-record-form.html
release: australia
product: Audit Management
classification: audit-management
topic_type: reference
last_updated: "2026-09-10"
reading_time_minutes: 1
breadcrumb: [Cloud File Configuration, Cloud File Access Setup, Cloud Document Management, Audit Management overview, Audit Management, Governance, Risk, and Compliance]
---

# Cloud file configuration record form

Update the access permissions for a record in the Cloud file configuration record form.

## Cloud file configuration record form

For a description of the field values, see the following table.

<table id="table_h21_nyj_4zb"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Name

</td><td>

Name of the Cloud file configuration record. For example, Engagement document access.

</td></tr><tr><td>

Table

</td><td>

Table used for the Cloud file configuration record. For example, Engagement \[sn\_audit\_engagement\]. For all the files used in this table, the access permissions are configured in this form.

</td></tr><tr><td>

Provider

</td><td>

Provider for the Cloud file configuration. Location where the files are present in the cloud. The default option is **OneDrive default**.

</td></tr><tr><td>

Order

</td><td>

The precedence of executing the configuration relative to another configuration with similar criteria when both the configurations apply to a record.

</td></tr><tr><td>

Active

</td><td>

Option to mark the record as active.

</td></tr><tr><td>

Filter condition

</td><td>

Condition used to create the document access record. A sample condition would be: "**State**" "**is one of**" "**Open**, **Work In Progress**, **Review**."

</td></tr><tr><td class="sub-head" colspan="2">

File upload location

</td></tr><tr><td>

Folder structure

</td><td>

Folder path to which the cloud files must be uploaded.The folder structure can be set up using static text and dynamic variables.

</td></tr><tr><td>

Fields

</td><td>

Field picker that lists all the fields from the selected table.

</td></tr><tr><td>

File location type

</td><td>

Type of Microsoft SharePoint location where the files are uploaded. The default option is **Site**.-   **Site**: Files are uploaded to the default document library in the Microsoft SharePoint site.
-   **Drive**: Files are uploaded to a specific document library within a Microsoft SharePoint site.

</td></tr><tr><td>

File location ID

</td><td>

ID of the location that you selected in the **File location type** field.-   For **Site**, enter the site ID in the format `hostname,siteCollectionId,siteId`, with no spaces.
-   For **Drive**, enter the ID of the document library.

For steps to find the ID, see [Find the File location ID for a Cloud file configuration](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/australia/governance-risk-compliance/audit-management/get-sharepoint-file-location-id.md).

</td></tr><tr><td class="sub-head" colspan="2">

Settings

</td></tr><tr><td>

Cloud actions conditions

</td><td>

Cloud actions such as Link cloud file or Upload files to cloud, which will be displayed in the Cloud files tab based on the selected condition.

</td></tr></tbody>
</table>