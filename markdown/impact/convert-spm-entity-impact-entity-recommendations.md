---
title: Manage work items with recommendations for the Impact Store Application
description: Convert an Impact entity to an SPM entity either from the Impact home page or from the Recommendations list. Creating an Impact entity and associating the SPM record details help you to avoid manual intervention in converting the entities from Impact to SPM portals, and thereafter any duplication of entities in the process.
locale: en-US
release: zurich
topic_type: task
last_updated: "2025-07-31"
reading_time_minutes: 3
breadcrumb: [Work items, Using Impact, Impact]
---

# Manage work items with recommendations for the Impact Store Application

Convert an Impact entity to an SPM entity either from the Impact home page or from the **Recommendations list**. Creating an Impact entity and associating the SPM record details help you to avoid manual intervention in converting the entities from Impact to SPM portals, and thereafter any duplication of entities in the process.

## Before you begin

Role required: Impact App Admin, Impact Platform Owner, Impact Portfolio Owner

You can create or convert impact entities like recommendations and free form accelerators into SPM work item based on the required role, and create and write access to at least one of the SPM tables.

**Note:** Impact entities can either be converted into an SPM and Collaborative Work Management \(CWM\) work item, or, into an SPM or CWM work item.

## About this task

When you convert an Impact entity to an SPM entity, you are creating an SPM entity using some of the attributes of the Impact entity, and then associating the new SPM entity with the Impact entity.

For an Impact entity to be converted to an SPM entity, the recommendation must:

-   Not be hidden by selecting the **Hide** option
-   Be a rule-based recommendation
-   Have been created by squad

It can be associated to a free form initiative as well.

Impact entities that can be converted to SPM entities are:

-   Recommendations that are created via rule engine or manually created by Impact squad user, which are not associated with any initiative or accelerator type, except for free form initiatives, can be converted into an SPM entity such as a demand, epic, project, or any other available options.
-   If the status of the recommendation changes to **Rejected**, or as a user you hide the recommendation after creating the SPM entity, then you cannot view the created SPM entity list, and can no longer take any action such as create or delete the SPM entity within Impact.

## Procedure

1.  Navigate to **All** &gt; **Impact** &gt; **Home**.

2.  Select the recommendation that you want to convert.

    -   From the latest three listed in the **Recommended next steps** section.
    -   Select **View full list** if it is not in the **Recommended next steps** section.
3.  Select the **View Details** list and click **Convert to work item** option.

4.  Select a work item from those that are listed for the recommendation.

    Some of the work items may be disabled. A particular impact entity can be converted to multiple SPM entities without restriction. A recommendation can also be associated with multiple strategic programs without requiring the removal of any existing associations.

5.  Select **Next**.

    The corresponding SPM table or the CWM table opens in a conversion form in Strategic Planning Workspace view. The SPM record details are auto-populated in the fields, as the fields from the Impact entity are mapped to the SPM entity in the Impact SPM Definition table \[sn\_impact\_cust\_impact\_spm\_definition\]. You can continue with the auto-filled record details or update the details if needed.

6.  Select **Convert**.

    A UI message confirms that an SPM entity is created successfully with a link to the created SPM entity.

7.  Select the link to view the record details, or select the recommendation and click **My work items**.

    You can view the work items that you created for this recommendation.

    ![New SPM entity created from the Impact entity.](../image/recom-spm-entity-impact.png)

    In the recommendation pop-up, the **My work items** tab lists all the SPM entities like demands, projects, and others that are associated to the recommendation. If you would like to create another work item, then select **Convert to work item**.

8.  To delete the work item, select the work item and click **Delete**.

    Select **Delete** in the Are you sure? pop-up. A message confirms the successful deletion of the work item.

    -   **Users who can convert an Impact entity to an SPM work item**

        Impact App Admin, Impact Platform Owner, Impact Portfolio Owner and Instance Admin can start the impact entity conversion to SPM work item if they have create access for the SPM entity.

    -   **Impact entities that can be converted to SPM work items**

        Recommendations and Free-form Initiatives can be converted to SPM work items.

    -   **Expiry of SPM license**

        If the SPM license expires and the user still has access to the SPM tables, then they can convert successfully. However, if their access to SPM tables is revoked then they won’t be able to create a conversion and will be redirected to the home page that displays an error message.

    -   **Required SPM plugins**
        -   Collaborative Work Management
        -   Portfolio Planning Core

