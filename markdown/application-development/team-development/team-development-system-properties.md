---
title: Team Development system properties
description: A reference topic that contains the information on the properties used in Team Development.
locale: en-US
release: zurich
product: Team Development
classification: team-development
topic_type: reference
last_updated: "2025-10-02"
reading_time_minutes: 1
breadcrumb: [Team Development Reference, Team Development, Planning your application, Building applications]
---

# Team Development system properties

A reference topic that contains the information on the properties used in Team Development.

<table id="table_xp1_rjx_pgc"><thead><tr><th>

System property

</th><th>

Function

</th></tr></thead><tbody><tr><td>

com.snc.teamdev.requires\_codereview

</td><td>

Setting this property adds the **Code Review Requests** module to the application menu. All changes pushed to this instance remain in the **Awaiting Code Review** stage until the Team Development Code Reviewers group approves the changes. See [Enable a code review](../task/t_EnableCodeReview.md).

</td></tr><tr><td>

glide.ui.javascript\_editor

</td><td>

Setting this property to false makes the following functions accessible:-   Script fields \(such as Script Include\).
-   Side-by-side script comparison.

 See [Merge tool](../concept/diff-merge-tool.md).

</td></tr><tr><td>

glide.update.suppress\_update\_version

</td><td>

Setting this property configures a table that doesn’t track customizations in the sys\_update\_version table. See [Suppress versions](../task/t_SuppressVersions.md).

</td></tr><tr><td>

mergetool.bg.left.highlight

</td><td>

Setting this property highlights the left column cell color when values differ between versions. See [Merge tool](../concept/diff-merge-tool.md).

</td></tr><tr><td>

mergetool.bg.right.highlight

</td><td>

Setting this property highlights the right column cell color when values differ between versions. See [Merge tool](../concept/diff-merge-tool.md).

</td></tr><tr><td>

mergetool.bg.left

</td><td>

Setting this property adds a left column cell color when version values are the same. See [Merge tool](../concept/diff-merge-tool.md).

</td></tr><tr><td>

mergetool.bg.right

</td><td>

Setting this property adds a right column cell color when version values are the same. See [Merge tool](../concept/diff-merge-tool.md).

</td></tr></tbody>
</table>**Parent Topic:**[Team Development Reference](team-development-reference.md)

