---
title: Configure an entity type for a linked object
description: Configure an entity type by using the Entity Based Access application. You can specify an entity type, such as Company or Vendors, and manage the object access for the entity that is linked to that entity type.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/zurich/governance-risk-compliance/grc-common-functions/create-an-entity-type-configuration-for-entity-based-access.html
release: zurich
product: GRC Common Functions
classification: grc-common-functions
topic_type: task
last_updated: "2025-07-31"
reading_time_minutes: 1
breadcrumb: [Manage Entity Based Access, Entity Based Access, Common GRC features, Governance, Risk, and Compliance]
---

# Configure an entity type for a linked object

Configure an entity type by using the Entity Based Access application. You can specify an entity type, such as Company or Vendors, and manage the object access for the entity that is linked to that entity type.

## Before you begin

Role required: sn\_grc\_ent\_access.admin

## Procedure

1.  Navigate to **All** &gt; **Entity Based Access Configurations** &gt; **Entity Type Configurations**.

2.  Select **New**.

3.  On the [form](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/governance-risk-compliance/grc-common-functions/entity-type-configurations-form.md), fill in the fields.

    For a description of the field values, see [Entity Type Configurations form](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/governance-risk-compliance/grc-common-functions/entity-type-configurations-form.md).

    The following example shows that Banking is defined as an entity type. When the entity type for an entity is defined as Banking, its object access is managed with the Entity Based Access configuration.

    \[Omitted image "entity-type-config.png"\] Alt text: Entity type.

4.  Activate the configuration by selecting **Activate**.

    An entity type is set up where you can manage the object access for entities that are associated with that entity type. The configuration that is displayed in the example grants the users, Anglin and administrator, access to all system objects that are associated with the entities that belong to the selected entity type.


-   **[Entity Type Configurations form](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/governance-risk-compliance/grc-common-functions/entity-type-configurations-form.md)**  
Use the Entity Type Configurations form to create an entity type configuration within the Entity Based Access application.

**Parent Topic:**[Managing Entity Based Access](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/governance-risk-compliance/grc-common-functions/using-entity-based-access.md)

