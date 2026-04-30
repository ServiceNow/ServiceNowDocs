---
title: View the history of changes to a changeset
description: View the details of changes in each committed changeset on the Activities tab.
locale: en-US
release: yokohama
product: DevOps \(Family\)
classification: devops-family
topic_type: task
last_updated: "2025-01-30"
reading_time_minutes: 1
breadcrumb: [Changesets and version control in CDM, Use, DevOps Config, IT Service Management]
---

# View the history of changes to a changeset

View the details of changes in each committed changeset on the **Activities** tab.

## Before you begin

**Important:** Starting with the Washington DC release, DevOps Config is being prepared for future deprecation. It will be hidden and no longer installed on new instances but will continue to be supported. For details, see the [Deprecation Process \[KB0867184\]](https://support.servicenow.com/kb_view.do?sysparm_article=KB0867184) article in the Now Support Knowledge Base.

Role required: cdm\_viewer or cdm\_editor or cdm\_exporter\_editor or cdm\_policy\_editor or cdm\_admin

## Procedure

1.  While working on a changeset, select the **Activity** tab.

    The **Changes** section displays the list of individual nodes for which changes were committed.

    ![cdm-changeset-activities-tab](../image/cdm-changeset-activities-tab.png)

<table id="table_gzb_kjf_1qb"><thead><tr><th>

Header

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Old name

</td><td>

The original name of the item. The entry is listed as "\(empty\)" when the name of the item has not changed. Select the link to view a detailed list of changes.

</td></tr><tr><td>

New name / New value / New type / New state

</td><td>

The setting that the item was changed to in the changeset.For all items, a value appears only if the data changed.

</td></tr><tr><td>

Conflict / Reason for conflict

</td><td>

Boolean that indicates whether this changeset has settings in conflict with another committed changeset.

</td></tr><tr><td>

Path

</td><td>

Path to the item that changed.

</td></tr><tr><td>

Updated / Updated by

</td><td>

User that updated the changeset and timestamp when it was committed.

</td></tr></tbody>
</table>2.  Select the **New name** link to view the new, old, and current setting of the name, value, type, and state of a CDI or variable.

    The Details dialog box displays the settings and indicates whether the changeset is in conflict with another changeset.

<table id="table_fv4_ghj_1qb"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

New name, New value, New type, New state

</td><td>

The new setting that the item was changed to in this changeset.A value appears only if the data changed.

 **Important:** The value that appears in the **New name** column might represent a setting that has not changed. To determine whether the name has changed, select the link. If there is a **New name** value in the dialog box, then the name has changed.

</td></tr><tr><td>

Old name, Old value, Old type, Old state

</td><td>

The original setting that the item had before the changes in this changeset were committed.

</td></tr><tr><td>

Current name, Current value, Current type, Current state

</td><td>

The setting of the item in the case that a changeset was committed after this changeset was committed.A value appears only if a valued changed in the other changeset.

</td></tr></tbody>
</table>
