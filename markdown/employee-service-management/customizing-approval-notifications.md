---
title: Customizing approval notification fields
description: You can customize the approval notification fields by creating the methods in a script include.
locale: en-US
release: xanadu
topic_type: concept
last_updated: "2024-08-01"
reading_time_minutes: 1
breadcrumb: [IT Service Management integration, Microsoft Teams Integration for Employee Experience, Configure, ServiceNow for Microsoft Teams and Microsoft 365, Employee Service Management]
---

# Customizing approval notification fields

You can customize the approval notification fields by creating the methods in a script include.

**Note:** The topic uses the API names of the script includes.

Actionable Notifications are sent for approval and comments on tickets. You can customize the fields displayed in the approval notifications by creating methods in the `sn_now_teams.ApprovalsVAUtil()` script include. These methods override the ones in the `sn_now_teams.ApprovalsVAUtilSNC()` script include.

For information about script includes, see [Script includes](https://www.servicenow.com/docs/access?context=c_ScriptIncludes&version=xanadu&pubname=xanadu-api-reference&ft:locale=en-US).

## Creating the method

The notification logic calls a method based on the table that the approval record is created for. The method names follow this format: get&lt;TableName&gt;Fields\(\), which you can use to create a method for any table in the base system.

**Note:** Custom tables aren’t supported for approval notifications.

For example: If the table name is sc\_request, the method name is getScRequestFields\(\). If the table name is incident, the method name is getIncidentFields\(\).

## Overriding the method fields

The methods that you create in the `sn_now_teams.ApprovalsVAUtil()` script include override the ones in `sn_now_teams.ApprovalsVAUtilSNC()`.

While creating the method, you can enter the field names that are displayed in the approval notification.

-   For TASK extended tables, you can dot-walk to the referenced field by using the *sysapproval* field.

    For example:

    ```javascript
    getChangeRequestFields: function() {
     return {
      "fields": ["sysapproval.number", "sysapproval.short_description", "sysapproval.risk", "sysapproval.start_date", "state"]
      }
    },
    ```

-   For NON-TASK tables, you must enter the table fields directly.

    For example:

    ```javascript
    getKbKnowledgeFields: function() {
     return {
      "fields": ["number", "short_description", "kb_knowledge_base", "author", "workflow_state"]
      }
    },
    ```

-   You can create a default method, getDefaultFields\(\), which is used if the system doesn’t find a method for the table in the approval record. The field references follow the TASK extended tables.

    For example:

    ```javascript
    getDefaultFields: function() {
     return {
      "fields": ["sysapproval.number", "sysapproval.requested_for", "sysapproval.price", "sysapproval.due_date", "state"]
      }
    },
    ```


**Parent Topic:**[Configure IT Service Management integration with Microsoft Teams](sn-ms-teams-config-it.md)

