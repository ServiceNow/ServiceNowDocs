---
title: Set rule-based improvement opportunity
description: Rule-based finding definition is a custom rule that displays improvement opportunities for a use case on the Summary and Insights page.
locale: en-US
release: xanadu
product: Process Mining
classification: process-mining
topic_type: task
last_updated: "2024-08-01"
reading_time_minutes: 4
breadcrumb: [Setting improvement opportunity from Project Builder, Setting improvement opportunity for projects, Working with improvement opportunities, Using Process Mining, Process Mining, Platform Analytics]
---

# Set rule-based improvement opportunity

Rule-based finding definition is a custom rule that displays improvement opportunities for a use case on the Summary and Insights page.

## Before you begin

Role required: sn\_process\_optimization\_analyst, sn\_process\_optimization\_power\_user, or sn\_process\_optimization\_admin

By setting up your own rules, you can focus on specific areas of the process that you'd want to know more about, thus identifying improvement opportunities for a given use case.

For example, you can set up a rule to display records that took more than 7 days from **Awaiting verification** to **Resolved**.

## Procedure

1.  Navigate to Improvement opportunity definition page.

    For information about Improvement opportunity definition page, see [Set improvement opportunities](improve-opportunities.md).

2.  Select **Create** on the Rule-based card.

3.  Provide details in the **Define** section.

    For details, see [Rule-based finding definition form from Finding Builder](../reference/finding-definition-form.md).

4.  Select **Configure**.

    The **Configure** tab is displayed.

    ![Configure rule-based finding in Finding Builder](../image/rule-find-config-builder.png)

5.  Fill the details on the form.

    1.  Define a filter by adding conditions that contain a field, operator, and values.

        Use the **Occurrence is** field to define whether the filter applies to the first, last, or all occurrences of this condition.

    2.  Use the **Add contextual condition** button to define additional contextual conditions for this filter.

        Use the **and** and **or** buttons to create as many contextual conditions as needed.

    3.  Select **Add next step** to define another filter within this chain.

        After creating a filter, a relationship section appears between the two filters. This section defines the relationship between the activities immediately above and below it.

    4.  Select a relationship between your filters.
        -   Directly followed by
        -   Eventually followed by
        -   Not directly followed by
        -   Not eventually followed by
    5.  Select the **Track duration** field.

        This field tracks the time between the specified finding steps to calculate the total duration of the finding process, which is displayed on the improvement opportunity.

    6.  Select **+ Add Chain** \(on the top right\) to create an additional chain of filters.

        A chain is a set of linked filters. Create a chain to define a separate set of related filters that must also evaluate to true, but doesn’t have a relationship with the filters in another chain. After you create a chain, you can navigate between chains using the **Chain &lt;number&gt;** tabs at the top of the window.

    7.  Select **Add constraint**.

        The constraints panel is displayed to the right. Use the Finding Constraint to set specific conditions between finding definitions steps, such as duration and relation constraints between certain steps, which help narrow down their scope beyond the basic finding rules.

    8.  Select **Add constraint**, provide all details and select **Add constraint**.

        ![Finding Definition constraint](../image/finding-constraint.png)

<table id="table_gwq_33h_1cc"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Name

</td><td>

Name of the constraint

</td></tr><tr><td>

Start

</td><td>

Event that triggers the finding constraint. The options available are the steps provided in the filters.

</td></tr><tr><td>

End

</td><td>

Event that concludes the finding constraint. The options available are the steps provided in the filters.

</td></tr><tr><td>

Min duration

</td><td>

Specifies the minimum duration between when the event defined in the **Start** field and event defined in the **End** field. The event in the **End** field must occur after the amount of time specified in this field.

</td></tr><tr><td>

Max duration

</td><td>

The maximum duration between when the event defined in the **Start** field and event defined in the **End** field. The event in the **End** field must occur before the amount of time specified in this field.

</td></tr><tr><td>

Relation constraint type

</td><td>

Optional constraint conditions to further define when the constraint triggers.-   **None**

No relation constraint

-   **Same**

Records must have the same value in a specific field. Specify this field in the **Relation constraint field** field.

-   **Different**

Records must have different values in a specific field. Specify this field in the **Relation constraint field** field.

-   **Same user**

Start and end conditions must be triggered by the same user.

-   **Different user**

Start and end conditions must be triggered by different users.

-   **Same event**

Indicates that the start and stop steps are identical, while intermediate steps can differ. This helps identify Ping-Pong patterns, such as A -&gt; B -&gt; A, where only the first and last steps need to match.

-   **Different event**

Indicates that the start and stop steps are distinct from each other, while intermediate steps can vary or be the same. This helps identify sequences where the initial and final activities are not the same, such as A -&gt; B -&gt; C, ensuring that the process begins and ends with different events.

</td></tr><tr><td>

Relation constraint field

</td><td>

Field associated with the relation constraint type.

 This field appears when **Same** or **Different** is selected in the **Relation constraint type** field.

 **Note:** The available relation constraint field will appear empty if there are no selections in the **Start Condition** or **End Condition** fields.

</td></tr></tbody>
</table>6.  Select **Save and exit**.


**Parent Topic:**[Setting improvement opportunity from Project Builder](../concept/setting-impr-opp-proj-build.md)

