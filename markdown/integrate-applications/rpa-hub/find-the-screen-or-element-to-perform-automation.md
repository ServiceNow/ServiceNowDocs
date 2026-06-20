---
title: Use the screen or element match rules
description: Use the screen or element match rules to match a screen or element from among multiple screens and elements with its corresponding rules. Match rules enables the connector to identify the appropriate screen or element and perform tasks.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/zurich/integrate-applications/rpa-hub/find-the-screen-or-element-to-perform-automation.html
release: zurich
product: RPA Hub
classification: rpa-hub
topic_type: task
last_updated: "2025-07-31"
reading_time_minutes: 5
breadcrumb: [Configure the Terminal connector, Terminal \(Mainframe\) connector, Connectors, Automation components, RPA Desktop Design Studio, Robotic Process Automation \(RPA\) Hub, Workflow Data Fabric]
---

# Use the screen or element match rules

Use the screen or element match rules to match a screen or element from among multiple screens and elements with its corresponding rules. Match rules enables the connector to identify the appropriate screen or element and perform tasks.

## Before you begin

Capture at least one emulator screen and an element.

Role required: none

## About this task

To perform tasks on a specific emulator screen or element from among multiple emulator screens and elements, the Terminal connector must first identify a screen. To identify a screen or element, the Terminal connector uses the screen match rules, attributes, and the element locators. The screen match rules, locators, and attributes provide unique identification criteria for each screen and element.

All captured screens have a default screen match rule. Additionally, you can define one or more screen match rules. You can modify or remove the default screen match rules or the screen match rules that you define.

Screen and elements have different match rules. For a screen, the terminal connector uses screen match rules and for an element, it uses locators.

\[Omitted image "terminal-connector-screen-rules.png"\] Alt text: Default screen match rule and the option to define a screen match rule.

The image shows the locators for a screen element.

\[Omitted image "terminal-connector-locators.png"\] Alt text: Field or table locators.

## Procedure

1.  Rename the screen with a unique name.

    1.  Under the Screen and elements pane, select the screen.

    2.  Under the **Properties** pane, rename the screen and press **Enter**.

        \[Omitted image "terminal-connector-rename-screen.png"\] Alt text: Update screen name.

        The new screen name appears under the Screen and elements pane.

    3.  Under the Screen and elements pane, right-click the screen and select **Refresh**.

        If the screen match rule matches a screen, the screen match icon \(\[Omitted image "screen-match-icon.png"\] Alt text: Screen match icon\) appears for both the screen and the screen match rule. The icon indicates that the screen match rule matches with the screen.

        \[Omitted image "terminal-connector-rule-matched.png"\] Alt text: Screen rule match.

2.  Define a screen match rule.

    You can add a field or text from the emulator screen that the Terminal connector uses as a screen match rule.

    1.  Select **Add**.

        \[Omitted image "terminal-connector-add-screen-rule.png"\] Alt text: Screen rule add button.

    2.  Right-click on the required field and select either of the options.

        -   **Add this Field as screen match rule**: The connector uses the field details such as row, column, and text as a screen match rule.
        -   **Add this Text as screen match rule**: The connector uses the field text as a screen match rule.
        \[Omitted image "terminal-connector-add-screen-rule-options.png"\] Alt text: New screen rule options.

        The screen match rule appears under the **Screen match rules** pane.

    3.  Select **OK**.

3.  Define an element and match rules.

    The Terminal connector provides multiple rules or locators that provide information about elements. For example, the row and column numbers of the field on the screen is one of the match rules. The Terminal connector provides five locators and you can choose any locator to match the element.

    1.  Rename the field.

        When you capture multiple elements, the Terminal connector provides them default names such as Field\_0, Field\_1, Table\_0, and Table\_1. To easily identify an element, you can rename it.

        \[Omitted image "terminal-connector-update-element-name.png"\] Alt text: Update default element name.

        The updated element name appears under the Screens and elements pane.

        \[Omitted image "terminal-connector-new-element-name.png"\] Alt text: New element name.

    2.  Right-click the element and select **Refresh**.

        The element match icon \(\[Omitted image "screen-match-icon.png"\] Alt text: Screen match icon\) appears for the element. The icon indicates that the locator matched with the element.

        \[Omitted image "terminal-connector-default-element-rule.png"\] Alt text: Default element match rule.

    3.  Use the other locators in the **Locator** drop-down to match the element.

        The table describes the locators.

<table id="table_ocz_h5q_w1c"><thead><tr><th>

Rule

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Field By Position

</td><td>

Matches a field with its row and column number in the screen. The Row and Column fields show the row and column numbers of the starting point of the field that you captured from the screen.\[Omitted image "terminal-conn-locator-one.png"\] Alt text: Row and column number of a field.

</td></tr><tr><td>

Field By Index

</td><td>

Matches a field with its index number in the screen.An index number is a unique identifier of a field in the Mainframe screen that enables the connector to identify a field. Each field on the emulator screen has a unique index number. The first field in the first row gets index 1, then the second field in the first row gets index 2, and so on. Index numbers are first assigned to the fields in the first row and then from the first field of the second row until all fields in the screen get index numbers.

\[Omitted image "terminal-conn-index.png"\] Alt text: Field indexes.

</td></tr><tr><td>

Field By Previous Field Text

</td><td>

Matches a captured field with the text in the field that is located immediately before the field that you captured. The **Previous Field Text** match rule shows the text in the previous field.\[Omitted image "terminal-conn-locator1.png"\] Alt text: Field By Previous Field Text.

\[Omitted image "terminal-conn-previous-field-text.png"\] Alt text: Previous Field text.

If there is no previous field, the **Previous Field Text** field shows no value.

</td></tr><tr><td>

Field By Next Field Text

</td><td>

Matches a field with the text in the field that is located immediately after the field that you captured. The **Next Field Text** match rule shows the text in the next field.\[Omitted image "terminal-conn-locator2.png"\] Alt text: Field By Next Field Text.

\[Omitted image "terminal-conn-next-field-text.png"\] Alt text: Next Field text.

If there’s no next field, the **Next Field Text** field shows no value.

</td></tr><tr><td>

Region \(Table\)

</td><td>

Use this locator when you want to capture data from an emulator screen in the tabular format. The image shows the selected the fields with data in a tabular format.\[Omitted image "terminal-conn-table-region.png"\] Alt text: Region in a screen.

</td></tr></tbody>
</table>4.  Define an attribute and match rules.

    1.  Select the field.

        The field attribute appears under the **Match attributes** pane.

        \[Omitted image "terminal-connector-element-attribute.png"\] Alt text: Element attribute.

    2.  Select the attribute.

    3.  Right-click the element and select **Refresh**.

        The element match icon \(\[Omitted image "screen-match-icon.png"\] Alt text: Screen match icon\) appears for the element and the attribute. The icon indicates that the attribute matches with the element.

        \[Omitted image "terminal-connector-attribute-refresh.png"\] Alt text: Attribute refresh.

5.  Modify screen match rules.

    1.  In the screen match rules section, select the rule.

        The Properties pane shows the match rule details.

        \[Omitted image "terminal-conn-match-rule-details.png"\] Alt text: Match rule details.

    2.  In the Properties pane, select the expand match rule icon \(\[Omitted image "match-rule-icon.png"\] Alt text: Match rule icon.\)

    3.  Update the values in the **Comparison Type** or **Comparison Value** fields.

    4.  Clear the **Enabled** option.

        \[Omitted image "terminal-conn-match-rules-update.png"\] Alt text: Match rules update options.

    5.  Select **Done**.

6.  Modify a field match rule.

    1.  Under the Screens and elements pane, select the required field that you captured.

        The Match attributes pane shows the field attributes.

        \[Omitted image "terminal-connector-field-attributes.png"\] Alt text: Field attributes.

    2.  In the Properties pane, select the expand match rule icon \(\[Omitted image "match-rule-icon.png"\] Alt text: Match rule icon.\)

    3.  Update the values in the **Comparison Type** or **Comparison Value** fields.

    4.  Clear the **Enabled** option.

        \[Omitted image "terminal-connector-field-match-rule-update.png"\] Alt text: Field match rules.

7.  To match both the screen and its elements with the corresponding rules, locators, or attributes at once, right-click the screen and select **Refresh screen and elements**.

    \[Omitted image "terminal-connector-match-screen-element.png"\] Alt text: Match screen and element.

    The element match icon \(\[Omitted image "screen-match-icon.png"\] Alt text: Screen match icon\) appears for the screen and its elements and the corresponding rules, locators, or attributes.

    \[Omitted image "terminal-connector-match-all.png"\] Alt text: Screen and element match.


**Parent Topic:**[Configure the Terminal connector](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/integrate-applications/rpa-hub/configure-terminal-connector.md)

