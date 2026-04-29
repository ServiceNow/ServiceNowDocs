---
title: About identifying affected accounts with Proactive Service Experience Workflows in Incident Management
description: An incident record is created when an event management system generates an alert and the affected accounts can be viewed in the Service Operations Workspace.
locale: en-US
release: australia
product: Proactive Service Experience Workflows
classification: proactive-service-experience-workflows
topic_type: concept
last_updated: "2026-03-12"
reading_time_minutes: 2
breadcrumb: [Proactive Service Experience Workflow, Use, Product Support for Technology]
---

# About identifying affected accounts with Proactive Service Experience Workflows in Incident Management

An incident record is created when an event management system generates an alert and the affected accounts can be viewed in the Service Operations Workspace.

When the technical support engineer logs in to the Service Operations Workspace, the affected configuration item and services are listed in the Overview section. The details about customer and consumer accounts are listed in the Customer impact tab. These details are automatically updated when the Configuration Item in the Incident record is updated. When the Configuration Item is updated, the **Refresh Impacted Services** script is automatically triggered and retrieves services that are experiencing an outage or degradation. The impacted services associated with the accounts are identified and updated. Additionally, if a CSM agent associates a case with the incident record, the Affected account list is also updated. When the Affected account list is updated, the customer impact is visible to the support teams working on the incident record. To learn more about the Customer impact tab, see [Enhancing customer impact visibility for PSEW processes](enhance-customer-impact-visibility-psew-process.md).

The following diagram shows the steps involved in creating an incident record.

![Infographic shows the process by which an incident record is created](../image/psew-incident-flow.png)

**Note:** The Change Management workflow follows the same process. When a configuration item is updated in a change request record, the **Refresh Impacted Services** script is triggered and the affected accounts are retrieved. Since the configuration item field is set to read-only, you must ensure that this field is populated before the script is triggered. See [Create a case from a change request](../task/psew-impact-change.md) for more details.

-   **[Create an incident in Proactive Service Experience Workflows](../task/create-an-incident-proactive.md)**  
Create an incident record in Proactive Service Experience Workflows to document an issue that your customer is facing.
-   **[Resolve an incident record in Proactive Service Experience Workflows](../task/aw-impact-analysis.md)**  
Resolve an incident record by creating cases from record so that you can identify and solve network issues for your enterprise customers.
-   **[Generate a proactive case from the customer impact tab](../task/generate-proactive-case-customer-impact-tab.md)**  
Generate a proactive case record for a customer issue in an incident, problem, or change. Inform the customer or consumer about the proactive case for the service issue.
-   **[Communicate with customer about proactive case](../task/create-communication-customer-impact-tab.md)**  
Communicate with the customer about the proactive case that is generated for service issue. Address the issue promptly and maintain clear, effective communication with the customer.
-   **[Update the proactive case with the resolution progress notes](../task/notify-customer-proactive-case.md)**  
Send notes to the proactive case record about the resolution progress. Update the proactive case record using insights from the customer impact tab.
-   **[Create a reactive case from the incident record](../task/create-reactive-case-cutomer-impact-tab.md)**  
Create a reactive case record from in an incident, problem, or change record. Analyze the impact and generate cases for service issues.

**Parent Topic:**[Using Proactive Service Experience Workflows](use-assurance-workflows.md)

