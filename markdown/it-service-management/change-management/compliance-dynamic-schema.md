---
title: Compliance dynamic schema
description: Compliance dynamic schema stores the risk and compliance details of a change as name and value pairs in a single field. This avoids adding a column to the Change Request table for each detail.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/it-service-management/change-management/compliance-dynamic-schema.html
release: brazil
product: Change Management
classification: change-management
topic_type: concept
last_updated: "2026-09-10"
reading_time_minutes: 3
breadcrumb: [Configure, Change Management, IT Service Management]
---

# Compliance dynamic schema

Compliance dynamic schema stores the risk and compliance details of a change as name and value pairs in a single field. This avoids adding a column to the Change Request table for each detail.

Regulated industries record compliance information with every change. Examples include whether the change handles personal data, whether an audit trail is required, and how long a rollback takes. These requirements vary, so the Change Request table stores them as dynamic attributes rather than as fixed fields.

Compliance dynamic schema applies the platform dynamic schema feature to change requests. For information, see [Dynamic Schema](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/platform-administration/dynamic-schema.md).

## Compliance dynamic schema elements

The compliance dynamic schema for change requests consists of the following elements.

-   **Dynamic namespace**

    The container for the schema, in the same way that a table name groups columns. Change requests use the `change_request/risk_and_compliance_attributes` namespace. All dynamic attributes, dynamic categories, and dynamic choices for the feature belong to this namespace.

-   **Dynamic attribute store field**

    The field that holds the attribute values as JSON. On the Change Request form this field is labeled **Risk and compliance attributes**.

-   **Dynamic category reference field**

    The field that references the dynamic category that applies to the change. On the Change Request form this field is labeled **Risk and compliance category**.


**Note:** Neither field appears on the Change Request form in the base system. You may need to configure the form to add these fields, and you can place them in the section that suits your process, such as the **Planning** or **Schedule** section.

## Dynamic categories for change requests

Categories are hierarchical. A category can have a parent category, so that a specific category nests under a broader one. For example, a category for changes that affect financial or payment systems can nest under a broader compliance category.

The base system includes example categories, such as Risk and Compliance, Financial Risk and Compliance, and SaaS/Cloud Security Compliance. You can deactivate these categories or add your own to match your organization's compliance requirements.

**Note:**

-   For more information about dynamic categories, see [Dynamic Schema](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/platform-administration/dynamic-schema.md).
-   To configure the Risk and compliance category, see [Configure the compliance dynamic schema](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/it-service-management/change-management/configure-compliance-dynamic-schema.md).

## Risk and compliance attributes

The namespace defines few dynamic attributes in the base system. These cover areas such as audit trail, downtime, estimated impacted users, lead time, rollback time, and compliance. Each attribute has a type, such as `True/False`, `Integer`, `Decimal`, or `String`, and a value entered for the attribute adheres to that type.

The attributes provided in the base system are examples. You can deactivate them or define the attributes that match the compliance requirements of your organization.

You can also record an attribute that is not defined in the namespace. Such an attribute is transient, applies only to the change request where you enter it, and is stored as a string whatever value you enter. Recording `"lead_time_to_complete" : "true"` on a change request creates a transient string attribute, because `lead_time_to_complete` is not defined in the namespace.

**Note:**

-   You can also read and update attribute values from scripts, including risk condition scripts and business rules. Use the dynamic schema scripting API to conditionally respond to attribute values or trigger downstream actions. For information about the scripting API, dynamic attributes, transient attributes, and configuration options, see [Dynamic Schema](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/platform-administration/dynamic-schema.md).
-   To configure the Risk and compliance attributes, see [Configure the compliance dynamic schema](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/it-service-management/change-management/configure-compliance-dynamic-schema.md).

For information about adding Risk and compliance attributes/categories to a change request, see [Create a change request](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/it-service-management/change-management/t_CreateAChange.md).

-   **[Configure the compliance dynamic schema](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/it-service-management/change-management/configure-compliance-dynamic-schema.md)**  
Review and adjust the dynamic namespace that supports the risk and compliance fields on a change request. Ensure the attributes and categories match the compliance obligations of your organization.

**Parent Topic:**[Configuring Change Management](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/it-service-management/change-management/configure-change-management.md)

