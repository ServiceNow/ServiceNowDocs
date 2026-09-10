---
title: Supplier Lifecycle Operations release notes
description: The ServiceNow Supplier Lifecycle Operations application enables you to quickly onboard and collaborate with suppliers, manage supplier relationships, monitor risk, compliance, and performance across the supplier life cycle. Supplier Lifecycle Operations was enhanced and updated in the Australia release.The Australia September 2026 release introduces FedEx Dataworks integration to enable relationship managers assess supplier risk during onboarding, and benchmark supplier performance — without leaving the supplier workspace.The ServiceNow Supplier Lifecycle Operations application enables you to quickly onboard and collaborate with suppliers, manage supplier relationships, monitor risk, compliance, and performance across the supplier life cycle. Supplier Lifecycle Operations was enhanced and updated in the Australia release.
locale: en-US
release: australia
topic_type: topic
last_updated: "2026-03-12"
reading_time_minutes: 7
---

# Supplier Lifecycle Operations release notes

The ServiceNow® Supplier Lifecycle Operations application enables you to quickly onboard and collaborate with suppliers, manage supplier relationships, monitor risk, compliance, and performance across the supplier life cycle. Supplier Lifecycle Operations was enhanced and updated in the Australia release.

## About Supplier Lifecycle Operations

Now Assist introduced AI on the platform. As that experience has evolved, there's a new name for the experience. ServiceNow Otto® is the conversational AI platform integrated into ServiceNow workflows. It provides agentic capabilities, supports multimodal interactions across web, mobile, and messaging channels, and enables autonomous orchestration for cross-system workflows.

-   **[ServiceNow product tiers](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/intelligent-experiences/ai-native-sku-overview.md)**

    The ServiceNow AI Platform now brings you a new AI experience with three licensing tiers available:

    -   Foundation: AI basics to deliver insights
    -   Advanced: AI to boost productivity across relevant use cases
    -   Prime: Act autonomously with all AI assets, and create your own
    Depending on your license, you will have access to certain application features, generative AI skills, agentic workflows, and AI agents.


Australia Early Availability

-   Enable supplier managers and admins to create and manage smart assessments in bulk for internal and external users.
-   Enhance email interactions for supplier managers by creating a centralized email view displaying all emails within the Source-to-Pay workspace at case, task, and supplier levels.
-   Improved action plans with Gantt chart visualizations, email notifications, messaging, and activity streams.
-   Automate the monitoring and follow-up of the expiring supplier documents. As documents approach expiration, supplier tasks are automatically generated in the supplier portal or workspace, requesting the document owner to submit updated documentation. After document expiry also, automatic tasks are created in place of follow-ups via email reminders and supplier cases.
-   Enable supplier contacts to upload documents from the portal even if the supplier document configuration isn’t done.

    **Note:** This facility is already enabled for supplier managers in the previous releases. They can upload documents from the workspace even if the supplier document configuration isn’t done.


## Activation and other requirements

**Important:**

-   The plugin Supplier Operations \(com.snc.sn\_so\) **must** be installed after upgrading to Supplier Lifecycle Operations Australia release. For more information, see [Install Supplier Operations](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/source-to-pay-operations/install-supplier-ops.md).
-   The Supplier Lifecycle Operations plugin \(com.snc.sn\_supplier\_mgmt\) is renamed to Supplier Case Management. For more information, see [Supplier Case Management](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/source-to-pay-operations/supplier-case-management.md).
-   Supplier Lifecycle Operations is available in the ServiceNow Store. For details, see the "Activation information" section of these release notes.

-   **Activation information**

    Install Supplier Lifecycle Operations by requesting it from the ServiceNow Store. Visit the [ServiceNow Store](https://store.servicenow.com/sn_appstore_store.do#!/store/home) to view all the available apps, and for information about submitting requests to the store. For cumulative release notes information for all released apps, see the [ServiceNow Store version history release notes](https://www.servicenow.com/docs/r/store-release-notes/sn-store-release-notes.html).


**Parent Topic:**[Source-to-Pay Operations release notes](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/release-notes/source-to-pay-operations-rn-landing.md)

## September 2026

The Australia September 2026 release introduces FedEx Dataworks integration to enable relationship managers assess supplier risk during onboarding, and benchmark supplier performance — without leaving the supplier workspace.

### What's new

-   ****

    FedEx Dataworks combines unmatched, proprietary real-world data signals with advanced analytics to power ServiceNow's Source-to-Pay workflows. Relationship managers can use these signals during supplier onboarding to validate suppliers, evaluate risk, and benchmark supplier performance — without leaving the supplier workspace.

    The FedEx Dataworks integration includes the following features:

    -   **Supplier validation in supplier onboarding Registration stage**: Verifies a supplier's details against FedEx Dataworks records to establish a FedEx Dataworks Supplier ID. This step is part of the supplier onboarding playbook and is required before risk assessment or performance benchmarking data can be retrieved.
    -   **FedEx Dataworks risk assessment in supplier onboarding Qualification stage**: Returns risk factor ratings for a matched supplier, covering customs risk, restricted country screening, and dangerous goods risk. Risk assessment is available in the supplier onboarding playbook after a successful supplier match.
    -   **Supplier performance benchmarking**: Retrieves FedEx Dataworks logistics performance metrics for a matched supplier, displayed in a dedicated section on the supplier profile page.
-   ****

    The AI L1 SLO Service Desk Specialist is a fully autonomous help desk automation solution that resolves supplier inquiries without manual intervention from a fulfiller.

    For general inquiry cases, the AI L1 SLO Service Desk Specialist retrieves relevant information from published knowledge base articles and the FSC Common KG Tags added under the Enterprise knowledge graph to investigate the issue.

-   **[Generate a knowledge article from a closed supplier case](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/source-to-pay-operations/generate-article-case.md)**

    Generate, review, and publish knowledge articles from closed supplier cases using ServiceNow Otto for SLO.

-   **[Generate a knowledge article from multiple closed cases](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/source-to-pay-operations/generate-article-multiple-cases.md)**

    Generate, review, and publish a knowledge article from multiple closed supplier cases using ServiceNow Otto for SLO.

-   **[Verify tax information change request using Relish](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/source-to-pay-operations/validate-tax-information.md)**

    Relish is a third-party supplier intelligence platform that validates supplier data while working on supplier cases.

    When a tax information change request is assigned to a supplier manager and they start working on it, they can verify the tax details using Relish.

-   **[View supplier sanction status using Relish](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/source-to-pay-operations/view-supplier-sanction-status.md)**

    Supplier managers can view the sanction status and last sanction check date for suppliers from the Manage Suppliers list.

    These fields in the supplier list are available regardless of whether Relish is installed or not, but are updated only when Relish is integrated. If Relish is not integrated, users can edit the field manually if they want.


### What's changed

-   **[Verify bank account ownership using Relish](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/source-to-pay-operations/verify-banking-information.md)**

    When a banking details change request is assigned to a supplier manager and they start working on it, they can verify the details using Relish.

    By default, bank validation checks only the bank routing number and address details. Relish also verifies the bank account number and account ownership information when bank account ownership validation is enabled.

-   **[Conduct bulk sanction screening using Relish](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/source-to-pay-operations/perform-bulk-sanction-screening.md)**

    When a sanction screening request for compliance verification is assigned to a supplier manager and they start working on it, they can verify the details using Relish.

    Supplier managers can conduct sanction screening for multiple suppliers simultaneously using the bulk sanction screening feature.

-   **[AI driven supplier onboarding using ServiceNow Otto for SLO](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/source-to-pay-operations/supplier-onboarding-agentic-workflow.md)**
    -   Leverages Web search results to generate a supplier scorecard highlighting key strengths, positive indicators, and potential risk signals.
    -   If Craft is configured, the workflow leverages the Craft integration to generate a comprehensive, normalized supplier scorecard and risk assessment. It provides a structured evaluation of the supplier’s overall profile and associated risk factors.
    -   If Relish is integrated, the supplier's banking information is further validated and synchronized with Relish.

### What's deprecated or removed

-   **Now LLM Service**

    Starting with the September 2026 release, Now LLM Service is being prepared for future deprecation. The Now LLM Service is no longer the default model provider for new or inactive AI assets, and it is no longer selected by default in AI Control Tower. A third-party LLM is now selected by default for AI assets, while existing configurations using the Now LLM Service continue unchanged. The Now LLM Service is still available for manual selection. For details, see the [Deprecation Process \[KB0867184\]](https://support.servicenow.com/kb_view.do?sysparm_article=KB0867184) article in the Now Support Knowledge Base.


## Australia Early Availability

The ServiceNow® Supplier Lifecycle Operations application enables you to quickly onboard and collaborate with suppliers, manage supplier relationships, monitor risk, compliance, and performance across the supplier life cycle. Supplier Lifecycle Operations was enhanced and updated in the Australia release.

### What's new

-   **[Smart Assessments](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/source-to-pay-operations/slo-campaign-mgmt.md)**

    Supplier managers can use the segmentation rules and assessment templates to create smart assessments in bulk for users. Smart assessments provide a survey-like experience with enhanced UI capabilities for both internal and external users. This feature utilizes the capabilities of the Smart Assessment Engine application.

-   **[Emails view for supplier managers in the Source-to-Pay Workspace](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/source-to-pay-operations/enabling-emails-view-for-contacts.md)**

    Supplier managers can access their emails within the Source-to-Pay Workspace from the **Emails** tab in the case, task, and supplier details pages respectively. Email actions are reflected and incomplete email errors are handled. Email-summarization is available from the workspace for tasks and cases only.

    Supplier contacts receive the emails and they can perform the assigned tasks directly via email without logging in to the Supplier Collaboration Portal.

    Internal stakeholders receive the emails and they can perform the assigned tasks directly via email without logging in to the Source-to-Pay Workspace.

-   **[AI driven supplier onboarding using ServiceNow Otto for SLO](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/source-to-pay-operations/supplier-onboarding-agentic-workflow.md)**

    Use theAI driven supplier onboarding workflow to automate data validation, duplicate checking, task generation, and supplier communication. Key enhancements include:

    -   Extract banking information from uploaded documents to reduce information mismatch.
    -   Use the document strategy generator AI agent to generate a customized onboarding task list using all published knowledge base articles.
    -   View a list of AI-suggested suppliers while reviewing supplier onboarding requests initiated through sourcing requests.
    -   Supplier relationship managers can manually approve or reject supplier onboarding requests.
    -   Resolve duplicate supplier onboarding requests from the Now Assist panel by updating the supplier legal name, contact email, or both.
-   **[Automate supplier case creation from emails](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/source-to-pay-operations/automated-supplier-case-creation-from-emails.md)**

    Convert supplier emails into cases automatically when registered supplier contacts send emails to a supplier inbox. Supplier cases are created for all SLO related queries and assigned to the supplier relationship manager. For queries unrelated to SLO, a universal request is created for resolution.

-   **[Summarize supplier performance in Source-to-Pay Workspace](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/source-to-pay-operations/summarize-supp-perf.md)**

    Generate comprehensive supplier performance summaries, including performance data, trends, and actionable insights, using the supplier performance summarization skill.

-   **[Analyze sentiments in supplier cases](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/source-to-pay-operations/slo-analyze-sentiments.md)**

    Use the sentiment analysis skill to analyze supplier case fields and determine the tone or sentiment of the fulfiller.

-   **[Generate an email response for supplier cases](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/source-to-pay-operations/generate-email-response-for-supplier-case.md)**

    Use the email response skill to analyze the supplier case details and generate professional email response regardless of the record type using past email responses, KB articles, and related tasks.


