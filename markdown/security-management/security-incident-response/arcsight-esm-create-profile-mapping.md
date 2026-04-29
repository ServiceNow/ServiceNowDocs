---
title: Create mappings for ArcSight ESM event ingestion integration
description: In this step, you ingest sample correlation events and map values to the SIR security incident fields.
locale: en-US
release: australia
product: Security Incident Response
classification: security-incident-response
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 9
breadcrumb: [Map event fields, Use, Set up instance, ArcSight ESM Event Ingestion integration, Security Incident Response integrations, Security Incident Response, Enterprise security case management applications, Security Operations]
---

# Create mappings for ArcSight ESM event ingestion integration

In this step, you ingest sample correlation events and map values to the SIR security incident fields.

## Before you begin

Role required: admin, sn\_si.admin

## About this task

As a user with the sn\_si.admin role, you can review up to five sample correlation events from the Correlation Event Sample Ingestion column on the left of the form to assist with mapping and translating event field values to the security incident fields in the SIR Incident Field Mapping column on the right.

Create custom mappings by adding or removing the fields on the mapping grid on the right side of the form. Fields displayed by default are typically important fields to populate on the security incident response form. However, these fields can be removed and any additional fields can be displayed using the + and - buttons. Create custom maps by adding or removing the fields on the mapping grid on the right side of the form. Customizing the fields permits you to map ArcSight ESM fields that are not displayed on the default mapping grid on the security incident.

## Procedure

1.  If the mapping form is not displayed, click **Mapping** on the progress bar.

2.  You can either pull the most recent sample correlation events for the selected correlation rule or provide the unique correlation event IDs for the specific correlation events that you want to use for your correlation event mapping experience.

3.  From the drop down list, select one of the following:

    -   Retrieve most recent correlation events
    -   Select correlation events based on event ID
    Click **Retrieve Events** to pull the latest sample correlation events from the ArcSight ESM console for the selected correlation search rule.

    The correlation event fields and values results are displayed as individual tabs.

    The pull for sample correlation events may take a few moments. A message indicating that the transaction is working is displayed at the top of the screen.

    In the following figure, the field-name value pairs for the ingested correlation event, or the imported sample events, are displayed on the left side of this form after the ingestion pull is completed. These values are the values that you map to the security incident fields on the SIR Incident Field Mapping side of the form.

    ![ArcSight ESM: Create Profile: Retrieve Events](../image/sir-arcsight-esm-profile-map-correlate.png)

4.  To map a field value from the left side of the form to a field on the security incident on the right side of the form, click-hold a blue field name on the left side of the form.

5.  Drag the field name, for example, `agent.hostname`, and drop it on a field in the Input Expression column next to a field name in the Security Incident column.

    To help you ensure that no event fields are overlooked or duplicated in the mapping process, fields are color-coded. Light blue fields on the left indicate that a correlation event field is not yet selected and mapped on the security incident. You may prefer to associate an incoming correlation field with more than one field on a security incident.

    A gray field indicates that a field has been selected and mapped to a field on the security incident. This color-coding helps you track which event fields have already been utilized for future security incident field mappings.

    ![ArcSight ESM: Create Profile: Drag](../image/sir-arcsight-esm-profile-map-drag.png)

6.  To add fields to the default fields displayed on the security incident on the right side of the form, follow these steps.

    1.  On the right of the form in the SIR Incident Field Mapping section, at the bottom of the grid, click the plus icon.

        A new field is displayed.

    2.  In the Security Incident column, expand the choice list that is displayed, and select a field.

        In the expanded choice list for the new field, some fields are shaded. In the following figure, `Affected User` has a gray background, because it has been mapped in the security incident. Similar to the color-coding for the correlation events fields on the left side of the form, this color-coding for the security incident fields on the right helps you track the already mapped SIR incident fields.

        ![ArcSight ESM: Create Profile:Gray fields](../image/sir-arcsight-esm-profile-map-grey.png)

        **Note:** So that multiple observables can be displayed on the same security incident, the Observable field can be mapped multiple times with different values. Similarly, the Configuration Item and Work notes fields support multiple values. If you try to map two values to a field that cannot support multiple values, when you preview the incident, an error message is displayed that there is no value for the field. Similarly, if a field on a security incident has a choice list from which you can choose multiple options, and you try to map an option to that field that is not displayed on the choice list, the field is not populated on the security incident.

    3.  Alternatively, type a value in the Search field for the new row.

    4.  From the left side of the form, left-click to select the **Event ID** that you want in the **Input Expression** field.

        With the drag-and-drop feature, map it next to your new field.

7.  Open the script editor and continue editing.

    For more information about the script editor, see [Use the script editor to format correlation event values](arcsight-esm-create-profile-script.md).**Incident generation filtering conditions**

8.  After you have completed the preceding field mapping steps, you can use the same field values in the Incident Generation Conditions builder to define additional criteria that an incoming correlation event must satisfy to create a SIR security incident.

    To set incident generation conditions, follow these steps.

    1.  Scroll to the Incident Generation Conditions section on the form and select the **Filter based on conditions** check box to enable the option.

        The Filter conditions builder is displayed. Use these filters to create security incidents that match the specific conditions described by the fields.

        The options in the choice lists for the first field in the Filter conditions builder match the fields that are displayed on the Correlation Event Sample Ingestion section for the events you ingested. These fields are dynamic and change depending on the correlation events that you ingest. Criteria that you enter are case-sensitive, and they must match exactly the values of the ArcSight ESM correlation event.

        Using the choice lists and fields of the condition builder, set filters for the first row.

    2.  To add more conditions, to the right of the fields, click **AND** or **OR**.

        If **AND** is selected, all conditions must be matched. If **OR** is selected, either condition can be matched.

    3.  In the second row, set a second filter condition.

        The following image is an example with two conditions that must be matched before security incidents are created.

        ![ArcSight ESM: Create Profile: Filter with matching conditions](../image/sir-arcsight-esm-profile-map-filter.png)

        You have set the incident generation conditions so that security incidents are created only when both of the filtering conditions that you entered are matched.

        This type of incident generation condition filtering helps you narrow down the security events, and limit the number of unnecessary security incidents that you create without modifying the underlying correlation search or filter out events in ArcSight ESM. If additional filtering criteria are set, only correlation events that match all criteria are mapped to incidents.

        **Note:** If any of the event field names have special characters such as quotes \(“\),hyphens \(‘\), underscores \(-\), or ampersands \(@\), these characters may need to be replaced for mapping translation purposes and possibly create a duplicate event name. The mapping can be done appropriately but a numerical suffix is appended to differentiate fields with duplicate event names. For example, if the first event field is `events.event` and the second event field is `events.event`, these fields cannot be uniquely identified as the remaining standard text characters are the same. In this case, a suffix is added to the second event field and the field is renamed to `events@event(1)`.

    **Event Aggregation Criteria to Handle Similar Correlation Events and Prevent Duplicate Incidents**

9.  To avoid creating duplicate security incidents, define additional event aggregation criteria so that incoming correlation events are aggregated to an open security incident.

    To set the criteria, follow these steps below:

    1.  Scroll to the **Event Aggregation Criteria** section on the form and select the Aggregation conditions check box to enable this option.

        The Incident Field Matching Values columns are displayed. These field names are the fields on the security incident that include any custom fields that are configured on the SIR security incident.

    2.  From the Available list, select the field values that you want to match on existing security incidents in your ServiceNow AI Platform and move them to the Selected list.

        All the field values that you select must be matched to append this incoming correlation event to an existing security incident. This includes fields, such as Observables and Configuration Items, that may have multiple correlation event field values mapped to them. All values must match. If only a subset of the values are matched, the event aggregation conditions will not be met and a new security incident will be created. See screen shot below for multi-value field mapping.

        ![ArcSight ESM: Create Profile: Aggregate](../image/sir-arcsight-esm-profile-map-aggregate.png)

        If a new correlation event matches all the values that are selected in the aggregation field conditions in the mapping step, the new correlation event is automatically added to the most recently opened security incident with the same field values. As a SOC analyst working with security incidents, you can view all the added aggregated correlation events on a related list on a security incident. All of the aggregated correlation events on a security incident are displayed on the **Aggregated ArcSight Events** related list. This list details associated time stamps and aggregated field values. This information helps you understand why these correlation events are being aggregated to existing security incidents. If this tab is not displayed, scroll to the left side of the record under **Related Links** and click the **Show All Related Lists** link.

        **Note:** If you do not see this related list, follow these steps:

        -   Right click the Security Incident form header and click **Configure** &gt; **Related Lists**.
        -   Select **Aggregated ArcSight Events** in the Available list, move it to the Selected list and click **Save**.
        -   Click **Show Related Lists**. You will now see the **Aggregated ArcSight Events** tab in the Related List section.
        ![ArcSight ESM: Aggregated Events](../image/sir-arcsight-esm-profile-agg-events.png)

    3.  To log a work note for each time an event is aggregated on the security incident, select the check box to enable this option.

        The work note logs that a new correlated event has been added along with a link to the correlated event details.

    You have successfully mapped values from a correlation event to fields on a SIR security incident. Also, you have configured additional conditions to limit the creation of security incidents with incident generation filtering criteria. You also aggregated correlation events to existing SIR security incidents when event field values match the configured aggregation criteria.

10. Choose one to continue with the profile configuration.

<table id="choicetable_ov3_gbq_nkb"><thead><tr><th align="left" id="d177758e483">

Option

</th><th align="left" id="d177758e486">

Description

</th></tr></thead><tbody><tr><td id="d177758e492">

** **

</td><td>

 

</td></tr><tr><td id="d177758e499">

**Continue**

</td><td>

The Mapping form is displayed. **Preview** is selected on the progress bar. The next step is to preview the fields you mapped on a SIR security incident.

</td></tr><tr><td id="d177758e516">

**Update**

</td><td>

Your data is saved and the ArcSight ESM Event Profiles list is displayed.

</td></tr><tr><td id="d177758e528">

**Previous**

</td><td>

The Correlation Event Selection form is displayed.

</td></tr><tr><td id="d177758e538">

**Delete**

</td><td>

Delete this event profile and the Event Profiles list is displayed.

</td></tr></tbody>
</table>
