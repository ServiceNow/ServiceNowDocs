---
title: Managing shipments by integrating with third-party carrier applications
description: You can check the status of your shipments in real time by integrating your ServiceNow instance with a third-party carrier application using the integration framework provided by the IT Asset Management application.
locale: en-US
release: australia
product: Hardware Asset Management
classification: hardware-asset-management
topic_type: concept
last_updated: "2026-03-12"
reading_time_minutes: 1
breadcrumb: [Exploring Hardware Asset Management, Hardware Asset Management, IT Asset Management]
---

# Managing shipments by integrating with third-party carrier applications

You can check the status of your shipments in real time by integrating your ServiceNow instance with a third-party carrier application using the integration framework provided by the IT Asset Management application.

![Third-party carrier integration workflow](../image/itam-carrier-integration.png)

## Requirements for integration with third-party carrier applications

**Important:** The IT Asset Management application provides only the integration framework to integrate with your third-party carrier applications. For the integration to work seamlessly, the implementation team must take care of the following requirements.

1.  Create a script include that extends from the base class `ITAMShipmentIntegration` script.

    For more details, see [Creating an integration script include for third-party carrier applications](creating-integration-script-include-ham.md).

2.  If you’re using any credentials, then use the Credential table or any table with Password2 fields and provide the KMF access map policy to enable your customers to access your application.

    For more details, see [Password2 encryption with the Key Management Framework \(KMF\)](https://www.servicenow.com/docs/access?context=password-2way-encrypted-fields&version=australia&pubname=australia-platform-security&ft:locale=en-US).

3.  Add the application name, API, and connection details to the Carrier integration profile \[sn\_itam\_carrier\_int\_profile\] table.

    For more details, see [View the carrier integration profile details](../task/view-integration-profiles.md).


**Note:** If you are creating the integration as part of an application, complete the following steps before you create a script include:

1.  Create an application.
2.  Make the application accessible from any application that belongs to a different scope. For more details, see [Creating an integration script include for third-party carrier applications](creating-integration-script-include-ham.md).

For more details, see [Track shipments using the integration framework](tracking-shipments-using-integration-framework.md).

