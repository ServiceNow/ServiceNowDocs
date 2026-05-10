---
title: Supplier Lifecycle Operations release notes
description: The ServiceNow Supplier Lifecycle Operations application enables you to quickly onboard and collaborate with suppliers, manage supplier relationships, monitor risk, compliance, and performance across the supplier life cycle. Supplier Lifecycle Operations was enhanced and updated in the Australia release.
locale: en-US
release: australia
topic_type: reference
last_updated: "2026-03-12"
reading_time_minutes: 4
---

# Supplier Lifecycle Operations release notes

The ServiceNow® Supplier Lifecycle Operations application enables you to quickly onboard and collaborate with suppliers, manage supplier relationships, monitor risk, compliance, and performance across the supplier life cycle. Supplier Lifecycle Operations was enhanced and updated in the Australia release.

## Supplier Lifecycle Operations highlights for the Australia release

[Australia Patch 1](../quality/australia-patch-1.md)

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


**Important:**

-   The plugin Supplier Operations \(com.snc.sn\_so\) **must** be installed after upgrading to Supplier Lifecycle Operations Australia release. For more information, see [Install Supplier Operations](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/source-to-pay-operations/supplier-lifecycle-operations/install-supplier-ops.md).
-   The Supplier Lifecycle Operations plugin \(com.snc.sn\_supplier\_mgmt\) is renamed to Supplier Case Management. For more information, see [Supplier Case Management](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/source-to-pay-operations/supplier-lifecycle-operations/supplier-case-management.md).
-   Supplier Lifecycle Operations is available in the ServiceNow Store. For details, see the "Activation information" section of these release notes.

## New in the Australia release

-   **[Smart Assessments](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/source-to-pay-operations/supplier-lifecycle-operations/slo-campaign-mgmt.md)**

    Supplier managers can use the segmentation rules and assessment templates to create smart assessments in bulk for users. Smart assessments provide a survey-like experience with enhanced UI capabilities for both internal and external users. This feature utilizes the capabilities of the Smart Assessment Engine application.

-   **[Emails view for supplier managers in the Source-to-Pay Workspace](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/source-to-pay-operations/supplier-lifecycle-operations/enabling-emails-view-for-contacts.md)**

    Supplier managers can access their emails within the Source-to-Pay Workspace from the **Emails** tab in the case, task, and supplier details pages respectively. Email actions are reflected and incomplete email errors are handled. Email-summarization is available from the workspace for tasks and cases only.

    Supplier contacts receive the emails and they can perform the assigned tasks directly via email without logging in to the Supplier Collaboration Portal.

    Internal stakeholders receive the emails and they can perform the assigned tasks directly via email without logging in to the Source-to-Pay Workspace.

-   **[AI driven supplier onboarding using Now Assist for SLO](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/source-to-pay-operations/supplier-lifecycle-operations/supplier-onboarding-agentic-workflow.md)**

    Use theAI driven supplier onboarding workflow to automate data validation, duplicate checking, task generation, and supplier communication. Key enhancements include:

    -   Extract banking information from uploaded documents to reduce information mismatch.
    -   Use the document strategy generator AI agent to generate a customized onboarding task list using all published knowledge base articles.
    -   View a list of AI-suggested suppliers while reviewing supplier onboarding requests initiated through sourcing requests.
    -   Supplier relationship managers can manually approve or reject supplier onboarding requests.
    -   Resolve duplicate supplier onboarding requests from the Now Assist panel by updating the supplier legal name, contact email, or both.
-   **[Automate supplier case creation from emails](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/source-to-pay-operations/supplier-lifecycle-operations/automated-supplier-case-creation-from-emails.md)**

    Convert supplier emails into cases automatically when registered supplier contacts send emails to a supplier inbox. Supplier cases are created for all SLO related queries and assigned to the supplier relationship manager. For queries unrelated to SLO, a universal request is created for resolution.

-   **[Summarize supplier performance in Source-to-Pay Workspace](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/source-to-pay-operations/supplier-lifecycle-operations/summarize-supp-perf.md)**

    Generate comprehensive supplier performance summaries, including performance data, trends, and actionable insights, using the supplier performance summarization skill.

-   **[Analyze sentiments in supplier cases](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/source-to-pay-operations/supplier-lifecycle-operations/slo-analyze-sentiments.md)**

    Use the sentiment analysis skill to analyze supplier case fields and determine the tone or sentiment of the fulfiller.

-   **[Generate an email response for supplier cases](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/source-to-pay-operations/supplier-lifecycle-operations/generate-email-response-for-supplier-case.md)**

    Use the email response skill to analyze the supplier case details and generate professional email response regardless of the record type using past email responses, KB articles, and related tasks.


## Activation information

Install Supplier Lifecycle Operations by requesting it from the ServiceNow Store. Visit the [ServiceNow Store](https://store.servicenow.com/sn_appstore_store.do#!/store/home) to view all the available apps, and for information about submitting requests to the store. For cumulative release notes information for all released apps, see the [ServiceNow Store version history release notes](https://docs.servicenow.com/bundle/store-release-notes/page/release-notes/store/sn-store-release-notes.html).

## Related ServiceNow applications and features

-   **[Now Assist for Supplier Lifecycle Operations \(SLO\)](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/source-to-pay-operations/supplier-lifecycle-operations/now-assist-slo.md)**

    Use the ServiceNow® Now Assist for Supplier Lifecycle Operations \(SLO\) application to guide your supplier managers through a conversation-like experience for their supplier needs.

-   **[Source-to-Pay Workspace](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/source-to-pay-operations/source-to-pay-workspace/source-to-pay-ws-overview.md)**

    Provide experiences and tools to support key activities, such as procuring goods and services, onboarding high-performing suppliers, and processing invoices.


**Parent Topic:**[Source-to-Pay Operations release notes](source-to-pay-operations-rn-landing.md)

