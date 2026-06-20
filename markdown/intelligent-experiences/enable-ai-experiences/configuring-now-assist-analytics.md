---
title: Configuring Now Assist Analytics
description: Configure the dashboard to view skill details.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/xanadu/intelligent-experiences/enable-ai-experiences/configuring-now-assist-analytics.html
release: xanadu
product: Enable AI Experiences
classification: enable-ai-experiences
topic_type: concept
last_updated: "2024-11-22"
reading_time_minutes: 1
keywords: [Now Assist Analytics, configuring, GenAI, GenerativeAI, CSM, Customer Service Management]
breadcrumb: [Analyzing Now Assist performance, Now Assist, Enable AI experiences]
---

# Configuring Now Assist Analytics

Configure the dashboard to view skill details.

## Configuration overview

Now Assist Analytics requires at least one Now Assist application, for example, Now Assist for Customer Service Management \(CSM\), to be installed and configured on your instance. See [Install Now Assist plugins](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/xanadu/markdown/xanadu/intelligent-experiences/enable-ai-experiences/install-now-assist-feature-plugins.md) for more information.

The following is an optional configuration task to map a Now Assist skill to a dashboard.

[Map a skill to a dashboard](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/xanadu/markdown/xanadu/intelligent-experiences/enable-ai-experiences/map-a-skill-to-a-dashboard.md) to view skill usage and performance indicators.

## Domain Separation

Now Assist Analytics supports domain separation only for indicators using the following data collection jobs.

-   \[GenAI Analytics\] Daily Data Collection
-   \[GenAI Analytics\] Historical Data Collection
-   \[Now Assist Analytics\] Daily Data Collection
-   \[Now Assist Analytics\] Historical Data Collection

See  for more information on applying domain separation configuration.

**Note:** Be sure to check the Run as field in the data collection job records has a valid user.

