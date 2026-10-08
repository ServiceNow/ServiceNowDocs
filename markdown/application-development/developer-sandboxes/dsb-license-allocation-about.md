---
title: License assignment
description: License assignment in App Engine Management Center \(AEMC\) lets Developer Sandboxes admins distribute purchased sandbox packs across non-production instances without opening a support case. Each pack contains 10 sandboxes, and assignments are managed from a license management instance.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/application-development/developer-sandboxes/dsb-license-allocation-about.html
release: brazil
product: Developer Sandboxes
classification: developer-sandboxes
topic_type: concept
last_updated: "2026-09-10"
reading_time_minutes: 3
keywords: [developer sandboxes, license allocation, license assignment, sandbox packs, App Engine Management Center, AEMC]
breadcrumb: [Installing, Developer Sandboxes, Build, AI Workflow Factory, Building applications]
---

# License assignment

License assignment in App Engine Management Center \(AEMC\) lets Developer Sandboxes admins distribute purchased sandbox packs across non-production instances without opening a support case. Each pack contains 10 sandboxes, and assignments are managed from a license management instance.

The license management instance \(or controller\) is the production instance where the sandbox licenses are managed and packs are allocated to the non-production instances.

For full details on how to assign a license, see [Assign Developer Sandboxes packs](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/application-development/app-engine-management-center/assign-dsb-packs-aemc.md) in the AEMC documentation.

The license assignment UI is part of the Developer Sandboxes Licensing plugin \(com.glide.dsb.licensing\) and is accessible from the Developer Sandboxes section of AEMC on your license management instance. The UI is not functional on non-production instances.

**Note:** The com.glide.dsb.licensing plugin should be used from only one instance, the license management instance.

## Prerequisite: Add managed instances

Before a sandbox license admin can assign packs to a non-production instance, the instance must be added as a managed instance in Multi-Instance Management. For example, use Multi-Instance Management to save an instance as a development instance linked to the license management instance.

Multi-Instance Management is required for assigning Developer Sandboxes licenses. It depends on the Multi-Instance Setup app \(`sn-app-amf`\), which must be installed separately from the ServiceNow® Store. This app is not a dependency of the `com.glide.dsb.licensing` plugin and is not installed automatically. For details on adding managed instances, see [Connecting controller and managed instances](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/platform-administration/connecting-controller-managed-instances.md).

## Key benefits of self-service license assignment

License assignment for sandboxes:

-   Distribute purchased packs across instances without opening a support case.
-   View purchased packs, assigned packs, and available capacity in one consolidated dashboard view, so you can see current assignment status before making changes.
-   Confirm that the target non-production instance has the required plugin installed before any packs are assigned, helping to avoid misconfiguration.

## Details and considerations for license assignment

Consider the following when using developer sandbox license assignment:

-   Only users with the sn\_dsb\_commons.sandbox\_license\_admin role or the admin role can assign licenses.
-   Pack assignments are permanent. After packs are assigned to an instance, the count can't be decreased. Admins can only increase an existing assignment.
-   A maximum of three packs can be assigned to a single non-production instance, with a maximum of 30 sandboxes per instance.
-   License management is available only from a license management instance. The AEMC UI is not accessible from non-production instances.

## How license assignment works

The license assignment dashboard retrieves purchased pack data from the subscription management table and current assignment state from the instance allocation table \(`sys_dsb_instance_allocation`\). Assignment works as follows:

1.  The assignment dashboard displays each purchased sandbox pack and the total number of sandboxes represented. Each pack contains 10 sandboxes.
2.  You \(a sandbox admin\) select **Assign sandboxes**. A modal opens where you select the non-production instance, as configured in Multi-Instance Management, to receive the packs.
3.  The ServiceNow AI Platform verifies the instance. If verification fails, an inline error indicates that the Developer Sandboxes plugin \(com.glide.dsb\) must be installed on the non-production instance before packs can be assigned.
4.  You select the number of packs to assign. The modal shows total packs available, packs already assigned to other instances, and an assignment progress indicator.
5.  You save the assignment. The status changes to **In progress** while the system processes the assignment, then changes to **Ready** or **Error**.

**Parent Topic:**[Installing Developer Sandboxes](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/application-development/developer-sandboxes/dev-sbx-installing.md)

