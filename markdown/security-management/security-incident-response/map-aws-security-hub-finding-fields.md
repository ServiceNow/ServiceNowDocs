---
title: Map the AWS Security Hub finding fields
description: Map the individual AWS Security Hub finding fields to the fields on the SIR security incident so that you can create incidents with the mapped data.
locale: en-US
release: yokohama
product: Security Incident Response
classification: security-incident-response
topic_type: task
last_updated: "2025-07-31"
reading_time_minutes: 6
breadcrumb: [Amazon Web Services \(AWS\) Security Hub integration, Security Incident Response integrations, Security Incident Response, Enterprise security case management applications, Security Operations]
---

# Map the AWS Security Hub finding fields

Map the individual AWS Security Hub finding fields to the fields on the SIR security incident so that you can create incidents with the mapped data.

## Before you begin

Role required: sn\_si.admin

## Procedure

1.  On the mapping page, in the AWS Security Hub Mapping section, select one of the Sample Ingestion Methods.

<table id="table_kyc_qbg_p4b"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

All default finding fields

</td><td>

Use this ingestion method to view the static list of all the findings fields. This method contains only default field names without any values. You can use this information to map with the SIR fields.

</td></tr><tr><td>

Retrieve Recent AWS Security Hub findings

</td><td>

Use this ingestion method to import the most recent findings data. You can ingest 5 sample findings by default and a maximum of 20 sample findings.

 The sample finding field values populate when the profile ingests the sample findings. You can map these findings to the **SIR Incident Target Fields**. The finding fields and values appear as individual tabs.

</td></tr><tr><td>

Import Sample Data

</td><td>

Select **Import Sample Data** to import sample findings from AWS Security Hub.This button appears when you select the Retrieve Recent AWS Security Hub findings ingestion method.

Retrieving sample findings from AWS Security Hub server takes some moments.

Map these findings to the **SIR Incident Target Fields**. The finding fields and values appear as individual tabs.

</td></tr></tbody>
</table>2.  To add fields to the default fields that are displayed on the security incident, do the following actions:

    On the SIR Incident Target Fields section, select the ![Map another field button.](../../secops-integration-ms-azure-sentinel/image/sentinel-map-button.png) button. It shows a list of SIR fields, from which you can select to display a new field.

    1.  In the Security Incident column, expand the list that is displayed and then select a field.

        **Note:** Multiple observables can be displayed on the same security incident. For example, the **Observable** field can be mapped multiple times with different values. Similarly, the **Configuration Item** and **Work notes fields** support multiple values. If you try to map two values to a field that can't support multiple values, you see an error message that this field doesn’t support multiple values. Similarly, if a field on a security incident has a list from which you can choose multiple options, and you try to map an option to that field that is not displayed on the list, the field doesn’t populate on the security incident.

    2.  From the AWS Security Hub Source Fields section, drag your field to map it to your new field.

    3.  When you select the check box that corresponds to a field, any new or updated changes made in AWS Security Hub are automatically updated in the respective SIR with new incident data.

        **Note:** In the base system, the system property sn\_sec\_security.finding\_updates is by default set to True to receive the AWS Security Hub updates related to new alerts that are linked to SIR.

        -   By default, the Affected Users, Configuration items, and Observables fields are checked. This means that whenever there are new observables or associated configuration items, or affected users that get added to the incident then that information is automatically extracted and populated in the respective related lists in the Security Incident Response \(SIR\) during that polling interval.
        -   For any other fields, you must select the check box that corresponds to a field for any new or updated changes made in the finding in AWS Security Hub. This automatically updates the respective SIR incident data with the new incident data.
        **Important:** Due diligence is required to be done before selecting this functionality as overriding the existing data may result in unstable data for the analyst to work with and any other automation that is set even by the field values of security incident may also get affected. So, it is important to do the due diligence before you select any override functionality.

3.  To remove a field, use the ![Remove button](../../secops-integration-ms-azure-sentinel/image/sentinel-remove-button.png), \(**Remove item**\) button next to the input expression field in the SIR Incident Target Fields section.

4.  To map a field value from the AWS Security Hub Source Fields section to a field on the SIR Incident Target Fields section, use one of the following actions:

    1.  Drag the field name \(for example, id\) and drop it next to a field name in the SIR Incident Target Fields column.

        You can match any value from the AWS Security Hub Source Fields section to a field on the SIR Incident Target Fields section. Fields are color-coded so that you don’t overlook or duplicate finding fields in the mapping process. Light blue fields indicate that a finding field isn’t yet selected and mapped on the security incident. You may prefer to associate an incoming finding field with more than one field on a security incident. A gray field indicates that a finding field has been selected and mapped to a field on the security incident. This way, you can visualize which field values have been added to the security incident and if any remaining important finding information remains unmapped. However, there are some fields in the AWS Security Hub Source Fields section that aren’t compatible with fields on the SIR Incident Target Fields section. If you map such values, it isn’t displayed when the SIR is created.

    2.  You can add a combination of text and field.

        For example, `Finding name is ${name}$`. Here, `Finding name is` can be manually entered while `${name}$` is mapped from the AWS Security Hub Source Fields section.

    3.  You can manually enter and map a source finding field to a target field.

        Use the $⁠\{field name\}$ format to manually map a source finding field. For example, to map a finding field Severity, the format is`$⁠{properties(severity)}$`.

    This integration classifies certain observable sub-types. When you map an AWS Security Hub finding field with the SIR observable field, the ServiceNow AI Platform auto-classifies the observable. If you want to generically map the incoming AWS Security Hub observable to the observable type in SIR, then drag and drop the AWS Security Hub field in the Observable field. However, if you are aware of the observable type for the incoming AWS Security Hub observable in SIR, then map specifically to the SIR Observable type field. Some examples of specific observable types in SIR include Observable\(Domain name\), Observable\(Email address\), Observable\(IP address \(V4\)\), and Observable\(Host name\).

    Sometimes, finding field values in AWS Security Hub may not translate directly to the fields on the SIR security incident. For these values, you can use a script editor to format field values on the security incident during the mapping step. Use the script editor if you want to format values that are similar, but not identical.

5.  To format a field translation for a new field from an AWS Security Hub finding to match a field value on a Security Incident, click the **Click here** link in the **SIR Incident Target Fields** header.

6.  To modify the fields which support field translation, click the ![Field format button](../../secops-integration-ms-azure-sentinel/image/sentinel-field-format-button.png) script format field translation icon.

    The fields that support field translation are **Category**, **Configuration Item**, and **Priority**. For example, click on ![Field format button](../../secops-integration-ms-azure-sentinel/image/sentinel-field-format-button.png) icon next to the Category. The AWS Security Hub findings Field Translation script editor opens.

7.  Enter any changes to the script and click **Update** to save the changes and return to the Mapping page.

    For example, for Category define the following in the script editor:

    ```
    "<Incoming Security Hub finding Field Value>" : "<Category to assign to the Security Incident>".
    ```

    This mapping ensures that a profile uses only configured categories.

8.  Continue your mapping by adding or removing field values.

    You can use the same field values in the Incident Generation Conditions builder to define additional criteria that an incoming finding must satisfy to create a security incident.

9.  To move to the Filtering and Aggregation section, click **Continue**.


## What to do next

Define and set filter conditions so that you can specify which findings create security incidents. You can use the same field values \(defined in the Mapping section\) in the Incident Generation Conditions builder \(in the Filtering and Aggregation section\) to define additional criteria that an incoming finding must satisfy to create a security incident.

