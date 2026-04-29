---
title: Third-party data integration for CSM
description: The third-party data integration feature enables you to retrieve data from third-party applications and display the data in Agent Workspace for CSM without having to store it in your ServiceNow instance.
locale: en-US
release: australia
topic_type: concept
last_updated: "2026-03-12"
reading_time_minutes: 3
breadcrumb: [CSM Configurable Workspace features, CSM Configurable Workspace, Organize agent workspaces, Configure, Customer Service Management]
---

# Third-party data integration for CSM

The third-party data integration feature enables you to retrieve data from third-party applications and display the data in Agent Workspace for CSM without having to store it in your ServiceNow instance.

Many enterprise customers use ServiceNow applications as part of their IT ecosystems. In these environments, ServiceNow applications coexist with other applications and exchange data through different types of integrations. For customer service agents who typically use a wide variety of applications, this can create a fragmented experience that impacts agent productivity and increases customer wait time.

A frequent integration takes place between ServiceNow and Salesforce applications. In this integration, customers use Salesforce to manage pre-sales activities and ServiceNow to manage post-sales activities. These post-sales activities represent service assurance.

To provide high quality service, agents using the Customer Service Management \(CSM\) application need a complete understanding of the customer's context, and this includes access to customer data maintained in other systems. A common example of this integration is enriching a CSM customer profile by providing a list of opportunities related to the customer's account. These opportunities are retrieved from Salesforce in real time and are presented in Agent Workspace for CSM.

Using the third-party data integration feature, data from third-party applications can be retrieved as needed. Agents can view the data in lists and forms. This feature uses remote tables to store the third-party data in memory on the application server. Remote tables are useful for data that changes frequently because the data is retrieved in real-time when a user accesses the data from the ServiceNow AI Platform.

## Activating third-party data integration

The following plugins are required to implement third-party data integration:

-   Remote Tables \(com.glide.script.vtable\): Adds the Remote Table Script Definition table \(sys\_script\_vtable\) and adds the **Remote Table** flag to the Tables \(sys\_db\_object\) table. Active on the base instance.
-   OAuth 2.0 \(com.snc.platform.security.oauth\): Adds the OAuth-related tables and extension points needed to support **OAuth 2.0 –JWT Bearer grant type**. Active on the base instance.
-   IntegrationHub \(com.glide.hub.integrations\): Provides the ability to build reusable integrations with third-party systems and call them from anywhere in the platform. IntegrationHub requires subscription and is available in several subscription packages. Different packages allow for different levels of automation and provide different subsets of predefined third-party integrations, or spokes. For more information, see [Request IntegrationHub](https://www.servicenow.com/docs/access?context=request-ih-overview&version=australia&pubname=australia-integrate-applications&ft:locale=en-US) and [IntegrationHub available spokes](https://www.servicenow.com/docs/access?context=spokes-list&version=australia&pubname=australia-integrate-applications&ft:locale=en-US).
-   Customer Service \(com.sn\_customerservice\)

## Configuring third-party data integration

Users with the system administrator role can configure the necessary components to enable third-party data integration for Agent Workspace for CSM. At a high level, the configuration steps include:

-   Setting up the **OAuth 2.0 – JWT Bearer grant type**, which provides the connection between the ServiceNow instance and the third-party application.
-   Setting up aliases to manage connection information and credentials when integrating with external systems and providing alias reference to the IntegrationHub action.
-   Creating a remote table to store the third-party data.
-   Creating a remote table script definition that maps the data from the third-party application table to the remote table.
-   Configuring ACLs for the remote table to provide user access to the third-party data.
-   Configuring the lists and forms that display data from the remote table.

For more information, see [Configure third-party data integration for CSM](../task/config-csm-third-party-integration.md).

## Using third-party data integration

Within Agent Workspace for CSM, agents can use this feature to:

-   View read-only data from third-party applications in lists and forms.
-   View data from multiple third-party applications in one browser tab.
-   View data from third-party applications in pop-up windows, sub tabs, and related items using iframes.
-   Open links to third-party application records from forms.

## Domain separation

Remote table script definitions are domain separated. If users do not have access to the same domain as the remote table script definition record, they cannot access records from the remote table specified in the script definition.

The data within the remote table is not domain separated.

For more information, see [Domain separation and remote tables](https://www.servicenow.com/docs/access?context=domain-separation-remote-tables&version=australia&pubname=australia-servicenow-platform&ft:locale=en-US).

## Related documentation

-   Authentication and credentials
    -   [Set up OAuth provider with JWT Bearer grant type](https://www.servicenow.com/docs/access?context=JWT-Bearer-token-support&version=australia&pubname=australia-platform-security&ft:locale=en-US)
    -   [Credentials and connection information](https://www.servicenow.com/docs/access?context=r-credentials&version=australia&pubname=australia-platform-security&ft:locale=en-US)
-   [IntegrationHub](https://www.servicenow.com/docs/access?context=integrationhub&version=australia&pubname=australia-integrate-applications&ft:locale=en-US)
-   [Flow Designer](https://www.servicenow.com/docs/access?context=flow-designer&version=australia&pubname=australia-application-development&ft:locale=en-US)
-   [Retrieving external data using remote tables and scripts](https://www.servicenow.com/docs/access?context=remote-tables&version=australia&pubname=australia-servicenow-platform&ft:locale=en-US)
-   [Salesforce spoke](https://www.servicenow.com/docs/access?context=salesforce-spoke&version=australia&pubname=australia-integrate-applications&ft:locale=en-US)

