---
title: Customize the timeline page span style
description: The Timeline Page Span Styles related list allows you to define conditional span styles.
locale: en-US
release: xanadu
product: Time Configuration
classification: time-configuration
topic_type: task
last_updated: "2024-08-01"
reading_time_minutes: 1
breadcrumb: [Timeline pages, Viewing record information over time, Time configuration references, Time configuration, Configure core features, Administer the ServiceNow AI Platform]
---

# Customize the timeline page span style

The Timeline Page Span Styles related list allows you to define conditional span styles.

## Procedure

1.  Navigate to **All** &gt; **System UI** &gt; **Timeline Pages**.

2.  Open the timeline page for which you want to define the span style.

3.  Go to the Timeline Page Span Styles related list and click **New**.

4.  Fill in the form and click **Submit**.

    |Field|Description|
    |-----|-----------|
    |Condition|[Condition Builder](https://www.servicenow.com/docs/access?context=c_ConditionBuilder&version=xanadu&pubname=xanadu-platform-user-interface&ft:locale=en-US) that filters the results that appear in the timeline.|
    |Label color|Color for the text under each span.|
    |Label decoration|Character style for the text under each span: **Bold**, **Italic**, **Underline**, or **Line-through**.|
    |Order|Number to determine the sequence in which the style conditions are evaluated. Style conditions with a lower order are evaluated first.|
    |Span color|Color of each span.|
    |Timeline page|Timeline page to which the span style applies. By default, the span applies to the current timeline.|


**Parent Topic:**[Timeline pages](../concept/c_TimelinePages.md)

