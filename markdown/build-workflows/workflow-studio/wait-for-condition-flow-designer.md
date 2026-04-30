---
title: Wait For Condition action
description: Pause a flow until record values match a specific set of conditions.
locale: en-US
release: xanadu
product: Workflow Studio
classification: workflow-studio
topic_type: reference
last_updated: "2024-08-14"
reading_time_minutes: 8
breadcrumb: [Workflow Studio actions, Flows, subflows, and actions reference, Workflow Studio reference, Workflow Studio, Build workflows]
---

# Wait For Condition action

Pause a flow until record values match a specific set of conditions.

## Roles and availability

Available as a Workflow Studio ServiceNow core action. Users with the flow\_designer or admin role can add an action to a flow and define configuration details.

## Inputs

Provide a value for each input that your flow needs. To add dynamic values, you can also drag and drop pills from the Data panel or select them from the pill picker.

-   **Record**

    Data type: **Record**

    The record whose field values the action monitors for changes. This record can come from a flow trigger, a subflow input, or the output of a previous flow step.

    **Note:** If this record is deleted, the flow stops waiting and continues running.

-   **Table**

    Data type: **Table Name**

    The table associated with the record to monitor. This read-only value is set to the table associated with the record you selected. Confirm that the system supports Wait for Condition for your selected table. For a list of unsupported tables, see the Unsupported tables section.

-   **Conditions**

    Data type: **Conditions**

    The record values necessary to resume running the flow. For example, if the condition is **\[State\]** **\[is\]** **\[Closed\]**, the flow pauses until the condition is met. Once met, the flow moves on to the next flow step. Only select conditions that apply to field values in the table to which the record belongs. See Condition evaluation for more information about creating valid conditions.

    **Note:** For conditions that depend on a specific duration, consider using [Wait for a duration flow logic](../concept/flow-logic-wait-for-a-duration.md) instead.

-   **Enable Timeout**

    Data type: **True/False**

    Option to limit the amount of time that the flow waits for the action to be completed before continuing.

    **Note:** Use the **Enable timeout** option to prevent this action from continuing to run. If the condition to continue is never met, a timeout value specifies when the system skips the Wait for Condition action and goes to the next item in the flow. You must set a Duration value to enable a timeout. You can also select a Schedule if you want to compute the duration end date based on a specific work schedule.

-   **Duration**

    Data type: **Duration**

    Amount of time that the flow waits before continuing when the **Enable timeout** option is selected. Enter the time to wait in hours, minutes, and seconds. If you leave this field empty, the flow does not wait.

-   **Schedule**

    Data type: **Choice**

    Schedule used to compute the timeout duration when the **Enable timeout** option is selected. For example, waiting for 10 hours as part of an 8-5 weekdays schedule causes the flow to wait for one or more business days. If you leave this field empty, the timeout runs without a schedule.


## Outputs

These outputs appear in the Data panel. You can use them as inputs elsewhere in your flow.

-   **State**

    Data type: **Choice**

    The completion status of the action as a numeric value.

    -   0 \(success\)
    -   1 \(error\)

## Condition evaluation

The Wait for Condition action only evaluates the wait condition when there are changes to fields in the **Record** you select. A valid wait condition meets these criteria.

-   Each condition evaluates a field from the table to which the record belongs.

    **Note:** Don't create conditions that dot-walk to another table or depend upon catalog item variables from a related record.

-   Each condition specifies a field value change rather than a relative time period.

    **Note:** For conditions that depend on a specific duration, consider using [Wait for a duration flow logic](../concept/flow-logic-wait-for-a-duration.md) instead.


In this example, the wait condition is valid because the **State** field belongs to the Incident table and the condition is a field value change to **Closed**.

![Condition met for a Wait for Condition action in Flow Designer.](../images/wait-for-condition-flow-met-example.png "Valid wait condition")

In this example, the wait condition is invalid because it is a time relative to the **Created** date. Actions that have a condition that relies on a time interval will not be met, so the action is never performed.

![Condition not met for a Wait for Condition action in Flow Designer.](../images/wait-for-condition-flow-not-met-example.png "Invalid wait condition")

## Wait for incident state closed

![Condition met for a Wait for Condition action in Flow Designer.](../images/wait-for-condition-flow-met-example.png)

In this example, a subflow provides an incident record as an input to the Wait For Condition action. The condition is valid because it uses a field value from the Incident table.

## General guidelines

Follow these general guidelines when creating flows that wait for a condition.

-   **Add trigger conditions instead of wait conditions to start flows**

    If you only want a flow to run when certain record conditions are met, create a flow with a record trigger instead of starting and pausing a flow. A waiting flow consumes more system resources than a flow trigger.

-   **Cancel flows whose resume conditions can never occur**

    Prevent your flows from waiting indefinitely by specifying flow stop conditions with [End Flow flow logic](../concept/flow-logic-end-action.md). To free up system resources, you can also cancel any flow whose resume conditions can never be met. For example, cancel flows waiting for incident record updates where the related incident is closed.

-   **Provide at least one condition to resume a flow**

    The Wait For Condition action requires at least one condition to resume running a flow. If you want to pause a flow for a specific amount of time, use the [Wait for a duration of time flow logic](../concept/flow-logic-wait-for-a-duration.md) instead.

-   **Restrict wait conditions to fields present on the current table**

    The Wait For Condition action can only monitor changes to the fields of the table to which the record belongs. Don't create conditions that dot-walk to fields in other tables. The action can't detect changes to fields in related records or catalog variables. For example, if an action waits for changes to an Incident record, then it cannot detect changes to a related record such as a catalog item or change task record. Instead of building wait conditions that dot-walk to another record, look up the related record whose value you want to monitor and use that record as the input of your Wait for Condition action. Avoid building wait conditions that rely on catalog variables.

-   **Use a conditions data pill to specify dynamic conditions**

    To enable flow designers to dynamically apply conditions, define an input of type Conditions and drag-and-drop the input data pill into the **Conditions** field.


## Unsupported tables

The system does not support Wait for Condition for the following tables.

|Table Category|Table Names|
|--------------|-----------|
|Audit|Sys Audit \[sys\_audit\], Audit Deleted Record \[sys\_audit\_delete\], Audit Relationship Change \[sys\_audit\_relation\], Audit Roles \[sys\_audit\_role\], Audit Relationship Change \[sys\_audit\_relation\], Audit Deleted Record \[sys\_audit\_delete\]|
|Email|Email \[sys\_email\], Email Account \[sys\_email\_account\], Email Log \[sys\_email\_log\]|
|Events|Event \[sysevent\], Notification \[sysevent\_email\_action\], Stationery \[sysevent\_email\_style\], Email Template \[sysevent\_email\_template\], Inbound Email Actions \[sysevent\_in\_email\_action\], Slow Event \[sysevent\_pattern\], Event Registration \[sysevent\_registration\], Script Action \[sysevent\_script\_action\]|
|Import Sets|Import Set \[sys\_import\_set\], Import Set Row \[sys\_import\_set\_row\], Import Set Row Error \[sys\_import\_set\_row\_error\], Transform History \[sys\_import\_set\_run\], Computer \[imp\_computer\], Notification \[imp\_notification\], Location \[imp\_location\], User \[imp\_user\]|
|JRobin|JRobin Database \[jrobin\_database\], JRobin Shard \[jrobin\_shard\], Graph Line \[jrobin\_graph\_line\], JRobin Shard Fragments \[jrobin\_shard\_location\], Member \[jrobin\_graph\_set\_member\], Round Robin Archive \[jrobin\_archive\], Round Robin Data Source \[jrobin\_datasource\], Round Robin Definition \[jrobin\_definition\], Round Robin Graph \[jrobin\_graph\], Round Robin Graph Set \[jrobin\_graph\_set\]|
|Logs|Log Entry \[syslog\], Service Portal Log Entry \[sp\_log\]|
|MID Server|MID Server Property \[ecc\_agent\_property\], Mid Server Log \[ecc\_agent\_log\], Queue \[ecc\_queue\], Configuration \[ecc\_queue\_config\], ECC Queue Statistics \(by ECC Agent\) \[ecc\_queue\_stats\_by\_ecc\_agent\]|
|Performance Analytics|Job Log \[pa\_job\_logs\]|
|Record Watcher|Responders \[sys\_rw\_action\], Channel Responders \[sys\_rw\_amb\_action\]|
|Reporting|Summary Set \[sys\_report\_summary\], Report Summary Line \[sys\_report\_summary\_line\]|
|Scheduled Jobs|Schedule Item \[sys\_trigger\], Broadcast Message \[sys\_broadcast\_message\], Broadcast Message Relationships \[sys\_broadcast\_message\_m2m\], Progress Worker \[sys\_progress\_worker\], Progress Worker Domain \[sys\_progress\_worker\_domain\]|
|SSO|SSO Properties \[sso\_properties\], Digest Token Properties \[digest\_properties\], SAML Update 1 Properties \[saml2\_update1\_properties\], SSO Federation \[sso\_federation\]|
|System Cache|Cache Flush \[sys\_cache\_flush\], Cache Entry \[sys\_db\_cache\]|
|System Clone|ServiceNow Instance \[instance\], Clone Security Token \[clone\_token\], Preserved Data \[clone\_preserved\_data\]|
|System Dictionary|Dictionary Entry Override \[sys\_dictionary\_override\]|
|System Events|Event Processor \[sys\_event\_processor\]|
|System Fields|Field Class \[sys\_glide\_object\]|
|System Performance|Component Status \[sys\_status\], Cluster Message \[sys\_cluster\_message\], Node State \[sys\_cluster\_state\]|
|Text Index|Ts Attachment \[ts\_attachment\], Text Index Attribute Map \[ts\_attribute\_map\], Ts Chain \[ts\_chain\], Chain Summary \[ts\_chain\_summary\], Text Index Column Attribute Map \[ts\_column\_attribute\_map\], Text Index Configuration \[ts\_configuration\], Text Index Configuration Attribute \[ts\_configuration\_attribute\], Ts Delete Doc \[ts\_deleted\_doc\], Ts Document \[ts\_document\], Ts Field \[ts\_field\], Text Search Groups \[ts\_group\], Japanese User Token \[ts\_japanese\_token\_dictionary\], Ts Phrase \[ts\_phrase\], Global Searches \[ts\_query\], Knowledge Searches \[ts\_query\_kb\], Text Search Stat \[ts\_search\_stats\], Text Search Summaries \[ts\_search\_summary\], Stop Word \[ts\_stop\], Synonym Dictionary \[ts\_synonym\_dictionary\], Synonym Set \[ts\_synonym\_set\], Text Search Table \[ts\_table\], Text Index Table Attribute Map \[ts\_table\_attribute\_map\], Service Catalog Searches \[sc\_ts\_query\], Ts Word \[ts\_word\], Ts Word Roots \[ts\_word\_roots\]|
|Update Sets|Update Set \[sys\_update\_set\], Update Version \[sys\_update\_version\], Customer Update \[sys\_update\_xml\], Update Set Log \[sys\_update\_set\_log\]|
|Upgrades|System Upgrades \[sys\_upgrade\_history\], Upgrade Details \[sys\_upgrade\_history\_log\], System Upgrade Metric \[sys\_upgrade\_metric\], Upgrade Blame Log \[sys\_upgrade\_blame\], Upgrade Manifest \[sys\_upgrade\_manifest\], Upgrade State \[sys\_upgrade\_state\]|
|Usage Analytics|Usage Data for Applications \[ua\_app\_usage\], UsageAnalytics Count Configurations \[usageanalytics\_count\_cfg\], Application Metadata \[ua\_app\_metadata\], UsageAnalytics Count for Tables \[usageanalytics\_count\], Subscription \[license\_details\], Role for Subscription \[role\_has\_license\]|
|Users|User Session \[sys\_user\_session\], User Token \[sys\_user\_token\], User Preference \[sys\_user\_preference\], Navigator History \[sys\_ui\_navigator\_history\]|
|Workflow|Workflow Execution \[wf\_workflow\_execution\], Workflow History \[wf\_history\], Workflow Executing Activity \[wf\_executing\], Workflow Queued Command \[wf\_command\], Workflow Context \[wf\_context\], Workflow Transition History \[wf\_transition\_history\]|

**Parent Topic:**[Workflow Studio actions](../concept/flow-actions.md)

