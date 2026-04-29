---
title: Automation opportunity sub-groups
description: Large automation opportunities in AIOps LEAP can be broken into smaller, more manageable sub-groups to achieve more granular and accurate incident resolution.
locale: en-US
release: australia
product: AIOps LEAP \(Learning-Enhanced Automation Playbooks\)
classification: aiops-leap-learning-enhanced-automation-playbooks
topic_type: concept
last_updated: "2026-03-12"
reading_time_minutes: 1
breadcrumb: [Exploring AIOps LEAP, AIOps Learning Enhanced Automation Platform \(LEAP\), Now Assist for ITOM, IT Operations Management]
---

# Automation opportunity sub-groups

Large automation opportunities in AIOps LEAP can be broken into smaller, more manageable sub-groups to achieve more granular and accurate incident resolution.

Large automation opportunities with over 150 records tend to generate overly lengthy resolution steps that lack precision and focus. These opportunities often represent a collection of related problems and issues that should be subdivided to produce more targeted and relevant solutions.

Breaking them into smaller sub-groups enables users to obtain more refined resolutions for recurring issues. The Action Insights panel on the automation opportunity details page offers recommendations to create these sub-groups for opportunities containing large record volumes.

## Automatic reorganization

During scheduled LEAP analysis reruns, clusters are automatically reorganized. Automation opportunities that lack any associated artifacts are marked as deactivated, while those containing resolution steps or other artifacts remain active and are linked to newly identified matching automation opportunities.

Resolution steps from the previous automation opportunities are appended to their new counterparts. Users can choose to keep these existing resolution steps or use the **Regenerate** button to create fresh ones. This approach allows organizations to leverage previous resolutions to help improve the quality of resolution steps for new automation opportunities.

## Benefits of sub-grouping

-   Can provide more focused and contextual resolution steps
-   May offer more targeted solutions for similar issues
-   Can help support improve incident resolution
-   Enables more effective management of large automation opportunities
-   May contribute to better operational efficiency by reusing prior resolutions where appropriate

See [Create sub-groups for automation opportunities](../task/creating-subgroups-for-automation-opportunities.md) for detailed steps to create sub-groups.

