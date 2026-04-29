---
title: Asset Attestation
description: Use Asset Attestation to maintain accurate details of all the serialized hardware assets that are assigned to your employees.
locale: en-US
release: australia
product: Hardware Asset Management
classification: hardware-asset-management
topic_type: concept
last_updated: "2026-03-12"
reading_time_minutes: 4
breadcrumb: [Exploring Hardware Asset Management, Hardware Asset Management, IT Asset Management]
---

# Asset Attestation

Use Asset Attestation to maintain accurate details of all the serialized hardware assets that are assigned to your employees.

Asset Attestation has no dependency on the availability of the assets at the office locations. Therefore, organizations that support hybrid and remote work models can audit their assets that are in use even if those assets are dispersed across remote locations. You can achieve asset data accuracy, improve asset utilization, and reduce risk by auditing your assets using Asset Attestation.

As an Asset manager or an Inventory administrator, you can create a one-time asset attestation or create an attestation schedule that creates recurring asset attestations. You can validate whether the serialized hardware asset that's assigned to an employee is still in use by receiving confirmation from the employee directly.

## Asset Attestation benefits

-   Step-by-step guidance on creating asset attestations and schedules using the playbook. For more details, see [Playbook for asset attestation](playbook-asset-attestation-ham.md).

    **Important:** Starting with Hardware Asset Management version 13.0.0, the playbook is the default option for the creation of asset attestations and schedules. However, if you set the value of the **sn\_itam\_common.enable\_asset\_attestation\_playbook** system property to **false** with the asset or inventory\_admin role, you will be shown forms to complete the attestation process instead of the playbook.

-   Ability to perform remote asset audits for the required hardware assets irrespective of their locations. For more details, see [Create an asset attestation in the Inventory view](../task/create-attestation-req-ham.md).
-   Option to set a schedule for creating recurring asset attestations. For more details, see [Create an asset attestation schedule](../task/create-attest-schedule-ham.md).
-   Intuitive and user-friendly Now Mobile app and Employee Center portal that enable the employees to confirm the ownership of the assigned hardware assets and also raise issues related to their hardware and consumable assets. For more details, see the following:
    -   [Confirm the assigned assets using the Now Mobile app](../task/confirm-ham-assets-now-mobile.md)
    -   [Confirm the assigned assets on the Employee Center portal](../task/confirm-assets-on-emp-center.md)
    -   [Raise issue related to your asset on the Employee Center portal](../task/report-asset-issue-attestation.md)
-   Comprehensive reports that enable Asset managers and Inventory administrators to monitor the status of asset attestations and remediation tasks, and take necessary actions. For more details, see the following:
    -   [View open asset attestations in the Hardware Asset Workspace](../task/view-open-asset-attest-ham.md)
    -   [View open remediation tasks for asset attestations in the Hardware Asset Workspace](../task/view-open-remediations-ham.md)
    -   [View attestations for a serialized hardware asset](../task/view-attestations-for-asset-ham.md)

## Requirements and limitations

Asset Attestation has a dependency on the following ServiceNow Store applications:

-   Employee Center \(sn\_ex\_sp\)
-   Employee Profile \(sn\_employee\)

For more details, see [Employee Center](https://www.servicenow.com/docs/access?context=employee-center-landing-page&version=australia&pubname=australia-employee-service-management&ft:locale=en-US) and [Employee profile](https://www.servicenow.com/docs/access?context=employee-profile-portal&version=australia&pubname=australia-employee-service-management&ft:locale=en-US).

If you plan to audit your assets by using Asset Attestation, then consider the following points:

-   Serialized hardware assets that belong to the opted-in resource categories can only be attested. Excluded hardware assets can't be attested.
-   Consumables, bundles, and pallets can't be attested.
-   Attestation supports assets that belong to resource categories of HAM solutions only if they’re opted-in.
    -   Hardware Asset Management integration with Telecommunications Network Inventory- Only assets of Server, Network gear, and Telecom Network Inventory \(TNI\) resource categories can be attested.
    -   Hardware Asset Management integration with Zero Touch Mobility- Only assets of Mobile Device resource category can be attested.

## Asset Attestation workflow

1.  An Asset manager or an Inventory administrator creates a one-time asset attestation by selecting the employees assigned with the assets and the model categories of the assets.

    An attestation record is created in the Asset Attestation \[sn\_itam\_common\_asset\_attestation\] table. Also, the details of the asset to be attested are added to the Attestations for Asset \[sn\_itam\_common\_attestation\_asset\_m2m\] table.

2.  An email notification is sent to the employees who are responsible for confirming the ownership of the assigned assets.
3.  The employees verify the asset details and either accept or deny the ownership of the asset through the Now Mobile app or on the Employee Center portal.

    The status of the asset attestation record is updated.


## Asset Attestation schedule workflow

1.  An Asset manager or an Inventory administrator creates an attestation schedule to create recurring attestations.

    An attestation schedule record is created in the Asset Attestation Schedule \[sn\_itam\_common\_attestation\_schedule\] table.

2.  The **ITAM Common- Asset attestation** daily job runs daily to check through all the asset attestation schedules. This daily job then creates asset attestations based on the frequency specified in the attestation schedule.

For more details on Asset Attestation, see [Audit your hardware assets by using Asset Attestation](audit-hardware-assets-attestation.md).

