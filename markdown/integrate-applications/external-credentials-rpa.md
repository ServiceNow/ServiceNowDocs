---
title: External credential vault in RPA Hub
description: With the external credential vault feature, you can retrieve robot credentials, application credentials, or Time-based One-time Password \(TOTP\) seed.
locale: en-US
release: australia
topic_type: concept
last_updated: "2026-03-12"
reading_time_minutes: 3
breadcrumb: [Credential Management, Use, RPA Hub, Workflow Data Fabric]
---

# External credential vault in RPA Hub

With the external credential vault feature, you can retrieve robot credentials, application credentials, or Time-based One-time Password \(TOTP\) seed.

## External credential vault integration with RPA Hub

The following diagram shows the integration of an external credential vault with RPA Hub.

A robot resides in the customers' environment. If the robot requires sensitive data during the automation execution, then the robot makes a GraphQL Application Programming Interface \(API\) call to the RPA Hub. An example of the sensitive data is user name and password details while logging in to an SAP application.

Based on the input provided in the **External Credential** check box, either on a robot credential form, an application credential form, or a TOTP authenticator form:

-   If the input is false \(if the check box isn’t selected\), the credentials are saved or retrieved from the instance.
-   If the input is true \(if the check box is selected in the robot credential form, an application credential form\), the credentials are fetched from a configured external credential vault. If the check box is selected in the TOTP authenticator form, the seed is fetched from a configured external credential vault.

For more information about configuring these fields, see [Create a robot credential in RPA Hub](../task/create-credential-set-botprocess.md), [Create an application credential in RPA Hub](../task/create-application-credential.md), and [Create a TOTP authenticator in RPA Hub](../task/map-totp-credential-set-rpa.md).

Examples of an external credential vault are CyberArk, Azure key Vault, and so on.

If the **External Credential** check box isn’t enabled, the API returns the data stored in the **Password2** field of the ServiceNow instance and then the robot uses the sensitive data for the automation execution.

If the **External Credential** check box is enabled, the credentials are fetched from a configured external credential vault. In this scenario, the API internally triggers a subflow. This subflow makes a REST API call to the external credential vault. You can route this REST API call via MID Server. Or, you can directly establish a connection with the external credential vault. This implementation is dependent on your organizational requirements. The MID Server resides in the customers' environment. For more information about MID Server, see [MID Server](https://www.servicenow.com/docs/access?context=mid-server-landing&version=australia&pubname=australia-servicenow-platform&ft:locale=en-US).

After the REST API call fetches the credential from the vault, the credentials are sent to the robot.

![Integration of external credential vault with RPA Hub.](../image/ext-cred-integration-rpa.png "Integration of external credential vault with RPA Hub")

## Important information

You must configure the external credential settings appropriately, so that the data isn’t stored or logged in the ServiceNow instance.

Verify that the value of the **Reporting** field is set to **Off** for the subflow of your external credential vault, for example **Demo CyberArk Subflow**. This setting verifies that the sensitive data isn’t captured or logged. For more information about configuring this setting, see [Activate flow reporting](https://www.servicenow.com/docs/access?context=enable-flow-reporting&version=australia&pubname=australia-build-workflows&ft:locale=en-US).

To configure the external credential vault in RPA Hub, see [Steps to configure an external credential vault in RPA Hub](../reference/config-ext-cred-rpa.md).

Outbound request logging enables you to understand what third party services your instance accesses and the volume of outbound requests. Additionally, logging can provide valuable information when debugging outbound integrations. For more information about system logging or outbound logging, see [Configure outbound logging](https://www.servicenow.com/docs/access?context=outbound-logging-configure&version=australia&pubname=australia-api-reference&ft:locale=en-US) and [Outbound web service logging properties](https://www.servicenow.com/docs/access?context=outbound-logging-properties&version=australia&pubname=australia-api-reference&ft:locale=en-US).

