---
title: GRC: Entity Based Access for AI assets
description: The GRC: Entity Based Access application enables you to segregate data on the AI asset records to ensure that only authorized users can access sensitive AI Risk and Compliance data while maintaining visibility into core entities. Entity-based access administrators can use this application to set up secure, controlled access to various AI assets and its related objects.
locale: en-US
release: yokohama
product: AI Risk Management
classification: ai-risk-management
topic_type: concept
last_updated: "2025-12-01"
reading_time_minutes: 3
breadcrumb: [Explore, AI Risk and Compliance, Governance, Risk, and Compliance]
---

# GRC: Entity Based Access for AI assets

The GRC: Entity Based Access application enables you to segregate data on the AI asset records to ensure that only authorized users can access sensitive AI Risk and Compliance data while maintaining visibility into core entities. Entity-based access administrators can use this application to set up secure, controlled access to various AI assets and its related objects.

## GRC: Entity Based Access for AI assets

Entity-Based Access \(EBA\) is a security feature designed to provide granular, data-level access control within AI Risk and Compliance application. Unlike role-based access control, EBA decides which records a user can access based on business entities such as departments, regions, or business units. This approach ensures that sensitive information is only accessible to authorized users, aligning with organizational compliance and confidentiality requirements.

[AI Risk and Compliance](../reference/ai-risk-and-compliance.md) managers can access risks, controls, related entities, issues, indicators, AI asset tasks, risk assessments, attestations, and AI assets data through entity-based access. Entities themselves stay visible to all users, while visibility of linked records is limited to authorized users.

When a user is qualified based on these configurations and has the minimum required roles, they have access to the following tables:

-   AI system \[sn\_grc\_ai\_gov\_ai\_system\]
-   AI system entity \[sn\_grc\_ai\_gov\_ai\_system\_entity\_map\]
-   AI system task \[sn\_grc\_ai\_gov\_ai\_system\_task\]

## Configure GRC: Entity Based Access

The following tasks must be performed to enable and use GRC: Entity Based Access for the AI asset records.

1.  Install the GRC: Entity Based Access application. For more information, refer to [Install the Entity Based Access application](../../grc-common/task/install-entity-based-access.md).
2.  Enable or disable the entity-based Access properties to control access to the objects that are associated with an AI asset. For more information, refer to [Set up Entity Based Access properties](../../grc-common/task/set-up-entity-based-access-properties.md).
3.  Configure an entity class for a linked object by using the GRC: Entity Based Access application. For more information, refer to [Configure an entity class for a linked object](../../grc-common/task/create-an-entity-class-configuration-for-entity-based-access.md).

    **Note:** Entities created with an AI asset are assigned an entity class such as AI system, AI model, dataset, or MCP server, depending on their category. To apply access restrictions to these entities, you must configure the appropriate entity class settings.

4.  Configure an entity type by using the GRC: Entity Based Access application. For more information, refer to [Configure an entity type for a linked object](../../grc-common/task/create-an-entity-type-configuration-for-entity-based-access.md).
5.  Set access restrictions for the existing records in bulk by using the entity-based record access update utility guided-experience. For more information, refer to [Set access restrictions using an entity based record access update utility](../../grc-common/task/create-a-bulk-access-update-configuration.md).
6.  Configure entity-based record access rules on record types to apply access restrictions to new records automatically. For more information, refer to [Configure entity-based record access rules](../../grc-common/task/configure-continuous-eba-monitoring-on-record-types.md).

    **Note:** Three records are provided by default, each with specific field configurations. The AI Asset record \(sn\_grc\_ai\_gov\_ai\_system\) includes Analyst and Business owner as user fields, and Analyst Group as a group field. For AI Asset task \(sn\_grc\_ai\_gov\_ai\_system\_task\), you can find Assigned to and Watch list as user fields. The Related Entity record \(sn\_grc\_ai\_gov\_ai\_system\_entity\_map\) doesn’t have any user or group fields configured by default.


