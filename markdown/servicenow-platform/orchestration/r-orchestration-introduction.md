---
title: Introduction to Orchestration
description: Orchestration automates simple or complex multi-system tasks on remote services, servers, applications, and hardware.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/servicenow-platform/orchestration/r-orchestration-introduction.html
release: australia
product: Orchestration
classification: orchestration
topic_type: reference
last_updated: "2026-03-12"
reading_time_minutes: 4
breadcrumb: [Classic Orchestration, ServiceNow AI Platform Additional Capabilities, Extend ServiceNow AI Platform capabilities]
---

# Introduction to Orchestration

Orchestration automates simple or complex multi-system tasks on remote services, servers, applications, and hardware.

An Orchestration process can cross all management disciplines and interact with hosted services and all types of infrastructure elements. These capabilities provide a powerful system for managing IT and Business processes quickly and reliably.

Orchestrated solutions aide collaboration among teams by providing reusable data and versioning for both the workflows and the activities within them. Subject matter experts can create activities that are reusable to numerous workflow developers. When an activity requires a change, developers can see the downstream implication of the change immediately by knowing which workflows use the activity. Well-designed orchestrations never fail and apply human tasks to address errors as they arise.

## Orchestration tools

Orchestration can make calls outside of a ServiceNow instance, directly to web services or through a MID Server to systems within corporate firewall. Orchestration also enables the creation reusable activities that wrapper Java Script functions for manipulating things inside the platform. Orchestration extends the [Workflow editor](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/build-workflows/workflow-editor.md) by providing these features:

-   [Activity packs](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/servicenow-platform/orchestration/c_OrchestrationActivityPacks.md) containing ready-to-use activities.
-   [Activity Designer](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/servicenow-platform/orchestration/c_WorkflowActivityDesigner.md), which enables developers to create custom activities without an over dependence to create scripts to orchestrate to third-party systems.
-   Ability to create activity packs using [Scoped Applications](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/servicenow-platform/orchestration/c_ActivityScoping.md).
-   A [Databus](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/servicenow-platform/orchestration/c_OrchestrationDatabus.md) for following the flow of data across orchestration activities.

Orchestration Core provides entitlements to use specific applications:

-   **[Client Software Distribution](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/servicenow-platform/orchestration/c_ClientSoftwareDistribution.md)**

    An application that automates software delivery from the Service Catalog. Provides OOB support for SCCM. Partner solutions support Macs using JAMF. Other third-party solutions provide support through the extension framework.

-   **[Configuring Password Reset](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/servicenow-platform/password-reset/password-reset-admin-guide.md)**

    An application for users to reset their password in Active Directory. It can expand to communicate with other third-party systems.

-   **[Orchestration ROI](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/servicenow-platform/orchestration/c_OrchestrationROI.md)**

    Enables users to evaluate estimated costs and actual costs for tasks, automate these tasks, and track the ROI of these tasks.


## Systems that Orchestration can automate

Orchestration can automate tasks such as employee onboarding, user access rights, server management, managed file transfers, and Security Operations Orchestration activities . For example, you might use the Active Directory and Exchange activities provided in the base Orchestration system to set up network accounts and mailboxes for new employees.

If Orchestration does not provide the activities you need for an integration, create the necessary activities using the templates in the [Orchestration Activity Designer](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/servicenow-platform/orchestration/c_WorkflowActivityDesigner.md). The external systems that Orchestration can automate for:

-   Any system exposing web services \([SOAP,](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/servicenow-platform/orchestration/t_CreateASOAPWebServiceActivity.md) [REST](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/servicenow-platform/orchestration/t_CreateARESTWebServiceActivity.md)\)
-   Any system accessible from the command line \(such as a UNIX system accessible through [SSH](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/servicenow-platform/orchestration/t_CreateAnSSHActivity.md), a Windows system enabled for [PowerShell](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/servicenow-platform/orchestration/t_CreateAPowershellActivity.md) remoting or WMI\)
-   Numerous proprietary services: Windows [Active Directory](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/servicenow-platform/orchestration/c_OrchActiveDirectoryActivities.md), Microsoft [Exchange](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/servicenow-platform/orchestration/c_OrchestrationExchangeActivities.md) mail servers, [InfoBlox](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/servicenow-platform/orchestration/c_InfobloxDDIActivityPack.md), and [F5 Networks](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/servicenow-platform/orchestration/c_OrchF5LoadBalancerActivities.md).

    **Note:** For a full list of Activity Pack service offerings, see [Orchestration Core Activity Packs](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/servicenow-platform/orchestration/c_OrchestrationActivityPacks.md).

-   Any filesystem accessible by [SFTP](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/servicenow-platform/orchestration/t_CreateAnSFTPActivity.md)
-   Any database with a compliant [JDBC](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/servicenow-platform/orchestration/t_CreateAJDBCActivity.md) driver
-   Additional Activity Packs are also available with other ServiceNow products, such as Security Operations

\[Omitted image "OrchestrationDiagram.png"\] Alt text: Orchestration capabilities

## Orchestration workflow

When an Orchestration activity starts within a workflow, Orchestration launches a [Discovery probes and sensors](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/it-operations-management/c_DiscoveryProbesAndSensors.md) and writes a probe record to the ECC Queue. The workflow pauses as the MID Server picks up the request and executes the probe. When the probe reports back, the workflow resumes as the results are analyzed. The workflow can exit or continue at this point.

\[Omitted image "OrchestrationWorkflow.png"\] Alt text: Orchestration workflow

