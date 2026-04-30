---
title: Installed with Multi Provider Document Services Framework
description: Several types of components are installed with activation of the Multi Provider Document Services Framework plugin, including tables and user roles.
locale: en-US
release: xanadu
product: Document Management Services
classification: document-management-services
topic_type: reference
last_updated: "2024-08-01"
reading_time_minutes: 1
breadcrumb: [Multi Provider Document Services Framework, Document Services, Manage content capabilities, Extend ServiceNow AI Platform capabilities]
---

# Installed with Multi Provider Document Services Framework

Several types of components are installed with activation of the Multi Provider Document Services Framework plugin, including tables and user roles.

## Roles installed

<table id="table_p1k_jpz_ztb"><thead><tr><th>

Role

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Admin

 mp\_document\_admin

</td><td>

Configures multiple providers, remote document actions, and corresponding subflows.

</td></tr><tr><td>

Document User

 mp\_document\_user

</td><td>

Creates, updates, and deletes documents managed for providers

</td></tr></tbody>
</table>## Tables installed

<table id="table_ggw_lqz_ztb"><thead><tr><th>

Table

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Multi Provider Document

 mp\_document

</td><td>

The documents connected with the third-party provider.

</td></tr><tr><td>

Multi Provider Document Version

 mp\_document\_version

</td><td>

The versions related to documents.

</td></tr><tr><td>

Multi Provider Document Activity

 mp\_document\_activity

</td><td>

Logs the activity for document and document versions table and can be used to troubleshoot the actions taken on documents and versions.

</td></tr><tr><td>

Multi Provider Collaborators

 mp\_collaborators

</td><td>

Third-party users collaborating on the ServiceNow instance.

</td></tr><tr><td>

Multi Provider Detail

 mp\_provider\_detail

</td><td>

Details of the thirty-party providers that have been configured.

</td></tr><tr><td>

Multi Provider Document Action

 mp\_document\_action

</td><td>

The actions associated with each subflow.

</td></tr><tr><td>

Multi Provider Permission

 mp\_provider\_permission

</td><td>

Permissions allowed by the provider.

</td></tr><tr><td>

Multi Provider Permission Configuration

 mp\_permission\_configuration

</td><td>

Role/group mapping to permissions provided from the mp\_permission table for each provider.

</td></tr></tbody>
</table>-   **[Multi Provider Document Services Framework Framework roles](multi-provider-roles.md#)**  
Multi Provider Document Services Framework Framework is installed with these roles.

**Parent Topic:**[Multi Provider Document Services Framework](../concept/multi-provider-documents-framework.md)

**Related topics**  


[Activate Multi Provider Document Services Framework](../task/activate-multi-provider-doc-framework.md)

[Microsoft OneDrive integration with Document Services](../concept/one-drive-integration.md)

[Google Drive integration with Document Services](../concept/google-drive-integration.md)

[Create provider details](../task/create-provider-details-mp.md)

[Create document actions](../task/create-document-actions.md)

[Create provider permissions](../task/create-provider-permissions-mp.md)

[Configure permissions](../task/configure-permissions-mp.md)

