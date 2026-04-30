---
title: Doctypes
description: The view\_content html page template on which all CMS is based defaults to doctype=html.
locale: en-US
release: zurich
product: Content Management System
classification: content-management-system
topic_type: concept
last_updated: "2025-07-31"
reading_time_minutes: 1
breadcrumb: [Style in Content Management, Configure Content Management sites, Content Management System, Configure UIs and portals, Configure user experiences]
---

# Doctypes

The view\_content html page template on which all CMS is based defaults to `doctype=html`.

The code looks like the following HTML source code.

```
<!DOCTYPE HTML>
```

If your CMS site does not render properly, remove the doctype from the page by setting the following property: **glide.html.doctype.pages** = chat\_desktop,live\_feed,live\_feed\_small,navigator,navpage11,image\_browse

The following is the default for this property: **glide.html.doctype.pages** = chat\_desktop,live\_feed,live\_feed\_small,navigator,navpage11,image\_browse,view\_content

Setting this doctype offers these benefits for building new sites:

-   Incorporating common practice: Use a practice that is becoming widely adopted across the Internet and can prevent certain browsers from running in quirks mode.
-   Cleaner CSS and markup: Write more standards-based CSS and markup to promote code sharing.
-   A step towards browser compatibility: Find solutions that work across browsers and avoid browser-specific workarounds.

**Parent Topic:**[Style in Content Management](c_StyleInContentManagement.md)

