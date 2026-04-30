---
title: Extracting and composing alert fields
description: Extracting and composing are ways to manage what you see in the alert output, making it simpler to filter, group, and read. Alert automation enables you to extract values from event payload's alert field and place it in an alert output field. Composing allows you to merge multiple alert fields into a single output field.
locale: en-US
release: xanadu
product: Service Operations Workspace for ITOM Apps
classification: service-operations-workspace-for-itom-apps
topic_type: concept
last_updated: "2024-08-01"
reading_time_minutes: 4
breadcrumb: [Create Enrich automation, Alert automation in Service Operations Workspace for ITOM, Using Service Operations Workspace for ITOM, Service Operations Workspace for ITOM, ITOM Health, IT Operations Management]
---

# Extracting and composing alert fields

Extracting and composing are ways to manage what you see in the alert output, making it simpler to filter, group, and read. Alert automation enables you to extract values from event payload's alert field and place it in an alert output field. Composing allows you to merge multiple alert fields into a single output field.

## Extracting alert fields

Alert notifications often contain relevant context buried within event payloads. By enriching alert outputs with values from the existing payload, you can better understand the significance of alerts and determine the appropriate steps for resolution. For example, a host name typically includes crucial information such as service, node, cluster, datacenter, and domain. To automatically add the value for a cluster tag based on incoming host data, you can extract just the cluster data.

When extracting alert fields, use regular expressions \(regex\) to build value formulas. Regex allows you to precisely identify and capture the relevant portions of the payload, enabling the creation of meaningful and actionable alert notifications.

**Note:** You can compose text using regular expression \(regex\) format conventions. Use one or more capture groups with parentheses to extract parts of the input. Capture groups in the regular expression are assigned to alert outputs based on the order in which they appear. The regex must match the entire input, so consider surrounding your regex with `.*` on each end. For example, `(\w+).acme.com.*` captures the host name in a fully qualified domain name. The parser for the regex engine is Perl Compatible Regular Expressions \(PCRE\) compatible.

![Extract alert fields](../image/sow-extract-alert-fields.png "Extract alert fields")

If you use multiple capture groups with parentheses, each extracted value appears in a separate output field.

![Extract field for multiple alert outputs](../image/sow-extract-multiple-alert-fields.png "Extract field for multiple alert outputs")

Preview the alert output across example events to verify that the values are extracted as expected by selecting **Preview multiple events**.

**Note:** This option is available only when example source events are available and matched with the regex filter.

## Example: Extracting alert fields

Suppose you need to extract only six letters from a specific field of an event and display them in a new alert field named `mynewfield`. You also want to tag this new alert field for later use in alert grouping. Here's how you can achieve this:

-   **Source input field**: Select the event field from which you want to extract data. In this case, the field is **Resource**.
-   **Regular expression**: Use a regular expression to extract the specific part you need from the selected field's value. For example, if the Resource field value contains "Zabbix integration" and you want to extract "Zabbix", your regular expression must be \(…...\).\*.
-   **Alert output**:

    -   Choose an existing alert field, an existing alert tag, or manually enter a new field name. In this case, let's enter a new field name `mynewfield`.
    -   Set `mynewfield` as a tag for later use in tag-based grouping. Notice the tag displayed before the field name.
    After applying the regular expression to the selected field's value \(in this case the **Resource** field value\), verify the extracted word displayed below the **Alert output** field. For instance, it should show "Zabbix" if the regular expression matches correctly.

-   **Preview multiple events**: Previewing multiple events allows you to verify if the regular expression accurately extracts data from a range of example events. This helps determine if any adjustments to the regular expression are needed.

## Composing alert fields

When creating an alert output, you can select or manually enter fields, tags, or free text to include. This data can be easily read, filtered, and grouped for better management and understanding of the alerts.

![Compose alert fields](../image/sow-compose-alert.png "Compose alert fields")

## Example: Composing alert fields

Suppose you want to have two input fields that compose data and display it in two different alert output field. In one scenario, you want the source value to come from an existing alert field along with a new field, showing the composed value in a new alert output field. You also plan to tag the new alert output field for later use in tag-based grouping. In the other scenario, you combine existing fields with free text and select the alert output to display in an existing alert field. Here's how you can achieve this:

-   Scenario 1:
    1.  **Source input field**: Select an existing alert field and add the text "and", followed by entering a new field name such as `NewTest`. For example: $\{classification\} and $\{NewTest\}.

        Note that alert fields are displayed in the `${field}` syntax format. You can also select the field name from the drop-down list, and the syntax will be added automatically.

    2.  **Alert output**: Enter the name of the new alert field where you want to display the values from the input fields. For example, let's name it `mynewfield`.

        Set `mynewfield` as a tag for later use in tag-based grouping. Notice the tag displayed before the field name.

-   Scenario 2:
    1.  **Source input field**: Select existing alert fields and include any desired free text for how you want them to appear in the alert output field. For example: $\{ci\_type\} and $\{node\} with state $\{resolution\_state\}.

        Alert fields are displayed in the `${field}` syntax format. You can also select the field name from the drop-down box, and the syntax will be added automatically.

    2.  **Alert output**: Select an existing alert field where you want to display the values from the input fields. For instance, select **Description**.

