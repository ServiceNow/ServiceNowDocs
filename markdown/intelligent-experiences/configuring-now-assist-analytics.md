---
title: Configuring Now Assist Analytics
description: Configure the dashboard to view skill details.
locale: en-US
release: xanadu
topic_type: concept
last_updated: "2024-11-22"
reading_time_minutes: 1
keywords: [Now Assist Analytics, configuring, GenAI, GenerativeAI, CSM, Customer Service Management]
breadcrumb: [Analyzing Now Assist performance, Now Assist, Enable AI experiences]
---

# Configuring Now Assist Analytics

Configure the dashboard to view skill details.

## Configuration overview

Now Assist Analytics requires at least one Now Assist application, for example, Now Assist for Customer Service Management \(CSM\), to be installed and configured on your instance. See [Install Now Assist plugins](../../now-assist-admin/task/install-now-assist-feature-plugins.md) for more information.

The following is an optional configuration task to map a Now Assist skill to a dashboard.

[Map a skill to a dashboard](map-a-skill-to-a-dashboard.md) to view skill usage and performance indicators.

## Domain Separation

Now Assist Analytics supports domain separation only for indicators using the following data collection jobs.

-   \[GenAI Analytics\] Daily Data Collection
-   \[GenAI Analytics\] Historical Data Collection
-   \[Now Assist Analytics\] Daily Data Collection
-   \[Now Assist Analytics\] Historical Data Collection

See [Approaches to Performance Analytics with domain separation](https://www.servicenow.com/docs/access?context=pa-domain-configurations&version=xanadu&pubname=xanadu-now-intelligence&ft:locale=en-US) for more information on applying domain separation configuration.

**Note:** Be sure to check the Run as field in the data collection job records has a valid user.

