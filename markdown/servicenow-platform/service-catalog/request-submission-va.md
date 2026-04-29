---
title: Submit a request topic conversation
description: Users can submit a request in a Virtual Agent conversation.
locale: en-US
release: australia
product: Service Catalog
classification: service-catalog
topic_type: concept
last_updated: "2026-03-12"
reading_time_minutes: 2
breadcrumb: [Service Catalog topic blocks in Virtual Agent powered by NLU, Service Catalog Reference, Service Catalog, Manage service capabilities, Extend ServiceNow AI Platform capabilities]
---

# Submit a request topic conversation

Users can submit a request in a Virtual Agent conversation.

The Submit a request topic conversation uses the following topic blocks:

-   Search Catalog Item
-   Request Catalog Item

Using the Submit a request topic conversation, users can submit a request by choosing from all available options. For example, when a user is requesting an item, the Virtual Agent prompts the user to enter a search keyword. After the user enters the keyword, the Virtual Agent responds with available choices in a carousel view.

When the user selects the required item, the following scenarios are possible:

-   A user can submit a request in the conversation mode \(by answering the questions in line\). After the request submission, a requested item card is displayed with the request number as a link to the request page.![Requested completed card in Virtual Agent](../image/va-request-complete.png)

    **Note:** In Now® Mobile, the URL opens the native screen.

-   A user can submit a request in a popup or a window.

    -   In case of a popup, Virtual Agent provides a link for the user to submit the request in a popup without navigating to a new tab. A non-conversational catalog item can be rendered as a popup only if it does not have any Custom, Custom with label, or UI Page variables. For more information, see [Service Catalog topic blocks in Virtual Agent](request-topic-blocks-va.md).
    -   In case of a window, Virtual Agent provides a link for the user to submit the request in the Service Portal defined in the **sn\_itsm\_va.com.snc.itsm.virtualagent.portal\_url** property. A non-conversational item will be rendered as a window it has a Custom, Custom with label, or UI Page variable. For more information, see [Service Catalog topic blocks in Virtual Agent](request-topic-blocks-va.md).
    **Note:** Now Mobile opens the item in Mobile Employee Service Portal \(mesp\).

    ![Submit a Request virtual agent chatbot dialogue.](../image/SubmitaRequest.png)


**Parent Topic:**[Service Catalog topic blocks in Virtual Agent powered by NLU](request-topic-blocks-va.md)

**Related topics**  


[Service Catalog topic blocks in Virtual Agent powered by NLU](request-topic-blocks-va.md)

