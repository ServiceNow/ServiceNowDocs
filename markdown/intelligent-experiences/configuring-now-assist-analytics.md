---
title: Configuring AI Analytics
description: Configure the AI Analytics dashboard to view usage, value, and performance indicators for generative AI features on your instance.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/intelligent-experiences/configuring-now-assist-analytics.html
release: australia
topic_type: concept
last_updated: "2026-03-12"
reading_time_minutes: 1
keywords: [Now Assist Analytics, configuring, GenAI, GenerativeAI, CSM, Customer Service Management]
breadcrumb: [Analyzing AI performance, Exploring AI Admin Hub, AI Admin Hub, Enable AI experiences]
---

# Configuring AI Analytics

Configure the AI Analytics dashboard to view usage, value, and performance indicators for generative AI features on your instance.

## Configuration overview

AI Analytics requires at least one ServiceNow Otto product, for example, ServiceNow Otto for Customer Service Management \(CSM\), to be installed and configured on your instance. See [Installing AI Analytics](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/intelligent-experiences/installing-now-assist-analytics.md) for more information.

The following is an optional configuration task used to map an AI skill to a dashboard.

[Map a skill to a dashboard](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/intelligent-experiences/map-a-skill-to-a-dashboard.md) to view skill usage and performance indicators.

## Domain Separation

AI Analytics supports domain separation only for indicators using the following data collection jobs.

-   \[GenAI Analytics\] Daily Data Collection
-   \[GenAI Analytics\] Historical Data Collection
-   \[Now Assist Analytics\] Daily Data Collection
-   \[Now Assist Analytics\] Historical Data Collection

See [Approaches to Performance Analytics with domain separation](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/now-intelligence/pa-domain-configurations.md) for more information on applying domain separation configuration.

**Note:** Be sure to check the Run as field in the data collection job records has a valid user.

