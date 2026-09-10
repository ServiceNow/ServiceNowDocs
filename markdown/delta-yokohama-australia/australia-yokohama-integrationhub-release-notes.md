---
title: Combined Integration Hub release notes for upgrades from Yokohama to Australia
description: Consolidated page of all release notes for Integration Hub from Yokohama to Australia.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/delta-yokohama-australia/australia-yokohama-integrationhub-release-notes.html
release: australia
topic_type: reference
last_updated: "2026-09-10"
reading_time_minutes: 6
breadcrumb: [Products combined by family]
---

# Combined Integration Hub release notes for upgrades from Yokohama to Australia

Consolidated page of all release notes for Integration Hub from Yokohama to Australia.

## How to use this page

To help you prepare for your upgrade, we have combined the cross-family Integration Hub release notes onto one page. Read this summary of the new features, changes, and updated information for your product from Yokohama to Australia.

**Tip:** If there were no updates for a release notes section in a certain family release, we included a short note for your reference. For example, if a product did not have any updates in Tokyo, the row says "No updates for this release."

## Important information for upgrading Integration Hub to Australia

Before you upgrade to Australia, review these pre- and post-upgrade tasks and complete the tasks as needed.

<table class="custom-rows"><thead><tr><th class="filter">

Release

</th><th>

Release notes

</th></tr></thead><tbody><tr><td>

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

Yokohama

</td><td>

-   **[View producer statistics in the Stream Connect dashboard](https://www.servicenow.com/docs/access?context=stream-connect-dashboard&family=yokohama&ft:locale=en-US)**

Get detailed information about Stream Connect producers and their performance, including a producer’s status and type, the number of bytes and messages produced to a topic, and producer data trends over time, in the Stream Connect dashboard.


</td></tr><tr><td>

Zurich

</td><td>

-   **[View alerts in the Stream Connect dashboard](https://www.servicenow.com/docs/access?context=stream-connect-dashboard&family=zurich&ft:locale=en-US)**

Get detailed information about alerts, including their severity level, state, type, and the affected entity in the Stream Connect dashboard.


</td></tr><tr><td>

Australia

</td><td>

-   **[Stream Producer](https://www.servicenow.com/docs/access?context=stream-producer&family=australia&ft:locale=en-US)**

Automatically stream changes from ServiceNow tables to Kafka topics with Stream Producer. Stream Producer uses change data capture \(CDC\) technology to capture inserts, updates, and deletes on selected tables. The captured changes are formatted as messages and sent to a Kafka topic, enabling real-time data synchronization with external applications.

-   **[Stream Producer schemas](https://www.servicenow.com/docs/access?context=schema-management&family=australia&ft:locale=en-US)**

Stream Producer supports the Avro serialization format for message payloads. When using an Avro format, Stream Producer uses the selected table's auto-generated schema to convert CDC payloads to Avro before sending them to Kafka.


</td></tr></tbody>
</table>## Changes

Between your current release family and Australia, some changes were made to existing Integration Hub features.

<table class="custom-rows"><thead><tr><th class="filter">

Release

</th><th>

Release notes

</th></tr></thead><tbody><tr><td>

Yokohama

</td><td>

-   **[Create an HTTP\(s\) connection](https://www.servicenow.com/docs/access?context=create-https-connection&family=yokohama&ft:locale=en-US) Options to specify the MID Server capabilities and MID application in a connection record**

The Configure Connection form, that you use to configure a connection between your ServiceNow instance, and a third-party application now provides the following fields when you select **Auto-Select MID Server** from the MID Selection list.

    -   Capabilities: The capabilities that the MID Server must support to be eligible for selection.
    -   MID Application: The application that the MID Server must support to be eligible for selection.

</td></tr><tr><td>

Zurich

</td><td>

-   **Coral theme**

Coral is now the default theme for new portal, web, and mobile experiences with Next Experience or Core UI enabled. This theme provides a fresh look and feel, featuring brand-neutral illustrations to enhance your user experience. A dark theme option is available for web and mobile experiences.

-   **Stream Connect menu changes**
    -   The Rescan Topics and Topic Inspector menu items are no longer listed under Stream Connect. You can view them on the [Hermes Messaging Service](https://www.servicenow.com/docs/access?context=hermes-messaging-service&family=zurich&ft:locale=en-US) menu.
    -   The Stream Connect Alerts sub menu has been removed. Its menu items, Alerts and Alerting Properties, are now listed directly under Stream Connect.

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
</table>## Deprecations

Between your current release family and Australia, some Integration Hub features or functionality were deprecated.

<table class="custom-rows"><thead><tr><th class="filter">

Release

</th><th>

Release notes

</th></tr></thead><tbody><tr><td>

Yokohama

</td><td>

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
</table>## Activation information

Review information on how to activate Integration Hub.

<table class="custom-rows"><thead><tr><th class="filter">

Release

</th><th>

Release notes

</th></tr></thead><tbody><tr><td>

Yokohama

</td><td>

-   **Activation information**

Integration Hub is included in Workflow Data Fabric and is available with activation of an Workflow Data Fabric subscription package. For details, see [https://www.servicenow.com/now-platform/workflow-data-fabric.html](https://www.servicenow.com/now-platform/workflow-data-fabric.html).


</td></tr><tr><td>

Zurich

</td><td>

-   **Activation information**

Integration Hub is included in Workflow Data Fabric and is available with activation of an Workflow Data Fabric subscription package. For details, see [https://www.servicenow.com/now-platform/workflow-data-fabric.html](https://www.servicenow.com/now-platform/workflow-data-fabric.html).


</td></tr><tr><td>

Australia

</td><td>

-   **Activation information**

Integration Hub is included in Workflow Data Fabric and is available with activation of an Workflow Data Fabric subscription package. For details, see [https://www.servicenow.com/now-platform/workflow-data-fabric.html](https://www.servicenow.com/now-platform/workflow-data-fabric.html).


</td></tr></tbody>
</table>## Additional requirements

If any additional requirements were introduced or changed for Integration Hub we have noted them here.

<table class="custom-rows"><thead><tr><th class="filter">

Release

</th><th>

Release notes

</th></tr></thead><tbody><tr><td>

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
</table>**Parent Topic:**[Products combined by family](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/delta-yokohama-australia/rn-combined-intro.md)

