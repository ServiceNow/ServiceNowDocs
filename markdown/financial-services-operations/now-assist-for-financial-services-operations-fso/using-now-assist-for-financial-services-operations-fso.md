---
title: Using generative AI in Now Assist for Financial Services Operations \(FSO\)
description: Use generative AI skills to summarize cases and customer profiles with Now Assist for FSO. Customers can also use Disputes intake via Virtual Agent to submit card disputes.
locale: en-US
release: australia
product: Now Assist for Financial Services Operations \(FSO\)
classification: now-assist-for-financial-services-operations-fso
topic_type: concept
last_updated: "2026-03-12"
reading_time_minutes: 6
breadcrumb: [Now Assist for FSO, Financial Services Operations \(FSO\)]
---

# Using generative AI in Now Assist for Financial Services Operations \(FSO\)

Use generative AI skills to summarize cases and customer profiles with Now Assist for FSO. Customers can also use Disputes intake via Virtual Agent to submit card disputes.

## Overview of AI skills in Now Assist for FSO

Now Assist for FSO includes the following skills:

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
</table>-   **Customer profile summarization**

    Provides a customer service representative \(CSR\) with a concise, comprehensive summary of particular customer. It combines customer data, owned products, and recent history to produce an overview for the CSR to better understand a customer's standing with the bank.

    The summary includes the following information:

    -   Owned active products
    -   Recent transactions
    -   Interaction history
    -   Cases
    The generated customer summary displays in the Customer 360 page as part of Agentic Contact Center for Banking.

    This skill is also used in the Interaction page as a dependency for the customer interaction context summary skill. It assists in generating the summarized context for an interaction.

-   **Customer interaction context summary**

    Provides a CSR with a call-contextual customer summary on the Interaction page. This is generated when a call is assigned to a CSR. The summary focuses on the context of the incoming call, providing the CSR with a snapshot of the customer's situation and sentiment when the call begins.

    The summary includes the following information:

    -   Customer profile, with an overview of the customer and a suggestion on the nature of the call
    -   Related cases
    -   Products and services that the customer has
    The generated context summary displays in the Interaction page as part of Agentic Contact Center for Banking.

-   **Disputes intake via Virtual Agent**

    Disputes intake via Virtual Agent enhances the customer experience by performing dispute intake with a chat bot. This can streamline the card dispute submission process for customers, and reduce workloads for live agents.

    The following figure shows the interaction between the Virtual Agent topic, the form data collector application, and Now LLM.

    ![Interaction flow in Disputes intake via Virtual Agent between the Virtual Agent topic, form data collector application, and Now LLM.](../../fso-now-assist/image/disputes-intake-via-va-overview.png)

    -   The Disputes intake via Virtual Agent topic contains the logic of creating a dispute case and filling out the dispute questionnaire based on the conversation. If the answer cannot be determined from the chat responses, it will present a question in a clear and easy-to-understand way to the user. For more information, see [Customize the Virtual Agent topic in Disputes intake via Virtual Agent](../../fso-now-assist/task/customize-report-a-dispute-va-topic.md).
    -   The form data collector takes the table name and view name as an input, and goes through each question on the form. While iterating over the questions, it asks Now LLM if the question is answered based on the chat history. If it is answered, it moves on to the next question. For more information, see [Form Data Collector](../../fso-now-assist/concept/learn-about-the-form-data-collector.md).
    -   Now LLM helps to infer answers from customer responses to proactively fill out fields in the record, and rephrases questions from the dispute questionnaire.
    **Note:** Certain questions will not infer answers from Now LLM to ensure that the correct dispute category and reason code are determined from the conversation. See [Bypassed questions from LLM processing](../../fso-now-assist/concept/learn-about-the-form-data-collector.md#id_fy4_shj_xgc) for more information.


By default, all skills exist in the global domain. When you use Now Assist in a domain-separated environment, users are only able to access data in their domain. For example, if a user uses the summarization skill, Now Assist only uses material that exists in the user's domain when generating that summary. Additionally, there is no co-mingling of data for domain-separated instances when using generative AI skills. The data resides only on the instance, and the shared services used for generative AI do not persist any requests \(prompts\) and responses. For more information, see [Domain separation in the Now Assist Admin console](https://www.servicenow.com/docs/access?context=domain-separation-in-the-now-assist-admin-console&version=australia&pubname=australia-intelligent-experiences&ft:locale=en-US). \(Note that global domain is not the same as global scope. For more information, see [Exploring Next Experience pickers](https://www.servicenow.com/docs/access?context=next-experience-pickers&version=australia&pubname=australia-platform-user-interface&ft:locale=en-US).\)

-   **[Summarize a dispute or claims case with case summarization](../task/summarize-case-using-now-assist-fso.md)**  
Generate a summary from the defined fields on the case record and quickly understand the case context by using the case summarization skill in the Now Assist for Financial Services Operations \(FSO\) application.
-   **[Summarize a customer profile in the Customer 360 page](../../fso-now-assist/task/summarize-customer-profile-fso.md)**  
Use the Customer profile summarization skill to generate an AI-powered overview of a customer's status and information within the Customer 360 page. This feature helps customer service representatives quickly understand a customer's status to provide personalized, real-time support.
-   **[Summarize customer interaction context in the Interaction page](../../fso-now-assist/task/summarize-customer-context-fso.md)**  
The customer interaction context summary skill is used in the Interaction page. It automatically generates a structured summary of customer service interactions, helping banking service representatives quickly understand customer context and interaction history.
-   **[Request generative AI capabilities in Financial Services Operations with Now Assist panel](../task/request-generative-ai-capabilities-in-fso.md)**  
Request the contextual generative AI capabilities, such as a case summary, in the Financial Services Operations \(FSO\) application by using the conversational interface in the Now Assist panel.
-   **[Submit a dispute case with Disputes intake via Virtual Agent](../../fso-now-assist/task/submit-dispute-case-disputes-intake-via-virtual-agent.md)**  
Create a new dispute case using the Disputes intake via Virtual Agent skill in the Now Assist for Financial Services Operations \(FSO\) application. Customers can interact with a Virtual Agent chat, which collects and infers details from customer responses.

**Parent Topic:**[Now Assist for Financial Services Operations \(FSO\)](now-assist-for-financial-services-operations.md)

