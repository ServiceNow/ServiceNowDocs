---
title: Create Enrich automation
description: Alert enrichment involves transforming raw events from monitoring tools into a standard format, aiding automated grouping and response. This includes extracting fields from lengthy alert payloads or composing them into a standardized format. Additionally, you can create tags, which are metadata added to alerts for easier filtering and grouping.
locale: en-US
release: xanadu
product: Service Operations Workspace for ITOM Apps
classification: service-operations-workspace-for-itom-apps
topic_type: task
last_updated: "2024-08-01"
reading_time_minutes: 8
breadcrumb: [Alert automation in Service Operations Workspace for ITOM, Using Service Operations Workspace for ITOM, Service Operations Workspace for ITOM, ITOM Health, IT Operations Management]
---

# Create Enrich automation

Alert enrichment involves transforming raw events from monitoring tools into a standard format, aiding automated grouping and response. This includes extracting fields from lengthy alert payloads or composing them into a standardized format. Additionally, you can create tags, which are metadata added to alerts for easier filtering and grouping.

## Before you begin

Role required: evt\_mgmt\_admin or srm\_responder

## About this task

Extracting takes values from event payload fields and places them in alert output fields, while composing combines multiple alert fields into one. For more information, see [Extracting and composing alert fields](../concept/extract-compose-fields.md).

For users familiar with the classic Event Management experience, enrich automations offer an easier interface with better teams support for the transform and compose step of event rules. Event rules offers more advanced features like binding overrides that are currently only available to admins. Admins may also enrich alerts with event field mapping rules. Additionally, changing alert values creates an event field mapping rule with the mapping type **Map field and transform value \(Single field\)**. This rule is linked to the event rule and runs simultaneously, allowing for streamlined mapping and transformation of event data to enrich alerts.

## Procedure

1.  Navigate to **Workspaces** &gt; **Service Operations Workspace**.

2.  In the primary navigation, select the Alert Automation icon \(![Alert automations icon](../../event-management/image/alert-automations-icon.png)\).

3.  On the Alert automation page, under **Automation types**, select **Enrich**.

    The Enrich alerts page is displayed.

    ![Enrich automation page](../image/enrich-automation-page.png)

4.  Select **Create automation**.

5.  In the **Automation name** field, enter the name of the automation.

    ![Enrich rule page where you can provide automation name, set conditions and actions.](../image/enrich-automation-conditions.png)

6.  Activate the automation by selecting the **Active** check box.

7.  To continue running other enrichment automations with same filter conditions after this automation is executed, enable the **Continue running automations of this type** toggle switch.

    When disabled, additional automations of this type will stop running after this automation is executed once. If the automation is managed by an administrator, it will stop running administrator-owned automations but will continue to run automations owned by other assignment groups.

8.  In the **If these conditions are met** section, set up filter criteria to identify the alerts you want to enrich.

    The condition is evaluated against the raw event received from the source monitoring system and does not account for enriched fields.

    1.  From the **Assignment group** field menu, select the assignment group to determine which team’s alerts will trigger the automation.

        The **Assignment group** represents a specific team responsible for handling certain alerts. By selecting an assignment group, you ensure that only the alerts assigned to that particular team will trigger the automation. This way, the automation is targeted and only activates for relevant alerts associated with the selected team.

        **Note:**

        -   If you’re logged in to the instance with an administrator role \(evt\_mgmt\_admin\), all of the assignment groups are available. Additionally, you can select **All groups** to enable generating alerts for any of the available groups.
        -   If you’re an operator, only the group you’re a part of is available.
        -   Only members of the selected group or administrators can update or delete the automation.
    2.  From the **Source** field menu, select the monitoring tool from where the alert is generated.
    3.  Set up the conditions by selecting the field, operator, and field value. Then, add more conditions using OR or AND operators.

        To add another set of conditions, select **+ New condition set**. You can also manually add an additional info field if you don’t see it in the drop-down list.

9.  In the **Then, apply the following actions** section, select the automation actions that will be triggered by this automation.

    You must select at least one action.

    -   **Extract alert fields**: Retrieves alert field values from the event payload and places them in an alert output field.
    -   **Copy or compose fields**: Merges various alert fields, tags and text to generate a composed alert output.
    -   **Change alert values**: Maps the current value of alert fields to specified new values.
<table id="choicetable_p43_zvd_s1c"><thead><tr><th align="left" id="d279109e269">

Option

</th><th align="left" id="d279109e272">

Action

</th></tr></thead><tbody><tr><td id="d279109e278">

**__Extract alert fields__**

</td><td>

1.  Enable the **Extract alert fields** toggle switch.
2.  From the **Source input field** menu, select a value. The menu displays the standard event fields, additional info, and tags. The field value is then displayed. You can also manually enter a field name that is not displayed and add your own value.

The example source events pane displays a sample of recent events in your system. If no events are displayed, you may create an event, see [Create or edit an event rule](../../event-management/task/create-or-edit-event-rule.md).

3.  In the **Regular expression** field, create a regular expression to extract the value that you want to extract.

**Note:** You can compose text using regular expression \(regex\) format conventions. Use one or more capture groups with parentheses to extract parts of the input. Capture groups in the regular expression are assigned to alert outputs based on the order in which they appear. The regex must match the entire input, so consider surrounding your regex with `.*` on each end. For example, `(\w+).acme.com.*` captures the host name in a fully qualified domain name. The parser for the regex engine is Perl Compatible Regular Expressions \(PCRE\) compatible. Nested JSON data is preprocessed to strip quotes and replace colons with equal signs.

4.  In the **Alert output** field, select an alert field or an alert tag. You can also manually enter a new field name.

If you want to add an alert tag, select the **Set as a tag** check box.

**Tip:** Create alert tags that can be shared across sources for easier filtering and grouping, such as the out-of-the-box tags.

![Extract alert fields](../image/sow-extract-alert-fields.png)

5.  Select **Preview multiple events** to verify that the regular expression \(regex\) is general-purpose enough to correctly extract values across many examples.

**Note:** This option is available only when example source events are available and matched with the regex filter.

![Preview extracted values from multiple events](../image/sow-preview-multiple-events.png)

 To include additional fields for extraction, select **+ Add fields**.

</td></tr><tr><td id="d279109e380">

**__Copy or compose fields__**

</td><td>

1.  Enable the **Copy or compose fields** toggle switch.
2.  From the **Source input field** menu, select alert fields and/or alert tags, manually enter a field name or even add free text. Alert fields are displayed in the `${field}` syntax format.
3.  In the **Alert output** field, select an existing alert field or alert tag, or manually enter an alert field. The **Alert output** field is an enriched alert containing the composed alert data.

For easier grouping, you can select a tag from the menu. If you want to use the new field name as a tag for grouping, select the **Set as a tag** check box.

**Tip:** Create alert tags that can be shared across sources for easier filtering and grouping, such as the out-of-the-box tags.

![Compose alert fields](../image/sow-compose-alert.png)

 To create additional alert data compositions, select **+ Add fields**.

</td></tr><tr><td id="d279109e441">

**__Change alert values__**

</td><td>

1.  Enable the **Change alert values** toggle switch.
2.  In **Alert field**, enter the field in the alert that you want to map values for.
3.  In the **From value** field, enter original value in the alert field that you want to change.
4.  In the **To value** field, enter the new value that will replace the original value in the alert field.

To add more field values, select **+ Add value** and to add more fields to map, select **+ Add field to map**.

</td></tr></tbody>
</table>10. In the **And finally** section, to continue running other enrichment automations with same filter conditions after this automation is executed, select **Run other enrich alert automations**.

    If you select **Don't run other enrich alert automations**, additional automations of this type will stop running after this automation is executed once. If the automation is managed by an administrator, it will stop running administrator-owned automations but will continue to run automations owned by other assignment groups.

11. In the **Automation details** section, provide an order and automation description.

    ![Enrich automation details section](../image/enrich-automation-details.png)

    1.  In the **Order** field, enter the automation order.

        **Note:** Automations run in order from the lowest to the highest. Ensure there are no enrichment automations with a lower order number that have matching conditions and have **Apply additional automations of this type** set to false. Otherwise, this may prevent subsequent automations from running.

        The **Automation is managed by** field displays the team or assignment group who owns, edits, and can delete this automation. The assignment group is the same as the one defined in the **If these conditions are met** section.

    2.  In the **Automation description** field, enter a brief description of the automation.
12. Select **Save automation**.

    A notification appears when the automation is successfully saved. Otherwise, an error message is displayed. The enrich automation that you created appears on the Enrich alerts page where you can view, edit, or delete the existing automation.


## What to do next

You can manage alerts more effectively by grouping similar alerts together with the help of [Create Group automation](group-alert-sow-itom.md).

**Related topics**  


[Extracting and composing alert fields](../concept/extract-compose-fields.md)

