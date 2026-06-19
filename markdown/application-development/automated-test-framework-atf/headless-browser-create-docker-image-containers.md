---
title: Create the Docker image and containers for Headless Browser setup in Linux
description: Pull the Docker image from the Public Registry.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/application-development/automated-test-framework-atf/headless-browser-create-docker-image-containers.html
release: australia
product: Automated Test Framework \(ATF\)
classification: automated-test-framework-atf
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 1
breadcrumb: [Headless Browser setup for Linux, Headless Browser for Automated Test Framework, Automated Test Framework \(ATF\), Testing and debugging applications, Building applications]
---

# Create the Docker image and containers for Headless Browser setup in Linux

Pull the Docker image from the Public Registry.

## Before you begin

Complete Step 2: [Configure Docker for Headless Browser setup in Linux](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/application-development/automated-test-framework-atf/headless-browser-configure-docker.md)

Role required: admin on your ServiceNow instance and local administrator on the host machine.

## Procedure

1.  In the command line, run `docker ps` to verify that Docker is working.

    Your results should look like this:

    \[Omitted image "verify-docker.png"\] Alt text: Command output to see if Docker is working

2.  Pull the latest Docker image from the GitHub repo [ATF Headless Runner](https://github.com/ServiceNow/atf-headless-runner/pkgs/container/atf-headless-runner).

    This command is an example, as these images are subject to change.

    `docker pull ghcr.io/servicenow/atf-headless-runner:lin-1.0.0`

    **Note:** The instance-to-image compatibility makes sure that the automation script inside the Docker image is compatible with the instance code. Elements such as the user interface might change over time to support new features or upgrades.


**Parent Topic:**[Headless Browser setup for Linux](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/application-development/automated-test-framework-atf/headless-browser-procedure-linux.md)

**Previous topic:**[Configure Docker for Headless Browser setup in Linux](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/application-development/automated-test-framework-atf/headless-browser-configure-docker.md)

**Next topic:**[Add secrets to Docker for Headless Browser setup in Linux](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/application-development/automated-test-framework-atf/headless-browser-add-secrets-docker.md)

