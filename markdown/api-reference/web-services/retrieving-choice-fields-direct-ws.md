---
title: Retrieve choice fields using direct web services
description: To retrieve or set choice fields, use the choice Value, not the Label.
locale: en-US
release: xanadu
product: Web Services
classification: web-services
topic_type: concept
last_updated: "2024-08-01"
reading_time_minutes: 1
breadcrumb: [Direct web services, SOAP web service, Inbound web services, Web services, API implementation, API implementation and reference]
---

# Retrieve choice fields using direct web services

To retrieve or set choice fields, use the choice **Value**, not the **Label**.

For example, if you want to retrieve a list of all closed incidents, use the numerical value for **Closed**, which is **7** by default.

```
<state>7</state>
```

To see a list of choice values:

1.  Navigate to the form containing the choice field. For example, navigate to **Incident &gt; Open** and select an incident.
2.  Right-click the choice value field and select **Configure Dictionary**. For example, configure the dictionary for the **State** field.
3.  From the Choices related list, note the value for the label you want to query. For example, note that the **Closed** choice has a value of **7**.

![incident stat value](../image/Choice_values.png)

**Parent Topic:**[Direct web services](c_DirectWebServices.md)

**Related topics**  


[Use forms to limit or extend the query response](using-forms-limit-extend-query-resp.md)

[Return the display value for reference variables](return-display-reference-variables.md)

[Clear values from a target instance](clearing-values-target.md)

[Retrieve journal entries using direct web services](retrieving-journal-entries.md)

[Persist an HTTP session across all SOAP calls](persist-session-all-soap-calls.md)

[SOAP direct web service API functions](../../web-services-apis/reference/r_DirectWebServiceAPIFunctions.md)

