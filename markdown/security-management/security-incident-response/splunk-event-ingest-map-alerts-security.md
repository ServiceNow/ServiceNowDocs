---
title: Map notable events
description: During the notable event field-mapping step, you map individual event fields from notable events to fields on a ServiceNow AI Platform Security Incident Response \(SIR\) security incident.
locale: en-US
release: australia
product: Security Incident Response
classification: security-incident-response
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 10
breadcrumb: [Set up a profile for scheduled notable event ingestion, Create an event profile, Splunk Enterprise Security event ingestion integration, Security Incident Response integrations, Security Incident Response, Enterprise security case management applications, Security Operations]
---

# Map notable events

During the notable event field-mapping step, you map individual event fields from notable events to fields on a ServiceNow AI Platform Security Incident Response \(SIR\) security incident.

## Before you begin

Role required: sn\_si.ingestion\_profile\_admin

**Note:** Users with the sn\_si.admin role can perform all operations available to a profile admin, as the sn\_si.admin role inherits the required permissions by default.

## About this task

The mapping grid can be customized for the notable event type selected in the correlation rule selection. Color-coding of the event fields helps you keep track of the event values that you have already mapped as they become grayed out while all remaining unmapped fields appear in blue. This helps you better visualize which field values have been added to the security incident and if any remaining important event information remains unmapped.

Map up to five notable events from the Notable Event Sample Ingestion column on the left of the form to the security incident fields in the SIR Incident Field Mapping column on the right.

Create custom mappings by adding or removing the fields on the mapping grid on the right side of the form. Default fields that are typically important field to populate on the security incident response form are displayed. However, these fields can be removed and any additional fields can be displayed using the + and - buttons. Create custom maps by adding or removing the fields on the mapping grid on the right side of the form. Customizing the fields permits you to map Splunk fields that are not displayed on the default-mapping grid on the SIR security incident.

## Procedure

1.  If the mapping form is not displayed, select **Mapping** on the progress bar.

2.  For a profile with a scheduled ingestion, below Notable Event Sample Ingestion, click **Fetch Sample Data** to pull the latest sample notable events from the Splunk Enterprise console for the correlation rule selected.

    **Note:** You can either pull the most recent sample notable events or provide the unique notable event IDs for the specific notable events that you want to use for your notable event mapping experience.

    The notable event fields and values results are displayed as individual tabs. You can ingest up to five notable events.

    The pull for sample notable events may take a few moments. A message indicating that the transaction is working is displayed at the top of the screen.

    Field-name value pairs for the ingested notable event, or the imported sample events, are displayed on the left side of this form after the ingestion pull is completed. These values are the values that you map to the security incident fields on the SIR Incident Field Mapping side of the form.

3.  To map a field value from the left side of the form to a field on the security incident on the right side of the form, click-hold a blue field name on the left side of the form.

4.  Drag the field name, for example, `rule_name`, and drop it on a field in the Input Expression column next to a field name in the Security Incident column.

    ![Drag-and-drop for values shown by arrow.](../image/splunk_es_drag_drop.png)

    The field value is displayed in the Input Expression column. In the following image, `rule_name` is mapped to the `Short description` field on the security incident. However, you can match any value from the left side to a field on the right. Verify that the value is mapped correctly on the security incident during the preview step.

    To help you ensure that no event fields are overlooked or duplicated in the mapping process, fields are color-coded. Light blue fields on the left indicate that a notable event field is not yet selected and mapped on the security incident. You may prefer to associate an incoming notable field with more than one field on a security incident.

    A gray field indicates that a field has been selected and mapped to a field on the security incident. This color-coding helps you track the mapping.

    ![Short description field and value on security incident highlighted](../image/splunk_es_map_3_security.png)

5.  To add fields to the default fields displayed on the security incident on the right side of the form, follow these steps.

    1.  On the right of the form in the SIR Incident Field Mapping section, at the bottom of the grid, click the plus icon.

        A new field is displayed.

    2.  In the Security Incident column, expand the list that is displayed, and select a field.

        ![Category field mapping](../image/splunk_es_map_4_security.png)

        **Note:** So that multiple observables can be displayed on the same security incident, the Observable field can be mapped multiple times with different values. Similarly, the Configuration Item and Work notes fields support multiple values. If you try to map two values to a field that cannot support multiple values, when you preview the incident, an error message is displayed that there is no value for the field. Similarly, if a field on a security incident has a list from which you can choose multiple options, and you try to map an option to that field that is not displayed on the list, the field is not populated on the security incident.

    3.  Alternatively, type a value in the Search field for the new row.

    4.  From the left side of the form, left-click to select the **Event ID** that you want in the Input Expression field.

6.  Continue mapping by adding or removing field values to the mapping.

    The following figure is an example of an edited mapping. In the bottom field on the right, the Work notes field is added, and it has more than one value. Note that for long text string field, you can expand the mapping field to see the full string and re-size as needed by pulling the lower right corner of the field as indicated in screen shot below with the added Work notes field:

    ![Work notes with multiple values highlighted](../image/splunk_es_mapexample_security.png)

    **Warning:** Please note that in the **SIR Incident Field Mapping** section, the URL and port number mentioned in the **Input Expression** field is just an example and not the URL or port number provided out-of-the-box.

    In the preview, these values are displayed in the Work notes on the security incident. Because the value is for a field that you added to the mapping section, and there are multiple values mapped to the Work notes field, the values are displayed as entered. In this example, the spaces and punctuation marks that you entered in the field are displayed on the Related Items section as a work note on the preview of the security incident.

7.  To receive updates for the mapped fields in SIR, select **Enable Updates** check box against the Input Expression.![Enable updates check box selected](../image/splunk_es_enable_updates.png)

8.  After you have completed the preceding field-mapping steps, you can use the same field values in the Incident Generation Conditions builder to define additional criteria that an incoming notable event must satisfy to create a SIR security incident.

    To set incident generation conditions, follow these steps.

    1.  Scroll to the Incident Generation Conditions section on the form and select the **Filter based on conditions** check box to enable the option.

        The Filter conditions builder is displayed. Use these filters to create security incidents that match the specific conditions described by the fields.

        The options in the lists for the first field in the Filter conditions builder match the fields that are displayed on the Notable Event Sample Ingestion section for the events you ingested. These fields are dynamic and change depending on the Splunk notable events that you ingest, or the event that you select for the manually forwarded notable event samples. Criteria that you enter are case-sensitive, and they must match exactly the values of the Splunk Enterprise Security notable event. If you are not sure about the values to enter in the filter fields, you may prefer to return to your Splunk Enterprise Security console and review your notable events for the keywords.

    2.  Using the lists and fields of the conditions builder, set filters for the first row.

    3.  To add more conditions, to the right of the fields, click **AND** or **OR**.

        If **AND** is selected, all conditions must be matched. If **OR** is selected, either condition can be matched.

    4.  In the second row, set a second filter condition.

        The following image is an example with two conditions that must be matched before security incidents are created.

        ![Filter conditions builder:2](../image/splunk_es_filters_2_security.png)

        You have set the incident generation conditions so that security incidents are created only when both of the filtering conditions that you entered are matched.

        This type of incident generation condition filtering helps you narrow down the security events, and limit the number of unnecessary security incidents that you create without modifying the underlying correlation search or filters in Splunk. If additional filtering criteria are set, only notable events that match all criteria are mapped to incidents.

        **Note:** If any of the event field names have special characters such as quotes \(“\), hyphens \(‘\), underscores \(-\), at \(@\), or ampersands \(&amp;\), these characters may must be replaced for mapping translation purposes and possibly create a duplicate event name. The mapping can be done appropriately but a numerical suffix is appended to differentiate fields with duplicate event names. For example, if the first event field is `alerts.alert` and the second event field is `alerts@alerts`, these fields cannot be uniquely identified as the remaining standard text characters are the same. In this case, a suffix is added to the second event field and the field is renamed to `alerts@alert(1)`.

    Event Aggregation Criteria to Handle Similar Notables and Prevent Duplicate Incidents

9.  To avoid creating duplicate security incidents, define additional event aggregation criteria so that incoming notable events are aggregated to an open security incident.

    To set the criteria, follow these steps below.

    1.  Scroll to the Event Aggregation Criteria section on the form and select the **Aggregate Conditions** check box to enable this option.

        The Incident fields with matching values are displayed. These field names are the fields on the security incident that include any custom fields that are configured on the SIR security incident.

    2.  From the multi-select input field, select the field values that you want to match on existing security incidents in your ServiceNow AI Platform.

    3.  Use the **Add New Criteria** to select multiple field matching conditions.

        All the field values that you select in the multi-selection input field are matched for aggregation criteria using the AND condition. Select **Add New Criteria** to select multiple field matching conditions where aggregation occurs if any one of the multi-selected field conditions that are defined are met using the OR condition.

        If a new notable event matches all the values that are selected in the aggregation field conditions in the mapping step, the new notable event is automatically added to the most recently opened security incident with the same field values. As a user with the sn\_si.analyst role working with security incidents, you can view all the added aggregate notable events on a related list on a security incident. All of the aggregated notable events on a security incident are displayed on the Splunk Event to Tasks related list. This list details associated timestamps and aggregated field values. This information helps you understand why these notable events are being aggregated to existing security incidents. If this tab is not displayed, scroll to the left side of the record under Related Links and click the **Show All Related Lists** link.

    4.  To log a work note for a new notable event that is recently added on the security incident, select the check box to enable this option.

        The work note logs that a new notable has been added along with a link to the alert details and any other details that may have been added to the work note field in your mapping section.

    You have successfully mapped values from a Splunk notable event to fields on a SIR security incident. Also, you have configured additional conditions to limit the creation of security incidents with incident generation filtering criteria. You also appended notable events to existing SIR security incidents when event field values match the configured aggregation criteria.

10. Choose one to continue with the profile configuration.

<table id="choicetable_svs_ttl_kdb"><thead><tr><th align="left" id="d496407e476">

Option

</th><th align="left" id="d496407e479">

Description

</th></tr></thead><tbody><tr><td id="d496407e485">

** **

</td><td>

 

</td></tr><tr><td id="d496407e492">

**Continue**

</td><td>

The Mapping form is displayed. **Preview** is selected on the progress bar. The next step is to preview the fields you mapped on a SIR security incident.

</td></tr><tr><td id="d496407e509">

**Update**

</td><td>

Your data is saved and the Splunk Event Profiles list is displayed.

</td></tr><tr><td id="d496407e518">

**Previous**

</td><td>

The Notable Event Selection form is displayed.

</td></tr><tr><td id="d496407e528">

**Delete**

</td><td>

Delete this event profile and the Splunk Event Profiles list is displayed.

</td></tr></tbody>
</table>
## What to do next

The next step is to preview the values that you mapped on the security incident. For more information, see [Preview security incident](splunk-event-ingest-preview-security.md).

