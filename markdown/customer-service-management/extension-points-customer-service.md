---
title: Extension points in Customer Service Management
description: Use extension points to call custom scripts in the Customer Service Management application.
locale: en-US
release: australia
topic_type: concept
last_updated: "2026-03-12"
reading_time_minutes: 2
breadcrumb: [Administer, Customer Service Management]
---

# Extension points in Customer Service Management

Use extension points to call custom scripts in the Customer Service Management application.

To access the available extension points, type **sys\_extension\_point.list** in the application navigator and press **Enter**. Click the desired extension point to view the record details.

You can create multiple implementations for each extension point and provide an order number for each implementation. The implementation that has the lowest order number is the implementation that is executed.

<table id="table_csm_extension_points"><thead><tr><th>

Extension point

</th><th>

Description

</th></tr></thead><tbody><tr><td>

sn\_customerservice.CSMService

</td><td>

Defines the default value logic for case objects. Available with the Customer Service \(com.sn\_customerservice\) plugin.

</td></tr><tr><td>

sn\_customerservice.CSMCaseSync

</td><td>

Use this extension point to customize the logic for parent-child case synchronization. This extension point can be used in one of two ways: -   Define the conditions for parent case records that can be considered for synchronization to child cases. The default functionality is based on the **sn\_customerservice.parent\_child\_ case\_sync** system property. Customers can add additional conditions using this extension point.
-   Customize the logic for parent-child case synchronization based on the state of the child case. By default, if the child case is in the **Resolved**, **Closed**, or **Cancelled** state, there is no sync from the parent case.

 This extension point is used by the CSCaseSyncHelper script include and is available with the Customer Service \(com.sn\_customerservice\) plugin.

**Note:** In the base system, parent-child case synchronization is available only for the Case table \(sn\_customerservice\_case\). This feature must be configured for tables that extend the Case table.

</td></tr><tr><td>

sn\_majorissue\_mgt.MajorCase

</td><td>

Available with the Major Issue Management \(com.sn\_majorissue\_mgt\) plugin.

</td></tr><tr><td>

sn\_action\_status.NeedsAttentionAccessUtil

</td><td>

Enables each application to choose the user roles that can enable and disable the **Needs Attention** field on a case form. Available with the Customer Service Case Action Status plugin \(com.snc.csm\_action\_status\).

</td></tr><tr><td>

sn\_cs\_sm.CSMChangeIntegrations

</td><td>

Creates the logic for mapping the **Change Request** field on the case record. Available with the Customer Service with Service Management \(com.sn\_cs\_sm\) plugin.

</td></tr><tr><td>

sn\_cs\_sm.CSMIncidentIntegrations

</td><td>

Creates the logic for mapping the **Incident** field on the case record.Available with the Customer Service with Service Management \(com.sn\_cs\_sm\) plugin.

</td></tr><tr><td>

sn\_cs\_sm.CSMProblemIntegrations

</td><td>

Creates the logic for mapping the **Problem** field on the case record. Available with the Customer Service with Service Management \(com.sn\_cs\_sm\) plugin.

</td></tr><tr><td>

sn\_cs\_sm\_request.CSMRequestIntegrations

</td><td>

Creates the logic for mapping the **Request** field on the case record.Available with the Customer Service with Request Management \(com.sn\_cs\_sm\_request\) plugin.

</td></tr><tr><td>

global.CSMRelationshipServiceEP

</td><td>

Create CSM relationships with responsibilities.Available with the Customer Service \(com.sn\_customerservice\) plugin.

</td></tr><tr><td>

global.CSMContentAccessEP

</td><td>

Creates the logic to implement ACLs for create, read, update, and delete \(CRUD\) operations.Available with the Customer Service \(com.sn\_customerservice\) plugin.

</td></tr><tr><td>

AddressMgmtExtensionPoint

</td><td>

Enables users to customize the reference qualifiers of the location field in the Account Address table​.Allows users to create an implementation of this extension point and override the “getAccountLocationsRefQual” function.

</td></tr></tbody>
</table>**Related topics**  


[Using extension points to extend application functionality](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/api-reference/web-services/extension-points.md)

[Using scripted extension points in server-side scripts](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/api-reference/web-services/scripted-extension-points.md)

[Using UI extension points in server-side UI macros](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/api-reference/web-services/ui-extension-points.md)

[Using client extension points in client-side UI scripting](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/api-reference/web-services/client-extension-points.md)

