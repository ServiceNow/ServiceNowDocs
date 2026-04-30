---
title: Basic system configuration
description: Basic system configuration encompasses changes made to the platform as well as supporting applications. These changes can affect global settings as well as settings for particular applications.
locale: en-US
release: zurich
topic_type: topic
last_updated: "2025-07-31"
reading_time_minutes: 2
breadcrumb: [Get started, Administer]
---

# Basic system configuration

Basic system configuration encompasses changes made to the platform as well as supporting applications. These changes can affect global settings as well as settings for particular applications.

Learn about these ServiceNow AI Platform basic system components and settings:

-   [ServiceNow plugins](../../plugins/concept/c_ServiceNowPlugins.md)
-   [Find components installed with an application](../../plugins/task/find-components.md)
-   [Available system properties](../../reference-pages/reference/r_AvailableSystemProperties.md#)
-   [Query join and complexity size limits](../../managing-data/concept/c_QueryJoinAndComplexitySizeLimits.md)
-   [Web proxy](../../import-sets/concept/c_WebProxy.md)

-   **[Experimentation framework](experimentation_framework.md)**  
The experimentation framework enables ServiceNow to test feature variants on customer instances and collect feedback to improve product experiences.
-   **[ServiceNow plugins](../../plugins/concept/c_ServiceNowPlugins.md)**  
Plugins are software components that provide features and functionalities within a ServiceNow instance.
-   **[Find components installed with an application](../../plugins/task/find-components.md)**  
Activating a plugin installs an application on your instance. Each application consists of components such as tables, user roles, and scheduled jobs. To view all components that are installed with an application, see the Application Files table.
-   **[Available system properties](../../reference-pages/reference/r_AvailableSystemProperties.md#)**  
Some properties are available on a system properties form, but some lesser-used properties are available only from the System Property \[sys\_properties\] table. Sometimes, the property does not exist in a base instance, but can be added if you change the value.
-   **[Query join and complexity size limits](../../managing-data/concept/c_QueryJoinAndComplexitySizeLimits.md)**  
The platform uses a relational database to store data. Retrieving data can involve multiple joins to create a single result set. While these joins are usually simple, in certain cases the system may issue very large joins to bring together large numbers \(&gt;20\) of tables.
-   **[Web proxy](../../import-sets/concept/c_WebProxy.md)**  
Several properties support Web proxy configuration.

**Parent Topic:**[Getting started on the ServiceNow AI Platform](../../general/concept/get-started-now-platform.md)

