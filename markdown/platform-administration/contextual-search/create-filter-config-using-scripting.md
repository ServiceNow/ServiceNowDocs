---
title: Create a filter configuration using scripts
description: Create filter conditions using script that you can associate with a table configuration. The search result displays results that meet the filter conditions.
locale: en-US
release: australia
product: Contextual Search
classification: contextual-search
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 1
breadcrumb: [Filter configuration for contextual search, Configuring contextual search, Contextual search, Search administration, Configure core features, Administer the ServiceNow AI Platform]
---

# Create a filter configuration using scripts

Create filter conditions using script that you can associate with a table configuration. The search result displays results that meet the filter conditions.

## Before you begin

Role required: admin

## Procedure

1.  Navigate to **All** &gt; **Contextual Search** &gt; **Table Configuration**.

2.  Open a table configuration record on which to create the filter.

3.  In the Filter Configurations related list, click **New**.

4.  On the form, fill in the fields.

<table id="test"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Resource configuration

</td><td>

Lookup icon ![Lookup icon to select a search context](../image/look-up-icon.png) to select a resource such as Knowledge Articles.

</td></tr><tr><td>

Table configuration

</td><td>

\[Read-only field\]. Table for which you want to apply the filter configuration.

</td></tr><tr><td>

Scripted filter

</td><td>

Check box to select if you want to enter scripts in the **Script** field.**Note:** The **Script** field appears only when you select **Scripted filter**.

</td></tr><tr><td>

Application

</td><td>

Application scope for your filter configuration.

</td></tr><tr><td>

Active

</td><td>

Check box to activate the filter configuration.

</td></tr></tbody>
</table>5.  Enter a script corresponding to the resource configuration.

    **Note:**

    Use one of these dynamic filter scripts to set up your dynamic filter.

6.  Click **Submit**.


**Parent Topic:**[Filter configuration for contextual search](../concept/filter-configuration-for-cxs.md)

