---
title: Configure information completeness rules for entity types in Investigative Case Management
description: Configure the rules for record completeness for each entity type.
locale: en-US
release: australia
topic_type: task
last_updated: "2026-04-07"
reading_time_minutes: 1
breadcrumb: [Entity Management, Investigative Case Management, Playbooks and Solutions, Configure agent workspaces, Configure, Public Sector Digital Services \(PSDS\)]
---

# Configure information completeness rules for entity types in Investigative Case Management

Configure the rules for record completeness for each entity type.

## About this task

While most entity record fields are not mandatory, each entity record contains a completeness field that tracks whether the record has sufficient data to be searchable within ICM. These rules outline the minimum amount of information required for each entity record type to be considered complete. These rules are configurable by an admin, and you can modify which fields are required to be filled in for an entity record to become searchable.

For more information on the default completeness rules for ICM entities, see [Completeness Rules by Investigative Case Management Entity Type](../reference/psds-icm-ref-entity-man-completeness-rules.md).

## Before you begin

Role required: admin

Set the scope to Investigative Case Management Foundation.

**Note:** Direct edits are flagged as customizations and can be overwritten on upgrade. Capture changes in an Update Set and note the sys\_id before editing.

## Procedure

1.  Navigate to **All** &gt; **System Definition** &gt; **Business Rules**.

2.  Filter the list to include only items from the Investigative Case Management Foundation application.

3.  Select the information completeness business rule of the entity for which you want to edit.

4.  Select **Advanced**.

5.  Edit the script, adding or removing fields as needed under the **Check for one of the two identification conditions**, and **If any of the identification conditions are met, mark as complete** line items.

    ![business rule editing, admin view.](../image/psds-info-complete-business-rule.png)

6.  Once you are finished editing the record, select **Update**.


## Result

The entity completeness fields have now been modified, and the entity record will now appear in a case dropdown menu when the modified criteria is met.

