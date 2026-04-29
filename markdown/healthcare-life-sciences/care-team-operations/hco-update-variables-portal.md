---
title: Update variables in record producers to capture tokenized data from Epic Hyperspace
description: Update the variable values in existing record producers to capture tokenized data from Epic.
locale: en-US
release: australia
product: Care Team Operations
classification: care-team-operations
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 1
breadcrumb: [Embed Care Team Portal in Epic, Configure, Healthcare Operations Core, Healthcare Operations, Healthcare and Life Sciences]
---

# Update variables in record producers to capture tokenized data from Epic Hyperspace

Update the variable values in existing record producers to capture tokenized data from Epic.

## Before you begin

Role required: admin

## About this task

When the Care Team Portal is launched inside of Epic Hyperspace via Hyperdrive, record producers can capture Epic launch tokens from the oAuth launch context to populate record producer variables.

This capture is possible due to the **Setup launch parameters from Epic** variable set, which includes the script **Populate launch data from Epic**.

To capture the launch tokens protected and shared by oAuth, a variable must be created on the record producer and the name must start with “sysparm\_”. This same variable name must be included as a key in Epic's FDI record launch context configuration.

![Variable naming for capturing tokenized data from an EMR system.](../image/hco-variable-example.png)

For example, to capture the “Workstation ID” field from an EMR system, the name value of the variable should “sysparm\_workstation\_id” and the launch parameter would be `sysparm_workstation_id` with the value set to `=%WORKSTATIONID%`.

For information about configuring launch parameters in Epic, see [Configure the integration settings in the Hyperdrive Client Test Harness for Care Team Portal](configure-hyperspace-hco.md).

## Procedure

1.  In the Record Producer, navigate to the **Variables** related list.

2.  Select **New**.

3.  Fill in fields as needed.

4.  Confirm that the name value of all variables begins with **sysparm\_** for any field in which you want to capture data coming from an EMR system.

5.  Select **Submit**.


