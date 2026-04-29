---
title: Create Location filter criteria
description: Use location filter criteria to filter input for users authentication based on the user location.
locale: en-US
release: australia
product: Authentication
classification: authentication
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 1
breadcrumb: [Location Filter, Filter criteria, Adaptive authentication, Authentication, Access Management]
---

# Create Location filter criteria

Use location filter criteria to filter input for users authentication based on the user location.

## Before you begin

Role required: adaptive\_auth\_admin

Plugin required: **Zero Trust - Location Based Access** \(`com.snc.zero_trust_location_access`\).

Property: Enable the Adaptive authentication property.

**Note:** Administrators can only create the policy based on location filters if the location is available for the current user session.

## Procedure

1.  Navigate to **All** &gt; **Adaptive Authentication** &gt; **Filter Criteria** &gt; **Location Filter Criteria**.

2.  Select **New**.

3.  On the form, fill in these fields.

    |Field|Description|
    |-----|-----------|
    |Name|Name to identify the criteria.|
    |Description|Short description of the criteria.|
    |Application|Scope of the application.|

4.  In the **Locations** sections, under the Locations for criteria tab, double-click to **Insert a new row**.

5.  Specify the locations.

    ![Location Filter](../images/apac-filter-criteria.png)

6.  Select **Submit**.


