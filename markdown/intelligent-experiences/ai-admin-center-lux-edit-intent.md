---
title: Edit an intent in AI Admin Center \(Lux UI\)
description: Edit the details and activation status of an intent record.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/australia/intelligent-experiences/ai-admin-center-lux-edit-intent.html
release: australia
topic_type: task
last_updated: "2026-10-02"
reading_time_minutes: 3
keywords: [AI Admin Center, Now Assist Center, AI, AI setup, intent]
breadcrumb: [Managing AI assets, Setting up AI capabilities and configurations, AI Admin Center, Enable AI experiences]
---

# Edit an intent in AI Admin Center \(Lux UI\)

Edit the details and activation status of an intent record.

**Important:** Lux is the new user experience for AI Admin Center. For more information on the Lux experience, see [AI Admin Center user experience \(Lux UI\)](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/australia/intelligent-experiences/ai-admin-center-lux-user-experience.md).

The Next Experience AI Admin Center workspace is being prepared for deprecation in the November store release and will no longer be supported. For more information on the Next Experience UI, see [AI Admin Center workspace \(Next Experience UI\)](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/australia/intelligent-experiences/now-assist-center-workspace.md).

In AI Admin Center version 6.1, the Next Experience and Lux user interfaces are both available.

## Before you begin

Role required: sn\_na\_center.nac\_admin

## About this task

Follow these steps to edit an intent record.

An intent is a data record that captures and defines what a user is trying to accomplish in a chat request. Intent records help the system classify, understand, and route user input appropriately.

Intents are discovered and captured by AI Agent Advisor through scheduled analysis of multiple interaction channels. You can create an intent manually in AI Admin Center. For more information, see [Create an intent in AI Admin Center \(Lux UI\)](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/australia/intelligent-experiences/ai-admin-center-lux-create-intent.md). You can also create, edit, or delete an intent using the conversational experience.

**Note:** This topic describes the AI Admin Center feature based on the Lux user experience \(UI\). There is no Next Experience UI version of this topic.

## Procedure

1.  Navigate to **All** &gt; **AI Admin Center** &gt; **Home** or **Admin** &gt; **AI Admin Center**.

2.  Select **Asset library** \(\[Omitted image "icon-aiac-lux-nav-inventory.png"\] Alt text: Asset library icon.\) in the side navigation panel.

    The Asset library page opens.

3.  Select the **Intents** tab.

4.  In the row of the intent you want to edit, select the intent name or select the **Actions** icon \(\[Omitted image "icon-aiac-lux-options.png"\] Alt text: Actions icon.\) and choose **View details**.

    The intent details page opens.

5.  Select **Edit**.

    The intent editing form opens.

6.  Update the form as needed.

    1.  Enter a name for the intent in the **Intent name** field.

    2.  Enter a description of the intent in the **Description** field.

    3.  In the **Example utterance** field, enter training utterance examples that are relevant to the intent.

        Type the utterance and select the **Add** icon \(\[Omitted image "icon-aiac-lux-add.png"\] Alt text: Add icon.\) to add the example.

        Select the **Remove** icon \(\[Omitted image "icon-now-assist-center-remove.png"\] Alt text: Remove icon.\) to remove the utterance.

    4.  In the **Detection criteria** tab, enter the conditions that determine when the intent applies to an utterance.

        **Tip:** Be specific about what the customer says or asks. Include two or three examples per bullet. Clarify what doesn't count as this intent to avoid confusion with similar intents.

    5.  In the **Resolution criteria** tab, enter the conditions that determine when the intent is considered resolved.

        **Tip:** Resolution requires concrete, observable outcomes, not effort. Number your conditions in logical order. Use "customer has," "confirmation was," or "system shows" to describe completed actions, not in-progress steps.

    6.  Turn the intent on or off by selecting the **Active** option.

7.  Select **Save**.


**Parent Topic:**[Managing AI assets in AI Admin Center](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/australia/intelligent-experiences/now-assist-center-using-asset-inventory.md)

**Related topics**  


[View your AI assets in the asset inventory \(Next Experience UI\)]()

[View your AI assets in the asset library \(Lux UI\)]()

[Create an asset in the AI asset inventory \(Next Experience UI\)]()

[Create an asset in AI Admin Center \(Lux UI\)]()

[Create an intent in AI Admin Center \(Lux UI\)]()

[Create a data asset in AI Admin Center \(Lux UI\)]()

