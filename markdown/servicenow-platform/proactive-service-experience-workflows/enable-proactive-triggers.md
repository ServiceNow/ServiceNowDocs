---
title: Enable Proactive Triggers
description: Use Proactive Triggers to create and view context-specific messages and use relevant actions on the chat widget.
locale: en-US
release: xanadu
product: Proactive Service Experience Workflows
classification: proactive-service-experience-workflows
topic_type: task
last_updated: "2024-08-01"
reading_time_minutes: 4
breadcrumb: [Installing Proactive Triggers, Proactive Triggers, Manage people and work capabilities, Extend ServiceNow AI Platform capabilities]
---

# Enable Proactive Triggers

Use Proactive Triggers to create and view context-specific messages and use relevant actions on the chat widget.

## Before you begin

**Note:** The Proactive Triggers feature \[sn\_pt\] is available as an app and must be installed from the ServiceNow Store. This feature is only available after you've installed and updated the Omni-Experience Standard Feature Set to the latest version through the ServiceNow Store. Subsequent updates are also available there. Visit the ServiceNow Store website to view all the available apps and for information about submitting requests to the store. For cumulative release notes information for all released apps, see the [ServiceNow Store version history release notes](https://docs.servicenow.com/bundle/store-release-notes/page/release-notes/store/sn-store-release-notes.html).

For conceptual information about Proactive Triggers, see [Exploring Proactive Triggers](../concept/proactive-triggers.md).

The Proactive Triggers feature can be used with Domain Separation. For more information about Domain Separation, see [Domain separation explained](https://www.servicenow.com/docs/access?context=bp-what-is-domain-separation&version=xanadu&pubname=xanadu-platform-security&ft:locale=en-US).

Role required: admin

## About this task

An admin first enables and then creates rules and actions as separate tasks.

## Procedure

1.  In the navigation filter, enter `sys_properties.list`.

    The entire list of properties in the System Properties \[sys\_properties\] table appears.

2.  Search for the `com.glide.cs.advanced-chat-popover` system property, and then change the value from **false** \(default\) to **true**.

    This system property enables the smart chat component on the Service Portal. This system property is only applicable to the requester persona.

3.  Navigate to **Conversational Interfaces** &gt; **Settings**.

    You must be in the Proactive Triggers scope to enable this feature.

4.  Under Proactive triggers, select the more info icon \(![More info icon.](../image/info-icon.png)\) next to the **Enable proactive triggers** field toggle switch to view the Proactive Triggers scope reminder.

    ![Proactive Triggers scope reminder.](../image/proactive-triggers-scope-info-2.png)

    For more information about scopes and how to change them, see [Application scopes](../../../app-store/dev_portal/application_model/concept/c_ApplicationScopes.md).

5.  Under **Proactive triggers**, select the **Enable proactive triggers** field toggle switch to enable the feature.

    By default, the Proactive Triggers feature is inactive.

6.  Next to **Rules**, select **View all**.

    The default sample rules included with Proactive Triggers appear.

    ![Default Proactive Triggers rules.](../image/proactive-rules-default.png)

7.  Navigate back to the **Conversational Interfaces** &gt; **Settings** page and next to **Trigger types**, select **View all**.

    The default trigger types appear. All trigger types default to **Active is true** except the Search Event trigger type. To turn on the Search Event trigger type, proceed to the next step.![Default Proactive Triggers types.](../image/pt-trigger-types.png)

8.  Turn on the Search Event trigger.

    The Search Event triggers a pop-up message on the Service Portal Default Search Profile whenever a search result yields no result. The Search Event trigger is an inactive default trigger type that uses the System API source rather than the web browsing source. Because this trigger type defaults to inactive, an admin must turn on the related business rule, trigger type, Proactive Triggers rule, and action prior to using this trigger.

    1.  Navigate to **System Definition** &gt; **Business rules**.

    2.  Search for `Proactive Trigger on Search` in the **Business Rules** field, and then select the business rule.

    3.  Select the **Active** option to turn on the business rule.

    4.  Adjust any settings, as needed.

        **Note:** Your organization may want to update the **Filter Conditions** on the **When to Run** related tab. For example, if your organization doesn’t use the Service Portal, update the default values in the Filter Conditions section to reflect your organization's preferred portal or site. Your organization may also want to adjust the Proactive Triggers API script in the **Advanced** related tab. For additional information on the Proactive Triggers API script, see [ProactiveTriggerAPI - Scoped](https://www.servicenow.com/docs/access?context=ProactiveTriggerScopedAPI&version=xanadu&pubname=xanadu-api-reference&ft:locale=en-US).

    5.  Select **Update**.

    6.  Navigate to **Conversational Interfaces** &gt; **Settings** and under **Proactive Triggers**, select **View All** next to **Trigger Types**.

    7.  Select **Search Event**.

    8.  In the Proactive Trigger Type form for Search Event, select the **Active** option to turn on the trigger type and adjust any settings, as needed.

    9.  Select **Update**.

    10. Select **Search - No Search Result** from the Proactive Rules related list.

    11. In the Proactive Rule form for Search - No Search Result, select the **Active** option to turn on the rule and adjust any settings, as needed.

    12. Select **Update**.

    13. Select **No Search Result Message** from the Proactive Actions related list.

    14. In the Proactive Action form for No Search Result Message, select the **Active** option to turn on the action and adjust any settings, as needed.

    15. Select **Submit**.

    The Search Event trigger type is turned on.


## Result

The Proactive Triggers feature is enabled and you know where to create rules, actions, and custom trigger types.

## What to do next

Create rules and actions for Proactive Triggers. For more information, see [Create rules and actions for Proactive Triggers](create-rule-actions.md).

Create custom trigger types. For more information, see [Create custom trigger types](create-custom-trigger-types.md).

**Related topics**  


[Enable message preview on the chat widget](https://www.servicenow.com/docs/access?context=web-client-message-preview&version=xanadu&pubname=xanadu-conversational-interfaces&ft:locale=en-US)

