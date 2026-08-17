---
title: Exploring ServiceNow Otto for Financial Services Operations \(FSO\)
description: With the ServiceNow Otto for Financial Services Operations \(FSO\) application, use agentic AI to summarize case details, enhance disputes intake with Disputes intake via Virtual Agent, and leverage agentic workflows and AI agents to automate the dispute resolution.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/zurich/financial-services-operations/now-assist-for-financial-services-operations-fso/exploring-now-assist-for-financial-services-operations-fso.html
release: zurich
product: Now Assist for Financial Services Operations \(FSO\)
classification: now-assist-for-financial-services-operations-fso
topic_type: concept
last_updated: "2025-07-31"
reading_time_minutes: 5
keywords: [generative AI for FSO overview, generative AI for financial service operations overview, generative AI for financial service operations sensitive data handling]
breadcrumb: [ServiceNow Otto for FSO, Financial Services Operations \(FSO\)]
---

# Exploring ServiceNow Otto for Financial Services Operations \(FSO\)

With the ServiceNow Otto for Financial Services Operations \(FSO\) application, use agentic AI to summarize case details, enhance disputes intake with Disputes intake via Virtual Agent, and leverage agentic workflows and AI agents to automate the dispute resolution.

## Overview of ServiceNow Otto for Financial Services Operations \(FSO\)

The following AI capabilities are available:

-   Summarize the details of a case for an insurance claim or a card dispute.
-   Use a Virtual Agent chatbot as part of the customer dispute intake flow. Card network and issuer policies are integrated in the chatbot conversation. Information on the dispute is gathered and inferred from the customer's responses and populated in case form fields.
-   Use agentic AI to assist dispute agents in handling transactions that are flagged as friendly fraud. The AI agent leverages the results from a friendly fraud detection tool to generate recommendations the appropriate action. If the transaction is rejected, it also helps draft a rationale to explain the decision to the end user.

## Skills

The ServiceNow Otto for Financial Services Operations \(FSO\) includes the following skills.

-   **Case summarization**

    Provides an agent with a summary of an insurance claim case or card dispute case, including the issue and the actions taken. An agent can generate a summary of a case to understand the case context. They can refresh the summary so that it includes the latest updates to the case, and post the summary to the case work notes.

    The generated case summary displays in the following areas:

    -   Insurance: Next to the claim details panel in the claim summary page, claim workspace, and claim details page
    -   Banking: Between the activities and case information panel
    The summary includes the information that the agent enters in the case record fields that are listed in the following table.

<table id="table_mgm_bw3_mbc"><thead><tr><th>

Industry

</th><th>

Skill description

</th><th>

Record fields

</th></tr></thead><tbody><tr><td>

Insurance

</td><td>

Provides a customized skill that is configured with a series of related tables for claims cases. The directions address a wide range of claims cases for all lines of business. Summarization is available at the base case level.

</td><td>

-   Incident description
-   Incident location
-   Incident date
-   Nature of loss
-   Stage
-   Assigned to
-   Insurance policy
-   Total claim amount


</td></tr><tr><td>

Banking

</td><td>

Provides a customized skill that is configured with a series of related tables for card dispute cases. The directions cover a range of card dispute cases across various categories.

</td><td>

-   Short description
-   Created
-   Assigned to
-   Stage
-   Dispute amount
-   Card network
-   Category
-   Reason code
-   Consumer
-   Account
-   Service
-   Product


</td></tr></tbody>
</table>-   **Disputes intake via Virtual Agent**

    Disputes intake via Virtual Agent enhances the customer experience by performing dispute intake with a chat bot. This can streamline the card dispute submission process for customers, and reduce workloads for live agents.

    The following figure shows the interaction between the Virtual Agent topic, the form data collector application, and Now LLM.

    \[Omitted image "disputes-intake-via-va-overview.png"\] Alt text: Interaction flow in Disputes intake via Virtual Agent between the Virtual Agent topic, form data collector application, and Now LLM.

    -   The Disputes intake via Virtual Agent topic contains the logic of creating a dispute case and filling out the dispute questionnaire based on the conversation. If the answer cannot be determined from the chat responses, it will present a question in a clear and easy-to-understand way to the user. For more information, see [Customize the Virtual Agent topic in Disputes intake via Virtual Agent](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/financial-services-operations/now-assist-for-financial-services-operations-fso/customize-report-a-dispute-va-topic.md).
    -   The form data collector takes the table name and view name as an input, and goes through each question on the form. While iterating over the questions, it asks Now LLM if the question is answered based on the chat history. If it is answered, it moves on to the next question. For more information, see [Form Data Collector](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/financial-services-operations/now-assist-for-financial-services-operations-fso/learn-about-the-form-data-collector.md).
    -   Now LLM helps to infer answers from customer responses to proactively fill out fields in the record, and rephrases questions from the dispute questionnaire.
    **Note:** Certain questions will not infer answers from Now LLM to ensure that the correct dispute category and reason code are determined from the conversation. See [Bypassed questions from LLM processing](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/financial-services-operations/now-assist-for-financial-services-operations-fso/learn-about-the-form-data-collector.md) for more information.


## ServiceNow Otto panel in Financial Services Workspace

For case summarization or a conversational interaction for dispute resolution, an agent can use the ServiceNow Otto panel in Financial Services Workspace. This enables an agent to request a case summary in a conversational interface. For more information, see .

## Sensitive data handling

Personally identifiable information and other sensitive data can be masked so that it doesn't appear in generative AI prompts. Placeholder text is sent with the prompt instead, and that placeholder text is replaced with the original text after the response has been received. This two-way masking ensures that your users see the correct values, but the Now LLM Service isn't exposed to any sensitive information. For more information, see .

**Important:** Exercise caution when using ServiceNow Otto for FSO with cases that contain sensitive data or other regulated workloads, such as healthcare claims. ServiceNow Otto for FSO should not be used for processing protected health information \(PHI\). When using ServiceNow Otto for FSO in a protected industry, validate and test the generated results in accordance with corresponding legislation and requirements. See [AI limitations](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/financial-services-operations/now-assist-for-financial-services-operations-fso/now-assist-for-financial-services-operations.md) for more information.

