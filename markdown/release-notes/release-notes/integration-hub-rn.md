---
title: Integration Hub release notes
description: The ServiceNow Integration Hub application extends the ServiceNow Workflow Studio automation capabilities by enabling you to integrate your instance data with data in external systems. Integration Hub was enhanced and updated in the Yokohama release.
locale: en-US
release: yokohama
topic_type: reference
last_updated: "2025-01-30"
reading_time_minutes: 4
---

# Integration Hub release notes

The ServiceNow® Integration Hub application extends the ServiceNow® Workflow Studio automation capabilities by enabling you to integrate your instance data with data in external systems. Integration Hub was enhanced and updated in the Yokohama release.

## Integration Hub highlights for the Yokohama release

-   Get alerts and alert notifications for your Stream Connect integrations.
-   Use error evaluation with Data Stream actions to catch step errors and specify error behavior for each step.
-   Edit, configure, and create connection aliases in the Action Properties section of actions in Workflow Studio.

See [Integration Hub](https://www.servicenow.com/docs/access?context=integrationhub&version=yokohama&pubname=yokohama-integrate-applications&ft:locale=en-US) for more information.

## New in the Yokohama release

-   **[Stream Connect alerting](https://www.servicenow.com/docs/access?context=stream-connect-alert&version=yokohama&pubname=yokohama-integrate-applications&ft:locale=en-US)**
    -   Get alerts for your Stream Connect integrations. Stream Connect uses both active and scheduled monitoring to detect events across multiple Stream Connect components. If an issue is detected, an alert is created, and a message is logged to the Stream Connect Log.
    -   Specify alert thresholds by configuring alerting properties. For example, you can specify a maximum amount of time to process the current message queue. If the estimated processing time exceeds your specified time, an alert is generated.
    -   Receive alert notifications via email, SMS, or the ServiceNow® mobile app. Notifications contain detailed alert information, including the alert number, level, and a description. You can configure notification settings based on alert types, severity, and user preferences.
-   **[View producer statistics in the Stream Connect dashboard](https://www.servicenow.com/docs/access?context=stream-connect-dashboard&version=yokohama&pubname=yokohama-integrate-applications&ft:locale=en-US)**

    Get detailed information about Stream Connect producers and their performance, including a producer’s status and type, the number of bytes and messages produced to a topic, and producer data trends over time, in the Stream Connect dashboard.

-   **[Check data usage in the Stream Connect dashboard](https://www.servicenow.com/docs/access?context=stream-connect-dashboard&version=yokohama&pubname=yokohama-integrate-applications&ft:locale=en-US)**

    View total data usage and data usage per month and topic with the Stream Connect dashboard. Data usage history is available for the last 12 complete months plus the current month.

-   **[Use error evaluation with Data Stream actions](https://www.servicenow.com/docs/access?context=data-stream-actions&version=yokohama&pubname=yokohama-integrate-applications&ft:locale=en-US)**

    Catch step errors and specify error behavior for each step in a Data Stream action. Create your own error conditions by specifying when an action returns an error state and the status codes and messages they return.

-   **[View connection aliases in integration actions](https://www.servicenow.com/docs/access?context=managing-connections-integration-hub&version=yokohama&pubname=yokohama-integrate-applications&ft:locale=en-US)**

    Edit, configure, and create connection aliases in the Action Properties section of actions in ServiceNow® Workflow Studio. View connection error details for connection aliases that are not set up or configured.


## UI changes

-   **[Create an HTTP\(s\) connection](https://www.servicenow.com/docs/access?context=create-https-connection&version=yokohama&pubname=yokohama-platform-security&ft:locale=en-US) Options to specify the MID Server capabilities and MID application in a connection record**

    The Configure Connection form, that you use to configure a connection between your ServiceNow instance, and a third-party application now provides the following fields when you select **Auto-Select MID Server** from the MID Selection list.

    -   Capabilities: The capabilities that the MID Server must support to be eligible for selection.
    -   MID Application: The application that the MID Server must support to be eligible for selection.

## Activation information

Integration Hub is included in Workflow Data Fabric and is available with activation of an Workflow Data Fabric subscription package. For details, see [https://www.servicenow.com/now-platform/workflow-data-fabric.html](https://www.servicenow.com/now-platform/workflow-data-fabric.html).

## Removed in this release

**Important:**

-   Starting with the Yokohama release, Microsoft Teams Spoke is being prepared for future deprecation. It will be hidden and no longer activated on new instances but will continue to be supported. Microsoft Teams Graph Spoke provides the latest experience for this functionality.

    For more information, search for the term `Microsoft Teams Spoke for ServiceNow IntegrationHub` in [Plugins planned for deprecation](../eol/plugin-changes-v-to-y.md#).

-   Starting with the Yokohama release, Gremlin Spoke is being prepared for future deprecation. It will be hidden and no longer activated on new instances but will continue to be supported. Spoke Generator provides the latest experience for this functionality.

    For details, see the [Deprecation Process \[KB0867184\]](https://support.servicenow.com/kb?id=kb_article_view&sysparm_article=KB0867184) article in the Now Support knowledge base.


## Related ServiceNow applications and features

-   **[Workflow Studio](https://www.servicenow.com/docs/access?context=workflow-studio&version=yokohama&pubname=yokohama-build-workflows&ft:locale=en-US)**

    ServiceNow® Workflow Studio enables process owners to automate approvals, tasks, notifications, and record operations without having to code. You can use the Workflow Studio design environment to author flows and actions and to view the results that they produce.

-   **[App Engine Studio](https://www.servicenow.com/docs/access?context=aes-overview&version=yokohama&pubname=yokohama-application-development&ft:locale=en-US)**

    ServiceNow® App Engine Studio \(AES\) is a development tool for creators of varying skill levels to build applications that meet the immediate needs of your organization.

-   **[MID Server](https://www.servicenow.com/docs/access?context=mid-server-landing&version=yokohama&pubname=yokohama-servicenow-platform&ft:locale=en-US)**

    The Management, Instrumentation, and Discovery \(MID\) Server is a Java application that runs as a Windows service or UNIX daemon on a server in your local network. The ServiceNow® MID Server enables communication and the movement of data between a ServiceNow instance and external applications, data sources, and services.

-   **[Robotic Process Automation \(RPA\) Hub](https://www.servicenow.com/docs/access?context=rpa-main-landing-page&version=yokohama&pubname=yokohama-integrate-applications&ft:locale=en-US)**

    Use the ServiceNow® Robotic Process Automation \(RPA\) Hub to enable end-to-end automation for your organization. With a combination of UI interactions, element-based automations, and APIs that interact between the various business applications, you can emulate user actions and eliminate mundane and repetitive human activities.

-   **[Connections and Credentials](https://www.servicenow.com/docs/access?context=r-credentials&version=yokohama&pubname=yokohama-platform-security&ft:locale=en-US)**

    Credentials and connection information are required to gain access to a computer or network device for ServiceNow® Discovery, ServiceNow® Service Mapping, and ServiceNow® Cloud Management, or to perform work using ServiceNow® Orchestration. When adding content to share on the ServiceNow® Developer Site or the ServiceNow® Store, you can configure connections and credentials relevant to your environment without modifying the built content.


**Parent Topic:**[App development and low-code release notes](build-automate-rn-landing.md)

