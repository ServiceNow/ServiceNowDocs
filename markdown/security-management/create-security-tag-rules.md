---
title: Create security tag rules
description: Security tag rules automatically apply tags to security incidents when specified conditions are met to provide security incident filtering for security analysts.
locale: en-US
release: yokohama
topic_type: task
last_updated: "2026-04-30"
reading_time_minutes: 1
breadcrumb: [Set up security tag groups and tags, Security Operations common functionality, Security Operations]
---

# Create security tag rules

Security tag rules automatically apply tags to security incidents when specified conditions are met to provide security incident filtering for security analysts.

## Before you begin

-   Security tags added by rules are removed automatically when rule conditions no longer match.
-   Manual security tags are preserved when automatic tags are applied.
-   When multi-selection is disabled for a security tag group, only one tag from that group can be applied to a security incident. If a security analyst manually applies a tag and an automatic tagging rule subsequently triggers for a different tag within the same group, the automatic tag overrides the manual tag.
-   Role required: sn\_si.admin

## Procedure

1.  Navigate to **All** &gt; **Security Operations** &gt; **Security Tags** &gt; **Tags**.

2.  Choose or [create a security tag](create-class-group-and-tags.md).

3.  In the **Security Tag Rules** related tab, select **New**.

4.  Fill in the fields on the form, as appropriate.

    |Field|Description|
    |-----|-----------|
    |Name|The name of the security tag rule.|
    |Security Tag|The security tag to attach to the rule.|
    |Active|Option to turn the security tag on or off.|
    |Description|A description of this rule.|

5.  Determine **Record Filtering.**

6.  Fill in the fields on the form, as appropriate.

    |Field|Description|
    |-----|-----------|
    |Use filter group|Option to associate the filter group to the rule.|
    |Table|The table to contain the rule.|
    |Condition|Option to add one or more filter conditions.|

7.  Select **Submit**


**Parent Topic:**[Set up security tag groups and tags](create-class-group-and-tags.md)

