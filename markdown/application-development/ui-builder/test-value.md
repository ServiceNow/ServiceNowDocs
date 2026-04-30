---
title: Test values in a page
description: Add test values to your URL as a way to bring test data into a page.
locale: en-US
release: zurich
product: UI Builder
classification: ui-builder
topic_type: concept
last_updated: "2025-07-31"
reading_time_minutes: 1
breadcrumb: [Manage UI Builder pages and page variants, Working in UI Builder, UI Builder, Builder library, Developing your application, Building applications]
---

# Test values in a page

Add test values to your URL as a way to bring test data into a page.

Use test values to give values for required and optional URL parameters as a way to test your page with actual data.

Test values are important because you can use them to simulate how your page behaves when the page gets its required or optional parameters from the URL. A UI Builder URL is not the same as the URL when you preview your page. So, UI Builder needs a way to simulate what happens to the page during different states of the preview URL.

For example, say that you’re building a record page that displays a form for a single record. For the record page to load, the page must have a &lt;table&gt; and &lt;sysId&gt; in the URL so that it can get and display the proper record. In UI Builder, you must supply test values for the table and sys\_id so that you can see how the page looks when you preview the page.

To get test values to show data, add a data resource, then configure the data resource to bind a record to the test value in the URL. For example, you could add `incident` as a test value.

![Edit test values for URL parameters popup displayed with required and optional parameter fields.](../image/test-values.png)

**Parent Topic:**[Manage UI Builder pages and page variants](work-pages.md)

