---
title: Additional options: Automate correlated event updates and closure based on SIR incident status
description: The ArcSight ESM integration has a bi-directional interface that allows for both correlation events to create security incidents, as well as an ability to update the correlation events once the security incident is created and/or closed with relevant incident details such as security incident number, assignment group, SIR incident URL, and so on.
locale: en-US
release: zurich
product: Security Incident Response
classification: security-incident-response
topic_type: task
last_updated: "2025-07-31"
reading_time_minutes: 4
breadcrumb: [Use, Set up instance, ArcSight ESM Event Ingestion integration, Security Incident Response integrations, Security Incident Response, Enterprise security case management applications, Security Operations]
---

# Additional options: Automate correlated event updates and closure based on SIR incident status

The ArcSight ESM integration has a bi-directional interface that allows for both correlation events to create security incidents, as well as an ability to update the correlation events once the security incident is created and/or closed with relevant incident details such as security incident number, assignment group, SIR incident URL, and so on.

## Before you begin

Role required: sn\_si.admin

## Procedure

1.  If the Additional Options page on the progress bar is not displayed, select **Additional Options**.

2.  Follow the instructions below to complete the configuration for updating correlated events when the security incident is created.

<table id="choicetable_bsh_yxn_kjb"><thead><tr><th align="left" id="d123707e77">

Option or Field

</th><th align="left" id="d123707e80">

Description

</th></tr></thead><tbody><tr><td id="d123707e86">

**Update Correlated Events upon SIR Incident Creation**

</td><td>

Select this option if you want to update the correlation event stage in ArcSight ESM and update the event with additional comments when a security incident is created from the correlation event. This can occur for correlation events that could either create a new security incident, as well as aggregate existing security incidents. **Note:** If this option is not selected, the event stage will not be updated when the security incident is created.

</td></tr><tr><td id="d123707e101">

**Correlated Event Stage Update**

</td><td>

Select a stage option from the Correlated Event Stage Update choice list that displays all available stages retrieved from the ArcSight ESM server.

</td></tr></tbody>
</table>    **Correlated event stage not configured**: If you have not configured any correlated event stages in your ServiceNow AI Platform instance, you will only see the **Assign Stage - Initial Setup** in the Correlated Event Stage Update choice list. To configure the stage, follow these steps:

    -   Enter a resource ID in the Enter Stage Resource ID field and click **Submit**. The resource ID is validated in the ArcSight ESM console and the following screen is displayed.

        ![ArcSight ESM: Stage Resource ID](../image/sir-arcsight-esm-profile-additional-stage.png)

    -   Click **Save** to save the new stage \(**Monitoring**\).
    -   Click the Select Correlated Event Stage drop down list.

        ![ArcSight ESM: Event Stage List](../image/sir-arcsight-esm-profile-additional-stage-list.png)

    -   You can select the newly created stage from the list.
    **Correlated event stage already configured**: If you have already configured the correlated event stage, follow these steps:

    -   Select **Use Previously Assigned Stage** in the Correlated Event Stage Update choice list.
    -   Select an existing stage from the Select Correlated Event Stage choice list as shown below.

        ![ArcSight ESM: Previously Assigned Stage](../image/sir-arcsight-esm-profile-additional-stage-2.png)

    -   Initial Comments posted back to Correlated Event: In addition to updating the correlation event stage value, you can also post comments to the correlation stage annotations. As indicated in the instructions, you may edit the default text displayed in the comments section including adding or modifying the substitution variables using format $⁠\{field name\}$ for any field on the Security Incident Response incident form.
    **Note:** You can either use the default stages defined in the ArcSight ESM console or create your own custom stages. To create a new stage, follow these steps:

    -   In the ArcSight ESM console, select **File** &gt; **New** &gt; **Stage**. The Inspect/Edit tab is displayed.
    -   Define the new stage and do not select the **User Required** check box. Ensure that the stage is defined correctly and is in the correct position in the event life cycle.
3.  In the Automating Correlated Event Closure section, you can define how to update the security incident when it is closed.

4.  On the form, fill in the fields.

<table id="choicetable_ybx_hds_nkb"><thead><tr><th align="left" id="d123707e234">

Option or Field

</th><th align="left" id="d123707e237">

Description

</th></tr></thead><tbody><tr><td id="d123707e243">

**Update Correlated Events upon SIR Incident Closure**

</td><td>

Select this option if you want to update the correlation event status and add additional comments when a security incident is closed from the correlated event. This will occur for both the initial triggering notable events that create the security incident, as well as aggregated events.**Note:** If this option is not selected, the event stage will not be updated when the security incident is closed.

</td></tr><tr><td id="d123707e255">

**Correlated Event Stage Update**

</td><td>

Select a stage option from the menu that displays all available stages retrieved from the ArcSight ESM server. Select the stage value to be set for all correlation events when a security incident is to be closed. **Note:** The stages displayed here are based on the stages configured in the Correlation Event Initial Updates section.

</td></tr><tr><td id="d123707e270">

**Select Correlated Event Stage**

</td><td>

Select an appropriate status here.

</td></tr><tr><td id="d123707e279">

**Closure Comments Posted back to Correlated Event**

</td><td>

In addition to updating the correlation event status value, you can also post closure comments to the correlation event annotations. As indicated in the instructions, you may edit the default text displayed in the comments section including adding or modifying the substitution variables using format $⁠\{field name\}$ for any field on the Security Incident Response incident form.

</td></tr></tbody>
</table>    ![ArcSight ESM: Closure Event Stage](../image/sir-arcsight-esm-profile-additional-stage-3.png)

5.  Click **Finish** to complete the configuration.

    A confirmation dialog is displayed. You have successfully completed the setup and configuration for the integration. Activate this profile to pull correlation events from the ArcSight ESM console based on your scheduling.


