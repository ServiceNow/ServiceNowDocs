---
title: Setting up healthcare locations and healthcare organizations
description: Understand how healthcare locations and healthcare organizations function and should be organized to set up your care teams and the physical locations they operate in correctly.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/healthcare-life-sciences/healthcare-and-life-sciences-service-management-core/understanding-healthcare-locations-and-healthcare-organizations.html
release: australia
product: Healthcare and Life Sciences Service Management Core
classification: healthcare-and-life-sciences-service-management-core
topic_type: concept
last_updated: "2026-07-24"
reading_time_minutes: 5
breadcrumb: [Configure, Healthcare and Life Sciences Service Management Core, Healthcare and Life Sciences Service Management, Healthcare and Life Sciences]
---

# Setting up healthcare locations and healthcare organizations

Understand how healthcare locations and healthcare organizations function and should be organized to set up your care teams and the physical locations they operate in correctly.

## Healthcare organizations

The **healthcare organization** \[sn\_hcls\_organization\] table stores the details of a healthcare organization in your ServiceNow instance. The Parent Organization field on the linked Internal Organization or External Organization record is the authoritative reference for defining the organization hierarchy within a healthcare delivery network, capturing the structure that supports operations like access control, visibility, and routing.

An example healthcare organization hierarchy might look like:

**HQ** → **Hospital** → **Department** → **Unit**

Structuring healthcare organizations correctly is vital to healthcare operations as it defines the organizational structure, influencing visibility, responsibility, and routing.

These roles are healthcare-specific labels for the underlying Service Model Foundation \(SMF\) personas. For the platform-wide persona reference, including a healthcare example, see [Service Model Foundation personas](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/customer-service-management/smf-persona.md).

## Healthcare organization \[sn\_hcls\_organization\] table technical details

\[Omitted image "hcls-healthcare-organizations.png"\] Alt text: ERD diagram showing how business organizations and healthcare organizations interact.

When a healthcare organization is created, an associated Business Organization record is also created with the same name that references the healthcare organization. A bidirectional reference exists between the two tables. Business Organization is an extension of Organization Core.

A healthcare organization is associated with a Business Organization record, either internal or external.

It contains specific attributes not found in the Organization Core table. For example, organization type.

Use the **Parent Organization** field to create multi-level hierarchies by labeling healthcare organizations as parent to other healthcare organizations.

The **healthcare organization location association** table is a M2M table used to store the explicit link between healthcare locations and their owning healthcare organization.

For information on the fields present in the Healthcare organization table, see [Healthcare organization table](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/healthcare-life-sciences/healthcare-and-life-sciences-service-management-core/hcls-healthcare-organization-table.md).

## Healthcare organization related lists

The Healthcare Operations app menu shows an example of what a healthcare organization's hierarchy and related data look like.

\[Omitted image "hcso-healthcare-org-menu.png"\] Alt text: Healthcare Organizations app menu in Healthcare Operations Core.

Healthcare organizations use the child organization related list to display their direct child organizations. When a healthcare organization is created, the value it lists for **Parent Organization** indicates who the parent organization will be.

The **Business Organizations served** value determines how you track the relationship between requesting and fulfilling healthcare organizations. You can set hierarchy or relationship-based support criteria for your healthcare locations.

The following are all healthcare organization related lists and their features:

-   **Child organization**—select **New** in the child organizations related list to add a new child organization to the current healthcare organization record.
-   **Members**—displays all members of this organization. Select **Edit** to add, remove, or alter the responsibilities of members.
-   **Case opened by members**—displays all cases currently opened by members of this organization.
-   **Healthcare locations**—displays all associated healthcare locations with this healthcare organization. Select **Edit** to manage these associations.
-   **Assignment groups**—displays all associated assignment groups.
-   **Available services**—displays all available services within this organization.
-   **Organization customer criteria**—displays which customers are serviced by this healthcare organization.

## Healthcare locations

The **healthcare location** \[sn\_hcls\_location\] table represents the physical or virtual places where care and operational work occur — campuses, buildings, wings, units, rooms, and other serviceable spaces.

An example healthcare location hierarchy might look like:

**Campus** → **Hospital Building** → **Pediatrics Wing** → **PICU Unit** → **Bed** or **Room**

Structuring healthcare locations correctly enables agents and care teams to reference the precise location of issues. For example, an IT support agent can identify what room in the PICU unit has a broken monitor that needs repair.

By tying work to a specific location, ambiguity is reduced in requests and escalations, enabling for more efficient responses from care teams.

## Healthcare location \[sn\_hcls\_location\] table technical details

\[Omitted image "hcls-healthcare-locations.png"\] Alt text: ERD diagram which shows how the common location table and healthcare location table interact.

The healthcare location table provides the ability to map common locations to healthcare organizations.

The common location \[cmn\_location\] table provides the basis for location setup across the ServiceNow platform. Healthcare locations leverage common locations to extend the existing data into the HCLS data model.

Healthcare locations enable you to add attributes that aren’t available in the common location table. For example, the altitude field is available in healthcare locations without being added to all common locations.

The **healthcare organization location association** table limits the common locations shown to care team members when reporting issues, displaying only those that their unit is responsible for. This table is used to store the explicit link between healthcare locations and their owning healthcare organization.

Use the **Parent location** field to create multi-level hierarchies by labeling healthcare locations as parent to other healthcare locations.

When you're creating a location, you can navigate the existing location hierarchy to select where the new location should reside.

\[Omitted image "hco-locations-hierarchy-choose.png"\] Alt text: The location selection panel within Healthcare Operations Core.

When a location is created, the **Location hierarchy** panel displays up to three parent levels higher within the location's hierarchy.

**Note:**

The location hierarchy is only shown when the healthcare location is opened from the Healthcare Operations Core app module.

For information on the fields present in the Healthcare location table, see [Healthcare location table](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/healthcare-life-sciences/healthcare-and-life-sciences-service-management-core/hcls-healthcare-location-table.md).

## Associating healthcare locations and healthcare organizations

\[Omitted image "hcls-hola-table.png"\] Alt text: ERD diagram that shows the connection between healthcare locations and healthcare organizations.

The **healthcare organization location association** table \[sn\_hcls\_organization\_location\_association\] establishes a definitive connection between healthcare organizations and healthcare locations. This connection determines the healthcare organization responsible for a particular location.

Healthcare locations define which common locations a healthcare organization is responsible for. When a member of a care team unit goes to report an issue, they’re presented with a limited list of common locations that their unit is responsible for. This eliminates the need to sift through all available common locations in the system.

When creating a healthcare organization or a healthcare location, you can use this table to associate a healthcare location with a healthcare organization \(or vice versa\).

For more information on this process, see [Associate healthcare locations with a healthcare organizations]()

This association is healthcare's implementation of the generic Service Model Foundation relationship model. For the platform-wide pattern, see [Service Model Foundation relationships](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/customer-service-management/csm-data-model-relationships.md).

## How to set up healthcare organizations and healthcare locations

To create healthcare locations and healthcare organizations, see the following topics.

1.  [Create a healthcare location]()
2.  [Create a healthcare organization]()
3.  [Associate healthcare locations with a healthcare organizations]()

