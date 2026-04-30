---
title: Enable viewing of search results for the current and another selected user
description: Enable the search as functionality when you want the ability to view search results common to the current user and another user that you specify.
locale: en-US
release: zurich
product: Contextual Search
classification: contextual-search
topic_type: task
last_updated: "2025-07-31"
reading_time_minutes: 1
breadcrumb: [Manage, Contextual search, Search administration, Configure core features, Administer]
---

# Enable viewing of search results for the current and another selected user

Enable the search as functionality when you want the ability to view search results common to the current user and another user that you specify.

## Before you begin

Role required: admin

## About this task

For example, an HR administrator may have some confidential information. A user might have partial access to the information. The Search as functionality applies security access to display results that are common to both the logged in or current user and the user referenced in the **Search as field**. The search result for the other user may have fewer entries than what that current user can actually view.

**Note:** No search result is displayed for **Predictive Intelligence Similarity** additional resources. Record producers only support searching for the current user.

## Procedure

1.  Navigate to **All** &gt; **Contextual Search** &gt; **Table Configuration**.

2.  Edit a table configuration record.

3.  In the Search as section, fill in the fields.

    ![Search as configuration fields.](../image/search-as.png)

<table id="table_gh2_gtj_lq"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Enable search as

</td><td>

Option to enable the Search as functionality.

</td></tr><tr><td>

Search as field

</td><td>

Field defining the other user to search as. This field appears only when you select **Enable search as**.

</td></tr><tr><td>

Results message

</td><td>

Message to display with search results when searching as a different user. This field appears only when you select **Enable search as**.

</td></tr><tr><td>

Condition

</td><td>

Condition restricting when the search result of the user mentioned in the **Search as field** should appear. This field appears only when you select **Enable search as**.**Note:** Both **Condition** and **Script** must evaluate to true for search results to appear. An empty condition or script also evaluates to true.

</td></tr><tr><td>

Script

</td><td>

A condition script, enabling administrators to implement more powerful conditions. For example, to restrict access to users that are members of a group, use gs.getUser\(\).isMemberOf\("&lt;group name&gt;"\). This field appears only when you select **Enable search as**.**Note:** Both **Condition** and **Script** must evaluate to true for search results to appear. An empty condition or script also evaluates to true.

</td></tr></tbody>
</table>
## Result

The **My Results** tab displays search results for the currently logged-in user. The **&lt;user-name&gt; Results** tab displays search results for the user referenced in the **Search as field**.

**Parent Topic:**[Managing contextual search](../concept/working-with-contextual-search.md)

