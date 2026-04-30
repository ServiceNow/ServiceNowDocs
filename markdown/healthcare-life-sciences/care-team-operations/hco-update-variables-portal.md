---
title: Update variables in record producers to capture tokenized data from Epic
description: Update the variable values in existing record producers to capture tokenized data from Epic.
locale: en-US
release: yokohama
product: Care Team Operations
classification: care-team-operations
topic_type: task
last_updated: "2025-01-30"
reading_time_minutes: 1
breadcrumb: [Embedding Care Team Portal in Epic Hyperspace via Hyperdrive, Configuring Healthcare Operations Core, Healthcare Operations Core, Healthcare Operations, Healthcare and Life Sciences]
---

# Update variables in record producers to capture tokenized data from Epic

Update the variable values in existing record producers to capture tokenized data from Epic.

## Before you begin

Role required: admin

## About this task

When the Care Team Portal is launched inside of Epic Hyperspace via Hyperdrive, record producers can capture tokenized querystring parameters to populate record producer variables.

This capture is possible due to a catalog client script associated with the record producers.

**For Care Team Operations for Healthcare IT:**The script is called “Populate EMR sessions params” and can found on the “Report an EMR issue” record producer.

**For Care Team Operations for Biomed:**The script is called “Populate biomed service session params” and can be found on the Request other biomed service” record producer.

**Note:** The preceding client scripts only work with the Care Team Portal.

To capture the tokenized querystring parameters, a variable must be created and the name must start with “sysparm\_”. This same variable name must be included at the end of the launch URL in the Epic Hyperspace FDI record.

![Example of variable naming for capturing tokenized data from an EMR system.](../image/hco-variable-example.png)

For example, to capture the “Workstation ID” field from an EMR system, the name value of the variable should “sysparm\_workstation\_id” and the querystring parameter would be `“sysparm_workstation_id =%WORKSTATIONID%”`.

A complete launch querystring would look like the following:

```
https://<instance-name>.service-now.com/careteam?glide_sso_id=<identity-provider-sysid>&sysparm_workstation_id=%WORKSTATIONID%&sysparm_user_template=%USERTEMPLATE%
```

## Procedure

1.  In the Record Producer, navigate to the **Variables** related list.

2.  Select **New**.

3.  Fill in fields as needed.

4.  Confirm that the name value of all variables begins with **sysparm\_** for any field in which you want to capture data coming from an EMR system.

5.  Select **Submit**.


