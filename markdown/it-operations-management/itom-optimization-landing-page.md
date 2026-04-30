---
title: ITOM Optimization
description: The IT Operations Management \(ITOM\) Optimization application provides automation for the cloud workflows used to manage the cloud resources throughout their life cycle. It enables certified and enterprise-compliant cloud deployment, cost visibility, and other cloud management processes.
locale: en-US
release: yokohama
topic_type: reference
last_updated: "2025-01-30"
reading_time_minutes: 2
breadcrumb: [IT Operations Management]
---

# ITOM Optimization

The IT Operations Management \(ITOM\) Optimization application provides automation for the cloud workflows used to manage the cloud resources throughout their life cycle. It enables certified and enterprise-compliant cloud deployment, cost visibility, and other cloud management processes.

## Features of ITOM Optimization

ITOM Optimization features provide an integrated, service-centric approach that maximizes business service quality, drives efficient processes, and promotes strong governance.

-   **[Cloud Provisioning and Governance](../../cloud-management-v2/concept/cloud-management-v2-landing-page.md)**

    The ServiceNow® Cloud Provisioning and Governance \(CPG\) application serves as a unified interface for accessing cloud resources, delivering cloud offerings to a catalog, and overseeing resource usage. This application is transformed as Cloud Services Catalog application, offering refined and streamlined management of usage and life cycle of cloud resources.


## Workflow migration

All default predefined workflows have been redesigned using Workflow Studio.

Policy Rule Actions can now use Workflow Studio subflows instead of legacy workflows. If you have not customized the default workflows, the legacy workflows are migrated to subflows automatically. If you have customized the default workflows, they aren’t migrated, and their use cases continue to work with the existing workflows.

The following workflows have been migrated to Workflow Studio flows or subflow:

-   Cloud operation change request
-   Cloud task processing
-   Cloud approval workflow
-   Post-process workflow
-   Pre-process workflow

The following workflows have been deprecated:

-   Retrieve cloud billing data
-   Retrieve cloud billing month
-   Cloud operation step workflow launcher

## ITOM Optimization licensing

The ServiceNow AI Platform® uses a licensing method where your organization is billed for using ITOM Optimization applications. The ServiceNow Product Documentation doesn't provide information on prices, packaging, or other details determined by your organization customer contract. For general information about licensing and subscriptions, see [ITOM/OT SU Licensing and subscriptions](itom-su-licensing-landing-page.md).

## Using guided setup to implement IT Operations Management applications

The IT Operations Management guided setup application provides a sequence of tasks that help you configure IT Operations Management applications on your ServiceNow instance. To open IT Operations Management guided setup, navigate to **Guided Setup** &gt; **ITOM Guided Setup**. For more information about using the guided setup interface, see [Using guided setup](https://www.servicenow.com/docs/access?context=guided-setup&version=yokohama&pubname=yokohama-platform-user-interface&ft:locale=en-US).

## What to do next

See [Plugins activated with ITOM Optimization](plugin-itom-optimization.md) to find the list of plugins you activate with IT Operations Management.

