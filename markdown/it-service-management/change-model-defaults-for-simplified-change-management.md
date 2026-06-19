---
title: Change model defaults for Simplified Change Management
description: When you activate the ITSM Change Management Admin Experience plugin \(sn\_itsm\_chg\_admin\), the simplified change models become the active defaults and the classic global models are deactivated.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/it-service-management/change-model-defaults-for-simplified-change-management.html
release: australia
product: IT Service Management
classification: it-service-management
topic_type: concept
last_updated: "2026-06-01"
reading_time_minutes: 1
breadcrumb: [Configure change models, Configuring Simplified Change Management, Configuring the fulfiller experience in Simplified IT Service Management, Configure integrations and ITSM experiences in Simplified IT Service Management, Configure and integrate, Simplified IT Service Management, IT Service Management]
---

# Change model defaults for Simplified Change Management

When you activate the ITSM Change Management Admin Experience plugin \(sn\_itsm\_chg\_admin\), the simplified change models become the active defaults and the classic global models are deactivated.

## What changes when you activate the plugin

Activating the plugin replaces the classic global change models with simplified equivalents as the defaults you see in the change creation page. Each simplified model targets a specific change type, giving you one clear path for every change you create.

|Change model|Before activation|After activation|
|------------|-----------------|----------------|
|Normal \(simplified\)|Inactive|Active default — visible in the change creation page|
|Emergency \(simplified\)|Inactive|Active default — visible in the change creation page|
|Change Registration \(simplified\)|Inactive|Active — visible in the change creation page|
|Global Normal \(classic\)|Active default|Deactivated and hidden, unless you have customized it|
|Global Emergency \(classic\)|Active default|Deactivated and hidden, unless you have customized it|
|Global Change Registration \(classic\)|Active|Deactivated and hidden|
|Standard, Unauthorized, Cloud, Cloud Infrastructure|Active|No change|

**Important:** If you have already modified the classic Global Normal or Global Emergency model, the plugin leaves that model exactly as it is. The simplified models still become the active defaults, so your existing customizations aren't overwritten.

## Required fields on Standard changes

To improve the completeness of Standard change records, the plugin enforces mandatory fields and restricts work note editing.

-   **Required fields**

    Short description, Description, Risk, Impact, Justification, Assignment group, Planned start date, and Planned end date.

-   **Work notes**

    Read-only for anyone without the Change Manager role, keeping the change history trustworthy.


## What stays the same

The following models and behaviors are unaffected by activation:

-   Standard, Unauthorized, Cloud, and Cloud Infrastructure change models retain their current behavior.
-   The simplified Change Registration model continues to work as before.
-   Any classic Global Normal or Emergency model you have customized remains inactive and unchanged.

## Reverting to previous defaults

To restore the change model defaults that were in place before activation, contact ServiceNow Support.

**Note:** Don't adjust these defaults manually, because the models function as an interdependent set.

**Parent Topic:**[Configure change models for Simplified Change Management](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/it-service-management/configure-change-models-scm.md)

