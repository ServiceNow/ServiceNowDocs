---
title: Ticket Conversations widget
description: Record of ticket items. Users can use this widget to communicate back and forth with the fulfiller and the receiver. You can use this base system widget as-is in your portal or clone it to suit your own business needs.
locale: en-US
release: australia
product: Service Portal
classification: service-portal
topic_type: concept
last_updated: "2026-03-12"
reading_time_minutes: 1
breadcrumb: [Example widgets, Widget library, Using portal widgets, Configuring Service Portal, Service Portal, Configure UIs and portals, Configure user experiences]
---

# Ticket Conversations widget

Record of ticket items. Users can use this widget to communicate back and forth with the fulfiller and the receiver. You can use this base system widget as-is in your portal or clone it to suit your own business needs.

The Ticket Conversations widget displays journal entries from the activity formatter of the target record. Journal entries are presented in chronological order, with the oldest entries appearing at the bottom of the widget. Entries made by the user that created the record appear on the right side of the center divider. Entries made by other users appear to the left.

The Ticket Conversations widget is intended only for tables that extend task.

Limit the number of journal entries that appears in the ticket conversation widget using the **glide.service\_portal.stream\_entry\_limit** system property. The default number is 100 on a base instance or 500 if the property is not in the System Property \[sys\_properties\] table. Change the number by navigating to **Service Portal** &gt; **Properties**, and enter the new number in the **Maximum number of stream entries displayed in Service Portal** field.

![Ticket Conversations widget](../image/WidgetTicketConversations.png "Ticket Conversations widget")

## Instance options

|Field|Description|
|-----|-----------|
|Use dynamic placeholder|Use a placeholder for journal fields. The default value is false.|
|No readable journal field message|The message that displays when there are no readable journal fields. Forms that have added journal fields may not display in the Ticket Conversation widget.|
|Enter key behavior|The action to perform when pressing the Enter key. The default is to submit the entry. The **System Property** option is based on the value of the **glide.service\_portal.comment.enter\_adds\_newline** system property.|

**Parent Topic:**[Example widgets](sp-example-widgets.md)

**Related topics**  


[Create and edit a page using the Service Portal Designer](../task/t_ConfigureAPage.md#)

[Configure widget instances](c_ConfigureWidgetInstances.md)

[Clone a widget](../task/t_CloneAndEditAWidget.md)

