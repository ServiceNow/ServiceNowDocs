---
title: Client software distribution extension keys
description: Client software distribution \(CSD\) extension keys allow you to customize the deployment and revocation of software from distribution providers.
locale: en-US
release: xanadu
product: Integration Hub
classification: integration-hub
topic_type: reference
last_updated: "2024-08-01"
reading_time_minutes: 1
breadcrumb: [Client software distribution extension framework, Client Software Distribution using Integration Hub, Integration Hub available solutions, Building integrations in Integration Hub, Integration Hub, Creating integrations with applications]
---

# Client software distribution extension keys

Client software distribution \(CSD\) extension keys allow you to customize the deployment and revocation of software from distribution providers.

These pre-defined keys allow you to generate input variables for flows that deploy and revoke software from external distribution providers:

-   **SetDeploymentData**: Sets the software order information and generates the input variables for the deployment flow.
-   **SetRevocationData**: Generates the input variables for the revocation flow.
-   **CheckRevocable**: Specifies the conditions that determine if an installation can be revoked. If the software configuration associated with the installed software allows uninstallation, the installed software can be revoked.

**Parent Topic:**[Client software distribution extension framework](../concept/csd-ext-framewrk.md)

