---
title: Create Enrich automation
description: Alert enrichment involves transforming raw events from monitoring tools into a standard format, aiding automated grouping and response. This includes extracting fields from lengthy alert payloads or composing them into a standardized format. Additionally, you can create tags, which are metadata added to alerts for easier filtering and grouping.
locale: en-US
release: australia
product: Service Operations Workspace for ITOM Apps
classification: service-operations-workspace-for-itom-apps
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 12
breadcrumb: [Alert automation in SOW for ITOM, Using SOW for ITOM, Service Operations Workspace for ITOM, ITOM AIOps, IT Operations Management]
---

# Create Enrich automation

Alert enrichment involves transforming raw events from monitoring tools into a standard format, aiding automated grouping and response. This includes extracting fields from lengthy alert payloads or composing them into a standardized format. Additionally, you can create tags, which are metadata added to alerts for easier filtering and grouping.

## Before you begin

Role required: evt\_mgmt\_admin, evt\_team\_operator, or srm\_responder

## About this task

Extracting takes values from event payload fields and places them in alert output fields, while composing combines multiple alert fields into one. For more information, see [Extracting and composing alert fields](../concept/extract-compose-fields.md).

For users familiar with the classic Event Management experience, enrich automations create event rules but with an easier interface and with better teams support. Event rules offer a few advanced features like thresholds and CI identification using IRE that are not yet available in enrich automations. Admins may also enrich alerts with event field mapping rules. Changing alert values creates an event field mapping rule with the mapping type **Map field and transform value \(Single field\)**. This rule is linked to the event rule and runs simultaneously, allowing for streamlined mapping and transformation of event data to enrich alerts.

## Procedure

1.  Navigate to **Workspaces** &gt; **Service Operations Workspace**.

2.  From the bottom of the navigation pane, select the AIOps configuration center icon ![ITOM AIOps configuration center icon](../../health-log-analytics-admin/image/icon-itom-aiops-config.png).

    The ITOM AIOps configuration center page appears. The configuration center is a centralized workspace. Use it to configure and manage AIOps features from a single place.

3.  On the ITOM AIOps configuration center page, under the Optimize section, select **Enrich alerts**.

    The Enrich alerts page is displayed.

    ![Enrich automation page](../image/enrich-automation-page.png)

4.  Select **Create automation**.

    By default, the **Active** check box is selected.

5.  In the **Automation name** field, enter the name of the automation for enriching alerts.

6.  In the **If these conditions are met** section, set up filter criteria to identify the alerts you want to enrich.

    The condition is evaluated against the raw event received from the source monitoring system and does not account for enriched fields.

    1.  From the **Assignment group** field menu, select the assignment group to determine which team’s alerts will trigger the automation.

        The **Assignment group** represents a specific team responsible for handling certain alerts. By selecting an assignment group, you ensure that only the alerts assigned to that particular team will trigger the automation. This way, the automation is targeted and only activates for relevant alerts associated with the selected team.

        **Note:**

        -   If you’re logged in to the instance with an administrator role \(evt\_mgmt\_admin\), all of the assignment groups are available. Additionally, you can select **All groups** to enable generating alerts for any of the available groups.
        -   If you’re an team operator, only the groups you’re a member of are available.
        -   Only members of the selected group or administrators can update or delete the automation.
    2.  From the **Source** field menu, select the monitoring tool from where the alert is generated.
    3.  Set up the conditions by selecting the field, operator, and field value. Then, add more conditions using OR or AND operators.

        To add another set of conditions, select **+ New condition set**. You can also manually add an additional info field if you don’t see it in the drop-down list.

        **Note:** Select **Load past events** to view previous events when creating the automation.

        ![Enrich rule page where you can provide automation name, set conditions and actions.](../image/enrich-automation-conditions.png)

7.  In the **Then, apply the following actions** section, select the automation actions that will be triggered by this automation.

    You must select at least one action.

    -   **Extract alert fields**: Retrieves alert field values from the event payload and places them in an alert output field.
    -   **Copy or compose fields**: Merges various alert fields, tags and text to generate a composed alert output.
    -   **Change alert values**: Maps the current value of alert fields to specified new values.
    -   **Improve configuration item \(CI\) identification**: Identifies CIs other than a host for better alert grouping, team assignment, and service health.
<table id="choicetable_p43_zvd_s1c"><thead><tr><th align="left" id="d199368e268">

Option

</th><th align="left" id="d199368e271">

Action

</th></tr></thead><tbody><tr><td id="d199368e277">

**__Extract alert fields__**

</td><td>

1.  Enable the **Extract fields** toggle switch.
2.  From the **Extract from field** menu, select a value. The menu displays the standard event fields, additional info, and tags. The field value is then displayed. You can also manually enter a field name that is not displayed and add your own value.

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

</td></tr><tr><td id="d199368e379">

**__Copy or compose fields__**

</td><td>

1.  Enable the **Copy or compose fields** toggle switch.
2.  From the **Composition** field, select alert fields and/or alert tags, manually enter a field name or even add free text. Alert fields are displayed in the `${field}` syntax format.
3.  In **Output to field**, select an existing alert field or alert tag, or manually enter an alert field. **Output to field** is an enriched alert containing the composed alert data.

For easier grouping, you can select a tag from the menu. If you want to use the new field name as a tag for grouping, select the **Set as a tag** check box.

**Tip:** Create alert tags that can be shared across sources for easier filtering and grouping, such as the out-of-the-box tags.

![Compose alert fields](../image/sow-compose-alert.png)

 To create additional alert data compositions, select **+ Add fields**.

</td></tr><tr><td id="d199368e447">

**__Change alert values__**

</td><td>

1.  Enable the **Change alert values** toggle switch.
2.  In **Alert field to change values for** field, enter the field in the alert that you want to map values for.
3.  In the **When value is** field, enter original value in the alert field that you want to change.
4.  In the **Change it to** field, enter the new value that will replace the original value in the alert field.

To add more field values, select **+ Add value** and to add more fields to map, select **+ Add field to map**.

![Change values of a field to a format that is easier to read, filter, and group.](../image/sow-change-alert-values.png)

</td></tr><tr><td id="d199368e503">

**Improve configuration item \(CI\) identification**

</td><td>

This option allows you to change how alerts are bound or linked to a Configuration Item \(CI\), ensuring alerts are associated with the correct IT components for better visibility and faster issue resolution.

 The default and most common way to bind alerts to CIs is based on the **Node** field. This works out of the box with no configuration needed. Use it by populating the **Node** field in your alert with a CI’s Name, Fully Qualified Domain Name \(FQDN\), IP, or MAC address. This supports host CIs including Computers, Operating Systems \(OS\), Switches, Routers, or any CI type or any class that extends the \[cmdb\_ci\_hardware\] table.

 You may enable this action to improve the CI identification for other types of CIs such as processes or service instances. The system searches for a matching CI in the appropriate CMDB table based on the selected CI type. For example, if you select VMware Virtual Machine Instance as the CI class, the system searches for a matching record in the \[cmdb\_ci\_vmware\_instance\] table using details from the event rule record, specifically the **Additional info** fields.

 ![Improve configuration item (CI) identification section](../image/enrich_automation_ci_identification.png)

 1.  Enable the **Improve configuration item \(CI\) identification** toggle switch.
2.  **Select which CI class you’d like to identify**: In the **CI class** field, specify the CI class for which the event’s node field is evaluated during CI identification. This determines the type of CI the system attempts to identify first.

Select **View items** to see the list of CIs of this type and their attribute values.

3.  **Identify the CI when the following alert fields match the CI attributes**: In this section, map alert fields to CI attributes to help the system find the correct CI:
    -   **Alert field**: Select the alert field that contains identifying information.
    -   **CI attribute**: Select the CI attribute that the alert field must map to.
4.  Use Advanced options to control how the system treats the alert node field during CI identification.

    -   Node field behavior: Choose one of the following:

        -   Consider node field: Uses the alert’s node value during CI identification.
        -   Ignore node field: Ignores the alert’s node value.
Based on the selected CI class, the system recommends whether you should consider or ignore the node field, but you can override this recommendation if needed.

    -   Use all matching additional info fields: Select this check box to use all matching fields from the event’s Additional Info for CI identification instead of mapping individual fields.
5.  **+ Add fallback**: Add fallback CI class and field mappings to define alternate identification logic. If the primary configuration does not identify a CI, the system evaluates each fallback in order until it finds a match.

Ensure that the **Node** field in the alert is populated correctly to identify a host CI. The CI you are identifying must have a [runs on](../../event-management/task/t_EMBindApplication.md) relationship to the host CI or be [mapped to the host](../../event-management/task/ci-device-binding.md).

6.  Ensure that at least one CI attribute is present in the **Additional info** field of the alert.

For instructions on how to populate these fields, see [Set additional info fields to match CI attribute format](set-addi-info-field-match-ci-attribute.md). The system attempts to match values from the **Additional info** field of the alert with the CI table. If a match is found, the alert is bound to the corresponding CI.

7.  Select **Test CI identification** to test the CI identification on sample events.

After successful CI identification, the system displays a message with the relevant details.![CI identification is successful](../image/enrich_automation_ci_binding_success.png)

If CI identification fails, the system shows a message explaining the details.![CI identification failed](../image/enrich_automation_ci_binding_failed.png)

 For more information on CI binding, see [Binding alerts to CIs](../../event-management/concept/ci-binding-alert.md).

</td></tr></tbody>
</table>8.  In the **And finally** section, to continue running other enrichment automations with same filter conditions after this automation is executed, select **Run other enrich alert automations**.

    ![Option to select whether you want to run other enrich alert automations.](../image/enrich-run-other-automation.png)

    If you select **Don't run other enrich alert automations**, additional automations of this type will stop running after this automation is executed once. If the automation is managed by an administrator, it will stop running administrator-owned automations but will continue to run automations owned by other assignment groups.

9.  In the **Automation details** section, provide an order and automation description.

    ![Enrich automation details section](../image/enrich-automation-details.png)

    1.  In the **Order** field, enter the automation order.

        **Note:** Automations run in order from the lowest to the highest. Ensure there are no enrichment automations with a lower order number that have matching conditions and have **Apply additional automations of this type** set to false. Otherwise, this may prevent subsequent automations from running.

        During alert processing, enrichment automations assigned to specific teams are applied first, based on the **Order** field. After these are evaluated, enrichment automations assigned to **Global / All groups** are applied. If multiple automations match, the automation with the highest order value is selected to improve CI identification.

        The **Automation is managed by** field displays the team or assignment group who owns, edits, and can delete this automation. The assignment group is the same as the one defined in the **If these conditions are met** section.

    2.  In the **Automation description** field, enter a brief description of the automation.
10. Select **Save automation**.

    A notification appears when the automation is successfully saved. Otherwise, an error message is displayed. The enrich automation that you created appears on the Enrich alerts page where you can view, edit, or delete the existing automation.


## What to do next

You can manage alerts more effectively by grouping similar alerts together with the help of [Create Group automation](group-alert-sow-itom.md).

**Related topics**  


[Extracting and composing alert fields](../concept/extract-compose-fields.md)

