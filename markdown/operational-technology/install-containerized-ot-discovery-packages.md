---
title: Install containerized OT Discovery packages
description: Install the OT Discovery containerized packages on your network.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/operational-technology/install-containerized-ot-discovery-packages.html
release: australia
product: Operational Technology
classification: operational-technology
topic_type: task
last_updated: "2026-06-01"
reading_time_minutes: 1
breadcrumb: [Air-gapped networks and OT Discovery installation, Configure the Discovery Console for OT, Discovery Console for Operational Technology \(OT\), Operational Technology Native Discovery components, Operational Technology Discovery, Operational Technology]
---

# Install containerized OT Discovery packages

Install the OT Discovery containerized packages on your network.

## Before you begin

Role required: admin

## About this task

To help meet the air-gapped challenge, ServiceNow provides containerized versions of the Discovery Console for OT and the OT Discovery Collector. The Discovery Sensor for OT package has everything it needs and can be installed as is to an air-gapped network. The following steps cover installation of the containerized Console and Collector packages.

## Procedure

1.  On your ServiceNow instance, navigate to the Service Graph Connector for ServiceNow Operational Technology \(OT\) Discovery Guided Setup page.

2.  Select **Get Started**.

    The **Download &amp; Deploy OT Discovery** page opens.

3.  In the first section of the setup, select **Download &amp; Deploy OT Discovery**.

4.  Select **Configure** and the **Downloads** page opens.

5.  Read the End User License Agreement \(EULA\) carefully and then check **Agree**.

6.  Download the containerized OT Discovery dependencies package and the installer package.

    **Note:** Download the OT Discovery Collector containerized package that is compatible with your machine's OS.

7.  Decompress the downloaded packages.

    **Note:** In case you're installing on a Debian OS, install Docker for Debian OS. For instructions, see [Install Docker Engine on Debian](https://docs.docker.com/engine/install/debian/)

8.  Set up the latest version of docker:

    ```
    sudo apt install docker-ce docker-ce-cli containerd.io docker-buildx-plugin docker-compose-plugin
    ```

9.  Run the `build-rabbit-and-mongo-images.sh`.

    ```
    chmod +x build-rabbit-and-mongo-images.sh
    	./build-rabbit-and-mongo-images.sh
    
    ```

    This builds the containers for RabbitMQ and MongoDB.

10. Copy the RabbitMQ and MongoDB containers into the `OCI_compliant_images` directory.

    ```
    sudo cp offline-console-mongodb_latest.tar.gz offline-console-rabbitmq_latest.tar.gz
    /home/serviceadmin/OfflineConsoleInstaller/OCI_compliant_images/
    
    ```

11. Copy the RabbitMQ and MongoDB containers into the Installer folder.

12. Install Podman:

    ```
    sudo apt install podman podman-compose
    ```

13. Install the offline console:

    ```
    chmod +x offline-console-init.sh
    ./offline-console-init.sh
    
    ```


