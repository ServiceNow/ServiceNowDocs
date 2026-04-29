---
title: Applications in DevOps Change Velocity
description: In DevOps Change Velocity, an application collects all the up-to-date data that connected tools send about plans, repositories, and pipelines.
locale: en-US
release: australia
product: DevOps Change Velocity
classification: devops-change-velocity
topic_type: concept
last_updated: "2026-03-12"
reading_time_minutes: 1
breadcrumb: [DevOps Change Velocity, IT Service Management]
---

# Applications in DevOps Change Velocity

In DevOps Change Velocity, an application collects all the up-to-date data that connected tools send about plans, repositories, and pipelines.

An application is needed to group plans, repositories, and pipelines together which enable tracking automatically and provide associations for DevOps data such as commits linked to work items. You can link the application with other ServiceNow products, including DevOps Config.

You must create an application to enable traceability for user stories, commits, test results, and more. Associating plans, repositories, and pipelines to an application also enables pipeline modeling, change governance, and metric reporting. In the DevOps Change, this procedure generates a single DevOps application record \(sn\_devops\_app\) that is used by both DevOps and DevOps Config \(if installed\).

When DevOps Config is installed, the DevOps application record is also linked to a CDM application record \(sn\_cdm\_application\). The CSDM application model \(name, owner, manufacturer\) functions as the link between ServiceNow DevOps products.

