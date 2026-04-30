---
title: Integration Hub release notes
description: The ServiceNow Integration Hub application extends the ServiceNow Workflow Studio automation capabilities by enabling you to integrate your instance data with data in external systems. Integration Hub was enhanced and updated in the Xanadu release.
locale: en-US
release: xanadu
topic_type: reference
last_updated: "2024-08-01"
reading_time_minutes: 5
---

# Integration Hub release notes

The ServiceNow® Integration Hub application extends the ServiceNow® Workflow Studio automation capabilities by enabling you to integrate your instance data with data in external systems. Integration Hub was enhanced and updated in the Xanadu release.

## Integration Hub highlights for the Xanadu release

-   Send and receive messages in an Apache Avro format with ServiceNow® Stream Connect.
-   Use the CyberArk Digital Vault to store and access your OAuth 2.0 credentials.
-   Use your personal credentials to connect to third-party integrations.

See [Integration Hub](https://www.servicenow.com/docs/access?context=integrationhub&version=xanadu&pubname=xanadu-integrate-applications&ft:locale=en-US) for more information.

## New in the Xanadu release

-   **Now Assist in Conversational Spokes**

    Use Now Assist in Conversational Spokes to utilize the conversational ability of Integration Hub Spoke actions. Now Assist in Conversational Spokes offers generative AI capabilities to make spoke actions conversational. With this, you can perform business actions and automate business workflows through conversational interface.

    Install Now Assist for Conversational Spokes plugin and start utilizing the conversational ability of the Look up User spoke action in Microsoft Active Directory v2 spoke. You can call this action from a conversational interface like Now Assist.


-   **[Send and receive messages in an Avro format with Stream Connect](https://www.servicenow.com/docs/access?context=schema-management&version=xanadu&pubname=xanadu-integrate-applications&ft:locale=en-US)**

    Import and create Avro schemas to store in the Stream Connect Schemas \[stream\_connect\_schema\] table. Stream Connect producers and consumers use the schemas to convert plain-text JSON messages into an Avro binary format and back. Using an Avro format can reduce the size of the payload and simplify your integration to your local Apache Kafka instance.

-   **[Track incoming requests for SOAP and REST APIs, and URL Export](https://www.servicenow.com/docs/access?context=integrationhub-usage-dashboard&version=xanadu&pubname=xanadu-integrate-applications&ft:locale=en-US)**

    View the data egress details in the enhanced Usage dashboard. Using the dashboard, you can track the data egress usage per source over time. This information is presented in a line chart and, if needed, you can view the amount of data transfer by source on any given date within the specified date range. The dashboard retrieves data from the Data Egress Count table \[data\_egress\_count\].

-   **[Enable parallel loading in custom \(load by script\) type data sources](https://www.servicenow.com/docs/access?context=custom-type-data-source&version=xanadu&pubname=xanadu-integrate-applications&ft:locale=en-US)**

    Use a script to partition data into smaller sections, then load the sections in parallel. Parallel loading can enable your integrations to finish faster and reduce the impact on other tasks.

-   **[CyberArk credential storage integration](https://www.servicenow.com/docs/access?context=c_CyberArkCredStorageIntegrate&version=xanadu&pubname=xanadu-platform-security&ft:locale=en-US) Use the CyberArk Digital Vault to store and access your OAuth 2.0 credentials**

    Use the ServiceNow® MID Server to access your OAuth 2.0 credentials stored on the CyberArk Digital Vault. The MID Server uses this information to generate OAuth 2.0 tokens for client credentials grant type that are then used to make REST API calls to the third-party server.

-   **[Make outbound REST and SOAP calls through a MID Server using mTLS](https://www.servicenow.com/docs/access?context=mtls-mid-server&version=xanadu&pubname=xanadu-integrate-applications&ft:locale=en-US)**

    Store mTLS password and certificate information on the instance, in a vault, or in a configuration file. The MID Server uses this information to make outbound REST and SOAP calls with the mTLS protocol.

-   **[Use the Personal Authentication dashboard](https://www.servicenow.com/docs/access?context=personal-auth-dashboard&version=xanadu&pubname=xanadu-integrate-applications&ft:locale=en-US)**

    Use your personal credentials to connect to third-party integrations. View, authenticate, revoke, and renew your personal authentications through a simplified, consolidated interface.

-   **[Enhancements to the external trigger endpoints](https://www.servicenow.com/docs/access?context=generate-endpt-oauth2&version=xanadu&pubname=xanadu-integrate-applications&ft:locale=en-US)**

    Generate an endpoint for webhooks in the third-party applications that support [OAuth 2.0 authentication](https://www.servicenow.com/docs/access?context=generate-endpt-oauth2&version=xanadu&pubname=xanadu-integrate-applications&ft:locale=en-US). The endpoint enables webhooks to connect with your ServiceNow instance.

    Generate the endpoints by updating the base system external event sources on your ServiceNow instance. After that, you can configure the endpoint on the third-party application and enable it to send a webhook to the ServiceNow instance to execute a flow. Based on the authentication type that the third-party system supports, you can generate a hash, secret, or token, or add roles or a user to the external event source. Finally, you generate the endpoint that you can use on the third-party system webhook.

-   **[Automatically generate a JSON payload for the JSON Builder step](https://www.servicenow.com/docs/access?context=json-build-step-action-designer&version=xanadu&pubname=xanadu-integrate-applications&ft:locale=en-US)**

    Enter a JSON payload into the step's script editor to automatically de-serialize the payload into structured input.

-   **[Enhanced OpenAPI step](https://www.servicenow.com/docs/access?context=open-api-step-action-designer&version=xanadu&pubname=xanadu-integrate-applications&ft:locale=en-US)**

    Choose to import an OpenAPI specification or a Postman Collection of a third-party outbound REST web service for building an integration. The OpenAPI step is now enhanced to support Postman API collections and is renamed as **OpenAPI/Postman step**.


## UI changes

-   **Legacy dashboards migrated**

    The Legacy Usage Overview dashboard, Orchestration Usage dashboard, ROI dashboard, ROI dashboard, and ROI Premium dashboard are migrated to the Platform Analytics workspace.


## Changed in this release

-   **[External Triggers framework to use new features provided by Platform Security](https://www.servicenow.com/docs/access?context=set-up-external-webhook-endpoints&version=xanadu&pubname=xanadu-integrate-applications&ft:locale=en-US)**

    Upgrade the existing external triggers framework to use new features like Hash-based and Token-based authentication profiles with access policies.


## Removed in this release

-   The Legacy Usage Overview dashboard is deprecated. This feature is no longer deployed, enhanced, or supported. For details, see the [Deprecation Process \[KB0867184\]](https://hi.service-now.com/kb_view.do?sysparm_article=KB0867184) article in the Now Support Knowledge Base.

## Activation information

Integration Hub is included in Workflow Data Fabric and is available with activation of an Workflow Data Fabric subscription package. For details, see [https://www.servicenow.com/products/automation-engine.html](https://www.servicenow.com/products/automation-engine.html).

## Related ServiceNow applications and features

-   **[Workflow Studio](https://www.servicenow.com/docs/access?context=workflow-studio&version=xanadu&pubname=xanadu-build-workflows&ft:locale=en-US)**

    ServiceNow® Workflow Studio enables process owners to automate approvals, tasks, notifications, and record operations without having to code. You can use the Workflow Studio design environment to author flows and actions and to view the results that they produce.

-   **[App Engine Studio](https://www.servicenow.com/docs/access?context=aes-overview&version=xanadu&pubname=xanadu-application-development&ft:locale=en-US)**

    ServiceNow® App Engine Studio \(AES\) is a development tool for creators of varying skill levels to build applications that meet the immediate needs of your organization.

-   **[MID Server](https://www.servicenow.com/docs/access?context=mid-server-landing&version=xanadu&pubname=xanadu-servicenow-platform&ft:locale=en-US)**

    The Management, Instrumentation, and Discovery \(MID\) Server is a Java application that runs as a Windows service or UNIX daemon on a server in your local network. The ServiceNow® MID Server enables communication and the movement of data between a ServiceNow instance and external applications, data sources, and services.

-   **[Robotic Process Automation \(RPA\) Hub](https://www.servicenow.com/docs/access?context=rpa-main-landing-page&version=xanadu&pubname=xanadu-integrate-applications&ft:locale=en-US)**

    Use the ServiceNow® Robotic Process Automation \(RPA\) Hub to enable end-to-end automation for your organization. With a combination of UI interactions, element-based automations, and APIs that interact between the various business applications, you can emulate user actions and eliminate mundane and repetitive human activities.

-   **[Connections and Credentials](https://www.servicenow.com/docs/access?context=r-credentials&version=xanadu&pubname=xanadu-platform-security&ft:locale=en-US)**

    Credentials and connection information are required to gain access to a computer or network device for ServiceNow® Discovery, ServiceNow® Service Mapping, and ServiceNow® Cloud Management, or to perform work using ServiceNow® Orchestration. When adding content to share on the ServiceNow® Developer Site or the ServiceNow® Store, you can configure connections and credentials relevant to your environment without modifying the built content.


**Parent Topic:**[Hyperautomation and Low-code release notes](build-automate-rn-landing.md)

