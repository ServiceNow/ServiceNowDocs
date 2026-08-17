---
title: Customer Dispute Management
description: Customer Dispute Management provides a structured process to register, investigate, and resolve customer disputes and complaints, including disputes referred to regulatory bodies.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/telecom-media-technology/alternative-dispute-resolution.html
release: australia
topic_type: concept
last_updated: "2026-03-12"
reading_time_minutes: 2
keywords: [customer dispute management, dispute resolution, complaint management, regulatory compliance]
breadcrumb: [Explore, Customer Service Problem Management, Telecommunications, Media, and Technology \(TMT\)]
---

# Customer Dispute Management

Customer Dispute Management provides a structured process to register, investigate, and resolve customer disputes and complaints, including disputes referred to regulatory bodies.

Customer Dispute Management \(CDM\) is a specialized complaint management system within the CSM/FSM workspace. CDM extends complaint case functionality to handle formal dispute resolution processes between customers and organizations.

## Key benefits

CDM provides the following benefits:

-   Supports compliance with regulatory bodies that require formal, auditable dispute resolution processes.
-   Provides a structured workflow for acknowledging, investigating, and resolving customer disputes.
-   Maintains an audit trail of investigation findings, proposed resolutions, and customer responses.
-   Classifies dispute analysis using a hierarchical structure of product, category, subcategory, and reason for consistent analysis reporting.

## How it works

A customer dispute moves through four stages:

-   **Intake**: The dispute is registered with details of the submitter, affected product or service, and supporting documents. The customer or authorized representative receives an email notification confirming registration.
-   **Investigation**: The agent reviews the customer's previously reported records, links relevant records to the dispute, and documents key findings.
-   **Resolution and dispute analysis**: The agent drafts a resolution plan, creates resolution tasks, and records a dispute analysis including product, category, subcategory, and dispute reason.
-   **Closure**: The agent proposes the resolution to the customer by email and records whether the customer accepts or rejects it. If the customer rejects the resolution, the agent generates and sends a deadlock letter. The agent notifies the customer of the outcome, records customer feedback, and closes the dispute with a resolution code and closing notes. For disputes submitted by a regulatory body, the agent sends a summary of findings, proposed resolution, and customer feedback.

For more information on the steps at each stage, see [CDM playbook stages and activities](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/telecom-media-technology/cdm-playbook-stages-and-activities.md).

CDM case records use the Case Playbook for Complaints feature to capture details and execute the workflow. For more information about the Case Playbook for Complaints, see [Case Playbook for Complaints](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/customer-service-management/csm-playbook-complaint-overview.md).

## Dispute analysis

A dispute analysis record captures the analysis of a dispute using a hierarchy of product, category, subcategory, and reason. The record also identifies the assignment group responsible for the affected product line. Agents can create dispute analysis records manually during the resolution and dispute analysis stage.

## Roles and permissions

The following roles control access to customer dispute, regulatory, and dispute analysis data:

|Role|Description|
|----|-----------|
|sn\_telco\_adr\_mgmt.manager|Create, read, and update customer dispute records.|
|sn\_telco\_adr\_mgmt.viewer|Read access to customer dispute data tables.|
|sn\_telco\_adr\_mgmt.admin|Create, read, update, and delete access to dispute analysis category, reason, analysis, and regulatory data tables. Users without this role have read-only access or create/read/update access limited to the dispute analysis table only.|

## Related information

For information about using CDM cases, see [Using Customer Dispute Management case](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/telecom-media-technology/use-alternative-dispute-resolution-case.md).

**Related topics**  


[Customer service case types](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/customer-service-management/customer-service-case-types.md)

