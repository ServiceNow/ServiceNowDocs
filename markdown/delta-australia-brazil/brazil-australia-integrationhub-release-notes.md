---
title: Combined Integration Hub release notes for upgrades from Australia to Brazil
description: Consolidated page of all release notes for Integration Hub from Australia to Brazil.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/delta-australia-brazil/brazil-australia-integrationhub-release-notes.html
release: brazil
topic_type: reference
last_updated: "2026-09-24"
reading_time_minutes: 6
breadcrumb: [Products combined by family]
---

# Combined Integration Hub release notes for upgrades from Australia to Brazil

Consolidated page of all release notes for Integration Hub from Australia to Brazil.

## How to use this page

To help you prepare for your upgrade, we have combined the cross-family Integration Hub release notes onto one page. Read this summary of the new features, changes, and updated information for your product from Australia to Brazil.

**Tip:** If there were no updates for a release notes section in a certain family release, we included a short note for your reference. For example, if a product did not have any updates in Tokyo, the row says "No updates for this release."

## Important information for upgrading Integration Hub to Brazil

Before you upgrade to Brazil, review these pre- and post-upgrade tasks and complete the tasks as needed.

<table class="custom-rows"><thead><tr><th class="filter">

Release

</th><th>

Release notes

</th></tr></thead><tbody><tr><td>

Australia

</td><td>

No updates for this release.

</td></tr><tr><td>

Brazil

</td><td>

No updates for this release.

</td></tr></tbody>
</table>## New features

Between your current release family and Brazil, new features were introduced for Integration Hub.

<table class="custom-rows"><thead><tr><th class="filter">

Release

</th><th>

Release notes

</th></tr></thead><tbody><tr><td>

Australia

</td><td>

-   **[OAUTHBEARER authentication for Stream Connect message replication](https://www.servicenow.com/docs/access?context=hla-data-input-kafka-credentials&family=australia&ft:locale=en-US)**

Authenticate using OAUTHBEARER as part of the SASL credential framework for Stream Connect message replication. OAUTHBEARER authentication lets Stream Connect administrators meet customer requirements, improve security, and align with existing OAuth capabilities on the platform, enabling seamless integration with Kafka environments that require advanced authentication.


 -   **[Stream Connect Dashboard updates](https://www.servicenow.com/docs/access?context=stream-connect-dashboard&family=australia&ft:locale=en-US)**
    -   The Topics menu displays topic aliases, Hermes topics, and Direct Kafka topics.
    -   The **Data usage** tab shows data for the Hermes cluster or the Direct Kafka cluster. Use the **Kafka Cluster** list to select which cluster data to display.
    -   The Consumers and Producers menus reference topic aliases instead of Hermes topics.

 -   **[Use Direct Kafka to integrate your on-premise ServiceNow instance with your local Kafka environment](https://www.servicenow.com/docs/access?context=direct-kafka&family=australia&ft:locale=en-US)**

Configure a custom Kafka connection to enable your on-premise instance to connect directly to your local Kafka environment.

-   **[Create topic aliases for Stream Connect topics](https://www.servicenow.com/docs/access?context=manage-topic-alias&family=australia&ft:locale=en-US)**

Use topic aliases to simplify topic management in Stream Connect. A topic alias is a unique topic name that can be connected to any underlying Hermes or Direct Kafka topic. A topic alias can be moved to different instances and, wherever they’re moved, connected to an underlying topic.

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


</td></tr><tr><td>

Brazil

</td><td>

No updates for this release.

</td></tr></tbody>
</table>## Changes

Between your current release family and Brazil, some changes were made to existing Integration Hub features.

<table class="custom-rows"><thead><tr><th class="filter">

Release

</th><th>

Release notes

</th></tr></thead><tbody><tr><td>

Australia

</td><td>

No updates for this release.

</td></tr><tr><td>

Brazil

</td><td>

No updates for this release.

</td></tr></tbody>
</table>## Removed

Between your current release family and Brazil, some Integration Hub features or functionality were removed.

<table class="custom-rows"><thead><tr><th class="filter">

Release

</th><th>

Release notes

</th></tr></thead><tbody><tr><td>

Australia

</td><td>

No updates for this release.

</td></tr><tr><td>

Brazil

</td><td>

No updates for this release.

</td></tr></tbody>
</table>## Deprecations

Between your current release family and Brazil, some Integration Hub features or functionality were deprecated.

<table class="custom-rows"><thead><tr><th class="filter">

Release

</th><th>

Release notes

</th></tr></thead><tbody><tr><td>

Australia

</td><td>

No updates for this release.

</td></tr><tr><td>

Brazil

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

Australia

</td><td>

-   **Activation information**

Integration Hub is included in Workflow Data Fabric and is available with activation of an Workflow Data Fabric subscription package. For details, see [https://www.servicenow.com/now-platform/workflow-data-fabric.html](https://www.servicenow.com/now-platform/workflow-data-fabric.html).


</td></tr><tr><td>

Brazil

</td><td>

No updates for this release.

</td></tr></tbody>
</table>## Additional requirements

If any additional requirements were introduced or changed for Integration Hub we have noted them here.

<table class="custom-rows"><thead><tr><th class="filter">

Release

</th><th>

Release notes

</th></tr></thead><tbody><tr><td>

Australia

</td><td>

No updates for this release.

</td></tr><tr><td>

Brazil

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

Australia

</td><td>

No updates for this release.

</td></tr><tr><td>

Brazil

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

Australia

</td><td>

No updates for this release.

</td></tr><tr><td>

Brazil

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

Australia

</td><td>

No updates for this release.

</td></tr><tr><td>

Brazil

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

Australia

</td><td>

-   Integrate your on-premise ServiceNow instance with your local Kafka environment with Direct Kafka.
-   Simplify topic management in Stream Connect with topic aliases. A topic alias is a unique topic name that can be connected to any underlying Hermes or Direct Kafka topic.
-   View detailed statistics and monitor the health of your Integration Hub Remote Process Sync \(RPS\) integrations with the Remote Process Sync Dashboard.

 See [Integration Hub](https://www.servicenow.com/docs/access?context=integrationhub&family=australia&ft:locale=en-US) for more information.

</td></tr><tr><td>

Brazil

</td><td>

No updates for this release.

</td></tr></tbody>
</table>**Parent Topic:**[Products combined by family](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/delta-australia-brazil/rn-combined-intro.md)

