---
title: Getting started with Remote Process Sync
description: Learn the basics of setting up a Remote Process Sync integration in order to link the automated processes among two or more ServiceNow instances together.
locale: en-US
release: australia
product: Integration Hub Remote Process Sync
classification: integration-hub-remote-process-sync
topic_type: reference
last_updated: "2026-03-12"
reading_time_minutes: 20
breadcrumb: [Integration Hub Remote Process Sync, Workflow Data Fabric]
---

# Getting started with Remote Process Sync

Learn the basics of setting up a Remote Process Sync integration in order to link the automated processes among two or more ServiceNow® instances together.

**Note:** Integration Hub Remote Process Sync requires a subscription to the Integration Hub Enterprise package. For more information, see [Request Integration Hub](../../flow-designer/concept/request-ih-overview.md).

## Before getting started with your Remote Process Sync integration

Before deciding to move forward with Remote Process Sync as your integration framework, consider how this framework compares to other multi-instance ServiceNow AI Platform® integrations. While solutions such as [Instance Data Replication](https://www.servicenow.com/docs/access?context=instance-data-replication&version=australia&pubname=australia-servicenow-platform&ft:locale=en-US) and the [Remote Instance spoke](../../integrationhub-store-spokes/concept/remote-instance-spoke-1.md) support simple multi-instance integrations, Remote Process Sync supports more complex multi-instance integration use cases, focusing on integrating instances by high-level business processes.

**Note:** Remote Process Sync replaces the eBonding spoke for integrating instances.

![Instance Data Replication and the Remote Instance spoke support simple integrations for an entire table or using ServiceNow AI Platform APIs. Remote Process Sync supports more complex multi-instance integrations.](../images/idr-remotespoke-rps-comparison.png "Comparison of Instance Data Replication, Remote Instance spoke, and Remote Process Sync")

If you choose to use Remote Process Sync as your multi-instance integration framework, the next step is to learn about the difference between:

1.  Building your integration, and
2.  Managing your integration

Building your integration involves creating and configuring a process sync definition and its related records. For more information on how to get started with building your Remote Process Sync integration, either step through an example of how to [Build your first Remote Process Sync integration](../tasks/build-first-remote-process-sync-integration.md), or learn about [Process sync definitions](getting-started-with-remote-process-sync.md#process-sync-definitions).

![Building your Remote Process Sync integration.](../images/remote-process-sync-design-time.png "Building your Remote Process Sync integration")

Managing your integration involves monitoring the outbound and inbound queues and checking for errors related to any triggered process sync definitions. For more information on how to monitor and check for errors with your Remote Process Sync integration, see [Outbound queues and inbound queues](getting-started-with-remote-process-sync.md#outbound-and-inbound-queues) and [Monitoring and troubleshooting your integration](getting-started-with-remote-process-sync.md#monitoring-troubleshooting-rps). You may also want to periodically evaluate the outbound and inbound flows that run automatically for your integration and determine whether to make any changes to these flows in [Workflow Studio](https://www.servicenow.com/docs/access?context=workflow-studio&version=australia&pubname=australia-build-workflows&ft:locale=en-US).

**Note:** Both building and managing a Remote Process Sync integration on your instance also requires that you collaborate effectively with users of the remote instance, or remote instances. Be sure to meet with the stakeholders involved in your integration regularly to plan, manage, and continually improve the automated business processes that your multi-instance integration handles.

![Managing your Remote Process Sync integration.](../images/remote-process-sync-overview.png "Managing your Remote Process Sync integration")

## Process sync definitions

A process sync definition contains all of the configurations for your Remote Process Sync integration. Start by creating a new Process Sync Definition record for your integration. Navigate to **IntegrationHub** &gt; **Remote Process Sync** &gt; **Process Sync Definitions**, and then click **New**. In the Process Sync Definition form, fill in the following fields:

|Field|Description|
|-----|-----------|
|Name|Enter a name that accurately describes which part of your business process your instance handles. For example, if users on your instance work to fulfill Service Catalog requests for your customers, enter a name such as Service Catalog Request Fulfillment.|
|Description|Optionally, describe which part of your business process that this process sync definition handles.|
|Application|Automatically set to your current [application scope](https://www.servicenow.com/docs/access?context=c_ApplicationScope&version=australia&pubname=australia-application-development&ft:locale=en-US).|
|Domain|If your process relates to a specific domain, choose a domain other than `global`. For more information, see [Domain separation for service providers](https://www.servicenow.com/docs/access?context=domain-sep-landing-page&version=australia&pubname=australia-platform-security&ft:locale=en-US).|

Click **Submit**, and then you can see your newly created Process Sync Definition record in the list. Next, select the Process Sync Definition record that you just created. You can see that your Process Sync Definition record has the following related lists:

-   Capture Definitions
-   Process Events
-   Remote Systems
-   Outbound Flows
-   Inbound Flows

Refer to the following sections to learn how to set the configurations for each of these related items.

## Capture definitions

A capture definition specifies when your instance should send data to a remote instance and what data your instance should send. A capture definition contains the configurations for your process sync definition's trigger and captured fields. The trigger specifies what record operation, such as creating, updating, or deleting a record, causes your instance to send data to a remote instance. When a Capture Definition is triggered, it creates an object from a source record, which contains captured fields. Then, the outbound flow starts running and correlates the captured fields from the source record to fields in a related record on the remote system.

A Capture Definition record has the following fields:

|Field|Description|
|-----|-----------|
|Process Event|In the Capture Definition form, use the lookup using list icon \(![Lookup using list icon](../images/lookup-using-list-icon.png)\) to choose the Process Event record that you want to associate with this capture definition. If no process event exists yet, enter a name for your process event, and the system automatically creates a Process Event record and associates the record with your capture definition. For more information, see [Process Events](getting-started-with-remote-process-sync.md#process-events).|
|State|Choose **Active** to activate this capture definition so that the parent process sync definition triggers when the conditions you set in this form's Trigger section are met.|
|Order|Enter a value for the order in which you want your capture definition to trigger relative to other capture definitions. Lower order values are honored before higher order values.|
|Application|Automatically set to your current [application scope](https://www.servicenow.com/docs/access?context=c_ApplicationScope&version=australia&pubname=australia-application-development&ft:locale=en-US).|
|Domain|If your process relates to a specific domain, choose a domain other than `global`. For more information, see [Domain separation for service providers](https://www.servicenow.com/docs/access?context=domain-sep-landing-page&version=australia&pubname=australia-platform-security&ft:locale=en-US).|

In the Trigger section, choose an authorized source table whose records you want to trigger your process sync definition. You can also add field conditions that, when met, cause your process sync definition to trigger. When the conditions are met for the trigger specified in your capture definition, any outbound flows associated with your process sync definition start running. For more information, see [Outbound flows and inbound flows](getting-started-with-remote-process-sync.md#outbound-flows-and-inbound-flows).

|Field|Description|
|-----|-----------|
|Source Table Name|Choose an authorized table whose records will trigger your process sync definition every time the records are created, updated, and deleted.|
|Filter|Use the condition builder to add conditions that, when met, will trigger your process sync definition. For example, selecting **\[State\]** &gt; **\[is\]** &gt; **\[Work In Progress\]** causes your process sync definition to trigger every time a record in your selected table's State is updated to Work In Progress.|

Lastly, in the Capture section, add fields to the Selected list that you want to include in the payload for your outbound flow.

<table id="table_c1m_mgq_3nb"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Include fields

</td><td>

Add fields to the Selected list which you want to sync with fields in the remote instance every time your process sync definition triggers. Use the add item icon \(![Add item icon](../images/slushbucket-add-item-icon.png)\) to add fields from the Available list to the Selected list.**Note:**

-   When your integration runs, the outbound payload that is sent to remote instances always contains these captured fields, regardless of whether they were updated or not.
-   You can map these captured fields to fields in the remote instance by configuring mappings in the remote instance's inbound flow that is associated with the same process event. For more information, see [Outbound flows and inbound flows](getting-started-with-remote-process-sync.md#outbound-flows-and-inbound-flows).

</td></tr><tr><td>

Include Attachments

</td><td>

If selected, any attachments that are associated with triggering records on your local instance will sync with attachments in correlated records on the remote instance. For more information, see

</td></tr></tbody>
</table>**Note:** RPS captures both interactive and non-interactive changes. You can configure RPS to ignore non-interactive changes, such as changes made via a scheduled job, by setting the **glide.hub.process.sync.capture.non\_interactive.changes** property to **false**. For more information, see the [How to configure Remote Process Synchronization \(RPS\) framework to ignore non-interactive changes to records \[KB1565025\]](https://support.servicenow.com/kb?id=kb_article_view&sysparm_article=KB1565025) article in the Now Support Knowledge Base.

## Process events

A process event specifies which part of your business process begins in your local instance and ends in the remote instance. The Process Event record in your local instance and in the remote instance should have the same name because the process event signifies the link between these instances that allows them to share parts of the same business process. A Process Event record has the following fields:

<table id="table_g1m_zfk_2nb"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Name

</td><td>

Enter a name that describes the part of your business process that begins in your local instance and ends in the remote instance. For example, if users in your instance request software that will be provisioned in the remote instance, you can name the process event `User requests software`.**Note:** An administrator for the remote instance, or remote instances, must also create a process event with the same name that you use here. Creating these process events in separate instances creates the logical link that allows you to integrate data among multiple instances.

</td></tr><tr><td>

Application

</td><td>

Automatically set to your current [application scope](https://www.servicenow.com/docs/access?context=c_ApplicationScope&version=australia&pubname=australia-application-development&ft:locale=en-US).

</td></tr><tr><td>

Domain

</td><td>

If your process relates to a specific domain, choose a domain other than `global`. For more information, see [Domain separation for service providers](https://www.servicenow.com/docs/access?context=domain-sep-landing-page&version=australia&pubname=australia-platform-security&ft:locale=en-US).

</td></tr></tbody>
</table>## Remote systems

A remote system contains the configurations for the outbound and inbound connections related to another ServiceNow instance. A Remote System record has the following fields:

<table id="table_ofm_nck_2nb"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Name

</td><td>

Enter a name that describes the remote instance. For example, if the instance is managed by one of your customers, Customer A, enter `Customer A's Instance` in the name field.

</td></tr><tr><td>

Description

</td><td>

Optionally, enter more details that describe the remote instance's general purpose in your business process.

</td></tr><tr><td>

External ID

</td><td>

Enter the Sys ID for the Remote System record that shares the same process event with your instance. To get a record's Sys ID, select **Copy sys\_id** from the context menu \(![Context menu icon](../images/context-menu-icon.png)\) in the record's form view. For example, if your Remote Process Sync integration spans two instances, Instance A and Instance B, use the Sys ID from Instance A's Remote System record as the External ID in Instance B and vice-versa. Connecting the Sys IDs and External IDs in this way helps multiple instances know which instance to connect to when the automated outbound and inbound flows run.

</td></tr><tr><td>

Application

</td><td>

Automatically set to your current [application scope](https://www.servicenow.com/docs/access?context=c_ApplicationScope&version=australia&pubname=australia-application-development&ft:locale=en-US).

</td></tr><tr><td>

Domain

</td><td>

If your process relates to a specific domain, choose a domain other than `global`. For more information, see [Domain separation for service providers](https://www.servicenow.com/docs/access?context=domain-sep-landing-page&version=australia&pubname=australia-platform-security&ft:locale=en-US).

</td></tr><tr><td>

Error Subflow

</td><td>

The subflow to run if the Inbound or Outbound State becomes errored.

 Use the lookup using list icon \(![Lookup using list icon](../images/lookup-using-list-icon.png)\) to select a subflow. A subflow appears on this list if:

1.  It is an active, published subflow, and
2.  An input to the subflow is of type Reference to the Process Sync Remote Systems \[ih\_sync\_remote\_system\] table.

 Choose the subflow you want to run when the connection to the remote instance fails. The subflow you select runs whenever your local instance can't connect to the remote instance after your process sync definition triggers.

 There is an error subflow template you can copy and use to make your own Error Subflows. The RPS Error Subflow Template enables you to select notification methods for when the Inbound and Outbound States are errored. You can view the template by navigating to Workflow Studio and searching for it in the Subflows tab.

 You can view remote systems that your instance fails to connect to by navigating to **All** &gt; **IntegrationHub** &gt; **Remote Process Sync** &gt; **Remote Systems - With Errors**.

</td></tr><tr><td>

Connection Alias

</td><td>

Select the lookup using list icon \(![Lookup using list icon](../images/lookup-using-list-icon.png)\) to find and choose a Connection &amp; Credential Alias record that you want to use to authenticate with the remote instance. If you haven't set up a Connection &amp; Credential Alias record for this purpose yet, create a new record with Connection and Credential in the Type field. For more information, see [Create a Connection and Credential alias](https://www.servicenow.com/docs/access?context=connection-alias&version=australia&pubname=australia-platform-security&ft:locale=en-US).

</td></tr><tr><td>

Outbound State

</td><td>

Set to `Disabled` by default. You can change this field's value to `Active` by selecting the **Validate and Activate Remote System** related link in this Remote System record's form view after you finish creating the record.

</td></tr><tr><td>

Inbound API User

</td><td>

User who can connect to the remote instance. This user must have credentials that match those of the user with the ih\_process\_sync\_api role in the remote instance.

</td></tr><tr><td>

Run Inbound Flows as

</td><td>

Select the lookup using list icon \(![Lookup using list icon](../images/lookup-using-list-icon.png)\) to find and choose a user that you want to run the inbound flow for the associated process event. Option to specify the user that runs the flow. You can select the system user or the user who initiates the session. Select the user who initiates the session option when updates should come from the user who triggered the flow. For example, use this option when you want the incident record comments to come from the user who started the flow. Settings for the Run as option in a flow don't apply to child subflows.

</td></tr><tr><td>

Inbound State

</td><td>

Set to `Disabled` by default. You can change this field's value to `Active` by selecting the **Validate and Activate Remote System** related link in this Remote System record's form view after you finish creating the record.

</td></tr></tbody>
</table>**Note:** After creating a Remote System record with the appropriate fields filled in, you must then click the **Validate and Activate Remote System** related link. Clicking this link checks that you can successfully connect to the remote instance and then activates the outbound and inbound connections.

After creating a Process Event record and a Remote System record, you can then associate Workflow Studio subflows with these records so that automated actions run whenever your process sync definition triggers.

## Outbound flows and inbound flows

An outbound flow specifies which Workflow Studio subflow your instance uses to:

1.  Process local data, as fields captured in the capture definition, that will be sent to the remote instance
2.  Correlate this data with data on the remote instance
3.  Send this data to the remote instance

An Outbound Flow record has the following fields:

|Field|Description|
|-----|-----------|
|Process Event|Select the lookup using list icon \(![Lookup using list icon](../images/lookup-using-list-icon.png)\) to find and choose the Process Event record that you want to associate with this outbound flow. The process event that you select should logically relate to the automated actions that the outbound flow will run when your process sync definition triggers. For example, if your outbound flow maps fields from a Service Catalog Item Request record submitted by users in your local instance to related fields in the remote instance, then choose a process event related to users making Service Catalog item requests.|
|Outbound Subflow|Select the lookup using list icon \(![Lookup using list icon](../images/lookup-using-list-icon.png)\) to find and choose the Workflow Studio subflow that you want to run whenever your process sync definition triggers. Your instance provides you with a Remote Process Sync Outbound Flow Template - Basic subflow that you can use as a template in any Outbound Flow record. However, you can customize the Remote Process Sync Outbound Flow Template - Basic subflow so that it meets the needs of your business process. You can customize this subflow using the Remote Process Sync outbound actions. For more information, see [Build your first Remote Process Sync integration](../tasks/build-first-remote-process-sync-integration.md).|
|Remote System|Select the lookup using list icon \(![Lookup using list icon](../images/lookup-using-list-icon.png)\) to find and choose the Remote System record that you want to connect to when your outbound flow runs automated actions that require authenticating with the remote instance. The Remote System record you choose should be the remote instance that handles the inbound part of your Remote Process Sync integration.|
|Application|Automatically set to your current [application scope](https://www.servicenow.com/docs/access?context=c_ApplicationScope&version=australia&pubname=australia-application-development&ft:locale=en-US).|
|Domain|If your process relates to a specific domain, choose a domain other than `global`. For more information, see [Domain separation for service providers](https://www.servicenow.com/docs/access?context=domain-sep-landing-page&version=australia&pubname=australia-platform-security&ft:locale=en-US).|

An inbound flow specifies which Workflow Studio subflow your instance uses to:

1.  Correlate data on the local instance with the data sent from the remote instance
2.  Map fields sent from the remote instance to fields on the local instance
3.  Process data sent from the remote instance to the local instance

An Inbound Flow record has the following fields:

|Field|Description|
|-----|-----------|
|Process Event|Select the lookup using list icon \(![Lookup using list icon](../images/lookup-using-list-icon.png)\) to find and choose the Process Event record that you want to associate with this inbound flow. The process event that you select should logically relate to the automated actions that the inbound flow will run when your local instance is ready to handle the payload sent by the remote instance. For example, if your inbound flow maps fields from a Service Catalog Item Request record that users in the remote instance submitted to related fields in your local instance, then choose a process event related to users making Service Catalog item requests.|
|Inbound Subflow|Select the lookup using list icon \(![Lookup using list icon](../images/lookup-using-list-icon.png)\) to find and choose the Workflow Studio subflow that you want to run whenever your instance handles data sent by a remote instance. Your instance provides you with a Remote Process Sync Inbound Flow Template - Basic subflow that you can use as a template in any Inbound Flow record. However, you can customize the Remote Process Sync Inbound Flow Template - Basic subflow so that it meets the needs of your business process. You can customize this subflow using the Remote Process Sync inbound actions. For more information, see [Build your first Remote Process Sync integration](../tasks/build-first-remote-process-sync-integration.md).|
|Remote System|Select the lookup using list icon \(![Lookup using list icon](../images/lookup-using-list-icon.png)\) to find and choose the Remote System record that you want to connect to when your inbound flow runs automated actions that require authenticating with the remote instance. The Remote System record you choose should be the remote instance that handles the outbound part of your Remote Process Sync integration.|
|Application|Automatically set to your current [application scope](https://www.servicenow.com/docs/access?context=c_ApplicationScope&version=australia&pubname=australia-application-development&ft:locale=en-US).|
|Domain|If your process relates to a specific domain, choose a domain other than `global`. For more information, see [Domain separation for service providers](https://www.servicenow.com/docs/access?context=domain-sep-landing-page&version=australia&pubname=australia-platform-security&ft:locale=en-US).|

**Note:** Each outbound flow and inbound flow must always be associated with one process event and one remote system only.

Before simply choosing the system-provided Remote Process Sync Outbound Flow Template - Basic or Remote Process Sync Inbound Flow Template - Basic subflows for your process sync definition, you may want to customize these subflows in Workflow Studio.

## Syncing attachments

you can choose to send attachments associated with your local record by using the Include Attachments option in your [capture definition](getting-started-with-remote-process-sync.md#capture-definitions). However, Remote Process Sync handles attachments differently from other data in your integration due to security and attachment file size issues:

-   The first time that a record in your integration syncs, all attachments are sent in the outbound payload. Subsequent syncs can send either changes to attachments or all attachments.
-   Attachment metadata is always sent with the outbound payload. This metadata includes an encrypted synthetic key, hash, file name, content type, and size.
-   The remote instance decides which attachments to receive by comparing each hash and file name from the inbound payload to those on the instance. Then, the following process occurs:
    1.  The originating system validates the key and pushes attachments to the correlation record.
    2.  The originating system notifies the remote system that the attachments are complete.
    3.  The remote system moves the attachments from the correlation record to the target record.

## Syncing comments and work notes

In your integration, comments and work notes are synced among instances only when changes occur to those journal fields. Change metadata is included in payloads so that remote systems can identify which user created the comment or work note and when it was created.

## Outbound queues and inbound queues

After building your Remote Process Sync integration by creating and configuring the records mentioned in the previous sections, you can then manage your integration by monitoring the outbound queue and inbound queue in your instance.

An outbound queue contains the status, error information, retry data, and flow context information for outbound subflows that ran for data that was sent out of your instance. To view the records in your outbound queue, navigate to **IntegrationHub** &gt; **Remote Process Sync** &gt; **Outbound Queue State**.

An Outbound Queue State record has the following fields:

<table id="table_vhx_dbq_nnb"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Created

</td><td>

Date that the automated action in your integration occurred

</td></tr><tr><td>

Error info

</td><td>

Status message for the outbound payload

</td></tr><tr><td>

Process Event

</td><td>

[Process event](getting-started-with-remote-process-sync.md#process-events)

</td></tr><tr><td>

Remote System

</td><td>

[Remote System](getting-started-with-remote-process-sync.md#remote-systems)

</td></tr><tr><td>

Retry metadata

</td><td>

Metadata for any retry policies configured for your outbound payload

</td></tr><tr><td>

Status

</td><td>

Processing status of the payload in the outbound queue. Options include:-   Ready
-   Processed
-   Error
-   Skipped

</td></tr><tr><td>

Domain

</td><td>

Domain in which the automated action for your integration ran

</td></tr><tr><td>

Time In Queue

</td><td>

Time spent waiting for the processing of the record.

</td></tr><tr><td>

Processing Time

</td><td>

Time spent processing the record, in milliseconds.

</td></tr><tr><td>

Outbound Subflow Context

</td><td>

Sys ID of the execution record for the outbound flow that processed the payload

</td></tr></tbody>
</table>**Note:** You can get more detailed troubleshooting information for outbound payloads in associated Outbound Queue records. To access these records, navigate to **IntegrationHub** &gt; **Remote Process Sync** &gt; **Outbound Queue**.

An inbound queue contains the status, processing sequence, and correlation information for inbound subflows that ran for data that was sent from a remote instance to your local instance. To view the records in your inbound queue, navigate to **IntegrationHub** &gt; **Remote Process Sync** &gt; **Inbound Queue**.

An Inbound Queue record has the following fields:

<table id="table_fbn_2bl_snb"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Transform Context

</td><td>

Sys ID of the execution record for the inbound flow that processed the payload

</td></tr><tr><td>

Domain

</td><td>

Domain in which the automated action for your integration ran

</td></tr><tr><td>

Local Correlation ID

</td><td>

Correlation ID on the local instance

</td></tr><tr><td>

Operation

</td><td>

Type of record operation that the remote instance performed, which caused the remote instance to trigger and send data. Options include:-   Create
-   Update
-   Delete

</td></tr><tr><td>

Payload

</td><td>

String as JSON payload for inbound data

</td></tr><tr><td>

Process Event

</td><td>

[Process event](getting-started-with-remote-process-sync.md#process-events) associated with the integration action

</td></tr><tr><td>

Remote Correlation ID

</td><td>

Correlation ID on the remote instance

</td></tr><tr><td>

Remote System

</td><td>

[Remote System](getting-started-with-remote-process-sync.md#remote-systems) record associated with the instance that sent the data

</td></tr><tr><td>

Sequence

</td><td>

Order in the queue. A lower number is processed before a higher number.

</td></tr><tr><td>

Time In Queue

</td><td>

Time spent waiting for the processing of the record.

</td></tr><tr><td>

Processing Time

</td><td>

Time spent processing the record, in milliseconds.

</td></tr><tr><td>

Status

</td><td>

Processing status of the payload in the inbound queue. Options include:-   Ready
-   Processed
-   Error
-   Skipped

 **Note:** If an Inbound Queue record has an Error status, change the status to Ready to retry processing the inbound payload.

</td></tr></tbody>
</table>**Note:** Both the Outbound Queue and Inbound Queue tables are maintained by table cleaners that remove records from these tables every 30 days.

## Monitoring and troubleshooting your integration

You can use the following tables to monitor your Remote Process Sync integration, once it is built and running:

|Table|Description|
|-----|-----------|
|XML Stats|View the **process\_sync\_queue** section for information about the outbound and inbound queues for your integration, including the size of the queue as well as error and processing rates.|
|Outbound Queue|View the capture data for records that are staged to be sent out of your instance.|
|Outbound Queue State|View the state of records in the Outbound Queue table.|
|Inbound Queue|View the combined inbound queue and record table.|
|Logs|Start by turning on debugging by setting the **glide.ih.process.sync.debug** system property to `true`. Then, scan the Logs for error messages beginning with `OutboundQueueDao` and `InboundQueueDao` to find log messages with more information about potential issues with your integration.|

If an error occurs with your Remote Process Sync integration, begin by confirming whether the error is a connection error or a data processing error:

-   **Connection errors**

    Outbound connection errors automatically retry several times before setting the Remote System record's Outbound State to Error. If errors keep occurring for an outbound connection, confirm that nothing has changed with the Remote System's Inbound API User, such as a change in the user's credentials. Then, validate and activate the Remote System record again.

-   **Data processing errors**

    Data processing errors typically occur as a result of errors in an outbound flow or inbound flow. To troubleshoot these errors, you can add error handling actions to your flow, such as a Log action or Send Email action, when the flow's State changes to Error. You can also add actions that reprocess or skip processing of records in the Outbound Queue or Inbound Queue tables if an error with the flow occurs.


