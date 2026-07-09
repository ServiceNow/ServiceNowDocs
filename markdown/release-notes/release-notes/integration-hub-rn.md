---
title: Integration Hub release notes
description: The ServiceNow Integration Hub application extends the ServiceNow Workflow Studio automation capabilities by enabling you to integrate your instance data with data in external systems. Integration Hub was enhanced and updated in the Zurich release.
locale: en-US
release: zurich
topic_type: reference
last_updated: "2025-07-31"
reading_time_minutes: 4
---

# Integration Hub release notes

The ServiceNow® Integration Hub application extends the ServiceNow® Workflow Studio automation capabilities by enabling you to integrate your instance data with data in external systems. Integration Hub was enhanced and updated in the Zurich release.

## Integration Hub highlights for the Zurich release

-   Streamline the setup process for REST-based Data Stream actions by automatically generating the parsing and output components.
-   Use load-balancing MID Server clusters in Stream Connect message replication.
-   Enable testing of connection aliases directly from configuration templates.

See [Integration Hub](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/integrate-applications/integrationhub.md) for more information.

## New in the Zurich release

-   **[Generate the parsing phase for REST-based Data Stream actions](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/integrate-applications/data-stream-actions.md)**

    Automatically configure the splitter step, script parser step, and outputs for REST-based Data Stream actions. The **Test REST step** functionality in REST-based Data Stream actions executes a request to the configured REST endpoint, analyzes the response payload, and automatically sets up the parsing and output components.

-   **[Stream Connect enhancements](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/integrate-applications/stream-connect-apache-kafka.md)**
    -   Use a MID Server cluster, instead of a single MID Server for [message replication](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/integrate-applications/stream-connect-message-replication.md). With a MID Server cluster, if one of the MID Servers fails, the other MID Servers can share the load of the failed MID Server.
    -   In the [Kafka subscription record](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/integrate-applications/kafka-subscriptions-statistics.md), view the estimated time required for a consumer to process the current queue. The subscription record also links to the consumer record, so that you can see which consumer is processing the queue.
    -   Specify a compression format for Stream Connect producers with the **com.glide.kafka\_producer.compression\_type** system property. Stream Connect supports the GZIP and LZ4 compression formats.
-   **[View alerts in the Stream Connect dashboard](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/integrate-applications/stream-connect-dashboard.md)**

    Get detailed information about alerts, including their severity level, state, type, and the affected entity in the Stream Connect dashboard.

-   **[Test connection aliases directly from configuration templates](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/integrate-applications/test-alias-configuration-template.md)**

    For aliases using a configuration template, you can configure a Test Action field. This field enables you to test a connection from within the Action Properties section of actions in Workflow Studio.

-   **[Support for PowerShell version 6.0 or later in the PowerShell step](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/integrate-applications/powershell-step-action-designer.md)**

    Enable the PowerShell step to use a newer version of PowerShell by adding the MID Server property **mid.property.ihub.prefer\_powershell6Plus** and setting it to `true`.

-   **[Use WS-Security in a SOAP step on a MID Server](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/integrate-applications/soap-step-action-designer.md)**

    Enable a WS-Security policy in a SOAP step running on a MID Server.

-   **[Delay parallel loading in custom \(load by script\) data sources](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/integrate-applications/custom-type-data-source.md)**

    Configure a delay for parallel loading in custom data sources. When the data source is called, the parallel loading is scheduled to run after the configured amount of time.

-   **Spoke-specific AI agents**

    AI agents that implement different agentic workflows are available for various spokes. Use these spoke-specific AI agents to execute agentic workflows.

-   **[Save draft, publish, update external trigger definition, and support domain separation](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/build-workflows/create-saved-external-trigger.md)**

    The external trigger definition is updated to match the trigger builder so that the external trigger definition supports the saving of draft, publishing, updating external trigger definition, and supporting domain separation.

-   **[Create and manage external event sources](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/build-workflows/manage-external-event-sources.md)**

    Define and manage custom trigger definitions after creating external event sources.


## UI changes

-   **Coral theme**

    Coral is now the default theme for new portal, web, and mobile experiences with Next Experience or Core UI enabled. This theme provides a fresh look and feel, featuring brand-neutral illustrations to enhance your user experience. A dark theme option is available for web and mobile experiences.

-   **Stream Connect menu changes**
    -   The Rescan Topics and Topic Inspector menu items are no longer listed under Stream Connect. You can view them on the [Hermes Messaging Service](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/servicenow-platform/hermes-messaging-service.md) menu.
    -   The Stream Connect Alerts sub menu has been removed. Its menu items, Alerts and Alerting Properties, are now listed directly under Stream Connect.

## Changed in this release

-   **[New debugging property for Stream Connect](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/integrate-applications/kafka-subscriptions-statistics.md)**

    Enable more detailed logging in the Stream Connect logs with the **glide.ih.kafka.stream\_connect.debug** property. This property replaces the **glide.ih.kafka.debug.consume** property.

-   **[Spoke Generator license changes](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/build-workflows/spoke-builder.md)**

    Starting with Zurich, the Spokes list page and Spoke details pages are a part of the ServiceNow Integration Hub Starter Pack. To create a spoke using OpenAPI or Postman collection specification or Now Assist, you need a ServiceNow Integration Hub Professional license in your prod and sub-prod environments.


## Activation information

Integration Hub is included in Workflow Data Fabric and is available with activation of an Workflow Data Fabric subscription package. For details, see [https://www.servicenow.com/now-platform/workflow-data-fabric.html](https://www.servicenow.com/now-platform/workflow-data-fabric.html).

## Related ServiceNow applications and features

-   **[Workflow Studio](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/build-workflows/workflow-studio.md)**

    ServiceNow® Workflow Studio enables process owners to automate approvals, tasks, notifications, and record operations without having to code. You can use the Workflow Studio design environment to author flows and actions and to view the results that they produce.

-   **[App Engine Studio](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/application-development/aes-overview.md)**

    ServiceNow® App Engine Studio \(AES\) is a development tool for creators of varying skill levels to build applications that meet the immediate needs of your organization.

-   **[MID Server](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/servicenow-platform/mid-server-landing.md)**

    The Management, Instrumentation, and Discovery \(MID\) Server is a Java application that runs as a Windows service or UNIX daemon on a server in your local network. The ServiceNow® MID Server enables communication and the movement of data between a ServiceNow instance and external applications, data sources, and services.

-   **[Robotic Process Automation \(RPA\) Hub](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/integrate-applications/rpa-main-landing-page.md)**

    Use the ServiceNow® Robotic Process Automation \(RPA\) Hub to enable end-to-end automation for your organization. With a combination of UI interactions, element-based automations, and APIs that interact between the various business applications, you can emulate user actions and eliminate mundane and repetitive human activities.

-   **[Connections and Credentials](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/platform-security/r-credentials.md)**

    Credentials and connection information are required to gain access to a computer or network device for ServiceNow® Discovery, ServiceNow® Service Mapping, and ServiceNow® Cloud Management, or to perform work using ServiceNow® Orchestration. When adding content to share on the ServiceNow® Developer Site or the ServiceNow® Store, you can configure connections and credentials relevant to your environment without modifying the built content.


**Parent Topic:**[App development and low-code release notes](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/release-notes/build-automate-rn-landing.md)

