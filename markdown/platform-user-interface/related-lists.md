---
title: Getting information related to the open record
description: Use related items to gather information about and to enter information into the open record.
locale: en-US
release: xanadu
topic_type: reference
last_updated: "2024-08-01"
reading_time_minutes: 3
breadcrumb: [Getting or adding information to a record, Working on records in your Workspace, Using Configurable Workspace, Configurable Workspace UI, Configure UIs and portals, Configure user experiences]
---

# Getting information related to the open record

Use related items to gather information about and to enter information into the open record.

![Related items menu](../image/Related-items-menu.png)

The items in the Related items menu behave like tabs. When you click one, the corresponding content appears in the form pane. Workspace underlines the item that's active in the form pane. What items appear in the menu, what order they're in, and which one opens automatically are configurable by your system administrator.

The items contain information related to the record open in the form pane. You click the different items to get contextual information. For example, if the open incident is about a failed service, you might click **Impacted Services/CIs** to see if other services are also down. If the incident is a power outtage, you might click **Outages** to see if there are outages in other locations.

The **Details** item usually displays first by default. It is the only item that contains details of the open record. It also provides text fields that you can edit. For example, when you solve an issue, you should enter the resolution description in the section, **Resolution notes**. Your system administrator determines which fields from a record appear in the form pane.

Your configuration of workspace might include the following related items.

<table id="table_ol3_hlr_vjb"><thead><tr><th>

Item

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Details

</td><td>

Detailed information about the open record and text fields for you to enter information. The system administrator specifies the record fields that appear in the form pane. You use this item to read about the open record and to make entries in the record.

</td></tr><tr><td>

Task SLAs

</td><td>

Service level agreements \(SLAs\) for a task. Expected deadlines for resolving a task of this type.

</td></tr><tr><td>

Affected CIs

</td><td>

Configuration items \(CIs\) related to an incident. Often, an incident is related to one or more specific configuration items \(CIs\). If the configuration management database \(CMDB\) is populated, the CI records hold valuable information to help resolve incidents. You can associate configuration items to an incident to see how the incident affects dependent CIs.

</td></tr><tr><td>

Impacted Services/CIs

</td><td>

Services and configuration items \(CIs\) affected by this incident.

</td></tr><tr><td>

Child incidents

</td><td>

Child incidents are incidents related to the parent incident, the incident open in record view. All work notes or comments in a parent incident are copied into a child incident. When a parent incident is resolved, the child incidents are resolved.

</td></tr><tr><td>

Outages

</td><td>

Service outages related to the incident open in record view.

</td></tr><tr><td>

User's Calls

</td><td>

The **User’s Calls** related list displays historical calls between a requester and Service Desk agents. This feature is available to the users who has the Service Desk Call plugin \(com.snc.service\_desk\_call\) already activated. **Note:** The customer name in the **Opened for** field in Interaction is matched with the **Caller** field in Service Desk calls and records are retrieved based on the number of days mentioned in the interaction property **Number of days \(integer\) for which past user call records are retrieved. The default value is seven \(7\). A setting of zero \(0\) disables this feature.** \(**glide.new\_call.interaction.records\_age**\).

</td></tr><tr><td>

User's Task

</td><td>

When a requester contacts an agent through chat, phone call, request, or walk-in, the **User’s Task** related list shows the agent all of the other tasks \(incident, problem, change request, request, and so on\) that have been created for the requester. For example, if a requester calls about the status of a request that was made the previous day, the **User’s Task** related list shows the request. Workspace includes the other tasks in the **User’s Task** related list when the value for the **Opened for** field in the interaction record matches the:-   **Caller** field in an incident record
-   **Opened by** field in a problem record
-   **Requested by** field in a change record
-   **Requested for** field in a Service Catalog record

</td></tr></tbody>
</table>