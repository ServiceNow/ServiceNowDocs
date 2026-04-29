---
title: Custom content PDF export limitations
description: When you create custom content to be placed as widgets on dashboards and home pages, you must perform extra tests before you export the content to PDF.
locale: en-US
release: australia
product: Performance Analytics
classification: performance-analytics
topic_type: reference
last_updated: "2026-03-12"
reading_time_minutes: 1
breadcrumb: [Administering dashboards, Responsive dashboards in the Core UI, Reporting, dashboards, and Performance Analytics in the Core UI, Platform Analytics]
---

# Custom content PDF export limitations

When you create custom content to be placed as widgets on dashboards and home pages, you must perform extra tests before you export the content to PDF.

## Outside of ServiceNow support

As with any custom implementations, several actions have limited or no support when they are beyond the control of ServiceNow.

-   Custom content blocks: Content blocks that are not part of the base system or part of a plugin.
-   Custom content blocks: The number of content blocks containing report visualizations may affect export success. Successful export may also be intermittent.
-   Custom interactive filters \(dynamic content blocks\).
-   Custom Iframes, including Iframes that link back to existing UI pages and scripts.
-   Custom widgets: widgets not created by ServiceNow.
-   Custom Global UI scripts: UI scripts that are not part of the base system.
-   Custom UI pages: UI pages that are not part of the base system.
-   Custom script includes: Script includes that are not part of the base system.

PDF export engines do not render pages the same way a browser does. PDF export functionality supports the following web technologies: HTML 4, CSS2, and JavaScript 1.5. Content block developers are responsible for testing their code against PDF export and for adjusting their implementation to these limitations.

