---
title: Split.io integration with DevOps Change Velocity
description: Connect to your Split.io instance to manage feature flags requests directly from you ServiceNow instance.
locale: en-US
release: xanadu
product: DevOps Change Velocity
classification: devops-change-velocity
topic_type: concept
last_updated: "2025-07-31"
reading_time_minutes: 1
breadcrumb: [Integrate, DevOps Change Velocity, IT Service Management]
---

# Split.io integration with DevOps Change Velocity

Connect to your Split.io instance to manage feature flags requests directly from you ServiceNow instance.

## Split integration overview

Feature flags are used to turn code off and on in your production environment.

This integration extends the ServiceNow platform to manage the CHG approval process for feature flags and segments of Split. This capability enables managing updates to feature flags from DevOps Change Velocity.

-   Split.io feature flag tool integration support enables discovery of workspaces, environments, segments, and feature flags.
-   Users can set CHG request fields to enable Split.io for CHG control.
-   Upon approval/rejection of a CHG request, the callback URL in Split.io for the split or segment is invoked to resume implementation of the update to the split and segment.

-   **[Onboard Split to DevOps Change Velocity — Classic](../task/create-split-tool-record-devops.md)**  
Create a Split tool record to connect and discover workspaces, environments, segments, and feature flags from the connected Split tool.

**Parent Topic:**[Integrating DevOps Change Velocity with third party tools](integrating-devops-change-with-third-party-tools.md)

