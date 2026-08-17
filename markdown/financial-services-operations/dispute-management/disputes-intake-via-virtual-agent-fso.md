---
title: Disputes intake via Virtual Agent
description: Disputes intake via Virtual Agent is an AI skill that uses a chat bot to collect card dispute information from customers. This streamlines the submission process and reduces workloads for live agents by using AI to infer answers and fill out dispute forms automatically.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/financial-services-operations/dispute-management/disputes-intake-via-virtual-agent-fso.html
release: australia
product: Dispute Management
classification: dispute-management
topic_type: concept
last_updated: "2026-07-01"
reading_time_minutes: 4
breadcrumb: [Intake, Use, Dispute Management, Banking applications, Financial Services Operations \(FSO\)]
---

# Disputes intake via Virtual Agent

Disputes intake via Virtual Agent is an AI skill that uses a chat bot to collect card dispute information from customers. This streamlines the submission process and reduces workloads for live agents by using AI to infer answers and fill out dispute forms automatically.

## Workflow

The following figure shows an example interaction between the Virtual Agent topic, the form data collector application, and Now LLM.

\[Omitted image "disputes-intake-via-va-overview.png"\] Alt text: Interaction flow in Disputes intake via Virtual Agent between the Virtual Agent topic, form data collector application, and Now LLM.

-   The Disputes intake via Virtual Agent topic contains the logic of creating a dispute case and filling out the dispute questionnaire based on the conversation. If the answer cannot be determined from the chat responses, it will present a question in a clear and easy-to-understand way to the user. For more information, see [Customize the Virtual Agent topic in Disputes intake via Virtual Agent](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/financial-services-operations/dispute-management/customize-report-a-dispute-va-topic.md).
-   The form data collector takes the table name and view name as an input, and goes through each question on the form. While iterating over the questions, it asks the large language model \(LLM\) if the question is answered based on the chat history. If it is answered, it moves on to the next question. For more information, see [Form Data Collector](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/financial-services-operations/dispute-management/learn-about-the-form-data-collector.md).
-   The LLM helps to infer answers from customer responses to proactively fill out fields in the record, and rephrases questions from the dispute questionnaire.

**Note:** Certain questions will not infer answers from Now LLM to ensure that the correct dispute category and reason code are determined from the conversation. See [Bypassed questions from LLM processing](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/financial-services-operations/dispute-management/learn-about-the-form-data-collector.md) for more information.

-   **[Submit a dispute case with Disputes intake via Virtual Agent](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/financial-services-operations/dispute-management/submit-dispute-case-disputes-intake-via-virtual-agent.md)**  
Create a new dispute case using the Disputes intake via Virtual Agent skill in the ServiceNow Otto for Financial Services Operations \(FSO\) application. Customers can interact with a Virtual Agent chat, which collects and infers details from customer responses.
-   **[Resume a Disputes intake via Virtual Agent dispute case as an agent](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/financial-services-operations/dispute-management/resume-dispute-case-from-disputes-intake-via-virtual-agent.md)**  
As an agent, you can resume a card dispute case when a customer leaves a Virtual Agent chat in Disputes intake via Virtual Agent without submitting the dispute. Pick up where the customer left off and complete the details of the dispute case.
-   **[Resume a Disputes intake via Virtual Agent dispute case as a customer](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/financial-services-operations/dispute-management/resume-virtual-agent-dispute-case-as-customer.md)**  
Learn how a customer can resume a card dispute case in Disputes intake via Virtual Agent when they close a Virtual Agent chat before submitting the case.
-   **[Form Data Collector](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/financial-services-operations/dispute-management/learn-about-the-form-data-collector.md)**  
Learn about the Form Data Collector. This application is used to assist with populating case form fields during a customer's interaction with a Virtual Agent chatbot.

**Parent Topic:**[About dispute intake](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/financial-services-operations/dispute-management/dispute-intake-overview.md)

**Related topics**  


[Configure Disputes intake via Virtual Agent in ServiceNow Otto for Financial Services Operations \(FSO\)](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/financial-services-operations/dispute-management/configuring-disputes-intake-via-virtual-agent.md)

[Customize the Virtual Agent topic in Disputes intake via Virtual Agent](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/financial-services-operations/dispute-management/customize-report-a-dispute-va-topic.md)

[Submit a dispute case with Disputes intake via Virtual Agent](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/financial-services-operations/dispute-management/submit-dispute-case-disputes-intake-via-virtual-agent.md)

[Resume a Disputes intake via Virtual Agent dispute case as an agent](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/financial-services-operations/dispute-management/resume-dispute-case-from-disputes-intake-via-virtual-agent.md)

[Resume a Disputes intake via Virtual Agent dispute case as a customer](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/financial-services-operations/dispute-management/resume-virtual-agent-dispute-case-as-customer.md)

[Form Data Collector](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/financial-services-operations/dispute-management/learn-about-the-form-data-collector.md)

