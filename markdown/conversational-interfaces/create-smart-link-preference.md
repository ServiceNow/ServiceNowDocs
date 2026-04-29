---
title: Create a smart link preference
description: Create smart links to specify where a URL should open. For example, the URL could open in a new browser window, in a new browser tab, in the chat window, or in a pop-up window.
locale: en-US
release: australia
product: Conversational Interfaces
classification: conversational-interfaces
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 3
keywords: [Create, smart, link, preference, chat widget, URL Navigation]
breadcrumb: [URL navigation in Conversational Interfaces, General chat settings, Configuring Conversational Interfaces, Conversational Interfaces Console, Conversational Interfaces]
---

# Create a smart link preference

Create smart links to specify where a URL should open. For example, the URL could open in a new browser window, in a new browser tab, in the chat window, or in a pop-up window.

## Before you begin

Role required: virtual\_agent\_admin or admin

## About this task

If you \(as an admin\) have enabled [URL navigation](../concept/url-navigation-ci.md) on the page, you can specify patterns for where and how the links open in the chat windows. End users see the URL links based on the patterns you've specified.

For example, you can set these URL "smart links" to open in a new browser window, in a new browser tab, in the chat window, or in a pop-up window. If you specify a pop-up window, you can set the size of the window your end users see.

Smart links can be used in chats with live agents.

Error messages display for channels that don't support smart links.

## Procedure

1.  Navigate to **All** &gt; **Conversational Interfaces** &gt; **Settings**.

2.  Under the **System actions** section, select **View All** next to **URL navigation**.

3.  Select the **Target Location** tab.

4.  Select **New**.

5.  On the form, fill in the fields.

<table id="table_hrj_m1m_gtb"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Description

</td><td>

The purpose of the smart link.

</td></tr><tr><td>

Where to open

</td><td>

Where to open the link. Choose one of the following options:-   **New Browser Tab**: Opens the link in a new browser tab.
-   **Load in Place:**: Opens the link in the current location.
-   **Parent**: Opens the link at the highest or parent level.
-   **Popup**: Opens the link in a pop-up window and lets you specify the pop-up window size.
-   **Raise Event**: In the chat widget only, prevents the default select behavior, avoiding a page navigation \(the chat is kept open\).


</td></tr><tr><td>

Order

</td><td>

Number that indicates the order in which smart link preferences run. If there are multiple preferences, the system runs the first smart link preference found, from lowest to highest order.

</td></tr><tr><td>

URL Pattern

</td><td>

URL pattern that uses regular expression quantifiers.If the regular expression is invalid, an error message is shown.

 ![Invalid regular expression message.](../image/invalid-reg-expression.png)

</td></tr><tr><td>

Condition mode

</td><td>

Expression logic to specify a condition for applying the smart link preference.Select either:

-   Simple, or
-   Advanced


</td></tr><tr><td>

Set conditions **Note:** Applies only if you select the Simple condition mode.

</td><td>

If you select the **Simple** condition mode, use the condition builder to add or edit the condition.The condition builder specifies that the smart link is only applicable to links in the Service Portal when they're accessed on the chat widget.

 ![Simple condition builder with the conditions Portal is Service Portal and device type is chat widget.](../../virtual-agent/images/smart-link-condition-builder.png)

 -   **devicetype**: Refers to the channel. In the Australia release, only the chat widget \(**mweb**\) is supported. The mobile chat widget isn't supported currently.
-   **portal**: Represents a specific portal. Specify the portal URL suffix in the condition. Navigate to **All** &gt; **Service Portal** &gt; **Portals** to view portals and their suffixes
-   Select **Set**.


</td></tr><tr><td>

Script**Note:** Applies only if you select the Advanced condition mode.

</td><td>

If you select the **Advanced** condition mode, use the script editor to create or edit a JavaScript condition statement. When the end user selects the link, the component triggers a [Window: message event](https://developer.mozilla.org/en-US/docs/Web/API/Window/message_event). As a developer, if you see the [Window: message event](https://developer.mozilla.org/en-US/docs/Web/API/Window/message_event), you can decide how to handle the navigation. For example: ```
window.addEventListener('message', e => {
    if (e.data.type === 'SMART_LINK_CLICKED') {
    console.log(e.data);
    /**
       {
            type: 'SMART_LINK_CLICKED',
          src: 'https://domain.com/link/src'
       }
    */
  }
});
```

</td></tr></tbody>
</table>6.  Select **Save**.


## What to do next

If you would like to enable smart link preference for Microsoft Teams, you must first [Configure link authentication and opening experience in Microsoft Teams](../../virtual-agent/task/link-opening-authentication-msteams.md) and then [Configure smart links in Microsoft Teams](../../virtual-agent/concept/va-teams-sso.md)

**Parent Topic:**[URL navigation in Conversational Interfaces](../concept/url-navigation-ci.md)

