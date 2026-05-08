---
title: Setting up healthcare locations and healthcare organizations
description: Understand how healthcare locations and healthcare organizations function and should be organized to set up your care teams and the physical locations they operate in correctly.
locale: en-US
release: australia
product: Healthcare and Life Sciences Service Management Core
classification: healthcare-and-life-sciences-service-management-core
topic_type: concept
last_updated: "2026-03-12"
reading_time_minutes: 3
breadcrumb: [Configure, Healthcare and Life Sciences Service Management Core, Healthcare and Life Sciences Service Management, Healthcare and Life Sciences]
---

# Setting up healthcare locations and healthcare organizations

Understand how healthcare locations and healthcare organizations function and should be organized to set up your care teams and the physical locations they operate in correctly.

## Healthcare organizations

The **healthcare organization** \[sn\_hcls\_organization\] table stores the details of a healthcare organization in your ServiceNow instance. It’s the authoritative reference for defining the organization hierarchy within a healthcare delivery network, capturing the structure that supports operations like access control, visibility, and routing.

An example healthcare organization hierarchy might look like:

**HQ** → **Hospital** → **Department** → **Unit**

Structuring healthcare organizations correctly is vital to healthcare operations as it defines the organizational structure, influencing visibility, responsibility, and routing.

## Healthcare organization \[sn\_hcls\_organization\] table technical details

![ERD diagram showing how business locations and healthcare organizations interact.](../image/hcls-healthcare-organizations.png)

When a healthcare organization is created, an associated business location is also created with the same name that references the healthcare organization. A bidirectional reference exists between the two tables. A business location is an extension of a service organization.

A healthcare organization is associated with a business location, either internal or external.

It contains specific attributes not found in the service organization table. For example, organization type.

Use the **parent organization** field to create multi-level hierarchies by labeling healthcare organizations as parent to other healthcare organizations.

The **healthcare organization location association** table is used to store the explicit link between healthcare locations and their owning healthcare organization.

For information on the fields present in the Healthcare organization table, see [Healthcare organization table](../reference/hcls-healthcare-organization-table.md).

## Healthcare locations

The **healthcare location** \[sn\_hcls\_location\] table represents the physical or virtual places where care and operational work occur — campuses, buildings, wings, units, rooms, and other serviceable spaces.

An example healthcare location hierarchy might look like:

**Campus** → **Hospital Building** → **Pediatrics Wing** → **PICU Unit** → **Bed** or **Room**

Structuring healthcare locations correctly enables agents and care teams to reference the precise location of issues. For example, an IT support agent can identify what room in the PICU unit has a broken monitor that needs repair.

By tying work to a specific location, ambiguity is reduced in requests and escalations, enabling for more efficient responses from care teams.

## Healthcare location \[sn\_hcls\_location\] table technical details

![ERD diagram which shows how the common location table and healthcare location table interact.](../image/hcls-healthcare-locations.png)

The healthcare location table provides the ability to map common locations to healthcare organizations.

The common location \[cmn\_location\] table provides the basis for location setup across the ServiceNow platform. Healthcare locations leverage common locations to extend the existing data into the HCLS data model.

Healthcare locations enable you to add attributes that aren’t available in the common location table. For example, the altitude field is available in healthcare locations without being added to all common locations.

The **healthcare organization location association** table limits the common locations shown to care team members when reporting issues, displaying only those that their unit is responsible for. This table is used to store the explicit link between healthcare locations and their owning healthcare organization.

Use the **Parent location** field to create multi-level hierarchies by labeling healthcare locations as parent to other healthcare locations.

For information on the fields present in the Healthcare location table, see [Healthcare location table](../reference/hcls-healthcare-location-table.md).

## Associating healthcare locations and healthcare organizations

![ERD diagram that shows the connection between healthcare locations and healthcare organizations.](../image/hcls-hola-table.png)

The **healthcare organization location association** table \[sn\_hcls\_organization\_location\_association\] establishes a definitive connection between healthcare organizations and healthcare locations. This connection determines the healthcare organization responsible for a particular location.

Healthcare locations define which common locations a healthcare organization is responsible for. When a member of a care team unit goes to report an issue, they’re presented with a limited list of common locations that their unit is responsible for. This eliminates the need to sift through all available common locations in the system.

When creating a healthcare organization or a healthcare location, you can use this table to associate a healthcare location with a healthcare organization \(or vice versa\).

For more information on this process, see [Associate healthcare locations with a healthcare organizations](../task/hcls-sm-associate-healthcare-locations-organization.md)

## How to set up healthcare organizations and healthcare locations

To create healthcare locations and healthcare organizations, see the following topics.

1.  [Create a healthcare location](../task/hcls-sm-configure-healthcare-location.md)
2.  [Create a healthcare organization](hcls-sm-configure-healthcare-organizations.md)
3.  [Associate healthcare locations with a healthcare organizations](../task/hcls-sm-associate-healthcare-locations-organization.md)

