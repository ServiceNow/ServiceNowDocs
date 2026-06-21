---
title: Combined Integration Hub release notes for upgrades from Xanadu to Australia
description: Consolidated page of all release notes for Integration Hub from Xanadu to Australia.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/delta-xanadu-australia/australia-xanadu-integrationhub-release-notes.html
release: australia
topic_type: reference
last_updated: "2026-06-21"
reading_time_minutes: 15
breadcrumb: [Products combined by family]
---

# Combined Integration Hub release notes for upgrades from Xanadu to Australia

Consolidated page of all release notes for Integration Hub from Xanadu to Australia.

## How to use this page

To help you prepare for your upgrade, we have combined the cross-family Integration Hub release notes onto one page. Read this summary of the new features, changes, and updated information for your product from Xanadu to Australia.

**Tip:** If there were no updates for a release notes section in a certain family release, we included a short note for your reference. For example, if a product did not have any updates in Tokyo, the row says "No updates for this release."

## Important information for upgrading Integration Hub to Australia

Before you upgrade to Australia, review these pre- and post-upgrade tasks and complete the tasks as needed.

<table class="custom-rows"><thead><tr><th class="filter">

Release

</th><th>

Release notes

</th></tr></thead><tbody><tr><td>

Xanadu

</td><td>

No updates for this release.

</td></tr><tr><td>

Yokohama

</td><td>

No updates for this release.

</td></tr><tr><td>

Zurich

</td><td>

No updates for this release.

</td></tr><tr><td>

Australia

</td><td>

No updates for this release.

</td></tr></tbody>
</table>## New features

Between your current release family and Australia, new features were introduced for Integration Hub.

<table class="custom-rows"><thead><tr><th class="filter">

Release

</th><th>

Release notes

</th></tr></thead><tbody><tr><td>

Xanadu

</td><td>

-   **Now Assist in Conversational Spokes**

Use Now Assist in Conversational Spokes to utilize the conversational ability of Integration Hub Spoke actions. Now Assist in Conversational Spokes offers generative AI capabilities to make spoke actions conversational. With this, you can perform business actions and automate business workflows through conversational interface.

Install Now Assist for Conversational Spokes plugin and start utilizing the conversational ability of the Look up User spoke action in Microsoft Active Directory v2 spoke. You can call this action from a conversational interface like Now Assist.


-   **[Send and receive messages in an Avro format with Stream Connect](https://www.servicenow.com/docs/access?context=schema-management&family=xanadu&ft:locale=en-US)**

Import and create Avro schemas to store in the Stream Connect Schemas \[stream\_connect\_schema\] table. Stream Connect producers and consumers use the schemas to convert plain-text JSON messages into an Avro binary format and back. Using an Avro format can reduce the size of the payload and simplify your integration to your local Apache Kafka instance.

-   **[Track incoming requests for SOAP and REST APIs, and URL Export](https://www.servicenow.com/docs/access?context=integrationhub-usage-dashboard&family=xanadu&ft:locale=en-US)**

View the data egress details in the enhanced Usage dashboard. Using the dashboard, you can track the data egress usage per source over time. This information is presented in a line chart and, if needed, you can view the amount of data transfer by source on any given date within the specified date range. The dashboard retrieves data from the Data Egress Count table \[data\_egress\_count\].

-   **[Enable parallel loading in custom \(load by script\) type data sources](https://www.servicenow.com/docs/access?context=custom-type-data-source&family=xanadu&ft:locale=en-US)**

Use a script to partition data into smaller sections, then load the sections in parallel. Parallel loading can enable your integrations to finish faster and reduce the impact on other tasks.

-   **[CyberArk credential storage integration](https://www.servicenow.com/docs/access?context=c_CyberArkCredStorageIntegrate&family=xanadu&ft:locale=en-US) Use the CyberArk Digital Vault to store and access your OAuth 2.0 credentials**

Use the ServiceNow® MID Server to access your OAuth 2.0 credentials stored on the CyberArk Digital Vault. The MID Server uses this information to generate OAuth 2.0 tokens for client credentials grant type that are then used to make REST API calls to the third-party server.

-   **[Make outbound REST and SOAP calls through a MID Server using mTLS](https://www.servicenow.com/docs/access?context=mtls-mid-server&family=xanadu&ft:locale=en-US)**

Store mTLS password and certificate information on the instance, in a vault, or in a configuration file. The MID Server uses this information to make outbound REST and SOAP calls with the mTLS protocol.

-   **[Use the Personal Authentication dashboard](https://www.servicenow.com/docs/access?context=personal-auth-dashboard&family=xanadu&ft:locale=en-US)**

Use your personal credentials to connect to third-party integrations. View, authenticate, revoke, and renew your personal authentications through a simplified, consolidated interface.

-   **[Enhancements to the external trigger endpoints](https://www.servicenow.com/docs/access?context=generate-endpt-oauth2&family=xanadu&ft:locale=en-US)**

Generate an endpoint for webhooks in the third-party applications that support [OAuth 2.0 authentication](https://www.servicenow.com/docs/access?context=generate-endpt-oauth2&family=xanadu&ft:locale=en-US). The endpoint enables webhooks to connect with your ServiceNow instance.

Generate the endpoints by updating the base system external event sources on your ServiceNow instance. After that, you can configure the endpoint on the third-party application and enable it to send a webhook to the ServiceNow instance to execute a flow. Based on the authentication type that the third-party system supports, you can generate a hash, secret, or token, or add roles or a user to the external event source. Finally, you generate the endpoint that you can use on the third-party system webhook.

-   **[Automatically generate a JSON payload for the JSON Builder step](https://www.servicenow.com/docs/access?context=json-build-step-action-designer&family=xanadu&ft:locale=en-US)**

Enter a JSON payload into the step's script editor to automatically de-serialize the payload into structured input.

-   **[Enhanced OpenAPI step](https://www.servicenow.com/docs/access?context=open-api-step-action-designer&family=xanadu&ft:locale=en-US)**

Choose to import an OpenAPI specification or a Postman Collection of a third-party outbound REST web service for building an integration. The OpenAPI step is now enhanced to support Postman API collections and is renamed as **OpenAPI/Postman step**.


</td></tr><tr><td>

Yokohama

</td><td>

-   **[Stream Connect for Apache Kafka alerting](https://www.servicenow.com/docs/access?context=stream-connect-alert&family=yokohama&ft:locale=en-US)**
    -   Get alerts for your Stream Connect integrations. Stream Connect uses both active and scheduled monitoring to detect events across multiple Stream Connect components. If an issue is detected, an alert is created, and a message is logged to the Stream Connect Log.
    -   Specify alert thresholds by configuring alerting properties. For example, you can specify a maximum amount of time to process the current message queue. If the estimated processing time exceeds your specified time, an alert is generated.
    -   Receive alert notifications via email, SMS, or the ServiceNow® mobile app. Notifications contain detailed alert information, including the alert number, level, and a description. You can configure notification settings based on alert types, severity, and user preferences.
-   **[View producer statistics in the Stream Connect dashboard](https://www.servicenow.com/docs/access?context=stream-connect-dashboard&family=yokohama&ft:locale=en-US)**

Get detailed information about Stream Connect producers and their performance, including a producer’s status and type, the number of bytes and messages produced to a topic, and producer data trends over time, in the Stream Connect dashboard.

-   **[Check data usage in the Stream Connect dashboard](https://www.servicenow.com/docs/access?context=stream-connect-dashboard&family=yokohama&ft:locale=en-US)**

View total data usage and data usage per month and topic with the Stream Connect dashboard. Data usage history is available for the last 12 complete months plus the current month.

-   **[Use error evaluation with Data Stream actions](https://www.servicenow.com/docs/access?context=data-stream-actions&family=yokohama&ft:locale=en-US)**

Catch step errors and specify error behavior for each step in a Data Stream action. Create your own error conditions by specifying when an action returns an error state and the status codes and messages they return.

-   **[View connection aliases in integration actions](https://www.servicenow.com/docs/access?context=managing-connections-integration-hub&family=yokohama&ft:locale=en-US)**

Edit, configure, and create connection aliases in the Action Properties section of actions in ServiceNow® Workflow Studio. View connection error details for connection aliases that are not set up or configured.


</td></tr><tr><td>

Zurich

</td><td>

-   **[Generate the parsing phase for REST-based Data Stream actions](https://www.servicenow.com/docs/access?context=data-stream-actions&family=zurich&ft:locale=en-US)**

Automatically configure the splitter step, script parser step, and outputs for REST-based Data Stream actions. The **Test REST step** functionality in REST-based Data Stream actions executes a request to the configured REST endpoint, analyzes the response payload, and automatically sets up the parsing and output components.

-   **[Stream Connect enhancements](https://www.servicenow.com/docs/access?context=stream-connect-apache-kafka&family=zurich&ft:locale=en-US)**
    -   Use a MID Server cluster, instead of a single MID Server for [message replication](https://www.servicenow.com/docs/access?context=stream-connect-message-replication&family=zurich&ft:locale=en-US). With a MID Server cluster, if one of the MID Servers fails, the other MID Servers can share the load of the failed MID Server.
    -   In the [Kafka subscription record](https://www.servicenow.com/docs/access?context=kafka-subscriptions-statistics&family=zurich&ft:locale=en-US), view the estimated time required for a consumer to process the current queue. The subscription record also links to the consumer record, so that you can see which consumer is processing the queue.
    -   Specify a compression format for Stream Connect producers with the **com.glide.kafka\_producer.compression\_type** system property. Stream Connect supports the GZIP and LZ4 compression formats.
-   **[View alerts in the Stream Connect dashboard](https://www.servicenow.com/docs/access?context=stream-connect-dashboard&family=zurich&ft:locale=en-US)**

Get detailed information about alerts, including their severity level, state, type, and the affected entity in the Stream Connect dashboard.

-   **[Test connection aliases directly from configuration templates](https://www.servicenow.com/docs/access?context=test-alias-configuration-template&family=zurich&ft:locale=en-US)**

For aliases using a configuration template, you can configure a Test Action field. This field enables you to test a connection from within the Action Properties section of actions in Workflow Studio.

-   **[Support for PowerShell version 6.0 or later in the PowerShell step](https://www.servicenow.com/docs/access?context=powershell-step-action-designer&family=zurich&ft:locale=en-US)**

Enable the PowerShell step to use a newer version of PowerShell by adding the MID Server property **mid.property.ihub.prefer\_powershell6Plus** and setting it to `true`.

-   **[Use WS-Security in a SOAP step on a MID Server](https://www.servicenow.com/docs/access?context=soap-step-action-designer&family=zurich&ft:locale=en-US)**

Enable a WS-Security policy in a SOAP step running on a MID Server.

-   **[Delay parallel loading in custom \(load by script\) data sources](https://www.servicenow.com/docs/access?context=custom-type-data-source&family=zurich&ft:locale=en-US)**

Configure a delay for parallel loading in custom data sources. When the data source is called, the parallel loading is scheduled to run after the configured amount of time.

-   **Spoke-specific AI agents**

AI agents that implement different agentic workflows are available for various spokes. Use these spoke-specific AI agents to execute agentic workflows.

-   **[Save draft, publish, update external trigger definition, and support domain separation](https://www.servicenow.com/docs/access?context=create-saved-external-trigger&family=zurich&ft:locale=en-US)**

The external trigger definition is updated to match the trigger builder so that the external trigger definition supports the saving of draft, publishing, updating external trigger definition, and supporting domain separation.

-   **[Create and manage external event sources](https://www.servicenow.com/docs/access?context=manage-external-event-sources&family=zurich&ft:locale=en-US)**

Define and manage custom trigger definitions after creating external event sources.


</td></tr><tr><td>

Australia

</td><td>

-   **[Use Direct Kafka to integrate your on-premise ServiceNow instance with your local Kafka environment](https://www.servicenow.com/docs/access?context=direct-kafka&family=australia&ft:locale=en-US)**

Configure a custom Kafka connection to enable your on-premise instance to connect directly to your local Kafka environment.

-   **[Create topic aliases for Stream Connect topics](https://www.servicenow.com/docs/access?context=manage-topic-alias&family=australia&ft:locale=en-US)**

Use topic aliases to simplify topic management in Stream Connect. A topic alias is a unique topic name that can be connected to any underlying Hermes or Direct Kafka topic. A topic alias can be moved to different instances and, wherever they’re moved, connected to an underlying topic.

-   **[Stream Connect Dashboard updates](https://www.servicenow.com/docs/access?context=stream-connect-dashboard&family=australia&ft:locale=en-US)**
    -   The Topics menu displays topic aliases, Hermes topics, and Direct Kafka topics.
    -   The **Data usage** tab shows data for the Hermes cluster or the Direct Kafka cluster. Use the **Kafka Cluster** list to select which cluster data to display.
    -   The Consumers and Producers menus reference topic aliases instead of Hermes topics.
-   **[View the Remote Process Sync Dashboard](https://www.servicenow.com/docs/access?context=remote-process-sync-dashboard&family=australia&ft:locale=en-US)**

View detailed statistics and monitor the health of your Remote Process Sync \(RPS\) integrations. The Remote Process Sync Dashboard provides real-time visibility into key metrics, including records processed, queue sizes, processing times, and system status. Use this dashboard to identify issues, track performance trends, and promote smooth operation of your RPS integrations.

-   **[Produce messages to Hermes via a MID Server](https://www.servicenow.com/docs/access?context=MID-hermes-API&family=australia&ft:locale=en-US)**

Send message payloads to Hermes with MID script includes.

-   **[View usage metrics for Direct Kafka](https://www.servicenow.com/docs/access?context=direct-kafka-usage-metrics&family=australia&ft:locale=en-US)**

Track data usage between your instance and Direct Kafka systems. The Direct Kafka Usage metrics table provides administrators with visibility into data transfer volumes for bytes produced and consumed. View metrics aggregated by hour, day, or month at the cluster and topic level. Usage records are automatically retained for 13 months.

-   **[Use the read-only role for Stream Connect](https://www.servicenow.com/docs/access?context=stream-connect-apache-kafka-roles&family=australia&ft:locale=en-US)**

Use the new read-only role for Stream Connect to grant users view-only access to Stream Connect resources. Users with this role can view Stream Connect configurations and runtime statistics across all related modules, but can’t create, modify, or delete any Stream Connect settings.

-   **[View logs for Stream Connect producers](https://www.servicenow.com/docs/access?context=producer-statistics&family=australia&ft:locale=en-US)**

Get detailed log information for producers in the Stream Connect logs. Use the **glide.ih.kafka.producer.message\_bytes\_to\_log** property to specify how much of the message to display in the logs.

-   **[Configure alert thresholds for undelivered messages in Stream Connect](https://www.servicenow.com/docs/access?context=sc-alert-properties&family=australia&ft:locale=en-US)**

Set alert thresholds for undelivered messages based on how long a topic has gone without receiving new messages. Use this configuration to trigger INFO, WARNING, or CRITICAL alerts when message delivery stops for a specified period.

-   **[Configure alert thresholds for unprocessed messages in Stream Connect](https://www.servicenow.com/docs/access?context=sc-alert-properties&family=australia&ft:locale=en-US)**

Set alert thresholds for messages that remain unprocessed in a topic. You can trigger alerts based on how long messages sit in a topic without being consumed, helping to identify lagging or failing consumers.

-   **[Get metadata information for Stream Connect consumers](https://www.servicenow.com/docs/access?context=configure-script-consumer&family=australia&ft:locale=en-US)**

View the partition, offset, datacenter ID, and timestamp epoch for the script consumer and Kafka Message trigger.

-   **[View message timestamps in the Stream Connect script consumer](https://www.servicenow.com/docs/access?context=configure-script-consumer&family=australia&ft:locale=en-US)**

Get the message timestamp in the script consumer as a UTC time-zone string. You can use the UTC time-zone string to convert the timestamp to a **GlideDateTime** object.

-   **[Use an error subflow template to create your own error subflows in Remote Process Sync](https://www.servicenow.com/docs/access?context=getting-started-with-remote-process-sync&family=australia&ft:locale=en-US)**

Copy and modify the RPS Error Subflow Template to create error subflows. The template enables you to select notification methods for when the Inbound and Outbound States are errored.

-   **Specify attachment details in Remote Process Sync actions**

Specify the max attachment size and allowed attachment extensions in the [Identify New Attachments action](https://www.servicenow.com/docs/access?context=identify-new-attachments-action&family=australia&ft:locale=en-US) and the [Get Attachment Metadata for Local Record action](https://www.servicenow.com/docs/access?context=get-attachment-metadata-local-record-action&family=australia&ft:locale=en-US).

-   **Use a new retry policy for Remote Process Sync actions**

Retry failed requests at specified intervals with the RPS Push Attachment Policy. This policy works with the [Identify New Attachments action](https://www.servicenow.com/docs/access?context=identify-new-attachments-action&family=australia&ft:locale=en-US) and the [Get Attachment Metadata for Local Record action](https://www.servicenow.com/docs/access?context=get-attachment-metadata-local-record-action&family=australia&ft:locale=en-US).

-   **[SASL authentication support for Apache Kafka connections](https://www.servicenow.com/docs/access?context=hla-data-input-kafka-credentials&family=australia&ft:locale=en-US)**

Configure SASL authentication for your Apache Kafka connections with support for SASL\_SSL and SASL\_PLAINTEXT security protocols. Kafka credentials now support multiple SASL mechanisms: PLAIN- SCRAM-SHA-256, SCRAM-SHA-512.


</td></tr></tbody>
</table>## Changes

Between your current release family and Australia, some changes were made to existing Integration Hub features.

<table class="custom-rows"><thead><tr><th class="filter">

Release

</th><th>

Release notes

</th></tr></thead><tbody><tr><td>

Xanadu

</td><td>

-   **[External Triggers framework to use new features provided by Platform Security](https://www.servicenow.com/docs/access?context=set-up-external-webhook-endpoints&family=xanadu&ft:locale=en-US)**

Upgrade the existing external triggers framework to use new features like Hash-based and Token-based authentication profiles with access policies.


</td></tr><tr><td>

Yokohama

</td><td>

No updates for this release.

</td></tr><tr><td>

Zurich

</td><td>

-   **[New debugging property for Stream Connect](https://www.servicenow.com/docs/access?context=kafka-subscriptions-statistics&family=zurich&ft:locale=en-US)**

Enable more detailed logging in the Stream Connect logs with the **glide.ih.kafka.stream\_connect.debug** property. This property replaces the **glide.ih.kafka.debug.consume** property.

-   **[Spoke Generator license changes](https://www.servicenow.com/docs/access?context=spoke-builder&family=zurich&ft:locale=en-US)**

Starting with Zurich, the Spokes list page and Spoke details pages are a part of the ServiceNow Integration Hub Starter Pack. To create a spoke using OpenAPI or Postman collection specification or Now Assist, you need a ServiceNow Integration Hub Professional license in your prod and sub-prod environments.


</td></tr><tr><td>

Australia

</td><td>

No updates for this release.

</td></tr></tbody>
</table>## Removed

Between your current release family and Australia, some Integration Hub features or functionality were removed.

<table class="custom-rows"><thead><tr><th class="filter">

Release

</th><th>

Release notes

</th></tr></thead><tbody><tr><td>

Xanadu

</td><td>

-   The Legacy Usage Overview dashboard is deprecated. This feature is no longer deployed, enhanced, or supported. For details, see the [Deprecation Process \[KB0867184\]](https://hi.service-now.com/kb_view.do?sysparm_article=KB0867184) article in the Now Support Knowledge Base.

</td></tr><tr><td>

Yokohama

</td><td>

**Important:**

-   Starting with the Yokohama release, Microsoft Teams Spoke is being prepared for future deprecation. It will be hidden and no longer activated on new instances but will continue to be supported. Microsoft Teams Graph Spoke provides the latest experience for this functionality.

For more information, search for the term `Microsoft Teams Spoke for ServiceNow IntegrationHub` in [Plugins planned for deprecation](https://www.servicenow.com/docs/access?context=plugins-planned-for-deprecation&family=yokohama&ft:locale=en-US).

-   Starting with the Yokohama release, Gremlin Spoke is being prepared for future deprecation. It will be hidden and no longer activated on new instances but will continue to be supported. Spoke Generator provides the latest experience for this functionality.

For details, see the [Deprecation Process \[KB0867184\]](https://support.servicenow.com/kb?id=kb_article_view&sysparm_article=KB0867184) article in the Now Support knowledge base.


</td></tr><tr><td>

Zurich

</td><td>

No updates for this release.

</td></tr><tr><td>

Australia

</td><td>

No updates for this release.

</td></tr></tbody>
</table>## Deprecations

Between your current release family and Australia, some Integration Hub features or functionality were deprecated.

<table class="custom-rows"><thead><tr><th class="filter">

Release

</th><th>

Release notes

</th></tr></thead><tbody><tr><td>

Xanadu

</td><td>

No updates for this release.

</td></tr><tr><td>

Yokohama

</td><td>

No updates for this release.

</td></tr><tr><td>

Zurich

</td><td>

No updates for this release.

</td></tr><tr><td>

Australia

</td><td>

No updates for this release.

</td></tr></tbody>
</table>## Activation information

Review information on how to activate Integration Hub.

<table class="custom-rows"><thead><tr><th class="filter">

Release

</th><th>

Release notes

</th></tr></thead><tbody><tr><td>

Xanadu

</td><td>

Integration Hub is included in Workflow Data Fabric and is available with activation of an Workflow Data Fabric subscription package. For details, see [https://www.servicenow.com/products/automation-engine.html](https://www.servicenow.com/products/automation-engine.html).

</td></tr><tr><td>

Yokohama

</td><td>

Integration Hub is included in Workflow Data Fabric and is available with activation of an Workflow Data Fabric subscription package. For details, see [https://www.servicenow.com/now-platform/workflow-data-fabric.html](https://www.servicenow.com/now-platform/workflow-data-fabric.html).

</td></tr><tr><td>

Zurich

</td><td>

Integration Hub is included in Workflow Data Fabric and is available with activation of an Workflow Data Fabric subscription package. For details, see [https://www.servicenow.com/now-platform/workflow-data-fabric.html](https://www.servicenow.com/now-platform/workflow-data-fabric.html).

</td></tr><tr><td>

Australia

</td><td>

Integration Hub is included in Workflow Data Fabric and is available with activation of an Workflow Data Fabric subscription package. For details, see [https://www.servicenow.com/now-platform/workflow-data-fabric.html](https://www.servicenow.com/now-platform/workflow-data-fabric.html).

</td></tr></tbody>
</table>## Additional requirements

If any additional requirements were introduced or changed for Integration Hub we have noted them here.

<table class="custom-rows"><thead><tr><th class="filter">

Release

</th><th>

Release notes

</th></tr></thead><tbody><tr><td>

Xanadu

</td><td>

No updates for this release.

</td></tr><tr><td>

Yokohama

</td><td>

No updates for this release.

</td></tr><tr><td>

Zurich

</td><td>

No updates for this release.

</td></tr><tr><td>

Australia

</td><td>

No updates for this release.

</td></tr></tbody>
</table>## Browser requirements

If any specific browser requirements were introduced or changed for Integration Hub we have noted them here.

<table class="custom-rows"><thead><tr><th class="filter">

Release

</th><th>

Release notes

</th></tr></thead><tbody><tr><td>

Xanadu

</td><td>

No updates for this release.

</td></tr><tr><td>

Yokohama

</td><td>

No updates for this release.

</td></tr><tr><td>

Zurich

</td><td>

No updates for this release.

</td></tr><tr><td>

Australia

</td><td>

No updates for this release.

</td></tr></tbody>
</table>## Accessibility information

Review details on accessibility information for Integration Hub, such as specific requirements or compliance levels.

<table class="custom-rows"><thead><tr><th class="filter">

Release

</th><th>

Release notes

</th></tr></thead><tbody><tr><td>

Xanadu

</td><td>

No updates for this release.

</td></tr><tr><td>

Yokohama

</td><td>

No updates for this release.

</td></tr><tr><td>

Zurich

</td><td>

No updates for this release.

</td></tr><tr><td>

Australia

</td><td>

No updates for this release.

</td></tr></tbody>
</table>## Localization information

If there are specific localization considerations for Integration Hub we have noted them here.

<table class="custom-rows"><thead><tr><th class="filter">

Release

</th><th>

Release notes

</th></tr></thead><tbody><tr><td>

Xanadu

</td><td>

No updates for this release.

</td></tr><tr><td>

Yokohama

</td><td>

No updates for this release.

</td></tr><tr><td>

Zurich

</td><td>

No updates for this release.

</td></tr><tr><td>

Australia

</td><td>

No updates for this release.

</td></tr></tbody>
</table>## Highlight information

If there are specific highlight considerations for Integration Hub we have noted them here.

<table class="custom-rows"><thead><tr><th class="filter">

Release

</th><th>

Release notes

</th></tr></thead><tbody><tr><td>

Xanadu

</td><td>

-   Send and receive messages in an Apache Avro format with ServiceNow® Stream Connect.
-   Use the CyberArk Digital Vault to store and access your OAuth 2.0 credentials.
-   Use your personal credentials to connect to third-party integrations.

 See [Integration Hub](https://www.servicenow.com/docs/access?context=integrationhub&family=xanadu&ft:locale=en-US) for more information.

</td></tr><tr><td>

Yokohama

</td><td>

-   Get alerts and alert notifications for your Stream Connect integrations.
-   Use error evaluation with Data Stream actions to catch step errors and specify error behavior for each step.
-   Edit, configure, and create connection aliases in the Action Properties section of actions in Workflow Studio.

 See [Integration Hub](https://www.servicenow.com/docs/access?context=integrationhub&family=yokohama&ft:locale=en-US) for more information.

</td></tr><tr><td>

Zurich

</td><td>

-   Streamline the setup process for REST-based Data Stream actions by automatically generating the parsing and output components.
-   Use load-balancing MID Server clusters in Stream Connect message replication.
-   Enable testing of connection aliases directly from configuration templates.

 See [Integration Hub](https://www.servicenow.com/docs/access?context=integrationhub&family=zurich&ft:locale=en-US) for more information.

</td></tr><tr><td>

Australia

</td><td>

-   Integrate your on-premise ServiceNow instance with your local Kafka environment with Direct Kafka.
-   Simplify topic management in Stream Connect with topic aliases. A topic alias is a unique topic name that can be connected to any underlying Hermes or Direct Kafka topic.
-   View detailed statistics and monitor the health of your Integration Hub Remote Process Sync \(RPS\) integrations with the Remote Process Sync Dashboard.

 See [Integration Hub](https://www.servicenow.com/docs/access?context=integrationhub&family=australia&ft:locale=en-US) for more information.

</td></tr></tbody>
</table>**Parent Topic:**[Products combined by family](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/delta-xanadu-australia/rn-combined-intro.md)

