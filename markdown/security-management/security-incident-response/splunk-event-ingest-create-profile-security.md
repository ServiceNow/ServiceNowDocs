---
title: Create and name an event profile for the Splunk Enterprise Security event ingestion integration
description: You create an event profile in your ServiceNow AI Platform instance and determine which Splunk notable events create security incidents.Depending on the profile defined, Splunk ES notable events are automatically ingested into the Security Operations environment of your ServiceNow AI Platform instance.You can set up a profile so that notable events are automatically ingested.After you have created a profile for a scheduled notable event type ingestion, select a Splunk Enterprise Security correlation rule name for this profile for which you want to map corresponding notable events to a ServiceNow AI Platform Security Incident Response security incident.After you identify the specific correlation rule and notable event type for the profile, the next step is to map individual notable event fields to the fields on a ServiceNow AI Platform Security Incident Response \(SIR\) security incident.During the notable event field-mapping step, you map individual event fields from notable events to fields on a ServiceNow AI Platform Security Incident Response \(SIR\) security incident.After you complete the mapping step, preview the values that you mapped in a ServiceNow AI Platform Security Incident Response \(SIR\) security incident. This preview step permits you to verify that you have mapped all the notable fields that you want displayed on the security incident.For automated notable event ingestion profiles, this step is required in the event profile configuration. During this step, you can verify the default settings for notable event retrieval or modify the scheduling as needed. This step also permits you to retrieve historical notable events using a date range.Security incidents can be created and updated after they are created with a bi-directional interface with the Splunk Enterprise Security integration.Depending on the profile defined, Splunk ES notable events are forwarded manually as discrete notable events into the Security Operations environment of your ServiceNow AI Platform instance.You can set up a profile for manual forwarded events.During the notable event field mapping step, you map individual event fields from notable events to fields on a ServiceNow AI Platform Security Incident Response \(SIR\) security incident.Install and set up the ServiceNow Security Operations Event Ingestion Addon for Splunk Enterprise Security application in your Splunk enterprise console or Splunk Cloud instance if you want to export events manually and on-demand from your Splunk Enterprise Security console for this integration.
locale: en-US
release: xanadu
product: Security Incident Response
classification: security-incident-response
topic_type: task
last_updated: "2025-01-30"
reading_time_minutes: 52
breadcrumb: [Splunk Enterprise Security event ingestion integration, Security Incident Response integrations, Security Incident Response, Enterprise security case management applications, Security Operations]
---

# Create and name an event profile for the Splunk Enterprise Security event ingestion integration

You create an event profile in your ServiceNow AI Platform instance and determine which Splunk notable events create security incidents.

## Before you begin

Role required: sn\_si.ingestion\_profile\_admin

**Note:** Users with the sn\_si.admin role can perform all operations available to a profile admin, as the sn\_si.admin role inherits the required permissions by default.

## About this task

Before ServiceNow AI Platform Security Incident Response \(SIR\) security incidents are created from ingested notable events, the field values from alerts are displayed on a layout of a ServiceNow AI Platform security incident so that you can preview how the actual security incident will be created.

From an integration perspective using the available APIs, Splunk ES notable events are forwarded individually and manually as discrete notable events, or they’re automatically ingested into the Security Operations environment of your ServiceNow AI Platform instance depending on the profile type defined.

The integration workflows ingest different types of notable events such as unauthorized access attempts and malware, for example. These notable events are ingested based on the profiles that you configure in the Security Operations environment of your instance.

All notables are initially ingested for a configured correlation search type in a profile. Ingested notables can then be further filtered to specify which notables create security incidents. For example, you may prefer filters that create security incidents only for notable events that are identified as high-risk. Before a profile is activated, and it creates security incidents from ingested notable events, individual field values on the notable events are mapped to corresponding fields on a layout the security incident for a preview.

## Procedure

1.  Names for the event profiles in your ServiceNow AI Platform instance must be unique and can only be mapped to one active event profile at any given time.

2.  The ServiceNow AI Platform ingests specific notables using the workflows of the integration.

    All notable events that meet the selection criteria in your Splunk ES console are initially ingested into your ServiceNow AI Platform instance.

3.  A profile in your ServiceNow AI Platform is an encapsulation of a notable event in your Splunk ES console.

    There’s a one-to-one relationship between notable events that are ingested with a profile and connections to your Splunk ES console: one notable event type for one connection.

4.  To create profiles for scheduled notable events, see [Set up a profile for scheduled notable event ingestion](splunk-event-ingest-create-profile-security.md#).

5.  To create profiles for manual event forwarding, see [Set up a profile for manual event forwarding](splunk-event-ingest-create-profile-security.md#).


## Set up a profile for scheduled notable event ingestion

Depending on the profile defined, Splunk ES notable events are automatically ingested into the Security Operations environment of your ServiceNow AI Platform instance.

The following table shows the list of tasks you need to follow to set up a profile for scheduled ingestion of notable events:

|Task|Section|
|----|-------|
|Create an event profile|See [Create profiles for scheduled notable event ingestion](splunk-event-ingest-create-profile-security.md#)|
|Select notable events based on correlation search name|See [Select notable events based on correlation rule name for the profile for Splunk ES Event Ingestion integration](splunk-event-ingest-create-profile-security.md#)|
|Map notable event fields|See [Mapping notable event fields for the Splunk Enterprise Security integration](splunk-event-ingest-create-profile-security.md#)|
|Create custom mappings|See [Create mappings for Splunk ES notable event incident review and contributing event details \(scheduled ingestion\)](splunk-event-ingest-create-profile-security.md#)|
|Preview the security incident|See [Preview the security incident for the Splunk Enterprise Security Event Ingestion integration](splunk-event-ingest-create-profile-security.md#)|
|Schedule and retrieve new and updated notable events|See [Schedule and retrieve new and updated notable events for the Splunk Enterprise Security Event Ingestion integration](splunk-event-ingest-create-profile-security.md#)|
|Automate notable event updates and closure based on SIR incident status|See [Automate notable event updates and closure based on SIR incident status](splunk-event-ingest-create-profile-security.md#)|

### Create profiles for scheduled notable event ingestion

You can set up a profile so that notable events are automatically ingested.

#### Before you begin

Role required: sn\_si.admin

#### Procedure

1.  To create an event profile for a notable event or correlation rule type in your ServiceNow AI Platform instance, navigate to **Splunk Integration** &gt; **Splunk Event Profile**.

2.  If the Splunk Event Profile form is not displayed, click **Name** in the Progress bar.

3.  Click **New**.

4.  Fill in the fields.

    An example of a completed form follows the table.

<table id="simpletable_kt2_lqb_jfb"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Name

</td><td>

Unique name for the profile. If names are not unique, an error will be displayed and duplicate profile names are not saved. Profile names in your ServiceNow AI Platform instance must be unique.

</td></tr><tr><td>

Active

</td><td>

Check box is cleared and disabled by default. You should complete all sections in the profile before making it active.

</td></tr><tr><td>

Type

</td><td>

Select the profile type from the choice list. -   Scheduled Event Ingestion: This type of profile supports notable events that are ingested on a configured schedule. Fill in the fields.
-   Manual Event Forwarding: This type of profile supports notable events that are forwarded manually from your Splunk Enterprise Security Incident Review console on demand. See the following steps to fill out the form for these types of profiles.


</td></tr><tr><td>

Source

</td><td>

Splunk server or search end that you configured to ingest notable events. If you have multiple Splunk servers configured, select the appropriate server for the notable event types that will be ingested for the profile. You are required to enter a value.

</td></tr><tr><td>

Order

</td><td>

Default is 100. If you have created multiple profiles, this value provides a run time execution priority when two or more profiles share the same triggering conditions. The workflow in the profile with the lowest number has the highest priority.

</td></tr><tr><td>

\(Optional\) Description

</td><td>

Additional text to help you distinguish this profile from other profiles.

</td></tr></tbody>
</table>    The following figure is an example of a completed form for a scheduled notable event type.

    ![Splunk ES Event Profile](../image/new-images/notable-event-profile.png)

5.  For a profile with a scheduled notable event, choose one option to continue with the profile configuration.

    |Option|Description|
    |------|-----------|
    |**Continue**|Save the profile and progress to the Event Selection step.|
    |**Update**|Save updates to this profile and return to the Splunk Event Profiles list.|
    |**Save**|Save this profile and remain on the page.|
    |**Delete**|Delete this profile record and return to the Splunk Event Profiles list.|


#### What to do next

The next step is to select notable events for automatic ingestion.

### Select notable events based on correlation rule name for the profile for Splunk ES Event Ingestion integration

After you have created a profile for a scheduled notable event type ingestion, select a Splunk Enterprise Security correlation rule name for this profile for which you want to map corresponding notable events to a ServiceNow AI Platform Security Incident Response security incident.

#### Before you begin

Role required: sn\_si.admin

#### About this task

View the available correlation rules in your ServiceNow AI Platform instance so you know the notable event types for which you want to ingest and create security incidents. Select a correlation rule. You can select one or more notable event from the list in this form.

#### Procedure

1.  If the Notable Event Selection page is not displayed, select it on the progress bar to display it.

2.  From the Correlation Rule List, choose one of the following options to select a single correlation rule or multiple correlation rules and move them and move it to from the Available column to the Selected column.

    The list of correlation rules on this form matches the list of correlation rules in your Splunk ES Incident Review console. Up to 500 correlation rules are displayed on this form. If there are more than 500 correlation rules listed in your Splunk ES, only the first 500 notable events are displayed on this form in your ServiceNow AI Platform instance.

    |Option|Description|
    |------|-----------|
    |In the Correlation Rule List search field, enter text.|The column below the search field is filtered with available options based on the text that you enter. Select an correlation rule, and with the arrow keys, move the selected alarm from **Available** to **Selected**.|
    |In the Correlation Rule List, double-click a Correlation Rule.|The **Selected** column is populated with your selection.|
    |In the Correlation Rule List, single-click a Correlation Rule.|The correlation rule is selected. With the arrow keys, move the selected correlation rule from **Available** to **Selected**.|

    ![Splunk ES Event Profile: Select Notable Event](../image/new-images/splunk_es_profile_select.png)

3.  Choose one option to continue.

<table id="choicetable_svs_ttl_kdb"><thead><tr><th align="left" id="d226967e857">

Option

</th><th align="left" id="d226967e860">

Description

</th></tr></thead><tbody><tr><td id="d226967e866">

**Continue, or alternatively, click Mapping in the progress bar**

</td><td>

The Mapping form is displayed. **Mapping** is selected on the progress bar. The next step is to map notable event fields to a SIR security incident.

</td></tr><tr><td id="d226967e883">

**Update**

</td><td>

Your data is saved and the Splunk Notable Event Profiles list is displayed.

</td></tr><tr><td id="d226967e892">

**Previous**

</td><td>

The **Name** step is displayed.

</td></tr><tr><td id="d226967e904">

**Delete**

</td><td>

Delete this event profile and the Splunk Notable Event Profiles list is displayed.

</td></tr></tbody>
</table>
#### What to do next

You have successfully selected a correlation rule for a scheduled Splunk Enterprise Security profile. The next step is map notable event values to fields on a security incident.

### Mapping notable event fields for the Splunk Enterprise Security integration

After you identify the specific correlation rule and notable event type for the profile, the next step is to map individual notable event fields to the fields on a ServiceNow AI Platform Security Incident Response \(SIR\) security incident.

#### Overview

For the mapping step, you can ingest sample notable events for the selected correlation rule or export notable event data for manually forwarded notable events. The event mapping process is identical regardless of the profile type you are creating.

The following figures are examples of the default mapping configurations that are provided for each type of event profile. You can customize the fields that populate the security incident. During this mapping phase, you can ensure all relevant notable event field data is mapped to the appropriate place on the SIR incident form and then visualize the SIR incident in the preview section.

If Multiple correlations are used, then notable events can be fetched by selecting required Event. Use **Alert Name** to choose your alert if you have configured multiple alerts for ingestion.

After you click to fetch data, the Splunk notable event field names and corresponding values are populated on the left side of the form. These are the Splunk notable event fields that are available to map to the SIR security incident fields. Some fields can be mapped multiple times to the SIR security incident fields.

![Default mapping for scheduled notable events](../image/new-images/splunk_es_default_notable.png)

You may prefer to review a few sample notable events on your Splunk console to ingest for the field mapping configuration step. This step is labeled Mapping on the progress bar. If this page is not displayed, click **Mapping** on the progress bar. You can ingest up to five sample notable events from Splunk Enterprise Security to assist with the notable event field mapping process. There are options to either ingest the five most recent notable events for the correlation rule selected or ingest up to five specific notable events based on the notable event IDs.

Below is a summary of the steps required to map notable events:

-   Scheduled Notable Event Sample Data Ingestion: For sample data that is used for automatically ingested notable event profiles, available notable event fields and their corresponding values are displayed in a default mapping layout on the left side of the mapping form once the sample data is retrieved. Tabs are displayed for you to view the values for a specific notable event ID that you pulled. Verify that all the critical fields from the notable event sample ingestion section on the left of the form are mapped to ServiceNow security incident fields on the right of the form.
-   Field Mapping: Edit the mapping configuration by dragging notable event fields from the left side and dropping them on the ServiceNow SIR incident mapping section on the right. The mapping on the right associates the incoming notable event field with an outgoing security incident field.
-   Mapping Experience: Customize the mapping grid by adding or removing fields using the + icon at the bottom of the SIR incident field mapping section. Track overlooked or duplicated fields with the color coding that is provided \(mapped fields are greyed out, blue fields are unmapped\).
-   Incident Generation Conditions: Once the mapping section is complete, you can set filter conditions so that you can specify which notable events should create security incidents versus which notable events should be filtered out, for example, low priority notable events. This is done in the Incident Generation Conditions section located below the Notable Event Mapping section.
-   Event Aggregation Criteria: Define additional Event Aggregation criteria that aggregates an incoming notable event to an existing SIR security incident instead pf creating similar, potentially duplicate incidents. Using field matching value criteria for each profile, this additional aggregation capability can reduce the number of active, overlapping security incidents by placing all related security notable event data on a single security incident.
-   Format Field Translation: In certain cases, event field values in the Splunk Enterprise notable events may not translate directly to the fields on the SIR security incident. For these values, you can use a script editor to format field values on the security incident during the mapping step. Use the script editor if you want to format values that are similar, but not identical. For example, with the script editor, a category value of Malware Alert and Virus Infection may have different field values for the source category but both values can be translated to a common Malicious Code Activity in the Category field on the SIR security incident using the Format Field Translation functionality.

The next step is to ingest notable events and map values to the SIR security incident fields.

### Create mappings for Splunk ES notable event incident review and contributing event details \(scheduled ingestion\)

During the notable event field-mapping step, you map individual event fields from notable events to fields on a ServiceNow AI Platform Security Incident Response \(SIR\) security incident.

#### Before you begin

Role required: sn\_si.ingestion\_profile\_admin

**Note:** Users with the sn\_si.admin role can perform all operations available to a profile admin, as the sn\_si.admin role inherits the required permissions by default.

#### About this task

The mapping grid can be customized for the notable event type selected in the correlation rule selection. Color-coding of the event fields helps you keep track of the event values that you have already mapped as they become grayed out while all remaining unmapped fields appear in blue. This helps you better visualize which field values have been added to the security incident and if any remaining important event information remains unmapped.

Map up to five notable events from the Notable Event Sample Ingestion column on the left of the form to the security incident fields in the SIR Incident Field Mapping column on the right.

Create custom mappings by adding or removing the fields on the mapping grid on the right side of the form. Default fields that are typically important field to populate on the security incident response form are displayed. However, these fields can be removed and any additional fields can be displayed using the + and - buttons. Create custom maps by adding or removing the fields on the mapping grid on the right side of the form. Customizing the fields permits you to map Splunk fields that are not displayed on the default-mapping grid on the SIR security incident.

#### Procedure

1.  If the mapping form is not displayed, click **Mapping** on the progress bar.

2.  For a profile with a scheduled ingestion, below Notable Event Sample Ingestion, click **Fetch Sample Data** to pull the latest sample notable events from the Splunk Enterprise console for the correlation rule selected.

    **Note:** You can either pull the most recent sample notable events or provide the unique notable event IDs for the specific notable events that you want to use for your notable event mapping experience.

    The notable event fields and values results are displayed as individual tabs. You can ingest up to five notable events.

    The pull for sample notable events may take a few moments. A message indicating that the transaction is working is displayed at the top of the screen.

    In the following figure, the field-name value pairs for the ingested notable event, or the imported sample events, are displayed on the left side of this form after the ingestion pull is completed. These values are the values that you map to the security incident fields on the SIR Incident Field Mapping side of the form.

    ![Fetch sample data and ingested notable events](../image/new-images/splunk_map_initial_security.png)

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

        In the expanded list for the new field, some fields are shaded. In the following figure, `rule_name` has a gray background, because it has been mapped in the security incident. Similar to the color-coding for the notable events fields on the left side of the form, this color-coding for the security incident fields on the right helps you track the already mapped SIR incident fields.

        ![Category field mapping](../image/splunk_es_map_4_security.png)

        **Note:** So that multiple observables can be displayed on the same security incident, the Observable field can be mapped multiple times with different values. Similarly, the Configuration Item and Work notes fields support multiple values. If you try to map two values to a field that cannot support multiple values, when you preview the incident, an error message is displayed that there is no value for the field. Similarly, if a field on a security incident has a list from which you can choose multiple options, and you try to map an option to that field that is not displayed on the list, the field is not populated on the security incident.

    3.  Alternatively, type a value in the Search field for the new row.

    4.  From the left side of the form, left-click to select the **Event ID** that you want in the Input Expression field.

6.  Continue mapping by adding or removing field values to the mapping.

    The following figure is an example of an edited mapping. In the bottom field on the right, the Work notes field is added, and it has more than one value. Note that for long text string field, you can expand the mapping field to see the full string and re-size as needed by pulling the lower right corner of the field as indicated in screen shot below with the added Work notes field:

    ![Work notes with multiple values highlighted](../image/splunk_es_mapexample_security.png)

    **Warning:** Please note that in the **SIR Incident Field Mapping** section, the URL and port number mentioned in the **Input Expression** field is just an example and not the URL or port number provided out-of-the-box.

    In the preview, these values are displayed in the Work notes on the security incident. Because the value is for a field that you added to the mapping section, and there are multiple values mapped to the Work notes field, the values are displayed as entered. In this example, the spaces and punctuation marks that you entered in the field are displayed on the Related Items section as a work note on the preview of the security incident.

    The following image is an example of how the values in the preceding image are displayed on the security incident.

    ![Work Note field value displayed on security incident.](../image/splunksi_notes.png)

7.  To receive updates for the mapped fields in SIR, select the **Enable Updates** check box against the Input Expression.![Enable updates check box selected](../image/splunk_es_enable_updates.png)

8.  After you have completed the preceding field-mapping steps, you can use the same field values in the Incident Generation Conditions builder to define additional criteria that an incoming notable event must satisfy to create a SIR security incident.

    To set incident generation conditions, follow these steps.

    1.  Scroll to the Incident Generation Conditions section on the form and select the **Filter based on conditions** check box to enable the option.

        The Filter conditions builder is displayed. Use these filters to create security incidents that match the specific conditions described by the fields.

        The options in the lists for the first field in the Filter conditions builder match the fields that are displayed on the Notable Event Sample Ingestion section for the events you ingested. These fields are dynamic and change depending on the Splunk notable events that you ingest, or the event that you select for the manually forwarded notable event samples. Criteria that you enter are case-sensitive, and they must match exactly the values of the Splunk Enterprise Security notable event. If you are not sure about the values to enter in the filter fields, you may prefer to return to your Splunk Enterprise Security console and review your notable events for the keywords.

        ![Filter conditions builder](../image/splunk_es_filters_security.png)

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

        All the field values that you select in the multi-selection input field are matched for aggregation criteria using the AND condition. Click **Add New Criteria** to select multiple field matching conditions where aggregation occurs if any one of the multi-selected field conditions that are defined are met using the OR condition.

        ![Aggregation criteria](../image/splunk_es_event_aggregation.png)

        If a new notable event matches all the values that are selected in the aggregation field conditions in the mapping step, the new notable event is automatically added to the most recently opened security incident with the same field values. As a user with the sn\_si.analyst role working with security incidents, you can view all the added aggregate notable events on a related list on a security incident. All of the aggregated notable events on a security incident are displayed on the Splunk Event to Tasks related list. This list details associated timestamps and aggregated field values. This information helps you understand why these notable events are being aggregated to existing security incidents. If this tab is not displayed, scroll to the left side of the record under Related Links and click the **Show All Related Lists** link.

        ![Splunk Event to Tasks related list highlighted](../image/splunk_es_event_aggregation2.png)

    4.  To log a work note for a new notable event that is recently added on the security incident, select the check box to enable this option.

        The work note logs that a new notable has been added along with a link to the alert details and any other details that may have been added to the work note field in your mapping section.

    You have successfully mapped values from a Splunk notable event to fields on a SIR security incident. Also, you have configured additional conditions to limit the creation of security incidents with incident generation filtering criteria. You also appended notable events to existing SIR security incidents when event field values match the configured aggregation criteria.

10. Choose one to continue with the profile configuration.

<table id="choicetable_svs_ttl_kdb"><thead><tr><th align="left" id="d226967e1588">

Option

</th><th align="left" id="d226967e1591">

Description

</th></tr></thead><tbody><tr><td id="d226967e1597">

** **

</td><td>

 

</td></tr><tr><td id="d226967e1604">

**Continue**

</td><td>

The Mapping form is displayed. **Preview** is selected on the progress bar. The next step is to preview the fields you mapped on a SIR security incident.

</td></tr><tr><td id="d226967e1621">

**Update**

</td><td>

Your data is saved and the Splunk Event Profiles list is displayed.

</td></tr><tr><td id="d226967e1630">

**Previous**

</td><td>

The Notable Event Selection form is displayed.

</td></tr><tr><td id="d226967e1640">

**Delete**

</td><td>

Delete this event profile and the Splunk Event Profiles list is displayed.

</td></tr></tbody>
</table>
#### What to do next

The next step is to preview the values that you mapped on the security incident.

### Preview the security incident for the Splunk Enterprise Security Event Ingestion integration

After you complete the mapping step, preview the values that you mapped in a ServiceNow AI Platform® Security Incident Response \(SIR\) security incident. This preview step permits you to verify that you have mapped all the notable fields that you want displayed on the security incident.

#### Before you begin

Role required: sn\_si.admin

#### About this task

Preview a security incident and edit the mapping again as required to fix fields with errors or to populate any missing data. If the preview is not successfully completed, you cannot proceed to the scheduling step. Previews of SIR security incidents are not saved as actual incidents in the SIR product.

#### Procedure

1.  If the security incident preview is not displayed, click **Preview** in the progress bar.

2.  From the Event Name choice list, select an item if multiple Events were used.

3.  Select event IDs from the Sample Notable Event IDs choice list.

4.  From the Sample Notable Event IDs choice list, select an item.

    ![Select event choice list expanded.](../image/new-images/splunk-es-preview.png)

    The security incident is displayed. Do not change any information in the fields. This view is a read-only view, and a record of this security incident is not saved.

5.  Review the field mapping of the notable event values on the security incident.

    ![Error message on a security incident in the preview.](../image/new-images/preview-select-event.png)

    The preceding image is an example of a preview with a mapping error. In this example, a field value from the notable event does not have an acceptable value for the reference field on the SIR incident form. An error message is displayed that indicates an input value was not found for the `Configuration item` field in the ServiceNow® customer management database \(CMDB\). As a result, this mapped field value will not appear on the SIR security incident form without further modification.

6.  To resolve this error, click **Mapping** in the progress bar.

7.  Edit the mapping to fix incorrect values or populate any missing data.

8.  Preview the mapping again and continue to fix any errors that are described in error messages.

    The following figure is an example of the Incident Details tab on the bottom half of a SIR security incident after all error messages are resolved. For this example, the Description and Work notes fields were mapped, and these fields are populated with the values from the value pairs pulled from the Splunk Enterprise Security notable event samples. The first Work notes field has no value. This field was left blank on the mapping grid during the mapping step. The additional Work Note fields that have values were added to the mapping section.

    ![Work note and Description fields on the security incident preview](../image/previewsplunk_es_worknote_security.png)

9.  After you have fixed any errors and verified that the fields are the way you want them, choose one option to continue.

<table id="choicetable_svs_ttl_kdb"><thead><tr><th align="left" id="d226967e1841">

Option

</th><th align="left" id="d226967e1844">

Description

</th></tr></thead><tbody><tr><td id="d226967e1850">

**Continue**

</td><td>

The Scheduling form is displayed for profiles with scheduled notable events. **Scheduling** is selected on the progress bar.

</td></tr><tr><td id="d226967e1864">

**Finish**

</td><td>

For profiles with configured for manual event forwarding, click **Finish**. There is no scheduling step for profiles with event data that are exported on-demand directly from the Splunk Enterprise Security console.

</td></tr><tr><td id="d226967e1879">

**Update**

</td><td>

Your data is saved, and you are returned to the Splunk Event Profiles list.

</td></tr><tr><td id="d226967e1891">

**Previous**

</td><td>

The Mapping step on the progress bar is displayed.

</td></tr><tr><td id="d226967e1901">

**Delete**

</td><td>

Delete this event profile and the Splunk Event Profiles list is displayed.

</td></tr></tbody>
</table>
#### What to do next

If no error messages are displayed, and you are satisfied with the field mapping on the security incident, the next step is to [Schedule and retrieve alerts for the Splunk Enterprise Event Ingestion integration](splunk-event-ingest-schedule.md).

### Schedule and retrieve new and updated notable events for the Splunk Enterprise Security Event Ingestion integration

For automated notable event ingestion profiles, this step is required in the event profile configuration. During this step, you can verify the default settings for notable event retrieval or modify the scheduling as needed. This step also permits you to retrieve historical notable events using a date range.

#### Before you begin

Role required: sn\_si.admin

#### About this task

For profiles for automated notable event ingestion, you choose whether you want to ingest any historical notable events during the Scheduling step. You also choose how often you will poll for future new notable events and updated notable events that match the alert profile configuration.

For automated notable event ingestion profiles, before the profile is activated, you verify and modify the scheduling and alert retrieval. This is a required step for all event profile configuration process for scheduled alert profiles.

You configure these polling intervals on a per-profile basis. The performance of the Splunk event ingestion integration may be impacted by the different polling intervals. When scheduling, you may prefer to balance reducing polling overhead on the Splunk Enterprise Security server against a desire to be notified as soon as possible when a notable event is created or updated. A five-minute default value is set for any profile, but you may prefer to modify this setting to as low as one minute if required.

Pulling new and updated notable events

When the polling schedule is set, the scheduled job pulls both new and updated notable events that were pulled previously but did not meet the incident filtering criteria. This provides you with the flexibility to create incidents based on criteria that may not be present when a notable event is first created but becomes available after an update occurs, for example, during the investigation phase. Once an incident is created for a specific notable event, its subsequent updates are ignored since it is expected that the notable is now being treated as an active ServiceNow® security incident. However, all other notables that have been previously ingested but failed to meet the incident generation criteria, will continue to be pulled and checked against the incident generation criteria until they become part of an active incident.

#### Procedure

1.  If the Scheduling page on the progress bar is not displayed, select **Scheduling**.

2.  Choose one to schedule how and when notable events are pulled from the Splunk Enterprise Security console.

<table id="choicetable_phd_qqc_jfb"><thead><tr><th align="left" id="d226967e2023">

Option

</th><th align="left" id="d226967e2026">

Description

</th></tr></thead><tbody><tr><td id="d226967e2032">

**-   On-going Event Ingestion field selected
-   One-Time Retrieval field cleared
**

</td><td>

On-going EventBased on the default setting, the ServiceNow AI Platform instance pulls from the Splunk Enterprise Security server for new and updated notable events every five minutes. Security incidents are created if notable events are found and incident generation filtering criteria are matched. To balance ingestion polling overhead desire to get the most current data, five minutes is the default setting. However, this value can be modified to as low as one minute if needed.

</td></tr><tr><td id="d226967e2059">

**-   On-going Notable Event field cleared
-   One-Time Retrieval field selected
**

</td><td>

One-Time RetrievalUse this configuration if you want a one-time pull to ingest historical notable events.

 When this setting configured, a profile is used once to retrieve notable events from historical events that are based on a date range. To the right of the Since date field, click the calendar icon. In the calendar that is displayed, select the date that you want to start pulling alerts. Starting with the Since date value, notable events are retrieved up through the current date. Note that you can pull as far back as seven days from the current date. This functionality is not intended to retrieve significant amounts of historical events from Splunk Enterprise Security for archival reasons but rather a minimal amount of in-flight events that are being actively worked at the time of profile activation.

After the notable events are pulled, this setting will not retrieve more notable events for this profile going forward from the current date. This setting populates the security incident with all the notable events that are found for the range you enter.

</td></tr></tbody>
</table>    ![Scheduling page with calendar displayed.](../image/splunk_es_scheduling_security.png)

    As an example for scheduling an initial notable event ingestion time, if you have a daily Splunk security check that runs once a day at 4 AM local time, you can set up the corresponding notable event profile in your ServiceNow AI Platform instance to run at 4:05 AM local time to capture the security failure event right away and create a security incident. Enter `04 05 00` in the Initial event ingestion field. In the Increment \(Minutes\) field, enter `1440` \(24 hours\) to schedule the next event ingestion for 24 hours from the initial event ingestion. Both the initial event ingestion time and next event ingestion time are displayed in the fields.

3.  To configure the settings for this example, follow these steps.

    1.  With the Scheduling page displayed, select the **Ongoing event ingestion** check box to enable this option.

    2.  In the Increment \(minutes\) field, enter `1440` \(24 hours\).

    3.  Click the **Select Initial event ingestion** check box to enable editing for the Initial event ingestion and Next event ingestion fields.

    4.  In the Initial event ingestion field, enter `04 05 00`.

        In the The Next event ingestion \(estimated\) field, the time of the next event ingestion is displayed.

4.  Click one of the following to continue with the profile configuration.

    |Option|Description|
    |------|-----------|
    |**Continue**|The Additional Options form is displayed. **Additional Options** is selected on the progress bar. The next step is to update the notable events when the SIR incident is created and/or closed.|
    |**Update**|Your data is saved and the Splunk Event Security Profiles list is displayed.|
    |**Previous**|The Scheduling form is displayed.|
    |**Delete**|Delete this event profile and the Splunk Enterprise Security Event Profiles list is displayed.|


### Automate notable event updates and closure based on SIR incident status

Security incidents can be created and updated after they are created with a bi-directional interface with the Splunk Enterprise Security integration.

#### Before you begin

The Splunk Enterprise Security integration has a bi-directional interface that allows notable events to create security incidents as well as update the notable events after the security incident is created and/or closed.

Relevant incident details include SIR incident number, assignment group, SIR incident URL. This section is the final portion of the profile configuration set-up that provides optional capabilities to update the Splunk Enterprise Security notable events.

Role required: sn\_si.ingestion\_profile\_admin

**Note:** Users with the sn\_si.admin role can perform all operations available to a profile admin, as the sn\_si.admin role inherits the required permissions by default.

#### Procedure

1.  If the Additional Options page on the progress bar is not displayed, select **Additional Options**.

2.  Follow the instructions below to complete the configuration for updating notable events based on security incident updates.

<table id="choicetable_bsh_yxn_kjb"><thead><tr><th align="left" id="d226967e2318">

Option or Field

</th><th align="left" id="d226967e2321">

Description

</th></tr></thead><tbody><tr><td id="d226967e2327">

**Update Notable Events upon SIR Incident Creation**

</td><td>

Select this option if you want to update the notable event status and add additional comments when a security incident is created from the notable event. This can occur for both the initial triggering notable events that create the security incident, as well as aggregated events.

</td></tr><tr><td id="d226967e2336">

**Initial Notable Event Status Update**

</td><td>

You must select a status option from the menu that displays all available status values retrieved from the Splunk Enterprise Security server. This may include a custom created status, such as ServiceNow - Assigned as shown in the screen shot below. Select the status value to be set for all notable events when a security incident is created for an ingested notable event. This includes notables that create new incidents and notables that are ingested and aggregated to an existing open incident.

</td></tr><tr><td id="d226967e2351">

**Initial Comments posted back to Notable Event**

</td><td>

In addition to updating the notable status value, you can also post comments to the notable event incident review history. As indicated in the instructions, you may edit the default text displayed in the comments section including adding or modifying the substitution variables using format $⁠\{field name\}$ for any field on the Security Incident Response incident form.

</td></tr><tr><td id="d226967e2363">

**Close out Notable Events upon SIR Incident Closure**

</td><td>

Select this option if you want to update the notable event status and add additional comments when a security incident is closed from the notable event. This will occur for both the initial triggering notable events that create the security incident, as well as aggregated events.

</td></tr><tr><td id="d226967e2373">

**Closure Notable Event Status Update**

</td><td>

You must select a status option from the list menu that displays all available status values that are retrieved from the Splunk Enterprise Security server. This may include a custom created status, such as ServiceNow - Assigned as shown in the screen shot below. Select the status value to be set for all notable events when a security incident is created for an ingested notable event. This includes notables that create new incidents as well as notables that are ingested and aggregated to an existing open incident.

</td></tr><tr><td id="d226967e2388">

**Closure Comments Posted back to Notable Event**

</td><td>

In addition to updating the notable status value, you can also post closure comments to the notable event incident review history. As indicated in the instructions, you may edit the default text displayed in the comments section including adding or modifying the substitution variables using format $⁠\{field name\}$ for any field on the Security Incident Response incident form.

</td></tr><tr><td id="d226967e2400">

**Update SIR Automation Activity with Splunk Event comments**

</td><td>

Option to update your Splunk Event comments in the SIR Automation Activity. The comment in the SIR Automation Activity appears with the prefix `Comment from Splunk`.**Note:**

Starting from Splunk Enterprise Security version 8.0.x, the comments field has been deprecated, and therefore our application can no longer retrieve comments from Splunk Enterprise Security.

</td></tr><tr><td id="d226967e2429">

**Update Splunk comments with SIR work notes**

</td><td>

Option to update your SIR work notes in the Splunk Event comments. The comment in Splunk Event appears with the prefix `Comment from ServiceNow`.

</td></tr></tbody>
</table>3.  Click **Finish** to complete the configuration.

    A confirmation dialog is displayed. You have successfully completed the setup and configuration for the integration. Activate this profile to pull notable events from the Splunk Enterprise Security console based on your scheduling. There is a limit of 1,000 security incidents that can be created in a 24-hour period. Up to 100 notable events are per fired alert. Subsequent notable events will be ignored after the limits are reached.

    The following image shows the Additional Options tab with default values populated:

    ![Additional Options:1](../image/splunk_es_additional_security.png)

    With the Additional Options configuration enabled, the notable event incident review shows the status change and an update to the history comments:

    ![Additional Options: 2](../image/splunk_es_additional1_security.png)


## Set up a profile for manual event forwarding

Depending on the profile defined, Splunk ES notable events are forwarded manually as discrete notable events into the Security Operations environment of your ServiceNow AI Platform instance.

To set up a profile for manual forwarding of notable events:

<table id="table_zs4_1xf_4jb"><thead><tr><th>

Task

</th><th>

Section

</th></tr></thead><tbody><tr><td>

Create an event profile

</td><td>

See [Create profiles for manually forwarded events](splunk-event-ingest-create-profile-security.md#)

</td></tr><tr><td>

Map notable event fields

</td><td>

See [Mapping notable event fields for the Splunk Enterprise Security integration](splunk-event-ingest-create-profile-security.md#)

</td></tr><tr><td>

Create custom mappings

</td><td>

See [Create mappings for Splunk ES notable event incident review and contributing event details \(manual forwarding\)](splunk-event-ingest-create-profile-security.md#)

</td></tr><tr><td>

Preview the security incident

</td><td>

See [Preview the security incident for the Splunk Enterprise Security Event Ingestion integration](splunk-event-ingest-create-profile-security.md#)

</td></tr><tr><td>

Set up your Splunk environment for manual ingestion

</td><td>

See [Set up your Splunk environment for manual event ingestion for the Splunk Enterprise Security Notable Event Ingestion integration](splunk-event-ingest-create-profile-security.md#)

</td></tr><tr><td>

Automate notable event updates and closure based on SIR incident status

</td><td>

See [Automate notable event updates and closure based on SIR incident status](splunk-event-ingest-create-profile-security.md#)

</td></tr></tbody>
</table>### Create profiles for manually forwarded events

You can set up a profile for manual forwarded events.

#### Before you begin

Role required: sn\_si.admin

#### Procedure

1.  To create a profile that supports manual event forwarding, follow these steps.

    For events that you forward on-demand from your Splunk Enterprise Security console, you can base the individual field mapping on any existing profile. Alternatively, you can create a new mapping grid for exported attachment data. Events that you forward manually are not scheduled in the event profile.

    1.  If not already selected, in the choice list for the Type field, select **Manual Event Forwarding**.

    2.  In the Mapping Option field that is displayed, from the choice list, choose one mapping option to continue.

        Refer to the following figures and tables for more information about the available mapping options in the Mapping Options choice list.

        ![Splunk: manual event forwarding](../image/splunk-manualevent1-security.png)

<table id="table_psp_nxq_chb"><thead><tr><th>

Option or field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Create new field mapping option

</td><td>

New field mapping for your event. If you do not have an existing field mapping that is similar to the profile that you are creating, select this option to create a new map.

</td></tr><tr><td>

Default profile

</td><td>

Default event forwarding profile for all Splunk events. Default is cleared \(deactivated\).

 When this option is enabled, this profile becomes the default profile for manual event forwarding. This profile is used when there is no match on source from the manually forwarded event. It becomes the default profile for all events with unknown sources.

 The Source field is unavailable if the default profile option is enabled.

</td></tr><tr><td>

Source \(Notable Event field\)

</td><td>

This is a field that typically defines the correlation rule that triggered the notable, for example, Brute Force Attacks. This field is unavailable if the default profile option is enabled.

 If available, this field permits unique event field mapping to security incident fields based on the splunk correlation rule that is typically different for different event types.

 If you want to manage different correlation rules separately, you can create different profile event profiles based on correlation rule to accomplish this requirement.

</td></tr><tr><td>

Automate Notable Event Updates

</td><td>

Select this check box if you want to update the notable event status and add additional comments when a SIR incident is created from the notable event and / or when the SIR incident is closed. This will occur for both the initial triggering notable events that creates the SIR incident, as well as aggregated events.

</td></tr><tr><td>

Source \(Splunk Server\)

</td><td>

The Splunk server that you configured as the source for notable events. If you have multiple Splunk servers configured, select the appropriate server for the notable event types that will be updated for the profile. You are required to enter a value.

</td></tr><tr><td>

Order

</td><td>

Default is 100. Leave this setting at the default.If you have created a large number of profiles, this value provides a run time execution priority when two or more profiles share triggering conditions. The workflow in the profile with the lowest number has the highest priority.

</td></tr><tr><td>

\(Optional\) Description

</td><td>

Text to help you distinguish this profile from other profiles.

</td></tr></tbody>
</table>        For a profile with a new field mapping, verify that you have entered a value in the Source type field and click **Continue** to proceed to the mapping step of the configuration.

        For a profile with an existing field mapping, refer to the following figure and table for more information.

        ![Manual: existing profile](../image/copy_mapping_security.png)

<table id="table_epm_wqf_dhb"><thead><tr><th>

Option or field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Select existing profile for field mapping

</td><td>

Reuse an existing field mapping for your new notable event profile. The Copy from profile field is displayed. Follow these steps to copy an existing field mapping for this profile.

 1.  To the left of the Copy from profile field that is displayed, click the search icon.
2.  In the Splunk ES Event Profiles list that is displayed, click the profile name that has the map that you want to copy.

The profile name is displayed in the Copy from profile field.

</td></tr><tr><td>

Default profile

</td><td>

Default event forwarding profile for all Splunk notable events with unmatched source. Default is cleared \(disabled\).

 When this option is enabled, this profile becomes the default profile for manual event forwarding.

 The Source field is unavailable if the default profile option is enabled.

</td></tr><tr><td>

Source \(Notable Event field\)

</td><td>

This is a field that typically defines the correlation rule that triggered the notable, for example, Brute Force Attacks. This field is unavailable if the default profile option is enabled.

 If available, this field permits unique event field mapping to security incident fields based on the splunk correlation rule that is typically different for different event types.

 If you want to manage different correlation rules separately, you can create different profile event profiles based on correlation rule to accomplish this requirement.

</td></tr><tr><td>

Automate Notable Events

</td><td>

Select this check box if you want to update the notable event status and add additional comments when a security incident is created from the notable event or when the security incident is closed. This occurs for both the initial triggering notable events that creates the security incident, as well as aggregated events.

</td></tr><tr><td>

Source \(Splunk Server\)

</td><td>

Splunk server or search end that you configured as the source for notable events. If you have multiple Splunk servers configured, select the appropriate server for the notable event types that will be updated for the profile. You are required to enter a value.

</td></tr><tr><td>

Order

</td><td>

Default is 100. Leave this setting at the default.If you have created multiple profiles, this value provides a run time execution priority when two or more profiles share triggering conditions. The workflow in the profile with the lowest number has the highest priority.

</td></tr><tr><td>

\(Optional\) Description

</td><td>

Text to help you distinguish this profile from other profiles.

</td></tr></tbody>
</table>        At the bottom of the form for selecting an existing mapping for your profile, click **Finish** to complete the profile configuration.


### Create mappings for Splunk ES notable event incident review and contributing event details \(manual forwarding\)

During the notable event field mapping step, you map individual event fields from notable events to fields on a ServiceNow AI Platform Security Incident Response \(SIR\) security incident.

#### Before you begin

Role required: sn\_si.admin

#### About this task

Map up to five notable events from the Notable Event Sample Ingestion column on the left of the form to the security incident fields in the SIR Incident Field Mapping column on the right.

Create custom mappings by adding or removing the fields on the mapping grid on the right side of the form. Default fields that are typically important field to populate on the SIR incident form are displayed. However, these fields can be removed and any additional fields can be displayed using the + and - buttons. Create custom maps by adding or removing the fields on the mapping grid on the right side of the form. Customizing the fields permits you to map Splunk fields that are not displayed on the default mapping grid on the SIR security incident.

#### Procedure

1.  If the mapping form is not displayed, click **Mapping** on the progress bar.

2.  Follow these steps to upload attachment data in your ServiceNow AI Platform® instance.

    1.  If not already logged in, log in to your Splunk Enterprise console.

    2.  Navigate to the Search tab and enter a name for a search that has the notable event data that you want to export.

        An example search format to retrieve notable events for the Brute Force Access Behavior correlation rule would be the following: \`notable\`\|search source="Access - Brute Force Access Behavior Detected - Rule".

    3.  Expand the notable event, and in the Field column, select the fields that you want to import.

        These fields are the field-value pairs that are exported and displayed on the Mapping page in your ServiceNow AI Platform® instance.

        ![Splunk ES: Select notable events for export](../image/splunk_es_export_XML.png)

    4.  In your Splunk Enterprise console, in the upper right of the Search page, click the **Export** icon.

    5.  In the choice list for the Format field in the dialog that is displayed, click **XML Format**.

    6.  Enter a new filename.

    7.  Click **Export**.

        ![Splunk ES: Export XML file](../image/splunk_es_export_XML_2.png)

        The exported Splunk notable event XML file must now be uploaded to your ServiceNow AI Platform® instance.

    8.  If the Mapping page is not already displayed in your ServiceNow AI Platform® instance, click **Mapping** in the progress bar.

    9.  In the Notable Event Sample Ingestion column, click **Load Attachment Data**.

        ![Splunk ES: Load attachment data](../image/splunk_es_load_attachment.png)

    10. In the dialog that is displayed, click **Choose files** and navigate to the `.xml` file that you exported and click **Open**.

        After you click to load attachment data for manually forwarded events, the Splunk ES notable event fields are populated on the left side of the form. These values are the field values that you map to the security incident fields on the Sir Incident Field Mapping side of the form.

        The value pairs for the fields that you exported for the event are displayed on the left side of the mapping form.

3.  Follow steps 5 to 10 in the [Create mappings for Splunk ES notable event incident review and contributing event details \(scheduled ingestion\)](splunk-event-ingest-create-profile-security.md#) section.


### Set up your Splunk environment for manual event ingestion for the Splunk Enterprise Security Notable Event Ingestion integration

Install and set up the ServiceNow Security Operations Event Ingestion Addon for Splunk Enterprise Security application in your Splunk enterprise console or Splunk Cloud instance if you want to export events manually and on-demand from your Splunk Enterprise Security console for this integration.

#### Before you begin

Installing and setting up the ServiceNow Security Operations Event Ingestion Addon for Splunk Enterprise Security application in your Splunk enterprise console or Splunk Cloud instance is optional.

Verify that you have installed the application for this integration from the ServiceNow Store prior to installing the addon plugin from splunkbase that is required for manual event ingestion. If you have not installed the application for the integration from the ServiceNow Store, see [Install and configure Splunk Enterprise Security Notable Event Ingestion integration](splunk-event-ingest-install-and-configure-security.md) and follow the instructions to install it.

Role required: Splunk Enterprise Security administrator

#### About this task

If you want to export events manually and on-demand from your Splunk Enterprise console for the integration, download, install, and set up the ServiceNow Security Operations Event Ingestion Addon for Splunk Enterprise Security from splunkbase in your Splunk Enterprise Security console. This ServiceNow extension addon is required so that security incidents can be created from manually exported events in your ServiceNow AI Platform instance. This ServiceNow Security Operations Event Ingestion Addon for Splunk Enterprise Security application is available on [splunkbase](https://splunkbase.splunk.com/).

For manual event forwarding, you can identify up to two different ServiceNow AI Platform endpoints \(instances\) in your Splunk Enterprise Security console. You forward the events to the endpoint or endpoints manually to create security incidents. For example, you can specify both a staging \(development\) instance and a production instance. By specifying separate instances and naming primary and secondary workflows for each instance, you can choose where you want to forward different events.

#### Procedure

1.  If you have not already installed the ServiceNow Security Operations Event Ingestion Addon for Splunk Enterprise Security, follow these steps to install and configure it.

    1.  Navigate to [splunkbase](https://splunkbase.splunk.com/).

    2.  Search for the ServiceNow Security Operations Security Operations Event Ingestion Addon for Splunk Enterprise Security.

        **Note:** Verify that you have selected ServiceNow Security Operations Event Ingestion Addon for Splunk Enterprise Security. There are additional ServiceNow addons that are displayed in this list. These addons are for different ServiceNow Splunk integrations, and they are not required for this integration.

    3.  Download the application.

    4.  Open your Splunk Enterprise Security account.

    5.  On the Apps page, click the gear icon or the **Manage Apps** shortcut on the menu drop-down list.

    6.  On the upper left of the Apps page that is displayed, click **Install app from file**.

    7.  Click **Choose File**, select ServiceNow Security Operations Event Ingestion Addon for Splunk Enterprise Security, and click **Upload**.

    8.  If prompted, restart Splunk Enterprise.

        The ServiceNow Security Operations Event Ingestion Addon for Splunk Enterprise Security is installed in your Splunk Enterprise Security console. The next step to set up the Addon.

2.  To set up the Addon, follow these steps.

    1.  In Splunk Enterprise Security, click the **Apps** gear icon or **Manage Apps** on the menu drop-down list.

    2.  On the list of applications that is displayed, in the **Actions** column, click **Set up** for ServiceNow Security Operations Event Ingestion Addon for Splunk Enterprise Security.

    3.  Fill out the form.

        The following figure is an example of a completed form in your Splunk Enterprise Security console.

        ![API endpoints](../image/splunk_es_api_endpoint_security.png)

<table id="choicetable_knk_rmg_wgb"><thead><tr><th align="left" id="d226967e3679">

Field on Specify ServiceNow Primary Instance section

</th><th align="left" id="d226967e3682">

Description

</th></tr></thead><tbody><tr><td id="d226967e3688">

**Workflow action label**

</td><td>

Name of the ServiceNow AI Platform workflow for your production \(primary\) instance. This name is the name of a ServiceNow AI Platform instance that your users who are monitoring Splunk events identify as a primary instance, for example, Servicenow Event Ingestion \(Production\).Default for this field is Servicenow Event Ingestion \(Production\).

 In your Splunk Enterprise Security console, this workflow name is displayed for the production \(Primary\) instance in the expanded `Event Actions` drop-down list of a search. This name is the name of your production instance. You can edit the name.

</td></tr><tr><td id="d226967e3718">

**URL**

</td><td>

The URL for the ServiceNow AI Platform instance you entered in the preceding Workflow action label field.Copy the URL in your browser and paste it in this field in the form.

</td></tr><tr><td id="d226967e3733">

**Endpoint**

</td><td>

Base API path. For more information, refer to the figure that follows the table.If you do not have a value for the endpoint of your ServiceNow AI Platform production instance, follow these steps.

 1.  Log in to your ServiceNow AI Platform production instance as a user with the system administrator \(admin\) role.
2.  Enter `Scripted REST APIs` in the navigation panel.
3.  After the navigation panel is refreshed, select the **Scripted REST APIs** module that is displayed.
4.  If Event Ingestion is not listed in the Name column of the `Scripted REST APIs` list that is displayed, in the search field at the top, enter `Event Ingestion`.
5.  In the Base API path column on the refreshed page, copy this value and paste it in the Endpoint field on the form. An example base api path is, `/api/sn_sec_splunk_v2/event_ingestion`.


</td></tr><tr><td id="d226967e3784">

**Username**

</td><td>

User name for your ServiceNow AI Platform instance. This name is the user name for the ServiceNow AI Platform instance in which you assigned a user with the \(sn\_sec\_splunk\_v2.api\_account\_access\) role for manual event forwarding. For more information about assigning this role, see [Set up your ServiceNow AI Platform instance for the Splunk Enterprise Event Ingestion integration](splunk-event-ingest-setup-sn.md).

</td></tr><tr><td id="d226967e3817">

**Password**

</td><td>

Password for your ServiceNow AI Platform instance.This password is the password for the ServiceNow AI Platform instance in which you assigned a user with the \(sn\_sec\_splunk\_v2.api\_account\_access\) role for manual event forwarding.

</td></tr><tr><td id="d226967e3835">

**\(Optional\) Fields on Specify ServiceNow Secondary Instance section**

</td><td>

Description These fields are optional. You are not required to specify a secondary instance.

</td></tr><tr><td id="d226967e3850">

**Workflow action label**

</td><td>

Name of the ServiceNow AI Platform workflow for your secondary \(staging\) instance. This name is the name of a ServiceNow AI Platform instance that your users who are monitoring Splunk events identify as a secondary instance, for example, ServiceNow Event Ingestion \(Staging\).In your Splunk Enterprise Security console, this workflow name is displayed for the staging \(Secondary\) instance in the expanded Event Actions drop-down list of a search. This ServiceNow AI Platform instance is your staging instance. You can edit the name.

</td></tr><tr><td id="d226967e3880">

**URL**

</td><td>

The URL for the ServiceNow AI Platform instance you entered in the preceding Workflow action label field for the secondary ServiceNow AI Platform instance.Copy the URL in your browser and paste it in this field in the form.

</td></tr><tr><td id="d226967e3898">

**Endpoint**

</td><td>

Base API path. This value for the Base API path for your secondary instance is the same value as the Base API path for your primary instance. See the preceding figure of the form for more information.

</td></tr><tr><td id="d226967e3907">

**Username**

</td><td>

Username for your ServiceNow AI Platform staging instance. The user must have the \(sn\_sec\_splunk\_v2.api\_account\_access\) role.

</td></tr><tr><td id="d226967e3920">

**Password**

</td><td>

Password for your ServiceNow AI Platform staging instance. The user must have the \(sn\_sec\_splunkes.api\_account\_access\) role.

</td></tr></tbody>
</table>    The following figure is an example of the Scripted REST APIs list in your ServiceNow AI Platform. The list displays the location of the endpoint value of a ServiceNow AI Platform instance that you enter in the form as part of the set up for the ServiceNow Security Operations Event Ingestion Addon for Splunk Enterprise Security extension in your Splunk Enterprise Security console.

    ![Base API path highlighted.](../image/splunk_es_api_path_security.png)

3.  In the setup form in your Splunk Enterprise Security console, click **Save** to save your edits.

    After a few moments, at the top left of the form in your Splunk Enterprise Security console, a message is displayed that the record is successfully updated.

    After you save the form, the names \(Workflow action labels\) for your ServiceNow AI Platform instance\(s\) that you created in the form are available from the Event Actions choice list on a selected event of a search in your Splunk Enterprise Security console.


#### What to do next

If you have not already save searches in your Splunk Enterprise Security console, the next step is to save searches as alerts in your Splunk Enterprise Security console.

