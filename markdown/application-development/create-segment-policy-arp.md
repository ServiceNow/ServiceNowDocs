---
title: Create a segment policy
description: Create a segment policy to enable broad access to one or more policy categories without requiring individual policy records for each access attempt.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/application-development/create-segment-policy-arp.html
release: brazil
topic_type: task
last_updated: "2026-09-10"
reading_time_minutes: 2
keywords: [segment policy, wildcard policy, ARP, Application Runtime Policy, add a segment policy]
breadcrumb: [Use, Application Runtime Policy \(ARP\), Developing your application, Building applications]
---

# Create a segment policy

Create a segment policy to enable broad access to one or more policy categories without requiring individual policy records for each access attempt.

## Before you begin

-   You must be in the scope of the application you want to create a segment policy for. For more information about changing application scope, see [Application picker](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/application-development/c_ApplicationPicker.md).
-   The application must be in development.
-   Application Runtime Policy \(ARP\) must be activated in either Tracking or Enforcing mode for the selected application scope.

Role required: arp\_admin or admin.

## About this task

Segment policies provide a way to enable broad categories of allowed access to an application in development. Activating a segment policy for an area suppresses the creation of individual policy records via ARP for that area. If granular visibility into access patterns is needed for certification or review purposes, use individual policy records instead.

Because they provide such broad resource access, only use segment policies when out-of-scope resources called at runtime can't be known during application development.

## Procedure

1.  Navigate to **All** &gt; **System Policies** &gt; **Application Runtime Policy** &gt; **Segment Policies**.

2.  Verify that you're in the correct scope for the application you want to create a segment policy for.

    For more information, see [Application picker](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/application-development/c_ApplicationPicker.md).

3.  Select **New**.

4.  Select the **Active** option to enable segment policy at creation.

5.  In the **Short Description** field, enter a description of the policy.

6.  In the **Wildcard Policies** section, select the categories for which you want to enable broad access.

    |Option|Description|
    |------|-----------|
    |**Network**|Covers external network access.|
    |**Scripting**|Covers cross-scope script access.|
    |**ARL**|Covers application resource limits, including transaction event and scheduled job quotas.|
    |**Record**|Covers cross-scope table access. There are no additional wildcard options for this category.|

7.  Within each selected category, select the Unlock Wildcard icon \[Omitted image "crs-purple-lock.png"\] Alt text:.

8.  Select one or more wildcard options from the drop-down menu to specify sub-categories of unrestricted resource access.

    Select individual wildcards or select all wildcards to cover all subcategories. For more information about wildcard options for each category, see [Wildcard Policies options](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/application-development/wildcard-policy-options.md).

9.  Select **Submit**.


## Result

The segment policy is created and activated. ARP no longer creates individual policy records for access attempts in the selected categories. Existing individual policy records for those categories can be deleted. Application functionality that relies on the covered categories continues to work without per-resource policy approval.

## Creating a segment policy with wildcard options

\[Omitted image "arp-segment-wildcards-xmp.gif"\] Alt text: You must add wildcard options when creating segment policies for network, scripting, and application resource limits.

**Parent Topic:**[Using Application Runtime Policy](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/application-development/using-arp.md)

