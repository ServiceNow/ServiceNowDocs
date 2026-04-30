---
title: Using Now Assist in portal case form
description: Guide requesters through a self-service flow to find solutions to their problems using Genius Results and reduce the number of cases created.
locale: en-US
release: zurich
topic_type: concept
last_updated: "2025-07-31"
reading_time_minutes: 3
keywords: [Generative AI, generative AI for Customer Service Management, generative AI for customer service agents]
breadcrumb: [Using Virtual Agent in service portals, Automate and optimize, Use, Customer Service Management]
---

# Using Now Assist in portal case form

Guide requesters through a self-service flow to find solutions to their problems using Genius Results and reduce the number of cases created.

A guided flow enhances the user experience by assisting requester who is facing issues and are about to create a case. It helps them find solutions through genius results, thus reducing the number of cases created and the effort required by agents to close open cases.

-   As a requester, you can enter your details and receive the results as part of your case creation process.
-   As a requester, you can continue with the case creation even if the results don’t load and create a case.
-   As a requester, you can see the results on the same page until you submit the form or cancel the flow.

**Note:** This record producer is available for the Customer Support portal \(CSM\).

Guided Flow for Case Creation

1.  Enter Your Details:
    -   Navigate to **Request Something** &gt; **Support** &gt; **Create case for a product \(Now Assist\)**.

        **Note:** Verify that AI search in portals is activated. For more info, see [Enable and configure AI Search in Service Portal](https://www.servicenow.com/docs/access?context=enable-ais-sp&version=zurich&pubname=zurich-platform-user-interface&ft:locale=en-US)

    -   A single Subject field appears. Start entering your issue, and genius results, sources, related catalog items, and knowledge articles are displayed under related content.

        **Note:** You can also search for public content in the portal and get the search results from within the Now Assist genius result. The source of the search results is available as internal or external with the links to it.

2.  Review Results:

    -   If no genius results are found, related content is shown.
    -   If no results are found, a message appears: There’s not enough description for AI to find the results. Try using different keywords or another sentence.
    **Note:** Genius result configuration: The behavior of Now Assist results depends on the selected genius result configuration.

    -   When configured for Now Assist Q&amp;A, the system generates a direct answer based on your query and displays relevant sources below the response.
    -   When configured for multi-content response, the system follows the same response flow as Q&amp;A and includes additional features for displaying multiple content types in a single result.
        -   Response text includes the inline citations that correspond directly to the sources listed in the **Sources** section. The citations appear as numbered references — for example, \[1\] and \[2\] — and map to sources in the order they appear in the list. You can select a source to view the referenced content.
        -   You can access the Virtual Agent chat interface by selecting the chat icon under **Sources**. The Virtual Agent provides contextual follow-up questions to help resolve requests. Ensure that **Now Assist Actions** genius result configuration is setup to see this.
3.  Take Action:
    -   If you find a solution to your query, select the **Cancel** button to return to the home page.
    -   If no results are found or you’re not satisfied with the result, select the **Ask Now Assist** button, to open a contextual chat window in the Now Assist in Virtual Agent for additional help.

        **Note:**

        Enable enhanced chat experience from the Now Assist in Virtual Agent guided setup for the feature to work. For details, see [Display your chat assistant on a portal, channel, or mobile app](https://www.servicenow.com/docs/access?context=display-assistant-portal-channel&version=zurich&pubname=zurich-conversational-interfaces&ft:locale=en-US).

    -   If no relevant results are found, select **Continue with case creation** to proceed. This action enables the **Submit** button and shows the additional fields needed to complete the case form.
    -   Select **Submit** to create a record case.

This guided flow helps you find solutions faster, improves the user experience, and reduces case creation and agent effort.

