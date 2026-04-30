---
title: Self-service and omnichannel engagement for CSM release notes
description: With ServiceNow Omnichannel support, your customers can use chat on self-service portals or consumer messaging apps to connect with your organization, or connect using email or phone. ServiceNow Omnichannel and self-service applications were enhanced and updated in the Yokohama release.
locale: en-US
release: yokohama
topic_type: reference
last_updated: "2025-01-30"
reading_time_minutes: 4
---

# Self-service and omnichannel engagement for CSM release notes

With ServiceNow® Omnichannel support, your customers can use chat on self-service portals or consumer messaging apps to connect with your organization, or connect using email or phone. ServiceNow® Omnichannel and self-service applications were enhanced and updated in the Yokohama release.

## Omnichannel and self-service highlights for the Yokohama release

-   Integrate with contact centers using Contact Center Integration Core to import data from a third party contact center as a service \(CCaaS\) application.
-   Better integrate with contact centers by adding call controls to Agent Workspace with Interaction Controls Component \(ICC\).
-   Enhance B2B customer support through ServiceNow® self-service capabilities with the new Business Portal.
-   Provide a consistent experience for agents handling omnichannel interactions through email interactions, which preserve the context for agents by associating the email conversation between the agent and the customer.
-   Improve contact center efficiency by helping avoid the creation of duplicate cases through the use of the Email as an Interaction feature.

See [Omnichannels for communicating with customers](https://www.servicenow.com/docs/access?context=omnichannels-communicating-customers&version=yokohama&pubname=yokohama-customer-service-management&ft:locale=en-US), [Self-service for Customer Service Management](https://www.servicenow.com/docs/access?context=self-service-options-csm-customers&version=yokohama&pubname=yokohama-customer-service-management&ft:locale=en-US), and [Playbooks for Portals](https://www.servicenow.com/docs/access?context=playbooks-for-portals&version=yokohama&pubname=yokohama-customer-service-management&ft:locale=en-US) for more information.

**Important:** Engagement Messenger, Playbooks for Portals, and Omnichannel applications are available in the ServiceNow Store. For details, see the "Activation information" section of these release notes.

## New in the Yokohama release

-   **[Business Portal](https://www.servicenow.com/docs/access?context=configure-business-portal&version=yokohama&pubname=yokohama-customer-service-management&ft:locale=en-US)**

    Support your customers through the Business Portal self-service capabilities, such as knowledge articles, service catalogs, case management, Virtual Agent, and others. Help reduce maintenance effort through low-code configurations on pages with configurable widgets.

-   **[Email as an Interaction](https://www.servicenow.com/docs/access?context=omnichannels-communicating-customers&version=yokohama&pubname=yokohama-customer-service-management&section=email-channel&ft:locale=en-US)**

    Enhance case management with the Email as an Interaction feature.

    -   Transform emails into interactions, enabling customer communication to be tracked in a central location and help avoid unnecessary case creation.
    -   Manage straightforward customer inquiries via email, create cases for more complex issues, or link emails to existing cases.
    -   Notify agents on email responses received from customers.
-   **[Contact Center Integration Core](https://www.servicenow.com/docs/access?context=contactcenter-integration&version=yokohama&pubname=yokohama-customer-service-management&ft:locale=en-US)**

    As an admin, import data automatically from a third-party contact center as a service \(CCaaS\) application to facilitate external routing and third-party telephony integration in their ServiceNow® instance.

    **Note:** The Contact Center Integration Core is a framework that includes voice call features, which doesn't work unless CCaaS implements it.

    -   Import records such as queues, skills, and wrap-up codes from a third party into your ServiceNow instance.
    -   Maintain data consistency between your ServiceNow instance and third-party systems. Verify that chats and cases are routed to the correct agent and that the correct wrap-up codes are available when dispositioning an interaction.
-   **[Interaction Controls Component \(ICC\)](https://www.servicenow.com/docs/access?context=contact-center-integration-with-icc&version=yokohama&pubname=yokohama-customer-service-management&ft:locale=en-US)**

    As an agent, manage calls, such as muting, holding, and transferring, directly within the Configurable Workspace. As a part of the new Voice interaction page experience, the ICC framework helps improve workflow efficiency and promotes a consistent agent experience across all channels.

    **Note:** ICC must be integrated with your specific Contact Center as a Service \(CCaaS\) plugin to establish the telephony connection.

    Connect customers with field agents or third-party support teams in the embedded call interface. Choose between the following transfer options:

    -   Consult transfer: Share the call context with the external contact before transferring the customer.
    -   Blind transfer: Immediately transfer the call to the external contact.
-   **[OpenFrame Integration to Interaction Controls Component \(ICC\)](https://www.servicenow.com/docs/access?context=interaction-controls-component&version=yokohama&pubname=yokohama-customer-service-management&ft:locale=en-US)**

    ICC is a new component for a native call controls interface embedded in Agent Workspace. With the ICC component, you can do the following:

    -   Create the state context in OpenFrame to read the state of idle and active call state, and the state of the transfer.
    -   Provide iframe sandbox parameters to allow iframe access to security features and to enable additional iframe restrictions.
    -   Create an extension point implementation to create and get phone log segments.
-   **[Integrating Conversational SMS with AWS End User Messaging](https://www.servicenow.com/docs/access?context=conversational-sms-integration-amazon&version=yokohama&pubname=yokohama-conversational-interfaces&ft:locale=en-US)**

    Integrate the ServiceNow SMS channel with AWS end-user messaging to engage in conversations with Now Virtual Agent and live agents to address and resolve any customer queries or issues.


## UI changes

-   **[Using the email interaction page](https://www.servicenow.com/docs/access?context=using-email-interaction-page&version=yokohama&pubname=yokohama-customer-service-management&ft:locale=en-US)**

    The following UI elements have been added to the Email Interaction page:

    -   A **Contact** card to simplify the process of adding and viewing customer information.
    -   A **Customer History** tab that displays the details of previous conversations between the customer and the agent.

## Changed in this release

-   **[Using the email interaction page](https://www.servicenow.com/docs/access?context=using-email-interaction-page&version=yokohama&pubname=yokohama-customer-service-management&ft:locale=en-US)**

    Manage and view customer-related information and past conversations while interacting with customers via email.

-   **[Using the Now Assist in Virtual Agent enhanced chat in self-service portals](https://www.servicenow.com/docs/access?context=nass-portal&version=yokohama&pubname=yokohama-customer-service-management&ft:locale=en-US)**

    Receive comprehensive and detailed answers with intelligent search and conversational experiences using Now Assist in Virtual Agent. The search results are synthesized from Knowledge Base articles, Virtual Agent articles, and catalog items with links to the sources. The agent retains conversation context across multi-turn questions, promoting continuity and relevance in responses.


## Activation information

Install the Engagement Messenger, Playbook for Portals, and Omnichannel applications by requesting them from the ServiceNow Store. Visit the [ServiceNow Store](https://store.servicenow.com/sn_appstore_store.do#!/store/home) website to view all the available apps and for information about submitting requests to the store. For cumulative release notes information for all released apps, see the [ServiceNow Store version history release notes](https://docs.servicenow.com/bundle/store-release-notes/page/release-notes/store/sn-store-release-notes.html).

## Browser requirements

Internet Explorer isn't supported.

## Related ServiceNow applications and features

-   **[Field Service Management](https://www.servicenow.com/docs/access?context=fsm-application-landing-page&version=yokohama&pubname=yokohama-field-service-management&ft:locale=en-US)**

    The Field Service Management application helps you manage work orders and related tasks, resources, skills, assets, and locations. Assign work order tasks and dispatch agents to a customer location to perform field work.

-   **[Knowledge Management](https://www.servicenow.com/docs/access?context=knowledge-management&version=yokohama&pubname=yokohama-servicenow-platform&ft:locale=en-US)**

    From the Customer Service Portal and Consumer Service Portal, enable your customers to search for shared information using the ServiceNow® Knowledge Management application. Customer service agents can use knowledge content to help resolve cases.

-   **[IT Service Management applications](https://www.servicenow.com/docs/access?context=r_ITServiceManagement&version=yokohama&pubname=yokohama-it-service-management&ft:locale=en-US)**

    Customer Service Management includes integrations with the following ServiceNow® Service Management applications: [Incident Management](https://www.servicenow.com/docs/access?context=csm-integration-sm-incident&version=yokohama&pubname=yokohama-customer-service-management&ft:locale=en-US), [Problem Management](https://www.servicenow.com/docs/access?context=csm-integration-sm-problem&version=yokohama&pubname=yokohama-customer-service-management&ft:locale=en-US), [Change Management](https://www.servicenow.com/docs/access?context=csm-integration-sm-change&version=yokohama&pubname=yokohama-customer-service-management&ft:locale=en-US), and [Request Management](https://www.servicenow.com/docs/access?context=csm-integration-sm-request&version=yokohama&pubname=yokohama-customer-service-management&ft:locale=en-US). With these integrations, you can create incident, problem, change, and request records from customer service cases. Customers can also submit requests from the Customer Service Portal.


**Parent Topic:**[Customer Service Management release notes](customer-service-mgmt-rn-landing.md)

