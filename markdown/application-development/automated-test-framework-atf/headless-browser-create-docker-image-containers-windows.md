---
title: Create the Docker image and containers for Headless Browser setup in Microsoft Windows
description: Pull the Docker image from the Public Registry.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/zurich/application-development/automated-test-framework-atf/headless-browser-create-docker-image-containers-windows.html
release: zurich
product: Automated Test Framework \(ATF\)
classification: automated-test-framework-atf
topic_type: task
last_updated: "2025-07-31"
reading_time_minutes: 1
breadcrumb: [Headless Browser setup for Microsoft Windows, Headless Browser, Automated Test Framework \(ATF\), Testing and debugging applications, Building applications]
---

# Create the Docker image and containers for Headless Browser setup in Microsoft Windows

Pull the Docker image from the Public Registry.

## Before you begin

Complete Step 3: [Configure Docker for Headless Browser setup in Microsoft Windows](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/application-development/automated-test-framework-atf/headless-browser-configure-docker-windows.md)

Role required: admin on your ServiceNow instance and local administrator on the host machine.

## Procedure

1.  In an administrator command line, run `docker ps` to verify that Docker is working.

    Your results should look like this:

    \[Omitted image "verify-docker.png"\] Alt text: Command output to see if Docker is working

2.  Pull the latest Docker image from the GitHub repo [ATF Headless Runner](https://github.com/ServiceNow/atf-headless-runner/pkgs/container/atf-headless-runner).

    This command is an example, as these images are subject to change:

    `docker pull ghcr.io/servicenow/atf-headless-runner:win-1.0.0`

    **Note:** The instance-to-image compatibility makes sure that the automation script inside the Docker image is compatible with the instance code. Elements such as the user interface might change over time to support new features or upgrades.


**Parent Topic:**[Headless Browser setup for Microsoft Windows](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/application-development/automated-test-framework-atf/headless-browser-procedure-windows.md)

**Previous topic:**[Configure Docker for Headless Browser setup in Microsoft Windows](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/application-development/automated-test-framework-atf/headless-browser-configure-docker-windows.md)

**Next topic:**[Add secrets to Docker for Headless Browser setup in Microsoft Windows](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/application-development/automated-test-framework-atf/headless-browser-add-secrets-docker-windows.md)

