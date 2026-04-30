---
title: Access control through organizational structure
description: Describes how access to processing activity records can be restricted by using Entity-Based Access \(EBA\).
locale: en-US
release: xanadu
product: Privacy Workspace
classification: privacy-workspace
topic_type: concept
last_updated: "2025-11-27"
reading_time_minutes: 2
breadcrumb: [Use, Privacy Management, Governance, Risk, and Compliance]
---

# Access control through organizational structure

Describes how access to processing activity records can be restricted by using Entity-Based Access \(EBA\).

User access to processing activity records and related data can be restricted based on an organizational structure. This structure may reflect a legal entity, jurisdiction, business unit, or any segmentation aligned with how your privacy teams operate. This approach enables granular security and supports regulatory compliance for organizations functioning across multiple regions or subsidiaries.

Entity-Based Access \(EBA\) implements this control by enforcing data segregation according to the defined organizational structure. With EBA, users can only view and manage records for the entities or jurisdictions to which they have been explicitly granted access. Records outside this defined scope remain hidden.

## Key characteristics

-   Dynamic segmentation: Access can be assigned based on the organizational structure, such as legal entity, jurisdiction, business unit, or any defined grouping. So processing activity records are only visible to the appropriate teams.
-   Regulatory alignment: Access controls can be mapped to organizational structures, helping organizations meet local regulatory requirements and maintain clear audit trails.

For information about configuring access control, see [Configure access control](configure-access-control-by-legal-entity.md).

## UI impact

-   Processing activity details: Hidden for records outside the user’s scope.
-   Data lineage: Information for inaccessible entities is hidden, and navigation buttons on the side panel are disabled.
-   Reports and dashboards: Visibility in reports such as processing activity, risk scan, and compliance is filtered based on entity configuration.

## Role capabilities

<table id="table_gyj_m5m_lhc"><thead><tr><th>

Role

</th><th>

Capabilities

</th></tr></thead><tbody><tr><td>

Privacy admin

</td><td>

-   Create entity configurations
-   Perform bulk access updates

</td></tr><tr><td>

Privacy manager

</td><td>

View entity configurations

</td></tr><tr><td>

Privacy analyst

</td><td>

Access records for configured entities and their associated downstream entities

</td></tr><tr><td>

Privacy business user

</td><td>

Access records for configured entities and their associated downstream entities

</td></tr></tbody>
</table>**Note:** Assigned roles such as assignee, reviewer, and analyst retain access to their assigned records even if those records fall outside the configured entity.

-   **[Configure access control](configure-access-control-by-legal-entity.md)**  
Describes the step-by-step process for configuring Entity-based access control in Privacy Management, including property activation, hierarchy setup, record mapping, user assignment, bulk updates, and activating entity-based record access rules.

**Parent Topic:**[Using Privacy Management](concept/using-privacy-mgmt.md)

