---
title: Tool throttling
description: In DevOps Change Velocity, when a tool is throttled, processing of new events is delayed until the throttling expires and the tool status changes to Throttled. This is available for Azure DevOps, GitHub, and GitLab.
locale: en-US
release: yokohama
product: DevOps Change Velocity
classification: devops-change-velocity
topic_type: reference
last_updated: "2025-07-31"
reading_time_minutes: 1
breadcrumb: [Manage, DevOps Change Velocity, IT Service Management]
---

# Tool throttling

In DevOps Change Velocity, when a tool is throttled, processing of new events is delayed until the throttling expires and the tool status changes to **Throttled**. This is available for Azure DevOps, GitHub, and GitLab.

When the tool is throttled, you will receive an error message.![Error message for throttled tools.](../image/rate-limit-01.png)

**Throttled status**

Throttled status means that the tool is not allowing API requests to get data because it has reached or exceeded a certain usage limit. API response has a rate limit or too many request errors. In that case, DevOps tool status is changed to **Throttled**.

**Why does this happen**

Some tools limit the number of API requests that can be made within a specific amount of time. This limit helps prevent abuse and denial-of-service attacks, and ensures that the API remains available for all users.

When this happens, the DevOps tool status is changed to **Throttled** and further inbound events aren’t processed until the rate limit imposed by the tool is removed. Till that time, the inbound events will be in the **Deferred** state. After the throttle expires, processing of events resumes.

**How to reset the throttle**

Generally, the tool API provides the information about how long the rate limit will be imposed. This indicates the throttle reset time. This information is used to resume API requests for that tool, if there are any pending inbound events or discover or historical import requests.

If a tool doesn't provide the throttle reset time, the default value, which is 15 minutes is applied. The default value can be changed using the property **Default throttle reset time in minutes from current time** \(sn\_devops.throttle.reset.time.default\), from the DevOps properties page.

**Where to check for the throttled status and reset status**

Tool Connection Status \(sn\_devops\_tool\_connection\_status\) table contains tool throttling related information. It has columns like tool, throttle reset time, throttle active, which indicates which tool is under throttle, when this throttle will be reset, and whether the throttle is active or not.![Tool connection status table.](../image/rate-limit-02.png)

REST\_RATE\_LIMIT\_ERROR will be logged in DevOps error logs. Also, the tool under throttle will have **Throttled** status.

**Parent Topic:**[Managing DevOps Change Velocity](../concept/using-devops-change-velocity.md)

