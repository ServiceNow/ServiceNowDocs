---
title: Integrating with Computer Telephony Integration \(CTI\)
description: Integrate Customer Service Management \(CSM\) with Computer Telephony Integration \(CTI\) to enable and support voice features in your Workspace.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/customer-service-management/cti-csm-integration.html
release: australia
product: Customer Service Management
classification: customer-service-management
topic_type: concept
last_updated: "2026-03-12"
reading_time_minutes: 2
breadcrumb: [Integrate, Customer Service Management]
---

# Integrating with Computer Telephony Integration \(CTI\)

Integrate Customer Service Management \(CSM\) with Computer Telephony Integration \(CTI\) to enable and support voice features in your Workspace.

CTI helps integrate a telephony system to your ServiceNow Workspace via OpenFrame and Interaction Controls Component \(ICC\). Any third-party Contact Center as a Service \(CCaaS\) platform \(like Amazon Connect or Genesys\) can integrate to the ServiceNow CRM Platform. CCaaS can integrate their voice call controls and workflows into their provisioned ServiceNow instance to enable agents to handle phone calls directly within their Workspace.

CTI enables and supports the following capabilities:

-   **Screen pop:**

    When a call comes in, the Interaction record automatically opens in the ServiceNow instance.

-   **Click-to-dial:**

    When an agent selects a phone number in ServiceNow, the call is placed via CCaaS without any interruption.

-   **Presence sync:**

    The agent status \(Available, Away, Not Available\), as updated by the agent in the ServiceNow Workspace, is reflected in CCaaS.

-   **Call controls in the UI:**

    Hold, transfer, mute, and disconnect controls are available directly in the ServiceNow Workspace, without the agent needing to interact with the phone system separately.


Developers can use the CTI framework to integrate voice features using one or both approaches. As CTI is an integration concept rather than a product, it has no associated role. To enable CTI integration, developers must assign the sn\_openframe\_user role to agents who use the integrated voice features. In either approach, CTI serves as the underlying mechanism that connects the CCaaS platform to the provisioned ServiceNow instance.

-   OpenFrame embeds an external CCaaS provider’s telephony interface directly within the ServiceNow Workspace via an iFrame.
-   ICC delivers ServiceNow native voice call controls in a separate window within the CSM Configurable Workspace, when enabled.

When using CTI the user must have the OpenFrame user \(sn\_openframe\_user\) role.

For more information, see the following topics:

-   Computer Telephony Integration
-   [Computer Telephony Integration workflows](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/customer-service-management/cti-workflows.md)
-   [Interaction Controls Component \(ICC\) for voice calls](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/customer-service-management/contact-center-integration-with-icc.md)
-   [Use Interaction Controls Component \(ICC\) call controls with Amazon Connect](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/customer-service-management/amazon-connect-for-voice-calls.md)

