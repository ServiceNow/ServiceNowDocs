---
title: Setting up ServiceNow Voice
description: Enable ServiceNow Voice and integrate it with a third-party phone system such as Amazon Connect.
locale: en-US
release: zurich
topic_type: concept
last_updated: "2025-07-31"
reading_time_minutes: 2
breadcrumb: [ServiceNow Voice, Manage people and work capabilities, Extend ServiceNow AI Platform capabilities]
---

# Setting up ServiceNow Voice

Enable ServiceNow Voice and integrate it with a third-party phone system such as Amazon Connect.

When you set up a third-party phone system and integrate it with the ServiceNow instance, an agent can accept an incoming call or make an outbound call from the ServiceNow instance using the integrated softphone. This experience is based on the configurations made within the third-party phone system.

## Get started with Voice

1.  Procure a license for a ServiceNow application, such as ITSM or CSM, which includes ServiceNow Voice.
2.  Install the ServiceNow Voice applications in ServiceNow® Store. For information about this installation, see [Install ServiceNow Voice applications](../task/install-ccc-apps.md).
3.  Sign up and create an account with a third-party phone system. By default, Amazon Connect is supported. For information about creating an Amazon Web Services \(AWS\) account, see the Amazon [documentation](https://aws.amazon.com/premiumsupport/knowledge-center/create-and-activate-aws-account/).
4.  Configure the framework for the third-party phone system within the ServiceNow instance. By default, the framework is supported for Amazon Connect. For information about this configuration, see [Integrate ServiceNow Voice with Amazon Connect](../task/integrate-ccc-amazonconnect.md).

-   **[Install ServiceNow Voice applications](../task/install-ccc-apps.md)**  
You can install the ServiceNow Voice applications if you have the admin role. The application includes demo data and installs related ServiceNow® Store applications and plugins if they are not already installed.
-   **[Domain separation and ServiceNow Voice](domain-separation-voice.md)**  
 Domain separation is supported for ServiceNow Voice. Domain separation enables you to separate data, processes, and administrative tasks into logical groupings called domains. You can control several aspects of this separation, including which users can see and access data.
-   **[Configuring a phone PIN](set-pin-ccc.md#)**  
You can set up or reset a phone PIN that can be used for caller authentication during a call with an agent.
-   **[Configure the E.164 format for a consumer phone number](../task/configure-e614-consumer.md)**  
Ensure that all the necessary information for a phone number is included and properly formatted to successfully route an international call over a territory's public telephone network. Provide the E.164-compliant formatting and validation for phone number.
-   **[Configuring CTI component logging](../task/config-cti-comp-log.md)**  
Configure CTI component logging to enable component logging to the system logs.
-   **[Configure Real Time Transcription for ServiceNow Voice Customer Service Management](../task/configure-rtt-sn-voice.md)**  
Configure settings in your Amazon Connect instance, and in your ServiceNow instance to allow agents to see a real time transcription of voice calls with customers.
-   **[Configure Real Time Transcription for ServiceNow Voice for IT Service Management](../task/configure-rtt-sn-voice-itsm.md)**  
Configure settings in your Amazon Connect instance, and in your ServiceNow instance to allow agents to see a real time transcription of voice calls with customers.
-   **[Scripting for operation handlers](cloud-call-center-api.md)**  
You can use the APIs in the ServiceNow Voice framework to create a seamless voice call experience for your callers and agents.

**Parent Topic:**[ServiceNow Voice](cloud-call-center-overview.md)

