---
title: Install containerized OT Discovery components on Rocky 10
description: Install the containerized packages for the Discovery Console for OT and the OT Discovery Collector onto a machine with Rocky 10 OS.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/operational-technology/install-containerized-ot-discovery-rocky-10.html
release: australia
product: Operational Technology
classification: operational-technology
topic_type: task
last_updated: "2026-06-01"
reading_time_minutes: 1
breadcrumb: [Air-gapped networks and OT Discovery installation, Configure the Discovery Console for OT, Discovery Console for Operational Technology \(OT\), Operational Technology Native Discovery components, Operational Technology Discovery, Operational Technology]
---

# Install containerized OT Discovery components on Rocky 10

Install the containerized packages for the Discovery Console for OT and the OT Discovery Collector onto a machine with Rocky 10 OS.

## Before you begin

Role required: admin

## Procedure

1.  On your ServiceNow instance, navigate to the Service Graph Connector for ServiceNow Operational Technology \(OT\) Discovery Guided Setup page.

2.  Select **Get Started**.

    The **Download &amp; Deploy OT Discovery** page opens.

3.  In the first section of the setup, select **Download &amp; Deploy OT Discovery**.

4.  Select **Configure**.

    The **Downloads** page opens.

    **Note:** Review the End User License Agreement \(EULA\) and select **Agree** before proceeding. Consider moving these actions to separate steps.

5.  Download the containerized OT Discovery dependencies package and the installer package.

    **Note:** Download the OT Discovery Collector containerized package that is compatible with your machine's OS.

6.  Decompress the downloaded packages.

7.  Run the `Build the Offline Installer` script.

    This creates a ZIP archive that contains an offline installer that can be used in air-gapped networks.

8.  After the installer is complete, move the ZIP archive to the target system for installation.

9.  Decompress the offline installation archive.

10. Copy the required files:

    ```
    scp -r offline-console-init-support-files-main serviceadmin@<Console IP Address>:/home/serviceadmin
    ```

    ```
    scp -r OfflineConsoleInstaller serviceadmin@<Console IP Address>:/home/serviceadmin
    ```

    ```
    serviceadmin //@<password>
    ```

    ```
    ssh serviceadmin@<Console IP Address>
    ```

11. Install Podman:

    ```
    dnf install -y zip podman
    ```

12. Set up the latest version of Docker:

    1.  Update system:

        ```
        sudo dnf update -y
        ```

    2.  Install the dnf plugins package, which is required for config-manager:

        ```
        sudo dnf install -y dnf-plugins-core.
        ```

    3.  Add the official Docker repo: ``.

        ```
        sudo dnf config-manager --add-repo https://download.docker.com/linux/centos/docker-ce.repo
        ```

13. Install Docker.

    ```
    sudo dnf install -y docker-ce docker-ce-cli containerd.io docker-buildx-plugin docker-compose-plugin
    dnf install -y which
    
    ```

14. Unzip the Discovery Console for OT dependencies package and build the containers for RabbitMQ and MongoDB:

    ```
    chmod +x build-rabbit-and-mongo-images.sh
    ./build-rabbit-and-mongo-images.sh
    
    ```

15. Copy the RabbitMQ and MongoDB containers into the Installer folder:

    ```
    sudo cp offline-console-mongodb_latest.tar.gz offline-console-rabbitmq_latest.tar.gz
    /home/serviceadmin/OfflineConsoleInstaller/OCI_compliant_images/
    
    ```

16. Install the offline console:

    ```
    chmod +x offline-console-init.sh
    ./offline-console-init.sh
    
    ```


