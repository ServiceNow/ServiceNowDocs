---
title: Client software distribution extension keys
description: Client software distribution \(CSD\) extension keys allow you to customize the deployment and revocation of software from distribution providers.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/zurich/servicenow-platform/orchestration/r\_CSDExtensionKeys.html
release: zurich
product: Orchestration
classification: orchestration
topic_type: reference
last_updated: "2025-07-31"
reading_time_minutes: 1
breadcrumb: [Client software distribution extension framework, Client Software Distribution, Orchestration applications, Classic Orchestration, ServiceNow AI Platform Additional Capabilities, Extend ServiceNow AI Platform capabilities]
---

# Client software distribution extension keys

Client software distribution \(CSD\) extension keys allow you to customize the deployment and revocation of software from distribution providers.

These pre-defined keys allow you to generate input variables for workflows that deploy and revoke software from external distribution providers:

-   **SetDeploymentData**: Sets the software order information and generates the input variables for the deployment workflow.
-   **SetRevocationData**: Generates the input variables for the revocation workflow.
-   **CheckRevocable**: Specifies the conditions that determine if an installation can be revoked. If the software configuration associated with the installed software allows uninstallation, the installed software can be revoked.

**Parent Topic:**[Client software distribution extension framework](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/servicenow-platform/orchestration/c_CSDExtensionFramework.md)

