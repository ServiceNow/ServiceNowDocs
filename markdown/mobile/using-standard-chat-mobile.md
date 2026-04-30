---
title: Using standard chat on mobile
description: Standard chat on mobile delivers an intuitive, text-based support experience within a static chat window, enhanced by AI-powered responses and integrated knowledge resources. You can interact with a Virtual Agent to resolve issues, access knowledge articles, and request catalog items all in one place.
locale: en-US
release: zurich
topic_type: concept
last_updated: "2025-07-31"
reading_time_minutes: 5
keywords: [Now Assist, generative AI, Virtual Agent]
breadcrumb: [Using Now Assist, Now Assist for Mobile, Mobile Platform]
---

# Using standard chat on mobile

Standard chat on mobile delivers an intuitive, text-based support experience within a static chat window, enhanced by AI-powered responses and integrated knowledge resources. You can interact with a Virtual Agent to resolve issues, access knowledge articles, and request catalog items all in one place.

## Opening a standard chat

To begin using standard chat, open your organization's support portal or application on your mobile device. Tap the chat option, which is indicated by a Now Assist icon \(![](../image/na-va-icon-home.png)\) on your mobile home page, to bring up the chat window and initiate a conversation.

## Chatting with the Virtual Agent

![standard chat window example with booking travel](../image/na-va-standard-chat.png "Standard chat")

When chatting with the Virtual Agent, you can enter your questions or describe your issue in plain, natural language. The agent will analyze your input and respond with synthesized answers, suggest relevant knowledge articles, and provide you with suggested next steps.

The generated responses display in-line citations to show where information was gathered from, as well as a list of any promoted actions you can take in response to the request. Only the first six lines of the response are shown, with the remaining lines accessible under the **Read More** button.

If your request is unclear or ambiguous, the agent will prompt you with clarifying questions to better understand your needs, ensuring accurate and helpful guidance.

## Suggested actions

![suggestions to check leave balance, block calendar, and notify teammates](../image/na-va-suggested-actions-standard.png "Suggested actions in standard chat")

Suggested actions provide you with next steps you can take related to your Virtual Agent conversation. After completing a chat topic or request, these suggestions appear under a **Here's what you can do next** header. Selecting a suggested action initiates it directly in the same conversation, carrying over any relevant details such as your name.

For more information on configuration, see [Now Assist in Virtual Agent system properties](https://www.servicenow.com/docs/access?context=nava-sys-props&version=zurich&pubname=zurich-conversational-interfaces&ft:locale=en-US)

## Knowledge base citations

Virtual Agent generates its responses using your organization’s knowledge base articles. You can tap inline citations to view the ServiceNow knowledge articles that were used to generate the response.

## External content connections citations

![list of record citations](../image/na-va-standard-ext-connector.png "External citations")

If external search sources have been configured by your organization, you can search through external content connections. This can include information from attachments and knowledge blocks, or from the following list of content connections:

-   Microsoft SharePoint
-   Confluence
-   Atlassian Jira Cloud
-   Google Drive
-   Microsoft Teams
-   Predefined web sources
-   ServiceNow documentation
-   Slack

Sources display with icons that indicate the type of record type each source is, such as a table, PDF, incident report, and so on For more information about external content connections, see [External Content Connectors](https://www.servicenow.com/docs/access?context=ext-cont-connectors-landing-page&version=zurich&pubname=zurich-platform-administration&ft:locale=en-US).

## Doc QnA

![Now Assist summary of an attached PDF](../image/na-doc-qna.png "Mobile Doc QnA")

Doc QnA enables you to upload documents to your Virtual Agent conversation. Now Assist can then generate a summary or answer questions using the document you provided.

The assistant can analyze file formats including text and image files such as PDF, Word \(.doc, .docx\), JPEG, and PNG. The maximum file size of a file is 5 megabytes \(MB\).

To attach a file to your conversation, tap the plus icon \(![](../image/na-doc-qna-icon.png)\) in your search bar.

## ServiceNow AI Lens

ServiceNow AI Lens leverages generative AI to scan, extract, and interpret data from your mobile device.

When you start a new Virtual Agent chat, select **Show all my options** to view the option to open ServiceNow AI Lens. Now Assist then gives you the option to choose an existing image or open your camera app to take a new photo. Once an image is selected, Now Assist allows you to input additional directions for how the image should be analyzed.

For more information, see [ServiceNow AI Lens for mobile](servicenow-lens-mobile.md).

## Web search mode

![Virtual Agent displaying internet search results](../image/na-web-search.png "Mobile web search mode")

Web search mode in Now Assist enables you to search the internet directly from within your chat, displaying external results rather than internal company information. Select the Start web search mode icon \(![](../image/na-web-search-icon.png)\) to enter web search mode.

While active, all user queries are answered using internet search results, and a banner shows that web search mode is enabled. The identifying banner disappears once web search mode is ended. For additional information, see [Using Now Assist web search on mobile](using-na-web-search-mobile.md).

## Feedback and additional support

The chat experience is further enhanced by feedback mechanisms that invite you to rate the Virtual Agent responses with thumbs up or down icons. This feedback helps to continually improve the quality and relevance of the support provided.

If you find that your issue can’t be resolved through the Virtual Agent alone, the system is designed to offer further assistance by connecting you to a live support agent, allowing you to reset the conversation, or enabling you to create a formal incident report, depending on how your organization has configured the support environment.

## Push notifications

![Virtual Agent push notifications on a phone locked screen](../image/na-va-push-notification.png "Virtual Agent push notifications")

When progress has been made on a request submitted via Virtual Agent, you’ll receive a push notification. Tapping the notification opens the Virtual Agent chat in your mobile app.

## People citations

![User asking Now Assist for information on an employee named Alisa](../image/na-va-people-citations-standard.png "People citations in standard chat")

You can find information about people in your organization if you have Knowledge Graph activated. The system displays up to three possible matches, with inline citations and a Sources section for more details. Selecting a person's name takes you to their user profile, while selecting the numbered citation shows a popover with details like manager, location, email, teams, phone, and shared files.

## Additional resources

For more detailed information on all of standard chat’s specific skills, see [Standard chat](https://www.servicenow.com/docs/access?context=nava-standard-chat&version=zurich&pubname=zurich-conversational-interfaces&ft:locale=en-US).

For information on configuring Virtual Agent, see [Configuring assistants overview](https://www.servicenow.com/docs/access?context=configure-now-assist-va&version=zurich&pubname=zurich-conversational-interfaces&ft:locale=en-US).

**Parent Topic:**[Using Now Assist for Mobile](using-now-assist-mobile.md)

