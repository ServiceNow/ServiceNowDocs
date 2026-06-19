---
title: Non-persistent VDI monitoring configuration
description: Monitor non-persistent Virtual Desktop Infrastructures \(VDIs\) with Digital End-User Experience \(DEX\) so your organization can track performance issues and troubleshoot device and application performance.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/it-service-management/digital-end-user-experience-dex/monitoring-np-vdis.html
release: australia
product: Digital End-User Experience \(DEX\)
classification: digital-end-user-experience-dex
topic_type: concept
last_updated: "2026-03-12"
reading_time_minutes: 2
breadcrumb: [Configure, Digital End-User Experience, IT Service Management]
---

# Non-persistent VDI monitoring configuration

Monitor non-persistent Virtual Desktop Infrastructures \(VDIs\) with Digital End-User Experience \(DEX\) so your organization can track performance issues and troubleshoot device and application performance.

Non-persistent VDIs provide end users with a fresh desktop environment each time they log in. VDIs are a common choice for organizations requiring standardized and secure desktops, such as those in healthcare, education, or customer support.

When a VDI is initialized for the first time, it completes the standard registration process and downloads a certificate from the ServiceNow cloud. The certificate is then backed up to your persistent storage for future sessions.

During subsequent active sessions, the Agent Client Collector \(ACC\) continuously collects performance and usage data. Before a session ends, the logoff script pushes any residual metrics to the ServiceNow instance, helping avoid data loss. In subsequent sessions, the logon script restores the certificate from your persistent storage, enabling local authentication and eliminating the need to download certificates again. This process minimizes the load on the ServiceNow instance and supports efficient operation.

**Note:** DEX supports monitoring non-persistent VDIs on VMware. Multi-user sessions aren't supported.

## Benefits of monitoring non-persistent VDIs

Monitoring non-persistent VDIs with Digital End-User Experience provides the following benefits:

-   **Enhanced user experience**

    You can identify performance issues such as slow logging in, crashes, or sluggish application and device performance, even after the desktop session ends.

-   **Efficient troubleshooting**

    You can analyze device and application metrics data to pinpoint issues reported by employees, reducing guesswork in problem resolution.


## Configuration workflow

To enable monitoring on a non-persistent VDI pool, complete the following tasks on a reference device used to create the golden image.

1.  [Install Agent Client Collector on a non-persistent VDI reference device](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/it-service-management/digital-end-user-experience-dex/install-acc-on-np-vdi-golden-image.md). Install Agent Client Collector on the reference device using the MID-less installation method, configure non-persistent mode in `acc.yml`, and verify host data and policy synchronization.
2.  [Enable DEX browser extension](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/it-service-management/digital-end-user-experience-dex/enable-dex-browser-extension.md). Install the DEX browser extension on the reference device for monitoring web applications.
3.  [Prepare non-persistent VDI reference device](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/it-service-management/digital-end-user-experience-dex/prepare-np-vdi-golden-image.md). Remove the registration certificate, agent identifier, cached databases, and logs from the reference device, and update `acc.yml` so that each duplicate VDI registers with a unique identity.
4.  [Manage logon and logoff scripts for non-persistent VDIs](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/it-service-management/digital-end-user-experience-dex/configure-np-vdis.md). After you seal the reference device as the golden image and configure your VDI pool to use it, place the logon and logoff scripts in your VDI management tool and update the authentication steps to connect to your persistent storage.

For policy reference content for non-persistent VDIs, see [Non-persistent VDI parameters, scripts, and settings](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/it-service-management/digital-end-user-experience-dex/non-persistent-vdi-scripts.md).

