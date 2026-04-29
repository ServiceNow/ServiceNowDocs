---
title: Troubleshooting IBM QRadar offense ingestion integration
description: This section covers important troubleshooting tips and frequently asked questions related to IBM QRadar offense ingestion.
locale: en-US
release: australia
product: Security Incident Response
classification: security-incident-response
topic_type: concept
last_updated: "2026-03-12"
reading_time_minutes: 3
breadcrumb: [IBM QRadar Offense Ingestion Integration, Security Incident Response integrations, Security Incident Response, Enterprise security case management applications, Security Operations]
---

# Troubleshooting IBM QRadar offense ingestion integration

This section covers important troubleshooting tips and frequently asked questions related to IBM QRadar offense ingestion.

-   Integration run: When a scheduled job starts executing, an integration run record with logs, errors, and warnings is displayed. The number of offenses pulled and the number of incidents created in a scheduled job run are also displayed. Users with the sn\_si.analyst role can see if any errors/profiles pulling failed during the integration run.

    Worknotes in the integration run provide links to the executed subflows. Users with the sn\_si.analyst role can check the `sn_event_ingestion_integration_run` table for any errors that have occurred. To troubleshoot any integration issues, you must first check the integration run. Errors are logged as worknotes in the integration run records for every scheduled job run.

    ![IBM QRadar integration run](../image/ibm-qradar-trouble-intrun.png)

-   SSL issues: When connecting to IBM QRadar cloud instances, ensure that the instance has a valid CA certificate which has not expired. You can import RSA or your own certificates into the platform and ensure that the common name of the certificate matches host name. See [https://support.servicenow.com/nav\_to.do?uri=%2Fkb\_view.do%3Fsys\_kb\_id%3D55ecefd61bf3774cada243f6fe4bcb44](https://support.servicenow.com/nav_to.do?uri=%2Fkb_view.do%3Fsys_kb_id%3D55ecefd61bf3774cada243f6fe4bcb44) for details.
-   Incomplete profile: While configuring the profile, in the Additional Options \([Automate offense updates and closure based on SIR incident status](../task/qradar-ibm-create-profile-additional.md)\) section, you must click the **Finish** button to ensure that the profile is moved to Waiting state indicating that it is waiting for ingestion.
-   Validate profile: To validate if the integration is working correctly, check the profile states, last pulled date of profile, offense import table, offense to task table records.
-   MID server configuration: If you are installing the IBM QRadar application on-premise, after configuring the MID server, you must create a MID server application. The MID server application name should be used in integration configurations tile instead of the MID server name.

    **Note:** The default MID serve timeout is 30 seconds. To see instructions on disabling the timeout period, see &lt;link&gt;. Note that this is a system-wide change and may impact other integrations.

-   Offense Updates: If you have enabled the `sn_sec_qradar.get_offense_updates` property and you notice a delay in the creation of security incidents, then disable the property. Do not enable this property when the polling interval is low and the offenses load on QRadar is high as this increases the queue load.
-   Missing event, flow data, remote\_ip, or users data in a security incident: If you observe that event, flow data, remote\_ip, or users data is missing in a security incident, then increase the timeout \(seconds\) for `sn_sec_qradar.sid_ttl` parameter. Increasing the duration delays the creation of the security incident until the AQLs complete parsing each offense.
-   Timeouts: If you view timeout errors in the application logs, review and modify the following flow designer actions:

<table id="table_pbg_yvf_qnb"><thead><tr><th>

Parameters

</th><th>

Action

</th></tr></thead><tbody><tr><td>

**Fetch Sample Offenses**

 `var flow_outputs = sn_fd.FlowAPI.executeAction('sn_sec_qradar.fire_rest_for_offenses', flow_inputs, 60000);`

</td><td>

Review and update the duration in milliseconds.

</td></tr><tr><td>

**Fetch Sample Offenses**

 `var flow_outputs = sn_fd.FlowAPI.executeAction('sn_sec_qradar.fire_rest_for_offenses', flow_inputs);`

</td><td>

Add a parameter for the `executeAction` and enter the duration in milliseconds.

</td></tr><tr><td>

**Fetch Offenses for profile and queue records in polling table**

 `var flow_outputs = sn_fd.FlowAPI.executeAction('sn_sec_qradar.fire_rest_for_offenses', flow_inputs, 180000);`

</td><td>

Review and update the duration in milliseconds.

</td></tr><tr><td>

**Wrapper for testing connection REST**

 `var rest_outputs = sn_fd.FlowAPI.executeAction('sn_sec_qradar.test_connection_rest', rest_inputs);`

</td><td>

Add a parameter for the `executeAction` and enter the duration in milliseconds.

</td></tr><tr><td>

**Wrapper for validating API credentials REST**

 `var rest_outputs = sn_fd.FlowAPI.executeAction('sn_sec_qradar.validate_credentials_rest', rest_inputs);`

</td><td>

Add a parameter for the `executeAction` and enter the duration in milliseconds.

</td></tr><tr><td>

**REST step for IBM QRadar Offense updates**

 `var result = sn_fd.FlowAPI.executeAction('sn_sec_qradar.'+restStep, inputs,60000);`

</td><td>

Review and update the duration in milliseconds.

</td></tr></tbody>
</table>
