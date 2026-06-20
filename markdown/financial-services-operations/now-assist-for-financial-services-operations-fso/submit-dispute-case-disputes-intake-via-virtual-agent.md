---
title: Submit a dispute case with Disputes intake via Virtual Agent
description: Create a new dispute case using the Disputes intake via Virtual Agent skill in the Now Assist for Financial Services Operations \(FSO\) application. Customers can interact with a Virtual Agent chat, which collects and infers details from customer responses.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/yokohama/financial-services-operations/now-assist-for-financial-services-operations-fso/submit-dispute-case-disputes-intake-via-virtual-agent.html
release: yokohama
product: Now Assist for Financial Services Operations \(FSO\)
classification: now-assist-for-financial-services-operations-fso
topic_type: task
last_updated: "2025-01-30"
reading_time_minutes: 2
breadcrumb: [Using generative AI, Now Assist for Financial Services Operations \(FSO\)]
---

# Submit a dispute case with Disputes intake via Virtual Agent

Create a new dispute case using the Disputes intake via Virtual Agent skill in the Now Assist for Financial Services Operations \(FSO\) application. Customers can interact with a Virtual Agent chat, which collects and infers details from customer responses.

## Before you begin

Role required: none

## Procedure

1.  Initiate a chat with Disputes intake via Virtual Agent by selecting the chat bubble.

2.  In the chat window, select **Show all my options**.

    \[Omitted image "disputes-va-show-options.png"\] Alt text: Select Show all my options when the chat window appears.

3.  In the topics list, select **Report a dispute**.

    \[Omitted image "disputes-va-report-dispute.png"\] Alt text: In the topics list, select Report a dispute.

    A new dispute case is created to capture the customer's responses.

4.  The Virtual Agent asks questions to the user to determine the dispute type, and the subsequent questions from the disputes questionnaire for this particular type of dispute.

    \[Omitted image "disputes-va-customer-input.png"\] Alt text: Disputes intake via Virtual Agent will prompt the customer for information, and the customer enters the information with text responses or by selecting options. \[Omitted image "disputes-va-select-txn.png"\] Alt text: The customer may also respond to questions by selecting options presented by Disputes intake via Virtual Agent.

    Disputes intake via Virtual Agent rephrases questions from the dispute questionnaire in a conversational format.

    The dispute case is populated with information from the user's responses. Disputes intake via Virtual Agent infers information from responses to populate other fields as necessary.

5.  When presented with the dispute submission disclaimer, select **Yes** to agree.

    If **No** is selected more than once, the user is redirected to a live agent.


## Result

Disputes intake via Virtual Agent creates a Card Disputes Service Case and presents the customer with a reference link.

\[Omitted image "disputes-va-complete.png"\] Alt text: The customer is presented with a case number at the end of the dispute submission process.

A card dispute processor may access the record and review its details in the workspace.

-   **[Resume a Disputes intake via Virtual Agent dispute case as an agent](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/yokohama/markdown/yokohama/financial-services-operations/now-assist-for-financial-services-operations-fso/resume-dispute-case-from-disputes-intake-via-virtual-agent.md)**  
As an agent, you can resume a card dispute case when a customer leaves a Virtual Agent chat in Disputes intake via Virtual Agent without submitting the dispute. Pick up where the customer left off and complete the details of the dispute case.
-   **[Resume a Disputes intake via Virtual Agent dispute case as a customer](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/yokohama/markdown/yokohama/financial-services-operations/now-assist-for-financial-services-operations-fso/resume-virtual-agent-dispute-case-as-customer.md)**  
Learn how a customer can resume a card dispute case in Disputes intake via Virtual Agent when they close a Virtual Agent chat before submitting the case.
-   **[Review a customer interaction with Disputes intake via Virtual Agent](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/yokohama/markdown/yokohama/financial-services-operations/now-assist-for-financial-services-operations-fso/review-interaction-with-dispute-intake-virtual-agent.md)**  
Retrieve a chat interaction between a customer and Disputes intake via Virtual Agent to review a transcript of the conversation and confirm responses.

**Parent Topic:**[Using generative AI](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/yokohama/markdown/yokohama/financial-services-operations/now-assist-for-financial-services-operations-fso/using-now-assist-for-financial-services-operations-fso.md)

