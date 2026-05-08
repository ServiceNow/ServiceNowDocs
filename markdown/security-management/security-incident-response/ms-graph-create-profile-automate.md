---
title: Automate alert updates and closure based on SIR incident status
description: The Microsoft Graph Security API alert ingestion integration has a bi-directional interface that allows for both alerts to create security incidents, as well as an ability to update the alerts once the security incident is created and/or closed with relevant incident details such as SIR incident number, assignment group, SIR incident URL, and so on. T
locale: en-US
release: australia
product: Security Incident Response
classification: security-incident-response
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 2
breadcrumb: [Create a profile, Microsoft Graph Security API alert ingestion integration, Security Incident Response integrations, Security Incident Response, Enterprise security case management applications, Security Operations]
---

# Automate alert updates and closure based on SIR incident status

The Microsoft Graph Security API alert ingestion integration has a bi-directional interface that allows for both alerts to create security incidents, as well as an ability to update the alerts once the security incident is created and/or closed with relevant incident details such as SIR incident number, assignment group, SIR incident URL, and so on. T

## Before you begin

Role required: sn\_si.admin

**Note:** The initial and closure alert statuses are updated only if this functionality is supported by the service provider. For details, see the Microsoft Graph Security API documentation and the security provider documentation.

## Procedure

1.  If the Additional Options page on the progress bar is not displayed, select **Additional Options**.

2.  Follow the instructions below to complete the configuration for updating alerts when the security incident is created.

<table id="choicetable_bsh_yxn_kjb"><thead><tr><th align="left" id="d427857e84">

Option or Field

</th><th align="left" id="d427857e87">

Description

</th></tr></thead><tbody><tr><td id="d427857e93">

**Update alerts upon SIR Incident Creation**

</td><td>

Select this option if you want to update the alert status and add additional comments when a security incident is created from the alert. This can occur for both the initial triggering alerts that create the security incident, as well as aggregated alerts.

</td></tr><tr><td id="d427857e102">

**Initial Alert Status Update**

</td><td>

Select an initial alert status from the list. This status will be set for all alerts when a security incident is created for an ingested alert. This includes alerts that create new incidents and alerts that are ingested and aggregated to an existing open incident.**Note:** Based on the alert status selected here, the alert status used by the security providers will be correspondingly updated.

</td></tr><tr><td id="d427857e114">

**Initial Comments posted back to Alert**

</td><td>

Based on the stage you have selected, default comments are displayed. You can modify the default text and use the $\{field name\}$ format to add or modify any fields available in the security incident form.

</td></tr><tr><td id="d427857e123">

**Close out alerts upon SIR Incident Closure**

</td><td>

Select this option if you want to use the automated alert closure option. This can occur for both the initial triggering alerts that create the security incident, as well as aggregated alerts. Alert status will be updated in the security provider with the status and closure comments after SIR incident is closed in the ServiceNow AI Platform.

</td></tr><tr><td id="d427857e139">

**Closure Alert Status Update**

</td><td>

Select an alert status from the list. Select the status value to be set for all alerts when a security incident is closed for an ingested alert.

</td></tr><tr><td id="d427857e148">

**Closure Comments Posted back to Alert**

</td><td>

The default closure comments are displayed here. You can edit the default text and use the $\{field name\}$ format to add or modify any fields available in the security incident form.

</td></tr></tbody>
</table>3.  Click **Finish** to complete the configuration and move the profile to the **Waiting** state.

    A confirmation dialog is displayed. You have successfully completed the setup and configuration for the integration. Activate this profile to pull alerts from the Microsoft Azure tenant based on your scheduling. A maximum of 1000 security incidents can be created within a 24 hour period.


