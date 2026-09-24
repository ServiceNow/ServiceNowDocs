---
title: Configure Multi-Instance management for AI Control Tower
description: Configuring Multi-Instance management for AI Control Tower.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/australia/intelligent-experiences/ai-control-tower/configure-multi-instance-management-for-aict.html
release: australia
product: AI Control Tower
classification: ai-control-tower
topic_type: task
last_updated: "2026-09-10"
reading_time_minutes: 1
keywords: [multi-instance management, AI governance workspace, instance configuration, manager instance]
breadcrumb: [Configure, AI Control Tower \(legacy\), Enable AI experiences]
---

# Configure Multi-Instance management for AI Control Tower

Configuring Multi-Instance management for AI Control Tower.

## Before you begin

**Note:** The feature is available on Yokohama release onwards.

This feature isn’t supported on Government Community Cloud \(GCC\) and on-premises instances.

Role required: AI Steward \[sn\_ai\_governance.ai\_steward\]

## About this task

**Note:** Make sure the plugin com.glide.mif.mtls is active. If it is not installed, contact Now Support to activate the plugin com.glide.mif.mtls for MIF features.

## Procedure

1.  Log in to the sub-prod instance and navigate to **All** &gt; **Multi-Instance Management** &gt; **Manager Instances**.

    The Manager Instances list view page appears.

2.  Select **New**.

3.  Select the **Application**: AI Control Tower Core.

4.  Select the **Manager Instance**.

    **Note:** The **Approval** field will show Awaiting Manager Confirmation.

5.  Select **Submit**.

6.  Log in to the valid prod instance \(selected in the step 4\) and navigate to Managed Instances.

    A record will appear with the request status in auto-approved state. It gets auto-approved in 5 to 10 minutes.

7.  Navigate to the Managed Instances tab on the Multi-instance Setup page to view all registered managed instances.


## Result

Multi-instance management is configured for the AI Control Tower.

For more information about Trust configuration and Trust configuration management, see [Cross-instance application trust configuration](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/platform-administration/grant-access-v2.md).

For more information about AI asset synchronization process, see [Multi-Instance Setup](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/australia/intelligent-experiences/ai-control-tower/multi-instance-management.md) section under Exploring the AI Control Tower configurations.

