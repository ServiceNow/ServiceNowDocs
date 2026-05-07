---
title: Granular admin role changes in Enterprise Architecture
description: Understand the transition from global admin usage to feature‑specific granular admin roles, outlining the intent, architectural principles, and governance expectations defined by the Granular Admin Directive.
locale: en-US
release: australia
topic_type: reference
last_updated: "2026-03-12"
reading_time_minutes: 1
breadcrumb: [Install Enterprise Architecture Workspace, Configuring Enterprise Architecture Workspace, Enterprise Architecture Workspace, Enterprise Architecture]
---

# Granular admin role changes in Enterprise Architecture

Understand the transition from global admin usage to feature‑specific granular admin roles, outlining the intent, architectural principles, and governance expectations defined by the Granular Admin Directive.

Enterprise Architecture now standardizes on granular admin roles to ensure controlled, least‑privilege access while preserving backward compatibility for existing customers.

## What changed

The global `admin` role is no longer referenced directly by application features or capabilities. Instead,

-   Ff\\eature‑specific granular admin roles are introduced \(for example, sn\_apm.apm\_admin, cost\_transparency\_analyst\).
-   Application modules, system properties, and applications reference only granular roles
-   The `admin` role continues to function through role inheritance, ensuring upgrade safety and non‑breaking behavior.

## Why this change

Direct usage of the `admin` role for feature administration resulted in:

-   Over‑privileged access models
-   Increased security risk
-   Tight coupling between unrelated features
-   Limited ability to delegate administration safely
-   Granular admin roles address these concerns by:
    -   Enforcing least‑privilege architecture principles
    -   Improving security and auditability
    -   Enabling user‑controlled delegation
    -   Preserving backward compatibility during upgrades

## Standard role pattern

![Role patter.](../../image/eaw-image/role-pattern.png)

-   `<feature>_admin` – Full administrative control for a specific feature or capability
-   `<feature>_read` – Read‑only access for operational or reporting use
-   `<feature>_user` – Standard usage access

## Example granular roles for Enterprise Architecture

-   `sn_apm.apm_admin` – Administers Enterprise Architecture features and configurations
-   `sn_apm.apm_read` – Read‑only access to Enterprise Architecture data
-   `sn_apm.apm_user` – Standard Enterprise Architecture user access

**Parent Topic:**[Install Enterprise Architecture Workspace](../../task/install-ea-workspace.md)

