---
title: Elimination of duplicate citations from UCF Shared list download
description: You can eliminate duplicate citations associated with the authority documents when you receive citations from UCF content as part of the same Shared list.
locale: en-US
release: zurich
product: Policy and Compliance Management
classification: policy-and-compliance-management
topic_type: concept
last_updated: "2025-07-31"
reading_time_minutes: 3
breadcrumb: [Configure UCF integration using UCF CCH, Manage UCF integration, Classic UI, Use, Policy and Compliance Management, Governance, Risk, and Compliance]
---

# Elimination of duplicate citations from UCF Shared list download

You can eliminate duplicate citations associated with the authority documents when you receive citations from UCF content as part of the same Shared list.

You can retain one citation as active and mark the duplicate citations as inactive. Move the control objectives of the duplicate citations to the active citation. If the duplicate citation is part of a parent–child hierarchy, then its Source ID is updated with the Source ID of the active citation.

## Duplication of UCF citations

Duplication occurs when you download UCF content that has multiple citations tied to the same Authority Document \(AD\). However, each of these citations is linked to a control objective or can be linked to multiple control objectives. In such cases, when you download UCF there would be as many citations linked to control objectives. The citations have different Source ID and different control objectives linked to them. Nevertheless, such citations are linked to the same AD.

Duplication is identified when the downloaded citations tied to an authority document have similar **Reference**, **Authority document**, and **Description** details but a different **Source ID**. Such citations that belong to the same authority document but downloaded multiple times are termed as duplicate citations.

![Duplicate citations downloaded from UCF.](../image/citation-ucf-duplication.png)

## Deduplication of UCF citations

You can retain one citation as active and mark the rest of the duplicate citations as inactive. The relationship of this inactive citation with that of the control objective is removed from the m2m table. In its stead, the record of the active citation is added to the control objective in the m2m table.

Similarly, the child citations of the duplicate citations, if any, can be grouped with the child citations of the active parent citation in the Citations related list of the active citation. For example, if the citation with Source ID 0123 is being retained, then the parent of the duplicate citation's child citation must be updated as 0123. Or, the child citation's parent Source ID as 0123 must be updated, so that the citation's parent–child relationship is retained.

## Fix provided to eliminate duplicate citations

This enhancement helps you to eliminate duplicate citations associated with the authority documents when you download UCF content, or by running an on-demand job after UCF content is downloaded. The fix is available when you:

-   Import data from the UCF Shared list. To download a UCF shared list, see [Download a UCF shared list](../task/download-a-shared-list.md).
-   Run the **UCF citation deduplication issue fix** on-demand job if you don’t want to import UCF again. This job eliminates the duplicate citations and fixes the parent–child relationship by appending the child citations of the inactive parent citation to the active parent.

1.  To run the on-demand job, navigate to **All** &gt; **System Definition** &gt; **Scheduled jobs**.
2.  Select **UCF citation deduplication issue fix** and click **Execute Now**.

After the fix:

1.  Navigate to **All** &gt; **Policy and Compliance** &gt; **Citations**
2.  Select **Group By** and right-click the list controls icon.
3.  Select **Reference** in the list.

    You can view citations with unique Reference ID, unique Description, and each citation belongs to a different AO. In the **Active** column, the active citation is **true**, and the duplicate citations are marked as **false**. Select and open one of the citation record, all control objectives are grouped in the Control objectives related list, and its child citations in the Citations related list.

    ![Active citation marked as true and duplicate citations marked as false.](../image/citation-dedup-fix.png)

    **Note:** Citations are considered as duplicate only when their **Reference ID**, **Authority document**, **Description** are the same. Even if one of these conditions isn’t fulfilled, then they’re considered as two different citations and not as duplicate.


**Parent Topic:**[Configure the UCF integration using the UCF Common Controls Hub](../task/configure-UCF-integration.md)

