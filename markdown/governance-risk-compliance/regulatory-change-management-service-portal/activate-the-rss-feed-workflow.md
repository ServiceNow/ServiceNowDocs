---
title: Activate and pull RSS feeds
description: Use the Workflow Studio to pull RSS feeds from the defined RSS sources after you activate the workflow. Regular pulling of RSS feeds ensures that you to stay on top of all your regulatory compliance needs. By default, the schedule to pull the feeds runs daily.
locale: en-US
release: yokohama
product: Regulatory Change Management Service Portal
classification: regulatory-change-management-service-portal
topic_type: task
last_updated: "2025-07-31"
reading_time_minutes: 1
breadcrumb: [Set up the RSS feeds infrastructure, Configure, Regulatory Change Management, Governance, Risk, and Compliance]
---

# Activate and pull RSS feeds

Use the Workflow Studio to pull RSS feeds from the defined RSS sources after you activate the workflow. Regular pulling of RSS feeds ensures that you to stay on top of all your regulatory compliance needs. By default, the schedule to pull the feeds runs daily.

## Before you begin

The workflow to pull RSS feeds is built with ServiceNow® Workflow Studio, so make sure you're familiar with the [Flow Designer](https://www.servicenow.com/docs/access?context=flow-designer&version=yokohama&pubname=yokohama-application-development&ft:locale=en-US) basics.

Role required: admin

## About this task

The RCM IT Admin schedules the Pull RSS Feed to Regulatory Change flow to run on a daily, weekly, or monthly basis and sets up the time for the flow.

## Procedure

1.  Navigate to **All** &gt; **Regulatory Change Management** &gt; **RSS Feeds**.

2.  To set up the RSS feed, select **Feed setup**.

3.  From the Feed Setup module, complete the following steps.

    1.  Select the **Pull RSS Feed to Regulatory Change** in the Flow Designer UI page.

    2.  Select **Test** and then **Activate** to activate the flow.


## Result

Upon successful activation of the flow, the system starts scanning the Regulatory Horizon to fetch the latest regulatory updates from the regulator websites.

