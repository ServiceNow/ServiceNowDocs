---
title: Automate incident updates and closures
description: Automate incident updates and closures based on the incident status. The Cortex XSIAM integration enables incidents to create security incidents and also to update the incidents after they are created or closed.
locale: en-US
release: australia
product: Security Incident Response
classification: security-incident-response
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 2
breadcrumb: [Security Incident Response Integration with Cortex XSIAM by Palo Alto Networks, Security Incident Response integrations, Security Incident Response, Enterprise security case management applications, Security Operations]
---

# Automate incident updates and closures

Automate incident updates and closures based on the incident status. The Cortex XSIAM integration enables incidents to create security incidents and also to update the incidents after they are created or closed.

## Before you begin

Role required: sn\_si.admin, sn\_si.ingestion\_profile\_admin

## Procedure

1.  If you are not continuing from the previous section of the Scheduling process, access the profile you are defining.

    1.  Navigate to **All** &gt; **Palo Alto Networks XSIAM** &gt; **XSIAM Profile**.

    2.  Select the profile you are continuing to define.

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

Option to sync ServiceNow Incident priority to XSIAM Incident severity.When enabled, changes to incident priority in ServiceNow will update the corresponding XSIAM incident severity based on your mapping configuration.

For example, ServiceNow Priority "1 - Critical" maps to XSIAM Severity "Critical".

</td></tr><tr><td>

Pull Closed Incidents

</td><td>

Pull Closed Incidents

</td><td>

Option to fetch closed incidents during ongoing ingestion and one-time retrieval. Closed SIR incidents will not be updated with new data from XSIAM.

</td></tr><tr><td>

Sync Work Notes to XSIAM

</td><td>

Sync SIR work notes to XSIAM

</td><td>

Option to sync Security Incident work notes to XSIAM incident comments. Work notes added to Security Incidents in ServiceNow® will appear as comments in the corresponding XSIAM incident.

</td></tr></tbody>
</table>    ![Automate incident updates and closures](../image/xsiam-additional-options.png)

3.  Select **Finish**.

4.  Activate the profile.

    1.  Select the **Name** section of the progress bar.

    2.  Select the **Active** check box.

    3.  Select **Continue**.


