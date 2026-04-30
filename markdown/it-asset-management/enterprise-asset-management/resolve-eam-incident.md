---
title: Resolve and close an Enterprise Asset Management incident
description: Take action on the assets that are affected by an Enterprise Asset Management incident so that you can resolve and close the incident.
locale: en-US
release: zurich
product: Enterprise Asset Management
classification: enterprise-asset-management
topic_type: task
last_updated: "2025-07-31"
reading_time_minutes: 2
breadcrumb: [Managing incidents in Enterprise Asset Management, Manage enterprise models and assets, Enterprise Asset Management, IT Asset Management]
---

# Resolve and close an Enterprise Asset Management incident

Take action on the assets that are affected by an Enterprise Asset Management incident so that you can resolve and close the incident.

## Before you begin

Role required: itil

## Procedure

1.  Navigate to **All** &gt; **Incident** &gt; **All**.

2.  From the list of available incidents, select the Enterprise Asset Management incident that you want to resolve and close.

3.  Specify what actions you want to take on the assets that are affected by the incident.

    1.  On the Incident form, select the **Affected Assets** related list.

    2.  From the list of affected assets, double-click the **Asset action** field for the asset that you want to take action on.

    3.  When prompted, select the action that you want to take on the asset.

    4.  Select the Save icon ![](../../software-asset-management2/image/save-icon.png).

    5.  If you choose to swap the asset, specify the asset that you are swapping the existing asset with.

        1.  Double-click the corresponding **Swapped Asset** field.
        2.  When prompted, select the Lookup using list icon ![](../../software-asset-management2/image/search-icon.png) to search for and select the asset that you want to swap the existing asset with.
        3.  Select the Save icon ![](../../software-asset-management2/image/save-icon.png).
    6.  If you are taking action on a consumable asset, specify the number of available assets that you want to take action on.

        You can take action on all available assets or only a portion of the available assets.

        1.  Double-click the corresponding **Consumable Quantity** field.
        2.  When prompted, enter the number of available assets that you want to take action on.
        3.  Select the Save icon \(![Save icon.](../../software-asset-management2/image/save-icon.png)\).
        **Important:** The **Consumable Quantity** field does not display the updated value automatically. To view the updated value, **Refresh** the **Affected Assets** related list.

4.  Based on the actions that you specified in the previous step, update/repair, swap, retire, or take no action on the affected assets.

5.  After you have completed taking all necessary actions on the affected assets, provide details about how the incident has been resolved.

    1.  Return to your Incident form.

    2.  On the **Resolution Information** tab, fill in the fields.

        |Field|Description|
        |-----|-----------|
        |Knowledge|Option to automatically create a knowledge article upon incident closure.|
        |Resolution code|Resolution category that specifies how the incident was resolved.|
        |Resolution notes|Description of how the incident was resolved.|
        |Resolved by|User who resolved the incident.|
        |Resolved|Date and time at which the incident was resolved.|

6.  On the form header, select **Resolve**.

    The incident is moved to the Resolved state, and you are automatically redirected to the Incidents list. If the asset has any child assets and was in a retired status as indicated in the **Asset action** box, the child assets will be released depending on the kind of asset.

    |Type of asset|Action|
    |-------------|------|
    |Simple|No action|
    |Simple with add-on|All child assets are released to the pending disposal state.|
    |User-assembled|All child assets are released to the pending disposal state.|
    |User-assembled with add-on|All child assets are released to the pending disposal state.|
    |Pre-assembled|No action|
    |Pre-assembled with add-on|All add-on assets are released to the pending disposal state.|

    The incident is moved to the Resolved state, and you are automatically redirected to the Incidents list.

7.  From the list of available incidents, select the incident that you just resolved.

8.  On the form header, select **Close Incident**.

    The incident is closed.


**Parent Topic:**[Managing incidents in Enterprise Asset Management](../concept/managing-eam-incidents.md)

