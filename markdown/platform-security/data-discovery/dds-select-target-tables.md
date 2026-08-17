---
title: Select target tables
description: Target tables are only used when defining real time anonymization policies. They are the basis for which users can select tables and columns in the policy creation process.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/platform-security/data-discovery/dds-select-target-tables.html
release: australia
product: Data Discovery
classification: data-discovery
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 1
breadcrumb: [Data Discovery sources, Data Discovery Store, Data Discovery, Platform Privacy]
---

# Select target tables

Target tables are only used when defining real time anonymization policies. They are the basis for which users can select tables and columns in the policy creation process.

## Before you begin

Role required: discovery.admin

## Procedure

1.  Navigate to **All** &gt; **Data Discovery** &gt; **Sources**.

2.  Select **Target Tables** in the navigation pane.

3.  Select the **Edit** button.

4.  Check the tables to target, they will show in the right side of the pop-up.

    **Note:** Target tables will scan all columns, unless specified otherwise [in policy](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/platform-security/data-discovery/dds-new-policy.md).

5.  Select the **Save** button.


## Result

Selected tables will now be targeted by [scheduled discovery jobs](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/platform-security/data-discovery/dds-scheduled-discovery.md).

