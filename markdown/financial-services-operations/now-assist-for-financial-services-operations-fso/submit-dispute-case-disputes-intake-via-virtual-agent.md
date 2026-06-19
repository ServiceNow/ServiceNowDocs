---
title: Submit a dispute case with Disputes intake via Virtual Agent
description: Create a new dispute case using the Disputes intake via Virtual Agent skill in the Now Assist for Financial Services Operations \(FSO\) application. Customers can interact with a Virtual Agent chat, which collects and infers details from customer responses.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/zurich/financial-services-operations/now-assist-for-financial-services-operations-fso/submit-dispute-case-disputes-intake-via-virtual-agent.html
release: zurich
product: Now Assist for Financial Services Operations \(FSO\)
classification: now-assist-for-financial-services-operations-fso
topic_type: task
last_updated: "2025-07-31"
reading_time_minutes: 2
breadcrumb: [Use generative AI, Now Assist for FSO, Financial Services Operations \(FSO\)]
---

# Submit a dispute case with Disputes intake via Virtual Agent

Create a new dispute case using the Disputes intake via Virtual Agent skill in the Now Assist for Financial Services Operations \(FSO\) application. Customers can interact with a Virtual Agent chat, which collects and infers details from customer responses.

## Before you begin

Role required: none

## Procedure

1.  Initiate a chat with Disputes intake via Virtual Agent by selecting the Now Assist icon.

2.  Select **Report a dispute**.

    \[Omitted image "disputes-va-report-dispute.png"\] Alt text: In the topics list, select Report a dispute.

    A new dispute case is created to capture the customer's responses.

3.  The Virtual Agent asks questions to determine the dispute type, and the subsequent questions from the disputes questionnaire for this particular type of dispute.

    \[Omitted image "disputes-va-customer-input.png"\] Alt text: Disputes intake via Virtual Agent will prompt the customer for information, and the customer enters the information with text responses or by selecting options. \[Omitted image "disputes-va-select-txn.png"\] Alt text: The customer may also respond to questions by selecting options presented by Disputes intake via Virtual Agent.

    The virtual agent will inform the customer if the transaction is already part of another case.\[Omitted image "disputes-va-existing-case.png"\] Alt text: Disputes intake via Virtual Agent informing the user that there are already disputes filed for the selected transaction.

    Disputes intake via Virtual Agent rephrases questions from the dispute questionnaire in a conversational format.

    The dispute case is populated with information from the customer's responses. Disputes intake via Virtual Agent infers information from responses to populate other fields as necessary.

4.  If the dispute is for an ACH transaction, the customer may be asked to sign a Written Statement of Unauthorized Debit \(WSUD\), if required.

5.  When presented with the dispute submission disclaimer, select **Yes** to agree.

    If **No** is selected more than once, the user is redirected to a live agent.


## Result

Disputes intake via Virtual Agent creates a Card Disputes Service Case and presents the customer with a reference link.

\[Omitted image "disputes-va-complete.png"\] Alt text: The customer is presented with a case number at the end of the dispute submission process.

A card dispute processor may access the record and review its details in the workspace.

-   **[Resume a Disputes intake via Virtual Agent dispute case as an agent](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/financial-services-operations/now-assist-for-financial-services-operations-fso/resume-dispute-case-from-disputes-intake-via-virtual-agent.md)**  
As an agent, you can resume a card dispute case when a customer leaves a Virtual Agent chat in Disputes intake via Virtual Agent without submitting the dispute. Pick up where the customer left off and complete the details of the dispute case.
-   **[Resume a Disputes intake via Virtual Agent dispute case as a customer](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/financial-services-operations/now-assist-for-financial-services-operations-fso/resume-virtual-agent-dispute-case-as-customer.md)**  
Learn how a customer can resume a card dispute case in Disputes intake via Virtual Agent when they close a Virtual Agent chat before submitting the case.
-   **[Review a customer interaction with Disputes intake via Virtual Agent](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/financial-services-operations/now-assist-for-financial-services-operations-fso/review-interaction-with-dispute-intake-virtual-agent.md)**  
Retrieve a chat interaction between a customer and Disputes intake via Virtual Agent to review a transcript of the conversation and confirm responses.

**Parent Topic:**[Using generative AI in Now Assist for Financial Services Operations \(FSO\)](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/financial-services-operations/now-assist-for-financial-services-operations-fso/using-now-assist-for-financial-services-operations-fso.md)

