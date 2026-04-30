---
title: Headless Browser setup for Microsoft Windows
description: The ServiceNow Headless Browser for Automated Test Framework \(ATF\) provides automation so you can skip having to manually open a browser during testing. The Headless Browser setup is available in both Linux and Microsoft Windows. This topic covers the setup for Windows.
locale: en-US
release: zurich
product: Automated Test Framework \(ATF\)
classification: automated-test-framework-atf
topic_type: concept
last_updated: "2025-07-31"
reading_time_minutes: 3
breadcrumb: [Headless Browser, Automated Test Framework \(ATF\), Testing and debugging applications, Building applications]
---

# Headless Browser setup for Microsoft Windows

The ServiceNow® Headless Browser for Automated Test Framework \(ATF\) provides automation so you can skip having to manually open a browser during testing. The Headless Browser setup is available in both Linux and Microsoft Windows. This topic covers the setup for Windows.

**Important:** Headless Browser is a legacy feature of ATF; it is recommended to instead use the ATF Test Generator and Cloud Runner application. Cloud Runner offers you an easy setup and a seamless user experience. You can install [Cloud Runner](https://store.servicenow.com/sn_appstore_store.do#!/store/application/db1676d7421441106f046193880e0b37) from the store app.

If you are an on-premise instance user, you must continue using the Headless Browser option. Cloud Runner is not currently available for on-premise instances.

There are several sequential procedures to follow in the one-time setup. Below are the instructions for the Microsoft Windows setup.

## Prerequisites

**Note:** MFA must be disabled in your instance to use the Headless Browser option.

Role required: admin on your ServiceNow instance and local administrator on the host machine.

**Warning:** The only supported version of Microsoft Windows as a host is Windows Server 2019 v10.0.17763.737. No other versions are supported. If you are unable to meet these requirements, a Linux host is recommended.

-   Make sure that the following programs are installed on your Windows server:
    -   Docker: [Install Docker for Headless Browser setup for Microsoft Windows](../task/headless-browser-install-docker.md)
    -   Java keytool: [Chocolatey tool for javaruntime](https://community.chocolatey.org/packages/javaruntime)
    -   OpenSSL: [Chocolatey tool for openssl](https://community.chocolatey.org/packages/openssl)
-   Two-way communication

    -   There must be two-way communication between the instance URL and your server.
    -   Find the IP address of your server and get your hostname. You can use one or both of them, but you need at least one. Make sure the address or hostname are visible from your ServiceNow instance.
    -   See [My IP Address](https://support.servicenow.com/now/en/pages/automation-store?id=ns_automation_store&catalog_sys_id=b85d23ae6f086100a5117357ea3ee4f3) to find the IP address ranges of your instance. You can then configure your server to allow inbound access to all of the indicated IP addresses/ranges.
    -   Use Port 2376 or your own default port for this procedure. Make sure your server's firewall rules allow inbound requests on this port from the IP addresses you get from the instance.
    **Note:** If you don't have a hostname and are connecting via the IP address, you can enter the IP address and put "localhost" in the Hostname environment variable.

-   To learn more, see [Use TLS \(HTTPS\) to protect the Docker daemon socket](https://docs.docker.com/engine/security/protect-access/#:~:text=Use%20TLS%20(HTTPS)%20to%20protect,to%20a%20trusted%20CA%20certificate.).

## Steps to set up the Headless Browser for Windows

Follow these seven steps \(plus verification\) to set up the Headless Browser for Windows.

1.  [Install Docker for Headless Browser setup for Microsoft Windows](../task/headless-browser-install-docker.md)  
Step 1 in the Windows setup for the ServiceNow® Headless Browser for Automated Test Framework: Install Docker.
2.  [Generate certificates for Headless Browser setup for Microsoft Windows](../task/headless-browser-certificates-windows.md)  
Generate TLS/SSL certificates to secure the Docker REST API and authenticate HTTP requests.
3.  [Configure Docker for Headless Browser setup in Microsoft Windows](../task/headless-browser-configure-docker-windows.md)  
Configure Docker Server to authenticate all requests.
4.  [Create the Docker image and containers for Headless Browser setup in Microsoft Windows](../task/headless-browser-create-docker-image-containers-windows.md)  
Pull the Docker image from the Public Registry.
5.  [Add secrets to Docker for Headless Browser setup in Microsoft Windows](../task/headless-browser-add-secrets-docker-windows.md)  
Create a Docker secret that stores the password of the ServiceNow user who will log into the instance to execute the tests. Docker Secrets is a feature of ServiceNow® for securely storing the passwords that will be used in containers.
6.  [Set up instance for Headless Browser in Microsoft Windows](../task/headless-browser-instance-setup-windows.md)  
Step 6 in the Microsoft Windows setup for the ServiceNow® Headless Browser for ATF: Set up your instance so it can support the Headless Browser.
7.  [Configure Automated Test Framework \(ATF\) for Headless Browser in Microsoft Windows](../task/headless-browser-configure-atf-windows.md)  
Step 7 in the Microsoft Windows setup for the ServiceNow® Headless Browser for ATF: Configure ATF with properties.
8.  [Verify Headless Browser procedures for ATF in Microsoft Windows](../task/headless-browser-verify-tests-windows.md)  
Verify that your Headless Browser setup procedures have been successful.

**Parent Topic:**[Headless Browser for Automated Test Framework](atf-headless-browser.md)

