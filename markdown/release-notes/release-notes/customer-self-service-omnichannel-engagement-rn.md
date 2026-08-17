---
title: Self-service and omnichannel engagement for CSM release notes
description: With self-service and omnichannel applications in the ServiceNow Customer Service Management \(CSM\) application, your customers can use chat on self-service portals, consumer messaging apps, email, or phone to connect with your organization. Self-service and omnichannel applications for CSM were enhanced and updated in the Zurich release.
locale: en-US
release: zurich
topic_type: reference
last_updated: "2025-07-31"
reading_time_minutes: 9
---

# Self-service and omnichannel engagement for CSM release notes

With self-service and omnichannel applications in the ServiceNow® Customer Service Management \(CSM\) application, your customers can use chat on self-service portals, consumer messaging apps, email, or phone to connect with your organization. Self-service and omnichannel applications for CSM were enhanced and updated in the Zurich release.

## Self-service and omnichannel applications for CSM highlights for the Zurich release

-   Integrate Amazon Connect with Interaction Controls Component \(ICC\) voice call features to allow agents manage phone interactions directly within their Workspace.
-   Allows agents to select a queue when making outbound calls to improve routing, reporting, and compliance.
-   Integrate WhatsApp Cloud API with CSM to enable rich media messaging, interactive controls, Virtual Agent automation, and Agent Workspace support without third-party dependencies.
-   Enable external routing of email interactions to reduce administrative effort.
-   Improve agent callback transfers for smoother handovers and support customers to request scheduled callbacks.

See [Omnichannels for communicating with customers](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/customer-service-management/omnichannels-communicating-customers.md) and [Interaction Controls Component \(ICC\) for voice calls](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/customer-service-management/contact-center-integration-with-icc.md) for more information.

**Important:** Self-service and omnichannel applications are available in the ServiceNow Store. For details, see the "Activation information" section of these release notes.

## New in the Zurich release

-   **[Using Interaction Controls Component \(ICC\) call controls with Amazon Connect](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/customer-service-management/amazon-connect-for-voice-calls.md)**

    Manage Amazon Connect calls directly in the CSM Configurable Workspace voice Interaction record page. This integration supports inbound and outbound call flows, presence management, and call transfers without switching applications.

-   **[Selecting queues for outbound calls](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/customer-service-management/select-queues-for-outbound-calls.md)**

    Enable agents to designate a specific queue for their outbound calls directly from the keypad or the phone directory in the Global Call window to improve routing and reporting. This provides a streamlined search interface that enables agents to find and select a single queue that can be applied across all outbound dialing methods.

-   **[Integrating WhatsApp with Customer Service Management using the WhatsApp Cloud API](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/customer-service-management/messg-integrating-whatsapp-with-csm-whatsapp-cloud.md)**

    Connect directly to WhatsApp Cloud API for more reliable, feature-rich customer support without third-party dependencies. The key capabilities include the following:

    -   Send and receive text messages for direct customer communication.
    -   Exchange images, videos, audio files, and documents for clearer, more contextual conversations.
    -   Simplify customer input with list pickers and location sharing.
    -   View typing indicators for more natural conversational flow.
    -   Automatically capture and record customer opt-in and opt-out messages to ensure compliance with WhatsApp's messaging policies.
-   **[Defining CCaaS callbacks](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/customer-service-management/interaction-controls-component-icc-callback-integration-features.md)**
    -   Offer callers a callback option that lets them retain their position in the queue and receive a call when an agent is available. Alternatively, callers can choose a specific date and time for the callback, also known as scheduled callback.
    -   As an agent, view callback requests in the order that they're received.
-   **[CCaaS callback features](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/customer-service-management/contact-center-intergration-with-icc-callback.md)**

    As an agent, address callback requests from the CSM Configurable Workspace. Initiate callbacks and manage active calls with the Callback context card and Callback Actions component on the voice interaction page.

    On the Callback actions component, you can use the **Call number** option to initiate a call; alternatively, the call can be initiated automatically at the end of the preview timer when enabled. After the call has ended, the **Close callback** option closes the callback interaction and changes the status to Closed complete. Agents can also retry the callback as needed.

    Monitor the callback life cycle and capture the preview time that measures the time between when an agent accepts the callback request and the agent dials out the customer.

-   **[Global call list](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/customer-service-management/ccaas-global-call-list.md)**

    Switch between workspaces using the global call list. As a CSM agent, you can accept calls and open interaction records in supported, unsupported, or default workspaces.

-   **[Phone directory](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/customer-service-management/ccaas-phone-directory.md)**

    Access the embedded phone directory in your CSM Configurable Workspace via Interaction Controls Component \(ICC\) to make outbound calls to external and internal contacts.

-   **[Call resiliency](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/customer-service-management/ccaas-call-resiliency.md)**

    Route phone calls to the CSM Configurable Workspace without creating an interaction record, helping agents handle calls even during connectivity issues.

-   **[Voice Controls Simulator tool](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/customer-service-management/voice-control-simulator-tool.md)**

    Test and validate voice call UI flows in the CSM Configurable Workspace to ensure CCaaS partners have clear insights into their supported voice control capabilities.

-   **[Monitoring calls](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/customer-service-management/call-monitoring.md)**

    Enable supervisors to monitor, coach, and barge-in on calls in real time by integrating ServiceNow's native voice call feature within an active call interface.


## UI changes

-   **[Selecting queues for outbound calls](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/customer-service-management/select-queues-for-outbound-calls.md)**

    The following UI components have been added to the Global Call window when making outbound calls from a keypad or phone directory:

    -   A new Search field to search and select from a list of available queues.
    -   A new toggle control that applies the selected queue to either the current call or all outbound calls by default. This option appears after selecting a queue.
-   **[Using the voice interaction page for callback requests](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/customer-service-management/csm-native-voice-record-page.md)**

    The following UI components have been added on the voice interaction page to manage callback requests:

    -   A Callback Actions component enables agents to initiate a call to the customers.
    -   A Callback Context card enables agents to get quick context before initiating the call.
    -   A Transfer button has been added in the Callback actions component to enable agents to transfer callback requests.
    -   The scheduled start time option has been added in the callback context card to help agents access the date and time of the scheduled callback and enable smoother conversations.
    -   The callback context card appears at the center of the voice interaction page to help agents stay informed and efficient during customer interactions.
    -   The following options have been added to the Reason for the Call list to help agents better capture the reason for callbacks:
        -   Customer Survey
        -   Sales Discovery
        -   Product Feedback
        -   Customer Relationship Building
-   **[Using the email interaction page](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/customer-service-management/using-email-interaction-page.md)**

    The following changes have been made to the Email Interaction page:

    -   A New Activity marker has been added to help distinguish the most recent conversation.
    -   A modeless dialog has been added to respond to emails without interrupting your workflow, enabling you to multitask and easily refer to record details.
    -   A compact email header has been added to help you focus on key message details.
    -   The activity stream shows only the latest reply in the email conversation for each response.
-   **[Using Agent Chat](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/conversational-interfaces/ci-agent-chat-using.md)**

    A **Leave Chat** button has been added to the record page so you can leave the chat without ending the session for other participating agents.


-   **Coral theme**

    Coral is now the default theme for new portal, web, and mobile experiences with Next Experience or Core UI enabled. This theme provides a fresh look and feel, featuring brand-neutral illustrations to enhance your user experience. A dark theme option is available for web and mobile experiences.


## Changed in this release

-   **[Using the email interaction page](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/customer-service-management/using-email-interaction-page.md)**

    View annotations for the most recent activity along with a compact email header that includes the subject, sender, and receiver details in the activity stream. Focus on new or unread email messages rather than the entire email conversation.

    View or edit the interaction record while drafting an email in a modeless dialog, keeping all relevant information accessible.

-   **[Using Agent Chat](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/conversational-interfaces/ci-agent-chat-using.md)**

    Leave a chat without ending it for other agents, enabling you to complete your task and exit the chat.

    Confirm before closing a chat tab to avoid unintentionally leaving the chat.

    Enable multiple agents to add wrap-up codes and comments for a single chat.

-   **[Import queues](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/customer-service-management/import-queues.md)**

    Review and update queues imported from a contact center in a post-import page. The post-import page for a queue mirrors the existing post-import pages for skills and wrap-up codes, providing a consistent user experience.

-   **[Interaction Controls Component \(ICC\) call features](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/customer-service-management/interaction-controls-component-icc-call-interaction-features.md)**

    Notify agents when a supervisor is coaching or has joined an active call while monitoring agents directly through the CCaaS system.

-   **[CCaaS callback features](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/customer-service-management/contact-center-intergration-with-icc-callback.md)**

    Callback management has been improved to make handling requests easier for agents. The key changes include:

    -   Equip agents to transfer the callback requests before dialing the call, enhancing flexibility in managing customer interactions.
    -   Enable scheduled callbacks, which help customers to choose a preferred callback time in addition to the existing ASAP option.
    -   Facilitate agents to view the list of queues and other agents for easier callback transfers and efficient customer management.
    -   Capture callback reasons more effectively with the expanded Reason for Call field, which includes additional choice values.
-   **[Unified routing of email interactions via CCaaS](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/customer-service-management/using-email-interaction-customer-service-management.md)**

    Email interaction handling has been enhanced to improve efficiency and responsiveness in managing customer communications. The key changes include:

    -   Support external routing of email interactions.
    -   Enable agents to put email interactions on hold while waiting for customer responses.
    -   Notify CCaaS when an interaction is put on hold so that CCaaS can free up the agent's capacity for handling other interactions.
    -   Send automatic email reminders to customers for interactions that are on hold for a configurable period.
    -   Reroute email interactions to available agents when the originally assigned agent is unavailable.
    -   Prevent creating outbound email interactions when emails are sent on top of cases.
-   **[Import queues](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/customer-service-management/import-queues.md)**

    Use bulk action to assign service channels to multiple queues simultaneously during queue-import, simplifying queue management for CCaaS integrations.

-   **Portal Data List widget**

    The Data List widget now offers more configuration flexibility and supports dynamic, context‑aware view selection. Key enhancements include:

    -   Role‑Based and Guest Views: Use the new role\_based\_views and guest\_view options to define different views for different user roles and for unauthenticated users removing the dependency on a single static view.
    -   Automatic URL Parameter Passing: Pass URL parameters automatically into scripts invoked from Data List instance options enabling admins to build richer, multi‑parameter conditions without extra setup.
    -   Script‑Based View Selection: Use the Data List Condition Script option to choose a view dynamically. Scripts can evaluate URL parameters and other context to determine the most appropriate view at runtime.
    -   Configurable Default Sorting: Define initial sorting behavior using the new sort\_by and sort\_order options letting the users see a meaningful default order when the list loads.

## Deprecations

Starting with the Zurich release, Customer Service CTI Demo Data Plugin and CTI Softphone Plugin are no longer deployed, enhanced, or supported. For details, see the [Deprecation Process \[KB0867184\]](https://hi.service-now.com/kb_view.do?sysparm_article=KB0867184) article in the Now Support Knowledge Base, [Components installed with Customer Service CTI Demo Data](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/customer-service-management/r_InstalledWithCustServCTIDemoData.md), and [Components installed with CTI Softphone](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/customer-service-management/r_InstalledWithCCTISoftphone.md).

## Activation information

Install self-service and omnichannel applications, such as OpenFrame and Interaction Controls Component \(ICC\), by requesting them from the ServiceNow Store. Visit the [ServiceNow Store](https://store.servicenow.com/sn_appstore_store.do#!/store/home) website to view all the available apps and for information about submitting requests to the store. For cumulative release notes information for all released apps, see the [ServiceNow Store version history release notes](https://www.servicenow.com/docs/r/store-release-notes/sn-store-release-notes.html).

## Browser requirements

Internet Explorer isn't supported. For more information, see [Browser support](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/platform-user-interface/browser-support.md).

## Accessibility information

-   **Dark theme**

    The new Coral theme includes a dark theme option for web and mobile experiences. This option is commonly used to alleviate eye strain and improve readability.


## Related ServiceNow applications and features

-   **[Field Service Management](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/field-service-management/fsm-application-landing-page.md)**

    The Field Service Management application helps you manage work orders and related tasks, resources, skills, assets, and locations. Assign work order tasks and dispatch agents to a customer location to perform field work.

-   **[Knowledge Management](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/servicenow-platform/knowledge-management.md)**

    From the Customer Service Portal and Consumer Service Portal, enable your customers to search for shared information using the Knowledge Management application. Customer service agents can use knowledge content to help resolve cases.

-   **[IT Service Management](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/it-service-management/r_ITServiceManagement.md)**

    The following IT Service Management applications can integrate with Customer Service Management: [Incident Management](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/customer-service-management/csm-integration-sm-incident.md), [Problem Management](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/customer-service-management/csm-integration-sm-problem.md), [Change Management](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/customer-service-management/csm-integration-sm-change.md), and [Request Management](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/customer-service-management/csm-integration-sm-request.md). With these integrations, you can create incident, problem, change, and request records from customer service cases. Customers can also submit requests from the Customer Service Portal.


**Parent Topic:**[Customer Service Management release notes](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/release-notes/customer-service-mgmt-rn-landing.md)

