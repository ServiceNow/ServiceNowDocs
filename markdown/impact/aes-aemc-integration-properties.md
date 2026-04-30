---
title: AES/AEMC integration properties
description: The AES/AEMC integration provides automated governance for custom application deployments by validating the scoped applications against admin-defined conditions before approval. When a developer submits a deployment request from App Engine Studio or ServiceNow Studio, the system automatically runs compliance checks using the Scan Engine to ensure all required rules are met. If the are not, it blocks the deployment.
locale: en-US
release: zurich
topic_type: concept
last_updated: "2025-11-04"
reading_time_minutes: 3
breadcrumb: [Scan Engine integrations, Scan Engine, Platform Health, Using Impact, Impact]
---

# AES/AEMC integration properties

The AES/AEMC integration provides automated governance for custom application deployments by validating the scoped applications against admin-defined conditions before approval. When a developer submits a deployment request from App Engine Studio or ServiceNow Studio, the system automatically runs compliance checks using the Scan Engine to ensure all required rules are met. If the are not, it blocks the deployment.

**Note:** Configuration of deployment pipelines is beyond the scope of this topic. The information in this topic assumes that the deployment pipelines within ServiceNow are configured. For information on configuring deployment pipelines, refer to [Configure Pipelines and Deployments](https://www.servicenow.com/docs/csh?topicname=config-p-and-d.html&version=latest).

Integrating Scan Engine with App Engine Studio, ServiceNow Studio, or Pipelines and Deployments requires you to perform two procedures:

-   Switching the default pipeline subflow
-   Configuring Scan Engine properties for AES/AEMC integration

**Note:** The following procedures will be performed only within the production controller which is part of the deployment pipeline.

## Switching the Default Pipeline Subflow

Perform the following procedure to select the Scan Engine subflow:

1.  Navigate to **ALL** &gt; **App Engine** &gt; **Pipelines and Deployments** &gt; **Pipeline Types**.
2.  Open the default pipeline type record by selecting its `name` in the Label column.
3.  Select the link to edit the record.
4.  Ensure **Deployment Pipeline** is set as the **Application** scope.
5.  Change the **Subflow** to **SE App Deployment Pipeline**.
6.  Save the changes to the form.

## Configuring Scan Engine Properties for AES/AEMC integration

Once the default pipeline subflow has been switched to the Scan Engine pipeline subflow, you then need to configure the Scan Engine for AES/AEMC integration by performing the following procedure:

1.  Navigate to **ALL &gt; Impact &gt; Configuration &gt; Scan Engine Properties**.
2.  From the related lists at the bottom of the form, select the **My SN Instances** tab.
3.  Create a single record to designate this instance as the production controller instance by first selecting **New**.
4.  Fill in the following required and optional fields:
    1.  **Instance Name** should match the `instance_name` system property.
    2.  **Instance URL** is the URL of the production controller instance.
    3.  **Environment** should be set to **Production**.
    4.  No additional information is needed. Submit the form without setting up an **Authentication Type**.
5.  When you return to the Scan Engine Properties page, select the **AES/AEMC Integration** tab in the middle of the form.
6.  Ensure that the **Enable AES/AEMC Integration \(Production Instance Only\)** field is enabled. If it is not, check that steps 1-6 were performed correctly.
7.  Select the **Enable AES/AEMC Integration \(Production Instance Only\)** check-box to reveal additional fields.
8.  You can keep the default values or enter new ones.
9.  Specify the conditions for which an application is considered "approved" to proceed to the first phase of the deployment pipeline.
10. Specify the maximum amount of time an application scan should be allowed to complete before being rejected due to a timeout.

Once configuration is complete, regular application submissions will now include an application scan as part of the deployment pipeline.

## Conditions for approving an application scan

When an application is submitted from App Engine Studio or ServiceNow Studio, the integration will begin a full scan of the application that is being submitted for deployment. The conditions specified in the Scan Engine Properties page determine the approval criteria for whether application scans continue on to the deployment pipeline. When the application scan completes and the conditions are met, the application moves to the next stage of the deployment process, usually a group approval.

If the conditions are not met, the deployment request is rejected. An email message is sent to the author of the application with details of the application scan.

The conditions used are configured by the administrator.

## Application scan timeout \(minutes\)

Application scans through the Scan Engine are usually relatively short. Ten minutes is the default value. If a scan fails to complete within ten minutes, the deployment request will be rejected and information about the rejection will be added to the request record.

Shorter or longer scan times can be configured by the administrator.

