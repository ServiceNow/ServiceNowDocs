---
title: Enable restricted customer access for Business Organizations
description: Run this one-time scheduled job to use the Restricted Customer Access configuration with organization customer criteria under Business Organizations. This procedure is applicable to customers upgrading from a previous release.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/customer-service-management/remove-legacy-contributor-roles-from-loc-mgr-contrib.html
release: brazil
topic_type: task
last_updated: "2026-09-10"
reading_time_minutes: 1
breadcrumb: [Configure Service Model Foundation, Data models, Set up your environment, Configure, Customer Service Management]
---

# Enable restricted customer access for Business Organizations

Run this one-time scheduled job to use the **Restricted Customer Access** configuration with organization customer criteria under Business Organizations. This procedure is applicable to customers upgrading from a previous release.

## Before you begin

Role required: admin

## About this task

For upgrade customers, to let a business organization use [Restricted Customer Access](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/customer-service-management/associate-customers-or-bus-loc-to-so.md) to limit what its Location Manager Contributor users can view, you must first remove that inherited, unrestricted access and replace it with the location-scoped Business Org Account Contributor and Business Org Consumer Contributor roles. Use the **Remove Legacy Roles from Loc Mgr Contrib** scheduled job to make this change.

**Note:** Run this job only if you want to use [Restricted Customer Access](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/customer-service-management/associate-customers-or-bus-loc-to-so.md) configuration with organization criteria under Business Organizations.

Before the Brazil release, Location Manager Contributor users \[sn\_customerservice.svc\_location\_manager\_contributor\] inherited the Account contributor \[sn\_customerservice.account\_contributor\] and Consumer contributor \[sn\_customerservice.consumer\_contributor\] roles. Those two roles give location managers blanket access to all customer regardless of the criteria.

For new customers, this configuration is available by default.

## Procedure

1.  Navigate to the **All** &gt; **System Definitions** &gt; **Scheduled Jobs** module.

2.  Open the **Remove Legacy Roles from Loc Mgr Contrib** job.

3.  Select the **Execute Now** button on the form.

    The job removes the Account contributor and Consumer contributor roles from Location Manager Contributor.

    **Note:** Run this job once. Running it again has no additional effect once the roles have already been swapped.

    Rolling back: If you need to restore the previous behavior, run the **Restore Legacy Roles to Loc Mgr Contrib** scheduled job. This job adds back the Account contributor and Consumer contributor roles to Location Manager Contributor.

    **Note:** After a rollback, business organizations can no longer use Restricted Customer Access to limit the customer access.


