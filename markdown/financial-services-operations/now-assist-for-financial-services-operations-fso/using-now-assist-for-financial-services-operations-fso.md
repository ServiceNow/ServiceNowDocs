---
title: Using generative AI in Now Assist for Financial Services Operations \(FSO\)
description: If you have an agent role, you can summarize the case details with the Now Assist for Financial Services Operations \(FSO\) application. Customers can also use Dispute intake via Virtual Agent to submit card disputes.
locale: en-US
release: zurich
product: Now Assist for Financial Services Operations \(FSO\)
classification: now-assist-for-financial-services-operations-fso
topic_type: concept
last_updated: "2025-07-31"
reading_time_minutes: 2
breadcrumb: [Now Assist for FSO, Financial Services Operations \(FSO\)]
---

# Using generative AI in Now Assist for Financial Services Operations \(FSO\)

If you have an agent role, you can summarize the case details with the Now Assist for Financial Services Operations \(FSO\) application. Customers can also use Dispute intake via Virtual Agent to submit card disputes.

Use the case summarization skill to understand the case context quicker. These summaries are useful for long-running or complex cases.

Dispute intake via Virtual Agent streamlines the card dispute submission process for cardholders by providing a chat interface. Case information is gathered from the customer’s responses, and dispute questionnaire questions are presented to the customer in conversational language.

By default, all skills exist in the global domain. When you use Now Assist in a domain-separated environment, users are only able to access data in their domain. For example, if a user uses the summarization skill, Now Assist only uses material that exists in the user's domain when generating that summary. Additionally, there is no co-mingling of data for domain-separated instances when using generative AI skills. The data resides only on the instance, and the shared services used for generative AI do not persist any requests \(prompts\) and responses. For more information, see [Domain separation in the Now Assist Admin console](https://www.servicenow.com/docs/access?context=domain-separation-in-the-now-assist-admin-console&version=zurich&pubname=zurich-intelligent-experiences&ft:locale=en-US). \(Note that global domain is not the same as global scope. For more information, see [Exploring Next Experience pickers](https://www.servicenow.com/docs/access?context=next-experience-pickers&version=zurich&pubname=zurich-platform-user-interface&ft:locale=en-US).\)

-   **[Summarize a dispute or claims case with case summarization](../task/summarize-case-using-now-assist-fso.md)**  
Generate a summary from the defined fields on the case record and quickly understand the case context by using the case summarization skill in the Now Assist for Financial Services Operations \(FSO\) application.
-   **[Request generative AI capabilities in Financial Services Operations with Now Assist panel](../task/request-generative-ai-capabilities-in-fso.md)**  
Request the contextual generative AI capabilities, such as a case summary, in the Financial Services Operations \(FSO\) application by using the conversational interface in the Now Assist panel.
-   **[Submit a dispute case with Disputes intake via Virtual Agent](../../fso-now-assist/task/submit-dispute-case-disputes-intake-via-virtual-agent.md)**  
Create a new dispute case using the Disputes intake via Virtual Agent skill in the Now Assist for Financial Services Operations \(FSO\) application. Customers can interact with a Virtual Agent chat, which collects and infers details from customer responses.

**Parent Topic:**[Now Assist for Financial Services Operations \(FSO\)](now-assist-for-financial-services-operations.md)

