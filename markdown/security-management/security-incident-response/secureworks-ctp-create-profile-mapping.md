---
title: Mapping Secureworks ticket fields to security incident response fields
description: Map individual ticket or event fields to fields on a ServiceNow AI Platform SIR security incident.
locale: en-US
release: yokohama
product: Security Incident Response
classification: security-incident-response
topic_type: concept
last_updated: "2025-01-30"
reading_time_minutes: 8
breadcrumb: [Mapping of ticket fields for the SecureWorks CTP integration, Create a profile for Secureworks CTP ticket ingestion integration, Secureworks CTP Ticket Ingestion Integration, Security Incident Response integrations, Security Incident Response, Enterprise security case management applications, Security Operations]
---

# Mapping Secureworks ticket fields to security incident response fields

Map individual ticket or event fields to fields on a ServiceNow AI Platform SIR security incident.

## Ticket field mapping

As a user with the sn\_si.admin role, use the fields from the Sample Tickets section on the left and map them to the security incident fields in the **SIR Incident Field Mapping** column. Edit the mapping configuration by dragging ticket or event fields from the left side and dropping them on the SIR Incident Field Mapping section on the right. The mapping on the right associates the incoming ticket field with an outgoing security incident field.

1.  To map a field value from the left side of the form to a field on the security incident on the right side of the form, click-hold a blue field name on the left side of the form.
2.  You can manually enter the field name in the Input Expression column or drag and drop the field name. For example, `description`, and drop it on a field in the **Input Expression** column next to a field name in the **Security Incident** column.

    The field value is displayed in the Input Expression column. In the following image, `categoryClass` is mapped to the `Category` field on the security incident.

    ![Secureworks CTP: Create Profile: Mapping](../image/secureworks-create-profile-mapping-1.gif)

    **Note:** If you enter the event field name manually in the **Input Expression** section, you must add a prefix as `${Event:eventfield}$` before the name of the field being mapped.

    To help you ensure that no ticket or event fields are overlooked or duplicated in the mapping process, fields are color-coded. Color-coding of the ticket fields helps you keep track of the ticket values that you have already mapped as they become greyed out while all remaining unmapped fields appear in blue. This helps you better visualize which field values have been added to the security incident and if any remaining important ticket information remains unmapped.

    Light blue fields on the left indicate that a ticket field is not yet selected and mapped on the security incident. You may prefer to associate an incoming ticket or event field with more than one field on a security incident. A gray field indicates that a field has been selected and mapped to a field on the security incident. This color-coding helps you track the mapping.

3.  To add fields to the default fields displayed on the security incident on the right side of the form, follow these steps:
    1.  On the right of the form in the SIR Incident Field Mapping section, at the bottom of the grid, click the plus \(+\) icon. A new field is displayed.
    2.  In the Security Incident column, expand the choice list that is displayed, and select a field.

        In the expanded choice list for the new field, some fields are shaded. In the following figure, Category has a gray background, because it has been mapped in the security incident. Similar to the color-coding for the ticket fields on the left side of the form, this color-coding for the security incident fields on the right helps you track the already mapped SIR incident fields.

        ![Secureworks CTP: Create Profile: mapping selection](../image/secureworks-create-profile-mapping-2.gif)

        **Note:** As multiple observables can be displayed on the same security incident, the Observable field can be mapped multiple times with different values. Similarly, the Configuration Item and Work notes fields support multiple values. If you try to map two values to a field that cannot support multiple values, when you preview the incident, an error message is displayed that there is no value for the field. Similarly, if a field on a security incident has a choice list from which you can choose multiple options, and you try to map an option to that field that is not displayed on the choice list, the field is not populated on the security incident.

    3.  Alternatively, type a value in the Search field for the new row.
    4.  From the left side of the form, select the ticket field and drag-and-drop it to an appropriate security incident field on the right.
4.  Remove fields by using the - icon next to the field name in the SIR Incident Field Mapping section.
5.  Continue mapping by adding or removing field values to the mapping.

**Format Field Translation**

In certain cases, ticket fields may not translate directly to the fields on the SIR security incident. For these values, you can use a script editor to format field values on the security incident during the mapping step. Use the script editor if you want to format values that are similar, but not identical. For example, with the script editor, a category value of Malware Alert and Virus Infection may have different field values for the source category but both values can be translated to a common Malicious Code Activity in the Category field on the SIR security incident using the Format Field Translation functionality.

To use the script editor, click the \{\} icon next to the Category field. The script editor is displayed

![Secureworks CTP: Create Profile: Script Editor](../image/secureworks-create-profile-mapping-3.gif)

.

Enter any changes to the script and click **Update** to save the changes and return to the Mapping page.

## Incident generation conditions

Once the mapping section is complete, you can set filter conditions so that you can specify which tickets should create security incidents versus which tickets should be filtered out, for example, low priority tickets. You can use the same field values in the Incident Generation Conditions builder to define additional criteria that an incoming ticket must satisfy to create a security incident. To set incident generation conditions, follow these steps.

1.  Scroll to the **Incident Generation Conditions** section on the form and select the **Filter based on conditions** check box to enable the option.

    The Filter conditions builder is displayed. Use these filters to create security incidents that match the specific conditions described by the fields.

    The options in the choice lists for the first field in the Filter conditions builder match the fields that are displayed on the **Sample Ticket Ingestion** section for the ingested tickets. These fields are dynamic and change depending on the tickets that you ingest. Criteria that you enter are case-sensitive, and they must match exactly the values of the Secureworks CTP ticket. If you are not sure about the values to enter in the filter fields, you may prefer to return to your Secureworks CTP console and review your tickets for the keywords.

    **Note:** The `worklogs`, `devices`, `attachments`, `watchers`, `availableactions`, and `closeCodes` ticket fields can have multiple values \(as the values are stored in arrays\). As the filter condition can retrieve only strings, you must use the `contains` filter condition for these fields to ensure that the data is filtered correctly.

2.  Using the choice lists and fields of the conditions builder, set filters for the first row.
3.  To add more conditions, to the right of the fields, click **AND** or **OR**.
    -   If **AND** is selected, all conditions must be matched.
    -   If **OR** is selected, either condition can be matched.
4.  \(Optional\) In the second row, set a second filter condition.

    This type of incident generation condition filtering helps you narrow down the tickets, and limit the number of unnecessary security incidents that you create without modifying the underlying rule or filters. If additional filtering criteria are set, only tickets that match all criteria are mapped to security incidents.


## Ticket aggregation criteria to handle similar tickets and prevent duplicate incidents

Define additional ticket aggregation criteria that aggregates an incoming ticket to an existing SIR security incident instead of creating similar, potentially duplicate incidents. Using field matching value criteria for each profile, this additional aggregation capability can reduce the number of active, overlapping security incidents by placing all related ticket data on a single security incident. To set the criteria, follow these steps below:

1.  Scroll to the **Ticket Aggregation Criteria** section on the form and select the **Aggregation Conditions** check box to enable this option.

    The Incident Field Matching Values columns are displayed. These field names are the fields on the security incident that include any custom fields that are configured on the SIR security incident.

2.  From the Available list, select the field values that you want to match on existing security incidents in your NOW Platform and move them to the Selected list.

    All the field values that you select must be matched to append this incoming ticket to an existing security incident. This includes fields, such as Observables and Configuration Items, that may have multiple ticket field values mapped to them. All values must match. If only a subset of the values are matched, the ticket aggregation conditions will not be met and a new security incident will be created. See screen shot below for multi-value field mapping.

    ![Secureworks CTP: Create Profile: Mapping: Aggregation](../image/secureworks-create-profile-mapping-4.gif)

    If a new ticket matches all the values that are selected in the aggregation field conditions in the mapping step, the new ticket is automatically added to the most recently opened security incident with the same field values. As a user with the sn\_si.analyst role working with security incidents, you can view all the added aggregated tickets on a related list on a security incident. This list details associated time stamps and aggregated field values. This information helps you understand why these tickets are being aggregated to existing security incidents. If this tab is not displayed in a security incident, scroll to the left side of the record under **Related Links** and click the **Show All Related Lists** link.

    **Note:** The Secureworks Aggregated Tickets related list is not available with the base system. You must configure the Related List layout and explicitly include it with the other related lists.

3.  \(Optional\) To log a work note for a new ticket that is recently added on the security incident, select the check box to enable this option. The work note logs that a new ticket has been added along with a link to the ticket details and any other details that may have been added to the work note field in your mapping section.

    You have successfully mapped values from a Secureworks CTP ticket to fields on a security incident. Also, you have configured additional conditions to limit the creation of security incidents with incident generation filtering criteria. You also appended tickets to existing security incidents when ticket field values match the configured aggregation criteria.

4.  Click **Continue** to continue with the profile configuration. The next step is to preview the fields you mapped on a SIR security incident

