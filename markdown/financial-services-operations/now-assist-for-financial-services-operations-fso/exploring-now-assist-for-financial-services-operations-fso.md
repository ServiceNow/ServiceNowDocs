---
title: Exploring Now Assist for Financial Services Operations \(FSO\)
description: With the Now Assist for Financial Services Operations \(FSO\) application, use agentic AI to summarize case details, enhance disputes intake with Disputes intake via Virtual Agent, and leverage agentic workflows.
locale: en-US
release: yokohama
product: Now Assist for Financial Services Operations \(FSO\)
classification: now-assist-for-financial-services-operations-fso
topic_type: concept
last_updated: "2025-01-30"
reading_time_minutes: 5
keywords: [generative AI for FSO overview, generative AI for financial service operations overview, generative AI for financial service operations sensitive data handling]
breadcrumb: [Now Assist for Financial Services Operations \(FSO\)]
---

# Exploring Now Assist for Financial Services Operations \(FSO\)

With the Now Assist for Financial Services Operations \(FSO\) application, use agentic AI to summarize case details, enhance disputes intake with Disputes intake via Virtual Agent, and leverage agentic workflows.

## Now Assist for Financial Services Operations \(FSO\) overview

The following AI capabilities are available:

-   Summarize the details of a case for an insurance claim or a card dispute.
-   Use a Virtual Agent chatbot as part of the customer dispute intake flow. Card network and issuer policies are integrated in the chatbot conversation. Information on the dispute is gathered and inferred from the customer's responses and populated in case form fields.
-   Use agentic AI to assist dispute agents in handling transactions that are flagged as friendly fraud. The AI agent leverages the results from a friendly fraud detection tool to generate recommendations the appropriate action. If the transaction is rejected, it also helps draft a rationale to explain the decision to the end user.

## Skills

The Now Assist for Financial Services Operations \(FSO\) application includes the following skills:

-   **Case summarization**

    Provides an agent with a summary of an insurance claim case or card dispute case, including the issue and the actions taken. An agent can generate a summary of a case to understand the case context. They can refresh the summary so that it includes the latest updates to the case, and post the summary to the case work notes.

    The generated case summary is displayed in the following areas:

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

    Enhances the customer experience by performing dispute intake with a chatbot.

    The following figure shows the interaction between the Virtual Agent topic, the form data collector application, and the Now LLM Service.

    ![Interaction flow in Disputes intake via Virtual Agent between the Virtual Agent topic, form data collector application, and Now LLM Service.](../../fso-now-assist/image/disputes-intake-via-va-overview.png "Dispute intake workflow with an agent")

    -   The Disputes intake via Virtual Agent topic contains the logic of creating a dispute case and filling out the dispute questionnaire based on the conversation. If the answer can’t be determined from the chat responses, it will present the next question in the questionnaire to the user in plain language. For more information, see [Customize the Virtual Agent topic in Disputes intake via Virtual Agent](../../fso-now-assist/task/customize-report-a-dispute-va-topic.md).
    -   The form data collector takes the table name and view name as an input, and goes through each question on the form. While iterating over the questions, it asks the Now LLM Service if the question is answered based on the chat history. If it’s answered, it moves on to the next question. For more information, see [Form Data Collector](../../fso-now-assist/concept/learn-about-the-form-data-collector.md).
    -   The Now LLM Service helps to infer answers from customer responses, and rephrases questions from the dispute questionnaire.

## Now Assist panel in Financial Services Workspace

The Now Assist panel in the Financial Services Workspace provides a conversational interface for agents to request case summariesand review AI-driven recommendations for agentic workflows, such as friendly fraud.

By using the Now Assist panel, agents can aid in decision-making and case handling. For more information about the Now Assist panel, see [Now Assist panel](https://www.servicenow.com/docs/access?context=now-assist-panel-overview&version=yokohama&pubname=yokohama-intelligent-experiences&ft:locale=en-US).

## Sensitive data handling

Personally identifiable information and other sensitive data can be masked so that it doesn't appear in agentic AI prompts. Placeholder text is sent with the prompt instead, and that placeholder text is replaced with the original text after the response has been received. This two-way masking helps ensure that your users see the correct values, but the Now LLM Service isn't exposed to any sensitive information. For more information, see .

**Important:** Exercise caution when using Now Assist for FSO with cases that contain sensitive data or other regulated workloads, such as healthcare claims. Now Assist for FSO shouldn’t be used for processing protected health information \(PHI\). When using Now Assist for FSO in a protected industry, validate and test the generated results in accordance with corresponding legislation and requirements. See [AI limitations](now-assist-for-financial-services-operations.md#id_jvg_1wv_lbc) for more information.

-   **[Form Data Collector](../../fso-now-assist/concept/learn-about-the-form-data-collector.md)**  
Learn about the Form Data Collector application that is used to assist with populating case form fields during a customer's interaction with a Virtual Agent chatbot.

**Parent Topic:**[Now Assist for Financial Services Operations \(FSO\)](now-assist-for-financial-services-operations.md)

