---
title: Enable tiny URL support
description: The default URLs by which the system renders pages may exceed the character limit of some browsers, resulting in an error message. You can enable tiny URL support, which generates shortened internal URLs, to help prevent this error.
locale: en-US
release: zurich
topic_type: task
last_updated: "2025-07-31"
reading_time_minutes: 1
breadcrumb: [Navigate to a record or module using a URL, Forms in the classic environment, Working in the classic environment, Working in Core UI, Configure UIs and portals, Configure user experiences]
---

# Enable tiny URL support

The default URLs by which the system renders pages may exceed the character limit of some browsers, resulting in an error message. You can enable tiny URL support, which generates shortened internal URLs, to help prevent this error.

## Before you begin

Role required: admin

## About this task

The Tiny URL Support plugin is activated and enabled automatically. Confirm that this plugin is enabled if you receive a failure to open page error during routine operations in the ServiceNow AI Platform.

**Note:** The system doesn’t convert all URLs to tiny URLs. Only some URLs the system generates as redirects are converted. For example, the URL that the browser generates when a user opens a record isn’t converted to a tiny URL.

## Procedure

1.  Navigate to **All** &gt; **System Properties** &gt; **System**.

2.  Select the **Use tiny URLs when a redirect URL becomes too large. This ensures that URLs that are too large for IE \(greater than 2083\) are not used. Instead, they are converted to a tiny URL to work around the IE issue.** \(**glide.use\_tiny\_urls** property\).

3.  Update the value in the **Minimum length of a redirect URL that is turned into a tiny URL \(default=1024\)** \(**glide.tiny\_url\_min\_length** property\), if desired.

4.  Select **Save**.


**Parent Topic:**[Navigate to a record or module using a URL](navigate-using-url.md)

