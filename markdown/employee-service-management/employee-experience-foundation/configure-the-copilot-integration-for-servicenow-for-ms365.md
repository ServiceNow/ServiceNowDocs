---
title: Setup Copilot integration for ServiceNow for Microsoft 365
description: Enable co-pilot integration for ServiceNow for Microsoft 365.
locale: en-US
release: zurich
product: Employee Experience Foundation
classification: employee-experience-foundation
topic_type: task
last_updated: "2026-03-03"
reading_time_minutes: 1
breadcrumb: [Setup the Servicenow instance, MS Teams and Microsoft 365, Integrate, ServiceNow for Microsoft Teams and Microsoft 365, Unified Employee Experience, Employee Service Management]
---

# Setup Copilot integration for ServiceNow for Microsoft 365

Enable co-pilot integration for ServiceNow for Microsoft 365.

## Before you begin

Ensure that you have the installed Microsoft Integrations - Core version 5.9.5.

**Important:** This integration is supported in zp7 release only.

Role required: admin

## About this task

After you upgrade to the latest Microsoft Integrations - Core, you must regenerate and re-upload the manifest file to enable the Copilot integration.

## Procedure

1.  Install Microsoft Integrations - Core version 5.9.5 plugin which is the latest.

2.  Regenerate the latest manifest file.

    You must generate a new manifest file and download it. For more information, refer to [Create and download the manifest file for self-configured apps](download-manifest-file-st.md#).

3.  Re-upload the latest manifest file.

    Upload the newly downloaded manifest file. For more information, refer to [Upload manifest file in Microsoft Teams](upload-manifest-ms-teams-st.md).


## Result

The co-pilot integration is complete.

**Parent Topic:**[Setting up the ServiceNow instance for Microsoft Teams integration](../concept/setup-tenants.md)

