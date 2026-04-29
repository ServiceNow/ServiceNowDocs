---
title: TISC playbook templates
description: This section describes the playbook templates that are shipped with TISC Sentinel solution.
locale: en-US
release: australia
product: Threat Intelligence Security Center
classification: threat-intelligence-security-center
topic_type: concept
last_updated: "2026-03-12"
reading_time_minutes: 3
breadcrumb: [Microsoft Sentinel integration, TISC Security Tools integrations, TISC Integrations, Integrate, Threat Intelligence Security Center, Security Operations]
---

# TISC playbook templates

This section describes the playbook templates that are shipped with TISC Sentinel solution.

|Use case|Playbook|Description|
|--------|--------|-----------|
|Importing Observables from TISC to Sentinel|Batch\_Indicator\_Uploader|Provides batching mechanism for exporting observables from TISC using Upload Indicators API provided by Microsoft Sentinel.|
|Import\_Observables\_Batch|Enables scheduled export of observables from TISC.|
|Export entities from Sentinel to TISC|Export\_Incident\_Entities|Export all entities of a Sentinel incident.|
|Export\_Hash\_Entity|Export file hash entities of Sentinel incident.|
|Export\_Domain\_Entity entities|Export domain entities of Sentinel incident.|
|Export\_IP\_Entity|Export IP entities of Sentinel incident.|
|Export\_URL\_Entity|Export URL entities of Sentinel incident.|
|Enrich Sentinel incidents|Incident\_Enrichment|Enables enrichment of Sentinel incidents by fetching details related to entities associated with it and posting information in the form of comments on the incident.|

**Note:** All the playbooks use TISC Custom Connector internally to use TISC APIs.

## Create playbooks from templates

1.  Navigate to T**ISC Solution** content page from the **Content Hub in Sentinel Workspace**.
2.  For each playbook shown in the contents page, do the following:
    1.  Select the playbook template, a context pane is displayed in the right hand side of the screen, click **Configuration**.
    2.  Read the description of the playbook template, go through the **Prerequisites** and **Post deployment** steps mentioned in the description.
    3.  Click on **Deploy custom connector** \(if you haven't already deployed the custom connector\).

        Add the **ServiceNow instance URL** on the **Deployment Configuration** page.

    4.  Click **Create Playbook**, you would be taken to the deployment configuration screen
    5.  In the Create playbook configuration screen:
        -   Select the appropriate resource group.
        -   Modify the playbook name, or use the default name.
        -   Provide the **Custom Connector nam**e \(make sure this matches with name of the connector you deployed in previous step\) in the Parameters section.
        -   Click **Review and Create**.

## Configure Import\_Observables\_Batch playbook

Make sure to create Batch\_Indicator\_Uploader playbook before the Import\_Observables\_Batch playbook is created.

1.  Navigate to **Logic App Designer** to edit the playbook.
2.  Update the Recurrence time \(in hours\) as required.
3.  From the TISC Custom Connector component within the playbook, update the parameters that are sent to TISC API.

<table id="table_hn3_3ww_c2c"><thead><tr><th>

Parameter Name

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Observable Type

</td><td>

Following are the supported types, select one or more:-   IP
-   File Hash
-   Domain
-   URL


</td></tr><tr><td>

Threat Score

</td><td>

Enter the threat score for observables. The threat score value MUST be a number in the range of 0-100.

</td></tr><tr><td>

Confidence

</td><td>

Enter the confidence for observables.The confidence value MUST be a number in the range of 0-100.

</td></tr><tr><td>

Reputation

</td><td>

Following are the supported values, select one or more:-   Clean
-   Malicious
-   Suspicious
-   Unknown


</td></tr><tr><td>

Threat Severity

</td><td>

Following are the supported severity levels, select one or more:-   Critical
-   High
-   Medium
-   Low


</td></tr><tr><td>

Threat Level

</td><td>

Following are the supported threat levels, select one or more:-   High
-   Medium
-   Low


</td></tr><tr><td>

Last Updated Delta in Hours

</td><td>

The last updated time\(in hours\) for observables.

</td></tr></tbody>
</table>
## Configure Export\_Incident\_Entities playbook

This playbook uses TISC Add observables API. Using the Logic App Designer, you can edit the parameters that are sent to the API from the playbook. For more information see [TISC API - POST /sn\_sec\_tisc/threat\_intel\_data/add\_observables](https://www.servicenow.com/docs/bundle/xanadu-api-reference/page/integrate/inbound-rest/concept/tisc-api.html#title_tisc-POST-add-observables).

You can follow the same procedure for all the below listed playbooks which export different types of entities:

-   Export\_Hash\_Entity
-   Export\_Domain\_Entity
-   Export\_IP\_Entity
-   Export\_URL\_Entity

## Configure Incident\_Enrichment playbook

This playbook uses TISC Observables API. Using the Logic App Designer, you can edit the parameters that are sent to the API from the playbook. For more information see [TISC API - POST /sn\_sec\_tisc/threat\_intel\_data/observables](https://www.servicenow.com/docs/bundle/xanadu-api-reference/page/integrate/inbound-rest/concept/tisc-api.html#title_tisc-POST-observables).

## Run playbooks

The following table describes how you can run the following playbooks.

|Playbook|Action|
|--------|------|
|Import\_Observables\_Batch|This playbook runs automatically based on the scheduled time which is mentioned in the recurrence trigger.|
|Export\_Incident\_Entities|On a Sentinel incident, select **Incident Actions** &gt; **Run Playbook** for execution.|
|Export\_Hash\_Entity|On a Sentinel incident, select **File hash entity** &gt; **Run Playbook** for execution.|
|Export\_Domain\_Entity|On a Sentinel incident, select **Domain entity** &gt; **Run Playbook** for execution.|
|Export\_IP\_Entity|On a Sentinel incident, select **IP entity** &gt; **Run Playbook** for execution.|
|Export\_URL\_Entity|On a Sentinel incident, select **URL entity** &gt; **Run Playbook** for execution.|
|Incident\_Enrichment|On a Sentinel incident, select **Incident Actions** &gt; **Run Playbook** for execution.|

**Parent Topic:**[Microsoft Sentinel integration](tisc-sentinel-integration.md)

