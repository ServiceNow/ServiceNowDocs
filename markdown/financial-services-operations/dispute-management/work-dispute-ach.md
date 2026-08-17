---
title: Resolving ACH disputes
description: Work on an ACH dispute case to review case information, verify that any outstanding tasks are completed, and resolve the dispute.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/financial-services-operations/dispute-management/work-dispute-ach.html
release: australia
product: Dispute Management
classification: dispute-management
topic_type: concept
last_updated: "2026-03-12"
reading_time_minutes: 2
breadcrumb: [Processing, Use, Dispute Management, Banking applications, Financial Services Operations \(FSO\)]
---

# Resolving ACH disputes

Work on an ACH dispute case to review case information, verify that any outstanding tasks are completed, and resolve the dispute.

ServiceNow Otto for FSO accelerates and optimizes ACH dispute processing. AI-powered agents work alongside human agents to provide real-time insights, actionable recommendations, and predictive guidance. This enables faster, more accurate decisions that reduce resolution time and enhance customer experience.

The Processing stage of the playbook provides transaction information such as dispute amount, transaction date and time, merchant name, transaction state, current activity, and activity SLA.

After a dispute case is submitted, each disputed transaction is displayed in a **Dispute Workspace**. The dispute transaction progresses through these stages: Investigate, Chargeback, and Closure. As the dispute proceeds, the appropriate stage is updated accordingly. To open a transaction in the Dispute Workspace, select the transaction number.

\[Omitted image "ach-dispute-processing.png"\] Alt text: Dispute workspace displaying an ACH dispute.

-   The transactions are displayed in the **Dispute Workspace**.
-   Each transaction progresses through a series of steps, during which a corresponding sequence of tasks is generated. The tasks are displayed in **Tasks**.
-   The **Open** tab displays the tasks open along with the SLA and State.
-   The **Short description** provides a preview of the task. Select the task to view its details.
-   The **Closed** tab displays all the tasks that have been closed.
-   The activity stream for the transaction is displayed below the task.
-   The dispute transaction and financial transaction details are displayed in the **Disputed** transaction details and **Financial transaction details** widget.
-   **Attachments** can be added as needed. If Card Data Security is installed and configured, **Attachments** in the contextual side panel will handle files differently in transaction records. For more information, see [Manage attachments in Card Data Security](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/financial-services-operations/dispute-management/manage-attachments-in-card-data-security.md).

## ACH reason codes

For a list of supported ACH dispute reason codes in the Dispute Rules Content Pack for Nacha application, see [Dispute Reason Codes](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/financial-services-operations/dispute-management/components-installed-with-dispute-rules-content-pack-for-nacha.md)

-   **[ACH dispute AI agents overview](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/financial-services-operations/dispute-management/ach-agentic-ai-workflow.md)**  
Agentic AI streamlines ACH dispute resolution by automating merchant analysis, Nacha eligibility checks, ACH dispute return recommendations, and communications with customers or ODFI \(Originating Depository Financial Institution\). This solution enhances efficiency, accuracy, and conformance, enabling financial institutions to resolve ACH disputes faster, reduce errors, and improve customer satisfaction.
-   **[Processing an ACH dispute](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/financial-services-operations/dispute-management/process-dispute-ach.md)**  
On the **Processing** tab of the card disputes playbook, all disputed transactions in an ACH dispute case are displayed on a dashboard. The tab also provides transaction information such as dispute amount, transaction date and time, merchant, transaction state, current activity, and activity SLA.

**Parent Topic:**[Managing Disputes](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/financial-services-operations/dispute-management/managing-disputes.md)

