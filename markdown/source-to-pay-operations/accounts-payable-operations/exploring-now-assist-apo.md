---
title: Exploring Now Assist for Accounts Payable Operations \(APO\)
description: With the Now Assist for Accounts Payable Operations \(APO\) application, an account payable \(AP\) fulfiller can use generative AI to summarize the details of a case.
locale: en-US
release: australia
product: Accounts Payable Operations
classification: accounts-payable-operations
topic_type: concept
last_updated: "2026-03-12"
reading_time_minutes: 7
breadcrumb: [Now Assist for APO, Accounts Payable Operations, Finance and Supply Chain]
---

# Exploring Now Assist for Accounts Payable Operations \(APO\)

With the Now Assist for Accounts Payable Operations \(APO\) application, an account payable \(AP\) fulfiller can use generative AI to summarize the details of a case.

## Now Assist for APO overview

Using the summarization capability of the Now Assist for APO application, an AP fulfiller can auto-map the invoice lines with purchase order lines, get a concise summary of a case quickly, extract invoice details from email and auto-create an invoice processing case.

Cases can be complex and a case summary may enable an AP fulfiller to provide a more concise summary.

## Skills

![now assist](../image/now-assist.png)

The Now Assist for APO application includes the following:

-   The generative AI skills enable an AP fulfiller to extract the details of an invoice case or inquiry case and suggest resolutions.
-   The generative AI skills perform the purchase order line-mapping and enable an AP fulfiller to review the mapping results.

-   **Purchase order line mapping**

    Provides AP fulfiller to automatically map the invoice lines with the purchase order lines.

    The purchase order line-mapping skill generates the invoice line mapping, changes the invoice line status to review mapping state and provokes the fulfiller to manually review the mapping results. After the fulfiller reviews the mapping results, the invoice line status is changed to mapping complete. The purchase order lines mapped using the Now Assist skill are controlled using the APO properties. For more information on the use of purchase order mapping in workspace, see [Set APO properties](../task/set-apo-properties.md) and [Using Playbook in Accounts Payable Operations](../task/how-to-use-playbook.md).

-   **Invoice case summarization**

    The summary skill reviews the issue, actions completed, status, and next steps. An AP fulfiller can refresh the summary as case updates happen and post the summary to work notes.

    The invoice case summary displays above the activity stream.

    For invoice processing cases, the summary skill also reviews the invoice status and invoice information located in the applicable document.

    For inquiry cases, the invoice case summarization skill generates a case summary by checking the short description, description, and tasks that were created for the case.

    Fulfiller can customize prompt configuration and prompt optimization using the pre-processor in the Now Assist skill kit \(NASK\). The skill supports multiple models such as OpenAI, Claude, Gemini, Now LLM Service. The configured pre-processor is applied across all supported models in NASK. To customize the prompt instructions, the sn\_skill\_builder\_admin role is mandatory.

-   **Invoice data extraction**

    The Invoice data extraction skill helps in extracting invoice details from PDFs submitted through email or supplier portal. The digitized invoice is processed within Accounts Payable Operations automatically. Invoices are extracted in languages \(English, Dutch, French, German, Japanese, Italian, Portuguese, Spanish\) supported by GPT-4o.

    With the Invoice data extraction skill, customers can achieve higher invoice extraction accuracy by leveraging GPT-4o and significantly reducing manual effort. Customers are provided with the flexibility of turning on the manual review of extraction results or can let invoice be processed through the workflow automatically without manual review.

-   **Invoice inquiry solution generator**

    The Invoice inquiry solution generator skill identifies, extracts the invoice inquiry details from the invoice data and related records. Automates the resolution for invoice inquiry cases.

    The skill suggests appropriate resolutions for inquiry cases by analyzing case details such as description, short description, related tasks and knowledge articles.

    Resolve supplier questions use case uses the field extractor skills, which extracts the invoice number and supplier \(from the description and short description\) and updates the case. The inquiry classifier categorizes the case by reading description, short description and updates the subcategory in the case. The Inquiry resolution provider agent automatically provides resolution for the inquiry submitted by suppliers or employees by analyzing the invoice, invoice lines, and other invoice-related tables \(tax, exceptions, approval history tables, purchase order tables, and knowledge base tables\).

    The skill is activated upon assignment of an inquiry case to an AP agent. The skill is used by the Inquiry resolution provider AI agent to generate invoice inquiry case resolution in the Now Assist panel \(Now Assist panel\) reviewed by an agent. The Agent is prompted with an input to close the case in the Now Assist panel. Upon confirmation, the case is closed with the appropriate closure code and closure details. If the agent chooses to respond with a "No", then the Now Assist panel chat window is terminated for manual closure. The resolution is updated in the activity history \(work notes\) of the case. For more information on the AI agent, see [Inquiry resolution provider AI agent](apo-help-resolve-supplier-questions-agentic.md).

-   **Relevant invoice finder**

    The Relevant invoice finder skill identifies the historically processed invoices that are most relevant to a given invoice using semantic matching.

    The skill compares the current invoice and its line descriptions with previously processed invoices along with its line descriptions, and generates a relevance score from 0 through 1 for each item. These invoices are then returned in a ranked list, ordered by relevance.

    The Recommend invoice owner AI agent uses this match score to suggest a [resolution plan](../reference/resolution-plan-scenarios.md#multiple) for Missing or invalid business owner exceptions.

-   **Email response for invoice case**

    The Email response for invoice case skill generates responses for email by analyzing invoice case contexts, activity, work notes, invoice details, approvals, payments, fulfiller's response in the past and knowledge base articles. The skill enables AP specialists and agents to automatically draft and manage responses to invoice-related inquiries. It also leverages the templates in drafting email responses.

    The skill reduces time spent by AP specialists and agents in manually drafting responses and improves productivity.

-   **Email response for invoice task**

    The Email response for invoice task skill generates responses for email by analyzing invoice case contexts, activity, work notes, invoice details, approvals, payments, fulfiller's response in the past and knowledge base articles. The skill enables AP specialists and agents to automatically draft and manage responses to invoice-related inquiries. It also leverages the templates in drafting email responses.

    The skill reduces time spent by AP specialists and agents in manually drafting responses and improves productivity.

-   **Sentiment analysis for invoice case**

    The Sentiment analysis for invoice inquiry case skill enables fulfiller to analyze and prioritize the invoice inquiry cases based on the response tone. The tone is categorized as positive, negative, or neutral. The sentiment score helps fulfiller to understand the urgency and emotional weight of the invoice inquiry case.

-   **Accounts payable document classification**

    The Accounts payable document classification skill automatically identifies and categorizes supplier sent email attachments as invoice, credit memo, and supporting documents. The system supports configurable confidence thresholds and an AI solution with confidence score. Documents are auto-approved if the AI-confidence score is greater than the configured threshold, and auto-approval is enabled in the APO properties page. AP specialist manually reviews the document if the AI confidence score is lesser than the configured threshold. After the documents are successfully categorized, the invoice data extraction skill triggers the extraction of invoices.

    If the email contains more than one invoice or credit memo, the system handles them as follows:

    -   The first invoice is processed using the parent case.
    -   For each additional invoice or credit memo, the system creates a separate invoice processing case. These cases are available under the **Linked Cases** related list on the parent case.
    -   All supporting documents are automatically copied to both the parent case and each linked case, ensuring every case has the context it needs for processing.
    -   **Supporting documents only**: If no invoices or credit memos are found, you can either cancel the case or convert it into an inquiry case.
    This skill accelerates invoice processing and manages substantial volumes of data across various formats, thereby reducing errors, enabling audit transparency, and eliminating manual intervention. The AI solution accurately classifies document types prior to invoice extraction, confirming that non-invoice documents such as contracts and receipts aren’t inadvertently processed as invoices. For more information on configuring the skill, see [Configure Accounts payable document classification skill](../task/config-doc-classification-skill-apo.md).


**Related topics**  


[Invoice Processing use case](docintel-invoice-process-usecase.md)

[Configuring the invoice ingestion flows using Accounts Payable Operations integration with Document Intelligence](config-apo-docintel-integration.md)

[Invoice Case Management](acc-pay-case-mgmt-overview.md)

