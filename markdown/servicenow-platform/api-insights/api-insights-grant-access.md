---
title: Manage requests received for API access in API Insights
description: Manage incoming received requests for API access in API Insights.
locale: en-US
release: australia
product: API Insights
classification: api-insights
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 1
breadcrumb: [Manage access requests, API Insights, Configuration Management Database \(CMDB\), Configuration Management, Extend ServiceNow AI Platform capabilities]
---

# Manage requests received for API access in API Insights

Manage incoming received requests for API access in API Insights.

## Before you begin

Role required: sn\_api\_insights\_ws.api\_mgmt\_architect

## Procedure

1.  Navigate to **Workspaces** &gt; **API Insights**.

2.  In the Access requests received section on the Overview tab, select the displayed numeric value.

3.  In the **Requests received** tab, review all incoming requests.

    You can review the details such as API name, requested by, request type, duration, and the reason for the request.

    **Important:** The **View requests** link in the API request reminder email works only if you have the sn\_api\_insights\_ws.api\_mgmt\_architect or sn\_api\_insights\_ws.api\_mgmt\_architect\_admin role and are part of the same group that received the email to view the requests.

4.  Select the check boxes next to the request names to select one or more access requests that you want to process.

5.  Manage the received requests.

    -   Select **Grant access** to approve access to the requested API.
    -   Select **Reject request** to deny access to the requested API.

## Result

A confirmation notification appears, indicating that the API request access flow process was initiated or completed successfully.

