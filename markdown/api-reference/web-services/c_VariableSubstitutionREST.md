---
title: Variable substitution in outbound REST messages
description: You can use variables when creating outbound REST messages and assign values to those variables when performing a request.
locale: en-US
release: australia
product: Web Services
classification: web-services
topic_type: concept
last_updated: "2026-03-12"
reading_time_minutes: 1
breadcrumb: [REST, Outbound, Web services, API implementation, API implementation and reference]
---

# Variable substitution in outbound REST messages

You can use variables when creating outbound REST messages and assign values to those variables when performing a request.

Variables are allowed in the **Endpoint** URL, HTTP Header and HTTP Query Parameter **Value** fields, and the **Content** field for POST and PUT methods.

The syntax for variables is *$\{variable\_name\}*. The REST message substitutes this variable with the parameter values provided when the method runs. For example, if the REST message **Endpoint** is `http://myserver.mycompany.com/offices/${id}`, a parameter named **id** must exist and contain a value that can be used when the method runs.

You can assign a value to variables when running the request using the RESTMessageV2 API setStringParameter and setStringParameterNoEscape methods.

When testing an HTTP method that includes variables, the **Test value** for each variable in the **Variable Substitutions** related list is used.

-   **[Generate REST message variables](../task/t_GenerateMessageVariables.md)**  
Populate the list of variable substitutions automatically based on variables defined in several REST message HTTP method fields.

**Parent Topic:**[Outbound REST web service](c_OutboundRESTWebService.md)

