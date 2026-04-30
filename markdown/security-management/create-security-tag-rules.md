---
title: Create security tag rules
description: Security tag rules provide filtering for security tag access.
locale: en-US
release: zurich
topic_type: task
last_updated: "2026-04-30"
reading_time_minutes: 1
breadcrumb: [Set up security tag groups and tags, Security Operations common functionality, Security Operations]
---

# Create security tag rules

Security tag rules provide filtering for security tag access.

## Before you begin

-   Security tags added by rules are removed automatically when rule conditions no longer match.
-   Manual security tags are preserved when automatic tags are applied.
-   When multi-selection is disabled for a security tag group, only one tag from that group can be applied to a security incident. If a security analyst manually applies a tag and an automatic tagging rule subsequently triggers for a different tag within the same group, the automatic tag overrides the manual tag.
-   Role required: sn\_si.admin

## Procedure

1.  Navigate to **Workspaces** &gt; **Security Exposure Management Workspace**.

2.  Select **Administration** in the navigation pane.

3.  Select **Review** on the **Security tags** tile.

4.  Security tags will be displayed in a list grouped by Security tag groups.

5.  Choose or [create a security tag](create-class-group-and-tags.md).

6.  In the **Security Tag Rules** related tab, select **New**.

7.  Fill in the fields on the form, as appropriate.

    |Field|Description|
    |-----|-----------|
    |Name|The name of the security tag rule.|
    |Security Tag|The security tag to attach to the rule.|
    |Active|Option to turn the security tag on or off.|
    |Description|A description of this rule.|

8.  Determine **Record Filtering.**

9.  Fill in the fields on the form, as appropriate.

    |Field|Description|
    |-----|-----------|
    |Use filter group|Option to associate the filter group to the rule.|
    |Table|The table to contain the rule.|
    |Condition|Option to add one or more filter conditions.|

10. Select **Submit**.


**Parent Topic:**[Set up security tag groups and tags](create-class-group-and-tags.md)

