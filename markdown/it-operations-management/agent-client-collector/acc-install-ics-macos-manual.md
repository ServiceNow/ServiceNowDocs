---
title: Install MID-less Agent Client Collector manually in a macOS environment
description: Install MID-less Agent Client Collector manually on a macOS machine to enable sending data from the agent to the instance through the cloud. Sending information through the cloud allows the MID Server to be used for more persistent resources.
locale: en-US
release: australia
product: Agent Client Collector
classification: agent-client-collector
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 2
breadcrumb: [Installing MID-less ACC, Configuring MID-less ACC, ACC deployment - endpoints, Configuring Agent Client Collector, Agent Client Collector, IT Operations Management]
---

# Install MID-less Agent Client Collector manually in a macOS environment

Install MID-less Agent Client Collector manually on a macOS machine to enable sending data from the agent to the instance through the cloud. Sending information through the cloud allows the MID Server to be used for more persistent resources.

## Before you begin

-   Install the ITOM Cloud Services Core \(sn\_itom\_cloud\_svc\) plugin.
-   Onboard your instance to use ITOM Cloud Services. For details, contact Customer Support.
-   Configure an agent registration key. For details, see [Configure an agent registration key](agent-registration-key-configuration.md).
-   Role required: agent\_client\_collector\_admin

## About this task

For details on sending data through the cloud in a MID-less deployment, see [DEX Architecture](https://www.servicenow.com/docs/access?context=dex-architecture&version=australia&pubname=australia-it-service-management&ft:locale=en-US).

## Procedure

1.  Download the installation files to your local machine.

    ```
    curl -L <download link from the Agent Downloads page on the instance>
    ```

2.  Validate the installation file signature.

    ```
    pkgutil --check-signature agent-client-collector-<version number>-macos-catalina_x64.pkg
    ```

    **Note:** Ensure that the `pkg` certificate chain has the ServiceNow developer ID installer certificate.

3.  Install the Agent Client Collector package.

    ```
    sudo installer -pkg agent-client-collector-<version number>-macos-catalina_x64.pkg -target /
    ```

4.  Copy the installation files.

    1.  Sample configuration file:

        `sudo cp -p /Library/Application\ Support/servicenow/agent-client-collector/acc.yml.example /Library/Application\ Support/servicenow/agent-client-collector/acc.yml`

    2.  Sample allow list file:

        `sudo cp -p /Library/Application\ Support/servicenow/agent-client-collector/check-allow-list.json.default /Library/Application\ Support/servicenow/agent-client-collector/check-allow-list.json`

5.  To create new check definitions to be included in the allow list, first disable the allow list by commenting out the **allow-list** parameter in the `acc.yml` file.

    `sudo -H -u _servicenow vi /Library/Application\ Support/servicenow/agent-client-collector/acc.yml`

    **Note:** This action compromises your system's security and is recommended only as a temporary measure until you finish updating the allow list. After completing the update, uncomment the allow list parameter in the configuration file to re-activate the allow list.

    For details on adding custom checks to an allow list, see [Generate an Agent Client Collector allow list](acc-generate-allow-list.md).

6.  In the `acc.yml` configuration file:

    1.  Set the following parameters:

        |Parameter|Value|
        |---------|-----|
        |backend-url|"&lt;gateway URL&gt;"|
        |connect-without-mid|true|
        |instance-url|"&lt;instance URL&gt;"|
        |registration-key|"&lt;regsitration-key&gt;"|
        |insecure-skip-tls-verify|false|

    2.  Comment out the **api-key** parameter.

7.  Save the configuration file.

8.  To ensure that the configuration file points to a valid endpoint, run the following commands to restart the Agent Client Collector:

    ```
    sudo launchctl unload -w /Library/LaunchDaemons/com.sn.acc.plist
    sudo launchctl load -w /Library/LaunchDaemons/com.sn.acc.plist
    ```

    **Note:** By default, exiting the installation program causes the program to restart immediately. To ensure that the program remains stopped after exiting, set the KeepAlive property in the `/Library/LaunchDaemons/com.sn.acc.plist` file to **false**.


**Parent Topic:**[Installing MID-less Agent Client Collector](../concept/acc-itom-cloud-services.md)

