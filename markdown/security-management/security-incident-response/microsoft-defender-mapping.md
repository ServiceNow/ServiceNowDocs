---
title: Map incident fields
description: Map Microsoft Defender Incident, and Event Fields to SIR Incident Target Fields.
locale: en-US
release: australia
product: Security Incident Response
classification: security-incident-response
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 6
breadcrumb: [Microsoft Defender integration for Security Operations, Security Incident Response integrations, Security Incident Response, Enterprise security case management applications, Security Operations]
---

# Map incident fields

Map Microsoft Defender Incident, and Event Fields to SIR Incident Target Fields.

## Before you begin

Role required: sn\_si.admin, sn\_si.ingestion\_profile\_admin

## Procedure

1.  If you aren’t continuing from the previous section of the Name criteria, access the profile you’re defining.

    1.  Navigate to **All** &gt; **Microsoft Defender Integration** &gt; **Defender Incident Profiles**.

    2.  Select the profile that you’re continuing to define.

    3.  Select **Mapping** in the progress bar.

2.  Select one of the Sample Ingestion Methods in the Defender Incident Field Mapping section.

<table id="table_kyc_qbg_p4b"><thead><tr><th>

Field

</th><th colspan="2">

Description

</th></tr></thead><tbody><tr><td>

All default Incident and evidence files

</td><td colspan="2">

Use this ingestion method to view the static list of all the Incident, and Event fields. This method contains only default field names without any values.

</td></tr><tr><td>

Retrieve Recent Defender Incidents

</td><td colspan="2">

Use this ingestion method to import the most recent Defender Incidents. If the Defender incident contains multiple alerts, the earliest alert that is part of the incident is shown in the mapping section. During ingestion as well the earliest security alert field values will be used.

 You can ingest 5 sample incidents.

 The sample field values populate when the profile ingests the sample incidents. You can map these incidents to the **SIR Incident Target Fields**. The Incident fields and values appear as individual tabs.

</td></tr><tr><td>

Retrieve Defender Incidents based on ID

</td><td>

Incident IDs \(comma separated\)

</td><td>

Specify incident IDs separated by commas. You can ingest 5 incident IDs.

</td></tr></tbody>
</table>3.  To add fields to the default fields that are displayed on the security incident, do the following actions:

    1.  Select ![Map another field button.](../../secops-integration-ms-azure-sentinel/image/sentinel-map-button.png) in the SIR Incident Target Fields section.

        It shows a list of SIR fields, from which you can select a new field.

    2.  In the Security Incident column, expand the list that is displayed and then select a field.

        **Note:** Multiple observables can be displayed on the same security incident. For example, the **Observable** field can be mapped multiple times with different values. Similarly, the **Configuration Item** and **Work notes fields** support multiple values. If you try to map two values to a field that can't support multiple values, you see an error message that this field doesn’t support multiple values. Similarly, if a field on a security incident has a list from which you can choose multiple options, and you try to map an option to that field that is not displayed on the list, the field doesn’t populate on the security incident.

    3.  From the Incident Fields section, drag your field to map it to your new field.

    4.  When you select the check box that corresponds to a field, any new or updated changes made in Defender will automatically update the respective SIR incident data with the new incident data.

        **Note:** In the base system, the system property sn\_sec\_def\_sntl.incident\_updates is by default set True to receive Defender updates related to new incidents that are linked to SIR.

        -   By default, the Affected Users, Configuration items, and Observables fields are checked. This means that whenever there are new observables or associated configuration items, or affected users that get added to the incident then that information is automatically extracted and populated in the respective related lists in the Security Incident Response \(SIR\) during that polling interval.
        -   For any other fields, you must select the check box that corresponds to a field for any new or updated changes made in the Defender incident record within Defender. This will automatically replace the respective SIR incident data with the new incident data.
        **Important:** Due diligence is required to be done before selecting this functionality as overriding the existing data may result in unstable data for the analyst to work with and any other automation that is set even by the field values of security incident may also get affected. So, it’s important to do the due diligence before you select any override functionality.

4.  To remove a field, use the ![Remove button](../../secops-integration-ms-azure-sentinel/image/sentinel-remove-button.png) Remove item button next to the input expression field in the SIR Incident Target Fields section.

5.  To map a field value from the Incident and Event Fields section to a field on the SIR incident Target Fields section, use one of the following actions:

    1.  Drag the Incident field name \(for example, id\) and drop it next to a field name in the SIR incident Target Fields column.

        You can match any value from the Incident and Event fields section to a field on the SIR incident Target Fields section. Fields are color-coded so that you don’t overlook or duplicate incident fields in the mapping process. Light blue fields indicate that an incident field isn’t yet selected and mapped on the security incident. You may prefer to associate an incoming incident fields with more than one field on a security incident. A gray field indicates that a field has been selected and mapped to a field on the security incident. This way, you can visualize which field values have been added to the security incident and if any remaining important incident information remains unmapped.

    2.  You can add a combination of text and field.

        For example, `Incident name is ${Incidents: name}$`. Here, `Incident name is` can be manually entered while `${Incidents: ${name}$` is mapped from the Incident and Event Fields section.

    3.  You can manually enter and map a source Incident or Event field to a target field.

        -   To manually map a source incident field use the $⁠\{field name\}$ format. For example, to map an incident field Severity, the format is`${incidentWebUrl}$`.
        -   To manually add Incident, and Event fields, use the `${evidenceName: evidenceField}$` format. For example, `${Alert: category}$`, `${deviceEvidence: healthStatus}$`.
    This integration classifies certain observable subtypes. When you map a Defender field with the SIR observable field, the auto-classifies the observable. If you want to generically map the incoming Defender observable to the observable type in, then drag the Incident and Event field in the Observable field. However, if you’re aware of the observable type for the incoming Defender observable, then map specifically to the Observable type field. Some examples of specific observable types in include Observable\(Domain name\), Observable\(Email address\), Observable\(IP address \(V4\)\), and Observable\(Host name\).

    Sometimes, incident field values in Defender may not translate directly to the fields on the SIR security incident. For these values, you can use a script editor to format field values on the security incident during the mapping step. Use the script editor if you want to format values that are similar, but not identical.

6.  To format a field translation for a new field from a Defender Incident to match a field value on a Security Incident, select the **Click here** link in the **SIR Incident Target Fields** header.

7.  To modify the fields that support field translation, select the ![Field format button](../../secops-integration-ms-azure-sentinel/image/sentinel-field-format-button.png) script format field translation icon.

    The fields that support field translation are **Affected user**, **Configuration Item**, and **Priority**. For example, select ![Field format button](../../secops-integration-ms-azure-sentinel/image/sentinel-field-format-button.png) icon next to the Category. The Defender Field Translation script editor opens.

8.  Enter any changes to the script and select **Update** to save the changes and return to the Mapping page.

    For example, for Category define the following in the script editor:

    ```
    "<Incoming Defender Field Value>":"<Category to assign to the Security Incident>".
    ```

    This mapping confirms that a profile uses only configured categories.

9.  Continue mapping by adding or removing field values.

    You can use the same field values in the Incident Generation Conditions builder to define additional criteria that an incoming Incident must satisfy to create a security incident.

    ![Map incident fields](../image/ms-def-mapping.png)

10. Select **Continue**.


## What to do next

[Define filter and aggregation criteria](ms-def-filtering-and-aggregation.md)

