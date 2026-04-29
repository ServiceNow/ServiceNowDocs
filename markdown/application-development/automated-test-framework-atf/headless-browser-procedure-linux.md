---
title: Headless Browser setup for Linux
description: The ServiceNow Headless Browser for Automated Test Framework provides automation so you can skip having to manually open a browser during testing. The Headless Browser setup is available in both Linux and Microsoft Windows. This topic covers the setup for Linux.
locale: en-US
release: australia
product: Automated Test Framework \(ATF\)
classification: automated-test-framework-atf
topic_type: concept
last_updated: "2026-03-12"
reading_time_minutes: 3
breadcrumb: [Headless Browser for Automated Test Framework, Automated Test Framework \(ATF\), Testing and debugging applications, Building applications]
---

# Headless Browser setup for Linux

The ServiceNow® Headless Browser for Automated Test Framework provides automation so you can skip having to manually open a browser during testing. The Headless Browser setup is available in both Linux and Microsoft Windows. This topic covers the setup for Linux.

**Important:** Headless Browser is a legacy feature of ATF; it is recommended to instead use the ATF Test Generator and Cloud Runner application. Cloud Runner offers you an easy setup and a seamless user experience. You can install [Cloud Runner](https://store.servicenow.com/sn_appstore_store.do#!/store/application/db1676d7421441106f046193880e0b37) from the store app.

If you are an on-premise instance user, you must continue using the Headless Browser option. Cloud Runner is not currently available for on-premise instances.

There are several sequential procedures to follow in the one-time setup.

## Prerequisites

**Note:** MFA must be disabled in your instance to use the Headless Browser option.

Role required: admin on your ServiceNow instance and local administrator on the host machine.

-   Install the [Docker application](https://docs.docker.com/engine/install/)
-   Install Java Runtime Environment \(JRE\) 1.8 - required for keytool utility

    **Note:** The version must be Java 1.8, or errors result in your ServiceNow instance when trying to validate the certificate created with the keytool utility. To learn more, see [Create encryption keys using the Java KeyStore keytool](https://www.servicenow.com/docs/access?context=t_CreateEncryptionKeys&version=australia&pubname=australia-platform-security&ft:locale=en-US).

-   Install OpenSSL
-   Two-way communication

    -   There must be two-way communication between the instance URL and your server.
    -   Find the IP address of your server and get your hostname. You can use one or both of them, but you need at least one. Make sure the address or hostname are visible from your ServiceNow instance.
    -   See [My IP Address](https://support.servicenow.com/now/en/pages/automation-store?id=ns_automation_store&catalog_sys_id=b85d23ae6f086100a5117357ea3ee4f3) to find the IP address ranges of your instance. You can then configure your server to allow inbound access to all of the indicated IP addresses/ranges.
    -   Use Port 2376 or your own default port for this procedure. Make sure your server's firewall rules allow inbound requests on this port from the IP addresses you get from the instance.
    **Note:** If you don't have a hostname and are connecting via the IP address, you can enter the IP address and put "localhost" in the Hostname environment variable.


## Steps to set up the Headless Browser for Linux

Follow these six steps \(plus verification\) to set up the Headless Browser for Linux.

1.  [Generate certificates for Headless Browser setup for Linux](../task/headless-browser-certificates.md)  
Generate TLS/SSL certificates to secure the Docker REST API and authenticate HTTP requests.
2.  [Configure Docker for Headless Browser setup in Linux](../task/headless-browser-configure-docker.md)  
Complete Step 2 in the Linux setup for the ServiceNow® Headless Browser for ATF: Configure Docker Server to authenticate all requests.
3.  [Create the Docker image and containers for Headless Browser setup in Linux](../task/headless-browser-create-docker-image-containers.md)  
Pull the Docker image from the Public Registry.
4.  [Add secrets to Docker for Headless Browser setup in Linux](../task/headless-browser-add-secrets-docker.md)  
Create a Docker secret, which stores the password of the ServiceNow user who will log into the instance to execute the tests. Docker Secrets is a feature of ServiceNow® for securely storing the passwords that will be used in containers.
5.  [Set up instance for Headless Browser in Linux](../task/headless-browser-instance-setup.md)  
Step 5 in the Linux setup for the ServiceNow® Headless Browser for ATF: Set up your instance so it can support the Headless Browser.
6.  [Configure ATF for Headless Browser in Linux](../task/headless-browser-configure-atf.md)  
Step 6 in the Linux setup for the ServiceNow® Headless Browser for ATF: Configure ATF with properties.
7.  [Verify Headless Browser procedures in Linux](../task/headless-browser-verify-tests.md)  
Step 7, the final step in the Linux setup for the ServiceNow® Headless Browser for ATF: Verify that your Headless Browser setup procedures are successful.

**Parent Topic:**[Headless Browser for Automated Test Framework](atf-headless-browser.md)

