---
title: Configure Docker for Headless Browser setup in Microsoft Windows
description: Configure Docker Server to authenticate all requests.
locale: en-US
release: australia
product: Automated Test Framework \(ATF\)
classification: automated-test-framework-atf
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 1
breadcrumb: [Headless Browser setup for Microsoft Windows, Headless Browser for Automated Test Framework, Automated Test Framework \(ATF\), Testing and debugging applications, Building applications]
---

# Configure Docker for Headless Browser setup in Microsoft Windows

Configure Docker Server to authenticate all requests.

## Before you begin

Complete Step 2: [Generate certificates for Headless Browser setup for Microsoft Windows](headless-browser-certificates-windows.md)

Role required: admin on your ServiceNow instance and local administrator on the host machine.

## About this task

After creating your client and server keys, now you configure the Docker Server to authenticate all requests using those keys, and expose the Docker API on Port 2376.

## Procedure

1.  Configure Docker to use the certificates you generated in Step 2.

2.  Find or create the `C:\ProgramData\docker\config\daemon.json` file.

3.  Add the following properties to the daemon.json file.

    Be sure to replace items in these commands with the correct paths to your certificates:

    **Note:** The double slashes are important to copy exactly.

    ```
    {
    "tlscacert": "C:\\Users\\Administrator\\certs\\ca.pem",
    "tlscert": "C:\\Users\\Administrator\\certs\\server-cert.pem",
    "tlscert": "C:\\Users\\Administrator\\certs\\server-cert.pem",
    "tlskey": "C:\\Users\\Administrator\\certs\\server-key.pem",
    "tlsverify": true,
    "hosts": ["tcp://0.0.0.0:2376", "npipe://"]
    }
    ```

    To learn more, see [Configure the Docker daemon](https://docs.docker.com/config/daemon/#configure-the-docker-daemon).

4.  In administrator PowerShell, run `restart-service *docker*`


**Parent Topic:**[Headless Browser setup for Microsoft Windows](../concept/headless-browser-procedure-windows.md)

**Previous topic:**[Generate certificates for Headless Browser setup for Microsoft Windows](headless-browser-certificates-windows.md)

**Next topic:**[Create the Docker image and containers for Headless Browser setup in Microsoft Windows](headless-browser-create-docker-image-containers-windows.md)

