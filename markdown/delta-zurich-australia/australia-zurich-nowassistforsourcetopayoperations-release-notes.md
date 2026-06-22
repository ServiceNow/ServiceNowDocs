---
title: Combined Now Assist for Source-to-Pay Operations release notes for upgrades from Zurich to Australia
description: Consolidated page of all release notes for Now Assist for Source-to-Pay Operations from Zurich to Australia.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/delta-zurich-australia/australia-zurich-nowassistforsourcetopayoperations-release-notes.html
release: australia
topic_type: reference
last_updated: "2026-06-22"
reading_time_minutes: 11
breadcrumb: [Products combined by family]
---

# Combined Now Assist for Source-to-Pay Operations release notes for upgrades from Zurich to Australia

Consolidated page of all release notes for Now Assist for Source-to-Pay Operations from Zurich to Australia.

## How to use this page

To help you prepare for your upgrade, we have combined the cross-family Now Assist for Source-to-Pay Operations release notes onto one page. Read this summary of the new features, changes, and updated information for your product from Zurich to Australia.

**Tip:** If there were no updates for a release notes section in a certain family release, we included a short note for your reference. For example, if a product did not have any updates in Tokyo, the row says "No updates for this release."

## Important information for upgrading Now Assist for Source-to-Pay Operations to Australia

Before you upgrade to Australia, review these pre- and post-upgrade tasks and complete the tasks as needed.

<table class="custom-rows"><thead><tr><th class="filter">

Release

</th><th>

Release notes

</th></tr></thead><tbody><tr><td>

Zurich

</td><td>

No updates for this release.

</td></tr><tr><td>

Australia

</td><td>

No updates for this release.

</td></tr></tbody>
</table>## New features

Between your current release family and Australia, new features were introduced for Now Assist for Source-to-Pay Operations.

<table class="custom-rows"><thead><tr><th class="filter">

Release

</th><th>

Release notes

</th></tr></thead><tbody><tr><td>

Zurich

</td><td>

-   **[Now Assist for FSC Common](https://www.servicenow.com/docs/access?context=now-assist-fsc-common&family=zurich&ft:locale=en-US)**

The Field Extractor skill extracts the invoice number and supplier invoice number from the inquiry case that is generated through different channels \(emails, virtual agent chats, or web content\). The access control lists \(ACLs\) confirm that only authorized agents can activate or configure the skill.

The Supplier summarization skill in Source-to-Pay Operations workspace provides unified view of supplier-related inquiries and pending actions. This feature helps specialists and supplier managers to quickly view a concise summary of supplier-related cases, tasks, and exceptions.

The Inquiry classifier skill auto-populates the subcategory of an invoice inquiry case by analyzing its description and short description in the Accounts Payable Operations.

-   **[Now Assist for Sourcing and Procurement Operations \(SPO\) skills in a Virtual Agent chat](https://www.servicenow.com/docs/access?context=now-assist-spo-va-using&family=zurich&ft:locale=en-US)**

Requesters can leverage contextual generative AI by using Now Assist for SPO in a Virtual Agent chat to complete self-service tasks, such as purchasing products.

-   **[Now Assist Sourcing Procurement Operations](https://www.servicenow.com/docs/access?context=now-assist-spo&family=zurich&ft:locale=en-US)**

Upload quotes from vendors to request a purchase using the Procurement product recommendation AI agent. Now Assist automatically extracts supplier information, item descriptions, quantities, and pricing from uploaded vendor quotes to pre-fill purchase requisition forms, eliminating manual data entry and accelerating request submission.

Long term stable \(LTS\) models are part of Now LLM Service and provide longer model stability windows for regulated industries. These models can integrate with tools to provide governance, monitoring, and compliance controls.

The Help fulfill procurement requests agentic workflow has been renamed to Conversational intake for sourcing and procurement to better reflect its expanded scope and capabilities.

Employees can initiate sourcing and procurement requests conversationally, with the agent automatically applying organizational policies, routing logic, and pre-filling request details for faster completion.

To enhance performance and simplify maintenance, the Conversational intake for sourcing and procurement agentic workflow now includes three core AI agents. The Procurement purchasing plan and Procurement sourcing plan AI agents have been consolidated into a single, unified Procurement product recommendation AI agent.

    -   **Procurement request tracking AI agent**: Finds and summarizes request status details to answer employee inquiries.
    -   **Procurement product recommendation AI agent**: Recommends products based on organizational buying criteria, creates purchasing or sourcing plans, and guides employees through the checkout or request process.
    -   **Procurement inquiry analysis AI agent**: Analyzes employee inquiries to determine next steps, routes tasks to the appropriate agent, provides knowledge-based answers, and manages fallback handling for unsupported requests.
-   **[Now Assist for SLO](https://www.servicenow.com/docs/access?context=now-assist-slo&family=zurich&ft:locale=en-US)**

Now Assist for SLO includes the Coordinate supplier onboarding agentic workflow to streamline the supplier onboarding process by automating supplier registration. AI agents automate the supplier onboarding process by validating profile data and banking details, checking for duplicate suppliers, task generation, communication with suppliers, and final approvals, streamlining the entire process for faster time-to-activation.

To make the workflow more dynamic, the Supplier document strategy generator AI agent creates tasks by referring to a KB article which has all the details about the regions and industry related tasks and documents required for onboarding. The KB article is available as a part of demo data, however, the admin can edit and configure this KB article as required.

The following AI agents in the Coordinate supplier onboarding agentic workflow perform the supplier onboarding tasks:

    -   **Supplier data steward AI agent**: Validates supplier data and checks for duplicate records, creates an invitation case for the supplier contact and assigns the necessary supplier tasks. Also, if required, communicates to the supplier about missing information that must be updated.
    -   **Supplier data validator AI agent**: Validates supplier-provided profile information and banking details \(like account name, account ID, and bank name\) in real time.
    -   **Supplier approval AI agent**: Manages approval or rejection of the supplier onboarding.
    -   **Supplier document strategy generator AI agent**: Generates a plan to create tasks after referring to the dedicated KB article which includes all the details about the tasks required for onboarding based on the region and industry.
For more information, see [\[Placeholder link text to key bundle-stpop.agentic-workflows-na-slo\]](https://www.servicenow.com/docs/access?context=agentic-workflows-na-slo&family=zurich&ft:locale=en-US).

-   **[Now Assist for APO](https://www.servicenow.com/docs/access?context=now-assist-apo&family=zurich&ft:locale=en-US)**

The Now Assist for APO includes Inquiry resolution provider agent and Recommend invoice owner which resolves invoice inquiries autonomously and recommends business owner for invoices \(Non-PO, Non-PO type credit memo\).

    -   The Inquiry resolution provider AI agent processes high volumes of repetitive invoice inquiries through various channels \(web, email, virtual agent, mobile and manual entry\) to significantly reduce the workload of human agents.
    -   The Recommend invoice owner AI agent identifies the missing business owner through semantic matching or by creating tasks. The Recommend invoice owner agent triggers when a Missing or invalid business owner exception is raised. For more information on the AI agents, see [Using AI agents in Now Assist for Accounts Payable Operations](https://www.servicenow.com/docs/access?context=using-apo-ai-agents&family=zurich&ft:locale=en-US)
-   **[New third-party AI model provider options available for all Now Assist applications](https://www.servicenow.com/docs/access?context=exploring-large-language-models&family=zurich&ft:locale=en-US)**

Google Gemini and AWS Claude are available for Now Assist skills and AI agents in addition to Now LLM Service and Azure OpenAI.


</td></tr><tr><td>

Australia

</td><td>

-   **[Now Assist for SPO](https://www.servicenow.com/docs/access?context=now-assist-spo&family=australia&ft:locale=en-US)**

[Analyze sentiment in procurement cases](https://www.servicenow.com/docs/access?context=analyze-sentiments-na-spo&family=australia&ft:locale=en-US)Helps procurement specialists to analyze procurement case fields and live agent chats to determine the tone of the fulfiller.

[Generate email responses](https://www.servicenow.com/docs/access?context=email-response-na-spo&family=australia&ft:locale=en-US)Analyze procurement case, sourcing request, purchase requisition, sourcing event, negotiation, and stretch items like procurement, sourcing, and receipt tasks to generate professional email response. This eliminates the need to manually look up information across multiple records and allows procurement specialists to handle inquiries effectively.

[Upload Statement Work \(SOW\) request](https://www.servicenow.com/docs/access?context=now-assist-spo-upload-sow&family=australia&ft:locale=en-US) Upload SOW documents to submit purchase requests. AI agents parse your documents, extract relevant data, and prepopulate your request, enabling you to focus on reviewing and approving submissions instead of manual data entry.

[Conversational intake sourcing procurement agentic](https://www.servicenow.com/docs/access?context=spo-help-fulfill-pr-agentic&family=australia&ft:locale=en-US) Streamline end‑to‑end procurement workflows with a conversational intake experience powered by AI agent support. AI agents guide you through relevant steps while providing contextual recommendations and real-time progress updates.

[Automatically assign categories](https://www.servicenow.com/docs/access?context=automatically-assign-categories&family=australia&ft:locale=en-US) Automatically classify service requests, purchase requisitions, and purchase orders into the correct spend categories using the spend categorization AI agent.

-   **[Now Assist for SLO](https://www.servicenow.com/docs/access?context=now-assist-slo&family=australia&ft:locale=en-US)**

[AI driven supplier onboarding](https://www.servicenow.com/docs/access?context=supplier-onboarding-agentic-workflow&family=australia&ft:locale=en-US) Use theAI driven supplier onboarding workflow to automate data validation, duplicate checking, task generation, and supplier communication. Key enhancements include:

    -   Extract banking information from uploaded documents to reduce information mismatch.
    -   Use the document strategy generator AI agent to generate a customized onboarding task list using all published knowledge base articles.
    -   View a list of AI-suggested suppliers while reviewing supplier onboarding requests initiated through sourcing requests.
    -   Supplier relationship managers can manually approve or reject supplier onboarding requests.
    -   Resolve duplicate supplier onboarding requests from the Now Assist panel by updating the supplier legal name, contact email, or both.
[Automate supplier case creation from emails](https://www.servicenow.com/docs/access?context=automated-supplier-case-creation-from-emails&family=australia&ft:locale=en-US) Convert supplier emails into cases automatically when registered supplier contacts send emails to a supplier inbox. Supplier cases are created for all SLO related queries and assigned to the supplier relationship manager. For queries unrelated to SLO, a universal request is created for resolution.

[Summarize supplier performance in Source-to-Pay Workspace](https://www.servicenow.com/docs/access?context=summarize-supp-perf&family=australia&ft:locale=en-US) Generate comprehensive supplier performance summaries, including performance data, trends, and actionable insights, using the supplier performance summarization skill.

[Analyze sentiments in supplier cases](https://www.servicenow.com/docs/access?context=slo-analyze-sentiments&family=australia&ft:locale=en-US) Use the sentiment analysis skill to analyze supplier case fields and determine the tone or sentiment of the fulfiller.

[Generate an email response for supplier cases](https://www.servicenow.com/docs/access?context=generate-email-response-for-supplier-case&family=australia&ft:locale=en-US) Use the email response skill to analyze the supplier case details and generate professional email response regardless of the record type using past email responses, KB articles, and related tasks.


-   **[Source-to-Pay Operations common skills](https://www.servicenow.com/docs/access?context=source-to-pay-common-skills&family=australia&ft:locale=en-US)**

The Email response generation skill uses generative AI to automatically draft professional, context-aware email responses for supplier inquiries, procurement communications, and AP case management across Source-to-Pay workflows \(APO, SPO, SLO\), reducing manual effort and improving response consistency.

The Sentiment analysis skill uses large language models to detect emotional tone \(Positive, Negative, or Neutral\) in cases across Source-to-Pay workflows \(APO, SPO, SLO\).

The AI Data Explorer for Source-to-Pay \(APO, SPO, SLO\) supports AI-driven prompt understanding, recommended queries, and drill-down capabilities within a unified interface.


-   **[Now Assist for APO](https://www.servicenow.com/docs/access?context=now-assist-apo&family=australia&ft:locale=en-US)**

Use the accounts payable document classification skill to identify and categorize email attachments, such as invoices, credit memos, and supporting documents, that were sent by suppliers.


-   **[Now Assist for POM](https://www.servicenow.com/docs/access?context=now-assist-for-purch-order-magmt&family=australia&ft:locale=en-US)**

Convert supplier emails into purchase order exceptions automatically when a registered supplier contact sends emails to a supplier inbox. Purchase order exceptions are created for all purchase order queries and assigned to the operational buyer. For queries unrelated to purchase order exceptions, a universal request is created.

Use the define PO exception mitigation strategy agentic workflow in Now Assist for POM to identify and execute mitigation strategies by analyzing delivery gaps and proposing order changes with alternative suppliers.


</td></tr></tbody>
</table>## Changes

Between your current release family and Australia, some changes were made to existing Now Assist for Source-to-Pay Operations features.

<table class="custom-rows"><thead><tr><th class="filter">

Release

</th><th>

Release notes

</th></tr></thead><tbody><tr><td>

Zurich

</td><td>

-   **[Changes to Now Assist usage measurement](https://www.servicenow.com/docs/access?context=monitoring-now-assist-usage&family=zurich&ft:locale=en-US)**




-   ****

</td></tr><tr><td>

Australia

</td><td>

No updates for this release.

</td></tr></tbody>
</table>## Removed

Between your current release family and Australia, some Now Assist for Source-to-Pay Operations features or functionality were removed.

<table class="custom-rows"><thead><tr><th class="filter">

Release

</th><th>

Release notes

</th></tr></thead><tbody><tr><td>

Zurich

</td><td>

No updates for this release.

</td></tr><tr><td>

Australia

</td><td>

No updates for this release.

</td></tr></tbody>
</table>## Deprecations

Between your current release family and Australia, some Now Assist for Source-to-Pay Operations features or functionality were deprecated.

<table class="custom-rows"><thead><tr><th class="filter">

Release

</th><th>

Release notes

</th></tr></thead><tbody><tr><td>

Zurich

</td><td>

No updates for this release.

</td></tr><tr><td>

Australia

</td><td>

No updates for this release.

</td></tr></tbody>
</table>## Activation information

Review information on how to activate Now Assist for Source-to-Pay Operations.

<table class="custom-rows"><thead><tr><th class="filter">

Release

</th><th>

Release notes

</th></tr></thead><tbody><tr><td>

Zurich

</td><td>

Install Now Assist for Source-to-Pay Operations by requesting it from ServiceNow Store. 

</td></tr><tr><td>

Australia

</td><td>

Install for Now Assist for Sourcing and Procurement Operations \(SPO\), Now Assist for Supplier Lifecycle Operations \(SLO\) and Now Assist for Accounts Payable Operations \(APO\), and Now Assist for Purchase Order Management \(POM\) by requesting it from the ServiceNow Store. Visit the [ServiceNow Store](https://store.servicenow.com/sn_appstore_store.do#!/store/home) to view all the available apps, and for information about submitting requests to the store. For cumulative release notes information for all released apps, see the [ServiceNow Store version history release notes](https://www.servicenow.com/docs/access?context=sn-store-release-notes&family=australia&ft:locale=en-US).

</td></tr></tbody>
</table>## Additional requirements

If any additional requirements were introduced or changed for Now Assist for Source-to-Pay Operations we have noted them here.

<table class="custom-rows"><thead><tr><th class="filter">

Release

</th><th>

Release notes

</th></tr></thead><tbody><tr><td>

Zurich

</td><td>

No updates for this release.

</td></tr><tr><td>

Australia

</td><td>

No updates for this release.

</td></tr></tbody>
</table>## Browser requirements

If any specific browser requirements were introduced or changed for Now Assist for Source-to-Pay Operations we have noted them here.

<table class="custom-rows"><thead><tr><th class="filter">

Release

</th><th>

Release notes

</th></tr></thead><tbody><tr><td>

Zurich

</td><td>

No updates for this release.

</td></tr><tr><td>

Australia

</td><td>

No updates for this release.

</td></tr></tbody>
</table>## Accessibility information

Review details on accessibility information for Now Assist for Source-to-Pay Operations, such as specific requirements or compliance levels.

<table class="custom-rows"><thead><tr><th class="filter">

Release

</th><th>

Release notes

</th></tr></thead><tbody><tr><td>

Zurich

</td><td>

No updates for this release.

</td></tr><tr><td>

Australia

</td><td>

No updates for this release.

</td></tr></tbody>
</table>## Localization information

If there are specific localization considerations for Now Assist for Source-to-Pay Operations we have noted them here.

<table class="custom-rows"><thead><tr><th class="filter">

Release

</th><th>

Release notes

</th></tr></thead><tbody><tr><td>

Zurich

</td><td>

No updates for this release.

</td></tr><tr><td>

Australia

</td><td>

No updates for this release.

</td></tr></tbody>
</table>## Highlight information

If there are specific highlight considerations for Now Assist for Source-to-Pay Operations we have noted them here.

<table class="custom-rows"><thead><tr><th class="filter">

Release

</th><th>

Release notes

</th></tr></thead><tbody><tr><td>

Zurich

</td><td>

[Zurich Patch 5](https://www.servicenow.com/docs/access?context=zurich-patch-5&family=zurich&ft:locale=en-US)

-   Review changes to Now Assist usage measurement.

[Zurich Patch 4](https://www.servicenow.com/docs/access?context=zurich-patch-4&family=zurich&ft:locale=en-US)

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

See [Now Assist](https://www.servicenow.com/docs/access?context=now-assist-source-to-pay-operations&family=zurich&ft:locale=en-US) for more information.

</td></tr><tr><td>

Australia

</td><td>

-   Prioritize cases by using the sentiment analysis skill to analyze a fulfiller's tone or sentiment of invoice cases, procurement cases, supplier cases, and tasks.
-   Draft professional email responses automatically for invoice cases, procurement cases, supplier cases, tasks with the email response generation skill.
-   Generate reports, visualizations, and KPIs using natural language queries with the AI data explorer.
-   Enable buyers execute the best mitigation strategies by analyzing delivery gaps and proposing order changes with alternative suppliers.

</td></tr></tbody>
</table>**Parent Topic:**[Products combined by family](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/delta-zurich-australia/rn-combined-intro.md)

