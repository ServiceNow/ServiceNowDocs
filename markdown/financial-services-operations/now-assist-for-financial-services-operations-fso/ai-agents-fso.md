---
title: Standalone AI agents in Financial Services Operations
description: Use AI agents in FSO to accelerate dispute resolution and assist with front-office customer servicing. These agents automate routine steps and provide recommendations, keeping humans in the loop for final decisions.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/financial-services-operations/now-assist-for-financial-services-operations-fso/ai-agents-fso.html
release: australia
product: Now Assist for Financial Services Operations \(FSO\)
classification: now-assist-for-financial-services-operations-fso
topic_type: concept
last_updated: "2026-03-12"
reading_time_minutes: 3
breadcrumb: [Use agentic AI, Now Assist for FSO, Financial Services Operations \(FSO\)]
---

# Standalone AI agents in Financial Services Operations

Use AI agents in FSO to accelerate dispute resolutionand assist with front-office customer servicing. These agents automate routine steps and provide recommendations, keeping humans in the loop for final decisions.

The following table describes the available AI agents in Now Assist for FSO.

|Agents|Agent role|
|------|----------|
|Merchant analysis for disputes AI agent|Assesses merchant credibility in the context of the disputed transaction's reason, using web intelligence and internal dispute history, eliminating manual research.|
|Nacha operating guidelines check AI agent|Verifies chargeback eligibility of transactions against Nacha operating guidelines without relying on complex system rules.|
|ACH dispute return recommendation AI agent|Combines merchant risk analysis and Nacha eligibility checks to provide clear, consistent recommendations, whether to file a return, deny the claim, or request more documentation. This helps dispute agents to make faster, more accurate, and compliant decisions.|
|Dispute communication AI agent|Automates and streamlines communication with customers and Originating Depository Financial Institutions \(ODFIs\) throughout the ACH dispute life cycle. The agent generates, personalizes, and sends timely, compliant email notifications related to dispute outcomes, whether filing a return, denying a dispute claim, or requesting additional supporting documentation. This ensures clarity, regulatory adherence, and efficient case resolution.|
|Banking CSR customer insights AI agent|Displays relevant customer insights in a clear, organized format. This feature helps you quickly explore and access meaningful customer data to identify opportunities and determine appropriate next steps.|
|Banking CSR support AI agent|Acts as a copilot for customer support representatives \(CSRs\) during customer interactions to assist with banking inquiries. This includes providing information about accounts \(checking, savings, loans, cards\), transaction history and details, balance inquiries, credit score checks, product eligibility, mortgage and loan details, deposit accounts, payment history, financial account summaries, and general banking policies or procedures.|
|Insurance CSR customer insights AI agent|Supports CSRs by providing quick access to comprehensive insurance customer data. It covers a wide range of details including policies, claims, and servicing cases. The agent processes natural language queries and returns structured, context-aware responses with follow-up options.|
|Insurance CSR support AI agent|Acts as a real-time copilot for insurance CSRs during live calls, supporting both typed queries and transcript-based question inference. Responses are scoped strictly to insurance topics and the customer associated with the active interaction.|

## Role masking

Required roles: sn\_bom\_credit\_card.dispute\_agent\_connector, sn\_bom\_credit\_card.dispute\_agent, sn\_fso\_csr.business\_agent, sn\_fso\_csr.personal\_agent, and now\_assist\_panel\_user.

AI agents use [role masking](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/intelligent-experiences/enable-ai-experiences/aia-role-masking.md) to determine which users can access them. Ones installed with Now Assist applications have specific roles that come included with the application. If you select **Users with specific roles** for user access, you must configure the security controls to include these roles. For the instructions to change the security controls, see [Define security controls for an AI agent](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/intelligent-experiences/enable-ai-experiences/define-sec-controls-aia.md).

In the data access settings, you must also add the necessary roles to the FSO AI agents listed in the table earlier.

-   **[ACH dispute AI agents overview](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/financial-services-operations/now-assist-for-financial-services-operations-fso/ach-agentic-ai-workflow.md)**  
Agentic AI streamlines ACH dispute resolution by automating merchant analysis, Nacha eligibility checks, ACH dispute return recommendations, and communications with customers or ODFI \(Originating Depository Financial Institution\). This solution enhances efficiency, accuracy, and conformance, enabling financial institutions to resolve ACH disputes faster, reduce errors, and improve customer satisfaction.
-   **[Agentic Contact Center for Banking AI agents overview](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/financial-services-operations/now-assist-for-financial-services-operations-fso/agentic-contact-center-for-banking-agents-overview.md)**  
Agentic Contact Center for Banking uses AI agents to enhance customer service by providing customer support representatives with intelligent assistance during interactions. The Banking CSR Customer Insights and Banking CSR Support agents help reduce handling time, enable proactive outreach, and deliver personalized customer experiences through AI-driven analysis and contextual insights.
-   **[Agentic Contact Center for Insurance AI agents overview](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/financial-services-operations/now-assist-for-financial-services-operations-fso/agentic-contact-center-for-insurance-agents-overview.md)**  
Agentic Contact Center for Insurance uses AI agents to enhance customer service by providing insurance customer service representatives with intelligent assistance during interactions. The two key agents—Insurance CSR Customer Insights and Insurance CSR Support—help reduce handling time, enable proactive outreach, and deliver personalized customer experiences through AI-driven analysis and contextual insurance data.

**Parent Topic:**[Agentic AI use cases for FSO](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/financial-services-operations/now-assist-for-financial-services-operations-fso/usecase-now-assist.md)

