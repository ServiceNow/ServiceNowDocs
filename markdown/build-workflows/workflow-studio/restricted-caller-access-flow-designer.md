---
title: Restricted caller access to Workflow Studio flows
description: Track flows and actions that require access to cross-scope resources. Allow or deny flows and actions access to cross-scope resources.Allow instances upgraded from San Diego and earlier releases to generate restricted caller access privilege requests for flows and actions.
locale: en-US
release: yokohama
product: Workflow Studio
classification: workflow-studio
topic_type: concept
last_updated: "2025-01-30"
reading_time_minutes: 4
breadcrumb: [Configuring flows, Configuring Workflow Studio, Workflow Studio, Build workflows]
---

# Restricted caller access to Workflow Studio flows

Track flows and actions that require access to cross-scope resources. Allow or deny flows and actions access to cross-scope resources.

The Restricted Caller Access Privileges table has dedicated source types to identify Workflow Studio calling sources.

-   **Flow**

    The system uses the flow source type to track operations run by ServiceNow Core actions. Restricted Caller Access Privileges records allow a flow to perform a specific operation on a specific cross-scope resource. Approving a flow to run an operation allows any other core action within the same flow to perform the same operation on the same cross-scope resource.

    For example, suppose you have a flow that runs the Look Up Records action on a cross-scope table. When caller restriction is enabled for the cross-scope table, the Look Up Records action generates a request to perform a read operation. When you allow the flow to perform read-operations on the cross-scope table any other read operations performed by core actions can also run. For example, your flow could run the Look Up Record and Lookup Attachments actions on the same cross-scope table. Suppose you add the Look Up Records action for the same cross-scope table to another flow or subflow. Since this read operation comes from another flow, the core action generates a separate access privilege request for approval. If you configure the Look Up Records action to access another cross-scope table, that too generates a separate access privilege request for approval.

-   **Flow Action**

    The system uses the flow action source type to track operations run by custom actions to a specific cross-scope resource. Restricted Caller Access Privileges records allow a custom action to perform a specific operation on a specific cross-scope resource. Approving an action to run an operation allows the custom action to perform the operation on the cross-scope resource in any context.

    For example, suppose you create a custom action that runs the Look Up Records step on a cross-scope table. When caller restriction is enabled for the cross-scope table, the Look Up Records step generates a request to perform a read operation. When you allow the custom action to perform read operations on the cross-scope table you can run the custom action from any context. For example, you can add the custom action to multiple flows or call the custom action from a script. As long as the custom action performs the operation on the allowed target cross-scope resource, the system allows the custom action to run. If you configure the custom action to access another cross-scope table, the custom action generates a separate access privilege request for approval.


**Parent Topic:**[Configuring flows](configuring-flow-designer.md)

## Upgrade restricted caller access privileges for flows and actions

Allow instances upgraded from San Diego and earlier releases to generate restricted caller access privilege requests for flows and actions.

### Before you begin

If you enable application administration for the target application, only application administrators of the target application can set access to an application. If application administration is not enabled, an admin user can set access to an application.

Role required: application admin or admin

**Note:** To learn about application-specific administrator roles and delegated development, see [Access control rules in application administration apps](https://www.servicenow.com/docs/access?context=ACL-access-checks&version=yokohama&pubname=yokohama-application-development&ft:locale=en-US) and [Delegated development and deployment](https://www.servicenow.com/docs/access?context=c_DelegatedDevelopment&version=yokohama&pubname=yokohama-application-development&ft:locale=en-US).

### About this task

In San Diego and earlier releases, the Restricted Caller Access Privileges table did not recognize flows and actions as source types. Customers who wanted to generate Restricted Caller Access Privileges records for flows and actions could only do so indirectly. They could use a script include or business rule to call a flow or action. When the script include or business rule ran it would generate an access privilege request to the cross-scope resource for approval.

**Warning:** Upgrading restricted caller access privileges to track flows and actions can cause service disruptions on instances that previously tracked cross-scope access from script includes or business rules. After upgrade, all flows and actions that attempt to access restricted resources will be blocked from running and instead generate their own restricted caller access privilege requests for approval. Someone must approve the access privilege requests before cross-scope flows and actions can run. Customers who already allowed indirect tracking of flows and actions using script calls may want to skip this task and continue calling flows and actions from scripts. Customers who want to replace their existing access privileges with the new Flow and Flow Action source types may want to schedule an outage to generate and approve the new access privilege requests.

### Procedure

1.  [Add a system property](https://www.servicenow.com/docs/access?context=r_AvailableSystemProperties&version=yokohama&pubname=yokohama-platform-administration&section=t_AddAPropertyUsingSysPropsList&ft:locale=en-US) .

    Create this property.

    |Field|Value|
    |-----|-----|
    |Name|`com.glide.hub.flow.restricted_caller_access.track_flows_as_source`|
    |Type|**true\|false**|
    |Value|true|

2.  [Define cross-scope access to an application resource](https://www.servicenow.com/docs/access?context=set-RCA-level&version=yokohama&pubname=yokohama-application-development&ft:locale=en-US) .

    Enable Caller Restriction for the tables you want flows and actions to request access to.

3.  If you are replacing existing script-based access-permissions, identify the existing cross-scope flows and actions that need access permissions.

    You must regenerate any existing access privileges for cross-scope flows and actions. The flow and action access privileges replace the existing script include and business rule access privileges.

4.  Generate access privilege requests for any existing cross-scope flows and actions.

    You can run cross-scope flows and actions by using or testing the cross-scope application.

    Cross-scope flows and actions generate access privilege requests to the tables set to caller restriction.

5.  [Allow flows and actions to access your application resources](https://www.servicenow.com/docs/access?context=scope-resource-access&version=yokohama&pubname=yokohama-application-development&ft:locale=en-US) .

    Identify access privilege requests with these source types.

    -   Flow
    -   Flow Action
    Set the Status to **Allowed** for each operation you want a flow or action to perform on your restricted application resource.


### Result

Flows and actions that attempt to access your restricted application resources generate an access privilege request.

### What to do next

Review and approve access privilege requests from your application record.

