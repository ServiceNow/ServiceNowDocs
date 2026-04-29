---
title: Map alerts for the Splunk Enterprise Event Ingestion integration
description: During the event field-mapping step, you map individual event fields from triggered alerts or imported event data to fields on a ServiceNow AI Platform Security Incident Response \(SIR\) security incident.
locale: en-US
release: australia
product: Security Incident Response
classification: security-incident-response
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 11
breadcrumb: [Create an event profile, Splunk Enterprise Event Ingestion integration for Security Operations by ServiceNow, Security Incident Response integrations, Security Incident Response, Enterprise security case management applications, Security Operations]
---

# Map alerts for the Splunk Enterprise Event Ingestion integration

During the event field-mapping step, you map individual event fields from triggered alerts or imported event data to fields on a ServiceNow AI Platform Security Incident Response \(SIR\) security incident.

## Before you begin

Role required: sn\_si.ingestion\_profile\_admin

**Note:** Users with the sn\_si.admin role can perform all operations available to a profile admin, as the sn\_si.admin role inherits the required permissions by default.

## About this task

The preconfigured mapping grid of the default security incident fields can be edited. The color-coding of the event fields helps you monitor the field values that you have already mapped. This step helps you visualize how your edits impact the fields on the security incident.

Map up to five alerts from the Alert Sample Ingestion column on the left of the form to the security incident fields in the SIR Incident Field Mapping column on the right.

Create custom maps by adding or removing the fields on the mapping grid on the right side of the form. Customizing the fields permits you to map Splunk fields that are not displayed on the default-mapping grid on the SIR security incident.

## Procedure

1.  If the mapping form is not displayed, select **Mapping** on the progress bar.

2.  For a profile with a scheduled alert, below Alarm Sample Ingestion, select the alert in the **Alert Name** and select **Fetch Sample Data** to pull the latest instance of a fired alert from the Splunk Enterprise console.

    The alerts are displayed as tabs. You can ingest up to five of the most recent alerts.

    The pull for sample events may take a few moments. A message indicating that the transaction is working is displayed at the top of the screen.

    **Note:** An additional mapping field, **Splunk Alert Name**, is added by the integration to allow for tracing an event to the source alert rule in Splunk. This may be helpful in scenarios where multiple Splunk alerts are combined into a single profile.

    When a single field contains multiple values, those values are parsed and mapped to individual field entries on the SIR incident field mapping section. For example, the source IP addresses, asset names, or URLs may have multiple observable field entries or multiple CIs, those are parsed and mapped to individual field entries on the SIR incident field mapping section.

    The field-name value pairs for the ingested alert, or the imported sample event, are displayed on the left side of this form after the pull is completed. These values are the values that you map to the security incident fields on the SIR Incident Field Mapping side of the form.

3.  For scheduled alert profiles, proceed to step five to map the values.

4.  Alternatively, for a profile for an event type that you want to export from your Splunk Enterprise console, follow these steps to upload attachment data in your ServiceNow AI Platform® instance.

    1.  If not already logged in, log in to your Splunk Enterprise console.

    2.  Navigate to the Search tab and enter a name for a search that has the event data that you want to export.

        For example, malware is a search term used for all malware events that you can forward with the workflow of this integration.

    3.  Expand the event, and in the Field column, select the fields that you want to import.

        These fields are the field-value pairs that are exported and displayed on the Mapping page in your ServiceNow AI Platform® instance.

    4.  In your Splunk Enterprise console, in the upper right of the Search page, select **Export** icon.

    5.  In the list for the Format field in the dialog that is displayed, select **XML Format**.

    6.  Enter a new filename.

    7.  Select **Export**.

        The file is downloaded to your ServiceNow AI Platform® instance.

    8.  If the Mapping page is not already displayed in your ServiceNow AI Platform® instance, select **Mapping** in the progress bar.

    9.  In the Alert Sample Ingestion column, select **Load Attachment Data**.

    10. In the dialog that is displayed, select **Choose files** and navigate to the `.xml` file that you exported and select **Open**.

        The value pairs for the fields that you exported for the event are displayed on the left side of the mapping form.

        In the following figure, the data pairs for an ingested scheduled alert are displayed on the left side of this form. Value pairs for imported events are also displayed on this side of the form. These values are the field values that you map to the security incident fields on the Sir Incident Field Mapping side of the form.

5.  To map a field value from the left side of the form to a field on the security incident on the right side of the form, select-hold a blue field name on the left side of the form.

6.  Drag the field name, for example, `host`, and drop it on a field in the Input Expression column next to a field name in the Security Incident column.

    ![Drag-and-drop for values shown by arrow.](../image/splunk-event-ingestion-alerts-mapping_category.png)

    The field value is displayed in the Input Expression column. In the following image, `category` is mapped to the `category` field on the security incident. However, you can match any value from the left side to a field on the right. Verify that the value is mapped correctly on the security incident during the preview step.

    To help you ensure that no events are overlooked or duplicated in the mapping process, fields are color-coded. Light blue fields on the left indicate that a field is not yet selected and mapped on the security incident. You may prefer to associate an incoming alert field with more than one field on a security incident.

    A gray field indicates that a field has been selected and mapped to a field on the security incident. This color-coding helps you track the mapping, because in certain cases, alert event fields may only be assigned once. For instance, you can only assign values to fields such as Short Description once. However, you can assign list fields such as Work Note multiple times by adding additional rows to the mapping grid.

7.  To add fields to the default mapping of the security incident on the right side of the form, follow these steps.

    1.  On the right of the form in the SIR Incident Field Mapping section, at the bottom of the grid, select the plus icon.

        A new field is displayed.

    2.  In the Security Incident column, expand the list that is displayed, and select a field.

        In the expanded list for the new field, some fields are shaded. In the following figure, `Category` has a gray background, because it has been mapped in the security incident. Similar to the color-coding for alert fields on the left side of the form, this color-coding for the security incident fields on the right helps you track the mapping.

        ![Location field on choice list for new field.](../image/214_splunk_map_4.png)

        **Note:** So that multiple observables can be displayed on the same security incident, the Observable field can be mapped multiple times with different values. Similarly, the Configuration Item and Work notes fields support multiple values. If you try to map two values to a field that cannot support multiple values, when you preview the incident, an error message is displayed that there is no value for the field. Similarly, if a field on a security incident has a list from which you can choose multiple options, and you try to map an option to that field that is not displayed on the list, the field is not populated on the security incident.

    3.  Alternatively, type a value in the Search field for the new row.

    4.  From the left side of the form, left-click to select the **Alert ID** that you want in the Input Expression field.

        With the drag feature, map it next to your new field.

8.  Continue mapping by adding or removing fields and adding values to the map.

    The following figure is an example of an edited mapping grid. In the bottom field on the right, the Work notes field is added, and it has more than one value. The values are separated by spaces and punctuation marks \(`${_time}$ | $(source}$ | ${Splunk Alert Name)$`\).

    ![Work notes with multiple values highlighted.](../image/splunkmapexample_v2.png)

    In the preview, these values are displayed in the Work notes on the security incident. Because the value is for a field that you added to the grid, and there are multiple values mapped to the Work notes field, the values are displayed as entered. In this example, the spaces and punctuation marks that you entered in the field are displayed on the Related Items section as a work note on the preview of the security incident.

    Incident generation filtering conditions

9.  After you have completed the preceding field-level mapping steps, you can use the same field values in the Filter conditions builder to define additional criteria that an incoming alert must satisfy to create a SIR security incident.

    To set filtering conditions, follow these steps.

    1.  Scroll to the Incident Generation Conditions section on the form and select the **Filter based on conditions** check box to enable the option.

        The Filter conditions builder is displayed. Use these filters to create security incidents that match the specific conditions described by the fields.

        The options in the lists for the first field in the Filter conditions builder match the fields that are displayed on the Alert Sample Ingestion section for the alert you ingested. These fields are dynamic and change depending on the Splunk alert that you ingest, or the event that you manually forward. Criteria that you enter are case-sensitive, and they must match exactly the values of the Splunk Enterprise alert or event. If you are not sure about the values to enter in the filter fields, you may prefer to return to your Splunk Enterprise console and review your alerts and events for the keywords.

    2.  Using the lists and fields of the conditions builder, set filters for the first row.

    3.  To add more conditions, to the right of the fields, select **AND** or **OR**.

        If **AND** is selected, all conditions must be matched. If **OR** is selected, either condition can be matched.

    4.  In the second row, set a second filter condition.

        The following image is an example with two conditions that must be matched before security incidents are created.

        ![Filter conditions builder.](../image/splunk_filters.png)

        You have set the triggering conditions so that security incidents are created only when both of the filtering conditions that you entered are matched.

        This type of filtering helps you isolate security events, and it limits the number of security incidents that you create. If additional filtering criteria are set, only alerts that are required are ingested without having to change the Splunk query or the triggered alert configuration.

        Aggregation Alerts to Prevent Duplicate Incidents

10. To avoid potentially creating duplicate security incidents, define additional incident field criteria so incoming alerts are aggregated to an open security incident.

    To set this criteria, follow these steps.

    1.  Scroll to the Alert Aggregation Criteria section on the form and select the Aggregate conditions check box to enable this option.

        The Incident Field Matching Values columns are displayed. These field names are the fields on the security incident that include any custom fields that are configured on the SIR security incident.

        ![Aggregation criteria slushbucket.](../image/SplunkProfileMappingsi-add.png)

    2.  From the Available list, select the field values that you want to match on existing security incidents in your ServiceNow AI Platform and move them to the Selected list.

        All the field values that you select must be matched to append this incoming alert to an existing security incident. If you prefer to review field values on security incidents to use for this criteria, navigate to **Incidents** &gt; **Show all incidents**.

        If a new alert matches all the values that are selected in the aggregation field conditions in the mapping step, the alert is automatically added to the most recently opened security incident with the same field values. As a user with the sn\_si.analyst role working with security incidents, you can view all the added aggregate alerts on a related list on a security incident. All of the aggregated alerts on a security incident are displayed on the Splunk Event to Tasks related list. This list details associated timestamps and aggregated field values. This information helps you understand why alerts are added to existing security incidents. If this tab is not displayed, scroll to the left side of the record under Related Links and select the **Show All Related Lists** link.

        ![Splunk Event to Tasks related list highlighted.](../image/aggregate_tab_si.png)

    3.  To log a work note for a new alert that is recently added on the security incident, select the check box to enable this option.

        The work note logs that a new alert has been added along with a link to the alert details.

    You have successfully mapped values from a Splunk alert or event to fields on a SIR security incident. Also, you have configured additional conditions to limit the creation of security incidents with filtering criteria. You also appended alerts or events to existing SIR security incidents.

11. Open the script editor and continue editing.

    For more information about the script editor, see [Use the script editor to format alert values for the Splunk Enterprise Event Ingestion integration](splunk-event-ingest_script_editor.md).

12. Choose one to continue with the profile configuration.

<table id="choicetable_svs_ttl_kdb"><thead><tr><th align="left" id="d271515e670">

Option

</th><th align="left" id="d271515e673">

Description

</th></tr></thead><tbody><tr><td id="d271515e679">

** **

</td><td>

 

</td></tr><tr><td id="d271515e686">

**Continue**

</td><td>

The Mapping form is displayed. **Preview** is selected on the progress bar. The next step is to preview the fields you mapped on a SIR security incident.

</td></tr><tr><td id="d271515e703">

**Update**

</td><td>

Your data is saved and the Splunk Event Profiles list is displayed.

</td></tr><tr><td id="d271515e715">

**Previous**

</td><td>

The Alert Selection form is displayed.

</td></tr><tr><td id="d271515e725">

**Delete**

</td><td>

Delete this event profile and the Splunk Event Profiles list is displayed.

</td></tr></tbody>
</table>
## What to do next

The next step is to preview the values that you mapped on the security incident.

**Parent Topic:**[Create and name an event profile](splunk-event-ingest-create-profile.md)

