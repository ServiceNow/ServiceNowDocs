---
title: Variable substitution in outbound SOAP
description: To use variable substitution, use the format $\{&lt;variable\_name&gt;\} instead of defining a specific value.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/zurich/api-reference/web-services/c\_VariableSubstitutionSOAP.html
release: zurich
product: Web Services
classification: web-services
topic_type: concept
last_updated: "2025-07-31"
reading_time_minutes: 1
breadcrumb: [Messages, SOAP, Outbound, Web services, API implementation, API implementation and reference]
---

# Variable substitution in outbound SOAP

To use variable substitution, use the format `${<variable_name>}` instead of defining a specific value.

```
...
<short_description xsi:type="xsd:string">${short_desc}</short_description>
...
```

To test variable substitution after you have modified the SOAP envelope with the variables, define values for the variables in the SOAP Message Parameters related list of the SOAP Message Function. For example, click **New** and enter the following information:

\[Omitted image "SoapMessageParameters.png"\] Alt text:

**Parent Topic:**[SOAP message](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/api-reference/web-services/c_SOAPMessage.md)

