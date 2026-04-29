---
title: Add shared pages to an experience
description: Add a page from another experience so that users can access shared content without duplicating pages.
locale: en-US
release: australia
product: UI Builder
classification: ui-builder
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 1
breadcrumb: [Use pages across experiences, Manage UI Builder pages and page variants, Working in UI Builder, UI Builder, Builder library, Developing your application, Building applications]
---

# Add shared pages to an experience

Add a page from another experience so that users can access shared content without duplicating pages.

## Before you begin

Role required: ui\_builder\_admin

## About this task

Before adding a shared page to your experience, there must be at least one page configured to be used across experiences.

## Procedure

1.  Navigate to **All** &gt; **Now Experience Framework** &gt; **UI Builder**.

2.  Open an experience to work in or create an experience by selecting **Create** &gt; **Experience**.

    See [Configure how users interact with your applications in UI Builder](../concept/work-experiences.md) for more information on creating experiences.

3.  Select the **+** icon next to **Pages**.

4.  Select the **Advanced** drop-down.

5.  Select **Add a page from another experience**.

6.  Select the page that you want to use from the list.

7.  Select **Proceed to setup**.

8.  Select the variants that you would like to use.

    |Page variant options|Description|
    |--------------------|-----------|
    |**All Variants**|Add all variants of the selected page to your experience.|
    |**Select specific variants to use**|Add specific variants to your experiences of the shared page to your experience.|

9.  Select **Next**.

10. Review the URL created for the shared page.

11. Select **Next**.

12. In the form, fill in the fields to configure when to display the shared page in your experience.

    |Field|Description|
    |-----|-----------|
    |Order of evaluation|The priority number determines the order in which page content from multiple sources is evaluated, with lower numbers taking precedence.|
    |Audiences|Select who can access the shared page.|
    |Conditions|Specify conditions for using shared pages from the source, where the selected variant is determined by the audiences and conditions configured in the source.|
    |Description|Add notes about the configuration.|

13. Select **Complete**.

    The shared page displays in your experience along with a label identifying its source experience.


**Parent Topic:**[Use pages across experiences](../concept/use-across-pages.md)

