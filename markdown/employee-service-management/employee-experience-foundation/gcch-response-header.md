---
title: Update your Microsoft Teams tenant URL for GCC-H or DoD
description: Configure your Microsoft Teams tenant URL for Government Community Cloud High \(GCC-H\) or US Department of Defense \(DoD\).
locale: en-US
release: australia
product: Employee Experience Foundation
classification: employee-experience-foundation
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 1
breadcrumb: [Integrating Employee Center with Microsoft Teams for GCC-H or DoD, Integrating ServiceNow with Microsoft Teams for GCC-H or DoD, ServiceNow for Microsoft Teams and Microsoft 365, Unified Employee Experience, Employee Service Management]
---

# Update your Microsoft Teams tenant URL for GCC-H or DoD

Configure your Microsoft Teams tenant URL for Government Community Cloud High \(GCC-H\) or US Department of Defense \(DoD\).

## Before you begin

Role required: security\_admin

## Procedure

1.  In the Navigation filter, enter `sys_response_header_list.do`.

2.  In the HTTP Response Headers table, append the appropriate URL in the **Value** field of the following records:

    -   Global
    -   Microsoft Integrations – Core/UI Page: ms\_login
    -   Employee Center Core/Service Portal: Employee Center
    Use the following URLs:

    -   GCC-H: `https://gov.teams.microsoft.us`
    -   DoD: `https://dod.teams.microsoft.us`
3.  Select **Update**.


**Parent Topic:**[Integrating Employee Center with Microsoft Teams for GCC-H or DoD](../concept/ec-teams-integration-gcch.md)

