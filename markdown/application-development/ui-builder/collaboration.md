---
title: Collaborate with other UI Builder developers
description: UI Builder provides real-time collaboration tools and user presence indicators for more efficient and intuitive UI development.Track and compare changes between different versions of a page when collaborating with other page builders.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/zurich/application-development/ui-builder/collaboration.html
release: zurich
product: UI Builder
classification: ui-builder
topic_type: concept
last_updated: "2025-07-31"
reading_time_minutes: 1
breadcrumb: [Working in UI Builder, UI Builder, Builder library, Developing your application, Building applications]
---

# Collaborate with other UI Builder developers

UI Builder provides real-time collaboration tools and user presence indicators for more efficient and intuitive UI development.

UI Builder lets you see who is online and working on the same page in an experience.

The avatars of other developers appear in the UI Builder header next to the undo button. A dot on the avatar of the user represents online status.

-   Green dot if the user is currently working on the page
-   No dot if the user is not logged in

\[Omitted image "collaboration-avatar-header.png"\] Alt text: Arrow pointing to a users avatar in the ui builder header.

A banner will appear asking you to reload the page to view the latest version if changes are made by other users while you are editing a page.

\[Omitted image "collaboration-outdated-banner.png"\] Alt text: Red banner informing the user that the page has been updated and needs to be reloaded to view the latest version.

If you have made changes at the same time as another user you will be prompted to **Overwrite and save** your changes to proceed with previewing the page.

\[Omitted image "collaboration-overwrite.png"\] Alt text: Modal that asks if you want to overwrite and save the changes you made in UI Builder.

**Parent Topic:**[Working in UI Builder](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/application-development/ui-builder/using-ui-builder.md)

## Find and compare page changes

Track and compare changes between different versions of a page when collaborating with other page builders.

### Before you begin

Role required: ui\_builder\_admin

### Procedure

1.  Navigate to **All** &gt; **Now Experience Framework** &gt; **UI Builder**.

2.  Open the experience that contains the page where you want to compare changes.

3.  Select the page with the changes you want to compare.

4.  Select the menu icon.

5.  Select **Compare versions**.

    \[Omitted image "code-comparison-menu-option.png"\] Alt text: Arrow pointing to the compare versions option in the UI Builder menu.

    The **Version comparison** drawer opens.

    \[Omitted image "code-comparison-compare-drawer.png"\] Alt text: UI Builder version comparison drawer showing the changes made since a page was last saved.

6.  Review changes by selecting an item that displays one of the following:

    -   Added
    -   Modified
    -   Moved
    -   Deleted

