---
title: Client software distribution extension keys
description: Client software distribution \(CSD\) extension keys allow you to customize the deployment and revocation of software from distribution providers.
locale: en-US
release: australia
product: Orchestration
classification: orchestration
topic_type: reference
last_updated: "2026-03-12"
reading_time_minutes: 1
breadcrumb: [Client software distribution extension framework, Client Software Distribution, Orchestration applications, Classic Orchestration, Workflow Data Fabric]
---

# Client software distribution extension keys

Client software distribution \(CSD\) extension keys allow you to customize the deployment and revocation of software from distribution providers.

These pre-defined keys allow you to generate input variables for workflows that deploy and revoke software from external distribution providers:

-   **SetDeploymentData**: Sets the software order information and generates the input variables for the deployment workflow.
-   **SetRevocationData**: Generates the input variables for the revocation workflow.
-   **CheckRevocable**: Specifies the conditions that determine if an installation can be revoked. If the software configuration associated with the installed software allows uninstallation, the installed software can be revoked.

**Parent Topic:**[Client software distribution extension framework](../concept/c_CSDExtensionFramework.md)

