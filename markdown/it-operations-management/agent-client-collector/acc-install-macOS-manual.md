---
title: Manually install Agent Client Collector on macOS
description: Install Agent Client Collector manually on a machine that uses macOS when the agent is not connected to the instance or you want enhanced customization options.
locale: en-US
release: yokohama
product: Agent Client Collector
classification: agent-client-collector
topic_type: task
last_updated: "2025-01-30"
reading_time_minutes: 2
breadcrumb: [Agent Client Collector installation on macOS system, Configuring Agent Client Collector Framework, Agent Client Collector Framework, Agent Client Collector, IT Operations Management]
---

# Manually install Agent Client Collector on macOS

Install Agent Client Collector manually on a machine that uses macOS when the agent is not connected to the instance or you want enhanced customization options.

## Before you begin

-   Ensure that you have configured the Agent Client Collector web server.
-   Verify that your server's OS and version matches the list of supported OS versions as described in [Agent Client Collector installation](../concept/acc-installation.md).
-   Navigate to **Agent Client Collector** &gt; **Deployment** &gt; **Agent Downloads** and download the signed `.pkg` relevant for your OS.
-   Store the `.pkg` installation package on one of your installed agents.

Role required: agent\_client\_collector\_admin

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

6.  Save the configuration file.

7.  In the configuration file, connect the agent with the MID Server.

    1.  Set the MID Server connection.

        ```
        "wss://<MID Server IP>:<Web Socket Port>/ws/events"
        ```

        The web socket port was configured on the MID Server when it was set as an Agent Client Collector listener.

    2.  Locate the **api-key** parameter and specify the API key value inside double quotation marks, as follows:

        **api-key:"111111111"**

        The specified API key is encrypted the first time the agent runs.

8.  To ensure that the configuration file points to a valid endpoint, run the following commands to restart the Agent Client Collector:

    ```
    sudo launchctl unload -w /Library/LaunchDaemons/com.sn.acc.plist
    sudo launchctl load -w /Library/LaunchDaemons/com.sn.acc.plist
    ```

    **Note:** By default, exiting the installation program causes the program to restart immediately. To ensure that the program remains stopped after exiting, set the KeepAlive property in the `/Library/LaunchDaemons/com.sn.acc.plist` file to **false**.


**Parent Topic:**[Agent Client Collector installation on macOS system](../concept/acc-install-mac-os.md)

