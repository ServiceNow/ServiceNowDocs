---
title: Automate offense updates and closure based on SIR incident status
description: The IBM QRadar integration has a bi-directional interface that allows for both offenses to create security incidents, as well as an ability to update the offenses once the security incident is created and/or closed with relevant incident details such as security incident number, assignment group, security incident URL, and so on.
locale: en-US
release: australia
product: Security Incident Response
classification: security-incident-response
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 2
breadcrumb: [Setup IBM QRadar profile, Set up instance, IBM QRadar Offense Ingestion Integration, Security Incident Response integrations, Security Incident Response, Enterprise security case management applications, Security Operations]
---

# Automate offense updates and closure based on SIR incident status

The IBM QRadar integration has a bi-directional interface that allows for both offenses to create security incidents, as well as an ability to update the offenses once the security incident is created and/or closed with relevant incident details such as security incident number, assignment group, security incident URL, and so on.

## Before you begin

Role required: sn\_si.admin

## Procedure

1.  If the Additional Options page on the progress bar is not displayed, select **Additional Options**.

2.  Follow the instructions below to complete the configuration for updating offenses when the security incident is created.

<table id="choicetable_bsh_yxn_kjb"><thead><tr><th align="left" id="d255493e72">

Option or Field

</th><th align="left" id="d255493e75">

Description

</th></tr></thead><tbody><tr><td id="d255493e81">

**Update Offenses upon SIR Incident Creation**

</td><td>

Select this option if you want to update the offense status and add additional comments when a security incident is created from the offense. This can occur for both the initial triggering offenses that create the security incident, as well as aggregated offenses.

</td></tr><tr><td id="d255493e90">

**Initial Offense Status Update**

</td><td>

You can select:-   Open: The status of the offense is set to **Open** and a comment is added indicating that a security incident has been created for the offense.
-   Hidden: The status of the offense is set to **Hidden** and this offense is hidden in the IBM QRadar dashboard.


</td></tr><tr><td id="d255493e117">

**Initial Comments posted back to Offense**

</td><td>

Based on the stage you have selected, the initial comments as defined in the IBM QRadar console are displayed here.

</td></tr><tr><td id="d255493e129">

**Pull Closed Offenses**

</td><td>

Select this option if you want the integration to fetch **Closed** offenses from IBM QRadar.These offenses will be evaluated for security incident creation, correlation, and historical visibility in ServiceNow®.

By default, closed offenses are ignored and open offenses are retrieved from IBM QRadar during polling.

</td></tr><tr><td id="d255493e156">

**Close out offenses upon SIR Incident Closure**

</td><td>

Select this option if you want to use the automated offense closure option. When the security incident is closed in ServiceNow with a relevant close code, the offense status is updated in IBM QRadar to **Closed** with closure comments. **Note:** The close code specified for the security incident must correspond to the closing reason specified in the IBM QRadar dashboard. The offense is closed in IBM QRadar only if a corresponding closing reason is found. If a corresponding reason is not found, the offense is closed with a default close code.

</td></tr><tr><td id="d255493e183">

**Closure Comments Posted back to Offense**

</td><td>

The closure comments as defined in the IBM QRadar dashboard are displayed here.

</td></tr><tr><td id="d255493e195">

**Default closing reason when security incident closes**

</td><td>

The default reason to be used when a security incident is closed, When a security incident is closed, a close code \(or the reason for closing\) is specified in the security incident record, If the close code does not match the closing reason specified in the IBM QRadar dashboard, and you try to close the security incident, an error message is displayed. In such cases, the default closing reason specified here is used when the security incident is closed.

</td></tr></tbody>
</table>    ![IBM QRadar: Create Profile: Automate Offense](../image/ibm-qradar-profile-auto.png)

3.  Select **Finish** to complete the configuration and move the profile to the **Waiting** state.

    A confirmation dialog is displayed. You have successfully completed the setup and configuration for the integration. Activate this profile to pull offenses from the IBM QRadar console based on your scheduling.


