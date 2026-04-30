---
title: Integrate New Relic platform events
description: Integrate New Relic with Event Management by adding a standard webhook in the New Relic old and new consoles.
locale: en-US
release: yokohama
product: Event Management
classification: event-management
topic_type: task
last_updated: "2025-01-30"
reading_time_minutes: 4
breadcrumb: [Integrate with push connectors, Configure a push connector, Configure Event Management connectors, Event Management Integrations, Configuring Event Management, Event Management, ITOM AIOps, IT Operations Management]
---

# Integrate New Relic platform events

Integrate New Relic with Event Management by adding a standard webhook in the New Relic old and new consoles.

## Before you begin

Verify that the Event Management Connectors \(sn\_em\_connector\) plugin is installed on the ServiceNow AI Platform instance.

Role required: evt\_mgmt\_integration

## About this task

Configure the Event Management environment for the collection of events from New Relic by authenticating New Relic as a data source. Set your ServiceNow AI Platform instance as the rest endpoint using a standard webhook. Use procedure step 1 for the new console. Use procedure step 2 for the old console.

Starting from the Xanadu release, the OOTB \(Out-Of-The-Box\) event rules provided with the connector, which you have not previously used \(i.e., neither activated, deactivated, nor modified\), will now have the **Apply additional matching rules** check box set to true. Previously, this check box was disabled. This change allows you to execute more event rules or automation using the same filter conditions for the events.

**Note:** This feature applies only to active event rules.

## Procedure

1.  For the new console:

    1.  Create a destination.

        1.  Navigate to**Alerts &amp; AI** &gt; **Destinations**.
        2.  In the**Add destinations**section, select the**Webhook**channel type.
        3.  In the**Webhook name** field, enter the webhook name.
        4.  In the**Endpoint URL** field enter:`https://<InstanceName>.service-now.com/api/sn_em_connector/em/inbound_event?source=newrelic`
        5.  In the**Basic Auth**section, enter your user name and password.

            **Note:** Verify the evt\_mgmt\_integration role is assigned to the selected user. To ensure proper authentication, use the least privileged user with the evt\_mgmt\_integration role, rather than a high privileged user.

        6.  Select**Save destination**.
    2.  Create a policy.

        1.  Navigate to**Alerts &amp; AI** &gt; **Alert Conditions &amp; Policies**.
        2.  Select**New Alert policy**and define a policy.
        3.  Select**Set up Notifications**.
        4.  In the**Add Channel**section select**Webhook**, and then select the destination that you created in the previous substep.
        5.  In the**Payload template**section, paste the following JSON payload.

            ```
            { "account_id": {{nrAccountId}}, "account_name": {{json accumulations.tag.account.[0]}}, "closed_violations_count": {{closedIncidentsCount}}, "open_violations_count": {{openIncidentsCount}}, "condition_description": "{{escape accumulations.conditionDescription.[0]}}", "condition_family_id": {{accumulations.conditionFamilyId.[0]}}, "condition_name": "{{escape accumulations.conditionName.[0]}}", "current_state": {{json state}}, "details": {{json issueTitle}}, "duration": {{#if issueDurationMs}}{{issueDurationMs}}{{else}}0{{/if}}, "event_type": "INCIDENT", "incident_acknowledge_url": {{json issueAckUrl}}, "incident_id": {{json issueId}}, "incident_url": {{json issuePageUrl}}, "metadata": { {{#if locationStatusesObject}}"location_statuses": {{json locationStatusesObject}},{{/if}} {{#if accumulations.metadata_entity_type}}"entity.type": {{json accumulations.metadata_entity_type.[0]}},{{/if}} {{#if accumulations.metadata_entity_name}}"entity.name": {{json accumulations.metadata_entity_name.[0]}},{{/if}} "section": "metadata" }, "owner": {{json owner}}, "policy_name": {{json accumulations.policyName.[0]}}, "policy_url": {{json policyUrl}}, "runbook_url": {{json accumulations.runbookUrl.[0]}}, "severity": {{json priority}}, "targets": [ { "id": "{{labels.targetId.[0]}}", "name": "{{#if accumulations.targetName}}{{escape accumulations.targetName.[0]}}{{else if entitiesData.entities}}{{escape entitiesData.entities.[0].name}}{{else}}N/A{{/if}}", "link": "{{issuePageUrl}}", "product": "{{accumulations.conditionProduct.[0]}}", "type": "{{#if entitiesData.types.[0]}}{{entitiesData.types.[0]}}{{else}}N/A{{/if}}", "labels": { {{#each accumulations.rawTag}}"{{escape @key}}": {{#if this.[0]}}{{json this.[0]}}{{else}}"empty"{{/if}}{{#unless @last}},{{/unless}}{{/each}} } } ], "timestamp": {{updatedAt}}, "violation_callback_url": {{json issuePageUrl}}, "violation_chart_url": {{json violationChartUrl}} }
            ```

        6.  Select**Send test notification**to get the test event in your ServiceNow instance.
        7.  Select**Save message**.
        8.  Select**Activate workflow**to activate the workflow.
    3.  Create alert conditions to apply to the policy:

        1.  Navigate to**Alerts &amp; AI** &gt; **Alert Conditions &amp; Policies**.
        2.  Select**Create alert condition**, define the required alert details, and add it to the policy you created in the previous step.
        3.  Select**Save Condition**.
2.  For the old console.

    1.  Create a notification channel.

        1.  Navigate to**Alerts &amp; AI** &gt; **Notification channels**.
        2.  In the**Channel details**tab, select the**Webhook**channel type.
        3.  In the**Base Url**text box, enter:`https://<InstanceName>.service-now.com/api/sn_em_connector/em/inbound_event?source=newrelic`
        4.  In the Basic Auth section, enter the user name and password of the relevant user.

            **Note:** Verify the evt\_mgmt\_integration role is assigned to the selected user. To ensure proper authentication, use the least privileged user with the evt\_mgmt\_integration role, rather than a high privileged user.

        5.  In the**Custom Payload**section, select**Add Custom Payload**, and select the**JSON**payload type.
        6.  Paste the following JSON payload into the**Custom Payload**.

            ```
            { "account_id": "$ACCOUNT_ID", "account_name": "$ACCOUNT_NAME", "closed_violations_count_critical": "$CLOSED_VIOLATIONS_COUNT_CRITICAL", "closed_violations_count_warning": "$CLOSED_VIOLATIONS_COUNT_WARNING", "condition_description": "$DESCRIPTION", "condition_family_id": "$CONDITION_FAMILY_ID", "condition_name": "$CONDITION_NAME", "current_state": "$EVENT_STATE", "details": "$EVENT_DETAILS", "duration": "$DURATION", "event_type": "$EVENT_TYPE", "incident_acknowledge_url": "$INCIDENT_ACKNOWLEDGE_URL", "incident_id": "$INCIDENT_ID", "incident_url": "$INCIDENT_URL", "metadata": "$METADATA", "open_violations_count_critical": "$OPEN_VIOLATIONS_COUNT_CRITICAL", "open_violations_count_warning": "$OPEN_VIOLATIONS_COUNT_WARNING", "owner": "$EVENT_OWNER", "policy_name": "$POLICY_NAME", "policy_url": "$POLICY_URL", "runbook_url": "$RUNBOOK_URL", "severity": "$SEVERITY", "targets": "$TARGETS", "timestamp": "$TIMESTAMP", "violation_callback_url": "$VIOLATION_CALLBACK_URL", "violation_chart_url": "$VIOLATION_CHART_URL" }
            ```

    2.  Create a policy.

        1.  Navigate to**Alerts &amp; AI** &gt; **Policies**.
        2.  Select**New Alert policy**and define a policy.
        3.  In the**Notification Channels**section, select**Add**, select**Webhook**, and then select the channel you created in the previous step.
    3.  Create alert conditions to apply to the policy:

        1.  Navigate to**Infrastructure** &gt; **Settings** &gt; **Alerts**.
        2.  Select**Create alert condition**, define the required alert details, add it to the policy you created in the previous step.
        3.  Select**Create**.

## Result

Alerts start flowing from the New Relic console into the Event Management plugin. The plugin extracts information from the original New Relic alert message to populate the required event fields and inserts the event into the database. In your ServiceNow AI Platform instance, navigate to**All Events**to see the events.

**Note:** By default, host binding is enabled for New Relic events for all providers \(Azure/AWS/GCP\). If all hosts in the environment are discovered using Cloud Discovery by providing credentials and discovered resources are in the cmdb\_ci\_vm\_object list, then the VM binding may not occur. To resolve this, you must enable the**New Relic - General**event rule. For further information about Event rules, see [Event rules](../concept/create-event-rules.md).

-   **[Integrate New Relic with REST API key token](integrate-newrelic-api-key.md)**  
Integrate using an API key to establish secure communication and automate data exchange via REST API. This simplifies integration, enabling seamless access to services and enhancing operational efficiency.

**Parent Topic:**[Integrate with push connectors](configure-listener-transform-script.md)

