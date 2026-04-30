---
title: Integrating with contact centers
description: Integrate your contact center platform with the ServiceNow Customer Service Management \(CSM\) application to unify customer service teams through a single user interface. This integration centralizes routing across departments and channels, and optimizes workforce engagement for more personalized customer experiences and simplified employee experiences.
locale: en-US
release: zurich
topic_type: concept
last_updated: "2025-07-31"
reading_time_minutes: 2
breadcrumb: [Integrate, Customer Service Management]
---

# Integrating with contact centers

Integrate your contact center platform with the ServiceNow Customer Service Management \(CSM\) application to unify customer service teams through a single user interface. This integration centralizes routing across departments and channels, and optimizes workforce engagement for more personalized customer experiences and simplified employee experiences.

## Contact Center integration overview

Prerequisite: Ensure that agents are set up via configuration through their contact center integration to access the ServiceNow Workspace. The agent profiles are synced automatically when the agent logs in through the contact center connector in OpenFrame. For example, agent John Jason in the ServiceNow workspace must be able to log in to the contact center.

See [Implement the Interaction Controls Component \(ICC\) for contact center voice call and callback integration](../task/enable-icc-for-ccaas.md) to enable ICC for CCaaS calls.

Additionally, the agent presence state must match between the ServiceNow workspace and the contact center. In some cases, the state “available” might have a different name in the contact center environment, “on queue” for example.

Review the following architecture diagram for more insight on the contact center integration flow with ServiceNow.

![Contact center integration with ServiceNow architecture](../image/contact-center-integration-flow.png "Contact Center integration flow")

## External routing with Contact Centers

Contact center spokes allow communication between ServiceNow and contact centers via the contact center API. Using a spoke requires the use of [Integration Hub](https://www.servicenow.com/docs/access?context=integrationhub&version=zurich&pubname=zurich-integrate-applications&ft:locale=en-US), and each contact center provider creates a spoke with actions to initiate the routing instructions. In general, the actions should correspond to these external routing events:

-   New interaction
-   End interaction
-   Transfer to agent
-   Transfer to queue

The spoke should also be able to retrieve data, such as skills, queues, and wrap-up codes. To learn more about creating a spoke, refer to [Building spokes using Spoke Generator](https://www.servicenow.com/docs/access?context=spoke-builder&version=zurich&pubname=zurich-build-workflows&ft:locale=en-US).

The contact center provider uses the AWA Work Offer API to provide the agent target for the work items. This allows the contact center provider to provide parameters to accept conversations, reject conversations, set timeout duration, and set the ServiceNow agent ID. See [AWA Offer Work API](https://www.servicenow.com/docs/access?context=awa-offer-work-api&version=zurich&pubname=zurich-api-reference&ft:locale=en-US).

In the ServiceNow platform, you can import contact center platform skills, queues, and wrap-up codes between the ServiceNow instance and the contact center provider.

Contact center integration gives you the ability to route ServiceNow chats, emails, or cases via an external routing platform.

Implementing the integration includes the following high-level steps:

1.  Set up the ServiceNow environment, including credentials, the AWA queue, and the OpenFrame configuration.
2.  Set up the integration on the contact center side, matching the ServiceNow setup.
3.  Create test users and test the integration.

For specific instructions for integrating with Genesys Cloud, refer to the [Genesys Cloud documentation](https://help.mypurecloud.com/articles/about-unified-experience-from-genesys-and-servicenow/).

## For agents

As an agent, you can manage the chat with the customer using the inbox card alert by accepting or rejecting the chat. After accepting a chat, you can continue chatting with the customer through the workspace chat panel.

Agents using the integration can do the following:

-   Accept work items​.

    **Note:** If the agent doesn’t accept the chat within the configured timeout period, the work items may time out and return to the queue.

-   Reject work item​s
-   Transfer to another agent​
-   Transfer to a queue​
-   Cancel a transfer to another agent

