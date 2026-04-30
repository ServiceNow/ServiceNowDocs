---
title: Integration with third-party applications and data sources
description: ServiceNow integrates with many third party applications and data sources.
locale: en-US
release: xanadu
topic_type: concept
last_updated: "2024-08-01"
reading_time_minutes: 2
breadcrumb: [Integrations, Configure core features, Administer the ServiceNow AI Platform]
---

# Integration with third-party applications and data sources

ServiceNow integrates with many third party applications and data sources.

The most common integrations are with CMDB, Incident Management, Problem Management, Change Management, User Administration, and Single Sign-on. A variety of techniques can be used, most notably Web Services, JDBC, LDAP, Excel, CSV, and Email, as well as any industry standard technologies that use SOAP, REST, or WSDL. Additionally, API and command-line integrations can be done using a MID Server. ServiceNow has performed the following integrations with enterprise systems and platforms.

## Technologies

The ServiceNow platform is based on service-oriented architecture \(SOA\), in which all data objects can use web services to access bi-directional data-level integration. The interface is also direct and dynamic because all modifications to existing objects and all new objects are automatically published as a Direct Web Service. A more indirect web service creation and usage can be achieved through Mapped Web Service where a transform map is used to gather incoming web service data into the final targeted tables. Finally, an advanced Scripted Web Service technique is available for defining process-based web services, where data is irrelevant, but serves more as a trigger for a process or a composite of actions that execute at the server.

Additionally the platform offers a rich interface for loading external data using import sets. Using this feature, you can load from various data sources such as HTTPS, FTPS, and SCP using file formats such as XML, CSV, and Microsoft Excel XLS files. Information can also be pulled from a data source using a direct JDBC connection, provided the network connectivity allows.

Information can be pulled from the platform to an external platform using an [ODBC driver](https://www.servicenow.com/docs/access?context=c_ODBCDriver&version=xanadu&pubname=xanadu-api-reference&ft:locale=en-US).

Forms, lists, and reports on the platform can be accessed directly using a URL, which facilitates integration on the UI level between two or more web applications.

A handful of single sign-on technologies is identified and implemented out of the box to allow fast integration with your portal, however, the technique is customizable in a script to allow for flexibility in the different SSO environments our customers have.

## Integration between ServiceNow Instances

There are times when you find you need to perform a specific integration between your instance and another ServiceNow instance. Instance-to-Instance integrations are a snap because all of the integration points exist between the two instances.

-   **[Integration options](c_IntegrationOptions.md)**  
Nearly all ServiceNow customers obtain additional value by integrating with third-party applications.
-   **[Managing integration sessions](managing-integration-sessions.md#)**  
Manage access to an instance by configuring how long integration sessions last before expiring.
-   **[Domain separation in third-party application and data source integration](domain-separation-app-data-source-integration.md)**  
This is an overview of domain separation and integration of third-party applications and data sources. Domain separation enables you to separate data, processes, and administrative tasks into logical groupings called domains. You can control several aspects of this separation, including which users can see and access data.

**Parent Topic:**[ServiceNow AI Platform integrations](../../administer/managing-data/concept/integrations.md)

