---
title: Activate GRC: Performance Analytics Integration
description: The GRC: Performance Analytics Integration plugin provides an integration between Performance Analytics and the Risk Management and Policy and Compliance Management applications. This plugin provides more insight into organizational risk and compliance performance.
locale: en-US
release: zurich
product: GRC: Risk Management Workspace
classification: grc-risk-management-workspace
topic_type: task
last_updated: "2025-07-31"
reading_time_minutes: 1
breadcrumb: [Monitor risks using GRC Performance Analytics Indicators, Use, Risk Management, Governance, Risk, and Compliance]
---

# Activate GRC: Performance Analytics Integration

The GRC: Performance Analytics Integration plugin provides an integration between Performance Analytics and the Risk Management and Policy and Compliance Management applications. This plugin provides more insight into organizational risk and compliance performance.

## Before you begin

Role required: admin

## About this task

This plugin includes demo data and activates related plugins if they are not already active.

## Procedure

1.  Navigate to **All** &gt; **System Applications** &gt; **All Available Applications** &gt; **All**.

2.  Find the plugin using the filter criteria and search bar.

    You can search for the plugin by its name or ID. If you cannot find a plugin, you might have to request it from ServiceNow personnel.

3.  Select **Install** to start the installation process.

    **Note:** When domain separation and delegated Admin are enabled in an instance, the administrative user must be in the **global** domain. Otherwise, the following error appears: `Application installation is unavailable because another operation is running: Plugin Activation for <plugin name>.`

    You will see a message after installation is completed. For information about the components installed with a plugin, see [Find components installed with an application](https://www.servicenow.com/docs/bundle/zurich-platform-administration/page/administer/plugins/task/find-components.html).


## What to do next

After activating the GRC: Performance Analytics Integration plugin on an instance with customized related lists on content \(risk or control objective\) or items \(risk or control\), you may have to manually add the PA Indicator to content relationships and/or the PA indicator to item relationships.

**Parent Topic:**[Monitor risks using GRC Performance Analytics Indicators](../../grc-risk/concept/pa-indicators-risk.md)

**Related topics**  


[List of plugins](activate-grc-pa-prem-integ.md)

