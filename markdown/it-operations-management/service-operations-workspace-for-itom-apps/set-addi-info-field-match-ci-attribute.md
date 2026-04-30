---
title: Set additional info fields to match CI attribute format
description: Set additional info fields in alerts to match the field and value format of CI attributes in CI records. This ensures accurate alert-to-CI binding, improving alert tracking and reducing manual effort.
locale: en-US
release: zurich
product: Service Operations Workspace for ITOM Apps
classification: service-operations-workspace-for-itom-apps
topic_type: task
last_updated: "2026-04-29"
reading_time_minutes: 1
breadcrumb: [Create Enrich automation, Alert automation in SOW for ITOM, Using SOW for ITOM, Service Operations Workspace for ITOM, ITOM AIOps, IT Operations Management]
---

# Set additional info fields to match CI attribute format

Set additional info fields in alerts to match the field and value format of CI attributes in CI records. This ensures accurate alert-to-CI binding, improving alert tracking and reducing manual effort.

## Before you begin

Ensure that you are on the Enrich Alerts page and the **Improve configuration item \(CI\) identification** toggle switch is enabled.

Role required: evt\_mgmt\_admin, evt\_team\_operator, or srm\_responder

## About this task

The system attempts to match the **Additional Info** fields of the alert with attributes in the CI table. If exactly one matching CI is found, the alert is linked to that CI. For CI identification to be successful, add new fields or ensure that your alert has additional info fields corresponding to column name for CI attributes. For example, use column name **ip\_address** instead of the column label **IP Address**. Each matching key name must have matching values. If there are matching fields in your alert that you don’t wish to use for binding, copy them to another field then clear the original field.

## Procedure

1.  Under **Improve configuration item \(CI\) identification**, in the **Select which CI class you'd like to identify** field, select the CI class.

    ![Improve configuration item (CI) identification option](../image/sow-enrich-ci-binding-0.png)

2.  Select **View items** next to the **Select which CI class you'd like to identify** field to open the list of CIs of the selected CI class.

    ![List of CIs](../image/sow-enrich-ci-binding-1.png)

3.  Select a CI name to open its details or record page.

    At least one field and its corresponding value from the CI details page must appear in the **Additional info** field of the alert.

    ![Details of a CI](../image/sow-enrich-ci-binding-2.png)

4.  In the Enrich Alerts page, use **Extract fields**, **Copy or Compose fields**, and **Change alert values** to set at least one **Additional info** field in your alert to precisely match the field and value format of the CI attributes in the CI record.

    Example: Suppose the CI record page has the **name** field with the value **CRUPRGWMIDCAV15**. To include these fields and their values in the **Additional info** field of the alert, set the fields as shown in the image.

    Map the `${u_host_host}` field to a new field called **name**. This field is added to the **Additional info** and is used for CI identification during the binding stage.

    ![Fields and its corresponding values from the CI details page appear in the Additional info field of the alert.](../image/sow-enrich-ci-binding-3.png)


