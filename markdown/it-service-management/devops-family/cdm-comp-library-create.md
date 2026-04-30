---
title: Create or update a component library
description: Create a component library to manage components that can be reused across multiple applications.
locale: en-US
release: xanadu
product: DevOps \(Family\)
classification: devops-family
topic_type: task
last_updated: "2024-08-01"
reading_time_minutes: 1
breadcrumb: [Sharing components among applications — Component libraries, Use, DevOps Config, IT Service Management]
---

# Create or update a component library

Create a component library to manage components that can be reused across multiple applications.

## Before you begin

**Important:** Starting with the Washington DC release, DevOps Config is being prepared for future deprecation. It will be hidden and no longer installed on new instances but will continue to be supported. For details, see the [Deprecation Process \[KB0867184\]](https://support.servicenow.com/kb_view.do?sysparm_article=KB0867184) article in the Now Support Knowledge Base.

Role required: cdm\_admin

## Procedure

1.  Navigate to **All** &gt; **DevOps Config** &gt; **DevOps Config Workspace**.

2.  Click the component libraries icon \(![Component libraries icon.](../image/icon-component-libraries.png)\) in the left navigation to open the **Component libraries** tab.

3.  Click **Create new library** to create a component library.

4.  On the form, fill in the fields.

<table id="table_vw1_lz3_bxb"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Library name

</td><td>

Name of the component library.This name must be unique across all CDM applications and libraries.

</td></tr><tr><td>

Description

</td><td>

Description about the component library, such as what type of components it includes.

</td></tr><tr><td>

Authoring groups

</td><td>

User groups with access to edit the component library. Users in the groups with appropriate roles can view the component library.**Note:** If you choose an authoring group, make sure you’re a member of that group, or you’ll lose editing access to the library.

However, if you have the cdm\_all\_app\_access and cdm\_admin roles, you will have full access to the component library, even if you're not a member of these authoring groups.

</td></tr></tbody>
</table>5.  Click **Create**.


## Result

A component library is created. The state of the library is set to Not Available, which means that any components added to the library cannot be used, updated, or exported.

## What to do next

1.  [Add or update a shared component in a component library](cdm-comp-library-add-component.md).
2.  [Activate a component library](cdm-comp-library-activate.md).

