---
title: Legacy - Create custom override definitions
description: Use scripts to override the default formulas used to create the analytics on the Conversational Analytics Dashboard.
locale: en-US
release: xanadu
product: Virtual Agent
classification: virtual-agent
topic_type: task
last_updated: "2024-08-01"
reading_time_minutes: 4
breadcrumb: [Legacy - Setting up the Conversational Analytics Dashboard, Legacy - Conversational Analytics Dashboard, Analyzing Virtual Agent performance, Virtual Agent, Conversational Interfaces]
---

# Legacy - Create custom override definitions

Use scripts to override the default formulas used to create the analytics on the Conversational Analytics Dashboard.

## About this task

**Important:**

Conversational Analytics dashboard is being prepared for future deprecation. It will be supported until deprecation but will no longer be available for installation. A new Conversational Analytics dashboard in Platform Analytics experience, which meets the compliance requirements of Government Community Cloud \(GCC\), and thus FedRAMP authorized, is available. See [Conversational Analytics dashboard in Platform Analytics experience](../concept/VA-dashboard-landing-page-pae.md).

For details on the deprecation process, see the [Deprecation Process \[KB0867184\]](https://support.servicenow.com/kb_view.do?sysparm_article=KB0867184) article in the Now Support Knowledge Base.

If you are an existing user of this dashboard and want to migrate analytics data to the new dashboard, see [Migrate data to Conversational Analytics dashboard in Platform Analytics experience \[KB1651556\]](https://support.servicenow.com/kb?id=kb_article_view&sysparm_article=KB1651556).

## Before you begin

Role required: Chat Analytics Admin

Be sure to set the application scope to Conversational Analytics.

## About this task

The Conversational Analytics Dashboard uses formulas to determine analytics, such as how to calculate duration. You can override the default formulas to tailor the analytics to your needs. For example, the default formula for duration in the dashboard is the time between the first and last exchanges in a conversation. You might like to override that formula by subtracting inactive times in the conversation.

The default formulas and formula overrides are in the sn\_ci\_analytics\_formula\_override table. You can only modify the existing formulas that are in the table by deactivating the default formula and creating a new formula override record. You cannot override some formulas because they are system dependent. You can, however, [create custom events](set-up-custom-events.md) to achieve a similar goal.

The default definitions are:

-   Duration—Time from the start of a conversation session until the last message is sent, rather than when the conversation session closes. You cannot replace the supplied script for Duration. You can only turn it on or off. If you deselect the **Active** check box, the duration is calculated until the end of the session. If you select the **Active** check box, the duration is calculated to the last message sent.
-   Self-solve rate—Number of conversations that did not have negative feedback, contained a topic that went through to the last node, and did not escalate to a live agent. The dashboard divides that number by the number of all conversations to get the rate.
-   Feedback—Defined as positive, neutral, and negative. For example, to override this behavior, first, use Virtual Agent \(VA\) Designer to create a ranking from 1 to 10. Then, you can use a script to override the dashboard's default behavior by grouping 1–4 as negative, 5–7 as neutral, and 8–10 as positive.
-   End state—Defined by default in 12 ways. For more information, see [Formula override examples](../reference/formula-override-examples.md).
-   Valid conversation—Defined as a conversation record that is included in the dashboard results for satisfying at least one of the following criteria.
    -   Non-actionable notification conversations, which do not require validation from the user, are counted as active conversations.
    -   Actionable notifications that are not part of an existing conversation are considered valid conversations when the status of the notification is either Sent or Completed.
    -   Conversation engages Virtual Agent topic discovery or direct live agent conversation.

**Note:** Formula overrides do not change the stored data. They only change how the dashboard displays the data by computing existing data in a different way.

## Procedure

1.  Navigate to **All** &gt; **Conversational Analytics** &gt; **Formula Override**.

    Alternatively, you can enter `sn_ci_analytics_formula_override.list` in the Filter Navigator to display the sn\_ci\_analytics\_formula\_override table.

2.  Select the formula you want to override.

    You cannot override the Duration formula, you can only activate or deactivate it. You can alter the scripts for other definitions. These are the only definitions you can alter.

    The Formula Override page appears and shows the existing formula.

    ![Formula Override record page showing existing formula.](../images/dashboard-formula-override-with-script.png)

3.  Copy the script in the Value Script field.

    The default formulas are read-only. So, to modify them, you must make a copy.

4.  Deselect the **Active** check box to make the default formula inactive.

5.  Click **Update**.

6.  Click **New** to create a formula override record that overrides the default formula.

    The Formula Override New Record page appears.

    ![Formula Override new record form.](../images/dashboard-formula-override.png)

7.  In the form, fill in the fields.

    |Field|Description|
    |-----|-----------|
    |**Type**|Select the Type of the default formula you want to override. For example, **DynamicProperties**.|
    |**Key**|Specifies the formula you want to override. For example, select **End State** to override the default formula for the definition of the end state of a conversation.|
    |**Value Field**|Specifies the new definition of the **Key** value.|
    |**Active**|Select the check box to make the new definition active. You can have multiple formulas for a property but only one can be active at a time. When you activate this definition, you must deactivate the default definition if not already done.|
    |**Advanced**|Selecting this check box removes **Value Field** and opens the **Value Script** field. You can paste the script of the default formula you copied earlier and modify it as required to change the existing formula used for the **Key** value. For example, if the **Key** value is **End State**, the script overrides the default formula that defines the end state of a conversation. For example scripts, see [Formula override examples](../reference/formula-override-examples.md).|

8.  Click **Submit**.


**Parent Topic:**[Legacy - Setting up the Conversational Analytics Dashboard](../concept/setting-up-va-dashboard-overview1.md)

