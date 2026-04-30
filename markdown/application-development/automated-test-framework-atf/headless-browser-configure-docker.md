---
title: Configure Docker for Headless Browser setup in Linux
description: Complete Step 2 in the Linux setup for the ServiceNow Headless Browser for ATF: Configure Docker Server to authenticate all requests.
locale: en-US
release: zurich
product: Automated Test Framework \(ATF\)
classification: automated-test-framework-atf
topic_type: task
last_updated: "2025-07-31"
reading_time_minutes: 2
breadcrumb: [Headless Browser setup for Linux, Headless Browser, Automated Test Framework \(ATF\), Testing and debugging applications, Building applications]
---

# Configure Docker for Headless Browser setup in Linux

Complete Step 2 in the Linux setup for the ServiceNow® Headless Browser for ATF: Configure Docker Server to authenticate all requests.

## Before you begin

Complete Step 1: [Generate certificates for Headless Browser setup for Linux](headless-browser-certificates.md)

This task: After creating your client and server keys as directed in Step 1, now you configure the Docker Server to authenticate all requests using those keys, and expose the Docker API on Port 2376.

Role required: admin on your ServiceNow instance and local administrator on the host machine.

## Procedure

1.  Configure Docker to use the certificates that you generated in Step 1.

    1.  Find or create the /etc/docker/daemon.json file. You can run: `touch /etc/docker/daemon.json`
    2.  Edit the daemon.json file and add the following JSON values. Be sure to replace with the correct paths to your certificates:

        ```
        {
        "debug": true,
        "tlscacert": "<path to your certificates>/ca.pem",
        "tlscert": "<path to your certificates>/server-cert.pem",
        "tlskey": "<path to your certificates>/server-key.pem",
        "tlsverify": true
        }
        
        ```

    To learn more, see [Configure the Docker daemon](https://docs.docker.com/config/daemon/#configure-the-docker-daemon).

2.  Configure Docker to expose the remote API on a port \(Port 2376 is suggested\).

    You can configure Docker to accept remote connections with the docker.service systemd unit file for Linux distributions using **systemd**, such as recent versions of RedHat, CentOS, Ubuntu and SLES, or with the daemon.json file, which is suggested for Linux distributions that do not use systemd.

    If using **systemd \(systemctl\)**:

    1.  Use the command `sudo systemctl edit docker.service` to open an override file for docker.service in a text editor.
    2.  Add or modify the following lines, substituting your own port if not using 2376.

        ```
        [Service]
        ExecStart=
        ExecStart=/usr/bin/dockerd -H tcp://0.0.0.0:2376
        ```

    3.  Save the file.
    4.  Reload the systemctl configuration.

        `sudo systemctl daemon-reload`

    5.  Restart Docker

        `sudo systemctl restart docker.service`

3.  To enable Docker access for the current user via a command line, copy certificates to the user's Docker home directory:

    -   `mkdir -pv ~/.docker`
    -   `cp ca.pem ~/.docker`
    -   `cp client-key.pem ~/.docker/key.pem`
    -   `cp client-cert.pem ~/.docker/cert.pem`
4.  Set DOCKER\_HOST and DOCKER\_TLS\_VERIFY environment variables for your user:

    -   `echo "export DOCKER_HOST=tcp://${SERVERIP}:2376 DOCKER_TLS_VERIFY=1" >> ~/.bash_profile`
    -   `source ~/.bash_profile`
    To learn more, see [Manage Docker as a non-root user](https://docs.docker.com/engine/install/linux-postinstall/#manage-docker-as-a-non-root-user).


**Parent Topic:**[Headless Browser setup for Linux](../concept/headless-browser-procedure-linux.md)

**Previous topic:**[Generate certificates for Headless Browser setup for Linux](headless-browser-certificates.md)

**Next topic:**[Create the Docker image and containers for Headless Browser setup in Linux](headless-browser-create-docker-image-containers.md)

