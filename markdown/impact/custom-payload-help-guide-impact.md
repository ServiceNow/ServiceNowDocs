---
title: Custom payload in alerts integration
description: Instance Observer integrations allow you to define and manage custom JSON request payload for ServiceNow and third-party integrations.
locale: en-US
release: yokohama
topic_type: reference
last_updated: "2025-04-21"
reading_time_minutes: 2
breadcrumb: [Alerts in Instance Observer, Impact Instance Observer, Platform Health, Impact Delivery Instance \(formerly Impact Digital Experience\), Impact]
---

# Custom payload in alerts integration

Instance Observer integrations allow you to define and manage custom JSON request payload for ServiceNow and third-party integrations.

You can now include additional fields in notification payloads, exclude specific data that is not required by the target system, format the payload to align with specific third-party API requirements or internal business logic, eliminating the need for complex scripted REST APIs on the customer side.

-   Use either the default payload or customize it to include additional data as needed.
-   Modify the default payload, if needed, which is displayed in the Editor window on the left.
-   Modify either the key or the value, or both as each parameter consists of a key and a value.
-   The Preview section on the right displays the expected JSON payload after rendering.
-   If the JSON is invalid, errors are highlighted, and the option to save is disabled.

## Default mustache payload template

```
{
  "alert_number": "{{alert_number}}",
  "alert_type": "{{alert_type}}",
  "alert_name": "{{alert_name}}",
  "alert_time": "{{alert_time}}",
  "instance": "{{instance}}",
  "description": "{{description}}",
  "alert_created": "{{alert_created}}"
}

```

![Edit payload for default mustache payload template.](../image/io-default-mustache-payload.png)

## Example: Default Payload + Custom Parameters

```
{
"alert_number": "{{alert_number}}",
  "alert_type": "{{alert_type}}",
  "alert_name": "{{alert_name}}",
  "alert_time": "{{alert_time}}",
  "instance": "{{instance}}",
  "description": "{{description}}",
  "alert_created": "{{alert_created}}",
  "Custom_message": "{{alert_name}}' of type {{alert_type}} generated for {{instance}} at {{alert_time}}. Please review.",
  "Severity": “High”
}

```

![Edit payload for default payload + custom parameters.](../image/io-default-payload-cust-param.png)

## Custom parameters and limits

The **custom\_parameter** field allows you to insert custom message into the JSON template, you can also use the existing parameters as shown in the custom parameter samples.

The limitations are:

-   Required: At least one and at most 20 parameters to save the template.
-   Maximum: 13 custom parameters.
-   If exceeded, a warning appears: `Template must have at least one default key and up to 20 keys. Adjust or select 'Reset to Default' to apply defaults.`

## Samples of custom parameters for syntax reference

"Information": "An alert \{\{alert\_name\}\} has been triggered for \{\{instance\}\} at \{\{alert\_time\}\} Description: \{\{description\}\}"

"Alert\_message": "New alert '\{\{alert\_name\}\}' of type \{\{alert\_type\}\} generated for \{\{instance\}\} at \{\{alert\_time\}\}. Please review."

"Event\_type": "Severity-High! An alert \{\{alert\_name\}\} has been triggered for \{\{instance\}\} at \{\{alert\_time\}\} Description: \{\{description\}\}"

## Third-party request body mapping

Some third-party integrations require specific key names. You can modify the default payload to match their expected format.

Example: Third-party request body:

```
{
  "endTime": 1,
  "entitySelector": "string",
  "eventType": "AVAILABILITY_EVENT",
  "properties": {},
  "startTime": 1,
  "timeout": 1,
  "title": "string"
}

```

## Modified IO payload to match third-party format

![Modified IO payload to match third-party format.](../image/io-modified-io-payload.png)

## Actions and validation

-   **Revert Changes**

    Restores the last saved content.

-   **Reset to Default**

    Resets the template to its default payload.

-   **Syntax Validator**

    Ensures JSON validity before saving. Errors prevent saving.

-   **Test Integration**

    Sends a sample notification to verify webhook integration.


