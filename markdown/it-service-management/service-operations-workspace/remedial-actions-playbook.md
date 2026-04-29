---
title: Remedial actions using Playbook
description: Resolve the CI-related issues using the remedial actions using Playbook in the Investigate tab.
locale: en-US
release: australia
product: Service Operations Workspace
classification: service-operations-workspace
topic_type: concept
last_updated: "2026-03-12"
reading_time_minutes: 6
breadcrumb: [Incident Management in Service Operations Workspace, Operating IT services in your organization, Service Operations Workspace for ITSM, IT Service Management]
---

# Remedial actions using Playbook

Resolve the CI-related issues using the remedial actions using Playbook in the Investigate tab.

The Investigate tab includes the following types of remedial action to resolve CI-related issues:

-   End process
-   Restart service

These remedial actions are available on the Investigate tab only if the following conditions are met:

-   The Investigation Framework \[sn\_invest\_fwk\] application is installed and configured. For more information, see [Setting up Investigation Framework in Service Operations Workspace](set-up-investigate.md) and [Configure the Remedial Actions Framework](../task/config-remedial-action-fw.md).
-   The remedial actions are configured to display on the UI. For more information, see [Customize the Investigate tab](customize-the-incident-record-page.md#).

Remedial actions use playbooks to resolve CI issues. Playbook provides you with an interactive UI to guide and execute the remedial actions step by step. With a playbook, you can control every execution step of the remediation process. Playbook is available on the contextual side panel of the Incident record page. When any remedial action is performed, that remediation process is added to a playbook. You can then select the playbook \(![Playbook icon](../image/playbook_icon.png)\) icon on the contextual side panel to open the playbook on a separate panel and execute the process. The playbook panel displays the following tabs:

-   Current: Displays the current list of playbooks that trigger the remedial action, including both processes and services that have the status New and In Progress.
-   History: Displays the historical list of playbooks, including both processes and services that have the status **Completed**, **Canceled**, or **Failed**.

You can perform remedial actions on both the affected CIs and the caller CIs associated with the incident record. The caller CIs are the CIs that are assigned to the caller.

**Note:** If the CI is DEX supported, the remedial actions playbook for the DEX actions are displayed. If the CI is SOW or default view supported, the remedial actions playbook for SOW actions are displayed.

You can cancel an ongoing End process or Restart service remedial action playbook. To cancel a remedial action playbook, select the remedial action playbook and select the menu \(![Menu icon](../../configurable-workforce-optimization-itsm/image/menu-icon.png)\) icon and then select **Cancel action** option. After the remedial action playbook is canceled, the corresponding action is also canceled. Then, the status of the remedial action is displayed as **Canceled** in the History tab of the playbook panel. To view the reason for cancellation, select the **View reason** option on the playbook. This option isn’t available if any of the following are true:

-   The remedial action is already in **Canceled** status.
-   The corresponding CI action record of the remedial action is already in progress.
-   The change request has already moved to implement state for actions associated to CIs of type server.

The Remedial actions section on the Investigate tab also contains the **Current** and **History** tab to display the list of remedial actions performed. By default, this section displays the list of remedial actions for the primary CI or current CI. You can switch the **Show actions performed on all CIs in this incident** toggle to display the list of remedial actions for all the CIs associated with the Incident.

Playbook is available only if both the Remedial Action Framework \[com.snc.sn\_reacf\] application and the Investigation Framework \[sn\_invest\_fwk\] application are installed and configured, as well as if the remedial actions are triggered.

**Note:** You can't execute concurrent or duplicate remedial actions when a remedial action is in progress on a process or service for a CI type device or server. You also can't execute concurrent or duplicate remedial actions on the same CI until the previous remedial action execution is completed. You can change this behavior and allow concurrent execution of the remedial action by selecting the **Allow concurrent execution** option for Remedial Action Type. For more information, see [Configure the Remedial Actions Framework](../task/config-remedial-action-fw.md).

## End process

The **End process** remedial action is available with the following metric information cards:

-   Top processes By Memory
-   Top processes By CPU

Select the CI and then select **End process** to stop the process running on the CI. The remediation process then is added to the playbook. Select the Playbook \(![Playbook icon](../image/playbook_icon.png)\) icon from the contextual side panel to open the playbook on a separate panel and execute the process. You can execute the End process remedial action for the following CI classes:

-   Device: For this CI class, a two-step process is executed where you must get the user approval before the End process remediation process can be executed. After it’s approved, you can directly stop the process on the device, which is also known as the endpoint.
-   Server: For this CI class, you must create a change request before the End process remedial action can be executed using a standard change request. You must also provide additional information to create a change request.

## Restart service

The **Restart service** remedial action is available with the Services metric information card.

Select the CI and then select **Restart service** to restart the services running on the CI. The remediation process then is added to the playbook. Select the Playbook \(![Playbook icon](../image/playbook_icon.png)\) icon on the contextual side panel to open the playbook on a separate panel and execute the process. You can execute the Restart service remedial action for the following CI classes:

-   Device: For this CI class, a two-step process is executed where you must get the user approval before the Restart service remediation process is executed. After it's approved, you can directly restart the services on the device, which is also known as the endpoint.
-   Server: For this CI class, you must create a change request before you can execute the remedial action using a standard change request. You must also provide additional information to create a change request.

**Parent Topic:**[Incident Management in Service Operations Workspace](incident-sow.md)

**Related topics**  


[Create an incident in Service Operations Workspace](../task/create-incident-sow.md)

[View and update incident information on the Overview tab in SOW](../task/view-update-inc-overview-tab.md)

[Viewing incident record information using the Contextual side panel](view-inc-record-info-contextual-sidepanel.md)

[Work on an incident list page in Service Operations Workspace](../task/work-incident-list-page-sow.md)

[Work on an incident record in Service Operations Workspace](../task/work-on-incident-sow.md)

[Close resolved incident](../task/close-resolved-incident-sow.md)

[Reopen an incident in Service Operations Workspace](../task/reopen-incident-sow.md)

[Incident Management in Service Operations Workspace reference](sow-im-reference.md)

