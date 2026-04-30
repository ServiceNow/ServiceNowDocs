---
title: Confirm access to Settings table
description: As part of the configuration for Localization Workspace, confirm access to the Settings table of Localization Framework.
locale: en-US
release: zurich
product: Localization Workspace
classification: localization-workspace
topic_type: task
last_updated: "2025-10-08"
reading_time_minutes: 1
breadcrumb: [Configuring Localization Workspace, Localization Workspace, Translation and localization, Configure core features, Administer]
---

# Confirm access to Settings table

As part of the configuration for Localization Workspace, confirm access to the Settings table of Localization Framework.

## Before you begin

Localization Framework must be installed. It is included with Localization Workspace if not already installed.

Role required: admin. The Localization admin role \(localization\_admin\) can't complete this procedure.

## About this task

Localization Workspace requires access to a Localization Framework table, Settings \[sn\_lf\_setting\]. The Settings table controls the ability to create and update translation projects. Confirm access using the following procedure.

## Procedure

1.  Navigate to **All** &gt; **System Definitions** &gt; **Tables**.

2.  In the **Name** field, search for `sn_lf_setting`.

3.  In the Table form, select the **Application Access** tab.

4.  Select two check boxes: **Can read**, **Can update**.

5.  Select **Update**.


**Parent Topic:**[Configuring Localization Workspace](../concept/configuring-localization-workspace.md)

