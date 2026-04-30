---
title: Mapping IBM QRadar offense fields to security incident response fields
description: Map individual offense, event, and flow fields to fields on a ServiceNow AI Platform SIR security incident.
locale: en-US
release: yokohama
product: Security Incident Response
classification: security-incident-response
topic_type: concept
last_updated: "2025-07-31"
reading_time_minutes: 10
breadcrumb: [Map offense fields, Setup IBM QRadar profile, Set up instance, IBM QRadar Offense Ingestion Integration, Security Incident Response integrations, Security Incident Response, Enterprise security case management applications, Security Operations]
---

# Mapping IBM QRadar offense fields to security incident response fields

Map individual offense, event, and flow fields to fields on a ServiceNow AI Platform SIR security incident.

## Offense field mapping

As a user with the sn\_si.admin role, use the fields from the Sample Offenses section on the left and map them to the security incident fields in the SIR Incident Field Mapping column. Edit the mapping configuration by dragging offense, event, or flow fields from the left side and dropping them on the ServiceNow SIR incident mapping section on the right. The mapping on the right associates the incoming offense field with an outgoing security incident field.

1.  After you have fetched the sample data, the next step is map the offense, event, or flow fields to the security incident. To map a field value from the left side of the form to a field on the security incident on the right side of the form, click-hold a blue field name on the left side of the form.
2.  Drag the field name, for example, `description`, and drop it on a field in the Input Expression column next to a field name in the Security Incident column.

    The field value is displayed in the Input Expression column. In the following image, `description` is mapped to the `Description` field on the security incident.

    ![IBM QRadar: Create Profile: Mapping: SIR1](../image/ibm-qradar-profile-mapping-sir1.png)

    **Note:** If you enter the event or flow field name manually in the Input Expression section, you must add a prefix as `${Event:eventfield}$` or `${Flow:flowfield}$` before the name of the field being mapped.

    ![IBM QRadar: Create Profile: Mapping: SIR2](../image/ibm-qradar-profile-mapping-sir2.png)

    To help you ensure that no offense, event, or flow fields are overlooked or duplicated in the mapping process, fields are color-coded. Color-coding of the offense fields helps you keep track of the offense values that you have already mapped as they become greyed out while all remaining unmapped fields appear in blue. This helps you better visualize which field values have been added to the security incident and if any remaining important offense information remains unmapped.

    Light blue fields on the left indicate that an offense field is not yet selected and mapped on the security incident. You may prefer to associate an incoming offense, event, or flow field with more than one field on a security incident. A gray field indicates that a field has been selected and mapped to a field on the security incident. This color-coding helps you track the mapping.

3.  To add fields to the default fields displayed on the security incident on the right side of the form, follow these steps:
    1.  On the right of the form in the SIR Incident Field Mapping section, at the bottom of the grid, click the plus \(+\) icon. A new field is displayed.
    2.  In the Security Incident column, expand the choice list that is displayed, and select a field.

        In the expanded choice list for the new field, some fields are shaded. In the following figure, Category has a gray background, because it has been mapped in the security incident. Similar to the color-coding for the offense fields on the left side of the form, this color-coding for the security incident fields on the right helps you track the already mapped SIR incident fields.

        ![IBM QRadar: Create Profile: Mapping: SIR3](../image/ibm-qradar-mapping-sir3.png)

        **Note:** As multiple observables can be displayed on the same security incident, the Observable field can be mapped multiple times with different values. Similarly, the Configuration Item and Work notes fields support multiple values. If you try to map two values to a field that cannot support multiple values, when you preview the incident, an error message is displayed that there is no value for the field. Similarly, if a field on a security incident has a choice list from which you can choose multiple options, and you try to map an option to that field that is not displayed on the choice list, the field is not populated on the security incident.

    3.  Alternatively, type a value in the Search field for the new row.
    4.  From the left side of the form, select the offense field and drag-and-drop it to an appropriate security incident field on the right.
4.  Remove fields by using the - icon next to the field name in the SIR incident field mapping section.
5.  Continue mapping by adding or removing field values to the mapping.

**Offense fields with multiple values**

-   Security incident fields such as **Category** and **User** fields, \(for example, Affected user, Assigned to\) available with the base product do not support multiple values.
-   The following IBM QRadar fields support multiple values:

    -   `categories`
    -   `destination_networks`
    -   `source_address_ids`
    -   `local_destination_address_ids`
    -   `remote_destination_ips`
    -   `rules_contributing_to_offense`
    -   `users`
    If you need to map the above fields to any Security Incident Response fields apart from CI and Observable type fields, you must create new Security Incident Response fields of type **List** and use them for mapping.

    **Note:** By default, only non-reference **List** type fields are supported.


**Format Field Translation**

In certain cases, offense field values in IBM QRadar may not translate directly to the fields on the SIR security incident. For these values, you can use a script editor to format field values on the security incident during the mapping step. Use the script editor if you want to format values that are similar, but not identical. For example, with the script editor, a category value of Malware Alert and Virus Infection may have different field values for the source category but both values can be translated to a common Malicious Code Activity in the Category field on the SIR security incident using the Format Field Translation functionality.

To use the script editor, click the ![IBM QRadar: Create Profile: script icon](../image/ibm-qradar-mapping-script-icon.png). The script editor is displayed.

![IBM QRadar: Create Profile: Script Editor](../image/ibm-qradar-mapping-script-editor.png)

Enter any changes to the script and click **Update** to save the changes and return to the Mapping page.

## Incident generation conditions

Once the mapping section is complete, you can set filter conditions so that you can specify which offenses should create security incidents versus which offenses should be filtered out, for example, low priority offenses. You can use the same field values in the Incident Generation Conditions builder to define additional criteria that an incoming offense must satisfy to create a security incident. To set incident generation conditions, follow these steps.

1.  Scroll to the **Incident Generation Conditions** section on the form and select the **Filter based on conditions** check box to enable the option.

    The Filter conditions builder is displayed. Use these filters to create security incidents that match the specific conditions described by the fields.

    The options in the choice lists for the first field in the Filter conditions builder match the fields that are displayed on the Sample QRadar Offense Ingestion section for the offenses you ingested. These fields are dynamic and change depending on the offenses that you ingest. Criteria that you enter are case-sensitive, and they must match exactly the values of the IBM QRadar offense. If you are not sure about the values to enter in the filter fields, you may prefer to return to your IBM QRadar console and review your offenses for the keywords.

    **Note:** The `categories`, `destination_networks`, `source_address_ids`, `local_destination_address_ids`,`remote_destination_ips`, `rules_contributing_to_offense`, and `users` offense fields can have multiple values \(as the values are stored in arrays\). As the filter condition can retrieve only strings, you must use the `contains` filter condition for these fields to ensure that the data is filtered correctly.

2.  Using the choice lists and fields of the conditions builder, set filters for the first row.
3.  To add more conditions, to the right of the fields, click **AND** or **OR**.
    -   If **AND** is selected, all conditions must be matched.
    -   If **OR** is selected, either condition can be matched.
4.  \(Optional\) In the second row, set a second filter condition.

    The following image is an example with two conditions that must be matched before security incidents are created.

    ![IBM QRadar: Create Profile: Mapping: SIR5](../image/ibm-qradar-mapping-sir5.png)

    You have set the incident generation conditions so that security incidents are created only when both of the filtering conditions that you entered are matched.

    This type of incident generation condition filtering helps you narrow down the offenses, and limit the number of unnecessary security incidents that you create without modifying the underlying rule or filters in IBM QRadar. If additional filtering criteria are set, only offenses that match all criteria are mapped to incidents.

    **Note:** If any of the offense field names have special characters such as quotes \(“\),hyphens \(‘\), underscores \(-\), or ampersands \(@\), these characters may need to be replaced for filtering purposes but a numerical suffix is appended to differentiate fields with duplicate offense names. For example, if the first offense field is `alerts.alert` and the second offense field is `alerts@alerts`, these fields cannot be uniquely identified as the remaining standard text characters are the same. In this case, a suffix is added to the second offense field and the field is renamed to `alerts@alert(1)` when displayed in the Filter Conditions list.


## Offense aggregation criteria to handle similar offenses and prevent duplicate incidents

Define additional offense aggregation criteria that aggregates an incoming offense to an existing SIR security incident instead of creating similar, potentially duplicate incidents. Using field matching value criteria for each profile, this additional aggregation capability can reduce the number of active, overlapping security incidents by placing all related offense data on a single security incident. To set the criteria, follow these steps below:

1.  Scroll to the Offense Aggregation Criteria section on the form and select the **Aggregation Conditions** check box to enable this option.

    The Incident Field Matching Values columns are displayed. These field names are the fields on the security incident that include any custom fields that are configured on the SIR security incident.

2.  From the Available list, select the field values that you want to match on existing security incidents in your ServiceNow AI Platform and move them to the Selected list.

    All the field values that you select must be matched to append this incoming alert to an existing security incident. This includes fields, such as Observables and Configuration Items, that may have multiple offense field values mapped to them. All values must match. If only a subset of the values are matched, the offense aggregation conditions will not be met and a new security incident will be created. See screen shot below for multi-value field mapping.

    ![IBM QRadar: Create Profile: Mapping: Aggregation](../image/ibm-qradar-profile-mapping-agg.png)

    If a new offense matches all the values that are selected in the aggregation field conditions in the mapping step, the new offense is automatically added to the most recently opened security incident with the same field values. As a user with the sn\_si.analyst role working with security incidents, you can view all the added aggregated offenses on a related list on a security incident. This list details associated time stamps and aggregated field values. This information helps you understand why these offenses are being aggregated to existing security incidents. If this tab is not displayed, scroll to the left side of the record under Related Links and click the **Show All Related Lists** link.

3.  \(Optional\) To log a work note for a new offense that is recently added on the security incident, select the check box to enable this option. The work note logs that a new offense has been added along with a link to the offense details and any other details that may have been added to the work note field in your mapping section.

    You have successfully mapped values from an IBM QRadar offense to fields on a security incident. Also, you have configured additional conditions to limit the creation of security incidents with incident generation filtering criteria. You also appended offenses to existing security incidents when offense field values match the configured aggregation criteria.

4.  Click **Continue** to continue with the profile configuration. The next step is to preview the fields you mapped on a SIR security incident

