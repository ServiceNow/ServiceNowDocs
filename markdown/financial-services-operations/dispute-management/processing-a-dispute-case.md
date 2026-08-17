---
title: Processing a Visa card dispute
description: A dispute case moves through Initiate, Processing, and Closure stages. The case playbook displays disputed transaction details, including customer information, dispute amount, card details, merchant, transaction state, and activity SLA.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/financial-services-operations/dispute-management/processing-a-dispute-case.html
release: australia
product: Dispute Management
classification: dispute-management
topic_type: concept
last_updated: "2026-03-12"
reading_time_minutes: 2
breadcrumb: [Managing disputes integrated with Visa, Processing, Use, Dispute Management, Banking applications, Financial Services Operations \(FSO\)]
---

# Processing a Visa card dispute

A dispute case moves through **Initiate**, **Processing**, and **Closure** stages. The case playbook displays disputed transaction details, including customer information, dispute amount, card details, merchant, transaction state, and activity SLA.

After a dispute case is submitted, all disputed transactions are displayed in the case playbook. Each transaction can be viewed in a separate **Dispute Workspace**, which displays all the details of the transaction. The dispute transaction progresses through these stages: **Investigate**, **Chargeback**, and **Complete**. To open a transaction in the **Dispute Workspace**, select the transaction number.

-   Each transaction progresses through a series of steps, during which a corresponding sequence of tasks is generated. The tasks are displayed in **Tasks**.
-   The **Open** tab displays the tasks open along with the SLA and State.
-   The **Short description** provides a preview of the task. Select the task to view its details.
-   The **Closed** tab displays all the tasks that have been closed.
-   The activity stream for the transaction is displayed below the task.
-   The dispute transaction and financial transaction details are displayed in **Disputed transaction details** and **Financial transaction details** widget.
-   The **Attachments** displays files attached to the case. If Card Data Security is installed and configured, **Attachments** in the contextual side panel will handle files differently in transaction records. For more information, see [Manage attachments in Card Data Security](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/financial-services-operations/dispute-management/manage-attachments-in-card-data-security.md).

**Note:** The case reaches the **Closure** stage only after all transactions under it attain the **Complete** status.

-   **[Investigate stage](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/financial-services-operations/dispute-management/investigate-stage.md)**  
The **Investigate** stage of the card dispute includes activities such as issuing provisional credit, reviewing participating merchant alerts, and investigating the transaction.
-   **[Chargeback stage](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/financial-services-operations/dispute-management/chargeback-stage.md)**  
This stage enables you to report fraud, initiate chargeback, associate dispute transactions, and review merchant representment evidence, create and review pre-arbitration, and case filing. Visa transactions comprises of two workflows for pre-arbitration and arbitration: collaboration workflow and allocation workflow.

**Parent Topic:**[Managing disputes integrated with Visa](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/financial-services-operations/dispute-management/work-on-a-dispute-case-integrated-with-visa.md)

**Related topics**  


[Summarize a dispute or claims case with case summarization](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/financial-services-operations/dispute-management/summarize-case-using-now-assist-fso.md)

