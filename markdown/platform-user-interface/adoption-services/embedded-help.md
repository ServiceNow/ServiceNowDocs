---
title: Embedded Help
description: Embedded help provides targeted help content to a user in a UI page, based on their role. Some embedded help content comes with the base instance. Your organization can add or replace embedded help content.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/platform-user-interface/adoption-services/embedded-help.html
release: australia
product: Adoption Services
classification: adoption-services
topic_type: concept
last_updated: "2026-03-12"
reading_time_minutes: 2
breadcrumb: [In-product help, Adoption services, Configure user experiences]
---

# Embedded Help

Embedded help provides targeted help content to a user in a UI page, based on their role. Some embedded help content comes with the base instance. Your organization can add or replace embedded help content.

## Overview

**Note:** Required: Embedded help is only available in Core UI. For configurable workspaces, use [Help Center](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/platform-user-interface/adoption-services/help-center.md).

The Embedded Help plugin \(com.glide.embedded\_help\) is active by default for all new and upgraded instances. Embedded help content appears in the right sidebar when the user clicks the help icon. If embedded help exists for the current UI page, the help icon has an indicator \(\[Omitted image "icon-embedded-help-available.png"\] Alt text: Embedded help indicator on help icon\).

\[Omitted image "embedded-help-catalog-task.png"\] Alt text: Catalog task page with embedded help

If there is no embedded help for a list or form, the sidebar displays links to the User Guide and the documentation site search. Click **Search Documentation** to search for documentation about that feature.

Users with the embedded\_help\_admin or admin role can add help to the page. They can also edit custom content that appears for a page. The following image shows what the admin sees when there is no help article, and how to open an existing article. If you want to edit base system help content, follow the steps in [Add custom Embedded Help from a copy](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/platform-user-interface/adoption-services/add-custom-help-copy.md).

\[Omitted image "embedded-help-call-to-action.png"\] Alt text: Add content or edit existing content

Embedded help is displayed based on the user's role. If the content has no associated role, all users see it. If the role is different than admin, users with the specified role and above see the content. For example, content with the itil role appears for itil, itil\_admin, and admin.

## Get started

<table id="table_h5k_wp5_5zb" class="nav-card"><tbody><tr><td>

[Explore\[Omitted image "bus-explore.svg"\] Alt text:Learn about the features and benefits of Embedded Help.](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/platform-user-interface/adoption-services/exploring-embedded-help.md)

</td><td>

[Configure\[Omitted image "bus-sdlc.svg"\] Alt text:Configure the Embedded Help content in your instance.](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/platform-user-interface/adoption-services/configuring-embedded-help.md)

</td><td>

[Reference\[Omitted image "bus-learn.svg"\] Alt text:Review system properties and domain separation information.](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/platform-user-interface/adoption-services/embedded-help-reference.md)

</td></tr></tbody>
</table>## Troubleshoot and get help

-   [Search the Known Error Portal for known error articles](https://support.servicenow.com/kb?id=kb_article_view&sysparm_article=KB0597477)
-   [Contact Customer Service and Support](https://support.servicenow.com/now?draw=case)

