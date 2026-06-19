---
title: Connection and credential alias record fields
description: The Microsoft OneDrive Spoke connection and credential alias controls how policy authoring operations authenticate with Microsoft SharePoint and Google Drive. Understanding the alias structure helps you configure and switch between system and personal authentication.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/governance-risk-compliance/policy-and-compliance-management/connection-credential-alias-policy-authoring.html
release: australia
product: Policy and Compliance Management
classification: policy-and-compliance-management
topic_type: reference
last_updated: "2026-06-05"
reading_time_minutes: 1
keywords: [connection credential alias, sn\_onedrive\_spoke.OneDrive, child alias, Microsoft System LES, integration type, policy authoring]
breadcrumb: [Authentication and document access in policy authoring, Creating and associating policy texts from Cloud documents, Policy authoring and redlining in Compliance Workspace, Policy and Compliance Management, Governance, Risk, and Compliance]
---

# Connection and credential alias record fields

The Microsoft OneDrive Spoke connection and credential alias controls how policy authoring operations authenticate with Microsoft SharePoint and Google Drive. Understanding the alias structure helps you configure and switch between system and personal authentication.

When the Microsoft OneDrive Spoke is installed, the platform ships a default Connection &amp; Credential alias record named OneDrive with the ID, sn\_onedrive\_spoke.OneDrive. All policy authoring flows that interact with SharePoint or OneDrive reference this alias. The alias contains a connection record, an associated credential, and one or more child aliases that enable switching between different service accounts or authentication modes.

## Alias record fields

The following fields are relevant to policy authoring configuration on the sn\_onedrive\_spoke.OneDrive alias record.

|Field|Value|Description|
|-----|-----|-----------|
|Name|OneDrive|Display name of the alias record.|
|ID|sn\_onedrive\_spoke.OneDrive|Unique system identifier for the alias. Referenced by all OneDrive and SharePoint flows for policy authoring.|
|Application|Microsoft OneDrive Spoke|The spoke application that owns this alias record.|
|Type|Connection and Credential|Indicates that the alias stores both connection and credential information.|
|Connection Type|HTTP|The protocol used for API calls to Microsoft endpoints \(graph.microsoft.com\).|

## Microsoft OneDrive Spoke Credential fields

The connection record linked to the alias references an OAuth 2.0 Credentials record named Microsoft OneDrive Spoke Credential. The following fields on this credential record are relevant to personal authentication configuration.

<table id="table_rdp_tyh_mjc"><thead><tr><th>

Field

</th><th>

Options

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Integration Type

</td><td>

System \(default\) \| Personal

</td><td>

Controls which credentials are used when policy authoring operations make API calls to Microsoft or Google.

 -   **System**: All operations use the shared service account credentials. Documents created or modified from ServiceNow are registered under the service account identity in the cloud location. This is the default behavior.
-   **Personal**: Create, connect, and upload operations use the logged-in user's personal OAuth credentials. Documents are registered under the individual user's identity, enabling audit traceability. Document access permission grants and content sync \(Update link\) continue to use system account credentials regardless of this setting.

</td></tr><tr><td>

OAuth Entity Profile

</td><td>

OneDrive OAuth

</td><td>

The OAuth profile that defines the authorization server, client ID, client secret, and token endpoints used to generate and refresh OAuth tokens.

</td></tr></tbody>
</table>## Supported cloud locations

Personal authentication is supported for the following cloud locations used in policy authoring:

-   Microsoft SharePoint
-   Google Drive

Personal authentication is not supported for Microsoft OneDrive.

