---
title: Create a Playbook Content Item
description: Create a content item of Playbook type on portal so that users can navigate to the playbook experience. These content items are specifically configured to enable the playbook experience on portals.
locale: en-US
release: yokohama
topic_type: task
last_updated: "2025-04-15"
reading_time_minutes: 1
breadcrumb: [Set up custom Playbooks for Portals, Playbooks for Portals, Playbooks in Customer Service Management, Agent tools, Organize agent workspaces, Configuring Customer Service Management, Customer Service Management]
---

# Create a Playbook Content Item

Create a content item of Playbook type on portal so that users can navigate to the playbook experience. These content items are specifically configured to enable the playbook experience on portals.

## Before you begin

Role required: admin

## Procedure

1.  Navigate to **All** &gt; **Playbook Content Items** &gt; **New**.

    ![content item form showing all fields](../image/playbook-content-item.png "Content item form")

2.  In the form, fill out the fields.

<table id="table_bpj_hvr_1fc"><thead><tr><th>

Field

</th><th>

Definition

</th></tr></thead><tbody><tr><td>

Name

</td><td>

The name of the content item you are creating

</td></tr><tr><td>

Table

</td><td>

Map your table here

</td></tr><tr><td>

Record ID

</td><td>

Always enter -1

</td></tr><tr><td>

Playbook experience

</td><td>

The name of your playbook experience

</td></tr><tr><td>

Playbook experience record generator

</td><td>

Map your record generator

</td></tr><tr><td>

Portal page

</td><td>

`csm_intake` standard with the Playbooks for Customer Service Management application.**Note:** You can clone the `csm_intake` page and modify it per your requirements.

</td></tr><tr><td>

Title

</td><td>

Title that appears at the top of the page.

</td></tr></tbody>
</table>3.  Select **Submit**.


## What to do next

After completing this step, you can navigate to the portal where the catalog is mapped and execute the content item. The playbook intake experience opens, with the record generator mapped as the first activity.

