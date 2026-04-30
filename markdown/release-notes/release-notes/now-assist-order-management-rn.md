---
title: Now Assist for Order Management release notes
description: The ServiceNow Now Assist for Order Management application brings platform AI capabilities to Sales Customer Relationship Management. Now Assist for Order Management is a new application in the Zurich release.
locale: en-US
release: zurich
topic_type: reference
last_updated: "2026-01-30"
reading_time_minutes: 6
---

# Now Assist for Order Management release notes

The ServiceNow® Now Assist for Order Management application brings platform AI capabilities to Sales Customer Relationship Management. Now Assist for Order Management is a new application in the Zurich release.

## Now Assist for Order Management highlights for the Zurich release

[Zurich Patch 7](../quality/zurich-patch-7.md)

-   Enable business-to-business \(B2B\) customers to create invoice dispute cases through AI-powered chat and voice assistants that guide them through conversational dispute intake on the Business Portal.
-   Provide uninterrupted handoff to human agents to support complex use cases, with full conversation context transferred to the CSM/FSM Configurable Workspace.
-   RMA AI agent for automated RMA entitlement and intelligent case handling.

[Zurich Patch 5](../quality/zurich-patch-5.md)

-   Review changes to Now Assist usage measurement.

[Zurich Patch 4](../quality/zurich-patch-4.md)

-   Enable B2B customers to submit order cases autonomously from the Business Portal by simply describing their needs in natural language using the manage order operations agent.
-   Summarize complex orders across products, services, and fulfillment tasks, enabling agents to quickly understand status, take the right actions, and avoid navigating fragmented views to make the next steps easier and improving productivity.

See [Now Assist for Order Management](https://www.servicenow.com/docs/access?context=now-assist-order-management&version=zurich&pubname=zurich-order-management&ft:locale=en-US) for more information.

**Important:** Now Assist for Order Management is available in the ServiceNow Store. For details, see the "Activation information" section of these release notes.

## Now Assist for Order Management features

[Zurich Patch 7](../quality/zurich-patch-7.md)

-   **[AI-powered invoice case management for customers](https://www.servicenow.com/docs/access?context=dispute-invoice-issues-now-assist&version=zurich&pubname=zurich-order-management&ft:locale=en-US)**

    Enable customers to report quantity-related invoice disputes through an AI-powered virtual assistant on the Business Portal. Customers can describe the discrepancies through natural conversation, and the assistant validates details, creates cases, and autonomously resolves eligible disputes by issuing credit notes or replacement orders, or connects customers with a human agent when needed.

-   **[Invoice dispute intake with voice assistant](https://www.servicenow.com/docs/access?context=now-assist-invoice-mgmt-voice-aiagent&version=zurich&pubname=zurich-order-management&ft:locale=en-US)**

    Enable customers to report quantity-related invoice disputes using voice commands through an AI-powered voice assistant on the Business Portal. Customers can describe discrepancies through natural speech and the assistant captures dispute details to create invoice cases or connects customers with a human agent.

-   **[Human agent handoff with context transfer](https://www.servicenow.com/docs/access?context=resolve-invoice-case-now-assist-agent&version=zurich&pubname=zurich-order-management&ft:locale=en-US)**

    Help customers to escalate complex disputes seamlessly to a live agent. The full conversation context, including invoice details, dispute reason, and prior AI actions are transferred to the CSM/FSM Configurable Workspace, enabling live agents to continue without asking customers to repeat information.

-   **[Now Assist for invoice case resolution](https://www.servicenow.com/docs/access?context=resolve-invoice-case-now-assist-agent&version=zurich&pubname=zurich-order-management&ft:locale=en-US)**

    Help accelerate invoice dispute resolution by surfacing similar cases and common resolution patterns in the Now Assist panel. Agents can request help with an invoice case to view how similar disputes were resolved, reducing research time and improving consistency.

-   **[Automated email notifications for invoice cases](https://www.servicenow.com/docs/access?context=now-assist-order-management-using&version=zurich&pubname=zurich-order-management&ft:locale=en-US)**

    Keep customers informed with automated email notifications at key points in the invoice case life cycle, including case creation confirmation, resolution details with credit note or replacement order information, and the next steps for cases requiring human review.

-   **[Return Merchandise Authorization](https://www.servicenow.com/docs/access?context=return-merchandise-authorization&version=zurich&pubname=zurich-order-management&ft:locale=en-US)**

    Leverage the RMA AI agent for automated entitlement and case handling with the following features:

    -   Automates entitlement checks with real‑time warranty validation
    -   Selects best‑fit resolution and sends for customer approval
    -   Generates recommended actions when no valid entitlement is found
    -   Provides proactive case updates and follow‑ups
    -   Answers customer queries and handles multi‑intent emails

[Zurich Patch 4](../quality/zurich-patch-4.md)

-   **[Enable the manage order operations agent in the Business Portal](https://www.servicenow.com/docs/access?context=enable-manage-order-operations-ai-agent&version=zurich&pubname=zurich-order-management&ft:locale=en-US)**

    Activate the manage order operations agent so that you can make the agent available to your customers on the Business Portal.

-   **[Request order changes using Now Assist](https://www.servicenow.com/docs/access?context=request-order-changes-now-assist&version=zurich&pubname=zurich-order-management&ft:locale=en-US)**

    Use the manage order operations agent to provide a seamless experience to your customers on the Business Portal, enabling them to create order cases using a virtual assistant effortlessly. The AI agent can intelligently categorize requests for expedited delivery by creating order-related cases linked directly to the specific order, significantly reducing manual case creation and speeding up resolution times. Interaction channels include chat and voice options.

-   **[Summarize an order using Summarization for Order Management](https://www.servicenow.com/docs/access?context=now-assist-order-mgmt-summarize-order&version=zurich&pubname=zurich-order-management&ft:locale=en-US)**

    Generate a summary of a complex order for a unified view of the order's current state to:

    -   Respond confidently to customer queries with accurate, real-time order status.
    -   Track changes and validate details to maintain consistency and transparency.
    -   Minimize errors and improve communication across suppliers and partners.
    -   Monitor tasks that are at risk of missing deadlines.
    -   Assign tasks to appropriate resources based on priority and skill.
    -   Make rapid prioritization decisions to avoid delays and help ensure timely fulfillment.

## Changed in this release

-   **[Changes to Now Assist usage measurement](https://www.servicenow.com/docs/access?context=monitoring-now-assist-usage&version=zurich&pubname=zurich-platform-administration&ft:locale=en-US)**

    Starting with Zurich Patch 5, Now Assist usage measurement is transitioning from a 365-day look-back model to a 365-day burn-down model, with usage resetting at the contract anniversary date. For more information, refer to [KB KB2704710: Now Assist Usage - Overview &amp; New Measurement Logic](https://support.servicenow.com/kb?id=kb_article_view&sysparm_article=KB2704710).


## Activation information

Request the Now Assist for Order Management application from the [ServiceNow Store](https://store.servicenow.com/sn_appstore_store.do#!/store/application/b75a55a63f71b6108428dd8d001f8bca) and install it using the ServiceNow® Application Manager. For more information, see [Install a ServiceNow Store application](https://www.servicenow.com/docs/access?context=t_InstallApplications&version=zurich&pubname=zurich-platform-administration&ft:locale=en-US).

## Plugin information

-   **New plugins**

    The following plugins are new in Zurich:

    [Zurich Patch 7](../quality/zurich-patch-7.md)

    -   Manage Invoice Operations \(com.sn\_inv\_ops\_aias\): Delivers AI-powered assistants that handle invoice dispute intake directly from the portal, resolves eligible cases autonomously, and seamlessly escalates to a human agent when needed. In the workspace, it continues to assist human agents by providing relevant insights and actions to accelerate invoice case resolution.

    -   RMA Case Management \(com.sn\_csm\_rma\_case\): Enables customers to create cases for install base item. It offers simplified processes, decreased turnaround time, and a unified workflow.

    [Zurich Patch 4](../quality/zurich-patch-4.md)

    -   Manage Order Operations \(com.sn\_ord\_ops\_aias\): Enables business-to-business \(B2B\) customers to submit order cases autonomously from the Business Portal by simply describing their needs in natural language.


## Browser requirements

Starting with the Zurich release, RMA Case Management for Sales Customer Relationship Management doesn't support mobile devices and Internet Explorer. For more information, see [Browser support](../../administer/navigation-and-ui/reference/browser-support.md).

## Related ServiceNow applications and features

-   **[Now Assist](https://www.servicenow.com/docs/access?context=platform-now-assist-landing&version=zurich&pubname=zurich-intelligent-experiences&ft:locale=en-US)**

    Help improve the productivity and efficiency in your organization, deliver better self-service, recommend actions, provide answers, and empower your users to search more effectively.

-   **[Overview tab in Now Assist Admin](https://www.servicenow.com/docs/access?context=configuring-now-assist&version=zurich&pubname=zurich-intelligent-experiences&ft:locale=en-US)**

    Use the Now Assist Admin console to provide you with quick and effortless access to the important information that you must set up, configure, and monitor Now Assist applications and features.

-   **[Now Assist panel](https://www.servicenow.com/docs/access?context=now-assist-panel-overview&version=zurich&pubname=zurich-intelligent-experiences&ft:locale=en-US)**

    Use this conversational interface in the CSM Configurable Workspace to summarize a chat, a case, or resolution notes so that you can get the context of this information more quickly.

-   **[Now Assist skills](https://www.servicenow.com/docs/access?context=now-assist-skills&version=zurich&pubname=zurich-intelligent-experiences&ft:locale=en-US)**

    Use the Now Assist products to provide agentic AI skills to meet the needs of users in different workflows, including case or incident summarization, chat summarization, resolution notes generation, and code generation.

-   **[Exploring Customer Service Management](https://www.servicenow.com/docs/access?context=exploring-csm&version=zurich&pubname=zurich-customer-service-management&ft:locale=en-US)**

    Learn how the Customer Service Management \(CSM\) application can help your organization resolve customer issues and requests for your customers. By adopting a proactive customer service approach, you can help increase your customer satisfaction and retention.


**Parent Topic:**[Now Assist and agentic AI release notes](../now-assist/now-assist-rn-landing.md)

**Parent Topic:**[Sales Customer Relationship Management release notes](sales-order-management-rn-landing.md)

