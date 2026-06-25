---
title: Style sheets
description: Styles sheets are standard Cascading Style Sheets \(CSS\) that define the look and feel of all elements within the interface.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/platform-user-interface/content-management-system/c\_StyleSheets.html
release: australia
product: Content Management System
classification: content-management-system
topic_type: concept
last_updated: "2026-03-12"
reading_time_minutes: 1
breadcrumb: [Style in Content Management, Configure Content Management sites, Content Management System, Configure UIs and portals, Configure user experiences]
---

# Style sheets

Styles sheets are standard Cascading Style Sheets \(CSS\) that define the look and feel of all elements within the interface.

Cascading Style Sheets \(CSS\) can either be internal \(stored in the database\) or external \(hosted on the server\), based on organizational needs. To define an internal style sheet, use standard CSS in the style field. Using external CSS allows the Content Management System to use the same CSS as a corporate website or other online resource.

Use an external style sheet by defining a URL that points to the .cssx file. If you upload a .cssx file to the platform, you can reference the .cssx file using a URL.

Content pages do not reference style sheets directly. To invoke a style sheet, you assign the style sheet to a Theme using the related list on the Theme form.

**Parent Topic:**[Style in Content Management](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/platform-user-interface/content-management-system/c_StyleInContentManagement.md)

**Related topics**  


[Customize a design theme](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/platform-user-interface/content-management-system/t_CreateADesignTheme.md)

