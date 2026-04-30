---
title: Auto-creation of cases and updates from incidents
description: Cases are created from the incidents.
locale: en-US
release: yokohama
product: Proactive Service Experience Workflows
classification: proactive-service-experience-workflows
topic_type: concept
last_updated: "2025-01-30"
reading_time_minutes: 2
breadcrumb: [Using Proactive Service Experience Workflows, Proactive Service Experience Workflows]
---

# Auto-creation of cases and updates from incidents

Cases are created from the incidents.

A case is designated as a major case based on the value specified in the `major_case_affected_account_threshold` system property. This value can be modified by the administrator.

For more information to generate proactive cases, see [Redirection to the right case type](../task/generate-proactive-cases.md).

![Image showing a major case and individual cases generated automatically from incidents](../image/psew-generate-proactive-cases.png)

Depending on the threshold value, different flows are triggered to either create one major incident, or several individual cases. The case record is then populated. For example, in minor case scenarios, the following information is populated:

-   Short description
-   Description
-   Proactive is true
-   Channel
-   Incident
-   Account field

The administrator can specify the fields that must be passed to the case records from the parent incident record to suit their business needs.

## Notify case information to customers

In the Service Operations Workspace, you can select one or more cases from the Cases section and select **Notify Customers**.

Enter your notification message and select **Submit**. The message is included under the Additional comments section with the case record and sent to the customer. When a customer responds to those comments either via an email, or from the CSM portal, these comments are copied to the incident record. The technical support engineer can view the response or any other feedback provided while reviewing the case.

![Dialog box on how to notify customers regarding case updates](../image/psew-auto-case-notify-cust.png)

**Note:**

To enable this feature, follow these steps:

-   In the application navigator, type `sys_properties.list.`
-   Search in the text field for the `proactive_workflows_for_providers.additional_comments_sync` system property.
-   Select the system property to open the record.
-   Enter **true** in the Value field and select **Update**.

To avoid additional comments from being copied to all cases related to the incident, deactivate the **Update case worknote for comments change** business rule in the incident table.

-   **[Setting major case threshold for auto generated cases](../task/psew-set-major-case-threshold.md)**  
Set the threshold value for major cases generated from incidents in the system properties.
-   **[Redirection to the right case type](../task/generate-proactive-cases.md)**  
Create a proactive case from an incident in the Proactive Service Experience Workflows.

**Parent Topic:**[Using Proactive Service Experience Workflows](use-assurance-workflows.md)

