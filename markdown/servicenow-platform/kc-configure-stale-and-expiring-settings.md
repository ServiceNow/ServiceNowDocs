---
title: Configure stale and expiring articles notification settings
description: Configure the system properties that define when the articles in a knowledge base can be flagged as stale or expiring.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/servicenow-platform/kc-configure-stale-and-expiring-settings.html
release: brazil
topic_type: task
last_updated: "2026-09-10"
reading_time_minutes: 1
breadcrumb: [Configuring Knowledge Center, Knowledge Center, Manage content capabilities, Extend ServiceNow AI Platform capabilities]
---

# Configure stale and expiring articles notification settings

Configure the system properties that define when the articles in a knowledge base can be flagged as stale or expiring.

## Before you begin

Role required: knowledge admin

Access to the **Knowledge Management Properties** in the Knowledge Center.

## About this task

Configure the thresholds for stale and expiring article notifications in your instance. The default settings identify articles as stale after 365 days and warn about expiring articles 30 days before their Valid To date. You can adjust these values to match your content life cycle and review schedules.

The articles are evaluated using these new threshold values only when Article optimization jobs run for script-based scans.

## Procedure

1.  Navigate to **All** &gt; **Knowledge Center** &gt; **Configurations** &gt; **Knowledge management properties**.

2.  Open the **Article Optimization Properties** section and locate the two properties.

    The first property,**Specify the number of days after publishing**, defines the number of days an article can exist without any updates, before it is flagged as stale. Default value is 365 days. For example, changing this to 180 days identifies articles that have not been updated in 6 months as stale.

    The second property, **Specify the number of days before expiration**, defines the number of days before an article's validity expires, when it can be flagged as expiring. Default value is 30 days. For example, changing this to 60 days alerts you two months before an article expires.

3.  Enter the number of days for each property based on your content review schedule.

    Consider your content update frequency and governance policies when setting these values. More frequent review \(lower day count\) requires more active maintenance, while less frequent review \(higher day count\) may result in stale articles remaining visible to users longer.

4.  Select **Save** to apply your changes.


## Result

The stale and expiring article notification thresholds are updated. All published articles are now evaluated using the new threshold values. You can now see stale and expiring article notifications based on these configured values.

**Related topics**  


[Review stale and expiring articles](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/servicenow-platform/kc-review-stale-expiring-articles.md)

