---
title: Automate incident updates and closures
description: Automate incident updates and closures based on the incident status. The Cortex XSIAM integration enables incidents to create security incidents and also to update the incidents after they are created or closed.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/zurich/security-management/security-incident-response/pan-xsiam-automate-inc-updates.html
release: zurich
product: Security Incident Response
classification: security-incident-response
topic_type: task
last_updated: "2026-08-20"
reading_time_minutes: 5
breadcrumb: [Security Incident Response Integration with Cortex XSIAM by Palo Alto Networks, Security Incident Response integrations, Security Incident Response, Enterprise security case management applications, Security Operations]
---

# Automate incident updates and closures

Automate incident updates and closures based on the incident status. The Cortex XSIAM integration enables incidents to create security incidents and also to update the incidents after they are created or closed.

## Before you begin

Role required: sn\_si.admin, sn\_si.ingestion\_profile\_admin

## Procedure

1.  If you aren't continuing from the previous section of the Scheduling process, access the profile you're defining.

    1.  Navigate to **All** &gt; **Palo Alto Networks XSIAM** &gt; **XSIAM Profile**.

    2.  Select the profile you're continuing to define.

    3.  Select **Additional Options** in the progress bar.

2.  On the form, fill in the fields.

<table id="table_kyc_qbg_p4b"><thead><tr><th>

Category

</th><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td rowspan="3">

Security Incident Creation Updates

</td><td>

Update incident status upon SIR Incident Creation

</td><td>

Option to use the automated incident update functionality. The Cortex XSIAM incident status is updated with the comments after the SIR incident is created in the ServiceNow AI Platform.

</td></tr><tr><td>

Initial incident status update

</td><td>

Initial incident status that is updated in the Cortex XSIAM environment, either New or In Progress.

</td></tr><tr><td>

Initial comments posted back to incident

</td><td>

Initial comments that are posted to the incident in the Cortex XSIAM environment.

</td></tr><tr><td rowspan="3">

Security Incident Closure Updates

</td><td>

Close out XSIAM incidents upon SIR Incident Closure

</td><td>

Option to use the automated incident status update functionality. Incidents will be closed in XSIAM with the comments given after the SIR incident is closed in the ServiceNow AI Platform.

</td></tr><tr><td>

Closure Incident Status Update

</td><td>

Status update in the Cortex XSIAM incident when the security incident is closed in SIR.

</td></tr><tr><td>

Closure Comments Posted back to XSIAM

</td><td>

Comments posted to the incident in the Cortex XSIAM incident when the security incident is closed in SIR.

</td></tr><tr><td>

Priority Mapping

</td><td>

Update Priority

</td><td>

Option to automatically sync ServiceNow incident priority to XSIAM incident severity.When enabled, a change to the incident priority in ServiceNow updates the corresponding Cortex XSIAM incident severity based on your mapping configuration.

</td></tr><tr><td>

Pull Closed Incidents

</td><td>

Pull Closed Incidents

</td><td>

Option to fetch closed incidents during ongoing ingestion and one-time retrieval. Closed SIR incidents will not be updated with new data from XSIAM.

</td></tr><tr><td rowspan="2">

Sync Work Notes to XSIAM

</td><td>

Sync SIR work notes between SIR and XSIAM war room

</td><td>

Option to sync Security Incident work notes to XSIAM incident comments. Work notes added to Security Incidents in ServiceNow® will appear as comments in the corresponding XSIAM incident.

</td></tr><tr><td>

Enable Attachment sync

</td><td>

Option to sync attachments between SIR security incidents and the XSIAM war room. Attachments added on either side sync to the other at the next polling interval.

</td></tr></tbody>
</table>    \[Omitted image "xsiam-additional-options.png"\] Alt text: Automate incident updates and closures

3.  Select a Sample Ingestion Method in the **Field Mapping** section.

<table id="table_w5t_p1r_hkc"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

All default Incident and Alert Fields

</td><td>

Loads the static list of all Incident, and Alert fields. Shows default field names only, with no values.

</td></tr><tr><td>

Security Incident Record Number

</td><td>

Queries a single Security Incident by its record number and populates the mapping section with that record's live field values.Use this to build mappings from a known record.

</td></tr></tbody>
</table>4.  To map a field value from the Incident and Alert Fields section to a field on the XSIAM incident Target Fields section, use one of the following actions:

    1.  Drag the Incident field name \(for example, id\) and drop it next to a field name in the XSIAM incident Target Fields column.

        You can match any value from the Incident and Alert fields section to a field on the XSIAM incident Target Fields section. Fields are color-coded so that you do not overlook or duplicate incident fields in the mapping process. Light blue fields indicate that an incident field is not yet selected and mapped on the security incident. You may prefer to associate an incoming incident fields with more than one field on a security incident. A gray field indicates that a field has been selected and mapped to a field on the security incident.

        This way, you can visualize which field values have been added to the security incident and if any remaining important incident information remains unmapped.

    2.  Add a combination of text and field value.

        For example, `Incident name is ${Incidents: name}$`. Here `Incident name is` can be manually entered while `${Incidents: name}$` is mapped from the Incident and Alert Fields section.

    3.  Manually enter and map a source Incident or Alert field to a target field.

        -   To manually map a source incident field use the $⁠\{field name\}$ format. For example, to map an incident field Severity, the format is `${Incidents: severity}$`.
        -   To manually add Incident and Alert fields, use the `$⁠{Source: field}$` format. For example, `$⁠{Incidents: incident_name}$`.
5.  In the XSIAM Target Fields section, select \[Omitted image "sentinel-map-button.png"\] Alt text: Map another field button. to add fields to the default fields that are displayed on the security incident.

6.  In the XSIAM Target Fields section, select \[Omitted image "sentinel-remove-button.png"\] Alt text: Remove button Remove item to remove a field.

7.  Select the check box for a field to automatically update the respective SIR incident data with changes from XSIAM.

    **Note:** In the base system, the system property sn\_sec\_pan\_xsiam.incident\_updates is by default set to False to receive the XSIAM updates related to new alerts that are linked to SIR.

    -   By default, the Affected Users, Configuration items, and Observables fields are checked. When new observables, configuration items, or affected users get added to the incident, that information is automatically extracted. The data is then populated in the respective related lists in the Security Incident Response \(SIR\) during that polling interval.
    -   For any other fields, select the check box that corresponds to a field. When changes are made in the XSIAM incident record, the respective SIR incident data is automatically replaced with the new incident data.
    **Important:** Due diligence is required to be done before selecting this functionality as overriding the existing data may result in unstable data for the analyst to work with and any other automation that is set even by the field values of security incident may also get affected. So, it is very important to do the due diligence before you select any override functionality.

8.  To format a field translation for a Cortex XSIAM Incident field, select the **Click here** link in the **XSIAM incident Target Fields** header.

9.  To modify the fields which support field translation, select the \[Omitted image "sentinel-field-format-button.png"\] Alt text: Field format button script format field translation icon.

    The fields that support field translation are **Affected user**, **Configuration Item**, and **Priority**. For example, select \[Omitted image "sentinel-field-format-button.png"\] Alt text: Field format button icon next to the Category. The Cortex XSIAM Field Translation script editor opens.

10. Enter any changes to the script and select **Update** to save the changes and return to the Mapping page.

    For example, for Category define the following in the script editor:

    ```
    "<Incoming Cortex XSIAM Field Value>":"<Category to assign to the Security Incident>".
    ```

    This mapping confirms that a profile uses only configured categories.

11. Continue mapping by adding or removing field values.

    You can use the same field values in the Incident Generation Conditions builder to define additional criteria that an incoming Incident must satisfy to create a security incident.

12. Select **Finish**.

13. Activate the profile.

    1.  Select the **Name** section of the progress bar.

    2.  Select the **Active** check box.

    3.  Select **Continue**.


