---
title: Now Assist for Source-to-Pay Operations release notes
description: The ServiceNow Now Assist for Source-to-Pay Operations application includes generative AI skills that can make developing on the ServiceNow AI Platform more efficient. Now Assist for Source-to-Pay Operations was enhanced and updated in the Yokohama release.
locale: en-US
release: yokohama
topic_type: reference
last_updated: "2025-01-30"
reading_time_minutes: 5
---

# Now Assist for Source-to-Pay Operations release notes

The ServiceNow® Now Assist for Source-to-Pay Operations application includes generative AI skills that can make developing on the ServiceNow AI Platform more efficient. Now Assist for Source-to-Pay Operations was enhanced and updated in the Yokohama release.

## Now Assist for Source-to-Pay Operations highlights for the Yokohama release

[Yokohama Patch 11](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/yokohama/markdown/yokohama/release-notes/yokohama-patch-11.md)

-   Review changes to Now Assist usage measurement.
-   Some Now Assist skills, agents, and agentic workflows are on by default.
-   Additional role configuration is required for agentic workflows and AI agents included with Now Assist applications.

Previous Patch releases

-   ServiceNow Otto for Sourcing and Procurement Operations \(SPO\) supports enhanced AI search and the Retrieval-augmented generation \(RAG\) framework to recommend suppliers and products through semantic search and contextual filters, enhancing recommendations with criteria like preferred suppliers and previous purchases.
-   ServiceNow Otto for Supplier Lifecycle Operations \(SLO\) supports a conversational intake that helps suppliers to view and update supply information through a conversational flow.
-   ServiceNow Otto for Accounts Payable Operations \(APO\) supports a conversational intake to complete self-service tasks, such as submit a request or track a request status.

## New in the Yokohama release

-   **[ServiceNow Otto for Sourcing and Procurement Operations \(SPO\)](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/yokohama/markdown/source-to-pay-operations/now-assist-spo.md)**

    ServiceNow Otto for SPO includes an agentic workflow that enhances conversational intake capabilities. This AI-powered agent team streamlines user inquiries to sourcing and procurement teams by gathering knowledge, clarifying requests, deflecting common questions, providing product information, and recommending the appropriate purchase plan. For more information, see [Use agentic workflows in Now Assist for Sourcing and Procurement Operations](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/yokohama/markdown/source-to-pay-operations/agentic-ai-now-assist-spo.md).

    The following new skills are available in Now Assist for SPO:

    -   Negotiation summarization for fulfillers: Summarize negotiations to keep fulfillers informed on their current status, progress, and action items.
    -   Negotiation event summarization for fulfillers: Summarize negotiation events to keep fulfillers informed on their current status, progress, and action items.
    -   Purchase order summarization for requesters: Summarize purchase orders to keep requesters informed about their current status, progress, and action items.
    -   Purchase requisition summarization for requesters: Summarize purchase requisitions to keep requesters informed about their current status, progress, and action items.
    -   Sourcing request summarization for requesters: Summarize sourcing requests to keep requesters informed about their current status, progress, and action items.
-   **[ServiceNow Otto for Supplier Lifecycle Operations \(SLO\)](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/yokohama/markdown/source-to-pay-operations/now-assist-slo.md)**

    ServiceNow Otto for SLO includes an agentic workflow to streamline the supplier onboarding process by automating supplier registration. AI agents automate the supplier onboarding process, including data validation, duplicate checking, task generation, and communication with suppliers, streamlining the entire process for faster time-to-activation. For more information, see .

    The following new skills are available in ServiceNow Otto for SLO:

    -   Conversational intake for suppliers: Suppliers can request profile updates, submit cases, and track inquiry statuses through a conversational interface powered by AI.
    -   Now Assist summarization panel: Case summaries are generated directly within the Now Assist Panel with no need to open individual case records.
    -   Multilingual support for summarization: Case details are summarized in the user's preferred language, improving accessibility for global teams.
-   **[ServiceNow Otto for Accounts Payable Operations \(APO\)](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/yokohama/markdown/source-to-pay-operations/now-assist-apo.md)**

    With the ServiceNow Otto for APO application, AP fulfillers can leverage generative AI capabilities to chat with live agents, submit a request, and track its status.

    The ServiceNow®Now Assist experience brings generative AI powered purchase order line mapping feature designed to enhance matching accuracy and reducing manual intervention.

    Generate purchase order summarization using Now Assist skills powered by generative AI.

    Use agentic workflows in Accounts Payable Operations to resolve invoice inquiry cases raised by employees and suppliers. These workflows also help track associated invoice records efficiently. With an agentic workflow, you can process a high volume of invoice inquiries that come through email attachments to significantly reduce the workload of human agents.

-   **New third-party AI model provider options available for all Now Assist applications**

    Google Gemini and AWS Claude are available for Now Assist skills and AI agents in addition to Now LLM Service and Azure OpenAI.


## UI changes

-   **[Use the ServiceNow Otto for Sourcing and Procurement Operations \(SPO\) skills in a Virtual Agent chat](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/yokohama/markdown/source-to-pay-operations/now-assist-spo-va-using.md)**

    Requesters can leverage contextual generative AI by using ServiceNow Otto for SPO in a Virtual Agent chat to complete self-service tasks, such as purchasing products.


## Changed in this release

-   **Changes to Now Assist usage measurement**

    Starting with Yokohama Patch 5, Now Assist usage measurement is transitioning from a 365-day look-back model to a 365-day burn-down model, with usage resetting at the contract anniversary date. For more information, refer to [KB KB2704710: Now Assist Usage - Overview &amp; New Measurement Logic](https://support.servicenow.com/kb?id=kb_article_view&sysparm_article=KB2704710).

-   **Some Now Assist skills are turned on by default**

    The new default behavior works as follows:

    -   New customers: When you install a Now Assist product, designated skills are turned on automatically.
    -   Existing customers who are upgrading \(starting with Yokohama Patch 11\): Any previously unconfigured skill is turned on automatically \(the skill was never configured and turned on, then turned off again\). Previously configured skills that were turned on, then off, remain inactive.
-   **Configure ACLs for AI agents and agentic workflows**

    Configure the access control lists for who can discover and trigger AI agents and agentic workflows in their guided setups in AI Agent Studio. You can determine whether an AI agent or agentic workflow behaves as a dynamic user or as an AI user. You can also specify if an AI agent or agentic workflow can be available to all authenticated users or publicly available.


## Activation information

Install Now Assist for Source-to-Pay Operations by requesting it from ServiceNow Store. Visit the [ServiceNow Store](https://store.servicenow.com/sn_appstore_store.do#!/store/home) website to view all the available apps and for information about submitting requests to the store. For cumulative release notes information for all released apps, see the [ServiceNow Store version history release notes](https://www.servicenow.com/docs/r/store-release-notes/sn-store-release-notes.html).

**Parent Topic:**[Now Assist and agentic AI release notes](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/yokohama/markdown/yokohama/release-notes/now-assist-rn-landing.md)

**Parent Topic:**[Source-to-Pay Operations release notes](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/yokohama/markdown/yokohama/release-notes/source-to-pay-operations-rn-landing.md)

