---
title: Create a saved external trigger
description: Save a set of trigger definitions as a reusable trigger that responds to external events through webhooks. When an event occurs in the configured third-party application that meets the specified conditions, the trigger is activated.
locale: en-US
release: australia
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 4
---

# Create a saved external trigger

Save a set of trigger definitions as a reusable trigger that responds to external events through webhooks. When an event occurs in the configured third-party application that meets the specified conditions, the trigger is activated.

## About this task

Create a saved trigger that responds to events occurring in a supported third-party spoke that is already configured in Workflow Studio. When an event occurs, the third-party spoke sends the event payload to Workflow Studio.

In the trigger definition, you specify:

-   The event payload structure in JSON format
-   The conditions that determine when the trigger starts

Obtain the event payload JSON from the third-party spoke that you configure.

## Before you begin

Role required: trigger\_designer, flow\_designer, or admin

Subscription required: This step requires an Integration Hub subscription.

Plugins required: Install the following Integration Hub plugins:

-   ServiceNow Integration Hub External Trigger \[com.glide.ih.external\_trigger\]: To use out of the box external triggers.

-   External Trigger Builder \[sn\_ext\_trg\_bldr\]: To create a saved external trigger.


**Note:** For information about what is included with different Integration Hub subscriptions, see [Legal schedules - Integration Hub overview](https://www.servicenow.com/content/dam/servicenow-assets/public/en-us/doc-type/legal/snc-addendum-integrationhub.pdf)

Create the required event sources in the Event source builder, or use the existing event sources from these spokes.

-   Jira Spoke
-   GitHub Spoke
-   Docusign eSignature Spoke
-   Microsoft Azure DevOps Boards Spoke

For more information about creating an event source, see [Create an external event source](manage-external-event-sources.md#).

**Important:** Keep the event payload JSON of the third-party application handy. Refer to the third-party webhook documentation to identify where you can copy the event payload JSON. For example, see the following link for Jira event payloads: [Executing a webhook](https://developer.atlassian.com/server/jira/platform/webhooks/#executing-a-webhook).

## Procedure

1.  Navigate to **All** &gt; **Process Automation** &gt; **Workflow Studio**.

2.  From the Workflow Studio home page, select **New** &gt; **Trigger**.

3.  On the form, fill in the fields.

    |Field|Description|
    |-----|-----------|
    |Trigger name|Name to identify the trigger.|
    |Trigger type|The type of the trigger to start your flow. Under External, select **Event \(Webhook\)**.|
    |Description|Description of the trigger.|
    |Application|Application scope to create the trigger. Workflow Studio displays the configured spokes that are supported.|
    |Event source|The third party system that will send the events to ServiceNow.|
    |Domain|Domain scope of the flow. For more information about domain separation, see [Domain separation explained](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/platform-security/bp-what-is-domain-separation.md).|

4.  Select **Show additional properties** and fill in the fields.

    |Field|Description|
    |-----|-----------|
    |Accessible from|The trigger data is accessible from all application scopes.|
    |Category|The category where your trigger is displayed.|
    |Trigger annotation|Annotation for your trigger that the user can see before they select the trigger.|

5.  Select **Build trigger**.

    Workflow Studio displays the Trigger definition page. In the Event source preview area, you can view information about how the external trigger endpoint is configured. Configurations you make to the trigger are auto-saved.

6.  Under **Parser**, fill in the fields.

    |Field|Description|
    |-----|-----------|
    |Trigger output name|Label to identify the trigger output.|
    |Request headers|Optional field to specify one or more headers to be included in the inbound request.|
    |Query parameters|Optional field to specify one or more parameters to be included in the inbound request.|

7.  Under **Body**, in **JSON editor**, paste the payload JSON from the third-party application.

    Refer to the third-party webhook documentation to learn about from where you can copy the payload JSON. ![Shows the JSON editor where you paste the payload data in JSON.](../images/json-editor-1.jpg)

8.  Select **Visualize objects**.

    The editor displays the objects that are in the payload JSON. You can reorder or remove the objects. The objects are available as data pills to use in conditions. ![Displays the objects after you select Visualize objects.](../images/json-editor-2.jpg)

9.  In **Condition editor**, drag and drop the data pills to create a condition set.

    Use **and** or **or** operator to add more conditions to the condition set.

10. Select **+New condition set** to add additional condition sets, as required.

11. Select **Publish** to make the trigger available for use.

    **Note:** Once the trigger is published, you can edit only the output **Label** fields.


## Result

The trigger is created and published. You can use the trigger in any of your flows. For information about adding a trigger to a flow, see [Use a saved trigger](use-saved-trigger.md).

-   **[Managing external event sources](manage-external-event-sources.md#)**  
Create and manage external event sources for a spoke or a scoped application that listen to events occurring in an application outside ServiceNow. Then, you can create external trigger definitions and associate them with the external event sources. When the event that you specify in the external trigger definition occurs, it starts one or more flows on your ServiceNow instance.

**Parent Topic:**[Building triggers](../concept/building-triggers.md)

