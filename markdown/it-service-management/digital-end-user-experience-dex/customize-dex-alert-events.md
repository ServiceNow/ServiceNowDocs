---
title: Customize DEX alert events
description: Apply your organization's own event processing rules, such as enrichment or routing, by transforming DEX metric rule events with a custom script before they're processed.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/it-service-management/digital-end-user-experience-dex/customize-dex-alert-events.html
release: brazil
product: Digital End-User Experience \(DEX\)
classification: digital-end-user-experience-dex
topic_type: task
last_updated: "2026-09-23"
reading_time_minutes: 1
keywords: [customize dex alert events, metric rule event extension, DEXMetricRuleEventExtension, extension point, transform event, event enrichment, event routing, read-only event properties]
breadcrumb: [Managing alert rules, Configure, Digital End-User Experience, IT Service Management]
---

# Customize DEX alert events

Apply your organization's own event processing rules, such as enrichment or routing, by transforming DEX metric rule events with a custom script before they're processed.

## Before you begin

Role required: sn\_dex.admin

The Application and Device Health plugin \(com.sn\_dex\) version 5.3.0 or later must be installed.

## About this task

By default, DEX processes metric rule events through a fixed pipeline for alerts, proactive engagement, and remedial actions. If your organization has its own event processing rules, you can use the sn\_dex.DEXMetricRuleEventExtension extension point to modify each event before DEX processes it. For example, you can enrich events with extra data or change how they're routed.

You customize events by creating a script include that implements a `transform(event)` method, and then registering that script include as an implementation of the extension point.

You can't customize the following event properties. They're read-only because DEX alert processing depends on them.

-   `severity`
-   `message_key`
-   `time_of_event`
-   `source`
-   `resource`
-   `classification`
-   `type`
-   `metric_name`

## Procedure

1.  Navigate to **All** &gt; **System Definition** &gt; **Script Includes** and select **New**.

2.  In the **Name** field, enter a name for your customization script.

    The name must match the `type` value in your script. The example in the next step uses `TestMetricRuleExtensionImp`.

3.  In the **Script** field, define a `transform(event)` method that modifies the event and returns it.

    Change only properties that aren't in the read-only list. The following example returns the event unchanged.Add your enrichment or routing logic before the `return` statement.

    ```
    var TestMetricRuleExtensionImp = Class.create();
    TestMetricRuleExtensionImp.prototype = {
        initialize: function() {
        },
    
        transform : function(event) {
            return event;
        },
    
        type: 'TestMetricRuleExtensionImp'
    };
    ```

4.  Select **Submit**.

5.  Create an extension instance for the sn\_dex.DEXMetricRuleEventExtension extension point.

    1.  In the **Point** field, enter `sn_dex.DEXMetricRuleEventExtension`.

    2.  In the **Class** field, select the script include you created.

    3.  In the **Order** field, enter the processing order for this implementation.

    4.  Select the **Active** check box.

    5.  Select **Submit**.


## Result

DEX runs your `transform(event)` method on metric rule events before it processes them for alerts.

## What to do next

For information about the rules that generate these events, see [Creating a metric rule](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/it-service-management/digital-end-user-experience-dex/create-metric-rules.md).

