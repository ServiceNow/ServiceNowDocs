---
title: Configuring Jira project settings in SPW
description: Configure integration settings for each Jira project before importing issues to ensure accurate and consistent visibility of work in both Strategic Planning Workspace and Jira. These settings such as team association and data mappings define how work items sync between both applications.
locale: en-US
release: australia
product: Strategic Planning
classification: strategic-planning
topic_type: concept
last_updated: "2026-03-12"
reading_time_minutes: 1
breadcrumb: [Configure, SPW Jira Integrations, Strategic Planning, Strategic Portfolio Management]
---

# Configuring Jira project settings in SPW

Configure integration settings for each Jira project before importing issues to ensure accurate and consistent visibility of work in both Strategic Planning Workspace and Jira. These settings such as team association and data mappings define how work items sync between both applications.

For each Jira project, perform the following tasks:

1.  [Associate the Jira project with an EAP team](../task/create-team-integration-settings-for-jira-project-in-spw.md).

    Each Jira project must be associated with an EAP team so that work items brought in from Jira map to the right team in SPW.

2.  [Review default data mapping configurations](../task/review-default-map-config-jira-projects-spw.md).

    Predefined data mapping configurations for Epics, Sprints, and Stories between the two applications are available but if these default mappings don't fit your team's requirements, you can edit them or create new ones. See [Create custom mapping configurations](custom-mapping-configuration-spw-jira.md#).

3.  [Enable bidirectional data sync](../task/enable-bidirectional-sync-spw-jira.md).

    This step ensures updates done in either application are reflected in the other so that data is consistent across.


These steps must be completed for every Jira project that you plan to integrate. Doing so ensures that imported issues sync correctly and enables portfolio managers with real-time visibility into execution.

