---
title: Configure persona field mapping for the community profile
description: Configure which fields appear in the community profile and manage the settings associated with those fields.
locale: en-US
release: zurich
product: Communities
classification: communities
topic_type: task
last_updated: "2025-07-31"
reading_time_minutes: 1
breadcrumb: [Configure the community profile, Configuring communities, Communities, Customer Service Management]
---

# Configure persona field mapping for the community profile

Configure which fields appear in the community profile and manage the settings associated with those fields.

## Before you begin

Role required: sn\_communities.admin

## Procedure

1.  Navigate to **All** &gt; **Community** &gt; **User Profile** &gt; **Persona Field Mapping**.

2.  Click **New**and then complete the Persona Field Mapping form.

<table id="table_lfn_yxr_d1b"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Persona

</td><td>

Name of the persona.

</td></tr><tr><td>

Source Value Table

</td><td>

Source table of the field to be added to the persona. Any table that is used as the **Source Value Table** should have a reference to the sys\_user table.

</td></tr><tr><td>

Source User Field

</td><td>

Field from the source value table.

</td></tr><tr><td>

Privacy Read Only

</td><td>

Select the check box to allow the community user to change the display settings for this field in their community profile.

</td></tr><tr><td>

Profile Field

</td><td>

Display name of the community profile field.

</td></tr><tr><td>

Source Value Field

</td><td>

Name of the field from the source table.

</td></tr><tr><td>

Read Only

</td><td>

Select the check box to not allow the community user to edit the value of this field.

</td></tr><tr><td>

Privacy Default

</td><td>

Privacy default setting for the field. It shows the field for the selected group of users.The available options are:

-   Everyone
-   Everyone after logging in
-   Only me
-   Followers


</td></tr></tbody>
</table>3.  Click **Submit**.


**Parent Topic:**[Configure the community profile](configure-community-profile.md)

