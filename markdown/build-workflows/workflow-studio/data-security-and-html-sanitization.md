---
title: Data security and HTML sanitization
description: Playbooks protects against cross-site scripting and code injection by evaluating all string data for HTML markup. The system only preserves HTML markup that is present in its inclusion list. All other HTML markup is removed from string data.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/australia/build-workflows/workflow-studio/data-security-and-html-sanitization.html
release: australia
product: Workflow Studio
classification: workflow-studio
topic_type: reference
last_updated: "2026-11-10"
reading_time_minutes: 1
breadcrumb: [Playbooks reference, Playbooks, Workflow Studio, Build workflows]
---

# Data security and HTML sanitization

Playbooks protects against cross-site scripting and code injection by evaluating all string data for HTML markup. The system only preserves HTML markup that is present in its inclusion list. All other HTML markup is removed from string data.

The inclusion list supports these HTML elements and attributes, which can't be modified.

|HTML element|Included Attributes|
|------------|-------------------|
|a|class, href, target, title|
|abbr|class, title|
|address|class|
|area|alt, class, coords, href, shape|
|article|class|
|aside|class|
|audio|autoplay, class, controls, loop, preload, src|
|b|class|
|bdi|class, dir|
|bdo|class, dir|
|big|class|
|blockquote|cite, class|
|br|class|
|caption|class|
|center|class|
|cite|class|
|code|class|
|col|align, class, span, valign, width|
|colgroup|align, class, span, valign, width|
|dd|class|
|del|class, datetime|
|details|class, open|
|div|class|
|dl|class|
|dt|class|
|em|class|
|emp|class|
|font|class, color, face, size|
|footer|class|
|h1|class|
|h2|class|
|h3|class|
|h4|class|
|h5|class|
|h6|class|
|header|class|
|hr|class|
|html| |
|i|class|
|img|alt, class, height, src, title, width|
|input|aria-label, class, type, value|
|ins|class, datetime|
|li|class|
|mark|class|
|nav|class|
|ol|class|
|p|class|
|pre|class|
|s|class|
|section|class|
|small|class|
|span|class|
|sub|class|
|sup|class|
|svg|class|
|strong|class|
|style| |
|table|align, border, class, valign, width|
|tag|class|
|tbody|align, class, valign|
|td|align, class, colspan, rowspan, valign, width|
|tfoot|align, class, valign|
|th|align, class, colspan, rowspan, valign, width|
|thead|align, class, valign|
|tr|align, class, rowspan, valign|
|tt|class|
|u|class|
|ul|class|
|video|autoplay, class, controls, height, loop, preload, src, width|

