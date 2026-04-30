---
title: Connect overlay
description: The Connect overlay appears over the standard user interface. It consists of the Connect sidebar, which is the primary interface for Connect Chat and Connect Support, and any Connect mini windows that are open. Each mini window contains a header, a conversation area, and a message field.The Connect sidebar is the primary interface for Connect Chat and Connect Support. It lists your conversations and provides access to create conversations.When you open a Connect Chat or Connect Support conversation in the Connect overlay, it opens in a Connect mini window. Each mini window contains a header, a conversation area, and a message field.
locale: en-US
release: yokohama
product: Connect
classification: connect
topic_type: concept
last_updated: "2025-01-30"
reading_time_minutes: 3
breadcrumb: [Connect interface, Connect, ServiceNow AI Platform Additional Capabilities, Extend ServiceNow AI Platform capabilities]
---

# Connect overlay

The Connect overlay appears over the standard user interface. It consists of the Connect sidebar, which is the primary interface for Connect Chat and Connect Support, and any Connect mini windows that are open. Each mini window contains a header, a conversation area, and a message field.

![Connect overlay](../image/ConnectOverlay.png "Connect overlay")

**Note:** An administrator can [disable](../task/t_DisableTheCollaborationOverlay.md) the Connect overlay so users can only use the Connect workspace, a full-screen interface with additional Connect tools.

## Connect sidebar

The Connect sidebar is the primary interface for Connect Chat and Connect Support. It lists your conversations and provides access to create conversations.

The sidebar is collapsed by default. Click the toggle Connect sidebar icon \(![Toggle Connect sidebar icon](../image/IconUI16ToggleConnectSidebar.png)\) in the banner frame to expand or collapse the sidebar, which appears on the right edge of the interface.

### Connect Chat

The chat view of the sidebar is available to all users. If Connect Support is enabled, users must click the chat tab of the sidebar, which is represented by a speech bubble icon. If Connect Support is not enabled, there are no tabs in the sidebar and the chat view displays by default.

The chat view of the sidebar lists all your current Connect Chat conversations. It also contains a filter tool and a button to create conversations.

![The chat tab of the Connect sidebar displays the Connect Chat view](../image/ConnectSidebarChatTab.png "Chat view of the Connect sidebar")

If you have unread messages in a conversation, a number appears by the conversation in the sidebar. Point to a conversation and click the **x** icon to remove the conversation from the sidebar.

### Connect Support

The support view of the sidebar is available when Connect Support is activated. The support view is visible only to users who are agents for at least one support queue. Users must click the support tab of the sidebar, which is represented by a headset icon.

The support view displays **Queues** to which you belong. It also displays your open support conversations under **Cases**.

![The support tab of the Connect sidebar displays the Connect Support view](../image/ConnectSidebarSupportTab.png "Support view of the Connect sidebar")

If you have unread messages in a conversation, a number appears by the conversation in the sidebar.

## Connect mini windows

When you open a Connect Chat or Connect Support conversation in the Connect overlay, it opens in a Connect mini window. Each mini window contains a header, a conversation area, and a message field.

Several icons appear in the mini window header and by the message field.

**Note:** The icons you see for each conversation depend on the conversation type and other conditions.

|Icon|Name|Description|
|----|----|-----------|
|![Add user icon](../image/IconAddUser.png)|Add user|Add a user to the conversation. This icon is visible for group and record conversations only. Administrators can enable this icon for Connect Support conversations.|
|![View document icon](../image/IconViewDocument.png)|View document|View the record associated with the conversation. This icon is visible for record and support conversations only.|
|![New window icon](../image/IconNewWindow.png)|New window|Open the conversation in the Connect workspace, a full-screen window with additional Connect tools.|
|![Collapse/Expand window icon](../image/IconCollapseExpandWindow.png)|Collapse/Expand conversation|Hide or show the conversation. Alternatively, click anywhere in the mini window header to the left of the icons.|
|![Close window icon](../image/IconCloseWindow.png)|Close window|Close the mini window. The conversation remains in the Connect sidebar and the history is preserved when you reopen the conversation. You can also close a mini window by pressing the Escape key.|
|![Connect action menu icon](../image/IconMenu.png)|Connect actions|Open the Connect actions menu, which contains options like **Transfer** and **Create Incident**. This icon is visible only when Connect actions are available for the conversation. By default, this icon is visible for support conversations only. Administrators can add options to this menu by creating [Connect actions](../task/t_AdministerConnectActions.md).|
|![Message type icon](../image/IconMessageType.png)|Message type|Choose whether messages are added to the associated record as comments or work notes. This icon is visible only for record and support conversations.|
|![Attach file icon](../image/IconAttach.png)|Attach file|Attach and send a file. Select one or more files and click Open. You can also add an attachment by dragging and dropping it directly in the conversation.|

