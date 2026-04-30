---
title: Bulk commits in GitLab
description: Bulk commits are supported with GitLab.
locale: en-US
release: yokohama
product: DevOps Change Velocity
classification: devops-change-velocity
topic_type: concept
last_updated: "2025-07-31"
reading_time_minutes: 1
breadcrumb: [GitLab, Integrate, DevOps Change Velocity, IT Service Management]
---

# Bulk commits in GitLab

Bulk commits are supported with GitLab.

To support large commits, perform these actions:

-   Install the ServiceNow IntegrationHub Action Template - Data Stream \(com.glide.hub.action\_type.datastream\) plugin.
-   For optimal performance, disable flow logging by setting the Flow Designer com.snc.process\_flow.reporting.level property to **Off**.
-   For MID Server settings, view the [MID Server support for Data Stream actions](https://www.servicenow.com/docs/access?context=dsa-on-mid&version=yokohama&pubname=yokohama-integrate-applications&ft:locale=en-US) section.

GitLab code push webhook sends a maximum of 20 commits in a notification. If the number of commits in the push are less than 20, a single inbound event is created and processed in the ServiceNow instance.

If the number of pushed commits are equal or greater than 20, multiple inbound events are created from the original event with each new event containing a batch of 19 commits. The original inbound event is marked as ignored.

Currently, GitLab Data stream action can process up to 10,000 commits in a single push.

**Parent Topic:**[GitLab integration with DevOps Change Velocity](gitlab-integration-dev-ops.md)

