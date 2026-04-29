---
title: Use a service reference in a C Sharp integration
description: Use a wizard to add a service reference for a C Sharp integration.
locale: en-US
release: australia
product: Web Services
classification: web-services
topic_type: concept
last_updated: "2026-03-12"
reading_time_minutes: 1
breadcrumb: [Call a web service, .NET tutorial, Examples, Inbound, Web services, API implementation, API implementation and reference]
---

# Use a service reference in a C Sharp integration

Use a wizard to add a service reference for a C Sharp integration.

Go to the **Solutions Explorer** and select **Service References** &gt; **Add Service Reference**. A wizard will appear asking for an address. Use: https://&lt;instance name&gt;.service-now.com/incident.do?WSDL. Accept the defaults for the rest of the wizard.

Open the app.config file and change the Security mode to "Transport" and the clientCredentialType and proxyCredentialType to "Basic"

![](../image/DotNetAppConfig.png "Dot net app config")

**Parent Topic:**[Call a web service in visual studio .NET](c_CallAWebServiceInVisualStudioNET.md)

