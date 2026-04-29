---
title: Create an Enterprise Asset Management incident
description: Create an incident record to document a deviation from an expected Enterprise Asset Management standard of operation.
locale: en-US
release: australia
product: Enterprise Asset Management
classification: enterprise-asset-management
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 2
breadcrumb: [Managing incidents in Enterprise Asset Management, Managing enterprise models and assets, Enterprise Asset Management, IT Asset Management]
---

# Create an Enterprise Asset Management incident

Create an incident record to document a deviation from an expected Enterprise Asset Management standard of operation.

## Before you begin

Role required: itil

To create an Enterprise Asset Management incident record, you must install all applicable Incident Management plugins on your ServiceNow instance. See [Incident Management plugins](https://www.servicenow.com/docs/access?context=incident-mgmt-plugins&version=australia&pubname=australia-it-service-management&ft:locale=en-US) for the complete list of Incident Management plugins.

## About this task

This procedure describes how an ITIL agent must complete an incident form to document and track an Enterprise Asset Management incident. Refer to [Incident Management](https://www.servicenow.com/docs/access?context=c_IncidentManagement&version=australia&pubname=australia-it-service-management&ft:locale=en-US) for more in-depth information on creating and managing incidents.

## Procedure

1.  [Create an incident](https://www.servicenow.com/docs/access?context=create-an-incident&version=australia&pubname=australia-it-service-management&ft:locale=en-US).

    After your incident is created, you are automatically redirected to the Incidents list.

2.  From the list of available incidents, select the incident that you created in the previous step.

3.  On the form header of your incident record, select the Additional actions menu icon \(![Additional actions menu icon.](../image/additional-actions-icon.png)\) and then select **View** &gt; **Enterprise Asset**.

    This option sets your incident record to the Enterprise Asset Management incident form view, which contains additional fields that are specific to Enterprise Asset Management.

4.  After the form reloads in the Enterprise Asset Management incident form view, specify the asset that is affected by this incident.

    1.  Select the Lookup using list icon ![](../../software-asset-management2/image/search-icon.png) in the **Asset** field.

    2.  In the Assets pop-up window, search for and select the asset that is affected by this incident.

        The pop-up window closes and you automatically return to the Incident form.

    3.  On the form header, select the Additional actions menu icon ![](../image/additional-actions-icon.png) and then select **Save**.

    When the form reloads, the **Configuration item** field and **Affected Assets** related list update automatically based on the asset that you selected.

    **Note:** The **Configuration item** field remains empty if you select a consumable asset.

    **Important:** If you select a multi-component asset, the **Affected Assets** related list displays only the parent asset. You must manually add each child asset that is affected by this incident. See [step 5](create-eam-incident.md#add-child-assets) for more details.

5.  If you selected a multi-component asset in the previous step, specify the child assets that are affected by this incident.

    1.  On the **Affected Assets** related list, select **Edit**.

    2.  In the Collection list on the Edit Members form, search for and select a child asset that is affected by this incident.

        **Note:** By default, the Edit Members form automatically runs a search filter to display only the relevant child assets in the Collection list.

    3.  Select the Add icon ![](../../software-asset-management2/image/add-icon.png) to move the selected child asset to the Affected Assets List.

    4.  Repeat steps b and c for each child asset that is affected by this incident.

    5.  Select **Save**.

    6.  After you return to the Incident form, select **Update**.


## What to do next

Resolve and close your incident.

**Parent Topic:**[Managing incidents in Enterprise Asset Management](../concept/managing-eam-incidents.md)

