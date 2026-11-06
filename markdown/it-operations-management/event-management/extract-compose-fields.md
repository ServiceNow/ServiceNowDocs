---
title: Alert field extraction, composition, and value mapping
description: Enrich automations let you extract values from event payload fields, combine multiple alert fields into a single output field, and map existing alert field values to new values. These actions help standardize alert data for filtering, grouping, and analysis.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/australia/it-operations-management/event-management/extract-compose-fields.html
release: australia
product: Event Management
classification: event-management
topic_type: concept
last_updated: "2026-11-01"
reading_time_minutes: 5
breadcrumb: [Create Enrich automation, Alert automation in SOW for ITOM, Event Management, ITOM AIOps, IT Operations Management]
---

# Alert field extraction, composition, and value mapping

Enrich automations let you extract values from event payload fields, combine multiple alert fields into a single output field, and map existing alert field values to new values. These actions help standardize alert data for filtering, grouping, and analysis.

## Extracting alert fields

Alert notifications often contain relevant context buried within event payloads. By enriching alert outputs with values from the existing payload, you can better understand the significance of alerts and determine the appropriate steps for resolution. For example, a host name typically includes crucial information such as service, node, cluster, datacenter, and domain. To automatically add the value for a cluster tag based on incoming host data, you can extract just the cluster data.

When extracting alert fields, use regular expressions \(regex\) to build value formulas. Regex allows you to precisely identify and capture the relevant portions of the payload, enabling the creation of meaningful and actionable alert notifications.

**Note:** You can compose text using regular expression \(regex\) format conventions. Use one or more capture groups with parentheses to extract parts of the input. Capture groups in the regular expression are assigned to alert outputs based on the order in which they appear. The regex must match the entire input, so consider surrounding your regex with `.*` on each end. For example, `(\w+).acme.com.*` captures the host name in a fully qualified domain name. The parser for the regex engine is Perl Compatible Regular Expressions \(PCRE\) compatible.

\[Omitted image "sow-extract-alert-fields-1.png"\] Alt text: Extract alert fields

If you use multiple capture groups with parentheses, each extracted value appears in a separate output field.

\[Omitted image "sow-extract-alert-fields-2.png"\] Alt text: Extract field for multiple alert outputs

Preview the alert output across example events to verify that the values are extracted as expected by selecting **Preview multiple events**.

**Note:** This option is available only when example source events are available and matched with the regex filter.

## Example: Extracting alert fields

Suppose you need to extract only six letters from a specific field of an event and display them in a new alert field named `mynewfield`. You also want to tag this new alert field for later use in alert grouping. Here's how you can achieve this:

-   **Source input field**: Select the event field from which you want to extract data. In this case, the field is **Metric Name**.
-   **Regular expression**: Use a regular expression to extract the specific part you need from the selected field's value. For example, if the **Metric Name** field value contains "Free swap space in %" and you want to extract "Free swap", your regular expression must be \(.........\).\*.
-   **Alert output**:

    -   Choose an existing alert field, an existing alert tag, or manually enter a new field name. In this case, let's enter a new field name `mynewfield`.
    -   Set `mynewfield` as a tag for later use in tag-based grouping. Notice the tag displayed before the field name.
    After applying the regular expression to the selected field's value \(in this case the **Metric Name** field value\), verify the extracted word displayed below the **Alert output** field. For instance, it should show "Free swap" if the regular expression matches correctly.

-   **Preview multiple events**: Previewing multiple events allows you to verify if the regular expression accurately extracts data from a range of example events. This helps determine if any adjustments to the regular expression are needed.

## Composing alert fields

When creating an alert output, you can select or manually enter fields, tags, or free text to include. This data can be easily read, filtered, and grouped for better management and understanding of the alerts.

\[Omitted image "sow-extract-alert-fields-3.png"\] Alt text: Compose alert fields

## Example: Composing alert fields

Suppose you want to have two input fields that compose data and display it in two different alert output field. In one scenario, you want the source value to come from an existing alert field along with a new field, showing the composed value in a new alert output field. You also plan to tag the new alert output field for later use in tag-based grouping. In the other scenario, you combine existing fields with free text and select the alert output to display in an existing alert field. Here's how you can achieve this:

-   Scenario 1:
    1.  **Source input field**: Select an existing alert field and add the text "and", followed by entering another field **u\_eventid**. For example: $\{classification\} and $\{u\_eventid\}.

        Note that alert fields are displayed in the `${field}` syntax format. You can also select the field name from the drop-down list, and the syntax will be added automatically.

    2.  **Alert output**: Enter the name of the new alert field where you want to display the values from the input fields. For example, let's name it `mynewfield`.

        Set `mynewfield` as a tag for later use in tag-based grouping. Notice the tag displayed before the field name.

-   Scenario 2:
    1.  **Source input field**: Select existing alert fields and include any desired free text for how you want them to appear in the alert output field. For example: Problem type: $\{type\} with severity $\{severity\}.

        Alert fields are displayed in the `${field}` syntax format. You can also select the field name from the drop-down box, and the syntax will be added automatically.

    2.  **Alert output**: Select an existing alert field where you want to display the values from the input fields. For instance, select **Description**.

## Changing alert values

Use the **Change alert values** action to map existing alert field values to new values. This action helps standardize data received from different monitoring tools for consistent filtering and grouping.

For example, you can map the **Severity** field value `DOWN` to `2` and `UP` to `5`. The specified replacement values are applied when the enrichment automation runs.

For instructions on configuring value mappings, see [Create Enrich automation](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/australia/it-operations-management/event-management/enrich-alert-sow-itom.md).

