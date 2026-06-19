---
title: DevOps Retry Policy
description: Enable the DevOps Custom HTTP Retry Policy for most tool communication from ServiceNow flows to automatically retry failed requests when a step encounters an intermittent issue, such as a network failure or request rate limit.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/it-service-management/devops-change-velocity/devops-retry-policy.html
release: australia
product: DevOps Change Velocity
classification: devops-change-velocity
topic_type: concept
last_updated: "2026-03-12"
reading_time_minutes: 1
breadcrumb: [Manage, DevOps Change Velocity, IT Service Management]
---

# DevOps Retry Policy

Enable the DevOps Custom HTTP Retry Policy for most tool communication from ServiceNow flows to automatically retry failed requests when a step encounters an intermittent issue, such as a network failure or request rate limit.

You can navigate to the action in **Flow Designer &gt; Designer &gt; Actions** and in the REST step, select **Enable Retry Policy**. For the DevOps Custom HTTP Retry Policy to take effect, override the default policy for the alias and select the DevOps retry policy.

To customize the retry configuration, access the DevOps Custom HTTP Retry Policy settings in **IntegrationHub &gt; Retry Policy**.

**Parent Topic:**[Managing DevOps Change Velocity](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/it-service-management/devops-change-velocity/using-devops-change-velocity.md)

