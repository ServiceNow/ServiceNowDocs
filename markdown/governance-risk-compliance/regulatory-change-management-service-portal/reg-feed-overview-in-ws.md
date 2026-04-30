---
title: Regulatory event alerts view
description: When you select a regulatory event alert in the List view in the Compliance Workspace, it displays the details of the alert on a new page. The details include the title of the alert, provider of the alert, its state, and other important information in the Overview tab and Details tab.
locale: en-US
release: xanadu
product: Regulatory Change Management Service Portal
classification: regulatory-change-management-service-portal
topic_type: concept
last_updated: "2025-07-31"
reading_time_minutes: 2
breadcrumb: [Manage regulatory tasks, Regulatory Change Management, Governance, Risk, and Compliance]
---

# Regulatory event alerts view

When you select a regulatory event alert in the List view in the Compliance Workspace, it displays the details of the alert on a new page. The details include the title of the alert, provider of the alert, its state, and other important information in the Overview tab and Details tab.

The regulatory event alerts page also displays the following tabs and related lists associated with the alert:

-   Overview tab
-   Details tab
-   Related documents list
-   Impact assessments list

The following section provides more information on the tabs and the related lists that are associated with the alert.

<table id="table_wlj_4q5_nqb"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Description

</td><td>

Detailed description of the regulatory event alert.

</td></tr><tr><td>

Stage: Visual component that guides through a sequence of stages of a regulatory event alert

</td><td>

Visual component for the regulatory event alert that displays the following stages:-   New: When a regulatory event alert is marked as applicable, the state of the alert is updated automatically to **In progress** in the Stepper component and a regulatory change task is automatically created.
-   Impact Assessment: When an impact assessment is initiated on the regulatory event alert, the stage in the stepper component is updated automatically to **Impact Assessment**.
-   In progress: When the state of the regulatory event alert is updated to**In progress**, the highlighted stage in the stepper component is displayed as **In progress**.
-   Closed: When the Regulatory event alert is in **Closed** state, the highlighted stage in the stepper component is displayed as **Closed**.

</td></tr></tbody>
</table>|Field|Description|
|-----|-----------|
|Regulatory alert|Details of the alert such as title of the alert, citation associated with the alert, provider URL, regulatory body URL, name of the provider, type of the alert, and coordinator of the alert.|
|Dates|Details of the important dates associated with the alert such as source publication date, comments date, effective date, compliance date, and expiration date.|
|Compose additional comments|Text box for entering additional comments related to the activity.|

|Field|Description|
|-----|-----------|
|Related documents|Details of the related documents associated with the alert such as citation, citation reference, title, and type.|

|Field|Description|
|-----|-----------|
|Impact assessments|Details about the impact assessment of the alert such as entity, risk assessment, assessor, inherent risk, and state.|

Taxonomy side-panel: The taxonomy side-panel displays the following taxonomy classes for the Regulatory event alert:

-   Regulatory bodies
-   Content types
-   Jurisdictions
-   Themes
-   Sectors

**Note:** The taxonomy classes are displayed only if the records have any values associated with them. For example, if the regulatory alert does not have any values for the taxonomy class Jurisdictions, the taxonomy category Jurisdictions is not displayed in the taxonomy side panel.

