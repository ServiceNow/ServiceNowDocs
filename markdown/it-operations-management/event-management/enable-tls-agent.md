---
title: Connect the agent to the MID Server using mTLS
description: Before configuring mTLS authentication on the agent, you must run a series of commands that enable configuring Transport Layer Security \(TLS\) authentication.
locale: en-US
release: zurich
product: Event Management
classification: event-management
topic_type: task
last_updated: "2025-07-31"
reading_time_minutes: 2
breadcrumb: [MID Web Server and agent mTLS Authentication, Configure the MID Web Server extension, MID Web Server, Event Management setup, Configuring Event Management, Event Management, ITOM AIOps, IT Operations Management]
---

# Connect the agent to the MID Server using mTLS

Before configuring mTLS authentication on the agent, you must run a series of commands that enable configuring Transport Layer Security \(TLS\) authentication.

## Before you begin

Ensure that you have performed the following tasks:

1.  [Create keys and certificates](create-keys-and-certificates.md)
2.  [Install the .pem file in the MID unified keystore and set up the MID Web Server](set-mid-web-server.md)
3.  [Connect the agent to the MID Web Server using TLS](agent-mid-connect.md)
4.  [Configure mTLS authentication for a MID Web Server](../../event-management/task/configure-mid-web-server-extension-mTLS.md)
5.  [Connect the agent to the MID Server using mTLS](enable-tls-agent.md)

Role required: agent\_client\_collector\_admin

## Procedure

1.  Generate a key for your agent.

    ```
    openssl ecparam -out labacc/acc.key -name prime256v1 -genkey
    ```

2.  Generate a certificate request for your agent, according to the following format:

    ```
    openssl req -new -key labacc/acc.key -out labacc/acc.csr -subj "/C=<country>/ST=<state>/L=<location>/O=<organization>/OU=<organization unit>/CN=<cn abbreviation>/emailAddress=<email address>"
    ```

    For example:

    ```
    openssl req -new -key labacc/acc.key -out labacc/acc.csr -subj "/C=US/ST=NC/L=Raleigh/O=ServiceNow/OU=ITOM Lab/CN=acclinux/emailAddress=john.smith@servicenow.com"
    ```

3.  Generate a signed certificate for your agent.

    ```
    openssl x509 -req -days 365 -in labacc/acc.csr -CA labca/labcacert.pem -CAkey labca/ec-labcakey.pem -CAcreateserial -extensions client -out labacc/acc.crt
    ```

4.  In the `labacc` folder, copy your key and certificate files to the agent host's virtual machine.

    ```
    cp ./acc.key <agent host config folder>
    cp ./acc.crt <agent host config folder>
    ```

    The configuration folder paths depend on your OS.

    -   Linux: `/etc/servicenow/agent-client-collector/`
    -   Windows: `C:\ProgramData\servicenow\agent-client-collector\config\`
    -   macOS: `/Library/Application\ Support/servicenow/agent-client-collector/`
5.  Navigate to the location where you copied the `.key` and `.crt` files from.

6.  Run the following commands to update the files' read permissions and enable the agent to read from them.

    -   Linux:
        1.  `chown servicenow:servicenow acc.key`
        2.  `chmod 0400 acc.key`
    -   Windows:
        1.  Select and hold \(or right-click\) the `.key` file and select the **Security** tab from the file properties.
        2.  Add the **servicenow** user to the list of users with read access to the file.
    -   macOS:
        1.  `chown _servicenow:_servicenow acc.key`
        2.  `chmod 0400 acc.key`
    **Note:** The agent must be run with the default servicenow user.

7.  In the acc.yml configuration file, add the following parameters to specify the path to your key and certificate files.

    ```
    key-file: "<path to acc.key file>/acc.key"
    cert-file: "<path to acc.cert file>/acc.crt"
    ```

8.  Restart the agent.

    -   Linux: `systemctl restart acc`
    -   Windows:
        1.  Open the Services application.
        2.  Select and hold \(or right-click\) the Agent Client Collector entry and select **Restart**.
    -   macOS:
        1.  `launchctl unload -w /Library/LaunchDaemons/com.sn.acc.plist`
        2.  `launchctl load -w /Library/LaunchDaemons/com.sn.acc.plist`
9.  Check the logs to verify that the agent was able to connect to the instance using TLS.

    Agent Client Collector logs are accessible from:

    -   Linux: `/var/log/servicenow/agent-client-collector/acc.log`
    -   Windows: The location specified by the `log-file` configuration flag. The default location is: `C:/ProgramData/ServiceNow/agent-client-collector/log/acc.log`

        If the `C:/ProgramData` directory is hidden \(such as on older Windows versions\), change the Explorer filter to show hidden elements.

    -   macOS: The default location is: `/Library/Application\ Support/servicenow/agent-client-collector/log/acc.log`

**Related topics**  


[MID Web Server and agent mTLS Authentication](../../event-management/concept/mid-web-server-mTLS-authentication.md)

