---
title: Connect to external systems
description: Connect Hub is a unified workspace for discovering, building, and managing integrations between ServiceNow and external systems. It consolidates discovery, configuration, and management into a single interface.
locale: en-US
release: australia
topic_type: concept
last_updated: "2026-03-12"
reading_time_minutes: 1
breadcrumb: [Workflow Data Fabric Home, Workflow Data Fabric]
---

# Connect to external systems

Connect Hub is a unified workspace for discovering, building, and managing integrations between ServiceNow and external systems. It consolidates discovery, configuration, and management into a single interface.

## Key capabilities of Connect Hub

Connect Hub provides a consolidated interface to accomplish key integration tasks :

-   **Discover external systems and integration opportunities**

    Explore available [external systems](../task/connecthub-create-external-systems.md#) and identify connection methods for over 200 third-party systems like MS Teams, Jira, and Snowflake.

-   **Build and manage connectors**

    Access prebuilt integration components including Spokes, Zero Copy Connectors, and custom connector types. Browse the connector library to select appropriate tools for your integration scenarios or integrate Model Context Protocol clients.

-   **Configure connections and credentials**

    Set up and manage secure authentication details, endpoint URLs, and access controls for your integrations between ServiceNow and external systems.

-   **Access specialized integration tools**

    Use Connect Hub as the entry point for building Spokes and setting up Model Context Protocol clients. ****


## Understanding connectors and connections

Connect Hub distinguishes between two fundamental integration concepts: connectors and connections. Understanding this relationship is essential for effective integration development.

-   **Connectors**

    Prebuilt integration components that define communication with specific external applications. A connector acts as a translator between ServiceNow and the target system, providing actions, triggers, and data-mapping capabilities. For example, a Jira connector contains all the logic needed to interact with Jira's API, including available operations like creating issues or updating workflows. Connectors are reusable tools that you configure once and use across multiple connection instances.

-   **Connections**

    Specific configuration instances that contain the credentials and endpoint details needed to establish communication with a particular external system. A connection holds authentication information such as API keys, OAuth tokens, or user name and password combinations, along with the target system's URL. You create a connection by selecting a connector and providing the specific credentials for your environment. For example, you might use the Jira connector to create separate connections for your development, staging, and production Jira instances.


The relationship between connectors and connections follows a one-to-many pattern. A single connector supports multiple connection instances, enabling you to reuse integration logic across different environments or system instances while maintaining separate credentials and configurations for each. For example, you can have one Jira spoke connector but have three different connections: one each for development, staging, and production respectively.

