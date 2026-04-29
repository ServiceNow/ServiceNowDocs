---
title: Set up domain separation for Enterprise Architecture users
description: Enterprise Architecture supports domain separation for managed service providers \(MSPs\) to protect the sensitive data of each customer. The protection also ensures inability to view business application data of one customer by another customer and also secures the data within the domain.
locale: en-US
release: australia
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 1
breadcrumb: [Configuring Enterprise Architecture \(formerly Application Portfolio Management\), Enterprise Architecture \(formerly Application Portfolio Management\), Enterprise Architecture \(formerly Application Portfolio Management\)]
---

# Set up domain separation for Enterprise Architecture users

Enterprise Architecture supports domain separation for managed service providers \(MSPs\) to protect the sensitive data of each customer. The protection also ensures inability to view business application data of one customer by another customer and also secures the data within the domain.

## Before you begin

Role required: admin

## About this task

## Procedure

1.  Install the Domain Support – Domain Extensions Installer system plugin to enable the domain separation feature forEnterprise Architecture.

2.  Create an administrator role at each domain level.

    The administrator can only configure and run the scheduled jobs.

3.  Create all your application portfolio data entities in the domain, specific to the enterprise, and not at the global level.

4.  Create indicators at the domain level.

    Do not create them at the global level and reuse the indicators for every customer under the parent level. Data is not visible at the global level.

5.  Create user groups and assign roles to users at the domain level, so that they can view only the data of the enterprise they belong to.

6.  Execute jobs for domain separated data.

    You can execute scheduled jobs, certification schedules, and assessments of indicators and scores at the domain level using the Run as role. Configure the Scheduled Script Execution form layout to add the **Run as** field from the Context menu.


**Parent Topic:**[Configuring Enterprise Architecture \(formerly Application Portfolio Management\)](../concept/configure-apm.md)

