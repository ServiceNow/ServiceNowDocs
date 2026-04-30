---
title: Use Sentiment Analysis with Workflow Studio
description: Create a flow to upgrade the assignment group of a case if the user has a negative sentiment in the short description.
locale: en-US
release: xanadu
product: Generative AI Controller
classification: generative-ai-controller
topic_type: task
last_updated: "2024-08-01"
reading_time_minutes: 2
breadcrumb: [Using Generative AI Controller, Generative AI Controller, Now Assist, Enable AI experiences]
---

# Use Sentiment Analysis with Workflow Studio

Create a flow to upgrade the assignment group of a case if the user has a negative sentiment in the short description.

## Before you begin

Role required: admin

## About this task

The Sentiment Analysis capability helps determine whether the user-generated text has a positive or negative sentiment. If a user is expressing negative statements such as "Level 1 support couldn't help me," you could upgrade the assignment group automatically for the case to help the user have a better experience.

For more information on tracking Generative AI Controller usage, see [Monitoring Now Assist usage](https://www.servicenow.com/docs/access?context=monitoring-now-assist-usage&version=xanadu&pubname=xanadu-platform-administration&ft:locale=en-US).

## Procedure

1.  Navigate to **All** &gt; **Process Automation** &gt; **Flow Designer**.

2.  Select **New** &gt; **Flow**.

3.  Enter the name of the flow, such as `Change assignment group if negative sentiment`.

4.  Select **Submit**.

5.  Select **Add a trigger**.

6.  Select **Record** &gt; **Created** to update a new record.

7.  Select the table that the flow should run on.

    For this example, select the Case \(sn\_customerservice\_case\) table.

8.  Select **Done**.

9.  Under Actions, select **Add an Action, Flow Logic, or Subflow** and then select **Action** to open the Actions panel.

10. In the action selector, search for the **Generative AI Controller** &gt; **Sentiment Analysis** action and select it.

11. Drag a data pill from the Data panel or select the data pill picker icon.

    In this case, drag the **Trigger** &gt; **Case Record** &gt; **Short description**. ![Short description added to the utterance field.](../image/sa-short-description-utterance.png)

12. Select **Done**.

    ![Complete sentiment analysis utterance](../image/sa-complete-utterance.png)

13. Add an action by selecting **Add an Action, Flow Logic, or Subflow**.

14. Select **Flow Logic** &gt; **If**.

15. Give the **Condition label** a name, such as `Negative sentiment`.

16. For the **Condition** field, drag a data pill or select the data pill picker icon to search for the correct condition.

    In this case, drag the **Sentiment Analysis** &gt; **response**. ![Short description field added.](../image/sa-if-condition-data-pill-picker.png)

17. Select `contains` the value `Negative`.

    **Note:** Capitalization matters. This flow won't work if the value is set to `negative`.

    ![Completed condition for If logic statement.](../image/sa-complete-if-statement.png)

18. Search for **Update Record** and select the action.

19. Drag the **Trigger** &gt; **Case Record** data pill into the **Record** field or select the icon to search.

    The **Table** field is filled in automatically based on the Trigger record.

20. Select **Add field value** and search for the fields that you want to update.

    In this example, select **Assignment group**.

21. Select which value you would like to set the field to.

    The field value depends on your use case. In this example, the value is set to `Service Desk`.

    ![Update record action filled in with Sentiment Analysis response setting assignment group to Service Desk.](../image/sa-complete-update-record.png)

22. Select **Done**.

23. Save the flow by selecting **Save**.


## What to do next

After you've saved the flow, you must activate the flow to migrate it to production or test it further.

