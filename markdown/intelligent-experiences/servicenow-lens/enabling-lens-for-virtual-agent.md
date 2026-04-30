---
title: Enabling ServiceNow AI Lens in Virtual Agent
description: You can enable ServiceNow AI Lens in Virtual Agent so that ServiceNow AI Lens can be triggered from Virtual Agent conversation.Enable the AI Search application on your instance so that you can use ServiceNow AI Lens skill to gather insights from an image using generative AI.Enable the default Now Assist in Virtual Agent assistant so that you can use ServiceNow AI Lens in Virtual Agent.Enable an assistant other than the default Now Assist in Virtual Agent assistant in ServiceNow AI Lens topic.Enable the chat function in Virtual Agent for a mobile device for ServiceNow AI Lens.
locale: en-US
release: yokohama
product: ServiceNow Lens
classification: servicenow-lens
topic_type: concept
last_updated: "2025-07-28"
reading_time_minutes: 3
breadcrumb: [Configure, ServiceNow AI Lens, Enable AI experiences]
---

# Enabling ServiceNow AI Lens in Virtual Agent

You can enable ServiceNow AI Lens in Virtual Agent so that ServiceNow AI Lens can be triggered from Virtual Agent conversation.

By enabling ServiceNow AI Lens in Virtual Agent, you can trigger AI-powered ServiceNow AI Lens to scan an image for getting insights, recommendation, resolution steps, and more.

## Enable AI Search

Enable the AI Search application on your instance so that you can use ServiceNow AI Lens skill to gather insights from an image using generative AI.

### Before you begin

Role required: ais\_admin or admin

### Procedure

1.  Navigate to **All** &gt; **AI Search** &gt; **AI Search Status**.

    ![AI Search Status module under AI Search application.](../image/nav-ai-search-status-lens.png)

2.  If AI search is not enabled, select **Request AI Search**.

    After AI Search is activated in your instance, you will see the following success message.

    ![AI search activation confirmation.](../image/ai-search-ready.png)


## Enable the default Now Assist assistant for ServiceNow AI Lens

Enable the default Now Assist in Virtual Agent assistant so that you can use ServiceNow AI Lens in Virtual Agent.

### Before you begin

If you have another assistant configured for your specific use case or industry, you can skip this procedure and follow [Enable other assistants in ServiceNow AI Lens topic](enabling-lens-for-virtual-agent.md#).

Role required: virtual\_agent\_admin or admin

### Procedure

1.  Navigate to **All** &gt; **Conversational Interfaces** &gt; **Assistants**.

    ![Assistants module under Conversational Interfaces application.](../image/nav-assistants-lens.png)

2.  Select the **Now Assist in Virtual Agent \(default\)** assistant.

    ![Now Assist in Virtual Agent assistant is enabled.](../image/now-assist-va-topic-lens.png)

3.  On the Overview tab, select **Save and continue**.

4.  On the Now Assist Skills tab, ensure that **Now Assist Topics** is selected.

    ![Selected Now Assist Topics from the Now Assist Skills tab.](../image/now-assist-topics-lens.png)

5.  Select **Save and continue**.

6.  Display your assistant on a portal.

    1.  On the Display experience tab, select the Portals tab.

    2.  Select the portal for which you want to enable the Now Assist assistant from the **Add portal** drop-down.

        ![Configuring display experience for a portal.](../image/display-exp-portal-lens.png)

    3.  On the Add chat experience dialog box, select **Enhanced chat** option.

        ![Selecting Enhanced chat option while configuring display experience for a portal.](../image/display-exp-portal-enhanced-chat-lens.png)

    4.  Select **Add**.

7.  Display your assistant on a mobile device.

    1.  On the Display experience tab, select the Mobile tab.

    2.  Under the Chat launcher functions section, select Agent Chat from the **Add function** drop-down.

        ![Configuring display experience for a mobile device by adding function.](../image/display-exp-mobile-lens.png)

    3.  On the Add chat experience dialog box, select **Enhanced chat** option.

        ![Selecting Enhanced chat option while configuring display experience for a mobile device.](../image/display-exp-mobile-enhanced-chat-lens.png)

    4.  Select **Add**.

8.  On the Information sources tab, select **Save and continue**.

9.  On the Branding tab, select **Save and continue**.

10. On the Chat experiences tab, select **Save and continue**.

11. On the Review tab, select **Done**.


## Enable other assistants in ServiceNow AI Lens topic

Enable an assistant other than the default Now Assist in Virtual Agent assistant in ServiceNow AI Lens topic.

### Before you begin

Skip this procedure, if you have enabled the default Now Assist assistant in the previous procedure.

Role required: virtual\_agent\_admin or admin

### Procedure

1.  Navigate to **All** &gt; **Conversational Interfaces** &gt; **Virtual Agent** &gt; **Designer**.

    Virtual Agent Designer opens in a new tab.

    ![Designer module for Virtual Agent under Conversational Interfaces.](../image/nav-va-designer.png)

2.  In the Topic tab, select **ServiceNow Lens** topic.

    ![ServiceNow AI Lens topic in Virtual Agent Designer.](../image/va-designer-lens-topic.png)

3.  In the Select LLM assistants section, select your assistant.

    ![Selecting other assistant in ServiceNow AI Lens topic for Virtual Agent.](../image/enable-other-assistant.png)

4.  Publish the **ServiceNow Lens** topic.


## \(Optional\) Enable Agent chat function for a mobile app

Enable the chat function in Virtual Agent for a mobile device for ServiceNow AI Lens.

### Before you begin

Role required: admin or delegated developer

### About this task

Do this procedure when you do not see the Now Assist ![](../../../common/image/icon-ai-sparkle.png) icon in the Now Mobile app.

### Procedure

1.  Navigate to **All** &gt; **System Mobile** &gt; **Mobile App Builder**.

    ![Mobile App Builder designer app.](../image/nav-mobile-app-builder-lens.png)

    The Mobile App Builder opens in a new tab.

2.  From the search option, search and select **Now Mobile**.

    ![Selecting the Now Mobile app in Mobile App Builder.](../image/now-mobile-lens.png)

3.  From the list of screens, select **Homepage**.

    ![Selecting the Homepage screen for the Now Mobile app in Mobile App Builder.](../image/now-mobile-homepage-lens.png)

4.  From the Now Platform configuration list, select the **Chat** function.

5.  Enable the **Chat with Virtual Agent** setting.

    ![Activating Chat with Virtual Agent setting for Homepage of Now Mobile in Mobile App Builder.](../image/mobile-agent-chat-active-lens.png)


