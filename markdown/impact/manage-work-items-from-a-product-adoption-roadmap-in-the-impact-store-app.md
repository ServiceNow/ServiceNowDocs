---
title: Manage work items from a capability linked to a Product Adoption Roadmap in the Impact Store App
description: Convert a capability linked to a product adoption roadmap to an SPM entity either from the Impact home page or from the Product Adoption Roadmaps.
locale: en-US
release: australia
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 2
breadcrumb: [Work items, Using Impact, Impact]
---

# Manage work items from a capability linked to a Product Adoption Roadmap in the Impact Store App

Convert a capability linked to a product adoption roadmap to an SPM entity either from the Impact home page or from the **Product Adoption Roadmaps**.

## Before you begin

Role required: Impact App Admin, Impact Platform Owner, Impact Portfolio Owner, Instance Admin.

## Procedure

1.  Navigate to **All** &gt; **Impact** &gt; **Product adoption** &gt; **.**.

2.  On the Impact Workspace, select **Product adoption** &gt; **Product adoption roadmaps**.

3.  Select the product map that you want to convert.

    **Note:** You can't convert a legacy product adoption roadmap to an SPM or a CWM work item.

4.  Select the more action \(![more actions icon](../image/more-action-icon.png)\) icon for the desired capability and click **Convert to work item** option.

5.  Select a work item from those that are listed for the product adoption roadmap.

6.  Select **Next**.

    The corresponding SPM table or the CWM table opens in a conversion form in Strategic Planning Workspace view. The SPM record details are auto-populated in the fields, as the fields from the Impact entity are mapped to the SPM entity in the Impact SPM Definition table \[sn\_impact\_cust\_impact\_spm\_definition\]. You can continue with the auto-filled record details or update the details if needed.

7.  Select **Convert**.

    You are redirected to the **Work items** page and a UI message confirms that an SPM entity is created successfully with a link to the created SPM entity.

8.  Select the link to view the record details, or open the capability from the product adoption roadmap and click **Work Items** on the capability details page.

    ![Capability details work items tab](../image/capability_workitems.png "Work Items tab")

    You can view the work items that you created for this capability. A work item \(![](../image/impact-my-work-item-icon.png)\) icon on the capability indicate that one or more work items are associated with it.

    You can also access the capability from the Capability Map and navigate to the **Work Items** section to view the created items.

    -   **Users who can convert an Impact entity to an SPM work item**

        Impact App Admin, Impact Platform Owner, Impact Portfolio Owner and Instance Admin can start the impact entity conversion to SPM work item if they have create access for the SPM entity.

    -   **Impact entities that can be converted to SPM work items**

        Recommendations, Free-form Initiatives and capabilities linked to product adoption roadmap can be converted to SPM work items.

    -   **Expiry of SPM license**

        If the SPM license expires and the user still has access to the SPM tables, then they can convert successfully. However, if their access to SPM tables is revoked then they won’t be able to create a conversion and will be redirected to the home page that displays an error message.

    -   **Required SPM and CWM plugins**
        -   Collaborative Work Management
        -   Portfolio Planning Core/ Strategic Portfolio Management

