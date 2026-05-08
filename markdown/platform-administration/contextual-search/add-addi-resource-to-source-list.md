---
title: Add additional resources to the source selector of a form
description: Add additional resources when you want the user to search beyond Knowledge and Service Catalog search resources. For example, add additional resources for Open Incidents, Resolved Incidents, or Similar Open Incidents.
locale: en-US
release: australia
product: Contextual Search
classification: contextual-search
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 1
breadcrumb: [Managing contextual search, Contextual search, Search administration, Configure core features, Administer the ServiceNow AI Platform]
---

# Add additional resources to the source selector of a form

Add additional resources when you want the user to search beyond Knowledge and Service Catalog search resources. For example, add additional resources for **Open Incidents**, **Resolved Incidents**, or **Similar Open Incidents**.

## Before you begin

Role required: admin

## About this task

Additional resources are pre-defined. An additional resource is either a searchable source table with query conditions or a reference to a Predictive Intelligence Similarity solution definition.

**Note:** You can only view the Predictive Intelligence resources if you are licensed for Predictive Intelligence and have activated [Predictive Intelligence for Contextual Search](../concept/predictive-intelligence-for-cxs.md).

## Procedure

1.  Navigate to **All** &gt; **Contextual Search** &gt; **Search Contexts**.

2.  Open the search context record for which you want to see the additional resources.

3.  In the Additional Resource Configurations related list, select **Edit**.

4.  Filter the additional resources displayed in the **Collection** field by defining filter conditions and selecting **Run filter**.

    As an example, you can display only additional resources with the Predictive Intelligence Similarity type.

5.  From the **Collection** field, move the required additional resources to the **Additional Resource Configurations List** field.

    For example, if you want to move additional resources whose type is **Predictive Intelligence Similarity**, then move **Similar Incidents**, **Similar Knowledge Articles**, **Similar Open Change Requests**, **Similar Open Incidents**, **Similar Open Problems**, and **Similar Resolved Incidents** from the **Collection** field to the **Additional Resource Configurations List** field.

    ![Edit Members form showing Predictive Intelligence Similarity additional resources moved to Additional Resource Configurations List.](../image/predictive-intelli-similarity.png)

    **Note:** You can view the Predictive Intelligence sources only if you have license for Predictive Intelligence.

6.  Select **Save**.

    The additional resources appear under **Additional Resource Configurations**.

    ![Additional resources displayed in Additional Resource Configurations related list.](../image/predictive-intelli-similarity1.png)


**Parent Topic:**[Managing contextual search](../concept/working-with-contextual-search.md)

**Related topics**  


[bundle-csm.similar-cases-additional-resources]

[bundle-csm.similar-cases-solution-definitions]

