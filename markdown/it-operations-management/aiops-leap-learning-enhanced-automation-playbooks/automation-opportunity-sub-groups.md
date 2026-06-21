---
title: Automation opportunity sub-groups
description: Large automation opportunities in LEAP can be broken into smaller, more manageable sub-groups to achieve more granular and accurate incident resolution.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/it-operations-management/aiops-leap-learning-enhanced-automation-playbooks/automation-opportunity-sub-groups.html
release: australia
product: AIOps LEAP \(Learning-Enhanced Automation Playbooks\)
classification: aiops-leap-learning-enhanced-automation-playbooks
topic_type: concept
last_updated: "2026-06-21"
reading_time_minutes: 2
keywords: [automation opportunities, LEAP, sub-groups]
breadcrumb: [Automation opportunities, Exploring LEAP, Learning Enhanced Automation Platform \(LEAP\), Now Assist for ITOM, IT Operations Management]
---

# Automation opportunity sub-groups

Large automation opportunities in LEAP can be broken into smaller, more manageable sub-groups to achieve more granular and accurate incident resolution.

Large automation opportunities with over 150 records tend to generate overly lengthy resolution steps that lack precision and focus. These opportunities often represent a collection of related problems and issues that should be subdivided to produce more targeted and relevant solutions.

Breaking them into smaller sub-groups lets users obtain more refined resolutions for recurring issues. The Action Insights panel on the automation opportunity details page offers recommendations to create these sub-groups for opportunities containing large record volumes.

## Sub-grouping example

A large automation opportunity containing 300 password reset incidents might include a mix of VPN password resets, Active Directory account lockouts, and SSO token expiry. While these are all password-related, each requires different resolution steps. LEAP displays suggestions for breaking the automation opportunity into three sub-groups so that each group receives targeted resolution steps — for example, one sub-group with VPN-specific steps, another with AD unlock procedures, and a third with SSO token refresh instructions.

## Automatic reorganization

During scheduled LEAP analysis reruns, clusters are automatically reorganized based on newly observed incident patterns. LEAP preserves existing artifacts and links them to updated automation opportunities rather than overwriting them.

The following table describes how each artifact type is handled during reorganization:

|Artifact|Behavior during rerun|
|--------|---------------------|
|Resolution steps|Appended to the new matching automation opportunity. Users can keep the existing steps or select **Regenerate** to create fresh ones.|
|Playbooks|Remain active and are linked to the new matching automation opportunity. Existing playbook configurations and execution history are preserved.|
|Knowledge base articles|Remain active and retain their association with the automation opportunity.|
|Problem records|Remain active and are linked to the new matching automation opportunity.|

Automation opportunities that no longer have any associated artifacts after reorganization are marked as deactivated. Opportunities that contain resolution steps, playbooks, or other artifacts remain active and are linked to newly identified matching automation opportunities.

For example: An automation opportunity for "email delivery failures" has resolution steps and a playbook created in the previous analysis run. When LEAP reruns the analysis and reorganizes clusters, this opportunity is matched to a new cluster. The existing resolution steps are appended to the new automation opportunity. The user can review the appended steps and decide whether to keep them or regenerate new ones based on the updated cluster data.

## Benefits of sub-grouping

-   Provides more focused and contextual resolution steps
-   Offers more targeted solutions for similar issues
-   Improves incident resolution
-   Enables more effective management of large automation opportunities
-   Supports operational efficiency by reusing prior resolutions where appropriate

For detailed steps, see [Create sub-groups for automation opportunities](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/it-operations-management/aiops-leap-learning-enhanced-automation-playbooks/creating-subgroups-for-automation-opportunities.md).

