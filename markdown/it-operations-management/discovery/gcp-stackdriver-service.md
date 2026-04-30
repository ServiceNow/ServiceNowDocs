---
title: Configure the Google Cloud Logging service to auto-update the CMDB
description: You can activate the Google Cloud Logging \(formerly Stackdriver Logging\) service to auto-update Configuration Management Database \(CMDB\) configuration items \(CI\) data whenever Google Cloud Connector or your Google account makes a life-cycle state or configuration change to a Google Cloud Platform \(GCP\) resource. As a result, the CI data in the CMDB is updated without having to wait for Discovery to run.
locale: en-US
release: yokohama
product: Discovery
classification: discovery
topic_type: task
last_updated: "2025-11-25"
reading_time_minutes: 2
breadcrumb: [Discovery for Google Cloud Platform, Discovery for cloud environment, Discovery, ITOM Visibility, IT Operations Management]
---

# Configure the Google Cloud Logging service to auto-update the CMDB

You can activate the Google Cloud Logging \(formerly Stackdriver Logging\) service to auto-update Configuration Management Database \(CMDB\) configuration items \(CI\) data whenever Google Cloud Connector or your Google account makes a life-cycle state or configuration change to a Google Cloud Platform \(GCP\) resource. As a result, the CI data in the CMDB is updated without having to wait for Discovery to run.

## Before you begin

-   Activate Discovery and Service Mapping Patterns. For more information, see [Google Cloud Platform Discovery](../../service-mapping/reference/google-gcp-discovery-pattern.md).
-   Verify that Discovery has successfully discovered logical datacenters of the Google Cloud project. For more information, see [Set up a cloud account and service account for Google Cloud Platform](../../cloud-management-v2-setup/task/gcp-first-cld-and-srvc-accts.md).

    **Note:** Verify that you have selected the **Should pull events** check box in the Google Service Account page before you execute datacenter discovery.


Role required:

-   discovery\_admin for Cloud Discovery and `sn_cmp.cloud_event_integration` if authentication to cloud event endpoint is required. This role is required to set up an Alert Rule in the instance.
-   Google Cloud Platform administrator for configuration steps in the GCP console.
-   Logging Role for the Google Cloud Platform integration user that would allow OAuth scopes for the following

    -   `https://www.googleapis.com/auth/logging.admin`
    -   `https://www.googleapis.com/auth/cloud-platform.read-only`
    -   `https://www.googleapis.com/auth/cloud-platform`
    -   `https://www.googleapis.com/auth/logging.read`

## About this task

Discovery integrates with Google Cloud's Cloud Logging API to collect log data from resources in your Google Cloud projects. This integration enables Discovery to automatically update the CMDB based on log entries that reflect changes in your environment. The Cloud Logging service provides:

-   Centralized log collection for Google Cloud resources.
-   APIs to query and export logs for operational workflows.

When configured, Discovery pulls the Cloud Logging API at regular intervals to detect updates and synchronize them with the CMDB.

## Procedure

1.  Log in to your Google Cloud Platform account.

    For your project, navigate to **APIs &amp; Services** &gt; **Library**.

2.  Enable the **Cloud Logging API**.

    1.  In the library, search for `Cloud Logging`.

    2.  Select the **Cloud Logging API** card.

    3.  On the Cloud Logging API page, select **Enable**.

3.  To modify the schedule, navigate to **System Scheduler** &gt; **Scheduled Jobs** and then select **GCP-Events-job** and then update the **Repeat** setting as needed.

    ![Google Cloud Event Scheduler form](../../cloud-management-v2-setup/image/google-cloud-event-scheduler.png)

4.  Select **Update**.


## Result

-   Once the Google Cloud Platform generates an event and Discovery receives the event information, the 'GCP-Events-job' scheduled jobs execute in the background.

-   The scheduled job passes the event payload to the Identification and Reconciliation Engine \(IRE\). The IRE then takes the necessary actions to modify the state of the resources based on the event.


