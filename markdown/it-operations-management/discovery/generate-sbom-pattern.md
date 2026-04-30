---
title: Download a software bill of materials \(SBOM\)
description: Download a software Bill of Materials \(SBOM\) to gain visibility to the components of the container image such as the operating system packages that are installed.
locale: en-US
release: xanadu
product: Discovery
classification: discovery
topic_type: task
last_updated: "2024-08-01"
reading_time_minutes: 1
keywords: [SBOM, Pattern, Container Image, Docker, Kubernetes, Discovery]
breadcrumb: [Container image scanning for software decomposition, Kubernetes discovery using patterns, Container discovery, Discovery, ITOM Visibility, IT Operations Management]
---

# Download a software bill of materials \(SBOM\)

Download a software Bill of Materials \(SBOM\) to gain visibility to the components of the container image such as the operating system packages that are installed.

## Before you begin

The SBOM must have been configured. For more information, see [Configure the SBOM generation](../task/enable-sbom.md).

Role required: discovery\_admin

## Procedure

1.  In the navigation filter, type `sn_itom_pattern_container_image_scan_status_list.do`.

2.  Choose the image for which you need the SBOM in the Container Image Scan Status list.

    If the scan status is **None** rather than **Scanned**, wait for the status to change before selecting the image record.

3.  Download the SBOM by selecting **download** in the **Manage attachments** section.


