---
title: Configure L1 IT Service Desk AI Specialist tasks
description: Select tasks that the L1 IT Service Desk AI Specialist is capable of.Settings that control how the L1 IT Service Desk AI Specialist classifies, triages, investigates, responds to, and reassigns incidents.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/australia/it-service-management/config-tasks-l1-sd-ai-spec-sow.html
release: australia
topic_type: task
last_updated: "2026-10-01"
reading_time_minutes: 11
breadcrumb: [Configure, L1 IT Service Desk AI Specialist, IT Service Management]
---

# Configure L1 IT Service Desk AI Specialist tasks

Select tasks that the L1 IT Service Desk AI Specialist is capable of.

## Before you begin

Role required: sn\_sow\_itsm\_common.sn\_service\_desk\_manager or admin

## Procedure

1.  Navigate to **All** &gt; **Service Operations Workspace**.

2.  On the Homepage, in the **L1 Service Desk AI Specialist** card, select **View details**.

    The L1 IT Service Desk AI Specialist setup page displays sections that you can select to review and configure the details:

    -   Profile
    -   Tasks
    -   Test
    -   Performance
    -   Activity
3.  Select **Tasks** to review or configure the following tasks on how the L1 IT Service Desk AI Specialist makes decisions, acts, and interacts with workflow.

    1.  Configure the Classify and assign section, which changes how the L1 IT Service Desk AI Specialist identifies incidents, classifies them, and assigns a specific incident type for follow-up.

        \[Omitted image "config-task-settings-1\_classify-assign.png"\] Alt text: Screenshot of the Classify and assign configuration section, showing fields for incident identification, classification, and assignment settings.

        See [Classify and assign](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/australia/it-service-management/config-tasks-l1-sd-ai-spec-sow.md) to learn more about the fields in this section.

    2.  Configure the Triage and diagnose section, which changes how the L1 IT Service Desk AI Specialist analyzes the incident for accurate handling.

        \[Omitted image "config-task-settings-2\_triage-diagnose.png"\] Alt text: Screenshot of the Triage and diagnose configuration section, showing fields for incident analysis and handling settings.

        See [Triage and diagnose](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/australia/it-service-management/config-tasks-l1-sd-ai-spec-sow.md) to learn more about the fields in this section.

    3.  Configure the Investigate and resolve section, which changes how the L1 IT Service Desk AI Specialist investigates to find relevant solutions and resolve the issue.

        \[Omitted image "config-task-settings-3\_investigate-resolve.png"\] Alt text: Screenshot of the Investigate and resolve configuration section, showing fields for solution search and issue resolution settings.

        See [Investigate and resolve](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/australia/it-service-management/config-tasks-l1-sd-ai-spec-sow.md) to learn more about the fields in this section.

    4.  Configure the Response formatting section, which changes how the L1 IT Service Desk AI Specialist communicates, to keep the requesters informed through communication channels.

        \[Omitted image "config-task-settings-4\_response-formatting.png"\] Alt text: Screenshot of the Response formatting configuration section, showing fields for communication and notification settings.

        See [Response formatting](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/australia/it-service-management/config-tasks-l1-sd-ai-spec-sow.md) to learn more about the fields in this section.

    5.  Configure the Reassign section, which changes how the L1 IT Service Desk AI Specialist directs unresolved incidents to the right team or agent for timely resolution.

        \[Omitted image "config-task-settings-5\_reassign.png"\] Alt text: Screenshot of the Reassign configuration section, showing fields for routing unresolved incidents to teams or agents.

        See [Reassign](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/australia/it-service-management/config-tasks-l1-sd-ai-spec-sow.md) to learn more about the fields in this section.

4.  Select **Save** to save your changes.

    You can make additional changes to your L1 IT Service Desk AI Specialist before selecting save. Changing tabs in the L1 IT Service Desk AI Specialist guided setup won't lose your changes.

    However, if you don't select **Save** before navigating to a new page or closing the browser, your changes are lost.


## L1 IT Service Desk AI Specialist task setting fields

Settings that control how the L1 IT Service Desk AI Specialist classifies, triages, investigates, responds to, and reassigns incidents.

### Classify and assign

Configure how the L1 IT Service Desk AI Specialist identifies incidents, classifies them, and assigns a specific incident type for follow-up.

<table id="table_oz2_dhw_wkc"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

**Table**

</td><td>

Selects the table where resolution workflows run.

</td></tr><tr><td>

**Fields to predict**

</td><td>

Selects the fields the L1 IT Service Desk AI Specialist classifies when they are empty. Available fields are Category, Subcategory, Service, Service offering, and Configuration item.

</td></tr><tr><td>

**Similar records search profile**

</td><td>

Selects the AI Search profile used to fetch similar records.

</td></tr><tr><td>

**Override existing field values with predictions**

</td><td>

Controls whether AI predictions from similar records can override existing service, offering, and CI values on the incident. When on, predictions can override existing values.

When off, predictions only fill empty fields.

</td></tr></tbody>
</table>[Return to top](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/australia/it-service-management/config-tasks-l1-sd-ai-spec-sow.md)

### Triage and diagnose

Configure how the L1 IT Service Desk AI Specialist analyzes the incident for accurate handling.

<table id="table_pz2_dhw_wkc"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

**Field to use**

</td><td>

Selects the record fields the L1 IT Service Desk AI Specialist uses to analyze next steps.

</td></tr><tr><td>

**Use attachment content**

</td><td>

Controls whether the L1 IT Service Desk AI Specialist scans the content of attached files during incident triage and diagnosis. When on, it scans attachment content.

</td></tr><tr><td>

**Map L1 Service Desk AI Specialist states to record states**

</td><td>

Maps the states of the L1 IT Service Desk AI Specialist execution to the states of the incident record. For example, you can map the L1 IT Service Desk AI Specialist **Awaiting info** state to the incident **On Hold** state.

If you customized state values for your Incident table, you can map them to the L1 IT Service Desk AI Specialist states here.

</td></tr><tr><td>

**Default routing decision**

</td><td>

Defines the routing decision the L1 IT Service Desk AI Specialist falls back to when no routing decision criteria match.-   Attempt resolution: it will attempt to resolve the incident.
-   Reassign: it will reassign the incident.

Attempt resolution is the default.

</td></tr><tr><td>

**Routing criteria**

</td><td>

Adds criteria that determine which records the L1 IT Service Desk AI Specialist handles. Attempt resolution: When an incident matches one of these criteria, the L1 IT Service Desk AI Specialist attempts resolution. Reassign: When an incident matches one of these criteria, the incident is reassigned. For information about adding, editing, and deleting routing criteria, see [Configure routing criteria](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/australia/it-service-management/config-routing-criteria-l1-sd-ai-spec-sow.md).

</td></tr></tbody>
</table>[Return to top](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/australia/it-service-management/config-tasks-l1-sd-ai-spec-sow.md)

### Investigate and resolve

Configure how the L1 IT Service Desk AI Specialist investigates to find relevant solutions and resolve the issue.

<table id="table_qz2_dhw_wkc"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

**Knowledge sources**

</td><td>

Selects a search profile that defines how the L1 IT Service Desk AI Specialist retrieves knowledge articles for investigation and resolution, so it uses relevant, accurate content to support incident handling. AI search profiles can include sources such as knowledge articles, ServiceNow documentation, or specific tables. You can create new AI Search profiles specifically for your L1 IT Service Desk AI Specialist. To customize the information the L1 IT Service Desk AI Specialist can access, add search profiles alongside the preinstalled ones, or remove them. Select at least one search profile for the L1 IT Service Desk AI Specialist to complete the Investigate and resolve task.

**Note:** To ensure that the L1 IT Service Desk AI Specialist can search a table from your instance, grant it access through its assigned roles. Without access, it can't search that table.

</td></tr><tr><td>

**Automatically create KFT records**

</td><td>

Controls whether the L1 IT Service Desk AI Specialist creates a KB Feedback Task \(KFT\) for `solution_proposed` resolutions that reference no existing KB article.When on, it creates the KFT automatically, which surfaces knowledge gaps for content authors to address.

</td></tr><tr><td>

**Execution mode**

</td><td>

Determines how autonomously the L1 IT Service Desk AI Specialist acts. -   **Autonomous**: Marks a ticket as resolved after it sends the resolution steps.
-   **Supervised**: Requires a human to accept its resolution proposal.

</td></tr><tr><td>

**Auto-submit catalog requests**

</td><td>

Controls whether the L1 IT Service Desk AI Specialist submits the catalog request on the employee's behalf when it has filled all required variables. When on: If there are no required variables, it submits the catalog request automatically. If there are required variables and the L1 IT Service Desk AI Specialist can fetch the information, it fills in those variables. If there are required variables and the L1 IT Service Desk AI Specialist can't fetch the information, it contacts the employee. It engages for as many replies as the **Replies before reassigning** setting allows, for example, three replies. Answering one variable can make other variables visible or required, based on the catalog item's configuration, and the L1 IT Service Desk AI Specialist requests these in the replies. After that, the L1 IT Service Desk AI Specialist auto-submits the catalog request. If it still does not have enough information, it creates a draft and routes it to the employee to complete.

When off: the L1 IT Service Desk AI Specialist sends the employee a link to the catalog item to create a request manually.

If the requester portal is an AIUX experience, the L1 IT Service Desk AI Specialist doesn't create a draft or ask follow-up questions on the incident. When auto-submit is on, it fills the variables once and submits the request if it filled every required variable. Otherwise, and when auto-submit is off, it sends the employee a link to the catalog item.

</td></tr><tr><td>

**Flag high-risk resolution steps**

</td><td>

Controls whether resolutions that require elevated access, backend changes, or irreversible actions go to a service desk agent instead of the requester. When on, these resolutions are sent to a service desk agent.

</td></tr></tbody>
</table>[Return to top](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/australia/it-service-management/config-tasks-l1-sd-ai-spec-sow.md)

### Response formatting

Configure how the L1 IT Service Desk AI Specialist communicates to keep requesters informed through communication channels.

<table id="table_rz2_dhw_wkc"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

**Inbound channels**

</td><td>

Selects the inbound channels, such as Activity stream, through which the L1 IT Service Desk AI Specialist receives messages from requesters.

</td></tr><tr><td>

**Outbound channels**

</td><td>

Selects the outbound channels the L1 IT Service Desk AI Specialist uses to send responses or notifications, such as Activity stream, email, portal, or phone. You can also set the preferred message format, such as HTML or plain text.

</td></tr><tr><td>

**Internal communication when confidence is low**

</td><td>

Controls whether the L1 IT Service Desk AI Specialist logs its solution as a work note rather than proposing it directly. When on, it logs the solution as a work note.

</td></tr><tr><td>

**Response templates**

</td><td>

Sets how the L1 IT Service Desk AI Specialist writes its message for each of three states: Follow up, Propose a solution, and Reassign to human. For each state, select **Dynamic** or **Template** authoring mode. The selector is independent per response type, and switching modes doesn't delete content saved in the other mode. **Template**: Defines the message the L1 IT Service Desk AI Specialist sends to the requester. Use the editor to add formatting such as bold text, specific fonts, tables, highlighting, links, and bullets. This is the default mode. **Dynamic**: The L1 IT Service Desk AI Specialist composes the full customer-facing message, using the instruction as additional grounding alongside its existing prompting. No placeholder substitution occurs in this mode.Catalog question messages aren't configured here. See [Catalog auto submission](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/australia/it-service-management/catalog-variable-collection-slot-fill-l1-sd-ai-spec.md).

</td></tr><tr><td>

**Requester reference portal**

</td><td>

Selects the portal that opens when a requester selects a knowledge article or catalog item link in the L1 IT Service Desk AI Specialist responses. The L1 IT Service Desk AI Specialist uses your instance's default portal unless you select another. You can select a Service Portal or an AIUX experience. Only users with the admin role can view and change this setting. If the portal you select is inactive or deleted, it uses the default portal. If the instance also has no active default portal, links open in the platform view. This setting also applies to links to requests and requested items. Links in work notes aren't affected and open in the platform view.

</td></tr></tbody>
</table>[Return to top](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/australia/it-service-management/config-tasks-l1-sd-ai-spec-sow.md)

### Reassign

Configure how the L1 IT Service Desk AI Specialist directs unresolved incidents to the right team or agent for timely resolution.

<table id="table_sz2_dhw_wkc"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

**Maximum number of interactions before escalation**

</td><td>

Sets how many times the L1 IT Service Desk AI Specialist contacts the requester before sending the incident to an agent. Enter a number greater than zero.

</td></tr><tr><td>

**Reassign on follow-up question**

</td><td>

Controls whether the ticket goes to a human agent when the requester asks a follow-up question. When off, the L1 IT Service Desk AI Specialist handles follow-ups. If you select Dynamic mode for Reassign to human, the L1 IT Service Desk AI Specialist uses your instruction to write the reassignment message instead of posting a generic template.

</td></tr><tr><td>

**Stuck monitor filter**

</td><td>

Sets the filter that identifies incidents considered stuck and in need of escalation.

</td></tr><tr><td>

**Choose where to reassign records**

</td><td>

Selects the assignment group or specific person to reassign the ticket to after the L1 IT Service Desk AI Specialist reviews it and chooses to reassign it.

</td></tr><tr><td>

**Cross-group reassignment**

</td><td>

Controls whether the L1 IT Service Desk AI Specialist surfaces a routing recommendation when a different assignment group consistently resolves similar incidents. Off: No recommendation. Recommend only: Posts a recommendation and unassigns the L1 IT Service Desk AI Specialist. The assignment group is never changed.

</td></tr><tr><td>

**Cross-group reassignment**

</td><td>

Controls how the L1 IT Service Desk AI Specialist handles an incident when a different assignment group consistently resolves similar resolved incidents. Service desk managers can edit this setting.-   **Off**: No action. This is the default.
-   **Recommend only**: Posts a recommendation and unassigns the L1 IT Service Desk AI Specialist. The assignment group is never changed.
-   **On**: Reassigns the incident autonomously. It sets the assignment group to the recommended group and unassigns the L1 IT Service Desk AI Specialist. It doesn't use the **Choose where to reassign records** setting.

The cross-group check runs before the L1 IT Service Desk AI Specialist does any resolution work, so **On** reassigns the incident even in supervised execution mode. For more information, see [Cross-group reassignment](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/australia/it-service-management/cross-group-reassignment-l1-sd-ai-spec.md).

</td></tr></tbody>
</table>[Return to top](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/australia/it-service-management/config-tasks-l1-sd-ai-spec-sow.md)

