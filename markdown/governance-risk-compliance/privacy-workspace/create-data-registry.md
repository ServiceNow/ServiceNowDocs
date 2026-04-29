---
title: Create a data registry
description: Create a repository of the users and specify the owners of various applications. This repository helps to identify which user must be assigned the personal data rights \(PDR\) request tasks.
locale: en-US
release: australia
product: Privacy Workspace
classification: privacy-workspace
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 1
breadcrumb: [Configure, Personal Data Rights \(PDR\), Privacy Management, Governance, Risk, and Compliance]
---

# Create a data registry

Create a repository of the users and specify the owners of various applications. This repository helps to identify which user must be assigned the personal data rights \(PDR\) request tasks.

## Before you begin

Role required: sn\_grc\_pdr.pdr\_admin, sn\_grc\_pdr.pdr\_manager

## About this task

A data registry provides information about the business application or business process, its owner, and the type of data it stores, such as customer data, employee data, prospect data, or ex-employee data. When a privacy data rights request is created, based on this registry or repository, the action tasks are created for the right owners.

## Procedure

1.  Navigate to **All** &gt; **Personal Data Rights** &gt; **Personal Data Rights Workspace** &gt; **Lists** &gt; **Data registries**.

2.  Select **New**.

3.  On the form, fill in the fields.

<table id="table_plf_llq_bcc"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td class="sub-head" colspan="2">

Data owner registry

</td></tr><tr><td>

Requester type

</td><td>

Type of personal data stored. The choices are:-   **Customer**
-   **Employee**
-   **Ex-Employee**
-   **Prospect**


</td></tr><tr><td>

Asset type

</td><td>

Type of asset that contains the data.

</td></tr><tr><td>

Select asset

</td><td>

Specific asset that belongs to the asset type.

</td></tr><tr><td>

Description

</td><td>

Description of the registry.

</td></tr><tr><td class="sub-head" colspan="2">

Assignment

</td></tr><tr><td>

User assignment method

</td><td>

Assignment rule. The choices are as follows:-   **Manually assign the user and group**: Select this option if you must manually assign a user and a group.
-   **Choose user from selected asset record**: Select this option if you must use the user specified in the selected asset record.


</td></tr><tr><td>

Group

</td><td>

Group to which the asset belongs.

</td></tr><tr><td>

User

</td><td>

User responsible for the PDR request.

</td></tr></tbody>
</table>4.  Select **Save**.


## Result

When the PDR agents generate tasks, based on the registry, the action tasks will be created for the various task owners.

**Parent Topic:**[Configuring Personal Data Rights](../concept/configuring-personal-data-rights.md)

