---
title: Virtual Agent Designer user input and bot response controls in Microsoft Teams
description: The Virtual Agent Designer user input and bot response controls for creating conversation topics are supported in Microsoft Teams conversations, including the table bot response, the card control that can display images, and the image bot response controls.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/conversational-interfaces/virtual-agent/va-designer-bot-controls.html
release: australia
product: Virtual Agent
classification: virtual-agent
topic_type: concept
last_updated: "2026-03-12"
reading_time_minutes: 2
breadcrumb: [VA feature support in Teams conversations, Conversational Integration with Microsoft Teams, Integrate VA with messaging apps, Integrate VA with other channels, Virtual Agent, Conversational Interfaces]
---

# Virtual Agent Designer user input and bot response controls in Microsoft Teams

The Virtual Agent Designer user input and bot response controls for creating conversation topics are supported in Microsoft Teams conversations, including the table bot response, the card control that can display images, and the image bot response controls.

Starting with Version 2.0.0, the updated card and new video bot response controls are supported in Microsoft Teams conversations. The video control displays a thumbnail image of the video that users select to open the video in their preferred web browser.

For more information about user input controls and bot responses, see [Assistant Designer user input controls](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/conversational-interfaces/virtual-agent/va-user-inputs.md) and [Assistant Designer bot responses](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/conversational-interfaces/virtual-agent/va-bot-responses.md), respectively.

Starting with Version 3.0.10, to improve the bot performance and enable a better conversational experience with Virtual Agent on Microsoft Teams, the non-card bot response controls such as text, links, and date cards are converted into adaptive cards.

As part of converting all controls to adaptive cards, the content displayed on notifications received through bot responses is customized. The Microsoft Teams bot displays a preview of the notification content on the card, such as the message content, card title, or description, where applicable.

\[Omitted image "notification-title-msteams.png"\] Alt text: In Microsoft Teams, this notification shows the title "New Date/Time" and a date/time picker to schedule an appointment. When done, the user selects the Submit button.

Starting with Version 3.0.10, during a conversation with the Microsoft Teams bot, you can search for a particular choice from the list using the drop-down picker controls.

\[Omitted image "msteams-type-head-option.png"\] Alt text: Start typing in the choice list to find the correct response. For example, start typing "s" to find the "Software" choice.

Starting from Version 4.1.0, you have the option to turn off the confirmation banner that appears when you send a response to Virtual Agent in Microsoft Teams conversation.

Set the **sn\_va\_teams.hide\_teams\_response\_message** system property value to **true** to turn off the confirmation banner \(by default the value of the system property is set to **false**\).

**Parent Topic:**[Virtual Agent feature support in Microsoft Teams conversations](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/conversational-interfaces/virtual-agent/va-teams-other-features.md)

