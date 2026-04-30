---
title: Microsoft purview endpoint storage configuration
description: Microsoft Purview endpoint evidence files storage configuration tells you where the endpoint evidence files are being stored by the purview- Custom managed store or Microsoft managed storage environments.
locale: en-US
release: yokohama
product: Data Loss Prevention
classification: data-loss-prevention
topic_type: concept
last_updated: "2025-04-23"
reading_time_minutes: 1
breadcrumb: [Create a new incident profile for Microsoft DLP integration, Data Loss Prevention Incident Response with Microsoft, DLP integrations, Data Loss Prevention Incident Response, Security Operations]
---

# Microsoft purview endpoint storage configuration

Microsoft Purview endpoint evidence files storage configuration tells you where the endpoint evidence files are being stored by the purview- Custom managed store or Microsoft managed storage environments.

In case of Microsoft managed store, Microsoft itself stores the evidence files in some location and for Custom managed store, you need to specify the container in which the evidence files will be stored by the purview when an alert gets generated.

Select either of the two storage types based on what is being configured at the purview end for the system to fetch the evidence files of the corresponding endpoint DLP incidents.

![Microsoft purview endpoint storage configuration.](../image/Microsoft-endpoint-storage.png)

**Note:** We recommend using the **Custom Managed Store** because Microsoft currently does not provide any APIs to retrieve evidence files from the **Microsoft Managed Store**. As a result, preview and download functionality is not supported for evidence stored in the Microsoft Managed Store. We have raised a case with Microsoft regarding this limitation.

**Parent Topic:**[Create a new incident profile for Microsoft DLP integration](../task/create-profile-microsoft-dlp-integration.md)

