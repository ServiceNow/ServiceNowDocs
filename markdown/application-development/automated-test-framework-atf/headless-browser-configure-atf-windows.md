---
title: Configure Automated Test Framework \(ATF\) for Headless Browser in Microsoft Windows
description: Step 7 in the Microsoft Windows setup for the ServiceNow Headless Browser for ATF: Configure ATF with properties.
locale: en-US
release: zurich
product: Automated Test Framework \(ATF\)
classification: automated-test-framework-atf
topic_type: task
last_updated: "2025-07-31"
reading_time_minutes: 2
breadcrumb: [Headless Browser setup for Microsoft Windows, Headless Browser, Automated Test Framework \(ATF\), Testing and debugging applications, Building applications]
---

# Configure Automated Test Framework \(ATF\) for Headless Browser in Microsoft Windows

Step 7 in the Microsoft Windows setup for the ServiceNow® Headless Browser for ATF: Configure ATF with properties.

## Before you begin

Complete Step 6: [Set up instance for Headless Browser in Microsoft Windows](headless-browser-instance-setup-windows.md)

Role required: admin on your ServiceNow instance and local administrator on the host machine.

Now that your connection and authentication are set up, you will configure ATF with several properties so that it can start containers successfully on the host machine.

## Procedure

1.  In your instance, navigate to **ATF** &gt; **Administration** &gt; **Properties**.

2.  Enable the top two properties: **Enable test/test suite execution** and **Enable scheduled test suite execution**.

3.  Scroll down to the **Headless Runner Properties** section.

4.  Enable the top check box.

5.  Enter the following values in the Headless Runner Properties form:

<table id="table_xzf_wtf_mqb"><thead><tr><th>

Form Label

</th><th>

Property Name

</th><th>

Value to Imput

</th></tr></thead><tbody><tr><td>

The user account used to login from the headless Client Test Runner and begin the tests

</td><td>

sn\_atf.headless.username

</td><td>

Username of the integration user that you created in [Add secrets to Docker for Headless Browser setup in Microsoft Windows](headless-browser-add-secrets-docker-windows.md)

</td></tr><tr><td>

The Docker secret ID that has the password stored of the user account

</td><td>

sn\_atf.headless.secret\_id

</td><td>

Docker “secret ID” that you obtained earlier, as well as the Docker secret name that you created in Step 2 of the [Add secrets to Docker for Headless Browser setup in Microsoft Windows](headless-browser-add-secrets-docker-windows.md) procedure.

</td></tr><tr><td>

The Docker image that is used for headless Client Test Runner

</td><td>

sn\_atf.headless.docker\_image\_name

</td><td>

Image name with tag that you downloaded: `ghcr.io/servicenow/atf-headless-runner:<tagname>`

</td></tr></tbody>
</table>    **Note:** If you forgot the secret ID, go to Windows host and run the command docker secret list.

6.  At the **The absolute path of the secret file on a docker container** field, enter: `C:\ProgramData\Docker\secrets\<YOUR SECRET NAME>`

7.  Leave the rest of the fields as they are.

8.  Select **Save**.


**Parent Topic:**[Headless Browser setup for Microsoft Windows](../concept/headless-browser-procedure-windows.md)

**Previous topic:**[Set up instance for Headless Browser in Microsoft Windows](headless-browser-instance-setup-windows.md)

**Next topic:**[Verify Headless Browser procedures for ATF in Microsoft Windows](headless-browser-verify-tests-windows.md)

