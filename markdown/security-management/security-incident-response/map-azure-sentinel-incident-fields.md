---
title: Map the Microsoft Azure Sentinel incident fields
description: Map the individual Microsoft Azure Sentinel incident fields to the fields on the SIR security incident so that you can create incidents with the mapped data.
locale: en-US
release: zurich
product: Security Incident Response
classification: security-incident-response
topic_type: task
last_updated: "2025-07-31"
reading_time_minutes: 7
breadcrumb: [Microsoft Azure Sentinel integration, Security Incident Response integrations, Security Incident Response, Enterprise security case management applications, Security Operations]
---

# Map the Microsoft Azure Sentinel incident fields

Map the individual Microsoft Azure Sentinel incident fields to the fields on the SIR security incident so that you can create incidents with the mapped data.

## Before you begin

**Important:**

Microsoft has extended the deprecation of the Azure Sentinel experience in the Azure portal from March 2026 to March 2027.

If you are currently using the Azure Sentinel integration with Security Incident Response \(SIR\), we strongly recommend migrating to the new Defender portal integration as soon as possible. The Defender integration includes a built-in migration utility that automatically converts your existing Sentinel profiles into Defender profiles, while ensuring continuity of incidents created through Sentinel after the transition. For more information, see [Microsoft Sentinel to Defender Migration Guide](https://support.servicenow.com/kb?id=kb_article_view&sysparm_article=KB2795226).

Role required: sn\_si.ingestion\_profile\_admin

**Note:** Users with the sn\_si.admin role can perform all operations available to a profile admin, as the sn\_si.admin role inherits the required permissions by default.

## Procedure

1.  On the mapping page, in the Azure Sentinel Field Mapping section, select one of the Sample Ingestion Methods.

<table id="table_kyc_qbg_p4b"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

All default Incident and entity fields

</td><td>

Use this ingestion method to view the static list of all the incidents and entity fields. This method contains only default field names without any values. You can use this information to map with the SIR fields.

</td></tr><tr><td>

Retrieve Recent Azure Sentinel incidents

</td><td>

Use this ingestion method to import the most recent incidents and entities data. If the Azure Sentinel incident contains the entity data, then the entity data is retrieved and it is available for mapping in the Azure Sentinel Source Fields section. Sometimes the Azure Sentinel incident may not contain the entity data, and hence the entity fields are not available for mapping in such a scenario.

 If the Azure Sentinel incident contains multiple alerts, the earliest alert that is part of the incident is shown in the mapping section. During ingestion as well the earliest security alert field values will be used.

 You can ingest 5 sample incidents by default and a maximum of 20 sample incidents.

 The sample incident field values populate when the profile ingests the sample incidents. You can map these incidents to the **SIR Incident Target Fields**. The incident fields and values appear as individual tabs.

</td></tr><tr><td>

Import Sample Data

</td><td>

Click **Import Sample Data** to import sample incidents from Azure Sentinel.This button appears when you select the Retrieve Recent Azure Sentinel incidents ingestion method.

 Retrieving sample incidents from Microsoft Azure Sentinel server may take a moment.

 Map these retrieved incidents to the **SIR Incident Target Fields**. The incident fields and values appear as individual tabs.

</td></tr></tbody>
</table>    ![Field mapping of Azure Sentinel incidents](../image/sentinel-field-mapping.png)

2.  To add fields to the default fields that are displayed on the security incident, do the following actions:

    1.  On the SIR Incident Target Fields section, click the ![Map another field button.](../image/sentinel-map-button.png) Map another field button.

        It shows a list of SIR fields, from which you can select a field for a new field to be displayed.

    2.  In the Security Incident column, expand the list that is displayed and then select a field.

        **Note:** Multiple observables can be displayed on the same security incident. For example, the **Observable** field can be mapped multiple times with different values. Similarly, the **Configuration Item** and **Work notes fields** support multiple values. If you try to map two values to a field that can't support multiple values, you see an error message that this field does not support multiple values. Similarly, if a field on a security incident has a list from which you can choose multiple options, and you try to map an option to that field that is not displayed on the list, the field does not populate on the security incident.

    3.  From the Azure Sentinel Source Fields section, drag and drop your field to map it to your new field.

    4.  When you select the checkbox that corresponds to a field, any new or updated changes made in Azure Sentinel will automatically update the respective SIR incident data with the new incident data.

        **Note:** In the base system, the system property sn\_sec\_sentinel.incident\_updates is by default set to True to receive the Microsoft Azure Sentinel updates related to new alerts that are linked to SIR.

        -   By default, the Affected Users, Configuration items, and Observables fields are checked. This means that whenever there are new observables or associated configuration items, or affected users that gets added to the incident then that information is automatically extracted and populated in the respective related lists in the Security Incident Response \(SIR\) during that polling interval.
        -   For any other fields, you must select the checkbox that corresponds to a field for any new or updated changes made in the Azure Sentinel incident record within Azure Sentinel. This will automatically update the respective SIR incident data with the new incident data.
        **Important:** Due diligence is required to be done before selecting this functionality as overriding the existing data may result in unstable data for the analyst to work with and any other automation that is set even by the field values of security incident may also get affected. So, it is very important to do the due diligence before you select any override functionality.

3.  To remove a field, use the ![Remove button](../image/sentinel-remove-button.png) Remove item button next to the input expression field in the SIR Incident Target Fields section.

4.  To map a field value from the Azure Sentinel Source Fields section to a field on the SIR Incident Target Fields section, use one of the following actions:

    1.  Drag the field name \(for example, id\) and drop it next to a field name in the SIR Incident Target Fields column.

        You can match any value from the Azure Sentinel Source Fields section to a field on the SIR Incident Target Fields section. Fields are color-coded so that you do not overlook or duplicate incident fields in the mapping process. Light blue fields indicate that an incident field is not yet selected and mapped on the security incident. You may prefer to associate an incoming incident field with more than one field on a security incident. A gray field indicates that a field has been selected and mapped to a field on the security incident. This way, you can visualize which field values have been added to the security incident and if any remaining important incident information remains unmapped.

    2.  You can add a combination of text and field.

        For example, `Incident name is ${name}$`. Here `Incident name is` can be manually entered while `${name}$` is mapped from the Azure Sentinel Source Fields section.

    3.  You can directly manually enter and map a source incident or entity field to a target field.

        -   To manually map a source incident field use the $⁠\{field name\}$ format. For example, to map an incident field Severity, the format is`$⁠{properties(severity)}$`.
        -   To manually add a source entity field, use the `$⁠{entity name: entity field}$` format. For example, to map an entity field Description of entity Security Alert, the format is `$⁠{SecurityAlert: properties(description)}$`.
    This integration classifies certain observable sub-types. When you map an Azure Sentinel field with the SIR observable field, the ServiceNow AI Platform auto-classifies the observable. If you want to generically map the incoming Azure Sentinel observable to the observable type in SIR, then drag and drop the Azure Sentinel field in the Observable field. However, if you aware of the observable type for the incoming Azure Sentinel observable in SIR, then map specifically to the SIR Observable type field. Some examples of specific observable types in SIR include Observable\(Domain name\), Observable\(Email address\), Observable\(IP address \(V4\)\), and Observable\(Host name\).

    If your incoming Azure Sentinel fields contain any MITRE-ATT&amp;CK information, then map it to the MITRE-ATT&amp;CK Technique field. Ensure that the incoming Azure Sentinel field contains the MITRE-ATT&amp;CK technique ID or technique name.

    Sometimes, incident field values in Microsoft Azure Sentinel may not translate directly to the fields on the SIR security incident. For these values, you can use a script editor to format field values on the security incident during the mapping step. Use the script editor if you want to format values that are similar, but not identical.

5.  To format a field translation for a new field from an Azure sentinel incident to match a field value on a Security Incident, click the **Click here** link in the **SIR Incident Target Fields** header.

6.  To modify the fields which support field translation, click the ![Field format button](../image/sentinel-field-format-button.png) script format field translation icon.

    The fields that support field translation are **Category**, **Configuration Item**, and **Priority**. For example, click on ![Field format button](../image/sentinel-field-format-button.png) icon next to the Category. The Azure Sentinel Field Translation script editor opens.

7.  Enter any changes to the script and click **Update** to save the changes and return to the Mapping page.

    For example, for Category define the following in the script editor:

    ```
    "<Incoming Sentinel Incident Field Value>" : "<Category to assign to the Security Incident>".
    ```

    This mapping ensures that a profile uses only configured categories.

8.  Continue your mapping by adding or removing field values.

    You can use the same field values in the Incident Generation Conditions builder to define additional criteria that an incoming incident must satisfy to create a security incident.

9.  To move to the Filtering and Aggregation section, click **Continue**.


## What to do next

Define and set filter conditions so that you can specify which incidents should create security incidents. You can use the same field values \(defined in the Mapping section\) in the Incident Generation Conditions builder \(in the Filtering and Aggregation section\) to define additional criteria that an incoming incident must satisfy to create a security incident.

