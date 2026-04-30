---
title: Now Assist for Source-to-Pay Operations release notes
description: The Now Assist for Source-to-Pay Operations application includes improved AI search, enhanced AI agents, and Summarization skills for fulfillers on the ServiceNow AI Platform. The Now Assist for Source-to-Pay Operations were updated in the Zurich release.
locale: en-US
release: zurich
topic_type: reference
last_updated: "2025-08-22"
reading_time_minutes: 7
---

# Now Assist for Source-to-Pay Operations release notes

The Now Assist for Source-to-Pay Operations application includes improved AI search, enhanced AI agents, and Summarization skills for fulfillers on the ServiceNow AI Platform. The Now Assist for Source-to-Pay Operations were updated in the Zurich release.

## Now Assist for Source-to-Pay Operations highlights for the Zurich release

[Zurich Patch 5](../quality/zurich-patch-5.md)

-   Review changes to Now Assist usage measurement.

[Zurich Patch 4](../quality/zurich-patch-4.md)

-   Some Now Assist skills are now turned on by default.
-   Additional role configuration is required for agentic workflows and AI agents included with Now Assist applications.

Previous Patch releases

-   Some Now Assist skills are now turned on by default.
-   Create purchase requisitions faster by uploading vendor quote files directly through Now Assist's AI-powered chat interface in the Employee Center.
-   Use the improved AI search in Shopping Hub, powered by the Retrieval Augmented Generation \(RAG\) framework, to get more accurate and relevant results.
-   The Help fulfill procurement requests agentic workflow has been renamed to Conversational intake for sourcing and procurement to better reflect its expanded scope and capabilities.
-   Use enhanced AI agents for the Conversational intake for sourcing and procurement agentic workflow in Now Assist for SPO to improve usability and operational efficiency.
-   Use enhanced AI agents for the Coordinate supplier onboarding agentic workflow in Now Assist for SLO to automate the registration of external suppliers and companies and streamlines the onboarding process.
-   Use the Field extractor skill to automate the extraction of invoice number or supplier invoice number from the inquiry case generated through various channels \(emails, virtual agent chats, or web content\). Automating the extraction of invoice and supplier numbers enhances Accounts Payable agents' efficiency, leading to faster and more accurate resolutions.
-   The Enhanced Inquiry resolution provider AI agent uses more data sources to suggest resolution to supplier inquiries.

See [Now Assist for Source-to-Pay Operations](https://www.servicenow.com/docs/access?context=now-assist-source-to-pay-operations&version=zurich&pubname=zurich-source-to-pay-operations&ft:locale=en-US) for more information.

## New in the Zurich release

-   **[Now Assist for FSC Common](https://www.servicenow.com/docs/access?context=now-assist-fsc-common&version=zurich&pubname=zurich-source-to-pay-operations&ft:locale=en-US)**

    The Field Extractor skill extracts the invoice number and supplier invoice number from the inquiry case that is generated through different channels \(emails, virtual agent chats, or web content\). The access control lists \(ACLs\) confirm that only authorized agents can activate or configure the skill.

    The Supplier summarization skill in Source-to-Pay Operations workspace provides unified view of supplier-related inquiries and pending actions. This feature helps specialists and supplier managers to quickly view a concise summary of supplier-related cases, tasks, and exceptions.

    The Inquiry classifier skill auto-populates the subcategory of an invoice inquiry case by analyzing its description and short description in the Accounts Payable Operations.

-   **[Now Assist for Sourcing and Procurement Operations \(SPO\) skills in a Virtual Agent chat](https://www.servicenow.com/docs/access?context=now-assist-spo-va-using&version=zurich&pubname=zurich-source-to-pay-operations&ft:locale=en-US)**

    Requesters can leverage contextual generative AI by using Now Assist for SPO in a Virtual Agent chat to complete self-service tasks, such as purchasing products.

-   **[Now Assist for Sourcing and Procurement Operations \(SPO\)](https://www.servicenow.com/docs/access?context=now-assist-spo&version=zurich&pubname=zurich-source-to-pay-operations&ft:locale=en-US)**

    Upload quotes from vendors to request a purchase using the Procurement product recommendation AI agent. Now Assist automatically extracts supplier information, item descriptions, quantities, and pricing from uploaded vendor quotes to pre-fill purchase requisition forms, eliminating manual data entry and accelerating request submission.

    Long term stable \(LTS\) models are part of Now LLM Service and provide longer model stability windows for regulated industries. These models can integrate with tools to provide governance, monitoring, and compliance controls.

    The Help fulfill procurement requests agentic workflow has been renamed to Conversational intake for sourcing and procurement to better reflect its expanded scope and capabilities.

    Employees can initiate sourcing and procurement requests conversationally, with the agent automatically applying organizational policies, routing logic, and pre-filling request details for faster completion.

    To enhance performance and simplify maintenance, the Conversational intake for sourcing and procurement agentic workflow now includes three core AI agents. The Procurement purchasing plan and Procurement sourcing plan AI agents have been consolidated into a single, unified Procurement product recommendation AI agent.

    -   **Procurement request tracking AI agent**: Finds and summarizes request status details to answer employee inquiries.
    -   **Procurement product recommendation AI agent**: Recommends products based on organizational buying criteria, creates purchasing or sourcing plans, and guides employees through the checkout or request process.
    -   **Procurement inquiry analysis AI agent**: Analyzes employee inquiries to determine next steps, routes tasks to the appropriate agent, provides knowledge-based answers, and manages fallback handling for unsupported requests.
-   **[Now Assist for Supplier Lifecycle Operations \(SLO\)](https://www.servicenow.com/docs/access?context=now-assist-slo&version=zurich&pubname=zurich-source-to-pay-operations&ft:locale=en-US)**

    Now Assist for SLO includes the Coordinate supplier onboarding agentic workflow to streamline the supplier onboarding process by automating supplier registration. AI agents automate the supplier onboarding process by validating profile data and banking details, checking for duplicate suppliers, task generation, communication with suppliers, and final approvals, streamlining the entire process for faster time-to-activation.

    To make the workflow more dynamic, the Supplier document strategy generator AI agent creates tasks by referring to a KB article which has all the details about the regions and industry related tasks and documents required for onboarding. The KB article is available as a part of demo data, however, the admin can edit and configure this KB article as required.

    The following AI agents in the Coordinate supplier onboarding agentic workflow perform the supplier onboarding tasks:

    -   **Supplier data steward AI agent**: Validates supplier data and checks for duplicate records, creates an invitation case for the supplier contact and assigns the necessary supplier tasks. Also, if required, communicates to the supplier about missing information that must be updated.
    -   **Supplier data validator AI agent**: Validates supplier-provided profile information and banking details \(like account name, account ID, and bank name\) in real time.
    -   **Supplier approval AI agent**: Manages approval or rejection of the supplier onboarding.
    -   **Supplier document strategy generator AI agent**: Generates a plan to create tasks after referring to the dedicated KB article which includes all the details about the tasks required for onboarding based on the region and industry.
    For more information, see .

-   **[Now Assist for Accounts Payable Operations \(APO\)](https://www.servicenow.com/docs/access?context=now-assist-apo&version=zurich&pubname=zurich-source-to-pay-operations&ft:locale=en-US)**

    The Now Assist for APO includes Inquiry resolution provider agent and Recommend invoice owner which resolves invoice inquiries autonomously and recommends business owner for invoices \(Non-PO, Non-PO type credit memo\).

    -   The Inquiry resolution provider AI agent processes high volumes of repetitive invoice inquiries through various channels \(web, email, virtual agent, mobile and manual entry\) to significantly reduce the workload of human agents.
    -   The Recommend invoice owner AI agent identifies the missing business owner through semantic matching or by creating tasks. The Recommend invoice owner agent triggers when a Missing or invalid business owner exception is raised. For more information on the AI agents, see [Using AI agents in Now Assist for Accounts Payable Operations](https://www.servicenow.com/docs/access?context=using-apo-ai-agents&version=zurich&pubname=zurich-source-to-pay-operations&ft:locale=en-US)
-   **[New third-party AI model provider options available for all Now Assist applications](https://www.servicenow.com/docs/access?context=exploring-large-language-models&version=zurich&pubname=zurich-intelligent-experiences&ft:locale=en-US)**

    Google Gemini and AWS Claude are available for Now Assist skills and AI agents in addition to Now LLM Service and Azure OpenAI.


## UI changes

-   **Coral theme**

    Coral is now the default theme for new portal, web, and mobile experiences with Next Experience or Core UI enabled. This theme provides a fresh look and feel, featuring brand-neutral illustrations to enhance your user experience. A dark theme option is available for web and mobile experiences.


## Changed features

-   **[Changes to Now Assist usage measurement](https://www.servicenow.com/docs/access?context=monitoring-now-assist-usage&version=zurich&pubname=zurich-platform-administration&ft:locale=en-US)**

    Starting with Zurich Patch 5, Now Assist usage measurement is transitioning from a 365-day look-back model to a 365-day burn-down model, with usage resetting at the contract anniversary date. For more information, refer to [KB KB2704710: Now Assist Usage - Overview &amp; New Measurement Logic](https://support.servicenow.com/kb?id=kb_article_view&sysparm_article=KB2704710).


-   **[Some Now Assist skills are turned on by default](https://www.servicenow.com/docs/access?context=now-assist-skills-on-by-default&version=zurich&pubname=zurich-intelligent-experiences&ft:locale=en-US)**

    The new default behavior works as follows:

    -   New customers: When you install a Now Assist product, designated skills are turned on automatically.
    -   Existing customers who are upgrading \(starting with Zurich Patch 4\): Any previously unconfigured skill is turned on automatically \(the skill was never configured and turned on, then turned off again\). Previously configured skills that were turned on, then off, remain inactive.

## Activation information

Install Now Assist for Source-to-Pay Operations by requesting it from ServiceNow Store. Visit the [ServiceNow Store](https://store.servicenow.com/sn_appstore_store.do#!/store/home) website to view all the available apps and for information about submitting requests to the store. For cumulative release notes information for all released apps, see the [ServiceNow Store version history release notes](https://docs.servicenow.com/bundle/store-release-notes/page/release-notes/store/sn-store-release-notes.html).

**Parent Topic:**[Now Assist and agentic AI release notes](../now-assist/now-assist-rn-landing.md)

**Parent Topic:**[Source-to-Pay Operations release notes](source-to-pay-operations-rn-landing.md)

