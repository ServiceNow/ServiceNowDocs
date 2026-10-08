---
title: Close a customer dispute
description: Notify the customer of the outcome, capture the customer's feedback, and record closing information before closing the dispute.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/telecom-media-technology/close-customer-dispute.html
release: brazil
topic_type: task
last_updated: "2026-09-10"
reading_time_minutes: 3
keywords: [close, closure, customer dispute management]
breadcrumb: [Use Customer DIspute Management, Use, Customer Service Problem Management, Telecommunications, Media, and Technology \(TMT\)]
---

# Close a customer dispute

Notify the customer of the outcome, capture the customer's feedback, and record closing information before closing the dispute.

## Before you begin

Role required: sn\_telco\_adr\_mgmt.manager

## About this task

The closure stage runs after the resolution and dispute analysis stage. Use this task to notify the customer, collect their feedback, and close the dispute record.

## Procedure

1.  Navigate to **All** &gt; **Workspaces** &gt; **CRM Workspace**.

2.  Select the lists \(\[Omitted image "Lists.png"\] Alt text: ListIcon.\) icon.

3.  Navigate to **Customer Dispute Management** &gt; **All**.

4.  Open the dispute record.

5.  On the Closure stage, enter the dispute resolution details.

    |Field|Description|
    |-----|-----------|
    |Resolution code|Type of proposed resolution to identify the dispute.|
    |Add resolution notes to comments|Option to add the resolution notes to the CDM case activity stream, making them available to anyone who can view the CDM activity stream.|
    |Resolution notes|Detailed summary to resolve the dispute. Generate the resolution notes using the ServiceNow Otto component. To learn more, see [Generate resolution notes for ADR case](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/telecom-media-technology/now-assist-tmt-generate-resolution-notes-ad.md).|

6.  Select **Continue**.

    The system sends the customer an email that summarizes the dispute, investigation findings, and proposed resolution.

7.  Add the feedback from the customer in the **Resolution notes** field.

8.  Record the customer's response by selecting **Customer accepted** or **Customer rejected**.

    If the customer accepted the resolution, select **Customer accepted** and the dispute moves to the closure step. If the customer rejected the resolution, select **Customer rejected**. You are prompted to generate a deadlock letter before the dispute moves to closure.

9.  Generate a deadlock letter, draft the letter content and select **Generate and send**.

    To learn more, see [Generate a deadlock letter using ServiceNow Otto for TMT](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/telecom-media-technology/now-assist-tmt-generate-deadlock-letter.md).

    The system creates a PDF of the letter, sends it to the customer by email, and adds the PDF to the dispute's attachments. The sent email is displayed at the Notify regulator step.

    When a deadlock letter is generated after a customer rejection, the dispute's resolution code and status are set to **Resolved rejected: Deadlock letter generated**.

10. Enter the closing information for the dispute, then select **Save**.

    |Field|Description|
    |-----|-----------|
    |**Description**|Summary of the dispute.|
    |**Resolution codes**|Code that best describes how the dispute was resolved. Includes **Resolved rejected: Deadlock letter generated** when applicable.|
    |**Resolution notes**|Details of the resolution provided to the customer.|
    |**Additional comments**|Comments visible to the customer.|
    |**Work notes**|Internal notes not visible to the customer.|


## Result

The dispute is marked closed. The closing information is saved with the dispute record and is available for future reference or auditing.

-   **[Generate resolution notes for ADR case](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/telecom-media-technology/now-assist-tmt-generate-resolution-notes-ad.md)**  
Generate the resolution notes for an Alternative Dispute Resolution \(ADR\) case by using the resolution notes generation for ADR skill in the ServiceNow Otto for TMT application.
-   **[Generate a deadlock letter using ServiceNow Otto for TMT](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/telecom-media-technology/now-assist-tmt-generate-deadlock-letter.md)**  
Generate a deadlock letter for Alternative Dispute Resolution \(ADR\) case. Quickly create the details of the deadlock letter by using the deadlock letter draft generation skill in the ServiceNow Otto for TMT application.

**Parent Topic:**[Using Customer Dispute Management case](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/telecom-media-technology/use-alternative-dispute-resolution-case.md)

**Related topics**  


[Create a Customer Dispute Management case]()

[Investigate customer disputes]()

[Resolve a customer dispute and record the dispute analysis]()

[View a Customer Dispute Management case record]()

[Customer Dispute Management](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/telecom-media-technology/alternative-dispute-resolution.md)

