---
title: DevOps Config and DevOps Change Velocity
description: DevOps Change Velocity collects data from all of your DevOps tools, providing visibility across the entire lifecycle of deployment, while DevOps Config manages and validates your DevOps configuration data.
locale: en-US
release: zurich
product: DevOps \(Family\)
classification: devops-family
topic_type: concept
last_updated: "2025-07-31"
reading_time_minutes: 1
breadcrumb: [Explore, DevOps Config, IT Service Management]
---

# DevOps Config and DevOps Change Velocity

DevOps Change Velocity collects data from all of your DevOps tools, providing visibility across the entire lifecycle of deployment, while DevOps Config manages and validates your DevOps configuration data.

**Important:** DevOps Config is now deprecated and no longer supported or available for new activation.

DevOps Change Velocity is a horizontal solution orchestrating on top of all of your separate DevOps tools. DevOps Change Velocity features change acceleration and can pause your pipeline. DevOps Config serves a different purpose.

DevOps Config is a point solution that functions as one of your DevOps tools, managing and testing your configuration data prior to production.

## DevOps Config works better together with DevOps Change Velocity

Use DevOps Config with DevOps Change Velocity to manage and validate configuration data collected by DevOps Change Velocity.

DevOps Change Velocity is an umbrella product that sits on top of your entire release pipeline \(planning, coding, testing, orchestration tools\) as your application supply chain \(value stream map\).

DevOps Config manages, validates, and provides results on how your application and infrastructure are configured, which are the elements instrumented in DevOps Change Velocity.

DevOps Change Velocity and DevOps Config are synced by app object.

With the DevOps Change Velocity change control feature, a change request is created for DevOps Config configuration changes.

In DevOps Change Velocity, navigate to **DevOps** &gt; **Orchestrate** &gt; **Pipeline Change Requests** to view and approve DevOps change requests created by DevOps Config changes. CDM snapshots are listed in the **Config data** related list of the DevOps change request.

![DevOps Config change request](../image/devops-config-change-request.png)

**Parent Topic:**[Exploring DevOps Config](devops-config-getting-started.md)

