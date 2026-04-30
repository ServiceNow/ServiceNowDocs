---
title: Confirm the assigned assets using the Now Mobile app
description: As an employee, acknowledge or deny the ownership of the serialized hardware assets assigned to you using the Now Mobile app.
locale: en-US
release: yokohama
product: Hardware Asset Management
classification: hardware-asset-management
topic_type: task
last_updated: "2025-06-17"
reading_time_minutes: 1
breadcrumb: [Confirming the assigned serialized hardware assets, Audit your hardware assets by using Asset Attestation, Using Hardware Asset Management, Hardware Asset Management, IT Asset Management]
---

# Confirm the assigned assets using the Now Mobile app

As an employee, acknowledge or deny the ownership of the serialized hardware assets assigned to you using the Now Mobile app.

## Before you begin

Role required: Log in as an employee.

## Procedure

1.  From your mobile device, launch the Now Mobile app.

2.  On the home screen of the Now Mobile app, tap **My assets** from the My items list.

    The list of all assets assigned to you, as well as those assets that need your confirmation, is displayed.

    **Note:** The **Confirm asset** indicator on any asset in the list indicates that you should acknowledge whether you have that asset or not.

3.  Tap the asset with the **Confirm asset** indicator.

    The following asset details are displayed:

    -   **Asset tag**
    -   **Serial number**
    -   **Display name**
4.  Verify the asset details and tap **Confirm asset**.

5.  Acknowledge or deny the ownership of the asset by selecting your response in the **Verify asset** dialog box.

    -   To confirm that you have the asset, tap **Yes**.
    -   To confirm that you don't have the asset, tap **No**.

        To further confirm whether you have the asset or not, select your response to the question **Are you sure you don't have this asset?**.

        1.  To proceed with your confirmation, tap **Confirm**.
        2.  To cancel your confirmation, tap **Cancel**.

## Result

-   The **Confirm asset** indicator is no longer displayed for the asset.
-   The **Attestation date** field of the asset on the asset attestation form is updated with the actual date on which you confirmed the asset.
-   The **State** field of the asset attestation changes from In progress to Closed complete only when that attestation has no other users and assets involved.
-   The **Status** field of the asset on the asset attestation form is updated based on your confirmation:
    -   If you selected **Yes**, the **Status** field changes from **Open** to **Yes**.
    -   If you selected **No**, the **Status** field changes from **Open** to **No**. Also, a remediation task is created for that attestation. The administrator can work on that task and initiate an investigation to find the asset status.

**Parent Topic:**[Confirming the assigned serialized hardware assets](../concept/confirming-assets-emp-portal-mobile.md)

