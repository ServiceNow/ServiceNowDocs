---
title: Run Certificate Discovery via certificate file import
description: In Certificate Inventory and Management, you can discover certificates by importing certificate files into the system using pattern-based Discovery.
locale: en-US
release: yokohama
product: Discovery
classification: discovery
topic_type: task
last_updated: "2025-08-04"
reading_time_minutes: 1
breadcrumb: [Visibility to TLS certificates, Configuring Certificate Inventory and Management, Certificate Inventory and Management, ITOM Visibility, IT Operations Management]
---

# Run Certificate Discovery via certificate file import

In Certificate Inventory and Management, you can discover certificates by importing certificate files into the system using pattern-based Discovery.

## Before you begin

Ensure that **TLS\_keepOriginalCertificate** is set to **False**.

Ensure the certificate is in one of the following formats: .cert, .pem, .txt, .der.

Role required: discovery\_admin or admin

## About this task

The import certificates are discovered using the Import SSL Certificate pattern, which relies on the following parameters:

-   Server: The host name or IP address where the certificates are hosted. If importing from the MID Server, specify localhost and leave temp\_certificate\_folder empty.
-   server\_certificates\_folder: The folder path on the server containing the certificates.
-   TLS\_keepOriginalCertificate parameter: Set to false to avoid potential out-of-memory issues due to increased payload size.
-   temp\_certificates\_folder: Temporary folder on the MID Server where the files are copied.

## Procedure

1.  Create a Discovery schedule with the following fields.

    For more information on setting up your Discovery schedules, see [Schedule a horizontal discovery](t_CreateADiscoverySchedule.md).

    1.  Select **Discovery**: **Import Certificates**

    2.  Select **Certificate Discovery Type**: **Import Certificates**.

    3.  Select **MID Server selection method**: **Specific MID Server**.

    4.  Select **MID Server**: Select the preferred MID Server.

    5.  Add the credentials for the Windows or Linux host machine where the certificates are located.

    6.  Fill out any other necessary fields.

    7.  Select **Save**.

2.  To add the Import SSL Certificate pattern, from the **Serverless Execution pattern** tab, select **New**.


## Result

When your Discovery schedule runs, it then automatically scans your files.

