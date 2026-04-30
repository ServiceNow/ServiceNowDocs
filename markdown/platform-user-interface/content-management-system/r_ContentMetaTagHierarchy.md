---
title: Content meta tag hierarchy
description: Page and site level meta tags are included in a content meta tag hierarchy.
locale: en-US
release: yokohama
product: Content Management System
classification: content-management-system
topic_type: reference
last_updated: "2025-01-30"
reading_time_minutes: 1
breadcrumb: [Content Management meta tags, Configure Content Management sites, Content Management System, Configure UIs and portals, Configure user experiences]
---

# Content meta tag hierarchy

Page and site level meta tags are included in a content meta tag hierarchy.

## Site and page level tags

CMS supports page level and site level tags. The system behavior is to show the sum of all page level and site level tags. For example, if you have two tags on the site and one tag on the page, all with different names, you see three tags on the page. Two are from the site and one is from the page. If both the site and the page have a tag of the same name, only the page tag is used.

**Note:** The Content Management System does not support some commonly used meta tags. For example, you cannot use the X-UA-Compatible meta tag, which allows you to specify which version of Internet Explorer a site should be rendered in.

## Example: all tags have unique names

```
 Site Level
Name         Content
breakfast    eggs
lunch        sandwich

Page Level
Name         Content
dinner       steak

Output
Name         Content
breakfast    eggs
lunch        sandwich
dinner       steak
```

## Example: page level tag overrides site level tag

```
Site Level
Name         Content
breakfast    eggs
lunch        sandwich

Page Level
Name         Content
lunch        tacos <--- overrides site level
dinner       steak

Output
Name         Content
breakfast    eggs
lunch        tacos
dinner       steak
```

**Parent Topic:**[Content Management meta tags](../concept/c_ContentManagementMetaTags.md)

