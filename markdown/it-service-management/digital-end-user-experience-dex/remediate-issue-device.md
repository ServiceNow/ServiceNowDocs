---
title: Remediate an issue on the device
description: You can create a remedial action or modify an existing one once you configure the remedial action framework. Remedial action enables you to trigger an action on the impacted device.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/zurich/it-service-management/digital-end-user-experience-dex/remediate-issue-device.html
release: zurich
product: Digital End-User Experience \(DEX\)
classification: digital-end-user-experience-dex
topic_type: concept
last_updated: "2025-07-31"
reading_time_minutes: 1
breadcrumb: [DEX remedial actions, Configure, Digital End-User Experience, IT Service Management]
---

# Remediate an issue on the device

You can create a remedial action or modify an existing one once you configure the remedial action framework. Remedial action enables you to trigger an action on the impacted device.

## Single device remedial action

You can execute a remedial action on a single device by navigating to the device health page to resolve the issue. To access the Device health page;

1.  Navigate to **Workspaces** &gt; **Service Operation Workspace** &gt; **Devices**.
2.  Select the device that you want to view the details.
3.  Select **Action library**.\[Omitted image "actionlib.png"\] Alt text: Action library
4.  Choose the remedial action that you want to run and select **Run action**. If the remedial action is applied for the first time, the end-user approval is required.
5.  Provide your approval on the user approval check and select **Submit**.\[Omitted image "userapprovalcheck.png"\] Alt text: User approval check.

**Note:** All remedial actions that you run from the device page are added to a playbook. You can monitor current and past remedial actions or cancel ongoing actions from the playbook. For more information, see [Monitor or cancel remedial actions in DEX device page Playbook](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/it-service-management/digital-end-user-experience-dex/manage-devices-remedial-actions-playbook.md).

\[Omitted image "ra-adh.png"\] Alt text: Remedial action on a single device

## Bulk remedial action

Remedial actions on multiple devices enable DEX engineers and the computing teams to manage the health of the end-user experience proactively. The DEX engineers can select multiple devices to execute the remedial action at the same time. Remedial actions are available for bulk remediation when DEX Admin configures the option **Available for bulk remediation** for a remedial action. Once the bulk remedial action is executed, the DEX engineers should be able to view the status of the remedial action executed on the selected devices.

\[Omitted image "bulk-ra.png"\] Alt text: Bulk remedial action

**Parent Topic:**[DEX remedial actions](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/it-service-management/digital-end-user-experience-dex/dex-remedial-actions.md)

