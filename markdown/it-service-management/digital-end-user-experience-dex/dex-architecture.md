---
title: DEX Architecture
description: Digital End-User Experience \(DEX\) architecture provides a seamless and integrated digital experience for end users.
locale: en-US
release: zurich
product: Digital End-User Experience \(DEX\)
classification: digital-end-user-experience-dex
topic_type: concept
last_updated: "2026-05-01"
reading_time_minutes: 5
breadcrumb: [Explore, Digital End-User Experience, IT Service Management]
---

# DEX Architecture

Digital End-User Experience \(DEX\) architecture provides a seamless and integrated digital experience for end users.

DEX uses a set of new multi-tenant, cloud-native services called ServiceNow shared services. In this architecture, DEX endpoint agents are able to communicate with the ServiceNow shared services without a MID Server. ServiceNow shared services provide authentication to DEX agents and enable message buffering and stateful stream processing of data sent to your ServiceNow instance and a time series datastore. ServiceNow shared services also enable a secure way to send policy updates and on-demand execution of checks on the DEX agents. Thus, ServiceNow shared services enable secure bi-directional communication between your ServiceNow instance and the DEX endpoint agents.

![High-level architectural diagram of Digital End-User Experience.](../image/architecture-diagram-MMASSET0021829.svg "DEX architectural diagram")

## Binaries installed on endpoints

-   Agent Client Collector \(ACC\): Deployed onto the end-user device endpoints such as a laptop or Virtual Desktop infrastructure \(VDI\) to collect various device level performance and operational metrics. ACC enables you to do the following:
    -   Configure a policy frequency to control what metrics are collected and the frequency of collection.
    -   Get the agent run remedial actions on the endpoint, such as clearing cache, restarting an application, and many more.
-   Browser extension: Helps track application performance and network metrics like page load time and network jitter. The communication between the browser extension and ACC, as well as the device and application metrics, are routed via the ServiceNow shared services. For more information, see [Enable DEX browser extension](../task/enable-dex-browser-extension.md).
-   DEX Desktop Assistant: Enables employees to incorporate ServiceNow functionalities into their daily workflow, providing access to monitoring local applications, requests, and push notifications and to performing network tests.

## Agent registration highlights

-   After the installation, ACC is registered on your organization's ServiceNow instance and the required certificates are downloaded from the instance. All the communication between ACC and your instance happens over secured HTTPS.
-   After the ACC registration, a connection with the ServiceNow shared services is established. The agent is authenticated with the shared services via the downloaded certificates.
-   ACC opens a bi-directional communication with the ServiceNow shared services using gRPC Remote Procedure Calls \(gRPC\) connection. gRPC connection is a secure and encrypted channel to send and receive data from the endpoints. The channel is secured via mutual Transport Layer Security \(mTLS\).
-   ACC sends various devices and application performance metrics to the shared services.
-   The instance also pushes data, such as DEX policies, to the agent via this bi-directional channel.
-   The ServiceNow shared services use the ServiceNow Hermes Messaging Service and Stream Connect to isolate your organization’s data.

    For more information, see [Hermes](https://www.servicenow.com/docs/bundle/yokohama-servicenow-platform/page/administer/hermes-messaging-service/concept/hermes-messaging-service.html) and [Stream Connect](https://www.servicenow.com/docs/bundle/yokohama-integrate-applications/page/administer/integrationhub/concept/stream-connect-quick-start.html).

-   Raw metrics collected from endpoints are processed further using the shared services and eventually pushed to your ServiceNow instance.
-   In addition, some of the configuration device metrics and agent heartbeats are directly pushed to the ServiceNow instance. The operation is performed over a secured HTTPS channel via a REST endpoint.

## Data security

There are various security measures to promote that the scripts are run securely.

-   Allow list: File shipped along with the agent verifying that no command other than the ones in the allow lists can be executed.

    For more information on the list, see [Generate an Agent Client Collector allow list](https://www.servicenow.com/docs/bundle/zurich-it-operations-management/page/product/agent-client-collector/task/acc-generate-allow-list.html).

-   Plugins certificate signing: The scripts are packaged in plugins which are deployed to the endpoint. To promote data integrity, the plugins can be signed by a certificate so that there are no malicious plugins deployed.

    For more information on certificate signing, see [Secure a custom plugin with a certificate](https://www.servicenow.com/docs/bundle/zurich-it-operations-management/page/product/agent-client-collector/concept/acc-self-sign-certificate.html).

-   Role-based access: All actions are available to only specific roles and user criteria within ServiceNow. For example, advanced actions can be assigned to the DEX engineer role and basic actions to the Service Desk.

    For more information, see [Configure the Remedial Actions Framework](https://www.servicenow.com/docs/bundle/zurich-it-service-management/page/product/service-operations-workspace/task/config-remedial-action-fw.html).

-   Audit: All action runs are audited in the Remedial Action Executions table \(ssn\_reacf\_remedial\_action\_execution\).

    For information about emergency plans \(such as notification and restore the service\), see [DEX subscription](dex-subscription.md).


## Data isolation

Your data is stored in a separate topic when the Hermes Messaging Service and Stream Connect persist in the file system while data is sent and received.

The agent client certificate issued by your ServiceNow instance holds the instance name for your organization. After the agent is authenticated, the instance name from the agent certificate is used to keep data isolated within a shared services cluster.

mTLS is used for a secure communication between the agent and server components. The agent authenticates itself using a client certificate with the following parameters:

-   Public Key Algorithm: id-ecPublicKey \(ECDSA\)
-   Key Size: 256-bit
-   Elliptic Curve: NIST Curve P-256

The setup promotes strong encryption and efficient key exchange using elliptic curve cryptography.

Agent assets and plugins \(like DEX\) that are downloaded from your ServiceNow instance through the shared services are signed by ServiceNow or the asset owners during their release. Signing promotes the authentication and integrity of the agent's asset or plugin to the agent.

## Data access

All collected data is transformed and presented on your ServiceNow instance.

Any data collected in the context of DEX is visible to users only with appropriate DEX roles. For more information about the DEX roles, see [Installed with DEX](../reference/components-installed-with-dex.md).

When following the standard ServiceNow practices on data governance, no special handling is required for DEX.

## Data retention

All the raw metrics collected from devices are stored in the ServiceNow instance for a maximum of seven days. Aggregated metrics are stored for a longer duration based on the type of aggregation. Aggregation metrics are used to show trend lines for various metrics. Hermes Messaging Service stores data for 36 hours by default. No other ServiceNow shared services store any metric data in transit.

