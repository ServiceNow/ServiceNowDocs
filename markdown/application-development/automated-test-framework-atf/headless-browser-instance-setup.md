---
title: Set up instance for Headless Browser in Linux
description: Step 5 in the Linux setup for the ServiceNow Headless Browser for ATF: Set up your instance so it can support the Headless Browser.
locale: en-US
release: xanadu
product: Automated Test Framework \(ATF\)
classification: automated-test-framework-atf
topic_type: task
last_updated: "2024-08-01"
reading_time_minutes: 3
breadcrumb: [Headless Browser setup for Linux, Headless Browser for Automated Test Framework, Test your apps with the ATF, Testing and debugging applications, Building applications]
---

# Set up instance for Headless Browser in Linux

Step 5 in the Linux setup for the ServiceNow® Headless Browser for ATF: Set up your instance so it can support the Headless Browser.

## Before you begin

Complete Step 5: [Add secrets to Docker for Headless Browser setup in Linux](headless-browser-add-secrets-docker.md)

Role required: admin on your ServiceNow instance and local administrator on the host machine.

This task: Set up the instance so that it successfully communicates and authenticates with the host machine.

## Procedure

1.  Create user:

    1.  Navigate to **User Administration** &gt; **Users** and select **New**.
    2.  Create a user - User ID, which can be whatever you want, as well as a user name and password. The password should be the same as the one you created for your Docker Secret container.
    3.  Add the role **atf\_test\_designer** for this user. \(To learn more, see the User Roles section in the [Test your apps with the ATF](../concept/automated-test-framework.md) topic.\)
2.  Create certificate:

    1.  Navigate to **System Definition** &gt; **Certificates** to open the **sys\_ certificate** table. Create a new certificate \(the name can be whatever you prefer\):
        -   **Type**: Java Key Store
        -   **Password**: Password for the keystore that you created in Step 1 \([Generate certificates for Headless Browser setup for Linux](headless-browser-certificates.md)\).
    2.  Select the Attach \(paper clip\) icon to attach the keystore file you saved earlier to this record.
    3.  Select **Submit**.
    4.  Click **Validate certificate** and confirm that the success message displays.
3.  Create protocol profile:

    1.  Navigate to **System Security** &gt; **Protocol Profiles** to open the **sys\_protocol\_profile** table. Create a new protocol profile record:

        |Option|Description|
        |------|-----------|
        |Protocol|One word, lowercase: “docker”|
        |Default port|2376 \(or the one you chose to use\)|
        |Keystore|Docker host keystore|

    2.  Select **Submit**.
4.  Create a Docker spoke connection:

    1.  Navigate to **Connections &amp; Credentials** &gt; **Connection &amp; Credential Aliases** to open the **sys\_alias** table.
    2.  Select the alias with the name **Docker**.
    3.  Under the Connections related list, select **New**.
    4.  Fill in these fields:
        -   **Name**: Any text you prefer
        -   **Credential field**: Leave blank
    5.  Select the **URL Builder** check box.
    6.  Select the **Mutual authentication** check box.
    7.  In the **Protocol profile** field, select the protocol profile you created earlier.
    8.  In the **Host** field, add the IP address or Host name of your server.
    9.  Select **Submit**.
    The Connection URL is automatically created by the system.

5.  Modify properties:

    **Warning:** By default, the **com.glide.communications.trustmanager\_trust\_all** property is set to **false**. The ServiceNow AI Platform trusts only certificates that it can verify against the JVM certificate store. Self-signed and enterprise-signed certificates are not trusted.

    You need to do this only when using self-signed certificates. To learn more, see [Generate certificates for Headless Browser setup for Linux](headless-browser-certificates.md).

    -   `com.glide.communications.httpclient.verify_hostname`: false
    -   `com.glide.communications.trustmanager_trust_all`: true

**Parent Topic:**[Headless Browser setup for Linux](../concept/headless-browser-procedure-linux.md)

**Previous topic:**[Add secrets to Docker for Headless Browser setup in Linux](headless-browser-add-secrets-docker.md)

**Next topic:**[Configure ATF for Headless Browser in Linux](headless-browser-configure-atf.md)

