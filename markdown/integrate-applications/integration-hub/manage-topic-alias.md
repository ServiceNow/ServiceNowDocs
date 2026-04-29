---
title: Topic aliases
description: Use topic aliases to simplify topic management in Stream Connect. A topic alias is a unique topic name that can be connected to any underlying Hermes or Direct Kafka topic. A topic alias can be moved to different instances and connected to a different underlying topic on each instance.Create a topic alias and connect it to an underlying Hermes or Direct Kafka topic.
locale: en-US
release: australia
product: Integration Hub
classification: integration-hub
topic_type: concept
last_updated: "2026-03-12"
reading_time_minutes: 4
breadcrumb: [Using Stream Connect for Apache Kafka, Import and stream data, Integration Hub, Workflow Data Fabric]
---

# Topic aliases

Use topic aliases to simplify topic management in Stream Connect. A topic alias is a unique topic name that can be connected to any underlying Hermes or Direct Kafka topic. A topic alias can be moved to different instances and connected to a different underlying topic on each instance.

## Topic alias example

This example shows the form for a topic alias that is connected to a Direct Kafka topic.

![Screen shot of a topic alias record.](../images/topic-alias.png)

The full name of the topic alias is Incoming-Messages \[Global\]. A topic alias has a qualified name: It's a combination of the name that it's given \(in this case, Incoming-Messages\) followed by its application scope. It’s possible for there to be multiple topic aliases with the same given name if the aliases are in different application scopes.

In the Related Links section, there are links to connect or disconnect topics. If a topic alias is already connected to a topic, there will be a link to disconnect it. In this example, the topic alias is already connected to a topic, so the link is **Disconnect Direct Kafka Topic**. If the topic alias wasn't already connected to a topic, the link would say **Connect Direct Kafka Topic**.

The links you see here are also determined by which plugins are installed.

-   If the ServiceNow Stream Connect Installer \(Direct Kafka\) \(com.glide.hub.stream\_connect.onprem\_installer\) plugin is installed, links to connect or disconnect Direct Kafka topics appear.
-   If the ServiceNow Stream Connect Hermes \(com.glide.hub.stream\_connect.hermes\) plugin is installed, links to connect or disconnect Hermes topics appear.
-   If both plugins are installed, links for both Hermes topics and Direct Kafka topics appear.

For a list of Stream Connect plugins, see [Integration Hub plugins](../reference/ih-plugins.md).

Below the Related Links are tabs for Topics, Kafka Subscriptions, and Kafka Producers.

-   The Hermes Topics tab displays any connected Hermes topics. This tab only appears on hosted instances that have access to the ServiceNow hosted Hermes service.
-   The Direct Kafka Topics tab displays any connected Direct Kafka topics. This tab generally appears only for on-premise instances where the ServiceNow Stream Connect Direct Kafka \(com.glide.hub.stream\_connect.direct\_kafka\) plugin is installed.
-   The Kafka Subscriptions tab displays any associated subscriptions and related statistics. For more on subscription statistics, see [Viewing Kafka subscriptions and statistics](kafka-subscriptions-statistics.md).
-   The Kafka Producers tab displays any associated producers and their related statistics. For descriptions of producer statistics, see [Viewing producer statistics](producer-statistics.md).

## Topic and topic alias tables

You can see topic aliases in the Topic Aliases \[sys\_sc\_topic\_alias\] table. Certain ServiceNow product offerings may create internal topic aliases that can't be deleted or modified.

Direct Kafka topics are on the Direct Kafka Topics \[sys\_kafka\_direct\_topic\] table. Hermes topics are on the Kafka Topics \[sys\_kafka\_topic\] table.

## Create and connect a topic alias

Create a topic alias and connect it to an underlying Hermes or Direct Kafka topic.

### Before you begin

Role required: stream\_connect\_admin

### Procedure

1.  Navigate to **All** &gt; **IntegrationHub** &gt; **Stream Connect** &gt; **Topic Alias** and select **New**.

2.  Enter a name and select **Submit**.

3.  From the Topic Aliases list, select the topic alias you just created.

4.  Under Related Links, select either **Connect Direct Kafka Topic** or **Connect Hermes Topic**.

    The links in the Related Links section are determined by which plugins are installed. If the ServiceNow Stream Connect Installer \(Direct Kafka\) \(com.glide.hub.stream\_connect.onprem\_installer\) plugin is installed, the **Connect Direct Kafka Topic** link appears. If the ServiceNow Stream Connect Hermes \(com.glide.hub.stream\_connect.hermes\) plugin is installed, the **Connect Hermes Topic** link appears. If both plugins are installed, both links appear.

    After selecting the link, a dialog box saying either Connect Direct Kafka Topic or Connect Hermes Topic appears.

5.  Use the magnifying glass icon to open the list of topics and select the one you want to connect to the topic alias, then select **OK**.

    **Note:** Only topics that aren't already connected to a topic alias show up in the list of topics.


### Result

After the topic alias is connected to a topic, the topic name appears in the appropriate tab: A Hermes topic appears in the Hermes Topics tab, and a Direct Kafka topic appears in the Direct Kafka Topics tab.

Under Related Links, the associated link changes from connect to disconnect. For example, a **Connect Hermes Topic** changes to a **Disconnect Hermes Topic**. You can use the disconnect link to disconnect the topic alias from the underlying topic.

**Note:** Disconnecting a topic alias may affect any active consumers or producers.

