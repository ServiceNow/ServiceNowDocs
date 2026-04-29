---
title: Introduction to Orchestration
description: Orchestration automates simple or complex multi-system tasks on remote services, servers, applications, and hardware.
locale: en-US
release: australia
product: Orchestration
classification: orchestration
topic_type: reference
last_updated: "2026-03-12"
reading_time_minutes: 4
breadcrumb: [Classic Orchestration, Workflow Data Fabric]
---

# Introduction to Orchestration

Orchestration automates simple or complex multi-system tasks on remote services, servers, applications, and hardware.

An Orchestration process can cross all management disciplines and interact with hosted services and all types of infrastructure elements. These capabilities provide a powerful system for managing IT and Business processes quickly and reliably.

Orchestrated solutions aide collaboration among teams by providing reusable data and versioning for both the workflows and the activities within them. Subject matter experts can create activities that are reusable to numerous workflow developers. When an activity requires a change, developers can see the downstream implication of the change immediately by knowing which workflows use the activity. Well-designed orchestrations never fail and apply human tasks to address errors as they arise.

## Orchestration tools

Orchestration can make calls outside of a ServiceNow instance, directly to web services or through a MID Server to systems within corporate firewall. Orchestration also enables the creation reusable activities that wrapper Java Script functions for manipulating things inside the platform. Orchestration extends the [Workflow editor](https://www.servicenow.com/docs/access?context=workflow-editor&version=australia&pubname=australia-build-workflows&ft:locale=en-US) by providing these features:

-   [Activity packs](../../../administer/orchestration-activities/concept/c_OrchestrationActivityPacks.md) containing ready-to-use activities.
-   [Activity Designer](../../../administer/orchestration-activity-designer/concept/c_WorkflowActivityDesigner.md), which enables developers to create custom activities without an over dependence to create scripts to orchestrate to third-party systems.
-   Ability to create activity packs using [Scoped Applications](../../../administer/orchestration-activity-designer/concept/c_ActivityScoping.md).
-   A [Databus](../../../administer/orchestration-activity-designer/concept/c_OrchestrationDatabus.md#) for following the flow of data across orchestration activities.

Orchestration Core provides entitlements to use specific applications:

-   **[Client Software Distribution](../concept/c_ClientSoftwareDistribution.md)**

    An application that automates software delivery from the Service Catalog. Provides OOB support for SCCM. Partner solutions support Macs using JAMF. Other third-party solutions provide support through the extension framework.

-   **[Configuring Password Reset](https://www.servicenow.com/docs/access?context=password-reset-admin-guide&version=australia&pubname=australia-servicenow-platform&ft:locale=en-US)**

    An application for users to reset their password in Active Directory. It can expand to communicate with other third-party systems.

-   **[Orchestration ROI](../concept/c_OrchestrationROI.md)**

    Enables users to evaluate estimated costs and actual costs for tasks, automate these tasks, and track the ROI of these tasks.


## Systems that Orchestration can automate

Orchestration can automate tasks such as employee onboarding, user access rights, server management, managed file transfers, and Security Operations Orchestration activities . For example, you might use the Active Directory and Exchange activities provided in the base Orchestration system to set up network accounts and mailboxes for new employees.

If Orchestration does not provide the activities you need for an integration, create the necessary activities using the templates in the [Orchestration Activity Designer](../../../administer/orchestration-activity-designer/concept/c_WorkflowActivityDesigner.md). The external systems that Orchestration can automate for:

-   Any system exposing web services \([SOAP,](https://www.servicenow.com/docs/access?context=t_CreateASOAPWebServiceActivity&version=australia&pubname=australia-servicenow-platform&ft:locale=en-US) [REST](../../../administer/orchestration-activity-designer/task/t_CreateARESTWebServiceActivity.md#)\)
-   Any system accessible from the command line \(such as a UNIX system accessible through [SSH](../../../administer/orchestration-activity-designer/task/t_CreateAnSSHActivity.md#), a Windows system enabled for [PowerShell](../../../administer/orchestration-activity-designer/task/t_CreateAPowershellActivity.md#) remoting or WMI\)
-   Numerous proprietary services: Windows [Active Directory](https://www.servicenow.com/docs/access?context=c_OrchActiveDirectoryActivities&version=australia&pubname=australia-servicenow-platform&ft:locale=en-US), Microsoft [Exchange](../../../administer/orchestration-activities/concept/c_OrchestrationExchangeActivities.md) mail servers, [InfoBlox](../../../administer/orchestration-activities/concept/c_InfobloxDDIActivityPack.md), and [F5 Networks](../../../administer/orchestration-activities/concept/c_OrchF5LoadBalancerActivities.md).

    **Note:** For a full list of Activity Pack service offerings, see [Orchestration Core Activity Packs](../../../administer/orchestration-activities/concept/c_OrchestrationActivityPacks.md).

-   Any filesystem accessible by [SFTP](../../../administer/orchestration-activity-designer/task/t_CreateAnSFTPActivity.md#)
-   Any database with a compliant [JDBC](../../../administer/orchestration-activity-designer/task/t_CreateAJDBCActivity.md#) driver
-   Additional Activity Packs are also available with other ServiceNow products, such as Security Operations

![Orchestration capabilities](../image/OrchestrationDiagram.png "Orchestration capabilities")

## Orchestration workflow

When an Orchestration activity starts within a workflow, Orchestration launches a [Discovery probes and sensors](https://www.servicenow.com/docs/access?context=c_DiscoveryProbesAndSensors&version=australia&pubname=australia-it-operations-management&ft:locale=en-US) and writes a probe record to the ECC Queue. The workflow pauses as the MID Server picks up the request and executes the probe. When the probe reports back, the workflow resumes as the results are analyzed. The workflow can exit or continue at this point.

![Orchestration workflow](../image/OrchestrationWorkflow.png "Orchestration workflow")

