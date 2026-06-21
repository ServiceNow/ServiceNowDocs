---
title: Configure ATF for Headless Browser in Linux
description: Step 6 in the Linux setup for the ServiceNow Headless Browser for ATF: Configure ATF with properties.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/xanadu/application-development/automated-test-framework-atf/headless-browser-configure-atf.html
release: xanadu
product: Automated Test Framework \(ATF\)
classification: automated-test-framework-atf
topic_type: task
last_updated: "2024-08-01"
reading_time_minutes: 2
breadcrumb: [Headless Browser setup for Linux, Headless Browser for Automated Test Framework, Test your apps with the ATF, Testing and debugging applications, Building applications]
---

# Configure ATF for Headless Browser in Linux

Step 6 in the Linux setup for the ServiceNow® Headless Browser for ATF: Configure ATF with properties.

## Before you begin

Complete Step 5: [Set up instance for Headless Browser in Linux](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/xanadu/markdown/xanadu/application-development/automated-test-framework-atf/headless-browser-instance-setup.md)

Role required: admin on your ServiceNow instance and local administrator on the host machine.

This task: Now that you've set up your connection and authentication, configure ATF with several properties so that it can start containers successfully on the host machine.

## Procedure

1.  In your instance, navigate to **ATF** &gt; **Administration** &gt; **Properties**.

2.  Enable the top two properties: **Enable test/test suite execution** and **Enable scheduled test suite execution**.

    \[Omitted image "properties-enabled-two.png"\] Alt text: Top two properties enabled in ATF Administration section

3.  Scroll down to the **Headless Runner Properties** section.

4.  Enable the top check box.

    \[Omitted image "enable-test-runner-box.png"\] Alt text: Top check box enabled in Headless Runner Properties section

5.  Enter the following values in the Headless Runner Properties form:

<table id="table_xzf_wtf_mqb"><thead><tr><th>

Form Label

</th><th>

Property Name

</th><th>

Value to Imput

</th></tr></thead><tbody><tr><td>

The user account used to login from the headless client test runner and begin the tests

</td><td>

sn\_atf.headless.username

</td><td>

Username of the integration user that you created in [Add secrets to Docker for Headless Browser setup in Linux](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/xanadu/markdown/xanadu/application-development/automated-test-framework-atf/headless-browser-add-secrets-docker.md)

</td></tr><tr><td>

The Docker secret ID that has the password stored of the user account

</td><td>

sn\_atf.headless.secret\_id

</td><td>

Docker “Secret ID” that you obtained earlier, as well as the Docker secret name that you created in Step 2 of the [Add secrets to Docker for Headless Browser setup in Linux](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/xanadu/markdown/xanadu/application-development/automated-test-framework-atf/headless-browser-add-secrets-docker.md) procedure.

</td></tr><tr><td>

The Docker image that is used for headless Client Test Runner

</td><td>

sn\_atf.headless.docker\_image\_name

</td><td>

Image name with tag that you downloaded: `ghcr.io/servicenow/atf-headless-runner:<tagname>`

</td></tr></tbody>
</table>    **Note:** If you forgot the secret ID, go to the Docker host and run the command `docker secret list`

6.  Leave the rest of the fields as they are.

7.  Select **Save**.


**Parent Topic:**[Headless Browser setup for Linux](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/xanadu/markdown/xanadu/application-development/automated-test-framework-atf/headless-browser-procedure-linux.md)

**Previous topic:**[Set up instance for Headless Browser in Linux](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/xanadu/markdown/xanadu/application-development/automated-test-framework-atf/headless-browser-instance-setup.md)

**Next topic:**[Verify Headless Browser procedures in Linux](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/xanadu/markdown/xanadu/application-development/automated-test-framework-atf/headless-browser-verify-tests.md)

