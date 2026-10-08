---
title: Create an intent in AI Admin Center \(Lux UI\)
description: Create an intent record to standardize a customer input goal and enable multichannel intent detection, AI agent routing, and contact center analytics.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/intelligent-experiences/ai-admin-center-lux-create-intent.html
release: brazil
topic_type: task
last_updated: "2026-10-02"
reading_time_minutes: 3
keywords: [AI Admin Center, Now Assist Center, AI, AI setup, intent]
breadcrumb: [Managing AI assets, Setting up AI capabilities and configurations, AI Admin Center, Getting started with AI, Enable AI Experiences]
---

# Create an intent in AI Admin Center \(Lux UI\)

Create an intent record to standardize a customer input goal and enable multichannel intent detection, AI agent routing, and contact center analytics.

**Important:** Lux is the new user experience for AI Admin Center. For more information on the Lux experience, see [AI Admin Center user experience \(Lux UI\)](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/intelligent-experiences/ai-admin-center-lux-user-experience.md).

The Next Experience AI Admin Center workspace is being prepared for deprecation in the November store release and will no longer be supported. For more information on the Next Experience UI, see [AI Admin Center workspace \(Next Experience UI\)](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/intelligent-experiences/now-assist-center-workspace.md).

In AI Admin Center version 6.1, the Next Experience and Lux user interfaces are both available.

## Before you begin

Role required: sn\_na\_center.nac\_admin

## About this task

An intent is a data record that captures and defines what a user is trying to accomplish in a chat request. Intent records help the system classify, understand, and route user input appropriately.

Intents are discovered and captured by AI Agent Advisor through scheduled analysis of multiple interaction channels. You can also create an intent using the conversational experience. Follow these steps to create an intent record manually.

**Note:** This topic describes the AI Admin Center feature based on the Lux user experience \(UI\). There is no Next Experience UI version of this topic.

## Procedure

1.  Navigate to **All** &gt; **AI Admin Center** &gt; **Home** or **Admin** &gt; **AI Admin Center**.

2.  Select **Asset library** \(\[Omitted image "icon-aiac-lux-nav-inventory.png"\] Alt text: Asset library icon.\) in the side navigation panel.

    The Asset library page opens.

3.  Select the **Create asset** button.

    The Create asset box opens showing options for the asset type.

4.  Select **Intent**.

    The New intent form opens.

5.  Complete the form.

    1.  Enter a name for the intent in the **Intent name** field.

    2.  Enter a description of the intent in the **Description** field.

    3.  In the **Example utterance** field, enter training utterance examples that are relevant to the intent.

        Type the utterance and select the **Add** icon \(\[Omitted image "icon-aiac-lux-add.png"\] Alt text: Add icon.\) to add the example.

    4.  In the **Detection criteria** tab, enter the conditions that determine when the intent applies to an utterance.

        **Tip:** Be specific about what the customer says or asks. Include two or three examples per bullet. Clarify what doesn't count as this intent to avoid confusion with similar intents.

    5.  In the **Resolution criteria** tab, enter the conditions that determine when the intent is considered resolved.

        **Tip:** Resolution requires concrete, observable outcomes, not effort. Number your conditions in logical order. Use "customer has," "confirmation was," or "system shows" to describe completed actions, not in-progress steps.

    6.  Turn the intent on or off by selecting the **Active** option.

6.  Select **Save**.


## Result

An intent is created and can be seen in the intents list on the Asset library page.

**Parent Topic:**[Managing AI assets in AI Admin Center](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/intelligent-experiences/now-assist-center-using-asset-inventory.md)

**Related topics**  


[View your AI assets in the asset inventory \(Next Experience UI\)]()

[View your AI assets in the asset library \(Lux UI\)]()

[Create an asset in the AI asset inventory \(Next Experience UI\)]()

[Create an asset in AI Admin Center \(Lux UI\)]()

[Edit an intent in AI Admin Center \(Lux UI\)]()

[Create a data asset in AI Admin Center \(Lux UI\)]()

