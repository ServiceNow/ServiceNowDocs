---
title: Use a service reference in a C Sharp integration
description: Use a wizard to add a service reference for a C Sharp integration.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/zurich/api-reference/web-services/c\_UseAServiceReference.html
release: zurich
product: Web Services
classification: web-services
topic_type: concept
last_updated: "2025-07-31"
reading_time_minutes: 1
breadcrumb: [Call a web service, .NET tutorial, Examples, Inbound, Web services, API implementation, API implementation and reference]
---

# Use a service reference in a C Sharp integration

Use a wizard to add a service reference for a C Sharp integration.

Go to the **Solutions Explorer** and select **Service References** &gt; **Add Service Reference**. A wizard will appear asking for an address. Use: https://&lt;instance name&gt;.service-now.com/incident.do?WSDL. Accept the defaults for the rest of the wizard.

Open the app.config file and change the Security mode to "Transport" and the clientCredentialType and proxyCredentialType to "Basic"

\[Omitted image "DotNetAppConfig.png"\] Alt text:

**Parent Topic:**[Call a web service in visual studio .NET](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/api-reference/web-services/c_CallAWebServiceInVisualStudioNET.md)

