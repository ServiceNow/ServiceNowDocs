---
title: Viewing and resolving ServiceNow IT service requests submitted from EMR systems
description: Work on task records that are automatically created when clinicians submit ServiceNow IT service requests from an EMR system.Work on ServiceNow IT service requests submitted by clinicians using the Incident module.Work on ServiceNow IT service requests submitted by clinicians using the EMR Help module.
locale: en-US
release: australia
product: EMR Help
classification: emr-help
topic_type: concept
last_updated: "2026-03-12"
reading_time_minutes: 3
breadcrumb: [Resolve EMR Help requests, EMR Help, Healthcare and Life Sciences Service Management, Healthcare and Life Sciences]
---

# Viewing and resolving ServiceNow IT service requests submitted from EMR systems

Work on task records that are automatically created when clinicians submit ServiceNow IT service requests from an EMR system.

Ensure that an administrator has added the EMR Incident Data related list to the Incident form. For more information, see Configuring the form layout.

Incidents are the task type configured by default with the EMR Help application.

You can use the EMR Help module or the Incident module to access incidents submitted from an EMR system.

-   To use the incident module, see [View and resolve an EMR incident from the Incident module](emr-help-issues-resolve.md#).
-   To use the EMR Help module, see [View and resolve an EMR incident from the EMR Help module](emr-help-issues-resolve.md#).

## View and resolve an EMR incident from the Incident module

Work on ServiceNow IT service requests submitted by clinicians using the Incident module.

### Before you begin

Role required: itil and sn\_ind\_rmt\_help.viewer

### Procedure

1.  Navigate to **All** &gt; **Incident** &gt; **Open**.

2.  On the Incidents list, search for the EMR incident that you want to work on.

3.  In the **Number** column, click the link to the EMR Incident.

4.  In the EMR Incident Data related list of the incident form, view the information from the EMR system.

    **Note:** Your administrator might need to configure the form to add the EMR Incident Data related list. You can view data in this related list only when you have the sn\_ind\_rmt\_help.viewer role in addition to the itil role. If you do not have the required roles, the EMR Incident Data related list appears empty.

5.  Resolve and close the incident.

    1.  Select the **Resolution Information** tab.

    2.  On the form, fill in the fields.

<table id="table_fyg_c1z_tnb"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Knowledge

</td><td>

Option for generating a knowledge article with the information from the incident.

</td></tr><tr><td>

Resolved by

</td><td>

User who resolved the issue and the date and time the incident was closed.

</td></tr><tr><td>

Resolved

</td><td>

Date and time when the incident was resolved.

</td></tr><tr><td>

Resolution code

</td><td>

Information to categorize resolved cases.

</td></tr><tr><td>

Resolution notes

</td><td>

Notes on how an incident was resolved.

</td></tr></tbody>
</table>    3.  Click **Resolve**.

    4.  Close the incident by clicking **Close Incident**.


## View and resolve an EMR incident from the EMR Help module

Work on ServiceNow IT service requests submitted by clinicians using the EMR Help module.

### Before you begin

Role required: itil and sn\_ind\_rmt\_help.viewer

### Procedure

1.  Navigate to **All** &gt; **EMR Help** &gt; **EMR Incidents** &gt; **My Open**.

2.  On the EMR Incidents list, search for the EMR incident that you want to work on.

3.  In the **Number** column, click the link to the EMR Incident.

4.  In the EMR Incident Data related list of the incident form, view the information from the EMR system.

    **Note:** Your administrator might need to configure the form to add the EMR Incident Data related list. You can view data in this related list only when you have the sn\_ind\_rmt\_help.viewer role in addition to the itil role. Else, the EMR Incident Data related list appears empty.

5.  Resolve and close the incident.

    1.  Select the Resolution Information tab.

    2.  On the form, fill in the fields.

<table id="table_fyg_c1z_tnb"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Knowledge

</td><td>

Option for generating a knowledge article with the information from the incident.

</td></tr><tr><td>

Resolved by

</td><td>

User who resolved the issue and the date and time the incident was closed.

</td></tr><tr><td>

Resolved

</td><td>

Date and time when the incident was resolved.

</td></tr><tr><td>

Resolution code

</td><td>

Information to categorize resolved cases.

</td></tr><tr><td>

Resolution notes

</td><td>

Notes on how an incident was resolved.

</td></tr></tbody>
</table>    3.  Click **Resolve**.

    4.  Close the incident by clicking **Close Incident**.


