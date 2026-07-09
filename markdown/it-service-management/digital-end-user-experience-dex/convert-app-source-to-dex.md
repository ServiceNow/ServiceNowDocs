---
title: Convert an application source to DEX
description: Convert a Visibility Content application to DEX monitoring. After conversion, the application is managed in the Application and Device Health system.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/it-service-management/digital-end-user-experience-dex/convert-app-source-to-dex.html
release: australia
product: Digital End-User Experience \(DEX\)
classification: digital-end-user-experience-dex
topic_type: task
last_updated: "2026-06-25"
reading_time_minutes: 1
keywords: [convert application source, Visibility Content, DEX migration, sn\_acc\_vis\_content\_application]
breadcrumb: [Advanced configuration, Configure, Digital End-User Experience, IT Service Management]
---

# Convert an application source to DEX

Convert a Visibility Content application to DEX monitoring. After conversion, the application is managed in the Application and Device Health system.

## Before you begin

Role required: sn\_dex.admin

Before you convert an application source, verify that the application record has a **Service** field value. The conversion is blocked if the **Service** field is empty.

## About this task

**Note:** After you convert an application to be monitored by DEX, you can't convert it back.

## Procedure

1.  Navigate to **All** and search for `sn_acc_vis_content_application.list`.

2.  Select the information icon next to the application you're converting.

    **Note:** The **Source** field on the record must show `sn_acc_vis_content`. If the source is already set to `sn_dex`, the button does not appear.

3.  Verify that the **Service** field is populated.

    If the **Service** field is empty, select a service before continuing. The conversion fails if no service is selected.

4.  Select **Convert to DEX app**.

    If any validation fails, an error message describes the issue and the source field is not updated.


## Result

The Source field is updated to `sn_dex`. The application is now managed by DEX and visible in DEX Self-service application queries and monitoring views.

**Note:** After conversion, the application counts toward the DEX monitored application limit \(default: 200 applications\). The limit is controlled by the **sn\_dex.max\_monitored\_apps** system property.

## What to do next

After converting the application source:

-   Confirm that the application appears in the DEX Application Management view. See [DEX application monitoring](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/it-service-management/digital-end-user-experience-dex/dex-application-monitoring.md).
-   Enable performance or compliance monitoring on the application record. See [Enable application monitoring](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/it-service-management/digital-end-user-experience-dex/enable-app-monitor.md).

**Parent Topic:**[Advanced configuration](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/it-service-management/digital-end-user-experience-dex/dex-advanced-configuration.md)

