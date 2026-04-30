---
title: About identifying affected accounts with Proactive Service Experience Workflows in Incident Management
description: An incident record is created when an event management system generates an alert and the affected accounts can be viewed in the Service Operations Workspace.
locale: en-US
release: zurich
product: Proactive Service Experience Workflows
classification: proactive-service-experience-workflows
topic_type: concept
last_updated: "2025-07-31"
reading_time_minutes: 1
breadcrumb: [Use, Proactive Service Experience Workflows]
---

# About identifying affected accounts with Proactive Service Experience Workflows in Incident Management

An incident record is created when an event management system generates an alert and the affected accounts can be viewed in the Service Operations Workspace.

When the technical support engineer logs in to the Service Operations Workspace, the affected configuration item, services, and customers are listed in the Overview section. These details are automatically updated when the Configuration Item in the Incident record is updated. When the Configuration Item is updated, the **Refresh Impacted Services** script is automatically triggered and retrieves services that are experiencing an outage or degradation. The impacted services associated with the accounts are identified and updated. Additionally, if a CSM agent associates a case with the incident record, the Affected Account list is also updated. When the Affected Account list is updated, the customer impact is visible to the support teams working on the incident record.

The following diagram shows the steps involved in creating an incident record.

![Infographic shows the process by which an incident record is created](../image/psew-incident-flow.png)

**Note:** The Change Management workflow follows the same process. When a configuration item is updated in a change request record, the **Refresh Impacted Services** script is triggered and the affected accounts are retrieved. Since the configuration item field is set to read-only, you must ensure that this field is populated before the script is triggered. See [Create a case from a change request](../task/psew-impact-change.md) for more details.

-   **[Create an incident in Proactive Service Experience Workflows](../task/create-an-incident-proactive.md)**  
Create an incident record in Proactive Service Experience Workflows to document an issue that your customer is facing.
-   **[Create cases from an incident record in Proactive Service Experience Workflows](../task/aw-impact-analysis.md)**  
Create cases from records so that you can identify and solve network issues for your enterprise customers.

**Parent Topic:**[Using Proactive Service Experience Workflows](use-assurance-workflows.md)

