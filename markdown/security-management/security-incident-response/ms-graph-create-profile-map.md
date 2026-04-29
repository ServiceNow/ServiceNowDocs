---
title: Mapping alerts to security incident response fields
description: Map individual alert fields from triggered alerts to fields on a ServiceNow AI Platform security incident.
locale: en-US
release: australia
product: Security Incident Response
classification: security-incident-response
topic_type: concept
last_updated: "2026-03-12"
reading_time_minutes: 9
breadcrumb: [Map alert fields, Create a profile, Microsoft Graph Security API alert ingestion integration, Security Incident Response integrations, Security Incident Response, Enterprise security case management applications, Security Operations]
---

# Mapping alerts to security incident response fields

Map individual alert fields from triggered alerts to fields on a ServiceNow AI Platform security incident.

## Alert field mapping

As a user with the sn\_si.admin role, use the fields from the Sample Alerts section on the left and map them to the security incident fields in the SIR Incident Field Mapping column on the right panel. Edit the mapping configuration by dragging alert fields from the left side and dropping them on the SIR incident mapping section on the right. The mapping on the right associates the incoming alert field with an outgoing security incident field.

1.  After you have fetched the sample data, the next step is map the alert fields to the security incident. To map a field value from the left side of the form to a field on the security incident on the right side of the form, click-hold a blue field name on the left side of the form.
2.  Drag the field name, for example, `category`, and drop it on a field in the Input Expression column next to a field name in the Security Incident column.

    The field value is displayed in the Input Expression column. In the following image, `category` is mapped to the `Category` field on the security incident.

    ![Microsoft Azure Security API: mapping fields](../image/ms-graph-create-profile-3.png)

    However, you can match any value from the left side to a field on the right. Verify that the value is mapped correctly on the security incident during the preview step.

    To help you ensure that no alert fields are overlooked or duplicated in the mapping process, fields are color-coded. Color-coding of the alert fields helps you keep track of the alert values that you have already mapped as they become greyed out while all remaining unmapped fields appear in blue. This helps you better visualize which field values have been added to the security incident and if any remaining important alert information remains unmapped.

    Light blue fields on the left indicate that an alert field is not yet selected and mapped on the security incident. You may prefer to associate an incoming alert field with more than one field on a security incident. A gray field indicates that a field has been selected and mapped to a field on the security incident. This color-coding helps you track the mapping.

    **Note:**

    1.  To manually enter a value in the Input Expression field, enter it in the format $\{fieldname\}$. The alert field will be mapped to the security incident field.
    2.  You cannot map ingested alerts to the MITRE-ATT&amp;CK Framework fields in the security incident mapping section. If you still map the fields, the information will not be available as part of the MITRE-ATT&amp;CK card in the MITRE-ATT&amp;CK framework section in the security incident form. To associate the MITRE-ATT&amp;CK Techniques, use the [Auto Extraction Feature](../../../threat-intelligence/concept/auto-extract-technique-rules.md#) available as part of the MITRE-ATT&amp;CK Framework in the Threat Intelligence Module.
3.  To add fields to the default fields displayed on the security incident on the right side of the form, follow these steps.
    1.  On the right of the form in the SIR Incident Field Mapping section, at the bottom of the grid, click the plus \(+\) icon. A new field is displayed.
    2.  In the Security Incident column, expand the choice list that is displayed, and select a field.

        In the expanded choice list for the new field, some fields are shaded. In the following figure, Category has a gray background, because it has been mapped in the security incident. Similar to the color-coding for the alert fields on the left side of the form, this color-coding for the security incident fields on the right helps you track the already mapped SIR incident fields.

        ![Microsoft Graph Security API: mapping and color coding](../image/ms-graph-create-profile-4.png)

        **Note:** As multiple observables can be displayed on the same security incident, the Observable field can be mapped multiple times with different values. Similarly, the Configuration Item and Work notes fields support multiple values. If you try to map two values to a field that cannot support multiple values, when you preview the incident, an error message is displayed that there is no value for the field. Similarly, if a field on a security incident has a choice list from which you can choose multiple options, and you try to map an option to that field that is not displayed on the choice list, the field is not populated on the security incident.

    3.  Alternatively, type a value in the Search field for the new row.
    4.  From the left side of the form, left-click to select the Alert ID that you want in the Input Expression field. With the drag-and-drop feature, map it next to your new field.
4.  Continue mapping by adding or removing field values to the mapping.
5.  After you have completed the preceding field mapping steps, you can use the same field values in the Incident Generation Conditions builder to define additional criteria that an incoming alert must satisfy to create a security incident. To set incident generation conditions, follow these steps.

## Format field translation

In certain cases, alert field values in Microsoft Graph Security API may not translate directly to the fields on the SIR security incident. For these values, you can use a script editor to format field values on the security incident during the mapping step. Use the script editor if you want to format values that are similar, but not identical. For example, with the script editor, a category value of Malware Alert and Virus Infection may have different field values for the source category but both values can be translated to a common Malicious Code Activity in the Category field on the SIR security incident using the Format Field Translation functionality.

To use the script editor, click the \{\} icon. The script editor is displayed.

![Microsoft Graph Security API Field Translation](../image/ms-graph-create-profile-3b.png)

## Incident generation conditions

Once the mapping section is complete, you can set filter conditions so that you can specify which alerts should create security incidents versus which alerts should be filtered out, for example, low priority alerts. You can use the same field values in the Incident Generation Conditions builder to define additional criteria that an incoming alert must satisfy to create a security incident. To set incident generation conditions, follow these steps.

1.  Scroll to the Incident Generation Conditions section on the form and select the Filter based on conditions option. The Filter conditions builder is displayed. Use these filters to create security incidents that match the specific conditions described by the fields.

    The options in the choice lists for the first field in the Filter conditions builder match the fields that are displayed on the Alert Sample Ingestion section for the alert you ingested. These fields are dynamic and change depending on the alert that you ingest Criteria that you enter are case-sensitive, and they must match exactly the values of the alert. If you are not sure about the values to enter in the filter fields, you may prefer to return to your Microsoft Azure tenant and review your alerts for the keywords.

2.  Using the choice lists and fields of the conditions builder, set filters for the first row.
3.  To add more conditions, to the right of the fields, click **AND** or **OR**.
    -   If **AND**is selected, all conditions must be matched.
    -   If **OR**is selected, either condition can be matched.
4.  In the second row, set a second filter condition

    The following image is an example with two conditions that must be matched before security incidents are created.

    ![Microsoft Graph Security API: incident generation conditions](../image/ms-graph-create-profile-3c.png)

    You have set the triggering conditions so that security incidents are created only when both of the filtering conditions that you entered are matched.

    This type of filtering helps you isolate security alerts, and it limits the number of security incidents that you create. If additional filtering criteria are set, only alerts that are required are ingested without having to change the query or the triggered alert configuration.


## Alert aggregation criteria to handle similar alerts and prevent duplicate incidents

Define additional alert aggregation criteria that aggregates an incoming alert to an existing SIR security incident instead of creating similar, potentially duplicate incidents. Using field matching value criteria for each profile, this additional aggregation capability can reduce the number of active, overlapping security incidents by placing all related alert data on a single security incident. To set the criteria, follow these steps below:

1.  Scroll to the Alert Aggregation Criteria section on the form and select the Aggregation Conditions option. The Incident Field Matching Values columns are displayed. These field names are the fields on the security incident that include any custom fields that are configured on the SIR security incident.
2.  From the Available list, select the field values that you want to match on existing security incidents in your ServiceNow AI Platform and move them to the Selected list. All the field values that you select must be matched to append this incoming alert to an existing security incident. This includes fields, such as Observables and Configuration Items, that may have multiple alert field values mapped to them. All values must match. If only a subset of the values are matched, the alert aggregation conditions will not be met and a new security incident will be created. See screen shot below for multi-value field mapping.

    ![Microsoft Graph Security API: Alert Aggregation Criteria](../image/ms-graph-create-profile-3d.png)

    If a new alert matches all the values that are selected in the aggregation field conditions in the mapping step, the alert is automatically added to the most recently opened security incident with the same field values. As a user with the sn\_si.analyst role working with security incidents, you can view all the added aggregate alerts on a related list on a security incident. All of the aggregated alerts on a security incident are displayed on the Aggregated Microsoft Graph Alerts related list. This list details associated time stamps and aggregated field values. This information helps you understand why alerts are added to existing security incidents. If this tab is not displayed, scroll to the left side of the record under Related Links and click the **Show All Related Lists** link.

3.  \(Optional\) To log a work note for a new alert that is recently added on the security incident, select the check box to enable this option. The work note logs that a new alert has been added along with a link to the alert details and any other details that may have been added to the work note field in your mapping section.

    You have successfully mapped values from an alert to fields on a SIR security incident. Also, you have configured additional conditions to limit the creation of security incidents with filtering criteria. You also appended alerts or events to existing SIR security incidents.

4.  Click **Continue** to continue with the profile configuration. The next step is to preview the fields you mapped on a SIR security incident

