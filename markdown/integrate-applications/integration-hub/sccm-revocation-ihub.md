---
title: SCCM software revocation
description: Revoke software without any user interaction using Microsoft System Center Configuration Manager \(SCCM\) if the software configuration specifies an SCCM uninstall collection, even if the software was installed by some other process or user.
locale: en-US
release: australia
product: Integration Hub
classification: integration-hub
topic_type: concept
last_updated: "2026-03-12"
reading_time_minutes: 1
breadcrumb: [CSD from SCCM, Client Software Distribution, Integration Hub solutions, Build integrations, Integration Hub, Workflow Data Fabric]
---

# SCCM software revocation

Revoke software without any user interaction using Microsoft System Center Configuration Manager \(SCCM\) if the software configuration specifies an SCCM uninstall collection, even if the software was installed by some other process or user.

-   **[Revoke software deployed through the service catalog](../tasks/revoke-from-serv-cat.md)**  
Software deployed by SCCM can be revoked, but only when the status of software is **Installed** and the application associated with the software configuration has an uninstall collection configured.
-   **[Revoke unentitled software](../tasks/revoke-unentitled-ihub.md)**  
Revoke software using Microsoft System Center Configuration Manager \(SCCM\) that a user is not entitled to use even if the software was installed by some other process or user.
-   **[SCCM software revocation flow](../reference/software-revoke-ihub.md)**  
The Revoke SCCM Application flow moves a user or device from an install collection to an uninstall collection to revoke software installed from Microsoft System Center Configuration Manager \(SCCM\).

**Parent Topic:**[Client software distribution from SCCM](csd-from-sccm-ihub.md)

