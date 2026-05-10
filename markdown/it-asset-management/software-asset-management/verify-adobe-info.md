---
title: Determine and verify Adobe subscription information in your ServiceNow instance
description: Determine the exact software subscription information to be pulled from the Adobe admin center and verify if the complete subscription information is pulled accurately to ServiceNow instance.
locale: en-US
release: australia
product: Software Asset Management
classification: software-asset-management
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 1
breadcrumb: [Integrating with Adobe Cloud, Software Asset Management publisher pack for Adobe, Supported software publisher licenses, Software Asset Management, IT Asset Management]
---

# Determine and verify Adobe subscription information in your ServiceNow instance

Determine the exact software subscription information to be pulled from the Adobe admin center and verify if the complete subscription information is pulled accurately to ServiceNow instance.

## Before you begin

Role required: sam\_admin

## Procedure

1.  Navigate to **License operations** &gt; **User subscription** &gt; **Direct integration profiles**.

2.  Filter with the Adobe Cloud integration profile you created to determine the exact software subscription information to be pulled from Adobe admin center to ServiceNow instance.

    This subscription information includes all subscriptions available on the Adobe admin center.

3.  Verify with the Adobe admin if complete subscription data isn't getting pulled accurately into Software Asset Management.

    After the validation is successful, look for system logs for any possible errors:

    1.  **Enable debug logs and re-run the job**: This action helps in capturing detailed information about the process. For more information, see [Configure outbound logging](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/api-reference/web-services/outbound-logging-configure.md).
    2.  **Check outbound logs for API calls and responses**: If the API response isn't successful, check [Adobe documentation](https://helpx.adobe.com/in/support.html) for the specific error.
    3.  **If the APIs were successful, review system logs**: Look for any technical failures or issues within the code itself.

