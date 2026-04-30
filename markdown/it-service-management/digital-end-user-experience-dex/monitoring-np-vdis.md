---
title: Monitoring non-persistent VDIs
description: Monitoring non-persistent Virtual Desktop Infrastructures \(VDIs\) with Digital End-User Experience \(DEX\) enables your organization to track performance issues and troubleshoot efficiently.
locale: en-US
release: yokohama
product: Digital End-User Experience \(DEX\)
classification: digital-end-user-experience-dex
topic_type: concept
last_updated: "2025-10-03"
reading_time_minutes: 1
breadcrumb: [DEX administration, Configure, Digital End-User Experience, IT Service Management]
---

# Monitoring non-persistent VDIs

Monitoring non-persistent Virtual Desktop Infrastructures \(VDIs\) with Digital End-User Experience \(DEX\) enables your organization to track performance issues and troubleshoot efficiently.

Non-persistent VDIs provide end users with a fresh desktop environment each time they log in. VDIs are an attractive choice for organizations requiring standardized and secure desktops, such as those in healthcare, education, or customer support.

When a VDI is initialized for the first time, it completes the standard registration process and downloads a certificate from the ServiceNow cloud. The certificate is then backed up to the persistent storage for future sessions.

During subsequent active sessions, the Agent Client Collector \(ACC\) continuously collects performance and usage data. Before a session ends, the log-off script pushes any residual metrics to the ServiceNow cloud, helping to prevent data loss. In subsequent sessions, the log-on script restores the certificate from persistent storage, enabling local authentication and eliminating the need to download certificates again. This process minimizes the load on the ServiceNow instance and promotes efficient operation.

## Benefits of monitoring non-persistent VDIs

Monitoring non-persistent VDIs with Digital End-User Experience addresses these challenges by enabling the following.

-   **Enhanced user experience**

    You can identify performance issues such as slow logging in, crashes, or sluggish application and device performance, even after the desktop session has ended.

-   **Efficient troubleshooting**

    You can analyze device and application metrics data to pinpoint issues reported by employees, reducing guesswork in problem resolution.


