---
title: Configuring Proactive Code Check
description: Impact Platform Health features Proactive Code Check that can be activated to perform a code review in your instances.
locale: en-US
release: yokohama
topic_type: concept
last_updated: "2025-02-27"
reading_time_minutes: 1
breadcrumb: [Configuring the Impact Store Application, Impact Store Application, Impact]
---

# Configuring Proactive Code Check

Impact Platform Health features Proactive Code Check that can be activated to perform a code review in your instances.

Proactive Code Check single instance scanning is supported with the ServiceNow Washington DC release and later. Synchronizing between multiple instances and viewing results on the dashboard are features supported with the ServiceNow Yokohama release and later.

## Single instance scanning

Developers can execute Proactive Code Check \(PCC\) on update sets in non-production instances to reduce technical issues from being introduced into production. The Impact Health Store Application is installed as part of the Impact Store App. For additional details on the installation process, see [Configuring the Impact Store Application](configuring-impact-platform.md).

## Multiple instance synchronization

Proactive Code Check allows synchronizing between production and non-production instances and viewing results on the Platform Health dashboard. This functionality requires an initial trust relationship between the production instance and the identified non-production instance.

For details on the configuration, see [Configure the Multi-Instance Framework for Proactive Code Check](configure-multi-instance-framework-proactive-code-review.md).

**Important:** The Impact Store App must be installed on any non-production instance to conduct code checks, as well as in a reporting or production instance.

