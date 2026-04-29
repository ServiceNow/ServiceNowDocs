---
title: Config Converse
description: With Config Converse, you can use natural language to create simple or complex configurations.
locale: en-US
release: australia
product: Sales and Order Management
classification: sales-and-order-management
topic_type: concept
last_updated: "2026-03-23"
reading_time_minutes: 2
breadcrumb: [CPQ, Configure, price, quote, Explore, Sales and Order Management]
---

# Config Converse

With Config Converse, you can use natural language to create simple or complex configurations.

The new Config Converse feature can make creating new configurations easier and faster by using natural language to leverage artificial intelligence.

## Enable Config Converse

To enable Config Converse, follow these steps:

1.  Submit a support request to enable AI features for CPQ.

    You’ll receive a message confirming that the features have been enabled. When the features are enabled, continue to step 2.

2.  In CPQ Admin, click **Utilities**.
3.  On the Utilities page, open the settings.
4.  Click to set **Enable Smart Predict**.
5.  Click to set **Enable Config Converse**.

When Config Converse has been enabled, follow these steps to enable the feature on a layout that’s part of a blueprint:

1.  In CPQ Admin, click to open a blueprint.
2.  Click to open a layout for editing, and then access the layout properties by clicking the gear icon.
3.  In the Layout Properties window, scroll down to the Config Converse section and click to set **Enable Config Converse**.
4.  If you want to create a default landing page for Config Converse in this layout, click **Use Landing Layout**.

    When the landing page is enabled, users see a window where they can enter a configuration request using natural language. Depending on the landing page settings, they may also be presented with other options, such as the ability to choose from a menu of configuration scenarios. Users can choose to skip using Config Converse and go to the regular configuration page by clicking **Skip**.


## Use Config Converse

To use Config Converse, type a configuration request into the prompt box, and then click **Generate configuration**. Use natural language. For example, you might enter a request like the following:

`I need to config a workload type of AI/ML using unstructured data types. Data will be accessed moderately frequently, with a data size of 20 TB, a growth rate of 20%, and 99.99% uptime. Data should be retained for two years. Setup will be handled in house.`

Config Converse searches for relevant fields based on the information in the prompt and updates the fields to generate a configuration that meets the requirements you provide. Depending on the configuration, a bill of materials \(BOM\) is also created.

As the configuration is generated, a **Configuration AI** pane appears that shows the details of the new configuration. When the initial configuration is complete, the user is prompted to specify any changes to be made. These changes can also be specified using natural language. Users can also modify the configuration without using Config Converse.

