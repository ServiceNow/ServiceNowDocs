---
title: Configure an entity class for a linked object
description: Configure an entity class for a linked object by using the Entity Based Access application. You can define an entity class, such as Business Process, Business Service, or Database, and manage the object access for the entity that is linked to that entity class.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/governance-risk-compliance/grc-common-functions/create-an-entity-class-configuration-for-entity-based-access.html
release: australia
product: GRC Common Functions
classification: grc-common-functions
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 1
breadcrumb: [Manage Entity Based Access, Entity Based Access, Common GRC features, Governance, Risk, and Compliance]
---

# Configure an entity class for a linked object

Configure an entity class for a linked object by using the Entity Based Access application. You can define an entity class, such as Business Process, Business Service, or Database, and manage the object access for the entity that is linked to that entity class.

## Before you begin

Role required: sn\_grc\_ent\_access.admin

## Procedure

1.  Navigate to **All** &gt; **Entity Based Access Configurations** &gt; **Entity Class Configurations**.

2.  Select **New**.

3.  On the [form](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/governance-risk-compliance/grc-common-functions/entity-class-configurations-form.md), fill in the fields.

    For a description of the field values, see [Entity Class Configurations form](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/governance-risk-compliance/grc-common-functions/entity-class-configurations-form.md).

    The following example defines Application as an entity class. When an entity is linked with the Application entity class, its object access is managed with the Entity Based Access configuration.

    \[Omitted image "entity-class.png"\] Alt text: Entity class.

4.  Activate the configuration by selecting **Activate**.

    An entity class configuration is configured. You can now control the object access for the entities that are associated with that entity class.


-   **[Entity Class Configurations form](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/governance-risk-compliance/grc-common-functions/entity-class-configurations-form.md)**  
Use the Entity Class Configurations form to set up access control to all the entities that are linked to the entity class.

**Parent Topic:**[Managing Entity Based Access](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/governance-risk-compliance/grc-common-functions/using-entity-based-access.md)

