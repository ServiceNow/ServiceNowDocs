---
title: Configure AES/AEMC integration properties
description: Configure the AES/AEMC integration to enforce automated Scan Engine compliance checks on custom app deployment requests from App Engine Studio and ServiceNow Studio.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/impact/aes-aemc-integration-properties.html
release: australia
topic_type: task
last_updated: "2026-05-07"
reading_time_minutes: 1
breadcrumb: [Deployment and synchronization integrations, Scan Engine integrations, Configure the Impact Store Application, Configuring Impact, Impact]
---

# Configure AES/AEMC integration properties

Configure the AES/AEMC integration to enforce automated Scan Engine compliance checks on custom app deployment requests from App Engine Studio and ServiceNow Studio.

## Before you begin

**Important:** Perform all steps in this task on the production controller instance only. Deployment pipelines within ServiceNow must already be configured before enabling this integration.

Deployment pipelines must already be configured in ServiceNow. No OAuth credentials or My SN Instances authentication are required, only a single My SN Instances record designating the production controller.

Role required: sn\_se.scan\_engine\_admin

## Procedure

1.  Switch the default pipeline subflow
2.  Navigate to **ALL** &gt; **App Engine** &gt; **Pipelines and Deployments** &gt; **Pipeline Types**.

3.  Open the default pipeline type record.

4.  Verify that **Deployment Pipeline** is set as the Application scope.

5.  Change **Subflow** to `SE App Deployment Pipeline` and save.

6.  Configure Scan Engine properties
7.  Navigate to **ALL** &gt; **Impact** &gt; **Configuration** &gt; **Scan Engine Properties** &gt; **My SN Instances** tab and select **New**.

8.  Create a single record with the following values:

    -   **Instance Name**: Must match the `instance_name` system property
    -   **Instance URL**
    -   **Environment: Production**
    -   **Authentication Type**: N/A \(leave blank\)
9.  Submit the form.

10. Return to **Scan Engine Properties** and select the **AES/AEMC Integration** tab.

11. Select **Enable AES/AEMC Integration \(Production Instance Only\)** to reveal additional configuration fields.

    If the checkbox does not appear, verify that the pipeline subflow was changed and the My SN Instances record was submitted correctly.

12. Configure approval conditions and scan timeout.

    |Setting|Default|
    |-------|-------|
    |Pass condition|Scan score of 100|
    |Scan timeout|10 minutes|


**Parent Topic:**[Deployment and synchronization integrations](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/impact/deployment-sync-integrations.md)

**Related topics**  


[Configure update set integration]()

