---
title: Audit your hardware assets by using Asset Attestation
description: Improve the asset utilization by auditing the hardware assets assigned to your employees and validating if the employees are using the assigned assets.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/it-asset-management/hardware-asset-management/audit-hardware-assets-attestation.html
release: brazil
product: Hardware Asset Management
classification: hardware-asset-management
topic_type: concept
last_updated: "2026-09-10"
reading_time_minutes: 3
keywords: [Asset attestation, Attestation playbook, Attestation schedule]
breadcrumb: [Attestation and conformance, Use, Hardware Asset Management, IT Asset Management, Asset Management]
---

# Audit your hardware assets by using Asset Attestation

Improve the asset utilization by auditing the hardware assets assigned to your employees and validating if the employees are using the assigned assets.

As an Asset manager or an Inventory administrator, you can create an asset attestation in any of the following ways:

-   [Create an asset attestation or a schedule using the playbook](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/it-asset-management/hardware-asset-management/create-attestation-using-playbook.md)
-   [Create an asset attestation in the Inventory view](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/it-asset-management/hardware-asset-management/create-attestation-req-ham.md).
-   [Create an asset attestation schedule](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/it-asset-management/hardware-asset-management/create-attest-schedule-ham.md).
-   [Create an attestation for a hardware asset](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/it-asset-management/hardware-asset-management/attest-single-asset-ham.md)

**Important:** Starting with Hardware Asset Management version 13.0.0, the playbook is the default option for the creation of asset attestations and schedules. However, if you set the value of the **sn\_itam\_common.enable\_asset\_attestation\_playbook** system property to **false** with the asset or inventory\_admin role, you will be shown forms to complete the attestation process instead of the playbook.

As an employee, you can confirm the assets assigned to you in any of the following ways:

-   [Confirm the assigned assets using the Now Mobile app](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/it-asset-management/hardware-asset-management/confirm-ham-assets-now-mobile.md).
-   [Confirm the assigned assets on the Employee Center portal](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/it-asset-management/hardware-asset-management/confirm-assets-on-emp-center.md).

For more details, see [Asset Attestation](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/it-asset-management/hardware-asset-management/asset-attestation-ham.md).

-   **[Playbook for asset attestation](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/it-asset-management/hardware-asset-management/playbook-asset-attestation-ham.md)**  
The Create asset attestation playbook provides detailed, step-by-step instructions for creating an asset attestation. This playbook guides you through each stage of the attestation process, starting from filling in the asset attestation details to the completion of attestation.
-   **[Create an asset attestation in the Inventory view](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/it-asset-management/hardware-asset-management/create-attestation-req-ham.md)**  
Create an asset attestation to validate whether the serialized hardware asset that's assigned to an employee is still in use.
-   **[Create an asset attestation schedule](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/it-asset-management/hardware-asset-management/create-attest-schedule-ham.md)**  
Create an attestation schedule so that recurring asset attestations are created based on the frequency that you specify.
-   **[Create an attestation for a hardware asset](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/it-asset-management/hardware-asset-management/attest-single-asset-ham.md)**  
Validate a particular serialized hardware asset by creating an attestation for that asset.
-   **[View attestations for a serialized hardware asset](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/it-asset-management/hardware-asset-management/view-attestations-for-asset-ham.md)**  
View all the attestation records associated with a serialized hardware asset to check the status of previous asset attestations.
-   **[View open asset attestations in the Hardware Asset Workspace](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/it-asset-management/hardware-asset-management/view-open-asset-attest-ham.md)**  
Get the details of all asset attestations that are awaiting action from your employees in the Hardware Asset Workspace.
-   **[Cancel an asset attestation](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/it-asset-management/hardware-asset-management/cancel-asset-attestation-ham.md)**  
Cancel an asset attestation when you no longer have to validate the ownership of the serialized assets.
-   **[Cancel an attestation schedule](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/it-asset-management/hardware-asset-management/cancel-attestation-schedule-ham.md)**  
Cancel an attestation schedule when you no longer want to create recurring asset attestations.
-   **[View open remediation tasks for asset attestations in the Hardware Asset Workspace](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/it-asset-management/hardware-asset-management/view-open-remediations-ham.md)**  
Get the details of all the remediation tasks for asset attestations that are awaiting your action in the Hardware Asset Workspace.
-   **[Complete the remediation task for asset attestation in the Hardware Asset Workspace](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/it-asset-management/hardware-asset-management/complete-attestation-remediation-ham.md)**  
As an asset manager or inventory administrator, complete the open remediation task that was created when your employee denied ownership of the assigned serialized hardware asset.

**Parent Topic:**[Attestation and conformance](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/it-asset-management/hardware-asset-management/attestation-compliance-ham.md)

**Related topics**  


[Manage Hardware Asset Management subscriptions]()

