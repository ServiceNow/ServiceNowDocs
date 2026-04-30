---
title: Configure access control
description: Describes the step-by-step process for configuring Entity-based access control in Privacy Management, including property activation, hierarchy setup, record mapping, user assignment, bulk updates, and activating entity-based record access rules.
locale: en-US
release: xanadu
product: Privacy Workspace
classification: privacy-workspace
topic_type: concept
last_updated: "2025-11-27"
reading_time_minutes: 3
breadcrumb: [Access control through organizational structure, Use, Privacy Management, Governance, Risk, and Compliance]
---

# Configure access control

Describes the step-by-step process for configuring Entity-based access control in Privacy Management, including property activation, hierarchy setup, record mapping, user assignment, bulk updates, and activating entity-based record access rules.

The following steps outline how to configure access control in Privacy Management using Entity-based access \(EBA\). This process enables organizations to restrict user access to processing activity records and related data according to their position in the organizational hierarchy. By following these steps, administrators can ensure that privacy teams and users only access records relevant to their assigned entities, supporting both security and regulatory compliance.

1.  Install Entity-based access plugin and enable the entity-based access control property. This activates entity-based access features and allows you to configure access restrictions by legal entity.

    For information, see [Configure Entity-based access](configure-entity-based-access.md).

2.  Establish the organizational structure \(parent-child relationships\), where a global entity contains regional entities, and those in turn contain country-level entities.

    For information, see [Add hierarchical relationships between entities](task/add-hierarchical-relationships.md).

3.  If processing activities already exist, map each record to the appropriate entity in the organizational hierarchy, ensuring it is correctly linked as a downstream entity under the relevant legal entity, jurisdiction, or other defined structure. This guarantees that access restrictions are enforced accurately, as each record is tied to the correct part of the organization.
4.  In the Entity Configuration module, do the following:

    -   Provide access to teams and users based on your organizational structure. You can grant access to individual users, such as entity owners or privacy analysts, or to groups.
    -   Specify whether access applies only to the selected entity or also to downstream entities. This step ensures that only the appropriate teams or users can access records for their part of the organization.
    For information, see [Create an entity configurations](task/create-oganizational-structure.md).

5.  Run a bulk access update to switch from role-based access to entity-based access for all applicable records. Bulk Access Update enforces entity-based access restrictions across relevant records in Privacy Management.

    When performing a bulk update:

    -   Select the entity configuration and associated entities.
    -   Choose the tables where restrictions apply \(for example, Processing Activity or Privacy Assessment\).
    -   Preview the affected records to validate changes.
    -   Enable the update to apply restrictions.
    The system queues a scheduled job that processes the update and applies the new access rules to all selected records.

    For information on how to run batch updates, see [Set access restrictions using an entity based record access update utility](task/create-bulk-access-update-config-privacy.md).

6.  Use entity-based record access rules to enable continuous monitoring. These rules automatically apply restrictions to new or modified records, ensuring access settings stay enforced without manual updates. When the structure of the entities change, the system updates access controls automatically.

    For information on how to configure entity-based record access rules, see [Set Entity based record access rules](task/eba-access-rules-config-privacy.md).


-   **[Configure Entity-based access](configure-entity-based-access.md)**  
Configure entity-based access by installing the Entity-based Access Configurations plugin and enabling properties for record types.
-   **[Create an entity configurations](task/create-oganizational-structure.md)**  
Create an organizational structure by configuring entity-based access for different levels such as headquarters, regional offices, and subsidiaries, and define access rules for users and groups.
-   **[Add hierarchical relationships between entities](task/add-hierarchical-relationships.md)**  
Define hierarchical relationships between entities \(Global → Regional → Country-level\) using Upstream and Downstream options. Adding an hierarchy creates a clear organizational structure.
-   **[Set access restrictions using an entity based record access update utility](task/create-bulk-access-update-config-privacy.md)**  
Set access restrictions for the existing records in bulk by using the Entity based record access update utility guided-experience. Use the workflow to enable or disable access to record types.
-   **[Set Entity based record access rules](task/eba-access-rules-config-privacy.md)**  
Use entity-based record access rules to secure records and enable continuous monitoring. These rules automatically apply restrictions to new or modified records, ensuring access settings stay enforced without manual updates. When entities or processing activities change, the system updates access controls automatically.

**Parent Topic:**[Access control through organizational structure](access-control-by-legal-entity.md)

