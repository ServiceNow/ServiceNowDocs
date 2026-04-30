---
title: Deactivate entity-based access configuration
description: Deactivate an entity-based access \(EBA\) configuration to disable access restrictions from associated records, confirming only active and relevant configurations control data access.
locale: en-US
release: zurich
product: GRC Common Functions
classification: grc-common-functions
topic_type: task
last_updated: "2025-07-31"
reading_time_minutes: 1
breadcrumb: [Manage Entity Based Access, Entity Based Access, Common GRC features, Governance, Risk, and Compliance]
---

# Deactivate entity-based access configuration

Deactivate an entity-based access \(EBA\) configuration to disable access restrictions from associated records, confirming only active and relevant configurations control data access.

## Before you begin

Role required: sn\_grc\_ent\_access.admin

## About this task

Remove outdated or redundant access restrictions from entity records, verifying that only current configurations remain active and relevant.

## Procedure

1.  Navigate to **All** &gt; **Entity Based Access Configurations**.

2.  Locate the entity-based access configuration that you want to deactivate.

3.  Select the configuration record name to open the record.

4.  Verify configuration details such as users, user groups, and applicability.

5.  Select **Deactivate**.

    The system evaluates whether this configuration is the only active configuration affecting access restrictions on the associated records. The system runs a validation check to identify any potential access impacts or dependency conflicts.

    If other active configurations exist that apply to the same records, a confirmation prompt appears.


## Result

The system updates the configuration and removes access restrictions for the affected records only if it is the only active configuration on the related records.

**Parent Topic:**[Managing Entity Based Access](../concept/using-entity-based-access.md)

