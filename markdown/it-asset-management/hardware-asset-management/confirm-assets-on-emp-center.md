---
title: Confirm the assigned assets on the Employee Center portal
description: As an employee, acknowledge or deny the ownership of the serialized hardware assets assigned to you on the Employee Center portal.
locale: en-US
release: australia
product: Hardware Asset Management
classification: hardware-asset-management
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 2
breadcrumb: [Confirming the assigned serialized hardware assets, Audit your hardware assets by using Asset Attestation, Using Hardware Asset Management, Hardware Asset Management, IT Asset Management]
---

# Confirm the assigned assets on the Employee Center portal

As an employee, acknowledge or deny the ownership of the serialized hardware assets assigned to you on the Employee Center portal.

## Before you begin

Role required: Log in as an employee.

To view the **My Assets** option on the global header navigation bar of the Employee Center portal, the value of the **enable\_assets** option must be set to **true** on the Additional options, JSON format field of the Employee Center menu record. For more details, see Enable or disable global header options.

**Note:** The **My Assets** option requires the Hardware Asset Management application to be activated.

## Procedure

1.  View the assets that are assigned to you on the Employee Center portal.

    -   Select the **Confirm assets** link in the email notification that you received.

        The link opens the **My Assets** page on the Employee Center portal.

    -   Select **My Assets** in the global header navigation bar of the Employee Center portal.

        **Note:** The number displayed on the **My Assets** option indicates the number of assets that you must confirm.

    -   View the list of assets from the Employee Profile.
        1.  Select **Profile** on the global header navigation bar of the Employee Center portal.
        2.  Select the **Assets** tab.
    The page displays all the hardware and consumable assets assigned to you. However, you can only confirm serialized hardware assets that are opted-in.

2.  For the hardware asset that you want to confirm, select **Confirm asset**.

    You can view the following details of the asset:

    -   Display name
    -   Asset tag
    -   Serial number
    -   Asset function
    **Note:** Any field that's empty isn't shown on the Confirm asset page.

3.  Acknowledge or deny the ownership of the asset by selecting your response to the question **Do you have this asset?**.

    -   To confirm that you have the asset, select **Yes**.
    -   To confirm that you don't have the asset, select **No**.
4.  Select **Submit**.


## Result

-   The **Confirm asset** option is no longer displayed for the asset.
-   The **Attestation date** field of the asset on the asset attestation form is updated with the actual date on which you confirmed the asset.
-   The **State** field of the asset attestation changes from In progress to Closed complete only when that attestation has no other users and assets involved.
-   The **Status** field of the asset on the asset attestation form is updated based on your confirmation:
    -   If you selected **Yes**, the **Status** field changes from **Open** to **Yes**.
    -   If you selected **No**, the **Status** field changes from **Open** to **No**. Also, a remediation task is created for that attestation. The administrator can work on that task and initiate an investigation to find the asset status.

**Parent Topic:**[Confirming the assigned serialized hardware assets](../concept/confirming-assets-emp-portal-mobile.md)

**Related topics**  


[bundle-emplsm.employee-center-landing-page]

