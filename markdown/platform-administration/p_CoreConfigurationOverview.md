---
title: Basic system configuration
description: Basic system configuration encompasses changes made to the platform as well as supporting applications. These changes can affect global settings as well as settings for particular applications.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/yokohama/platform-administration/p\_CoreConfigurationOverview.html
release: yokohama
topic_type: topic
last_updated: "2025-01-30"
reading_time_minutes: 2
breadcrumb: [Get started, Administer the ServiceNow AI Platform]
---

# Basic system configuration

Basic system configuration encompasses changes made to the platform as well as supporting applications. These changes can affect global settings as well as settings for particular applications.

Learn about these ServiceNow AI Platform basic system components and settings:

-   [ServiceNow plugins](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/yokohama/markdown/yokohama/platform-administration/c_ServiceNowPlugins.md)
-   [Find components installed with an application](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/yokohama/markdown/yokohama/platform-administration/find-components.md)
-   [Available system properties](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/yokohama/markdown/yokohama/platform-administration/r_AvailableSystemProperties.md)
-   [Query join and complexity size limits](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/yokohama/markdown/yokohama/platform-administration/c_QueryJoinAndComplexitySizeLimits.md)
-   [Web proxy](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/yokohama/markdown/yokohama/platform-administration/c_WebProxy.md)

-   **[ServiceNow plugins](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/yokohama/markdown/yokohama/platform-administration/c_ServiceNowPlugins.md)**  
Plugins are software components that provide features and functionalities within a ServiceNow instance.
-   **[Find components installed with an application](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/yokohama/markdown/yokohama/platform-administration/find-components.md)**  
Activating a plugin installs an application on your instance. Each application consists of components such as tables, user roles, and scheduled jobs. To view all components that are installed with an application, see the Application Files table.
-   **[Available system properties](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/yokohama/markdown/yokohama/platform-administration/r_AvailableSystemProperties.md)**  
Some properties are available on a system properties form, but some lesser-used properties are available only from the System Property \[sys\_properties\] table. Sometimes, the property does not exist in a base instance, but can be added if you change the value.
-   **[Add a system property](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/yokohama/markdown/yokohama/platform-administration/t_AddAPropertyUsingSysPropsList.md)**  
Add or create a property to control system behavior.
-   **[Create a system properties module](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/yokohama/markdown/yokohama/platform-administration/t_CreatingAPropertiesModule.md)**  
You can add a module in the application navigator to access the list of system properties. This module makes it easy to add properties to the System Properties table.
-   **[Query join and complexity size limits](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/yokohama/markdown/yokohama/platform-administration/c_QueryJoinAndComplexitySizeLimits.md)**  
The platform uses a relational database to store data. Retrieving data can involve multiple joins to create a single result set. While these joins are usually simple, in certain cases the system may issue very large joins to bring together large numbers \(&gt;20\) of tables.
-   **[Web proxy](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/yokohama/markdown/yokohama/platform-administration/c_WebProxy.md)**  
Several properties support Web proxy configuration.

**Parent Topic:**[Getting started on the ServiceNow AI Platform](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/yokohama/markdown/yokohama/platform-administration/get-started-now-platform.md)

