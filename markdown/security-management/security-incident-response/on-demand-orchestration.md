---
title: Manage on-demand orchestration
description: During Security Incident Response analysis, a security analyst may want to perform a task that is driven by a security incident workflow. For example, run a process dump on a particular CI. This can be accomplished with on-demand orchestration.
locale: en-US
release: yokohama
product: Security Incident Response
classification: security-incident-response
topic_type: concept
last_updated: "2025-01-30"
reading_time_minutes: 1
breadcrumb: [Managing security incidents and inbound requests, Security Incident Response, Enterprise security case management applications, Security Operations]
---

# Manage on-demand orchestration

During Security Incident Response analysis, a security analyst may want to perform a task that is driven by a security incident workflow. For example, run a process dump on a particular CI. This can be accomplished with on-demand orchestration.

Each registered Security Operations application includes several on-demand orchestrations in the base system. You can define [custom on-demand orchestrations](../task/define-new-on-demand-orchs.md), as needed.

On-demand orchestration can be invoked from a choice list at the bottom of the following lists and forms in Security Incident Response:

-   Security Incident form
-   Security Incident list
-   Security Incident Observables related list
-   Configuration Items related list

**Note:**

-   A property in Security Support Common called **sn\_sec\_cmn.use\_on\_demand\_tbl\_as\_allowed** defines which workflows are available for on-demand execution.
-   If the property is set to **true**, only workflows specified in the On Demand Orchestration \[sn\_sec\_cmn\_on\_demand\_orchestration\] table are available.
-   If the property is set to **false** \(default\), all workflows for applications configured in the [SecOps Application Registry](../task/register-new-secops-apps.md) are available.
-   Depending on the setting of the property, the list of workflows available is tailored to the type of information being analyzed.

