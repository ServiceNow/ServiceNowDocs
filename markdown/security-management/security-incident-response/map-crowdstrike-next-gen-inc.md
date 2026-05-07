---
title: Map detection fields
description: Map the individual CrowdStrike Next-Gen detection fields to the fields on the SIR security incident so that you can create detections with the mapped data.
locale: en-US
release: australia
product: Security Incident Response
classification: security-incident-response
topic_type: task
last_updated: "2026-05-06"
reading_time_minutes: 7
breadcrumb: [CrowdStrike Next-Gen SIEM integration, Security Incident Response integrations, Security Incident Response, Enterprise security case management applications, Security Operations]
---

# Map detection fields

Map the individual CrowdStrike Next-Gen detection fields to the fields on the SIR security incident so that you can create detections with the mapped data.

## Before you begin

Role required: sn\_si.ingestion\_profile\_admin

**Note:** Users with the sn\_si.admin role can perform all operations available to a profile admin, as the sn\_si.admin role inherits the required permissions by default.

## Procedure

1.  On the mapping page, in the CrowdStrike Next-Gen Field Mapping section, select one of the Sample Ingestion Methods.

<table id="table_kyc_qbg_p4b"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

All default Detection and Events Fields

</td><td>

Use this ingestion method to view the static list of all the detections and event fields. This method contains only default field names without any values. You can use this information to map with the SIR fields.

</td></tr><tr><td>

Retrieve Recent Detections

</td><td>

Use this ingestion method to import the most recent Detections and entities data. If the CrowdStrike Next-Gen detection contains multiple alerts, the earliest alert that is part of the detection is shown in the mapping section. During ingestion as well the earliest security alert field values will be used.

 You can ingest 5 sample detections.

 The sample detection field values populate when the profile ingests the sample detections. You can map these detections to the **SIR Incident Target Fields**. The Detection fields and values appear as individual tabs.

</td></tr></tbody>
</table>2.  To add fields to the default fields that are displayed on the security incident, do the following actions:

    1.  On the SIR Incident Target Fields section, select the ![Map another field button.](../../secops-integration-ms-azure-sentinel/image/sentinel-map-button.png) Map another field button.

        It shows a list of SIR fields, from which you can select a field for a new field to be displayed.

    2.  In the Security Incident column, expand the list that is displayed and then select a field.

        **Note:** Multiple observables can be displayed on the same security incident. For example, the **Observable** field can be mapped multiple times with different values. Similarly, the **Configuration Item** and **Work notes fields** support multiple values. If you try to map two values to a field that can't support multiple values, you see an error message that this field does not support multiple values. Similarly, if a field on a security incident has a list from which you can choose multiple options, and you try to map an option to that field that is not displayed on the list, the field does not populate on the security incident.

    3.  From the Detection and Event Fields section, drag and drop your field to map it to your new field.

    4.  When you select the check box that corresponds to a field, any new or updated changes made in CrowdStrike will automatically update the respective SIR incident data with the new incident data.

        **Note:** In the base system, the system property sn\_sec\_cs\_ngsiem.detection\_updates is by default set to False to receive the CrowdStrike Next- Gen updates related to new alerts that are linked to SIR.

        -   By default, the Affected Users, Configuration items, and Observables fields are checked. This means that whenever there are new observables or associated configuration items, or affected users that gets added to the incident then that information is automatically extracted and populated in the respective related lists in the Security Incident Response \(SIR\) during that polling interval.
        -   After ingestion, Security Incident records show Unmatched CI in the Configuration Items related list and Unmatched Affected Users in a dedicated related list when matching CMDB or identity records are not found, ensuring complete visibility of affected entities throughout the incident life-cycle.
        -   For any other fields, you must select the check box that corresponds to a field for any new or updated changes made in the CrowdStrike detection record within CrowdStrike. This will automatically update the respective SIR incident data with the new detection data.
        **Important:** Due diligence is required to be done before selecting this functionality as overriding the existing data may result in unstable data for the analyst to work with and any other automation that is set even by the field values of security incident may also get affected. So, it is very important to do the due diligence before you select any override functionality.

3.  To remove a field, use the ![Remove button](../../secops-integration-ms-azure-sentinel/image/sentinel-remove-button.png) Remove item button next to the input expression field in the SIR Incident Target Fields section.

4.  To map a field value from the Detection and Event Fields section to a field on the SIR incident Target Fields section, use one of the following actions:

    1.  Drag the Detection field name \(for example, id\) and drop it next to a field name in the SIR incident Target Fields column.

        You can match any value from the Detection and Event Fields section to a field on the SIR incident Target Fields section. Fields are color-coded so that you do not overlook or duplicate detection fields in the mapping process. Light blue fields indicate that an detection field is not yet selected and mapped on the security incident. You may prefer to associate an incoming detection fields with more than one field on a security incident. A gray field indicates that a field has been selected and mapped to a field on the security incident. This way, you can visualize which field values have been added to the security incident and if any remaining important incident information remains unmapped.

    2.  You can add a combination of text and field.

        For example, `Detection name is ${Detections: name}$`. Here `Detection name is` can be manually entered while `${Detections: name}$` is mapped from the Detection and Event Fields section.

    3.  You can directly manually enter and map a source detection or events fields to a target field.

        -   To manually map a source detection field use the $⁠\{field name\}$ format. For example, to map a detection field Severity, the format is`${Detections: severity}$`.
        -   To manually add a source events fields, use the `$⁠{events names: events fields}$` format. For example, to map an events fields Description of events Security Alert, the format is `${Events: description}$`.
    This integration classifies certain observable sub-types. When you map a CrowdStrike Next- Gen field with the SIR observable field, the ServiceNow AI Platform auto-classifies the observable. If you want to generically map the incoming CrowdStrike Next- Gen observable to the observable type in SIR, then drag and drop the Detection and Event field in the Observable field. However, if you aware of the observable type for the incoming CrowdStrike Next- Gen observable in SIR, then map specifically to the SIR Observable type field. Some examples of specific observable types in SIR include Observable\(Domain name\), Observable\(Email address\), Observable\(IP address \(V4\)\), and Observable\(Host name\).

    If your incoming CrowdStrike Next- Gen fields contain any MITRE-ATT&amp;CK information, then map it to the MITRE-ATT&amp;CK Technique field. Ensure that the incoming CrowdStrike Next- Gen field contains the MITRE-ATT&amp;CK technique ID or technique name.

    Sometimes, detection field values in CrowdStrike Next- Gen may not translate directly to the fields on the SIR security incident. For these values, you can use a script editor to format field values on the security incident during the mapping step. Use the script editor if you want to format values that are similar, but not identical.

5.  To format a field translation for a new field from a CrowdStrike Next- Gen detection to match a field value on a Security Incident, select the **Click here** link in the **SIR Incident Target Fields** header.

6.  To modify the fields which support field translation, select the ![Field format button](../../secops-integration-ms-azure-sentinel/image/sentinel-field-format-button.png) script format field translation icon.

    The fields that support field translation are **Affected user**, **Configuration Item**, and **Priority**. For example, click on ![Field format button](../../secops-integration-ms-azure-sentinel/image/sentinel-field-format-button.png) icon next to the Category. The CrowdStrike Next- Gen Field Translation script editor opens.

7.  Enter any changes to the script and select **Update** to save the changes and return to the Mapping page.

    For example, for Category define the following in the script editor:

    ```
    "<Incoming CrowdStrike Detection Field Value>" : "<Category to assign to the Security Incident>".
    ```

    This mapping ensures that a profile uses only configured categories.

8.  Continue your mapping by adding or removing field values.

    You can use the same field values in the Detection Generation Conditions builder to define additional criteria that an incoming detection must satisfy to create a security incident.

9.  To move to the Filtering and Aggregation section, select **Continue**.


## What to do next

Define and set filter conditions so that you can specify which detections should create security incidents. You can use the same field values \(defined in the Mapping section\) in the detection Generation Conditions builder \(in the Filtering and Aggregation section\) to define additional criteria that an incoming detection must satisfy to create a security incident.

