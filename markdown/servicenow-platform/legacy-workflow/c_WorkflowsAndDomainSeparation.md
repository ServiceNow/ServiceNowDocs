---
title: Domain separation and Workflow
description: Domain separation is supported in the Workflow application. Domain separation enables you to separate data, processes, and administrative tasks into logical groupings called domains. You can control several aspects of this separation, including which users can see and access data.Delegated administration allows child domains to inherit workflows from higher up the domain hierarchy and to override them with domain-specific versions if necessary.When a user starts a new workflow, the workflow runs with that user's domain and credentials.
locale: en-US
release: australia
product: Legacy Workflow
classification: legacy-workflow
topic_type: concept
last_updated: "2026-03-12"
reading_time_minutes: 3
breadcrumb: [Workflow concepts, Classic Workflow, ServiceNow AI Platform Additional Capabilities, Extend ServiceNow AI Platform capabilities]
---

# Domain separation and Workflow

Domain separation is supported in the Workflow application. Domain separation enables you to separate data, processes, and administrative tasks into logical groupings called domains. You can control several aspects of this separation, including which users can see and access data.

## Support level: Standard\*

-   Includes **Basic** level
-   Business logic: Processes can be created or modified per customer by the service provider. The use cases reflect proper use of the application by multiple service provider customers in a single instance.
-   The owner of the instance needs to be able to configure MVP business logic and data parameters per tenant as expected for the specific application.

Use case: As an admin, I need the ability to make comments mandatory on close of a record for one tenant, but not for another.

## Overview

When domain separation is enabled, workflows and workflow activities inherit the domain of the user who publishes or creates them.

## How domain separation works in the Workflow application

While workflows are managed by multiple tables, only the following tables are used for domain separation features:

-   **Workflow \[wf\_workflow\]** and **Workflow Version \[wf\_workflow\_version\]**: used for [Process administration](https://www.servicenow.com/docs/access?context=c_DelegatedAdministration&version=australia&pubname=australia-platform-security&ft:locale=en-US) or process separation.
-   **Workflow Context \[wf\_context\]**: used for [Understanding domain separation](https://www.servicenow.com/docs/access?context=c_DomainSeparation&version=australia&pubname=australia-platform-security&ft:locale=en-US).

**Note:** The Workflow Version table \[wf\_workflow\_version\] table does not contain a domain field; Workflow Version records inherit their domain from the parent Workflow record.

The Workflow Editor displays a workflow's domain in the title bar after the workflow name.

![](../image/WorkflowEditorDomain.png "Workflow editor domain")

**Parent Topic:**[Workflow concepts](c_WorkflowConcepts.md)

**Related topics**  


[Domain separation for service providers](https://www.servicenow.com/docs/access?context=domain-sep-landing-page&version=australia&pubname=australia-platform-security&ft:locale=en-US)

## Workflows and delegated administration

Delegated administration allows child domains to inherit workflows from higher up the domain hierarchy and to override them with domain-specific versions if necessary.

![Processes are visible upwards. A child domain can see workflows in a parent domain.](../image/WorkflowsAndDelegatedAdministration.png "Workflow and delegated administration")

Workflow records in the Workflow \[wf\_workflow\] and Workflow Version \[wf\_workflow\_version\] tables are considered processes. A user in a child domain may check out but not copy a workflow from a parent domain. When a user in a child domain checks out a workflow from a parent domain, the system creates a version of the workflow in that user's domain. This new version is a unique record in the Workflow \[wf\_workflow\] table. After the user publishes this new workflow, other users in the child domain use the new workflow, which overrides the workflow from the parent domain. The original workflow in the parent domain is no longer visible to users in the child domain.

For example, a managed service provider \(MSP\) hosts ITSM services for several companies, including ACME and Initech, on a single instance. As administrators, the MSP creates a Change Request - Emergency workflow that applies to all domains because it was created in the TOP domain, which is the highest domain in the domain hierarchy. This workflow overrides the global Change Request - Emergency workflow and specifies that emergency change requests require approval from the CAB approval group. Because of delegated administration, every domain in the hierarchy sees and uses this workflow. Now suppose the ACME domain requires a different approval policy where emergency change requests require approval from the emergency CAB approval group. The MSP creates another version of the Change Request - Emergency workflow in the ACME domain. This workflow overrides the version in the TOP domain and only applies to users in the ACME domain.

## Workflow permissions

When a user starts a new workflow, the workflow runs with that user's domain and credentials.

The workflow preserves a user's domain and credentials until an activity causes the workflow to wait, such as an approval activity waiting for approval or rejection. When the stopped workflow resumes, such as when a user approves a request, the workflow uses the credentials of the approving user, but continues to run within the domain of the original user.

