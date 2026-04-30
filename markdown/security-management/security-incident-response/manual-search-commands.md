---
title: Manual search commands
description: Manual search commands are entered from any Search window. You can create a security incident or event. After the command, there are pairs of field names and values used to create the desired record.The security event command, snsecevent, creates an event in ServiceNow with the Security classification.The Security Incident command, snsecincident, creates a Security Incident in your ServiceNow instance.
locale: en-US
release: xanadu
product: Security Incident Response
classification: security-incident-response
topic_type: concept
last_updated: "2024-08-01"
reading_time_minutes: 2
breadcrumb: [ServiceNow Security Operations add-on for Splunk overview, Security Incident Response integrations, Security Incident Response, Enterprise security case management applications, Security Operations]
---

# Manual search commands

Manual search commands are entered from any Search window. You can create a security incident or event. After the command, there are pairs of field names and values used to create the desired record.

## Security event

The security event command, **snsecevent**, creates an event in ServiceNow with the Security classification.

These events can be reviewed on their own, or alert rules within ServiceNow or manual actions can turn an event or collection of events into a security incident.

If the event becomes a security incident and each parameter is sent into the event, this data is used to populate the security incident as follows:

|Parameter Name|Required|Use|Use in Security Incident|
|--------------|--------|---|------------------------|
|node|Yes|The node represents the server or configuration item for the event. Ideally, this node maps to an existing CI within ServiceNow.|Use in Security Incident|
|type|Yes|The category of event.|Short description|
|resource|Yes|The configuration item.|Short description|
|source|No|The origination of this data. By default, the Splunk server generates the data.|Activity log|
|external\_url|No|The drilldown URL to use in ServiceNow to get back to the Splunk data regarding this event. By default, this URL contains the result link for any alert, or a link to the default Splunk search page.|External URL accessed via the **Drilldown** button on the Security Incident form|
|time\_of\_event|No|The time that the event was logged in Splunk.|N/A|
|All other values \(category, subcategory in the example\)|No|Any field that is not part of the information field in the event. If a security incident is created, it is used.|If the field exists, and is not populated, the security incident uses that value. For example, the category passed through the Event becomes the category of the new security incident. If a field with this name does not exist, the value is placed in the activity log.|

## Security incident

The Security Incident command, **snsecincident**, creates a Security Incident in your ServiceNow instance.

|Parameter|Required|Use|
|---------|--------|---|
|short\_description|Yes|A short, one line description of the incident.|
|category|No|The category of the security incident. If this category does not exist, it is created.|
|subcategory|No|The subcategory. If this subcategory does not exist, it is created.|
|cmdb\_ci|No|The configuration item for the security incident. Ideally, this item maps to an existing CI within ServiceNow.|
|description|No|The longer, detailed description of the incident.|

There are many possible useful columns – anything in the Security Incident transform map can be used. If new columns are added to the security incident, they too are used, as long as they are in the transform map. Some useful columns: location, priority, assignment\_group, assigned\_to, affected\_user, attack\_vector, and watch\_list.

