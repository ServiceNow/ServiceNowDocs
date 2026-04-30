---
title: Example use case: a-b-a transitions
description: Use finding rules to identify when records return to a previous state.
locale: en-US
release: zurich
product: Process Mining
classification: process-mining
topic_type: task
last_updated: "2025-07-31"
reading_time_minutes: 3
breadcrumb: [Set rule-based finding definitions using Classic view, Setting improvement opportunities from Classic view, Setting improvement opportunity for projects, Working with improvement opportunities, Using Process Mining, Process Mining, Platform Analytics]
---

# Example use case: a-b-a transitions

Use finding rules to identify when records return to a previous state.

## Before you begin

Role required: sn\_process\_optimization\_analyst, sn\_process\_optimization\_power\_user, or sn\_process\_optimization\_admin

This example creates a finding definition that uses two finding rules and a finding constraint to identify when an incident is assigned to a group \(in this example, the Database group\), and then switched back to its original assignment. Use finding definitions like this one to identify situations where incidents are incorrectly assigned.

## Procedure

1.  Navigate to **All** &gt; **Process Mining** &gt; **Projects** &gt; **All Projects**, and open the project where you want to include this finding.

2.  In the **Project Finding Definitions** tab, select the **New** button to create a finding definition.

3.  Fill in the details in the **Finding Definition** record.

    For information, see [Set rule-based finding definitions using Classic view](configure-finding-definition.md). ![Finding definition record](../image/aba-example-1.png)

4.  Right-click the form header, and select **Save** from the context menu.

    After saving, the **Finding Rules** and **Finding Constraints** tabs are visible.

5.  In the **Finding Rules** tab, select the **New** button to create a finding rule.

6.  Select the plus \(+\) icon to the right of the **Start condition** field to begin creating your start condition.

    **Note:** You must create conditions for each rule. There’s no option to select existing rules.

7.  Use the fields on the **Create new condition** form to create your first condition.

    For the start condition, you create a condition where an incident is created with any value in the **Assignment group** field.

    |Field|Value|
    |-----|-----|
    |Name|AG is Anything|
    |Table configuration|Incident|
    |Condition type|Field/value condition|
    |Field|Assignment group|
    |Predicate|is anything|
    |Occurrence\(s\) to match|All|
    |Condition subtype|Single|

    ![Finding definition record](../image/aba-example-2.png)

8.  Select **Submit** to save your condition.

9.  In the **Relation** field, select **eventually followed by**.

10. Select the plus \(+\) icon to the right of the **End condition** field to begin creating your end condition.

11. Use the fields on the **Create new condition** form to create your second condition.

    For the second condition, you create a condition where an incident is assigned to the Database group.

    |Field|Value|
    |-----|-----|
    |Name|AG is Anything|
    |Table configuration|Incident|
    |Condition type|Field/value condition|
    |Field|Assignment group|
    |Predicate|is|
    |Field value|Database|
    |Occurrence\(s\) to match|All|
    |Condition subtype|Single|

    ![Finding definition record](../image/aba-example-3.png)

12. Select **Submit** to save your condition.

    You now have your first finding rule, which identifies when an incident is assigned to the Database group. Now you must create a second finding rule in the same chain.![Finding definition record](../image/aba-example-4.png)

13. Select **Create new rule \(Same chain\)**

    This is a new rule in the same chain. You can see that the **Sequence** field is `2` and the **Start condition** field is automatically filled with the **End condition** of the previous rule.![Finding definition record](../image/aba-example-5.png)

14. In the **Relation** field, select **eventually followed by**.

15. Select the plus \(+\) icon to the right of the **End condition** field to begin creating your second end condition.

16. Use the fields on the **Create new condition** form to create your end condition.

    For the second condition, you create a condition where an incident is assigned to the Database group.

    |Field|Value|
    |-----|-----|
    |Name|AG is Anything \(2\)|
    |Table configuration|Incident|
    |Condition type|Field/value condition|
    |Field|Assignment group|
    |Predicate|is anything|
    |Occurrence\(s\) to match|All|
    |Condition subtype|Single|

    ![Finding definition record](../image/aba-example-6.png)

17. Select **Submit** to save your condition.

    You now have a completed second finding rule.

18. Select **Submit** to save your finding rule.

19. Open your project record again.

20. From the **Project Finding Definitions** tab, open the finding definition created in the previous steps.

    **Note:** This should be the one you created in step 3.

21. In the **Finding Constraints** tab, select the **New** button.

22. Use the fields on the **Finding Constraint** form to create your constraint.

    |Field|Value|
    |-----|-----|
    |Name|First AG matches Second AG|
    |Start condition|AG is Anything|
    |End condition|AG is Anything\(2\)|
    |Relation constraint|is the same event|

    ![Finding definition record](../image/aba-example-7.png)

    This finding constraint refines your finding rules. Now, for example when an incident is assigned to **Network**, then **Database**, and then back to **Network**, it will be discovered by this finding rule.

23. Select **Submit**.


**Parent Topic:**[Set rule-based finding definitions using Classic view](configure-finding-definition.md)

